---
name: creating-presentations
description: Creates HTML slide presentations using a specific design system with dark gradient backgrounds, glass effects, and violet accents. Use when asked to create slides, presentations, or decks. Provides layouts for title slides, text slides, bullet lists, quotes, stats, columns, and image+text combinations.
---

# Creating Presentations

This skill creates standalone HTML presentations. Each presentation is a single `.html` file containing all styles, markup, and navigation JavaScript.

## Quick Reference

| Layout | Class | Use For |
|--------|-------|---------|
| Title | `layout-title` | Opening/section title slides |
| Text | `layout-text` | Explanatory content, section intros |
| Two Column | `layout-two-col` | Comparisons, side-by-side content |
| Three Column | `layout-three-col` | Feature sets, pricing tiers |
| Image + Text | `layout-image-text` | Feature highlights, screenshots |
| Quote | `layout-quote` | Testimonials, impactful quotes |
| Stats | `layout-stats` | Key metrics, achievements |
| Bullets | `layout-bullets` | Key points with descriptions |

## Presentation Structure

Every presentation follows this structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>[PRESENTATION TITLE]</title>
  
  <!-- Google Font: Inter -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  
  <style>
    /* COPY FULL CSS FROM STYLES.md */
  </style>
</head>
<body>
  <div class="presentation">
    <!-- SLIDES GO HERE -->
  </div>

  <script>
    /* COPY NAVIGATION JS FROM SCRIPTS.md */
  </script>
</body>
</html>
```

**Important:** Copy the complete CSS from [STYLES.md](STYLES.md) and the JavaScript from [SCRIPTS.md](SCRIPTS.md).

## Slide Structure

Each slide is a `<section>` element with:
- Unique `id` in format `slide1`, `slide2`, etc.
- Class `slide` plus a layout class (e.g., `layout-title`)
- A `<div class="slide-content">` wrapper for all content
- A `<span class="slide-number">` showing position (e.g., "1 / 10")

```html
<section id="slide1" class="slide layout-title">
  <div class="slide-content">
    <!-- Content here -->
  </div>
  <span class="slide-number">1 / 10</span>
</section>
```

## Foundation Elements

See [FOUNDATIONS.md](FOUNDATIONS.md) for complete reference. Summary:

### Typography Classes

| Class | Purpose |
|-------|---------|
| `typo-h1` | Large heading (3.815rem, weight 800) |
| `typo-h2` | Section heading (2.441rem, weight 700) |
| `typo-h3` | Subsection heading (1.563rem, weight 600) |
| `typo-p` | Body text (1rem, secondary color) |
| `typo-muted` | De-emphasized text (0.9rem, muted color) |
| `typo-label` | Uppercase label (0.7rem, accent color) |

### Text Elements

- `typo-list` - Unordered list with accent bullets
- `typo-list-ordered` - Numbered list with accent numbers
- `typo-blockquote` - Styled quote with left border
- `typo-link` - Accent-colored link
- `typo-code` - Inline code
- `typo-code-block` - Multi-line code block

### Data Display

- `typo-stat` - Container for stat/metric
- `typo-stat-value` - Large gradient number (use `.unit` span for suffix)
- `typo-stat-label` - Description below number

### Components

- `typo-badge` - Inline badge/tag (default style)
- `typo-badge--accent` - Violet accent badge variant
- `typo-badge--muted` - Subtle muted badge variant
- `typo-card` - Card container with surface and shadow
- `typo-card-header` - Card header section
- `typo-card-body` - Card main content section
- `typo-card-footer` - Card footer section

### Utilities

| Class | Effect |
|-------|--------|
| `glass` | Frosted glass surface with blur and border |
| `glow` | Violet glow shadow around element |
| `text-gradient` | Violet gradient text fill |
| `text-accent` | Violet accent color text |
| `divider` | Subtle horizontal rule |

## Layout Templates

### Layout: Title (`layout-title`)

Centered title slide for opening or section breaks.

```html
<section id="slide1" class="slide layout-title">
  <div class="slide-content">
    <div class="accent-line"></div>
    <h1 class="typo-h1">Presentation Title</h1>
    <p class="typo-p">Subtitle or tagline goes here</p>
  </div>
  <span class="slide-number">1 / 10</span>
