# Step 8 — Vertical Track: Content Rules

Content rules for building vertical documents (.docx). Read this file after Gate 2 (sceptical review passed), before generating the document.

The core principle: **a document can breathe.** Unlike slides, you have space for argument, evidence, and nuance. Use that space well — tight prose, not bloat. Every paragraph earns its place, every section advances the argument.

---

## Section Heading Rule

The user chooses one of two styles at Gate 1 (or you ask if not yet decided):

### Option A: Action Headings (Recommended)
Section headings are **complete sentences stating the key message** — same principle as slide action titles, but adapted for documents.

| Bad (topic label) | Good (action heading) |
|---|---|
| "Market Analysis" | "The target market is large enough to sustain the growth thesis" |
| "Cost Structure" | "Rising input costs require a structural response, not incremental cuts" |
| "Competitive Position" | "No incumbent has locked up the market — the window remains open" |

### Option B: Topic Headings
Traditional section labels. Appropriate for formal reports, board documents, and audiences that expect conventional structure.

| Examples |
|---|
| "Market Overview" |
| "Competitive Landscape" |
| "Financial Impact Assessment" |
| "Implementation Roadmap" |

With topic headings, the **topic sentence** of each section's opening paragraph must carry the argumentative weight that the heading doesn't.

---

## Prose Rules

### The Paragraph Contract

Every paragraph follows a contract:
1. **Topic sentence**: States the paragraph's point. A reader skimming only topic sentences should follow the full argument.
2. **Evidence / development**: 2-3 sentences that support, explain, or qualify the point.
3. **Implication** (optional): What this means for the decision — the "so what?"

**Max 5 sentences per paragraph.** If a paragraph runs longer, it's making two points — split it.

### Sentence-Level Rules

- **Active voice by default.** Passive only when the actor is genuinely unknown or irrelevant.
- **Short sentences for key claims.** Long sentences for nuance and qualification. Vary rhythm.
- **Lead with the point, not the setup.** Cut "In order to understand X, it is important to first consider..." — start with X.
- **One idea per sentence.** If a sentence has two independent clauses joined by "and" or "but," consider splitting.
- **Specific over vague.** "$4.2M in annual savings" not "significant cost reduction." "Q2 2025" not "the near term."

### Connective Tissue

Unlike slides, documents need transitions between sections and paragraphs. But keep them lean:

| Bloated | Lean |
|---|---|
| "Having examined the market dynamics in the previous section, we now turn our attention to the competitive landscape." | "The competitive landscape reinforces this opportunity." |
| "It is also worth noting that, in addition to the factors discussed above, there are several other considerations." | "Three additional factors matter." |
| "Based on the analysis presented in the preceding sections, we can draw the following conclusions." | Cut entirely — just state the conclusions. |

---

## Section Depth

Documents allow layered depth that slides cannot. Use it deliberately:

```
# Main Section Heading (H1)
Opening paragraph with the section's core argument.

## Sub-section (H2)
Detailed argument or evidence thread.

### Sub-sub-section (H3)
Granular detail — data tables, methodology notes, worked examples.
Only use H3 when the section genuinely has sub-components.
```

**Depth rules**:
- H1 sections correspond roughly to slides in the slide track — one per major argument
- H2 sub-sections carry the detail that slides push to appendix
- H3 is rare in body sections — more common in appendices
- Never go deeper than H3

---

## Evidence Presentation

### Inline Evidence

Weave evidence into the narrative. Don't dump data points — integrate them:

| Bad (data dump) | Good (evidence woven into argument) |
|---|---|
| "Revenue was $42M in 2023, $38M in 2022, and $31M in 2021. This represents a CAGR of 16.4%. The industry average CAGR is 8.2%." | "Revenue has grown at roughly twice the industry rate — 16% CAGR over the past three years, reaching $42M in 2023 — driven primarily by enterprise expansion." |
| "Customer churn is 4% for enterprise, 9% for mid-market, and 14% for SMB. Enterprise NPS is 62, mid-market is 45, and SMB is 31." | "Enterprise customers are notably stickier: 4% churn and an NPS of 62, compared to 9%/45 for mid-market and 14%/31 for SMB. This pattern holds across all cohorts since 2021." |

