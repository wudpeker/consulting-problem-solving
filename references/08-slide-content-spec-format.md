# Slide Content Spec — Format Definition

This file defines the format for `08-slide-content-spec.md` — the engagement-specific file that serves as the **single source of truth** for all slide content. The deck builder (html-slide-deck-editor or pptx skill) reads this file verbatim. No rephrasing, no re-interpretation.

---

## Purpose

The slide content spec captures the output of content distillation (Gate 2b) in a structured, builder-readable format. It separates **what to say** (this spec) from **how it looks** (visual style, theme, colors, visualization choices — handled by the deck builder at Gate 3).

**Key invariant:** Regenerating a deck from the same spec file produces identical content. Only visual treatment changes.

---

## Separation of Concerns

| This spec decides | The deck builder decides |
|---|---|
| What text appears on each slide | Colors, fonts, sizes |
| Slide roles and logical structure | Which visualization type to use (bar, donut, progress) |
| Data values and their labels | How to render data visually |
| Content grouping (numbered points) | Visualization type for points (cards, panels, nodes, metric blocks) |
| Slide ordering | Transitions, animations |
| | Background contrast (light/dark) |

**Rule:** If it's about *what to communicate*, it belongs in the spec. If it's about *how it looks*, it belongs with the builder.

---

## File Structure

```markdown
# Slide Content Specification
<!-- Generated: {date} -->
<!-- Engagement: {client}/{project} -->
<!-- SINGLE SOURCE OF TRUTH — deck builder uses this verbatim -->

---

## Slide {N} — {Short Label}
- **Role**: {role}
- **Layout**: {layout}
- **Eyebrow**: {UPPERCASE LABEL}
- **Title**: {Action title — complete sentence stating key insight}
- {Content fields per slide type...}
- **Source**: {citation(s)}

---

## Slide {N+1} — {Short Label}
...
```

---

## Field Reference

### Metadata Fields

| Field | Required | Values | Notes |
|-------|----------|--------|-------|
| **Role** | Yes | See Role Values below | Declares slide purpose — informs builder's layout and visual choices |
| **Layout** | Yes | `hero`, `multi-col`, `split`, `full-width-stack`, `centered`, `step-flow`, `metric-row` | Structural layout hint for the deck builder |

### Content Fields

| Spec Field | What It Contains | Notes |
|------------|-----------------|-------|
| Eyebrow | Uppercase category label | e.g., "MARKET OPPORTUNITY" |
| Title | Action title — complete sentence | States the slide's key insight |
| Hero Title | Multi-line display text | Lines listed as `- "text"` items |
| Body Text | Paragraph or bullet list | Bullets prefixed with `- ` |
| Point N | Numbered content point | Single line or with indented sub-points (`  - detail`) |
| Callout Bar | Key takeaway statement | One sentence |
| Quote | Attributed quotation | Sub-fields: Text, Attribution |
| Source | Citation(s) | Footer reference line |

---

## Role Values

| Role | Typical Layout | When to Use |
|------|---------------|-------------|
| `cover` | hero | Opening slide — title, subtitle, branding |
| `section-divider` | hero | Separates major sections |
| `executive-summary` | full-width-stack | 3-5 bullet overview of entire argument |
| `context` | full-width-stack or split | Background, triggering event, objectives |
| `argument` | multi-col or split | Single point with supporting evidence |
| `comparison` | split | Two alternatives side by side |
| `roadmap` | full-width-stack | Phased implementation with timeline |
| `framework` | multi-col or step-flow | Pillars, operating model, architecture |
| `deep-dive` | full-width-stack | Detail supporting an overview slide |
| `metrics` | metric-row or multi-col | Quantitative dashboard |
| `closing` | hero | Thank you, next steps, contact |
| `appendix` | full-width-stack | Supporting detail, methodology, data tables |

---

## Slide Type Examples

### Cover

```markdown
## Slide 1 — Cover
- **Role**: cover
- **Layout**: hero
- **Eyebrow**: STRATEGIC REVIEW
- **Hero Title**:
  - "The Future of"
  - "Digital Commerce"
- **Body Text**: Prepared for Board of Directors | March 2026
```

### Executive Summary

```markdown
## Slide 2 — Executive Summary
- **Role**: executive-summary
- **Layout**: full-width-stack
- **Eyebrow**: EXECUTIVE SUMMARY
- **Title**: Three strategic shifts will unlock $200M in new revenue
- **Body Text** (bullets):
  - Shift GTM focus to enterprise — highest WTP, lowest churn, 3x LTV vs. SMB
  - Expand into APAC ahead of competitors — none of top 3 have regional presence
  - Consolidate supply chains into one network — 15-20% cost reduction
- **Callout Bar**: Target: $200M incremental revenue by 2028
- **Source**: Internal analysis; McKinsey Digital Commerce Report 2025
```

### Argument (multi-col with points)

```markdown
## Slide 3 — Enterprise Drives Revenue
- **Role**: argument
- **Layout**: multi-col (3)
- **Eyebrow**: MARKET OPPORTUNITY
- **Title**: Enterprise customers drive the majority of revenue and all of the margin
- **Point 1**: Revenue share — 62% of total revenue from enterprise
- **Point 2**: Net retention — 118% enterprise vs. 94% SMB
- **Point 3**: Gross margin — 78% enterprise vs. 45% SMB
- **Callout Bar**: Enterprise = highest LTV and lowest acquisition cost
- **Source**: FY2025 segment analysis
```

### Comparison (split with points)