</section>
```

### Layout: Text (`layout-text`)

Vertically centered, left-aligned text for explanations.

```html
<section id="slide2" class="slide layout-text">
  <div class="slide-content">
    <div class="accent-line"></div>
    <h2 class="typo-h2">Section Title</h2>
    <p class="typo-p">First paragraph of explanatory content.</p>
    <p class="typo-p">Second paragraph with additional details.</p>
  </div>
  <span class="slide-number">2 / 10</span>
</section>
```

### Layout: Two Column (`layout-two-col`)

Header with two columns below.

```html
<section id="slide3" class="slide layout-two-col">
  <div class="slide-content">
    <div class="header">
      <div class="accent-line"></div>
      <h2 class="typo-h2">Two Column Title</h2>
      <p class="typo-muted">Optional subtitle</p>
    </div>
    <div class="columns">
      <div class="col-left">
        <h3 class="typo-h3">Left Heading</h3>
        <p class="typo-p">Left column content here.</p>
      </div>
      <div class="col-right">
        <h3 class="typo-h3">Right Heading</h3>
        <p class="typo-p">Right column content here.</p>
      </div>
    </div>
  </div>
  <span class="slide-number">3 / 10</span>
</section>
```

### Layout: Three Column (`layout-three-col`)

Header with three columns below.

```html
<section id="slide4" class="slide layout-three-col">
  <div class="slide-content">
    <div class="header">
      <div class="accent-line"></div>
      <h2 class="typo-h2">Three Column Title</h2>
      <p class="typo-muted">Optional subtitle</p>
    </div>
    <div class="columns">
      <div class="col">
        <h3 class="typo-h3">First Column</h3>
        <p class="typo-p">First column content.</p>
      </div>
      <div class="col">
        <h3 class="typo-h3">Second Column</h3>
        <p class="typo-p">Second column content.</p>
      </div>
      <div class="col">
        <h3 class="typo-h3">Third Column</h3>
        <p class="typo-p">Third column content.</p>
      </div>
    </div>
  </div>
  <span class="slide-number">4 / 10</span>
</section>
```

### Layout: Image + Text (`layout-image-text`)

Side-by-side image and text. Text on left, image on right by default.

```html
<section id="slide5" class="slide layout-image-text">
  <div class="slide-content">
    <div class="text-side">
      <div class="accent-line"></div>
      <h2 class="typo-h2">Feature Title</h2>
      <p class="typo-p">Description of the feature or concept shown in the image.</p>
      <p class="typo-p">Additional context or details.</p>
    </div>
    <div class="image-side">
      <div class="image-container">
        <img src="path/to/image.png" alt="Description">
      </div>
    </div>
  </div>
  <span class="slide-number">5 / 10</span>
</section>
```

**Reversed variant** (image on left): Add `layout-image-text--reversed` class.

```html
<section id="slide6" class="slide layout-image-text layout-image-text--reversed">
  <!-- Same structure as above -->
</section>
```

**Image placeholder** (when no image):

```html
<div class="image-container">
  <div class="image-placeholder">
    <svg class="image-placeholder-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
      <rect x="3" y="3" width="18" height="18" rx="2" ry="2"/>
      <circle cx="8.5" cy="8.5" r="1.5"/>
      <polyline points="21 15 16 10 5 21"/>
    </svg>
    <span class="image-placeholder-text">Image description</span>
  </div>
