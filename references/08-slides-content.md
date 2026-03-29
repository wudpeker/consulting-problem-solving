# Step 8 — Slides Track: Content Rules

Content rules for building slide decks. Read this file after Gate 2 (sceptical review passed), before distilling the content spec (Gate 2b).

The core principle: **no undifferentiated walls of text.** Slides can be dense when the content demands it — detailed roadmaps, comparison tables, framework breakdowns. But every piece of text on a slide must be structured, scannable, and earn its place. If content reads like prose paragraphs, it belongs in the vertical track.

---

## Action Title Rule

Every slide title is a **complete sentence stating the key insight**. Lead with the argument, not the topic or the number.

| Bad (topic label) | Bad (number-led) | Good (insight-led) |
|---|---|---|
| "Market Analysis" | "$4.2B TAM at 23% CAGR" | "The target market is large and growing fast enough to sustain our thesis" |
| "Cost Breakdown" | "Costs up 18% YoY" | "Rising input costs are compressing margins and require a structural response" |
| "Customer Segments" | "Enterprise = 62% of revenue" | "Enterprise customers drive the majority of revenue and all of the margin" |
| "Competitive Landscape" | "5 major competitors" | "No incumbent has locked up the market — the window is open" |

**Test**: Cover the slide body. Does the title alone tell you the point? If not, rewrite.

---

## Slide Body Rules

The body is the content below the action title. This is where the "wall of text" problem lives. Different slide types need different content structures — but all share one rule: **no unstructured prose blocks.**

### The Universal Rule

**No paragraphs on slides.** If text flows as continuous prose — sentences connecting to sentences — it won't be read. Every piece of content must be in a structured form: bullets, table cells, callout boxes, labeled diagram elements, or short standalone statements. The reader should be able to enter the slide at any point and grasp individual pieces without reading sequentially.

### Slide Types and Their Content Rules

**Argument slides** (the most common — making a single point with evidence):
- 3-5 bullets, each one line (~12 words / ~60 characters)
- Parallel construction: all bullets start with the same part of speech

**Comparison / evaluation slides** (options, criteria, trade-offs):
- Table or matrix format — structured into rows and columns
- Can be dense — 6-8 rows is fine if cells are short (2-5 words each)
- Mark the recommended option in content (e.g., bold label, '→ Recommended')

**Roadmap / timeline slides** (phased implementation, milestones):
- Phase-structured content — the builder decides the visual format
- Each phase: name + 2-3 key actions + timeline + owner
- More content than argument slides — acceptable because it's spatially organized

**Framework / architecture slides** (pillars, operating model, value chain):
- Element-based: short labeled items (3-8 words each) organized by category or hierarchy
- Can have many elements if the logical grouping is clear

**Deep-dive / detail slides** (supporting a framework or overview slide):
- Can carry more text than argument slides — up to 6-8 structured points
- Use sub-sections with bold headers to break content into scannable groups
- Often paired with the overview slide via numbering (see Framework-to-Deep-Dive Numbering)

**Exec summary slides**:
- 3-5 crisp bullets — this slide must stay tight regardless
- See dedicated section below

### What Makes Text a "Wall"

The problem isn't density — it's lack of structure. A slide with 8 short items in a well-organized table is readable. A slide with 3 long bullets that each run to 2-3 lines is not. Watch for:

- **Bullets longer than one line**: Either cut words or split into two items
- **Bullets that are really paragraphs**: A bullet with subclauses ("which..., resulting in..., thereby...") is prose with a dot in front of it
- **Missing visual structure**: If all the content is in one undifferentiated bullet list, add hierarchy — bold lead-ins, grouping headers, or convert to a different format (table, columns, diagram)
- **Setup language**: "Based on our analysis of..." / "It is worth noting that..." — start with the point

### Bullet Formats by Content Type

**Recommendations** — imperative verb + object + quantified impact:
```
• Launch enterprise sales motion — target $2M ARR in 12 months
• Consolidate three regional supply chains into one network — 15-20% cost reduction
• Hire VP Engineering by Q2 to unblock platform rebuild
```