```markdown
## Slide 4 — Competitive Landscape
- **Role**: comparison
- **Layout**: split
- **Eyebrow**: COMPETITIVE POSITION
- **Title**: No incumbent has locked up the market — the window is open
- **Point 1**: Current players — top 3 hold 28% combined share, no dominant player
  - In market and growing, but fragmented
- **Point 2**: Our position — first-mover advantage in APAC
  - None of top 3 have meaningful APAC presence
- **Source**: Competitive intelligence review Q4 2025
```

### Roadmap (full-width-stack with points)

```markdown
## Slide 5 — Implementation Roadmap
- **Role**: roadmap
- **Layout**: full-width-stack
- **Eyebrow**: IMPLEMENTATION
- **Title**: Three phases over 18 months, starting with enterprise GTM in Q2
- **Point 1**: Enterprise GTM — Q2-Q3 2026 | Hire VP Sales, build enterprise pipeline, close 5 anchor accounts
- **Point 2**: APAC Expansion — Q4 2026-Q1 2027 | Singapore office, 3 local partnerships, regulatory compliance
- **Point 3**: Supply Chain — Q2-Q3 2027 | Consolidate to single network, 15-20% cost savings target
- **Callout Bar**: Total investment: $12M over 18 months; payback in 24 months
- **Source**: Implementation planning team estimates
```

### Metrics (metric-row with points)

```markdown
## Slide 6 — Performance Dashboard
- **Role**: metrics
- **Layout**: metric-row (3)
- **Eyebrow**: KEY METRICS
- **Title**: Three indicators confirm the enterprise thesis is working
- **Point 1**: Enterprise ARR — $4.2M (+34% YoY)
- **Point 2**: Net Revenue Retention — 118% (+6pp vs. prior year)
- **Point 3**: Enterprise Churn — 4.2% (-1.8pp vs. prior year)
- **Source**: FY2025 financial data
```

### Section Divider

```markdown
## Slide 7 — Section Break
- **Role**: section-divider
- **Layout**: hero
- **Eyebrow**: PART TWO
- **Hero Title**:
  - "Market"
  - "Opportunity"
```

### Closing

```markdown
## Slide 8 — Closing
- **Role**: closing
- **Layout**: hero
- **Eyebrow**: NEXT STEPS
- **Hero Title**:
  - "Ready to"
  - "Move Forward"
- **Body Text**: Contact: team@company.com | Follow-up session: April 2026
```

---

## Format Rules

1. **Horizontal rules (`---`) between slides** — clear visual boundaries
2. **Slide numbering is sequential** — `## Slide 1`, `## Slide 2`, etc.
3. **Short label after the number** — `## Slide 3 — Enterprise Drives Revenue`
4. **Text is verbatim** — the deck builder copies it exactly, no rephrasing
5. **No visual or formatting instructions** — no colors, icons, visualization types, font sizes, CSS, HTML, or grid coordinates
6. **No framework labels as titles** — "Situation", "Complication", "Resolution" never appear
7. **Multi-col and metric-row specify count** — `multi-col (3)`, `metric-row (4)`
8. **Body Text format** — plain text for paragraphs, `(bullets):` suffix with `- ` prefixed items for bullet lists
9. **Source is optional** — include on any slide with quantitative claims; omit on cover, divider, closing slides
10. **Data values inline** — numbers, percentages, and trends are embedded naturally in point text, no rendering hints (the builder decides bar vs. donut vs. progress)
11. **Point sub-points are optional** — `Point 1` can be a single line or have indented sub-points for detail

---

## Anti-Patterns

| Don't | Why | Do Instead |
|-------|-----|------------|
| Specify colors (`red`, `teal`, `#FF0000`) | Builder picks colors from theme | Just provide the content |
| Specify visualization types (`progress-bar`, `donut`) | Builder decides how to render data | Provide the data value and label |
| Add icon names or badge colors | Visual treatment is builder's job | Describe the content semantically |
| Specify font sizes or families | Theme handles typography | Omit — builder applies from theme |
| Add CSS or HTML | Spec is content, not code | Use field names only |
| Use topic-label titles | Violates action title rule | Write complete insight sentences |
| Write prose paragraphs in Body Text | Slides need structured content | Use bullets or short statements |
| Repeat content across slides | One message per slide | Move supporting detail to appendix |
| Add transition/animation instructions | Builder handles transitions | Omit — builder decides |
| Add a `**Visual**` field or per-slide visual direction | Visual decisions are the builder's job — it infers from role + content | Omit — describe only what to communicate |

---

## What the Builder Infers

The deck builder uses the spec's **role**, **layout**, and **point structure** to choose visualization autonomously:

- **Role** → the primary semantic signal. `argument` → cards or columns, `comparison` → side-by-side panels, `roadmap` → timeline nodes, `metrics` → metric blocks, `framework` → pillars or step-flow. The builder picks the best visual treatment for the role.
- **Point count + Layout** → determines grid structure. `multi-col (3)` with 3 points → three-column layout. `split` with 2 points → left/right panels.
- **Point text** → builder parses content semantically. Numbers and percentages become emphasized metrics. Pipe-separated segments (`Q2-Q3 2026 | description`) become structured fields. Sub-points become detail items within the visual element.
- **Hero Title lines** → builder applies accent/emphasis styling per theme
- **Background contrast** → builder decides light/dark based on role and theme. Cover, section-divider, closing default to dark; content slides default to light. Theme can override.

The spec author never needs to think about visual rendering. Write the content as numbered points; the builder infers cards, panels, timeline nodes, metric blocks, or any other visualization from the role and content.
