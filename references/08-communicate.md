# Step 8: Communicate

The final step — packaging all the work into a compelling deliverable. This is where the pyramid principle and storylining come together. The best analysis in the world is worthless if it isn't communicated clearly.

## Interaction Model: User Configures the Output

The partner decides how the final output looks. This step starts with the user making seven structured choices that fully define the deliverable's shape, narrative approach, and visual identity. Use the **AskUserQuestion** tool to collect these choices in a structured way.

### INPUT Phase: Collect the User's Communication Preferences

Before building anything, collect the following seven inputs from the user. Use the **AskUserQuestion** tool to present structured choices. You may batch these into 2-3 AskUserQuestion calls (each call supports up to 4 questions).

---

#### AskUserQuestion — Batch 1 (Narrative, Title, Exec Summary, Context Slide)

**Question 1 — Narrative Structure**
header: "Narrative"
question: "Which narrative structure should the deck follow?"
multiSelect: false
Options:

1. **Answer-First (Pyramid)**
   - Lead with the conclusion, then support it with arguments, then evidence. The audience knows where you stand immediately. Minto's Pyramid Principle, BLUF. Best for: aligned audiences, senior stakeholders, time-constrained settings.

2. **Evidence-First (Build)**
   - Start with observations and data, let the pattern emerge, arrive at a conclusion the audience "discovers" with you. Classic scientific paper structure. Best for: skeptical audiences, counterintuitive conclusions, technical reviews. The detective story — clues accumulate until the solution becomes undeniable.

3. **Narrative Arc (SCR)**
   - Establish shared context (Situation), introduce a disrupting tension (Complication), resolve it (Resolution). The backbone of McKinsey storylining and Freytag's dramatic pyramid. The energy comes from tension and release. Best for: persuasion when the audience needs to feel the problem before they'll accept the solution.

4. **Transformation (Current → Future → Bridge)**
   - Paint the "as-is," paint a compelling "to-be," then lay out the path between them. Duarte's oscillation pattern, Monroe's Motivated Sequence. The energy comes from the aspiration gap. Best for: change management, vision-setting, fundraising pitches.

5. **Comparative Evaluation (Options → Criteria → Rec)**
   - Present structured alternatives, evaluate against explicit criteria, arrive at a selection. The audience's journey is one of structured choice — they need to feel the rigor of the process, not just the answer. Best for: board decisions, investment committees, vendor selections, policy choices.

6. **Sequential / Process (Step-by-Step)**
   - Walk through events, phases, or steps in temporal or logical order. The sequence itself is the insight. Best for: project updates, implementation plans, post-mortems, how-to content.

**Question 2 — Title and Subtitle**
header: "Title"
question: "What should the title and subtitle of the document be? (Enter as 'Title | Subtitle' or just a title)"
multiSelect: false
Options:
- **Auto-generate from problem statement** — I'll derive a title and subtitle from the problem definition and key recommendation.
- **Enter custom title** — (user selects "Other" to type their own)

**Question 3 — Executive Summary**
header: "Exec Summary"
question: "Include an executive summary slide/page?"
multiSelect: false
Options:
- **Yes (Recommended)** — A one-slide/page synthesis of the full argument, structured to match the chosen narrative approach. Mandatory for serious decks.
- **No** — Skip the executive summary. Use only for very short or informal deliverables.

**Question 4 — Context & Objectives Slide**
header: "Context"
question: "Include a Context & Objectives slide/section?"
multiSelect: false
Options:
- **Yes (Recommended)** — Sets the stage: why we're here, what was asked, what success looks like. Grounds the audience before the analysis.
- **No** — Jump straight into findings. Use when the audience is already deeply familiar with the context.

---

#### AskUserQuestion — Batch 2 (Content Pages, Appendix, Visual Style)

**Question 5 — Number of Content Pages**
header: "Page Count"
question: "How many content slides/pages? (This count excludes the title slide, exec summary, and context & objectives — it covers analysis, findings, recommendations, and next steps only.)"
multiSelect: false
Options:
- **Compact (4-6)** — Tight, high-level, one insight per slide. Best for time-constrained audiences.
- **Standard (8-12)** — Room to develop each argument with supporting evidence. The consulting default.
- **Comprehensive (15-20)** — Deep treatment with detailed evidence, multiple sub-analyses, and implementation detail.
- **Custom** — (user selects "Other" to specify an exact number)