**Findings / Insights** — declarative statement + supporting evidence:
```
• Enterprise customers churn at half the rate of SMB (4% vs. 9% annually)
• Top 3 competitors have no presence in APAC — greenfield opportunity
• Customer acquisition cost rose 40% in 18 months, outpacing LTV growth
```

**Actions / Next steps** — imperative verb + owner + timeline:
```
• Finalize vendor shortlist (Procurement, by Mar 15)
• Present business case to board (CFO, April board meeting)
• Launch Phase 1 pilot in Northeast region (Ops lead, Q2)
```

### Good vs. Bad Examples

| Bad (prose dump) | Good (distilled bullet) |
|---|---|
| "The company should consider consolidating its three regional supply chains into a single integrated network, which analysis suggests could reduce logistics costs by 15-20% while improving delivery times." | **Consolidate three regional supply chains into one network** — 15-20% logistics cost reduction, faster delivery |
| "Based on our analysis of customer segments, the enterprise segment shows the highest willingness to pay and lowest churn, suggesting the company should shift its go-to-market focus toward enterprise." | **Shift GTM focus to enterprise** — highest WTP, lowest churn, 3x LTV vs. SMB |
| "There is a significant opportunity to expand into the APAC market given that none of the top three competitors have established a meaningful presence in the region." | **Expand into APAC ahead of competitors** — none of top 3 have regional presence |
| "The implementation should be phased over three stages, starting with quick wins in the first quarter, followed by major organizational changes in months 3-12, and structural capability building over years 1-3." | **Phase implementation in 3 stages**: quick wins (Q1) → org changes (M3-12) → capability build (Y1-3) |

---

## Content Distillation Process

Between the approved storyline (Gate 1) and the HTML build (Gate 4), distill all content from Steps 6-7 into slide-ready form. This is a discrete step — do not skip it.

### The Process

1. **For each slide in the headline sequence**, identify the source material from Steps 6-7.
2. **Identify the slide's role** (argument, comparison, roadmap, framework, deep-dive) — this determines which content rules apply and signals the builder's visualization choice.
3. **Strip all connective prose**: Remove "Based on our analysis...", "This suggests that...", "It is worth noting...", "As discussed in...". Start with the point.
4. **Structure the content** for the chosen slide type: bullets for argument slides, table/matrix for comparisons, spatial layout for roadmaps/frameworks.
5. **Apply the wall-of-text test**: Can you enter the slide at any point and grasp individual pieces? If you have to read top-to-bottom like a document, restructure.

### What Gets Cut

- Hedging language ("it appears that", "potentially", "it could be argued")
- Setup sentences ("In order to understand X, we first need to...")
- Redundant evidence (keep the strongest data point, cut the rest)
- Qualifiers that don't change the point ("in most cases", "generally speaking")
- Attribution within bullets ("according to our analysis") — the slide IS the analysis

### Where Cut Content Goes

- **Appendix slides**: Supporting data, detailed breakdowns, methodology
- **Speaker notes**: Nuance, caveats, transition language, elaboration the presenter says aloud
- **The vertical document**: If the user needs both formats, the document carries the full narrative

---

## Executive Summary (Slides Format)

The exec summary slide is **3-5 crisp bullets**, not paragraphs. It follows the same bullet rules as content slides.

Adapts to narrative structure but **never uses framework labels**:
- **Answer-First**: Recommendation → supporting reasons → impact (as bullets)
- **Evidence-First**: Key signals → conclusion they point to (as bullets)
- **SCR**: Context → disruption → path forward (as bullets, no "Situation"/"Complication"/"Resolution")
- **Transformation**: Today → target → path (as bullets)
- **Comparative**: Decision → options → winner → why (as bullets)
- **Sequential**: Phases → timeline → outcome (as bullets)

**Spine test**: Exec summary bullets alone should convey the full argument. Slide titles alone should reconstruct the exec summary.

---

## Narrative-First, Not Data-First

