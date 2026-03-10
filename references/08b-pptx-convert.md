# Step 8b: PowerPoint Conversion

Convert the approved HTML landing page into a `.pptx` file using PptxGenJS. The HTML is a **beautiful web experience** — not a slide deck preview. Your job is to **interpret** its design language and content, then build a PowerPoint that carries the same visual DNA adapted to slides.

## Prerequisites

Before reading this file, Gate 4 must be complete:
- HTML landing page generated, QA'd, and approved by the user

## The Interpretation Challenge

The HTML landing page is a continuous vertical web experience. PowerPoint is discrete 16:9 slides. These are fundamentally different media. You are NOT copying cards one-to-one. You are:

1. **Extracting the design system** — colors, fonts, visual treatments, spatial hierarchy
2. **Extracting the content** — structured text, data, visuals from each section
3. **Determining slide boundaries** — deciding how the continuous flow maps to discrete slides
4. **Translating the aesthetic** — carrying the landing page's visual character into what PowerPoint can do well

---

## Step 1: Extract the Design System

Read the `:root` CSS custom properties to get:
- Colors (strip `#` prefix for pptx — all hex values must be 6-char without `#`)
- Font families (map to available system fonts if web fonts were used)
- Font sizes (convert rem to pt: `rem * 16 = pt`)
- Spacing values (convert rem/px to inches: `px / 96 = inches`)

Note the visual treatments used across sections:
- Which sections use dark backgrounds vs. light?
- What accent colors appear and where?
- How does the page create visual rhythm — alternating backgrounds, stat callout bands, transition sections?
- What decorative elements exist — gradients, shapes, textures, borders?

---

## Step 2: Map Sections to Slides

Read each `[data-section]` element and its `data-content` attribute. Then decide the slide mapping:

### Mapping Rules

| HTML Section Type | Typical Slide Mapping |
|---|---|
| `hero` | 1 **cover slide** (see Cover Slide below) |
| `exec-summary` | 1 exec summary slide |
| `argument` | 1 slide per argument section |
| `stats` | 1 slide — or merge into adjacent argument slide if only 2-3 stats |
| `comparison` | 1-2 slides depending on density (split if >6 rows) |
| `roadmap` | 1-2 slides (overview + detail, or single if compact) |
| `framework` | 1 overview slide + 1 per deep-dive if needed |
| `transition` | Usually merged — the transition statement becomes the action title of the next slide. Only create a standalone divider slide if the narrative needs a clear break. |
| `closing` | 1 closing/next-steps slide |
| `appendix` | 1 slide per appendix topic |

**The HTML will have more sections than the deck has slides.** That's expected — the web format uses stat callout bands, transition sections, and visual breaks that don't need their own slides. Merge, combine, or absorb these into adjacent slides.

### Deciding Slide Boundaries

For each HTML section, ask:
1. Does this section make a **distinct point** that needs its own slide? → Own slide.
2. Is this section a **visual punctuation** (stat callout, transition quote) that supports an adjacent section? → Merge into the adjacent slide.
3. Is this section **too dense** for one slide? → Split into 2 slides.

Present the proposed slide mapping to yourself as a checklist before building — section N → slide M, with rationale for merges and splits.

### Cover Slide

The HTML hero section is an immersive full-viewport web experience — that does NOT translate directly to PowerPoint. The deck needs a **traditional PowerPoint cover slide** that follows presentation conventions while inheriting the landing page's design DNA.

**Required elements**:
- **Title**: The deck title (from the hero `<h1>` or the approved storyline)
- **Subtitle**: Client name, project name, or a one-line framing statement
- **Date**: Presentation date
- **Presenter / team**: Name(s) and role(s), if known (ask the user if not provided)
- **Logo**: Client or firm logo, if a brand file is selected

**Design approach**:
- Extract the hero section's **background treatment** (dark/light, gradient, accent color) and apply it to the cover slide background
- Use the hero's **typography scale** — large commanding title, smaller subtitle — but arrange it for a centered or structured slide layout, not a web hero
- If the hero uses a gradient or texture, render it as a background image for the slide
- Keep the cover clean and uncluttered — no bullets, no body text, no data. Just title, subtitle, metadata, and visual presence.
- If a brand file exists, follow its cover slide specifications (logo placement, footer, colors)