**Question 6 — Appendix Section**
header: "Appendix"
question: "Include an appendix section?"
multiSelect: false
Options:
- **Yes (Recommended)** — Detailed data tables, methodology notes, assumptions, sensitivity analyses, and backup slides. Keeps the main deck clean while preserving rigor.
- **No** — No appendix. Everything that matters is in the body. Use for short, informal deliverables.

**Question 7 — Visual Style**
header: "Visual Style"
question: "Which visual style should the deliverable follow?"
multiSelect: false
Options:
- **Clean & Minimal** — White space, simple typography, muted accent colors. Elegant and modern. Lets the content breathe.
- **Data-Heavy / Analytical** — Dense charts, tables, and quantitative evidence on every page. Serious, rigorous feel. Best for technical or financial audiences.
- **Visually Rich / Diagrammatic** — Frameworks, process flows, icons, and conceptual diagrams. Best for strategy presentations and change narratives.
- **Corporate / Branded** — (user selects "Other" to specify brand colors, fonts, and any template requirements)

**Question 8 — Brand Styling** (ask only if output is PowerPoint)
header: "Brand"
question: "Apply a brand styling profile?"
multiSelect: false

Before presenting this question, check which `.md` files exist in `references/styles/`. List each one as an option by brand name. Always include a "None" option and a custom option.

Options (dynamically generated):
- **[Brand Name]** — for each `.md` file found in `references/styles/` (e.g., "McKinsey" if `mckinsey.md` exists)
- **None (Recommended)** — Use the visual style from Q7 with the default palette from the pptx skill's design guidance.
- **Custom** — (user selects "Other" to describe brand requirements; you then create a new styling file from the template)

**If a brand style is selected**: Read the corresponding file from `references/styles/` and apply all specified fonts, colors, layout rules, and slide type overrides when generating the PowerPoint. The brand styling file takes precedence over the Q7 visual style for any property it defines — but the Q7 choice still governs overall content density and layout philosophy (e.g., "Data-Heavy" still means dense charts even in McKinsey styling).

**If "Custom" is selected**: Ask the user for their brand's key elements (primary color, fonts, any specific requirements), create a new `.md` file in `references/styles/` using the template from `references/brand-styling-template.md`, and apply it.

---

### Additional Context Questions (asked as free-text follow-ups after the structured choices above)

After collecting the seven structured inputs, ask these open-ended follow-ups conversationally (not via AskUserQuestion):

1. **Audience**: "Who will be in the room? What's their level (C-suite, middle management, board)? What do they already know about this problem?"
2. **Key message**: "If the audience remembers only one thing, what should it be?"
3. **Tone**: "Should this feel bold and decisive, or cautious and options-oriented? Is this a 'we recommend X' deck or a 'here are three paths, let's discuss' deck?"
4. **Sensitive content**: "Are there findings or recommendations that are politically sensitive? Anything to frame carefully or leave for the appendix?"

---

## What You're Producing

Either an **Executive Presentation** (.pptx) or an **Executive Report** (.docx), shaped by the user's seven choices above. The deliverable's structure is not fixed — it is **assembled from the user's selections**.

### If PowerPoint (.pptx)

Use the pptx skill to create the presentation. Follow the storyline structure below, adjusted per the user's narrative structure choice.

### If Word Document (.docx)

Use the docx skill to create the report. Follow the same narrative structure adapted for prose format.

---

## Narrative Structure Playbooks

Based on the user's choice in Question 1, follow the corresponding playbook to build the storyline. Each playbook defines the arc — the specific slide/section sequence, how to build the headline chain, and what kind of content belongs where.

### CRITICAL: No Literal Framework Labels in Deliverables

**Never use framework terminology as literal section headings, slide titles, or labels in the final deliverable.** The frameworks (SCR, Current→Future→Bridge, Options→Criteria→Rec, etc.) are *thinking tools* that shape the narrative structure — they are NOT labels the audience should see.

