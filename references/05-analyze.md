# Step 5: Conduct Analyses

This is where the real work happens. You're executing the analyses defined in the work plan, testing hypotheses, and building an evidence base. The output is a combination of data analysis (spreadsheets) and written findings.

## Interaction Model: User Validates Assumptions and Reviews Results

This step has the most back-and-forth. The user validates assumptions before you run each analysis, reviews results as they emerge, and can trigger re-analysis if something doesn't look right. Their corrections make the work better — treat revision requests as the process working correctly, not as failures.

### INPUT Phase: Validate Assumptions Before Each Analysis

Before executing each major analysis (or batch of related analyses), present the assumptions you'll use and get approval:

1. **Key assumptions**: "For this analysis, I need to assume [X], [Y], and [Z]. Here's my rationale for each. Do these seem reasonable? Do you have better numbers?"
2. **Sensitivity ranges**: "For the sensitivity analysis, I'd use these brackets: [low/base/high]. Do these feel right?"
3. **Data gaps**: "I don't have data for [X]. Would you like me to use [proxy approach], or can you provide this data?"
4. **Methodology**: "I'll approach this by [method]. Any concerns or alternative approaches you'd prefer?"

Do not proceed with an analysis if the user has flagged an assumption as unreasonable. Revise the assumption first.

## What You're Producing

1. **Analysis Workbook** (.xlsx): All quantitative analyses in a structured spreadsheet with charts
2. **Findings Document** (.md): Narrative summary of what each analysis revealed

## Execution Approach

Work through the analyses in the work plan (Step 4) in priority order. For each analysis:

1. **State the question** you're answering
2. **Execute the analysis** using the approach defined in the work plan
3. **Apply the "so what?" test**: What does this finding mean for the key question?
4. **Assess your hypothesis**: Confirmed, partially confirmed, or disproven?
5. **Identify follow-up questions**: What new questions does this raise?

## Quantitative Analysis Best Practices

### Data Handling
When the user provides data files (.csv, .xlsx):
- Use the xlsx skill to read and analyze the data
- Create a clean analysis workbook with labeled tabs
- Document assumptions and transformations

When no data is provided:
- Do NOT silently make up estimates. Ask the user first.
- For each key assumption, present a suggested value with reasoning and ask the user to confirm, adjust, or provide their own number
- Provide sensitivity ranges (low / base / high case) and let the user validate
- Cite public data sources when available and ask if the user has better internal data

### Analysis Types and How to Execute Them

**Trend Analysis**
- Chart the metric over time
- Calculate CAGR, period-over-period changes
- Identify inflection points and annotate what caused them
- "So what?": Is the trend accelerating, decelerating, or stable?

**Segmentation**
- Break the metric by relevant dimensions (customer segment, geography, product, channel)
- Look for outliers — which segments are dramatically better or worse?
- Calculate each segment's share of the total
- "So what?": Where is the concentration? Where is the variance?

**Benchmarking**
- Compare performance metrics to peers, industry averages, or best-in-class
- Normalize for size/scale differences where relevant
- Identify the gap between current performance and the benchmark
- "So what?": How big is the gap? Is it closing or widening?

**Financial Modeling**
- Build a simple model: inputs → calculations → outputs
- Include a base case and 2-3 sensitivity scenarios
- Calculate key metrics (NPV, IRR, payback, ROI as appropriate)
- "So what?": Does the economic case hold under reasonable scenarios?

**Root Cause Analysis**
- Use the issue tree structure to drill into each branch with data
- Quantify each branch's contribution to the overall problem
- Identify the 2-3 branches that explain the majority of the issue
- "So what?": Which root causes, if addressed, would have the biggest impact?

### Workbook Structure

Organize the .xlsx analysis workbook with:

- **Summary tab**: Key findings table, one row per analysis, columns for analysis name, key finding, and implication
- **One tab per major analysis**: Clear labels, data with headers, charts where appropriate
- **Assumptions tab**: All estimates and assumptions in one place with sources and confidence levels

## Qualitative Analysis

For qualitative analyses:

