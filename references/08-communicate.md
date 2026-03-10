# Step 8: Communicate

Package all the work into a compelling deliverable. The best analysis is worthless if it isn't communicated clearly.

This step has two tracks with **different content rules**:
- **Slides (.pptx)**: Distilled, visual, one-message-per-slide. Read `08-slides-content.md` for content rules, then `08a-html-design.md` and `08b-pptx-convert.md` for production.
- **Vertical (.docx)**: Narrative prose, section depth, longer evidence chains. Read `08-vertical-content.md` for content rules, then generate with the docx skill.

Ask the user which format they want before proceeding. Then read **only** the relevant content rules file.

---

## INPUT Phase: Collect Narrative and Structure Preferences

Use **AskUserQuestion** to collect structured choices in 2 batches (up to 4 questions each).

### Batch 1: Narrative, Title

**Q1 — Narrative Structure** (header: "Narrative", multiSelect: false):
1. **Answer-First (Pyramid)** — Lead with conclusion, support with arguments, then evidence. Best for: aligned/senior/time-constrained audiences.
2. **Evidence-First (Build)** — Observations -> pattern -> conclusion. Best for: skeptical audiences, counterintuitive conclusions.
3. **Narrative Arc (SCR)** — Situation -> Complication -> Resolution. Best for: persuasion, audiences that need to feel the problem first.
4. **Transformation (Current -> Future -> Bridge)** — As-is -> to-be -> path. Best for: change management, vision-setting.
5. **Comparative Evaluation (Options -> Criteria -> Rec)** — Alternatives -> evaluation -> selection. Best for: board decisions, vendor selections.
6. **Sequential / Process (Step-by-Step)** — Temporal/logical order. Best for: implementation plans, project updates.

**Q2 — Title and Subtitle** (header: "Title"): Auto-generate from problem statement, or user enters custom.

### Batch 2: Structure, Page Count, Appendix

**Q3 — Executive Summary** (header: "Exec Summary"): Yes (recommended) / No.

**Q4 — Context & Objectives** (header: "Context"): Yes (recommended) / No.

**Q5 — Content Pages** (header: "Page Count"): Compact (4-6) / Standard (8-12) / Comprehensive (15-20) / Custom. Count excludes title, exec summary, and context slides/pages.

**Q6 — Appendix** (header: "Appendix"): Yes (recommended) / No.

### Follow-up Questions (conversational, after structured choices)

1. **Audience**: Who, what level, what they know
2. **Key message**: The one thing to remember
3. **Tone**: Bold/decisive vs. cautious/options-oriented
4. **Sensitive content**: Anything to frame carefully or put in appendix

---

## CRITICAL: No Literal Framework Labels

**Never use framework terminology as slide titles, section headers, or labels.** The frameworks shape structure — the audience sees only context-specific content.

Instead of "Situation" -> describe the actual context. Instead of "Complication" -> describe the actual disruption. Instead of "Resolution" -> describe the actual solution. Instead of "Current State" / "Future State" / "Bridge" -> describe what's happening, the vision, and the path.

**Exception**: "Executive Summary" is a standard navigational label and should be used as-is.

---

## Assembly Order

```
1. Title Slide/Page                    <- ALWAYS
2. Executive Summary                   <- if Q3 = Yes
3. Context & Objectives                <- if Q4 = Yes
4. Content Pages (per narrative)       <- count from Q5
5. Appendix                            <- if Q6 = Yes
```

### Frontmatter Template

```yaml
---
id: 08-final-deliverable
type: communication
step: 8
title: "Final Deliverable"
status: draft
addresses: "01-problem-definition.md#kq"
presents:
  - "07-recommendations.md#rec-core"
  - "06-synthesis.md#ans"
narrative_structure: answer-first  # answer-first | evidence-first | narrative-arc | transformation | comparative | sequential
format: slides  # slides | vertical
page_count: 0
---
```

---

## Narrative Structure Playbooks

Each playbook has two variants: a **slide sequence** (for the slides track) and a **section outline** (for the vertical track).

### 1. Answer-First (Pyramid)
**Arc**: Conclusion -> Supporting Arguments -> Evidence

**Slide sequence**:
```
Title -> [Exec summary] -> [Context] -> THE ANSWER (core rec) -> Argument 1 + evidence -> Argument 2 + evidence -> Argument 3 + evidence -> Implementation/next steps -> [Appendix]
```

**Section outline**:
```
Title page -> [Exec summary] -> [Context] -> The Recommendation (section) -> Argument 1 (section with sub-sections for evidence) -> Argument 2 -> Argument 3 -> Implementation Roadmap -> [Appendix]
```

### 2. Evidence-First (Build)
**Arc**: Observations -> Pattern -> Conclusion

**Slide sequence**:
```
Title -> [Exec summary] -> [Context] -> Observation 1 -> Observation 2 -> Observation 3 -> The pattern/insight -> Implication -> Recommendation -> Next steps -> [Appendix]
```

**Section outline**:
```
Title page -> [Exec summary] -> [Context] -> Key Observations (section per observation with supporting data) -> The Pattern (synthesis section) -> Implications -> Recommendation -> Next Steps -> [Appendix]
```

### 3. Narrative Arc (SCR)
**Arc**: Situation -> Complication -> Resolution