Instead of framework jargon, use **descriptive, context-specific language** that communicates what each section actually says about the client's situation. For example:
- Instead of "Situation" → describe the actual context (e.g., "The European market has delivered consistent 8% growth for a decade")
- Instead of "Complication" → describe the actual disruption (e.g., "Three regulatory changes threaten the core business model")
- Instead of "Resolution" → describe the actual solution (e.g., "A dual-track strategy preserves margin while capturing the adjacent opportunity")
- Instead of "The Current State" → describe what's happening now (e.g., "Manual processes consume 40% of analyst time")
- Instead of "The Future State" → describe the vision (e.g., "Automated workflows free analysts to focus on high-value judgment calls")
- Instead of "The Bridge" → describe the path (e.g., "Three investments close the gap in 18 months")

The headline chain templates below use placeholders like `[describe the baseline context]` to remind you to generate context-specific language. The audience should experience a compelling narrative — not see the scaffolding behind it.

**One exception**: The executive summary slide/page title should begin with "Executive Summary" — this is a standard navigational label that audiences expect, not framework jargon.

### Playbook 1: Answer-First (Pyramid)

**Arc**: Conclusion → Supporting Arguments → Evidence

**Headline Chain Template**:
```
1. [Title slide]
2. [Exec summary — if selected] The answer is X, supported by three pillars
3. [Context — if selected] [Company] asked us to evaluate [question]
4. Our recommendation is [core recommendation] — THE ANSWER
5. The first reason: [argument 1 with headline-as-sentence]
6. Evidence: [data/chart supporting argument 1]
7. The second reason: [argument 2 with headline-as-sentence]
8. Evidence: [data/chart supporting argument 2]
9. The third reason: [argument 3 with headline-as-sentence]
10. Evidence: [data/chart supporting argument 3]
11. Implementation requires [next steps]
12. [Appendix — if selected]
```

**When to use**: The audience is aligned, senior, or time-constrained. They want the answer up front.

### Playbook 2: Evidence-First (Build)

**Arc**: Observations → Pattern → Conclusion

**Headline Chain Template**:
```
1. [Title slide]
2. [Exec summary — if selected] Three converging signals point to [conclusion]
3. [Context — if selected] We set out to understand [question]
4. Observation 1: [data point / finding that surprises or intrigues]
5. Observation 2: [second data point that reinforces the pattern]
6. Observation 3: [third data point that makes the pattern undeniable]
7. Taken together, these findings reveal [the pattern / insight]
8. This means [implication for the business]
9. Therefore, we recommend [recommendation]
10. Next steps to act on this insight
11. [Appendix — if selected]
```

**When to use**: The conclusion is counterintuitive. The audience needs to see the evidence accumulate before they'll accept the answer.

### Playbook 3: Narrative Arc (SCR)

**Arc**: Situation → Complication → Resolution

**Headline Chain Template**:
```
1. [Title slide]
2. [Exec summary — if selected] [Company] faces [complication] but can [resolution]
3. [Context — if selected] The starting point: [shared context everyone agrees on]
4. [Describe the baseline context — e.g., "Global widget demand has grown 8% annually since 2019"]
5. [Supporting detail that sets the scene — e.g., "Three product lines drive 85% of margin"]
6. [Describe the disruption — e.g., "New EU regulations eliminate the cost advantage in two core segments"]
7. [Quantify the stakes — e.g., "Inaction puts $120M in annual revenue at risk by 2027"]
8. [State the key insight — e.g., "A dual-track compliance and diversification strategy preserves margin"]
9. [State the recommendation — e.g., "Invest $15M over 18 months in regulatory readiness and adjacent-market entry"]
10. [Specific initiative 1 — e.g., "Accelerate reformulation of the top 12 affected SKUs"]
11. [Specific initiative 2 — e.g., "Launch pilot in Southeast Asian market by Q3"]
12. [Quantified benefit — e.g., "Combined impact: $95M in protected and new revenue by 2028"]
13. Next steps and milestones
14. [Appendix — if selected]
```

**Important**: Do NOT label sections as "Situation," "Complication," or "Resolution." The audience should experience the narrative tension naturally — they should feel the baseline, then the disruption, then the path forward — without seeing the framework labels.

**When to use**: The audience needs to feel the problem before they'll accept the solution. Classic persuasion structure.

### Playbook 4: Transformation (Current → Future → Bridge)

**Arc**: As-Is → To-Be → How to Get There

