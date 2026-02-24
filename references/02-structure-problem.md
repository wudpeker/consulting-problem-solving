# Step 2: Structure the Problem

This is where McKinsey thinking really shines. Structuring means decomposing the key question into a MECE set of sub-issues that, if answered, collectively answer the main question. The output is an issue tree — the analytical backbone of the entire engagement.

## Interaction Model: User Chooses the Framework

The user (partner) makes the final call on the structuring approach. They may have a preferred framework, domain-specific knowledge about how to decompose the problem, or strong opinions about which branches matter. Your job is to present options, recommend one, and then build what they choose.

### INPUT Phase: Get the User's Framework Preference

Before building the issue tree, ask the user:

1. **"How would you structure this problem? Do you have a framework in mind?"** — Some users will have a clear answer. If so, use it. If they say "you pick" or "suggest something," move to option presentation.
2. **Present 2-3 framework options** with trade-offs: "For this type of problem, I'd suggest one of these approaches: [Option A] because [reason], [Option B] because [reason], or [Option C — custom structure] because [reason]. I'd lean toward [A] because [reasoning]. Which resonates with you?"
3. **"Are there dimensions of this problem that absolutely need to be in the tree?"** — The user may know that certain branches are critical even if the framework wouldn't naturally surface them.
4. **"How deep should we go? High-level (2 levels) or detailed (3-4 levels)?"** — Let them set the granularity.

The user's choice of framework is final. Even if you think Option B is better than Option A, if the partner says A, you build A.

## What You're Producing

1. **Issue Tree** (.md): A hierarchical decomposition of the key question into MECE sub-issues, typically 2-3 levels deep
2. **Hypothesis Set**: For each major branch, a preliminary hypothesis about what you expect to find
3. **Optional SVG diagram**: For complex trees, a visual representation

## MECE: The Core Discipline

**Mutually Exclusive**: No overlap between branches. If an item could fit in two branches, your structure is wrong.
**Collectively Exhaustive**: No gaps. If you answered every branch but could still miss the answer to the key question, you have a gap.

Test your tree by asking: "If I conclusively answered every leaf node, would I have a complete answer to the key question?" If yes, it's collectively exhaustive. Then check: "Could any insight or data point belong to more than one branch?" If no, it's mutually exclusive.

## Common Structuring Frameworks

Present these as options for the user to choose from. Don't force-fit — sometimes a custom structure is better, and the user may know this.

### Profitability
```
Why is profitability declining?
├── Revenue issues
│   ├── Volume decline
│   │   ├── Market shrinkage
│   │   └── Share loss
│   └── Price/mix deterioration
│       ├── Pricing pressure
│       └── Mix shift to lower-margin products
└── Cost issues
    ├── Variable costs (COGS)
    │   ├── Raw materials
    │   ├── Labor
    │   └── Manufacturing efficiency
    └── Fixed costs (SG&A + overhead)
        ├── Headcount growth
        ├── Real estate / facilities
        └── Other overhead
```

### Market Entry
```
Should we enter Market X?
├── Market attractiveness
│   ├── Market size and growth
│   ├── Profitability (margins in the market)
│   └── Competitive dynamics
├── Our ability to win
│   ├── Capabilities fit
│   ├── Assets we can leverage
│   └── Gaps to fill
└── Economic case
    ├── Required investment
    ├── Expected returns (NPV/IRR)
    └── Risk profile
```

### Operational Improvement
```
How can we reduce costs by X%?
├── Quick wins (0-6 months)
│   ├── Procurement savings
│   ├── Process waste elimination
│   └── Discretionary spend reduction
├── Medium-term (6-18 months)
│   ├── Organizational redesign
│   ├── Technology automation
│   └── Supply chain optimization
└── Structural changes (18+ months)
    ├── Footprint rationalization
    ├── Outsourcing / insourcing decisions
    └── Business model changes
```

