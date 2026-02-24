# Accenture Strategy & Consulting — Brand Styling

## Metadata

```yaml
brand_name: "Accenture"
version: "1.0"
last_updated: "2026-02-24"
notes: "Purple-dominant brand. Uses neutrals (black/gray) for 55% of visual weight, core purples for 35%, and accent purples + secondaries for 10%. Graphik is the core brand font; GT Sectra Fine is used for subtitles and sub-headlines on covers and dividers. Falls back to Arial if custom fonts unavailable. Purple '>' chevron appears bottom-left on all slides."
```

---

## Slide Dimensions

```yaml
layout: "LAYOUT_16x9"
```

---

## Typography

### Font Families

```yaml
heading_font: "Graphik"          # Graphik Bold for headlines. Fallback: Arial Black
body_font: "Graphik"             # Graphik Regular for body text. Fallback: Arial
accent_font: "GT Sectra Fine"    # Used for subtitles on covers/dividers. Fallback: Georgia
```

### Size Scale

```yaml
slide_title: 36                  # Content slide headline (min 30pt)
section_header: 20               # Subtitle / sub-heading on content slides
body_text: 20                    # Single-column body text (use 18pt for two-column layouts)
small_body: 18                   # Two-column body text, level 4-5 bullets
footnote: 12                     # Level 6 text, source citations, footnotes
callout_number: 54               # Large stat callouts, key messages, section divider titles
callout_label: 14                # Label beneath callout number or presenter name
```

### Weight and Style Defaults

```yaml
title_bold: true
section_header_bold: false       # Subtitles are in accent_font (GT Sectra Fine), regular weight
body_bold: false
footnote_italic: false
```

### Bullet Hierarchy

```yaml
# Accenture uses a specific bullet alternation pattern:
# Level 1: bullet (•), 20pt (18pt in two-col)
# Level 2: en dash (–), 20pt (18pt in two-col)
# Level 3: bullet (•), 20pt (18pt in two-col)
# Level 4: en dash (–), 18pt (16pt in two-col)
# Level 5: bullet (•), 18pt (16pt in two-col)
# Level 6: no bullet, 12pt
```

---

## Color Palette

### Core Brand Colors

```yaml
primary: "A100FF"                # Accenture purple — dominant brand color
secondary: "7500C0"              # Deep purple — used in gradients, darker accents
accent: "460073"                 # Dark purple — gradient anchor, dark-mode base
```

### Text Colors

```yaml
text_dark: "000000"              # Primary text on light backgrounds (pure black per brand)
text_light: "FFFFFF"             # Text on dark/purple backgrounds
text_muted: "808080"             # De-emphasized text — footnotes, captions
```

### Background Colors

```yaml
bg_light: "FFFFFF"               # Content slide background
bg_dark: "460073"                # Dark purple — used as gradient start on covers/dividers
bg_alternate: "F2F2F2"           # Light gray for subtle contrast
```

### Gradient Definitions

```yaml
# Accenture uses purple-to-pink/orange gradients on covers, dividers, and closing slides.
# These are multi-stop gradients — approximate with the start and end colors:
gradient_start: "460073"         # Deep purple (top-left)
gradient_end: "D4A0E8"          # Soft pink/lavender (bottom-right)
# Some variants include warm tones:
gradient_warm_end: "F4A261"      # Peach/orange (used on some divider variants)
```

### Chart Data Colors

```yaml
chart_colors:
  - "A100FF"                     # Purple (primary)
  - "7500C0"                     # Deep purple
  - "0041C2"                     # Blue (secondary)
  - "00B4AA"                     # Teal (secondary)
  - "00C853"                     # Green (secondary)
  - "FF6D00"                     # Orange (secondary)
  - "FFD600"                     # Yellow (secondary)
  - "FF4081"                     # Coral/pink (secondary)
```

### Functional Colors

```yaml
positive: "00C853"               # Green — growth, success
negative: "FF1744"               # Red — decline, risk
neutral: "808080"                # Gray — baseline, unchanged
highlight: "F3E5FF"              # Very light purple — background emphasis
```

### Table Colors

```yaml
table_header_fill: "A100FF"      # Purple header row
table_header_text: "FFFFFF"      # White text on header
table_body_text: "000000"        # Black body text
table_border: "D0D0D0"          # Light gray borders
table_alt_row: "F8F8F8"         # Subtle alternating row shading (optional)
```

---

## Layout Rules

### Margins and Spacing

```yaml
slide_margin: 0.5
content_gap: 0.3
title_bar_height: 1.0
```

### Title Bar Style

```yaml
title_bar_style: "text_only"     # Content slides: headline text on white, no color band
title_bar_fill: ""
title_bar_text_color: "000000"   # Black headline text on content slides
```

### Subtitle Style

```yaml
subtitle_color: "A100FF"         # Purple subtitle text (GT Sectra Fine) on content slides
```

### Footer

```yaml
show_footer: true
footer_text: "Copyright © 2025 Accenture. All rights reserved."
show_page_numbers: true
show_date: false
footer_font_size: 8
footer_color: "808080"
```

### Brand Mark

```yaml
# Purple ">" chevron appears bottom-left on all slides
chevron_color: "A100FF"          # Purple on light backgrounds
chevron_color_dark: "FFFFFF"     # White on dark/gradient backgrounds
chevron_placement: "bottom_left"
```

---

## Logo

```yaml
logo_file: ""                    # Accenture wordmark + ">" — place in styles/logos/ if available
logo_placement: "top_right"      # Logo top-right on title slides
logo_width: 1.5
logo_margin: 0.4
```

---

## Slide Type Overrides

### Title Slide

```yaml
title_slide:
  bg_color: "FFFFFF"             # White background (main variant)
  title_size: 60                 # 60pt for short titles; use 48pt if title exceeds 2 lines
  title_color: "000000"          # Black, Graphik Bold
  title_max_lines: 3
  subtitle_size: 24              # GT Sectra Fine, purple
  subtitle_color: "A100FF"
  presenter_size: 14             # Presenter name, bottom-left
  presenter_color: "000000"
  show_logo: true                # Accenture logo top-right
  show_business_unit: true       # "Accenture Strategy & Consulting" bottom-right
```

### Section Divider Slide

```yaml
divider_slide:
  bg_color: "gradient"           # Purple-to-pink gradient (see Gradient Definitions)
  text_color: "FFFFFF"
  text_size: 54                  # Graphik Bold
  subtitle_size: 24              # GT Sectra Fine
  subtitle_color: "FFFFFF"
```

### Content Slide

```yaml
content_slide:
  bg_color: "FFFFFF"
  title_size: 36                 # Min 30pt, Graphik Bold, black
  subtitle_size: 20              # GT Sectra Fine, purple
  subtitle_color: "A100FF"
```

### Key Message Slide

```yaml
key_message_slide:
  bg_color: "gradient"           # Purple gradient
  text_color: "FFFFFF"
  text_size: 54                  # Centered, Graphik Bold
  text_align: "center"
  text_valign: "middle"
```

### Conclusion / Thank You Slide

```yaml
closing_slide:
  bg_color: "gradient"           # Purple-to-pink gradient with ">" chevron motif
  text_color: "FFFFFF"
  text_size: 54                  # "Thank You" in Graphik Bold
  show_logo: false               # Chevron motif replaces logo
```
