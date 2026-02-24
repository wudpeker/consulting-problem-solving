# Brand Styling Template

Copy this file, rename it to the brand name (e.g., `accenture.md`), and fill in all values. Place completed files in the `references/styles/` folder.

All color values are 6-digit hex WITHOUT the `#` prefix (e.g., `1E2761` not `#1E2761`). All sizes are in points unless noted otherwise. All dimensions are in inches unless noted otherwise.

---

## Metadata

```yaml
brand_name: ""
version: ""
last_updated: ""
notes: ""
```

---

## Slide Dimensions

```yaml
layout: "LAYOUT_16x9"    # LAYOUT_16x9 | LAYOUT_16x10 | LAYOUT_4x3 | LAYOUT_WIDE
```

---

## Typography

### Font Families

```yaml
heading_font: ""          # Used for slide titles, section headers, callout numbers
body_font: ""             # Used for body text, bullets, table cells
accent_font: ""           # Used for footnotes, source citations, captions (optional — falls back to body_font if blank)
```

### Size Scale

```yaml
slide_title: 36           # Main slide title
section_header: 24         # Sub-headers within a slide
body_text: 14              # Standard body copy and bullets
small_body: 12             # Secondary text, dense content
footnote: 9                # Source citations, disclaimers, footer text
callout_number: 60         # Large stat callouts (e.g., "$15M", "3x")
callout_label: 12          # Label beneath a callout number
```

### Weight and Style Defaults

```yaml
title_bold: true
section_header_bold: true
body_bold: false
footnote_italic: true
```

---

## Color Palette

### Core Brand Colors

```yaml
primary: ""               # Dominant brand color — used for title bars, key shapes, emphasis
secondary: ""             # Supporting brand color — used for secondary shapes, section accents
accent: ""                # High-contrast pop color — used sparingly for highlights, key data points
```

### Text Colors

```yaml
text_dark: ""             # Primary text on light backgrounds (usually near-black, e.g., 2D2D2D)
text_light: ""            # Text on dark backgrounds (usually white or near-white)
text_muted: ""            # De-emphasized text — footnotes, captions, secondary labels
```

### Background Colors

```yaml
bg_light: ""              # Light slide background (e.g., FFFFFF or F5F5F5)
bg_dark: ""               # Dark slide background — title slides, section dividers, conclusion
bg_alternate: ""          # Optional alternate background for visual variety (e.g., light gray)
```

### Chart Data Colors

Ordered sequence used for chart series, bars, and segments. List 6-8 colors from most to least prominent.

```yaml
chart_colors:
  - ""                    # Series 1 (typically primary)
  - ""                    # Series 2 (typically secondary)
  - ""                    # Series 3 (typically accent)
  - ""                    # Series 4
  - ""                    # Series 5
  - ""                    # Series 6
```

### Functional Colors

```yaml
positive: ""              # Growth, success, improvement (e.g., green)
negative: ""              # Decline, risk, warning (e.g., red)
neutral: ""               # Baseline, unchanged, informational (e.g., gray)
highlight: ""             # Background highlight for emphasis (e.g., light yellow)
```

---

## Layout Rules

### Margins and Spacing

```yaml
slide_margin: 0.5         # Minimum distance from content to slide edge (inches)
content_gap: 0.3          # Standard gap between content blocks (inches)
title_bar_height: 1.0     # Height of the title area at top of content slides (inches)
```

### Title Bar Style

```yaml
title_bar_style: "color_band"   # color_band | text_only | underline
title_bar_fill: ""              # Fill color for the title bar (if color_band). Leave blank to use primary.
title_bar_text_color: ""        # Text color on the title bar. Leave blank to auto-derive from fill.
```

### Footer

```yaml
show_footer: true
footer_text: ""                 # e.g., "Confidential — Do not distribute"
show_page_numbers: true
show_date: true
footer_font_size: 8
footer_color: ""                # Leave blank to use text_muted
```

---

## Logo

```yaml
logo_file: ""                   # Filename (placed in references/styles/logos/). Leave blank for no logo.
logo_placement: "bottom_right"  # top_left | top_right | bottom_left | bottom_right | title_only
logo_width: 1.0                 # Width in inches (height auto-scales to preserve aspect ratio)
logo_margin: 0.3                # Distance from slide edge (inches)
```

---

## Slide Type Overrides

Optional per-slide-type customization. Leave sections blank to inherit from the defaults above.

### Title Slide

```yaml
title_slide:
  bg_color: ""                  # Leave blank to use bg_dark
  title_size: 44
  title_color: ""               # Leave blank to use text_light
  subtitle_size: 20
  subtitle_color: ""            # Leave blank to use text_light with slight muting
  show_logo: true
```

### Section Divider Slide

```yaml
divider_slide:
  bg_color: ""                  # Leave blank to use primary
  text_color: ""                # Leave blank to use text_light
  text_size: 36
```

### Content Slide

```yaml
content_slide:
  bg_color: ""                  # Leave blank to use bg_light
  title_size: ""                # Leave blank to use slide_title from size scale
```

### Conclusion / Thank You Slide

```yaml
closing_slide:
  bg_color: ""                  # Leave blank to use bg_dark
  text_color: ""                # Leave blank to use text_light
  show_logo: true
```