**Headline Chain Template**:
```
1. [Title slide]
2. [Exec summary — if selected] From [current state] to [future vision] via [bridge]
3. [Context — if selected] We were asked to chart a path from [starting point] to [aspiration]
4. [Describe today's reality — e.g., "Manual underwriting processes handle only 200 applications per day"]
5. [What's broken — e.g., "Error rates exceed 12% and cycle times have doubled since 2023"]
6. [Describe the vision — e.g., "AI-augmented workflows can process 1,500 applications daily at <2% error"]
7. [What good looks like — e.g., "Top-quartile insurers already achieve 5x throughput with similar models"]
8. [Describe the path — e.g., "Three investments close the gap in 18 months"]
9. [Initiative 1 — e.g., "Deploy automated triage for low-complexity applications (60% of volume)"]
10. [Initiative 2 — e.g., "Retrain underwriting staff on exception-handling workflows"]
11. [Initiative 3 — e.g., "Integrate real-time data feeds to eliminate manual lookups"]
12. [Roadmap — e.g., "Phased rollout: pilot in Q2, scale in Q3, full deployment by Q4"]
13. [Appendix — if selected]
```

**Important**: Do NOT use labels like "The Current State," "The Future State," or "The Bridge." Instead, describe each section in terms that are specific to the client's situation — what's happening today, what's possible, and how to get there. The aspiration gap should be felt through the content, not signposted with framework jargon.

**When to use**: Change management, vision-setting, or any situation where the aspiration gap is the motivating force.

### Playbook 5: Comparative Evaluation (Options → Criteria → Recommendation)

**Arc**: Alternatives → Evaluation Framework → Selection

**Headline Chain Template**:
```
1. [Title slide]
2. [Exec summary — if selected] Option [X] best meets our criteria across [dimensions]
3. [Context — if selected] [Company] needs to choose between [N options] for [decision]
4. [Describe the alternatives — e.g., "Three platform architectures can support the next decade of growth"]
5. [Option A — e.g., "Full cloud migration delivers maximum scalability at highest upfront cost"]
6. [Option B — e.g., "Hybrid architecture balances flexibility with infrastructure continuity"]
7. [Option C — e.g., "Modernize-in-place minimizes disruption but limits future optionality"]
8. [Describe the evaluation approach — e.g., "Five criteria reflect the board's stated priorities"]
9. [Show the framework — e.g., "Cost, scalability, risk, timeline, and talent availability weighted by strategic importance"]
10. [Show comparative results — e.g., "The hybrid approach scores highest on the weighted assessment"]
11. [Explain why — e.g., "Hybrid architecture outperforms on cost-adjusted scalability and implementation risk"]
12. [Risks — e.g., "Key risks center on integration complexity — mitigated by a phased rollout"]
13. [Implementation — e.g., "A 24-month implementation in three phases minimizes operational disruption"]
14. [Appendix — if selected]
```

**Important**: Do NOT use generic labels like "The Options," "Evaluation Criteria," or "Evaluation." Each headline should describe *what* is being compared, *what* the criteria reflect, and *what* the assessment reveals — in language specific to the decision at hand.

**When to use**: The audience needs to see the rigor of the selection process. Board decisions, vendor selections, investment committees.

### Playbook 6: Sequential / Process (Step-by-Step)

**Arc**: Phase 1 → Phase 2 → Phase 3 → ... → Phase N

**Headline Chain Template**:
```
1. [Title slide]
2. [Exec summary — if selected] A [N]-phase approach delivers [outcome] by [timeline]
3. [Context — if selected] [Company] needs to [objective] — here is the execution plan
4. Overview: The [N] phases at a glance [framework/timeline slide]
5. Phase 1: [name] — [action title stating what happens and why it matters]
6. Phase 1 detail: [key activities, milestones, deliverables]
7. Phase 2: [name] — [action title]
8. Phase 2 detail: [key activities, milestones, deliverables]
9. Phase N: [name] — [action title]
10. Phase N detail: [key activities, milestones, deliverables]
11. Dependencies and risk factors across phases
12. Overall timeline and resource requirements
13. [Appendix — if selected]
```

**When to use**: Implementation plans, project updates, post-mortems, process documentation.

---

## Assembling the Deck/Document Structure

The final structure is assembled from the user's choices. Not every section is present — only those the user selected.

### Assembly Order