### Tables in Documents

Tables work differently in documents than on slides:
- **Slides**: Tables are glanced at. Max 4-5 rows, key cells highlighted.
- **Documents**: Tables are studied. They can be larger (up to ~15 rows) and carry more detail.
- Every table needs an **introductory sentence** explaining what the reader should take from it.
- Every table needs a **source line** below it.

### Charts and Figures

- Introduce every chart with a sentence stating the takeaway — don't make the reader figure it out.
- Place charts close to the prose that references them, not collected at the end.
- Caption format: "Figure 1: [Descriptive title]. Source: [citation]."

---

## Executive Summary (Vertical Format)

The exec summary is **2-3 tight paragraphs**, not bullets. It reads as a condensed version of the full argument.

Structure adapts to narrative choice but **never uses framework labels**:
- **Answer-First**: State the recommendation, the 2-3 strongest reasons, and the expected impact.
- **Evidence-First**: Describe the key signals observed, the pattern they reveal, and the conclusion.
- **SCR**: Describe the context, what changed, and the recommended path forward.
- **Transformation**: Describe today's position, the target, and the path.
- **Comparative**: State the decision, the options evaluated, the winner, and why.
- **Sequential**: Summarize the phases, timeline, and expected outcome.

**Test**: A reader who reads only the exec summary should understand the full argument and the recommended action. They should be able to brief someone else from it.

---

## Recommendations in Vertical Format

Recommendations in documents get more space than on slides. Structure each recommendation as a mini-section:

```markdown
## [Action-oriented heading: imperative verb + object]

[1-2 sentence description of what this means in practice.]

**Rationale**: [2-3 sentences linking back to analysis findings. Cite specific evidence.]

**Expected impact**: [Quantified range with confidence level and basis.]

**Implementation**: [Key actions, owner, timeline — can use a short bullet list here.]

**Risks**: [1-2 key risks with mitigations, if material.]
```

This structure gives each recommendation enough space to be convincing while staying scannable. The heading and first sentence carry the point; the rest is supporting detail a reader can skim or study.

---

## Narrative-First, Not Data-First

Same principle as slides — every section must make sense without numbers. Numbers emphasize points, not construct them. Strip test: remove all numbers; if the argument collapses, rewrite around the insight. See `08-slides-content.md` § "Narrative-First" for full rules.

---

## Building the Section Outline

1. Select playbook matching Q1 choice (see `08-communicate.md` narrative playbooks — use the **section outline** variant)
2. Fill section headings using Steps 1-7 content
3. Include/exclude sections per Q3, Q4, Q6
4. Fit to scope from Q5 (page count is a softer constraint for documents — content depth matters more than page count)
5. **Argument flow test**: Read just the section headings (H1 and H2). They should tell a coherent story. If a heading is vague ("Additional Considerations"), sharpen it or cut the section.
6. **Evidence mapping**: For each section, note the 2-3 key data points from Step 5 that will appear. This prevents data dumps — you know in advance which numbers are earning their place.

---

## Source Citations

Every section that quotes numbers includes a `Source: [citation(s)]` line at the end (8-9pt, gray). Multiple sources separated by semicolons. Same format as slides but placed at section end rather than slide footer.

For documents with many sources, consider a "Sources" section in the appendix with full references, using abbreviated inline citations.

---

## Pitfalls (Vertical-Specific)

- **Slide content pasted into paragraphs**: Bullets strung together with "and" and "additionally" don't make prose. Write the argument fresh.
- **Wall of text**: If a section has no sub-headings, tables, or figures for more than a page, it needs visual relief.
- **Buried recommendations**: Each recommendation needs its own visible section heading. Don't bury "we recommend..." inside a paragraph.
- **Over-documenting**: Not every finding needs to appear in the body. Use the appendix for supporting detail that doesn't advance the core argument.
- **Executive summary that's a table of contents**: "Section 1 covers... Section 2 examines..." is navigation, not an executive summary. State the argument.
