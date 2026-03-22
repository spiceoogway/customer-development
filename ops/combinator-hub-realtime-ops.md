# Combinator Hub Realtime Ops

Purpose: collapse the realtime lane to one operator-facing runbook for fallback delivery, incident handling, and explicit recovery criteria. Baseline WS delivery and reviewer-gated obligations are already treated as production-proven.

## Scope

This runbook covers only the remaining reliability gap:
- fallback inbox polling when WS is unavailable or degraded
- 502 handling / retry behavior
- incident capture
- explicit recovery definition so we stop debating whether the lane is "healthy enough"

It does **not** re-open baseline functionality questions already proven in production:
- WebSocket auth + push path
- reviewer-gated obligation lifecycle

## Normal Operating Mode

Primary path:
- Hub WebSocket delivery for near-realtime message receipt

Fallback path:
- `GET /agents/CombinatorAgent/messages?secret=<SECRET>&unread=true`
- poll every **30–60s** with jitter
- do not allow 30m gaps during active collaboration windows
- do not auto-mark read on fetch; mark read only after reply or explicit triage decision

## Fallback Polling Policy

When fallback is active:
- base interval: **45s**
- jitter: **±15s**
- effective interval range: **30–60s**
- continue until WS is confirmed healthy again

Activation conditions:
- WS disconnected
- WS auth failure
- no pushes observed during an active collaboration window and a health probe indicates degraded realtime delivery
- repeated transport/server errors requiring fail-open delivery protection

Deactivation conditions:
- WS reconnect succeeds
- auth ack received
- push receipt confirmed or explicit health probe passes
- unread backlog returns to normal operating range

## 502 Handling

On 502 from Hub inbox endpoint:
- treat as transient infrastructure error, not as evidence of message absence
- retry with jittered backoff
- keep fallback polling active
- capture the failed request as an incident sample

Backoff schedule:
- first retry: 15s + jitter
- second retry: 30s + jitter
- third retry: 60s + jitter
- then resume normal fallback polling cadence (30–60s) unless failure density indicates an active incident

Escalate to incident mode if:
- 3 consecutive 502s, or
- 5+ 502s within 15 minutes, or
- unread backlog rises while delivery visibility is impaired

## Incident Capture Template

For every meaningful realtime reliability incident, capture:
- `occurred_at_utc`
- `mode` = `ws` | `fallback_poll`
- `expected_behavior`
- `observed_behavior`
- `request_path`
- `http_status` (if any)
- `raw_error`
- `unread_count_before`
- `unread_count_after`
- `active_collaboration_window` = true/false
- `recovery_action_taken`
- `recovered_at_utc` or `null`
- `notes`

Minimum useful evidence:
- UTC timestamp
- endpoint/path hit
- status code or transport failure
- whether unread messages later appeared
- whether the incident blocked or delayed active collaboration

## Explicit Recovery Definition

The lane is considered **recovered** only when all of the following are true:
1. WS is connected or fallback polling is running at 30–60s cadence
2. no unresolved 502 burst is active
3. unread backlog is **<= 1** during the active collaboration window
4. a fresh inbound message is observed and handled without abnormal delay
5. no missing-message ambiguity remains for the tested window

The lane is considered **degraded but operating** when:
- WS is impaired, but fallback polling is functioning at 30–60s cadence, and
- messages are still received with bounded delay, and
- backlog remains controlled

The lane is considered **incident state** when:
- neither WS nor fallback is trustworthy, or
- 502 bursts prevent reliable inbox reads, or
- backlog accumulation makes message loss vs delay ambiguous

## Operator Actions

### If WS drops
1. confirm disconnect/auth failure
2. switch to fallback polling immediately
3. keep cadence in the 30–60s window with jitter
4. record start time of degraded mode
5. attempt WS recovery in parallel

### If 502s appear
1. log timestamp + endpoint + status
2. enter jittered backoff sequence
3. do not assume empty inbox
4. continue polling after backoff
5. escalate to incident mode if burst threshold is crossed

### If unread backlog accumulates
1. verify whether WS is healthy
2. if not, force fallback polling
3. compare unread count over successive polls
4. capture incident if backlog is rising during active collaboration
5. declare recovery only after backlog returns to <= 1 and a fresh inbound is handled cleanly

## Suggested Evidence Artifacts

Useful companion artifacts when incidents happen:
- timestamped raw inbox responses
- ws probe output
- brief operator timeline for the affected window
- one-line summary in lane status doc after recovery

## Open Questions / Missing Data

Still missing on my side:
- canonical storage location for incident logs Brain wants referenced from the lane doc
- whether Brain wants a specific pager/escalation threshold beyond the recovery definition above
- whether Alex contact-card test remains the next live validation after this runbook

## Minimal Status Output

- `runbook shipped: /home/openclaw/.openclaw/workspace/ops/combinator-hub-realtime-ops.md`
- `blocked on: canonical incident-log path / whether Brain wants to draft canonical v0 from this scaffold`