### Customer / Growth
```
How do we grow revenue by X%?
├── Grow existing customers
│   ├── Increase purchase frequency
│   ├── Increase basket size / upsell
│   └── Reduce churn
├── Acquire new customers
│   ├── New segments
│   ├── New channels
│   └── Geographic expansion
└── New products / services
    ├── Adjacent offerings
    ├── Innovation pipeline
    └── Partnerships / M&A
```

## Building a Custom Issue Tree

When standard frameworks don't fit (or when the user prefers a custom approach):

1. Start from the key question
2. Ask: "What are the 2-4 major components of this question?" — these become Level 1 branches
3. For each Level 1 branch, ask the same question recursively
4. Stop when you reach branches that can be answered with a specific analysis or data point (usually 2-3 levels)
5. MECE-check at every level

## Hypothesis Generation

For each major branch (Level 1 or Level 2), form a hypothesis. Present these to the user — they often have stronger hypotheses based on their domain knowledge. The hypothesis should be:

- **Specific**: "We're losing share to Competitor Y in the mid-market segment" not "we might have a competitive problem"
- **Testable**: You should be able to design an analysis that would prove or disprove it
- **Actionable**: If true, it should imply a course of action

## Output Format

```markdown
# Issue Tree: [Key Question]

## Framework Used
[Name of framework and why it was selected — reference the user's choice]

## Tree Structure

[Key Question]
├── [Branch 1]
│   ├── [Sub-branch 1.1]
│   │   ├── [Leaf 1.1.1]
│   │   └── [Leaf 1.1.2]
│   └── [Sub-branch 1.2]
├── [Branch 2]
│   ├── [Sub-branch 2.1]
│   └── [Sub-branch 2.2]
└── [Branch 3]
    ├── [Sub-branch 3.1]
    └── [Sub-branch 3.2]

## Hypotheses

| Branch | Hypothesis | How to Test |
|--------|-----------|-------------|
| [Branch 1] | [Specific, testable hypothesis] | [Analysis approach] |
| [Branch 2] | [Specific, testable hypothesis] | [Analysis approach] |
| [Branch 3] | [Specific, testable hypothesis] | [Analysis approach] |

## MECE Check
- **Mutually Exclusive**: [Brief confirmation that branches don't overlap]
- **Collectively Exhaustive**: [Brief confirmation that no major issues are missing]
```

## REVIEW Phase: User Makes the Final Call on the Tree

After building the draft issue tree using the user's chosen framework, present it for review. The user's approval is the gate to proceed.

1. **Framework validation**: "Here's the tree built on the [framework] you chose. Does this decomposition capture the problem the way you see it?"
2. **Branch validation**: "Here are the Level 1 branches: [list]. Do these cover the right dimensions? Anything to add, remove, or rename?"
3. **Depth check**: "I've gone [N] levels deep. Is this the right granularity, or should any branch go deeper or shallower?"
4. **Hypotheses review**: "For each branch, here's my initial hypothesis. Do any of these conflict with what you know? Would you change or add any?"
5. **MECE check together**: "I've tested for MECE — no overlaps and no gaps that I can see. Do you spot any overlap or any missing dimension?"

**Do not proceed to Step 3 until the user explicitly approves the issue tree.** If they want to change the framework entirely, rebuild from scratch. If they want to adjust branches, make the changes and re-present.

## Common Pitfalls

- **Too many branches**: If Level 1 has more than 4-5 branches, you probably haven't grouped well enough. Consolidate.
- **Not MECE**: The most common failure. Test rigorously.
- **Too shallow**: A one-level tree isn't useful. Push to at least 2 levels.
- **Too deep**: More than 3-4 levels and you're getting into analysis territory. Save that for Step 5.
- **Framework worship**: Don't use a profitability framework for a talent problem. Let the problem drive the structure.
- **Picking a framework without asking**: The user may have strong opinions or domain knowledge. Always present options and let them choose.
- **Overriding the user's choice**: If the partner picks a framework, build it — even if you'd have chosen differently. You can note trade-offs, but the decision is theirs.