**Slide sequence**:
```
Title -> [Exec summary] -> [Context] -> Baseline context (2 slides) -> Disruption + stakes (2 slides) -> Key insight -> Recommendation -> Specific initiatives -> Quantified benefit -> Next steps -> [Appendix]
```

**Section outline**:
```
Title page -> [Exec summary] -> [Context] -> The Landscape (2-3 pages of baseline) -> What Changed (disruption, evidence, stakes) -> The Path Forward (insight + recommendation) -> Initiatives in Detail -> Expected Impact -> Next Steps -> [Appendix]
```

Use context-specific headlines — never label sections "Situation," "Complication," "Resolution."

### 4. Transformation (Current -> Future -> Bridge)
**Arc**: As-Is -> To-Be -> How to Get There

**Slide sequence**:
```
Title -> [Exec summary] -> [Context] -> Today's reality + what's broken -> The vision + what good looks like -> The path (initiatives) -> Roadmap -> [Appendix]
```

**Section outline**:
```
Title page -> [Exec summary] -> [Context] -> Where We Are Today (detailed current state) -> Where We Need to Be (vision with specifics) -> How We Get There (initiatives, phasing, ownership) -> Roadmap & Milestones -> [Appendix]
```

Never use "Current State," "Future State," "Bridge" as labels.

### 5. Comparative Evaluation
**Arc**: Alternatives -> Evaluation -> Selection

**Slide sequence**:
```
Title -> [Exec summary] -> [Context] -> The alternatives (1 slide each) -> Evaluation approach/criteria -> Comparative results -> Why winner wins -> Risks -> Implementation -> [Appendix]
```

**Section outline**:
```
Title page -> [Exec summary] -> [Context] -> Options Overview -> Option A (detailed section) -> Option B -> Option C -> Evaluation Framework & Criteria -> Comparative Analysis -> Recommendation & Rationale -> Risks & Mitigations -> Implementation -> [Appendix]
```

### 6. Sequential / Process
**Arc**: Phase 1 -> Phase 2 -> ... -> Phase N

**Slide sequence**:
```
Title -> [Exec summary] -> [Context] -> Overview (phases at a glance) -> Phase 1 + detail -> Phase 2 + detail -> ... -> Dependencies/risks -> Timeline/resources -> [Appendix]
```

**Section outline**:
```
Title page -> [Exec summary] -> [Context] -> Approach Overview -> Phase 1 (detailed section with activities, milestones, dependencies) -> Phase 2 -> ... -> Cross-Phase Risks & Dependencies -> Resource Requirements & Timeline -> [Appendix]
```

---

## Context & Objectives (when selected)

1. Why we're here (triggering event), 2. What was asked (question/scope), 3. How we approached it (1-2 sentences), 4. What success looks like (from Step 1).

---

## REVIEW Phase: Five Gates

### Slides Track

```
Gate 1 — Storyline:      Present headline sequence and structure. Get approval.
Gate 2 — Sceptical Review: Launch sceptical review subagent (see SKILL.md). Resolve MUST FIX items.
                           READ 08-slides-content.md for content distillation rules.
                           READ 08a-html-design.md BEFORE PROCEEDING to Gate 3.
Gate 3 — Visual Style:    Collect visual style + brand preferences. Confirm choices. (Defined in 08a-html-design.md)
Gate 4 — HTML Page:       Generate HTML, run automated QA, present to user. Get approval. (Defined in 08a-html-design.md)
                           READ 08b-pptx-convert.md BEFORE PROCEEDING
Gate 5 — PowerPoint:      Convert HTML to pptx, run visual QA with subagent. Present final file. (Defined in 08b-pptx-convert.md)
```

**Sequence is mandatory.** Do not skip gates. Do not read 08a until Gate 2 passes. Do not read 08b until Gate 4 passes.

### Vertical Track

```
Gate 1 — Storyline:       Present section outline and key messages. Get approval.
Gate 2 — Sceptical Review: Launch sceptical review subagent (see SKILL.md). Resolve MUST FIX items.
                            READ 08-vertical-content.md for prose and section rules.
Gate 3 — Visual Style:     Collect visual style + brand (see 08-vertical-content.md). Confirm choices.
Gate 4 — Document:         Generate document using docx skill. Present for review.
```

---

## Language Quality: Final Editing Pass

Before presenting, run all prose through editing per `references/writing-style.md`: cut filler, active voice, specific language, complete-sentence titles (slides) or strong topic sentences (vertical), read exec summary aloud. The goal is prose worthy of a top-tier consulting firm.

---

## Pitfalls

- **Topic titles instead of action titles**: "Q3 Revenue" tells nothing (applies to both tracks — slides use action titles, vertical uses strong section headings)
- **Wrong structure for audience**: Evidence-First for a time-constrained CEO is wrong
- **Building around numbers**: Numbers emphasize points, not construct them. If a slide/section is meaningless without its numbers, rewrite around the insight
- **Flabby prose**: Apply Strunk & White ruthlessly
- **Exposing framework scaffolding**: Never use literal framework labels as titles/headers
- **Skipping gates**: All gates must complete in sequence before building starts
- **Using slide rules for documents or vice versa**: Each track has its own content file — read and follow the right one