```
1. Title Slide / Title Page                    ← ALWAYS present
2. Executive Summary                           ← if user selected YES in Q3
3. Context & Objectives                        ← if user selected YES in Q4
4. Content Pages (per narrative playbook)       ← count from Q5
5. Appendix                                    ← if user selected YES in Q6
```

**Title slide** uses the user's title and subtitle from Q2 (or auto-generated from the problem statement if they chose that option), plus date and confidentiality marking.

**Content page count**: The number from Q5 covers all slides/pages between the Context & Objectives section and the Appendix. This is the analysis, findings, recommendations, and next steps — the "meat" of the deck. Adapt the playbook headline chain to fit within this count. If the user chose 4-6 content pages, compress: combine related insights, use one slide per argument. If they chose 15-20, expand: add evidence slides, sub-analyses, implementation detail.

---

## The Pyramid Principle

Barbara Minto's Pyramid Principle is the communication backbone for all narrative structures (even non-pyramid ones use it at the slide level):

1. **Start with the answer** (the governing thought)
2. **Group supporting arguments** logically below it
3. **Support each argument** with evidence
4. **Every level answers "why?" or "how?"** for the level above

Even in an Evidence-First or SCR deck, each individual slide should follow the pyramid internally: action title states the point, body provides the support.

## Storylining

Before building slides or pages, build the storyline. The storyline is the sequence of key messages (action titles / section headings) that takes the audience through the chosen narrative arc.

### How to Build the Storyline

1. **Select the playbook** matching the user's narrative structure choice (Q1)
2. **Fill in the headline chain** using content from Steps 1-7
3. **Include or exclude** exec summary, context & objectives, and appendix per the user's choices (Q3, Q4, Q6)
4. **Fit to the page count** from Q5 — compress or expand the playbook template
5. **Test the chain**: Read just the headlines in sequence. They should tell the complete story on their own.

If you read just the titles/headlines in sequence, you should get the full story regardless of which narrative structure was chosen.

---

## Visual Style Application

Based on the user's choice in Q7, apply the following visual principles:

### Clean & Minimal
- Generous white space (40%+ of each slide should be empty)
- One accent color + black/dark gray text
- Simple sans-serif typography
- Charts with minimal gridlines and labels
- No decorative elements — content speaks for itself

### Data-Heavy / Analytical
- Dense layouts with charts, tables, and callout numbers
- Multiple data visualizations per slide where appropriate
- Footnotes and source citations on every data slide
- Muted, professional color palette (blues, grays)
- Small but readable fonts to fit more information

### Visually Rich / Diagrammatic
- Framework diagrams, process flows, and concept maps
- Icons to represent key ideas
- Color-coded categories and phases
- Visual metaphors (bridges, pyramids, funnels)
- Balance of text and visual elements

### Corporate / Branded
- Apply the user's specified brand colors, fonts, and logo
- Follow any template or style guide they provide
- Match the visual language of their existing materials

### Applying a Brand Styling Profile

When the user selects a brand styling profile (Q8), read the corresponding `.md` file from `references/styles/` and apply its properties systematically:

1. **Typography**: Use the specified `heading_font`, `body_font`, and `accent_font` with the size scale from the file. These override the pptx skill's default font choices.
2. **Colors**: Use the full palette — core brand colors, text colors, backgrounds, chart colors, and functional colors. These override any palette from the Q7 visual style.
3. **Layout**: Apply the specified margins, title bar style, and footer settings.
4. **Logo**: If `logo_file` is specified and the file exists in `references/styles/logos/`, include it per the placement rules.
5. **Slide type overrides**: Apply any per-slide-type customizations (title slide, dividers, content, closing).
6. **Q7 still governs density**: The visual style choice (Clean & Minimal, Data-Heavy, Visually Rich) still determines layout density, chart frequency, and content-to-whitespace ratio — the brand styling file only controls the visual identity (fonts, colors, spacing, chrome).

---

## PowerPoint-Specific Guidance

### Slide Design Principles

**The Action Title Rule**: Every slide title is a complete sentence stating the key message — not a topic label.

| Bad title | Good title |
|-----------|-----------|
| "Market Analysis" | "The target market is growing at 12% annually, driven by segment X" |
| "Cost Breakdown" | "Manufacturing costs have risen 23% due to raw material inflation" |
| "Recommendations" | "A three-phase approach can recover $15M in annual margin" |