**This is a thought leadership piece, not a quantitative research report.** Every slide must make sense without numbers. Numbers emphasize points — they never construct them.

- **Strip test**: Remove all numbers from a slide. If it becomes meaningless, the slide is structured wrong — rewrite around the insight.
- **Emphasis, not backbone**: Good: "Adoption is accelerating — enterprise deployments tripled last year." Bad: "Enterprise AI deployments reached 14,200 in 2024, up from 4,700 in 2023."
- **No data dumps**: If a slide has more than 2-3 numbers, question whether each one is pulling its weight.

Data integrity rules (freshness, cross-checking, fewer-is-better) are enforced at Step 5 — see `05-analyze.md` Data Quality and Consistency. The Sceptical Review Subagent (Gate 2) will catch anything that slips through.

---

## Structural Composition

### One Message Per Slide

If you can't state the slide's point in one sentence (the action title), the slide is doing too much.

### Source Footer

Any slide with numbers gets a `Source: [citation(s)]` line at the bottom (~8pt, light gray). Multiple sources separated by semicolons. No superscript footnotes. Omit only on slides with no quantitative content.

### Framework-to-Deep-Dive Numbering

When a framework slide has multiple blocks and subsequent slides detail each, use consistent numbering (Arabic, Roman, or letters) on both overview and detail slides.

---

## Building the Storyline

1. Select playbook and assemble slide sequence per `08-communicate.md` (Assembly Order + Q3-Q6 choices)
2. **Narrative-first test**: Read just the headlines — they should tell the complete story as a logical argument. If any headline only works because of a number, rewrite it to lead with the insight
3. **Number placement pass**: Only after the narrative is locked, decide where a specific number would strengthen a point. Most slides should work without any numbers
4. **Content distillation pass**: For each slide, distill source material from Steps 6-7 into the appropriate structured format. Strip all connective prose. Apply the wall-of-text test

---

## Pitfalls (Slides-Specific)

- **Prose masquerading as bullets**: A bullet that's a full sentence with subclauses is just a paragraph with a dot in front of it. Cut it down.
- **Inconsistent bullet structure**: If bullet 1 starts with a verb and bullet 3 starts with a noun phrase, the slide feels sloppy. Pick one structure and hold it.
- **Same slide type throughout**: A deck of 15 argument slides with 4 bullets each is monotonous. Mix slide types — argument, comparison table, roadmap, framework, stat callout — to maintain visual and structural variety.
- **Too many slides per point**: One argument = one slide. If you're spending 3 slides on one supporting recommendation, consolidate or the deck will feel padded.
- **Appendix avoidance**: The appendix exists for a reason. Detail-heavy content (methodology, full data tables, sensitivity analyses) belongs there, not crammed onto content slides.
- **Density without structure**: A dense slide is fine if the content is organized (tables, labeled sections, grouped elements). A dense slide is unreadable if it's a flat list of 10+ undifferentiated bullets.

---

## Saving the Content Spec (Gate 2b)

After content distillation is complete, save the distilled content as a **slide content file**. This file becomes the single source of truth for all deck generation.

### Process

1. **Distill all slides** using the process above — every slide should have its action title, content fields, and layout choice finalized.
2. **Read the format definition**: `references/08-slide-content-format.md` — this defines the exact schema, field names, primitive mapping, and rules.
3. **Write the spec file** to `{engagement_folder}/08-slide-content.md` following the format definition exactly.
4. **Present the spec to the user** for review. Walk through each slide's content. The user approves, requests changes, or rejects.
5. **Revise until explicit approval.** The approved spec is the final output of this skill for the slides track.

### What the Spec Captures

- Every slide's role and layout
- Every content field (eyebrow, title, body text, numbered points with optional sub-points, etc.)
- Data values embedded naturally in point text
- Source citations
- Slide ordering

### What the Spec Does NOT Capture

- Visual style, brand, theme, colors beyond named semantic colors
- CSS, HTML, grid coordinates, font choices
- Transitions, animations
- These belong to the builder skill downstream — not to this skill