</div>
```

### Layout: Quote (`layout-quote`)

Centered large quote with attribution.

```html
<section id="slide7" class="slide layout-quote">
  <div class="slide-content">
    <span class="quote-mark">"</span>
    <blockquote class="typo-blockquote">The quote text goes here. Make it impactful and memorable.</blockquote>
    <div class="quote-attribution">
      <span class="typo-h3">Author Name</span>
      <span class="typo-p">Title or Context</span>
    </div>
  </div>
  <span class="slide-number">7 / 10</span>
</section>
```

### Layout: Stats (`layout-stats`)

Grid of 3 key metrics.

```html
<section id="slide8" class="slide layout-stats">
  <div class="slide-content">
    <div class="header">
      <div class="accent-line"></div>
      <h2 class="typo-h2">Key Metrics</h2>
      <p class="typo-muted">Optional context</p>
    </div>
    <div class="stats-grid">
      <div class="typo-stat">
        <span class="typo-stat-value">99<span class="unit">%</span></span>
        <span class="typo-stat-label">First Metric</span>
      </div>
      <div class="typo-stat">
        <span class="typo-stat-value">2.5<span class="unit">M</span></span>
        <span class="typo-stat-label">Second Metric</span>
      </div>
      <div class="typo-stat">
        <span class="typo-stat-value">150<span class="unit">+</span></span>
        <span class="typo-stat-label">Third Metric</span>
      </div>
    </div>
  </div>
  <span class="slide-number">8 / 10</span>
</section>
```

### Layout: Bullets (`layout-bullets`)

Key points with titles and descriptions.

```html
<section id="slide9" class="slide layout-bullets">
  <div class="slide-content">
    <div class="header">
      <div class="accent-line"></div>
      <h2 class="typo-h2">Key Points</h2>
      <p class="typo-muted">Optional subtitle</p>
    </div>
    <div class="bullet-list">
      <div class="bullet-item">
        <span class="bullet-marker"></span>
        <div class="bullet-content">
          <h3 class="typo-h3">First Point</h3>
          <p class="typo-p">Supporting description for the first point.</p>
        </div>
      </div>
      <div class="bullet-item">
        <span class="bullet-marker"></span>
        <div class="bullet-content">
          <h3 class="typo-h3">Second Point</h3>
          <p class="typo-p">Supporting description for the second point.</p>
        </div>
      </div>
      <div class="bullet-item">
        <span class="bullet-marker"></span>
        <div class="bullet-content">
          <h3 class="typo-h3">Third Point</h3>
          <p class="typo-p">Supporting description for the third point.</p>
        </div>
      </div>
    </div>
  </div>
  <span class="slide-number">9 / 10</span>
</section>
```

## Workflow

1. Create a new `.html` file
2. Copy the HTML structure from [Presentation Structure](#presentation-structure)
3. Copy the full CSS from [STYLES.md](STYLES.md) into the `<style>` tag
4. Copy the JavaScript from [SCRIPTS.md](SCRIPTS.md) into the `<script>` tag
5. Add slides inside `<div class="presentation">`:
   - Each slide needs unique `id="slideN"` (sequential from 1)
   - Each slide needs `class="slide layout-[type]"`
   - Update all `<span class="slide-number">` to show correct `X / Y`
6. Use foundation elements within slide content as needed

## Rules

- Every slide MUST have `class="slide"` plus exactly one layout class
- Every slide MUST have a unique `id` in format `slideN` where N is sequential starting from 1
- Every slide MUST contain `<div class="slide-content">` as the direct child wrapper
- Every slide MUST have `<span class="slide-number">X / Y</span>` with correct position
- Slide numbers MUST be updated to reflect total count after adding/removing slides
- Use `typo-*` classes for all typography, not raw HTML heading/paragraph elements
- Two-column layouts use `col-left` and `col-right`
- Three-column layouts use `col` for all three columns
- Stats layout expects exactly 3 stats in the grid
- The presentation container `<div class="presentation">` wraps all slides
- Always include the Inter font from Google Fonts