- **Best practice reviews**: Research what leading organizations do, identify patterns, assess applicability
- **Process analysis**: Map the current process, identify bottlenecks and waste, estimate improvement potential
- **Risk assessment**: Identify risks, assess likelihood and impact, propose mitigations

Document qualitative findings in the findings document (.md) with the same rigor as quantitative ones — every finding needs a "so what?"

## Findings Document Format

```markdown
# Analysis Findings

## Summary of Key Findings

| # | Finding | So What? | Confidence |
|---|---------|----------|------------|
| 1 | [Crisp statement of what the analysis showed] | [Implication for the key question] | High/Medium/Low |
| 2 | ... | ... | ... |

## Detailed Findings

### Analysis 1: [Name]
**Question**: [What were we trying to answer?]
**Approach**: [Brief description of method]
**Key Finding**: [What did we learn?]
**Supporting Evidence**: [Data points, charts referenced in workbook]
**So What?**: [What this means for the key question]
**Hypothesis Status**: [Confirmed / Partially confirmed / Disproven — and what we now believe instead]

### Analysis 2: [Name]
[Same structure]

## Emerging Themes
[Patterns that cut across individual analyses — these feed into Step 6]

## Open Questions
[New questions raised by the analysis that may need follow-up]

## Key Assumptions and Limitations
[What we assumed, what data was missing, how it affects confidence in the findings]
```

## REVIEW Phase: User Reviews Results and Can Trigger Re-Analysis

This is the most iterative review phase. Present findings as they emerge and be prepared for the user to challenge them.

### After key findings emerge, present them for review:

1. **Present findings clearly**: "Here's what the analysis shows: [key finding]. The data supporting this is [evidence]."
2. **Check against experience**: "Does this match what you're seeing on the ground? Any surprises?"
3. **Surface hypothesis outcomes**: "This finding [confirms/disproves] our hypothesis that [X]. Before I adjust the direction, what's your read?"
4. **Flag unexpected patterns**: "I found [unexpected result]. Should I dig deeper, or is there a contextual explanation?"
5. **Validate interpretations**: "The data suggests [implication]. Are there factors I might be missing that would change this interpretation?"

### Handling corrections and re-analysis

The user may:

- **Challenge an assumption**: "That assumption doesn't match our reality." → Revise the assumption and re-run the analysis. Present the updated results.
- **Dispute a finding**: "That can't be right — we know X." → Investigate the discrepancy. Check data, methodology, and assumptions. Present what you find.
- **Request deeper analysis**: "Can you dig deeper into [aspect]?" → Run additional analysis on the requested area and present results.
- **Provide new information**: "Actually, we have data on that." → Incorporate the new data and re-run affected analyses.
- **Request a pivot**: "This isn't the right angle — let's look at it from [different perspective]." → Adjust the analysis approach per the user's direction.

**For any correction that changes a finding, re-present the updated finding for approval before moving on.** The user needs to see that their correction was incorporated and agree with the new result.

### When to pause and get user direction:

- After completing each P1 analysis (or batch of related P1 analyses)
- When a finding contradicts the hypothesis significantly
- When you need to make a judgment call between two valid interpretations
- When data limitations force you to rely heavily on assumptions
- Before pivoting analytical direction based on emerging findings

**Do not proceed to Step 6 until the user has reviewed all key findings and approved them.** If they've requested re-analysis on any finding, complete the re-analysis and get approval on the updated results before synthesizing.

## Common Pitfalls

- **Analysis without "so what?"**: A chart without an insight is decoration. Every analysis must answer what it means for the decision.
- **False precision**: Don't present estimates to 4 decimal places. Round appropriately.
- **Confirmation bias**: If an analysis disproves your hypothesis, that's valuable — don't bury it.
- **Boiling the ocean**: Stick to the prioritized work plan unless the user redirects.
- **Silent assumptions**: Never use an estimate without asking the user first.
- **Plowing through despite user concerns**: If the partner says "that doesn't look right," stop and investigate. Don't defend the analysis — fix it.
- **Not re-presenting after corrections**: When the user challenges something and you fix it, always show them the updated version. Don't just say "fixed" and move on.
