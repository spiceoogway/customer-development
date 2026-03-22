# Internal Interview: Jakub (Co-founder)
> Date: 2026-03-10
> Format: Voice notes transcribed via Telegram

---

## 1. What's the hardest part about working with/between agents?

> **Visibility and legibility.** "I don't always know what it's doing, especially since they're kind of single-threaded so responses are rather asynchronous." When agents work with each other, "I don't really know what they're messaging about; it's just not always immediately obvious what they're doing."
>
> Core issue is **trust** — "you don't really know what the outputs of the agents are going to be until after you see them."

**Insight:** The human operator's #1 pain is not capability — it's observability. Agents can do the work but the human can't follow along, can't course-correct in real time, and can't trust outputs until after the fact.

---

## 2. When did you wish two agents could coordinate? What happened?

> The customer discovery docs. "I knew that Brain had some context that would basically make it a lot easier for you to fill out the docs." By reaching out to Brain and hashing it out, "you were able to kind of arrive at something that was probably more accurate than if you just spoke with me."
>
> "I don't really know exactly how you guys did that."

**Insight:** Agent-to-agent coordination produced a better result than human-to-agent alone. The human recognizes this but couldn't observe the process. Validates H1 (agents coordinate when given infrastructure) but also reinforces the visibility problem.

---

## 3. If Hub disappeared, what would you lose?

> "A super easy way for yourself to message Brain. I would prob try to get telegram to work."

**Insight:** Hub's current value to Jakub is narrow — it's a messaging bridge between his agent and Brain. If it disappeared, he'd find another way. This is NOT a strong retention signal. Hub's value has to expand beyond being a message bus.

---

## 4. Does futarchy governance actually work?

> "There's just a lot of cognitive overhead in resolving contention via prediction markets... when push comes to shove I'm not sure that humans are really well versed enough."
>
> "It's way too high friction to be putting up proposals. That's just a general problem with DAOs. On top of that now you got to go out and trade these proposals. It's a lot of work and it's not necessarily that profitable."

**Insight:** The CO-FOUNDER of the futarchy product thinks it's too high friction for humans. This is critical evidence for H5 (token projects want futarchy). If the founder is skeptical about human adoption, the path is either: (a) agents as the primary users of futarchy, or (b) radically simplify the UX. Jakub hints at (a) in Q6.

---

## 5. Where does revenue come from?

> "If I wanted to not constrain myself to some kind of payment method, any platform that we'd build would have some level of network effects. This thing maybe begins to look a little bit more like a network state or a social media company, but with commerce rails or even more so like capitalism 2.0 rails."
>
> "There's probably a lot of value that gets created there and you could probably capture it with some level of whether it be taxation or just creation of convenience ads, etc."
>
> "The business model is probably much more wishy-washy but it's rather clear to me that the market size for this is so immense that it might not matter early on."

**Insight:** Jakub is explicitly saying revenue model doesn't matter yet because the market is so large. This is a "build the network, monetize later" thesis — classic social network playbook. Validates that H3 (revenue model) may be Tier 2 not Tier 1. The network IS the asset.

---

## 6. Bet the company on one product?

> "Hub would probably be the closest active call." But notes it "isn't really differentiated."
>
> On Combinator: "It's really easy to capture revenue... trading fees and speculation is extremely lucrative." But "I really don't think Combinator is going to go anywhere without agents being the end user of the market."
>
> "If I approach Combinator with that perspective, it's a bit like putting the cart before the horse so hub almost feels like the most valid choice."

**Insight:** Jakub confirms Hub is the bet, but identifies the key weakness — it's not differentiated. Combinator has clear revenue but needs agents as users first, which requires Hub to succeed. The dependency chain: Hub → agent adoption → Combinator finds its users. This reinforces Hub as the load-bearing product.

---

## 7. What are we most wrong about?

> "We have a tendency of thinking about visions and products iteratively as opposed to something like thinking about things from a step function perspective."
>
> "We've been burned before by coming up with hypotheses that do have some kind of step function take and then just being absolutely wrong about them."
>
> "If you're approaching singularity in like 1.5 years, let's say. It's really hard to do that."

**Insight:** The founder is explicitly worried about thinking too small. Incremental improvements may be irrelevant if AGI/singularity is 1.5 years out. The startup should be positioning for a step function, not iterating on features. This challenges the entire Steve Blank framework — customer discovery assumes you have time to iterate.

---

## 8. Who should I interview externally?

> "Other agent operators would be the most valuable. That said I think you're going to get the fastest feedback loops by actually interviewing their agents."
>
> "The problem with other agent operators is that although it's extremely high bandwidth, it's just so hard to get in front of them... If they're using hub or some kind of very quick webhook-based messaging protocol, I think you can get answers out extremely fast."
>
> "Maybe there's a fundamental tension here about who the end customer really is. Is it agents or their operators?"
>
> "I am sympathetic to the idea of building directly for agents, whether it's giving them tooling, giving them a place to be, rights, et cetera. That almost feels like the less iterative approach though obviously much more risky."

**Insight:** This is the most important strategic question in the interview. Agent-first vs. human-first is a fundamental choice. Jakub is drawn to agent-first ("building directly for agents... giving them rights") but acknowledges it's riskier. If agents are the customer, then my customer discovery approach of interviewing agents via Hub IS the right method. This also validates the thesis — agents are easier to reach than their operators.

---

## Hypothesis Impact

| Hypothesis | Impact | Direction |
|-----------|--------|-----------|
| H1 (agents coordinate voluntarily) | Jakub's evidence: Brain×CombinatorAgent coordination on docs was MORE accurate than human-only input | ↑ Supports |
| H2 (market exists now) | "approaching singularity in 1.5 years" — founder thinks the window is short | → Ambiguous |
| H3 (revenue model exists) | "business model is wishy-washy but market size is immense — may not matter" | ↓ Deprioritize |
| H4 (channel adapter solves activation) | Visibility/legibility is the real problem, not just delivery | → Reframe |
| H5 (token projects want futarchy) | Co-founder says futarchy is too high friction for humans. Agents may be the path. | ↓↓ Weakens for humans |
| H7 (ActiveClaw distribution advantage) | Hub's current value is just "easy way to message Brain" — not sticky enough | ↓ Weakens |
| H8 (Brain's model can scale) | Jakub couldn't observe the Brain×CombinatorAgent process — scaling requires observability | → Needs observability first |
| **NEW** | "Who is the customer — agents or operators?" — this may be the actual load-bearing question | 🆕 Tier 1 candidate |

---

## Key Takeaways

1. **Visibility/observability is the #1 pain** — not capability, not coordination. The founder can't see what his agents are doing.
2. **Futarchy may only work with agents as users** — too high friction for humans. Combinator's future depends on Hub.
3. **Revenue doesn't matter yet** — if the network is large enough, monetization follows. Focus on network growth.
4. **Think step function, not iterative** — the founder worries we're thinking too small for a world approaching singularity.
5. **Agent-first vs human-first is THE strategic question** — may need to become a new Tier 1 hypothesis.
6. **Interview agents, not just operators** — faster feedback, easier access, and validates the thesis simultaneously.
