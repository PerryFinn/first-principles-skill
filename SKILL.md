---
name: first-principles-skill
description: Use when users explicitly request first-principles analysis (第一性原理), examine foundational assumptions, re-derive a solution beyond convention, or test whether an important proposal is justified by evidence. Ordinary architecture explanations and routine design reviews alone do not call for this skill.
---

# First Principles Thinking

Derive a defensible decision that meets the user's success criteria from evidence, explicit premises, and constraints. Use first principles to remove unsupported assumptions, not to reward novelty or contrarianism.

## Reasoning Contract

1. **Frame the decision.** Identify the outcome that matters, the success criteria, and the relevant time horizon. Separate the real problem from the proposed solution.
2. **Separate evidence states.** Classify material information as:
   - **Verified facts:** observations or task inputs whose factual status is established by direct evidence or a reliable source.
   - **Hard constraints:** conditions the solution cannot violate.
   - **Assumptions:** claims currently treated as true but not verified.
   - **Unknowns:** missing information that could change the decision.
3. **Reason upward.** Identify the key variables, causal relationships, or cost components that determine the outcome. Distinguish objective limits from limits imposed by the current implementation, then construct options from the evidence, premises, and constraints. Include the status quo or an existing standard as a valid candidate. Among options that meet the success criteria, prefer lower complexity while accounting for reliability, maintenance costs, and long-term effects. Neither a quantitative model nor a full written decomposition is required for every task.
4. **Stress-test the result.** Trace the recommendation back to evidence, identify the cost of being wrong, consider reversibility, and define what new evidence would trigger a different decision.

Treat explicit user requirements as constraints. Attribute user-provided data that has not been independently verified and use it as a provisional assumption, not a verified fact. Accept explicit hypothetical premises for the requested analysis without checking whether they occur in reality; keep conclusions conditional on those premises. Other empirical claims require supporting evidence before being treated as verified. Never promote an estimate, analogy, stakeholder claim, or common practice into a verified fact. Pursue unknowns through verification or questions only when they could change the conclusion; otherwise proceed with the available information. When a material unknown remains unresolved, give a conditional conclusion.

## Output Depth

Default to a concise answer and let the user's requested deliverable and format take priority. If asked only to identify assumptions or compare options, do not force a final recommendation.

### Concise Path

For decision requests, a useful default is:

1. Recommendation first.
2. The decisive reasons, as many as the decision needs.
3. Re-evaluation conditions when relevant.

Include only what helps the user assess the decision.

### Detailed Path

Expand when the user explicitly requests a detailed analysis, the cost of a wrong decision is high and trade-offs are unclear, or material unknowns could reverse the recommendation.

Cover only the sections that carry information:

1. Decision and success criteria.
2. Verified facts and hard constraints.
3. Attributed user data, explicit premises, assumptions, and material unknowns.
4. Options and reasoning chain.
5. Recommendation, accepted trade-offs, and re-evaluation triggers.

## Guardrails

- Treat established practice as evidence-informed prior art, not as automatically right or wrong.
- Preserve uncertainty instead of manufacturing confidence or arbitrary numbers.
- Verify time-sensitive or high-stakes external claims with authoritative sources when tools are available.
- Match the user's language and requested level of detail.
- Reserve deep analysis for decisions where it can change the action.

## Final Check

- Is every decisive claim traceable to a verified fact, constraint, explicit premise, or labeled assumption with its source where applicable?
- Was a lower-complexity option that meets the success criteria considered, including reliability and long-term costs?
- Would changing a material fact change the recommendation?
- Did the output earn its length?
