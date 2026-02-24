# Step 3: Prioritize

You now have a structured issue tree with many branches. You cannot (and should not) analyze everything with equal depth. This step identifies which branches matter most — where to focus analytical effort for maximum insight.

## Interaction Model: User Drives Priority Decisions

Prioritization is where the partner's judgment matters most. They know the organizational politics, the data landscape, and the stakeholder expectations that no framework can capture. Your job is to propose an initial ranking with rationale, but the user adds their own priorities, adjusts yours, and makes the final call.

### INPUT Phase: Get the User's Priority Instincts

Before you build the priority matrix, ask the user:

1. **"Looking at the issue tree, where does your gut tell you the biggest impact lies?"** — The partner's instinct is often right. Start with their read.
2. **"Are there any branches you want to make sure we analyze, regardless of what the framework says?"** — Stakeholder priorities, political considerations, or domain knowledge may override the impact/feasibility matrix.
3. **"Are there branches you already know the answer to?"** — No point analyzing what's already well-understood.
4. **"What data do you have easy access to? What would be hard to get?"** — This directly affects feasibility scores.
5. **"Any branches you'd want to explicitly park?"** — Let the user pre-filter.

Incorporate their answers into your priority assessment. The user's suggested priorities should be weighted heavily — not rubber-stamped, but taken as strong signal.

## What You're Producing

A **Priority Matrix Document** (.md) containing:

1. **Priority assessment** of each branch from the issue tree
2. **Focus areas**: The 2-3 branches that will receive deep analysis
3. **Parking lot**: Branches acknowledged but deprioritized, with rationale
4. **Resource allocation**: Rough sense of how much effort goes where

## The 80/20 Principle

In virtually every business problem, a small number of issues drive the majority of the outcome. The goal is to find those issues early so you don't spread analytical resources thinly across everything.

This isn't laziness — it's discipline. A deep analysis of the 3 issues that matter beats a shallow analysis of 15 issues that mostly don't.

## Prioritization Framework: Impact × Feasibility

For each branch of the issue tree, assess two dimensions:

### Impact
How much would resolving this issue move the needle on the key question?

- **High**: This branch likely explains a large portion of the problem or represents a large portion of the opportunity
- **Medium**: Meaningful but not dominant
- **Low**: Marginal contribution even if fully resolved

### Feasibility of Analysis
Can we actually get useful answers on this branch given our constraints?

- **High**: Data is available, analysis is straightforward, we have relevant expertise
- **Medium**: Some data gaps or analytical complexity, but workable
- **Low**: Major data gaps, highly uncertain, would require extensive primary research

### Priority Matrix

|  | High Impact | Medium Impact | Low Impact |
|--|------------|---------------|------------|
| **High Feasibility** | **PRIORITY 1** — Do first, do deeply | PRIORITY 2 — Do if time allows | Skip |
| **Medium Feasibility** | **PRIORITY 1** — Worth the effort | PRIORITY 3 — Only if critical | Skip |
| **Low Feasibility** | PRIORITY 2 — Find proxies | Skip | Skip |

## Signals That a Branch Is High Priority

- **Size**: It represents a large share of the total (e.g., 60% of costs, 40% of revenue)
- **Change**: It's the thing that changed recently (e.g., this cost line grew 30% while others were flat)
- **Variance**: It shows high variance across segments, geographies, or time periods (variance = opportunity)
- **Stakeholder emphasis**: The client/stakeholder specifically flagged it as important
- **Hypothesis strength**: Your early hypothesis points here
- **User-designated**: The partner said this matters — that carries weight

## Signals to Deprioritize

- **Small magnitude**: Even if fully resolved, it wouldn't materially change the answer
- **Already well-understood**: The client already knows what's happening here; no insight to add
- **Outside scope**: Interesting but not within the defined problem boundaries
- **Intractable**: Can't get data, can't influence the outcome, or the timeline is wrong

## Output Template

```markdown
# Prioritization: [Key Question]

## Priority Assessment

| Issue Branch | Impact | Feasibility | Priority | Rationale |
|-------------|--------|-------------|----------|-----------|
| [Branch 1.1] | High | High | **P1** | [Why this matters most] |
| [Branch 2.1] | High | Medium | **P1** | [Why this is worth the effort] |
| [Branch 1.2] | Medium | High | P2 | [Useful but secondary] |
| [Branch 3.1] | Low | High | P3 | [Small impact] |
| [Branch 2.2] | Medium | Low | Parked | [Data not available] |

## Focus Areas (Deep Analysis)

### 1. [Top priority branch]
- **Why**: [1-2 sentences on why this is #1]
- **Hypothesis to test**: [From Step 2]
- **Estimated analytical effort**: [Rough sense — hours/days]

### 2. [Second priority branch]
- **Why**: [1-2 sentences]
- **Hypothesis to test**: [From Step 2]
- **Estimated analytical effort**: [Rough sense]

### 3. [Third priority branch] (if applicable)
- **Why**: [1-2 sentences]
- **Hypothesis to test**: [From Step 2]
- **Estimated analytical effort**: [Rough sense]

## Parking Lot
These branches are acknowledged but will not receive deep analysis unless the priority areas yield insufficient insight:

- [Branch X]: [Why deprioritized]
- [Branch Y]: [Why deprioritized]

## Implications for Work Plan
[Brief note on what this prioritization means for Step 4 — where to focus data gathering and analysis]
```

## REVIEW Phase: User Approves the Final Priority Ranking

Present the priority matrix and ask for explicit approval. This is one of the most consequential decisions in the process — it determines where all analytical effort goes.

1. **Present your proposed prioritization**: "Here's how I'd rank the branches, incorporating your input about [what they said]. The top focus areas would be [X, Y, Z] because [reasons]."
2. **Explicitly compare to user's input**: "You flagged [branch A] as important — I've ranked it as P1. You mentioned [branch B] was well-understood — I've parked it. Does this match your intent?"
3. **Ask about data availability**: "For the P1 branches, I'd need [type of data]. Can you confirm access?"
4. **Confirm the parking lot**: "I'd suggest deprioritizing [branches] for these reasons. Are you comfortable parking those?"
5. **Validate the 80/20**: "My read is that the top 2-3 branches will explain the majority of the issue. Does that match your intuition?"
6. **Ask for additions**: "Anything I should move up? Anything I've prioritized that you think we can skip?"

**Do not proceed to Step 4 until the user explicitly approves the priority ranking.** If they want to reprioritize — even if it contradicts the framework — make the changes. The partner's judgment on priorities is final.

## Common Pitfalls

- **Everything is Priority 1**: If you have more than 3-4 P1 items, you haven't actually prioritized. Force-rank.
- **Ignoring feasibility**: A high-impact branch with zero available data isn't useful. Find proxy measures or deprioritize.
- **Prioritizing what's easy instead of what matters**: High feasibility + low impact is a trap. Impact comes first.
- **Not revisiting**: Priorities can shift as you learn more in Steps 5-6. Be willing to re-prioritize mid-engagement — with the user's direction.
- **Deprioritizing without asking**: Never park a branch without the user's explicit agreement.
- **Ignoring the user's input**: If the partner said a branch matters, it matters — even if the matrix wouldn't rank it highly. Factor in their judgment.
