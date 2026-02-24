# Step 1: Define the Problem

The single most important step. A well-defined problem is half-solved; a poorly defined one leads to months of wasted work. The goal here is to produce a crisp problem statement that everyone would agree captures what we're actually trying to solve.

## Interaction Model: User-Led Problem Definition

This step is heavily user-driven. The user (partner) owns the problem — they know the context, the stakeholders, and what success looks like. Your job as the associate is to help them articulate it crisply, not to impose your own framing.

### INPUT Phase: Solicit the User's Framing

Before you write anything, get the user's perspective. Ask these questions (using the AskUserQuestion tool or conversationally, as appropriate):

1. **"What's the situation? Walk me through what's happening."** — Let them describe the problem in their own words. Don't rush to reframe it.
2. **"What would success look like? If we solve this perfectly, what changes?"** — This surfaces success criteria.
3. **"What's in scope and out of scope for this work?"** — Let them set boundaries. Suggest scope options if they're unsure, but let them decide.
4. **"Are there constraints I should know about — budget, timeline, politics, data availability?"** — These shape everything downstream.
5. **"Do you have an initial hypothesis about what's going on?"** — The partner's gut feel is valuable signal.

Listen carefully to their answers. The user's language, emphasis, and framing should directly shape the deliverable.

### What You're Producing

A **Problem Definition Document** (.md) containing:

1. **Context**: What's the situation? Who is the client/stakeholder? What prompted this?
2. **Key Question**: One sentence. The single question that, if answered, solves the problem.
3. **Scope**: What's in bounds and out of bounds.
4. **Success Criteria**: How will we know we've answered the question well?
5. **Constraints**: Budget, timeline, political realities, data availability, regulatory requirements.
6. **Stakeholders**: Who cares about the answer? Who has to act on it?
7. **Initial Hypotheses**: 1-3 preliminary hypotheses about the answer.

## How to Extract the Key Question

The user will typically describe a situation, not a question. Your job is to convert their description into a precise question — but then present it back to them for approval. Some patterns:

| User says | Key question might be |
|-----------|----------------------|
| "Revenue is declining" | "What are the primary drivers of revenue decline, and what actions can reverse the trend within 12 months?" |
| "We need to enter a new market" | "Should we enter [market X], and if so, what is the optimal entry strategy?" |
| "Our costs are too high" | "How can we reduce operating costs by [X]% while maintaining service quality?" |
| "Employee turnover is killing us" | "What is driving attrition among [segment], and what interventions would reduce it to [target]%?" |

The key question always implies a decision or action. "What's happening?" is a research question. "What should we do about it?" is a consulting question. Push toward the latter — but ultimately the user decides the framing.

## Scoping Discipline

Scope creep is the enemy. Be explicit about boundaries:

- **Time horizon**: Are we solving for next quarter or next 5 years?
- **Geography**: Global, regional, single market?
- **Business scope**: Entire company, single division, one product line?
- **Decision scope**: Are we recommending and implementing, or just recommending?

If the user hasn't specified scope, do NOT assume — ask them directly. Present options where possible and let them decide.

## Template

```markdown
# Problem Definition

## Context
[2-3 paragraphs on the situation, the stakeholder, and what prompted this work]

## Key Question
> [One clear, decision-oriented question]

## Scope
- **In scope**: [what we will address]
- **Out of scope**: [what we will not address]
- **Time horizon**: [timeframe for the recommendation]

## Success Criteria
[What a good answer looks like — specific, measurable where possible]

## Constraints
[Budget, timeline, data, political, regulatory limitations]

## Stakeholders
| Stakeholder | Role | Interest |
|-------------|------|----------|
| [Name/Group] | [Decision maker / Influencer / Implementer] | [What they care about] |

## Initial Hypotheses
[1-3 preliminary hypotheses about the answer — these will be tested in later steps]
```

## REVIEW Phase: User Refines the Problem Statement

After building the draft problem statement using the user's input, present it and ask for explicit review:

1. **Key Question**: "Here's how I've framed the key question based on what you told me: [proposed question]. Is this right, or would you frame it differently?" — Be ready for the user to completely rewrite it. That's fine.
2. **Scope**: "I've scoped this as [proposed scope]. Does that match your intent? Anything to add or remove?"
3. **Success criteria**: "Here are the success criteria I captured. Are these the right measures? Anything missing?"
4. **Constraints**: "These are the constraints I'm working with. Did I miss anything?"
5. **Initial hypotheses**: "Here are the hypotheses I'd start with. Do any of these feel wrong? Would you add or change any?"

**Do not proceed to Step 2 until the user explicitly approves the problem statement.** If they suggest changes — even to a single word in the key question — make the revision and re-present.

## Common Pitfalls

- **Too broad**: "How do we grow?" is not a useful key question. Push for specifics — but let the user decide the specifics.
- **Solution-first**: "Should we build a new app?" presupposes the solution. Back up to the problem: "How do we improve customer engagement?" Gently suggest this reframe, but accept the user's call.
- **Missing the real question**: The stated problem often isn't the real one. Probe gently — but respect that the user may have good reasons for their framing.
- **Assuming scope without asking**: Never fill in scope, time horizon, or geography without asking. These shape the entire analysis.
- **Rushing past the user's input**: This step is where you build a shared understanding. Spending an extra turn getting the framing right saves enormous effort downstream.