**Slide Body Guidelines**:
- One message per slide
- Visual evidence: Charts, tables, diagrams over text
- Minimize text: 1-line bullets, max 5-6 per slide
- Source everything

### Framework-to-Deep-Dive Numbering

When a slide (or page) presents a **framework** — a visual with multiple blocks, pillars, phases, or components — and subsequent slides (or pages) detail each block individually, apply **consistent numbering** to link the overview to the detail:

1. **On the framework slide**: Label each block with a number or letter identifier (e.g., `1`, `2`, `3` or `A`, `B`, `C` or `i`, `ii`, `iii`). The choice of Arabic numerals, Roman numerals, uppercase letters, or lowercase letters should match the document's style and the user's preference — if not specified, default to Arabic numerals.

2. **On each deep-dive slide**: Include the same identifier in the slide title or a prominent tag, so the audience can instantly trace the detail back to its position in the framework. Format example:
   - Framework slide title: "A three-pillar strategy drives the turnaround"
     - Block labels: `1. Cost restructuring`, `2. Revenue diversification`, `3. Operational excellence`
   - Deep-dive slide titles: "**1.** Cost restructuring can unlock $8M in annual savings", "**2.** Revenue diversification targets three adjacent markets", "**3.** Operational excellence requires investment in automation"

3. **Consistency rule**: The numbering scheme used on the framework page must carry through identically to every deep-dive page. Never switch from Roman to Arabic mid-sequence.

This applies equally to Word documents — section headers for deep-dive content should carry the same identifier as the corresponding element in the framework figure.

### Chart Choice Guide

| What you're showing | Chart type |
|--------------------|------------|
| Trend over time | Line chart |
| Comparison across categories | Bar chart |
| Part of whole | Stacked bar or waterfall (avoid pie charts) |
| Correlation | Scatter plot |
| Process or flow | Diagram / flowchart |
| Single key number | Large number callout with context |

---

## Executive Summary Guidance (when selected)

When the user selects "Yes" for the executive summary (Q3), it serves as the **structural spine** of the entire document.

The exec summary format adapts to the chosen narrative structure — but **never uses framework labels** as headings or paragraph markers. The structure should be felt, not announced:

- **Answer-First**: Lead with the recommendation, then the 2-3 supporting reasons, then expected impact.
- **Evidence-First**: Lead with the key signals, summarize each, state the conclusion they point to.
- **Narrative Arc (SCR)**: Open with the shared context, introduce the disruption or tension, then present the path forward — using language specific to the client's situation, not the words "Situation," "Complication," or "Resolution."
- **Transformation**: Describe where things stand today, paint the target outcome, then summarize the path between them — without labeling sections "Current State," "Future State," or "Bridge."
- **Comparative Evaluation**: State the decision, the options considered, the evaluation approach, the winner, and why.
- **Sequential**: Summarize the phases, the overall timeline, and the expected outcome.

**The spine test**: If you delete every slide except the exec summary, the reader should still understand the full argument. If you delete the exec summary and read only the slide titles in sequence, you should reconstruct the exec summary.

---

## Context & Objectives Guidance (when selected)

When the user selects "Yes" for Context & Objectives (Q4), this slide/section should cover:

1. **Why we're here**: The triggering event, request, or business need
2. **What was asked**: The specific question or scope of work
3. **How we approached it**: Brief methodology note (1-2 sentences)
4. **What success looks like**: The decision criteria or success metrics from Step 1

This grounds the audience before the analysis begins. Draw directly from the Step 1 problem statement.

---

## Word Document-Specific Guidance

### Report Structure (assembled from user choices)

- **Title page**: Uses title and subtitle from Q2 (or auto-generated), plus date and confidentiality marking
- **Executive Summary** (1-2 pages, if selected in Q3): Adapted to the chosen narrative structure
- **Context & Objectives** (1-2 pages, if selected in Q4): Why, what, how, and success criteria
- **Content sections** (count from Q5, adapted to chosen narrative playbook): Analysis, findings, recommendations, next steps — organized per the playbook
- **Appendices** (if selected in Q6): Detailed data, methodology, assumptions, sensitivity analyses

### Writing Style for Reports