**What NOT to do**:
- Don't try to recreate the web hero layout on a slide (full-bleed images, scroll-triggered elements, etc.)
- Don't skip the cover and jump straight to the exec summary — every deck needs a proper opening slide
- Don't add content beyond the title/subtitle/metadata — the cover sets the tone, it doesn't make an argument

---

## Step 3: Translate the Visual Language

### From Web to PowerPoint

The landing page's aesthetic must come through in the deck. Translate intelligently:

| Web Treatment | PowerPoint Translation |
|---|---|
| Dark hero section with large title | Traditional cover slide: title, subtitle, date, presenter, logo — with hero's background treatment (see Cover Slide) |
| Alternating light/dark section backgrounds | Alternating slide backgrounds (mirror the rhythm) |
| Full-bleed gradient or texture background | Slide background image (render gradient as PNG if needed) |
| Stat callout band (large numbers in a row) | Large `addText` callout numbers with labels, centered |
| Side-by-side comparison layout | Two-column slide layout (x positions calculated) |
| Horizontal timeline | Timeline diagram using shapes and lines |
| Transition/quote band | Divider slide with centered quote on dark background — or merge into next slide's title |
| Icon grid | Icons with labels arranged in grid using shapes |
| Asymmetric two-column (60/40) | Proportional column widths (e.g., x=0.5 w=5.4 / x=6.2 w=3.3) |

### What to Keep

- **Color palette**: Use the exact CSS variable colors throughout
- **Font pairing**: Map web fonts to system fonts (see table below)
- **Visual rhythm**: If the HTML alternates dark/light sections, the deck should alternate dark/light slides
- **Hierarchy**: The size relationships between titles, body, and callouts should feel proportionally similar
- **Character**: If the page feels bold and dark, the deck should feel bold and dark. If minimal and airy, same.

### What to Adapt

- CSS effects that don't exist in pptx (complex gradients, blur, advanced shadows) — simplify or use background images
- Scroll animations, hover states — drop entirely
- Full-bleed layouts — adapt to 10" × 5.625" with 0.5" margins
- Continuous flow between sections — each slide must stand alone

### What to Drop

- Navigation elements, scroll indicators
- Motion/animation (unless using pptx native animations, which are usually not worth the effort)
- Responsive breakpoints

---

## Font Mapping

If the HTML uses Google Fonts or web-only fonts, map to the closest available system font:

| Web Font | System Fallback |
|---|---|
| Google Sans / Poppins | Calibri |
| Playfair Display | Georgia |
| Source Sans Pro | Calibri |
| Merriweather | Georgia |
| Montserrat | Arial |
| Lora | Palatino |
| Fira Sans | Calibri |
| DM Serif Display | Cambria |

If a brand file specifies fonts, **always use the brand file fonts** for pptx regardless of what the HTML used.

---

## Layout Translation

PowerPoint slides are 10" x 5.625" (16:9). Standard positions:

