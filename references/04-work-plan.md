# Step 4: Build the Work Plan

Now that you know what to focus on, build a structured plan for the analyses you'll conduct. This translates priorities into concrete actions with clear outputs.

## Interaction Model: User Validates and Approves the Plan

The work plan defines what analyses will be done, what data is needed, and in what order. The user needs to validate this because they know what data they actually have, what analyses their stakeholders expect, and what constraints exist. The user reviews and approves the final work plan before any analysis begins.

### INPUT Phase: Get Data and Constraint Information

Before building the plan, ask the user:

1. **"What data do you have readily available?"** — List the data the plan will need and ask which they can provide. This is critical — a beautiful work plan with no data is useless.
2. **"Are there specific analyses your stakeholders expect to see?"** — Sometimes the audience demands a particular analysis regardless of its priority ranking.
3. **"Any timeline constraints?"** — When does the work need to be done by? Are there interim milestones?
4. **"Any approach preferences?"** — For key analyses, the user may prefer one method over another.
5. **"What estimation approach is acceptable where data is missing?"** — Some users want conservative estimates; others want aggressive. Establish this now.

## What You're Producing

A **Work Plan Spreadsheet** (.xlsx) with:

1. **Summary tab**: Overview of the plan — key workstreams, timeline, milestones
2. **Detailed plan tab**: Each analysis with its question, approach, data needs, and expected output
3. **Data inventory tab** (if applicable): What data is available, what's missing, how to get it

## Work Plan Structure

For each priority area from Step 3, define the specific analyses needed:

### Analysis Definition

Each analysis should answer one specific question. Define:

| Field | Description |
|-------|-------------|
| **Workstream** | Which priority area this belongs to |
| **Analysis name** | Short, descriptive name |
| **Question to answer** | The specific question this analysis resolves |
| **Approach** | How you'll do it — calculation, comparison, benchmarking, survey, interview, etc. |
| **Data needed** | What inputs are required |
| **Data source** | Where the data comes from (user-provided, public, estimated) |
| **Output** | What the deliverable looks like (chart, table, model, etc.) |
| **Hypothesis** | What you expect to find |
| **Priority** | P1/P2/P3 from Step 3 |

### Sequencing

Some analyses build on others. Map dependencies:
- **Independent**: Can run in parallel
- **Dependent**: Needs output from another analysis as input
- **Gating**: Must complete before deciding whether to pursue other analyses

## Creating the Spreadsheet

Use the xlsx skill to create a professionally formatted workplan. Structure:

### Tab 1: Summary
- Project name, key question, date
- Workstream overview table: workstream name, # of analyses, estimated effort, key milestone
- Timeline view (if the user specified a timeline)

### Tab 2: Detailed Analysis Plan
Columns:
- ID (e.g., WS1-A1, WS1-A2, WS2-A1)
- Workstream
- Analysis Name
- Question to Answer
- Approach
- Data Needed
- Data Source
- Data Status (Available / Needed / Gap)
- Output Format
- Hypothesis
- Priority
- Dependencies
- Status (Not Started / In Progress / Complete)

### Tab 3: Data Inventory (when data is discussed)
Columns:
- Data Item
- Source
- Status (Have / Need to Request / Unavailable)
- Format
- Notes
- Workaround if unavailable

## Typical Analysis Types

Depending on the problem domain, common analyses include:

**Quantitative**:
- Trend analysis (how has X changed over time?)
- Segmentation (how does X vary across segments?)
- Benchmarking (how does our X compare to peers?)
- Sensitivity analysis (how much does the answer change if assumptions shift?)
- Financial modeling (NPV, IRR, payback period)
- Regression / correlation (what drives X?)

**Qualitative**:
- Best practice review (what do leaders in this space do?)
- Process mapping (where are the bottlenecks / waste?)
- Stakeholder analysis (who needs to be aligned?)
- Risk assessment (what could go wrong?)

## Output Quality Standards

The work plan should be concrete enough that someone could pick it up and execute it without further clarification. Each analysis row should be self-contained.

## REVIEW Phase: User Approves the Work Plan

Present the completed work plan and ask for explicit approval. The user needs to sign off before any analysis begins.

1. **Validate the analysis list**: "Here are the analyses I've planned for each priority area, based on your data availability and priorities. Do these make sense? Any to add or remove?"
2. **Confirm data status**: "Here's my data inventory — what you have, what I'll need to estimate, and what's missing. Does this look right?"
3. **Review approach choices**: "For [key analysis], I'm proposing [approach]. Is that the right method, or would you prefer something different?"
4. **Confirm sequencing**: "Here's the order I'd execute in. Any analyses you'd want to see results from first?"
5. **Validate assumptions approach**: When data isn't available: "For [analysis], I'd need to estimate [parameter]. I'd assume [value with rationale]. Does that seem reasonable, or do you have a better number?"
6. **Overall sign-off**: "Does this work plan cover everything you need? Once you approve, I'll start executing the analyses."

**Do not proceed to Step 5 until the user explicitly approves the work plan.** If they want to add analyses, change approaches, or reprioritize, revise and re-present.

## Common Pitfalls

- **Too vague**: "Analyze the market" is not an analysis. "Compare market size and growth rates across segments A, B, C using [source] data" is.
- **Missing data plan**: Every analysis needs data. If you haven't identified where the data comes from, the plan isn't actionable.
- **No sequencing**: Some analyses depend on others. Failing to sequence them leads to rework.
- **Over-planning**: The work plan should take proportional effort. 15-25 analyses is typical. More than 30 suggests you haven't prioritized enough.
- **Assuming data availability**: Never assume the user has data you haven't confirmed. Ask first.
- **Skipping user approval**: The work plan is a contract between you and the partner about what gets done. Don't start work without their sign-off.