Apply the writing style guide principles (see `references/writing-style.md`) throughout. The prose should be:
- **Concise**: Omit needless words. No throat-clearing.
- **Active**: "The analysis reveals" not "It was revealed by the analysis"
- **Specific**: Concrete numbers and examples, not vague generalizations
- **Direct**: Lead with the conclusion, then support it

---

## Language Quality: Final Editing Pass

Before presenting the final deliverable to the user, run all prose through a dedicated editing pass. Read `references/writing-style.md` for the full style guide and apply its principles:

- Omit needless words — cut filler, hedging, and throat-clearing
- Use active voice — "Revenue declined" not "A decline in revenue was observed"
- Be specific — "$4.2M savings" not "significant savings"
- Avoid fancy words — "use" not "utilize," "help" not "facilitate"
- Place emphatic words at the end of sentences
- Write naturally — if it sounds stiff read aloud, rewrite it

This applies to:
- **PowerPoint**: All slide titles, bullet points, and speaker notes
- **Word**: All prose throughout the document
- **Both**: Executive summary especially — this is the highest-visibility text

The goal is prose worthy of a top-tier consulting firm: clear, tight, forceful, and free of fluff.

---

## REVIEW Phase: User Approves Storyline and Final Output

This step has **two review gates**: the storyline and the final deliverable.

### Review Gate 1: Storyline Approval

Before building any slides or writing any pages, present the storyline:

1. **Present the proposed storyline**: "Here's the narrative arc I'm proposing using the [chosen structure] approach — [list of headlines]. Does this flow make sense?"
2. **Confirm the structure**: "Based on your choices, the deck will have: [title slide] + [exec summary if yes] + [context & objectives if yes] + [N content pages] + [appendix if yes] = [total] pages/slides."
3. **Check emphasis**: "I'm leading with [X] and building toward [Y]. Is that the right emphasis for your audience?"
4. **Check for gaps**: "Anything missing from the story? Anything to reorder?"

**Do not build the deliverable until the user approves the storyline.**

### Review Gate 2: Final Deliverable Approval

After building the deliverable:

1. **Present it**: Share the file and walk through the key sections/slides.
2. **Check the executive summary** (if included): "Does this executive summary capture the message you want?"
3. **Check the flow**: "Does the narrative build logically? Any sections to reorder?"
4. **Check the details**: "Any data points, recommendations, or phrasings to adjust?"
5. **Check the visual style**: "Does the visual treatment match what you had in mind?"
6. **Check the tone**: "Does this strike the right tone for your audience?"
7. **Offer iteration**: "Happy to revise anything — what would you change?"

**The user may request multiple rounds of revision.** This is normal — the final communication is the face of all the work. Revise and re-present until they're satisfied.

---

## Common Pitfalls

- **Topic titles instead of action titles**: "Q3 Revenue" tells nothing. "Q3 revenue declined 8% as enterprise deals slipped" tells everything.
- **Wrong narrative structure for the audience**: An Evidence-First build for a time-constrained CEO, or an Answer-First pyramid for a skeptical board that hasn't bought in yet.
- **Too many slides/pages**: Respect the user's page count. Use appendices for detail that doesn't fit.
- **Data dumps**: Charts without a message are noise. Every visual must support a specific claim.
- **Missing the "so what?" chain**: The storyline should flow logically regardless of narrative structure.
- **Building before confirming storyline**: Always get storyline approval first.
- **Ignoring the visual style choice**: A "clean & minimal" deck with dense tables, or a "data-heavy" deck with mostly text.
- **Flabby prose**: Every sentence should earn its place. Apply Strunk & White ruthlessly.
- **Ignoring format preference**: If the user asked for Word, don't give them PowerPoint (and vice versa).
- **Skipping the editing pass**: The final deliverable should be polished. Sloppy language undermines credibility.
- **Including sections the user turned off**: If they said no to exec summary, don't sneak one in. Respect their choices.
- **Exposing framework scaffolding**: Never use literal framework labels ("Situation," "Complication," "Resolution," "Current State," "Future State," "Bridge," "The Options," "Evaluation Criteria") as slide titles, section headers, or exec summary labels. These are internal thinking tools — the audience should see descriptive, context-specific language that tells the story directly. The framework should be invisible; the narrative should feel natural.