- **Full-width content**: x=0.5, w=9, leaving 0.5" margins
- **Two columns**: Left: x=0.5, w=4.25 / Right: x=5.25, w=4.25 (0.5" gap)
- **Three columns**: x=0.5/3.5/6.5, w=2.7 each (0.3" gaps)
- **Asymmetric 60/40**: Left: x=0.5, w=5.4 / Right: x=6.2, w=3.3
- **Title area**: y=0.3 to y=1.0 (top 1" of slide)
- **Content area**: y=1.2 to y=5.0
- **Footer/source**: y=5.2, small font, muted color

---

## Color Translation

- Strip `#` prefix from all hex values
- Never use 8-char hex (no alpha channel in color strings) — use `transparency` property on `fill` instead
- Map CSS `opacity` to pptx `fill.transparency` (opacity 0.5 = transparency 50)

---

## Brand File Integration

If a brand styling file was selected in Gate 3, use it as the **authoritative source** for pptx-specific values:

- Font families → use exactly as specified (with fallbacks)
- Font sizes → use the pt values directly
- Colors → use the hex values directly (already without `#`)
- Layout rules → margins, content gaps, title bar height
- Footer → text, font size, color, page numbers, date
- Logo → placement, size, margin
- Slide type overrides → per-slide background, title size, colors

The HTML design should already reflect the brand file, but if there are discrepancies, the **brand file wins** for pptx-specific properties (margins in inches, sizes in points).

---

## Build Process

### 1. Set Up the Script

```javascript
const pptxgen = require("pptxgenjs");
let pres = new pptxgen();
pres.layout = "LAYOUT_16x9";
pres.author = "...";
pres.title = "...";
```

### 2. Define Helpers

Create helper functions for repeated elements (fresh objects each time — never reuse option objects):

```javascript
// Factory functions to avoid object mutation issues
const makeShadow = () => ({ type: "outer", blur: 6, offset: 2, color: "000000", opacity: 0.15, angle: 135 });
const makeAccentBar = (y, h, color) => ({ shape: pres.shapes.RECTANGLE, x: 0.5, y, w: 0.08, h, fill: { color } });
```

### 3. Build Slides Per the Section-to-Slide Mapping

For each slide in the mapping:
1. Create slide: `let slide = pres.addSlide()`
2. Set background — mirror the HTML section's background treatment (dark/light/accent/gradient)
3. Add title (action title from the section's `<h1>`)
4. Add content elements — translate the HTML section's structured content into pptx elements
5. Add source footer if the section has numbers
6. Add page number / footer if brand requires it

### 4. Write File

```javascript
pres.writeFile({ fileName: "output.pptx" });
```

---

## Gate 5: PowerPoint QA

After generating the pptx, run the standard pptx QA process.

### Content QA

```bash
python -m markitdown output.pptx
```

Check for missing content, typos, wrong slide order.

### Visual QA

Convert to images and use a **QA subagent** (fresh eyes):

```bash
python scripts/office/soffice.py --headless --convert-to pdf output.pptx
pdftoppm -jpeg -r 150 output.pdf slide
```

Subagent prompt:

```
Visually inspect these slides. Assume there are issues — find them.

These slides were built by interpreting a beautifully designed HTML landing page. The deck should carry the same visual DNA — colors, fonts, hierarchy, and character — adapted for PowerPoint. It should NOT look like a generic template deck.

Compare against the approved HTML landing page. Look for:
- Does the deck carry the landing page's visual character? (color palette, typography, dark/light rhythm)
- Overlapping elements (text through shapes, lines through words)
- Text overflow or cut off at edges/box boundaries
- Source citations or footers colliding with content above
- Elements too close (< 0.3" gaps) or sections nearly touching
- Uneven gaps (large empty area in one place, cramped in another)
- Insufficient margin from slide edges (< 0.5")
- Columns or similar elements not aligned consistently
- Low-contrast text (light text on light background, dark on dark)
- Text boxes too narrow causing excessive wrapping
- Color or font mismatches from the HTML design
- Missing visual elements that were present in the HTML
- Brand styling inconsistencies (if a brand was applied)
- Slides that feel generic or templated compared to the HTML's design quality

For each slide, list issues or areas of concern, even if minor.

Read and analyze these images:
[list slide image paths with expected descriptions]
```

### Fix and Re-verify

1. Fix all issues found
2. Re-convert affected slides to images
3. Re-inspect until a full pass reveals no new issues

**Do not declare success until you've completed at least one fix-and-verify cycle.**

### Present to User

Present the final `.pptx` file. Offer iteration:
- Check exec summary, flow, details, visual style, tone
- Compare against the HTML landing page for design fidelity
- Multiple revision rounds are normal

---

## Common Pitfalls

Refer to the pptx skill's `pptxgenjs.md` for the full list of PptxGenJS pitfalls. The critical ones for conversion:

1. **No `#` in hex colors** — causes file corruption
2. **No 8-char hex** — use `opacity`/`transparency` properties instead
3. **No `transparency` on `line` or text** — only valid on `fill` and `image`
4. **No negative `w` or `h` on LINE shapes** — PowerPoint rejects them
5. **Never reuse option objects** — PptxGenJS mutates them in-place
6. **No `ROUNDED_RECTANGLE` with accent borders** — corners won't align
7. **No gradient fills** — use gradient images as backgrounds instead
8. **Test in PowerPoint, not just LibreOffice** — LibreOffice is far more lenient
9. **Don't replicate web layouts literally** — a beautiful landing page section with 3 visual layers and a gradient becomes a clean slide with the same content and color, not a pixel-perfect copy of the web layout
