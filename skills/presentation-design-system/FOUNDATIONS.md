# Foundation Elements

Complete reference for all typography, text elements, and utility classes.

## Typography Classes

### Headings

```html
<h1 class="typo-h1">Heading One</h1>
<h2 class="typo-h2">Heading Two</h2>
<h3 class="typo-h3">Heading Three</h3>
```

| Class | Size | Weight | Use |
|-------|------|--------|-----|
| `typo-h1` | 3.815rem | 800 | Main titles |
| `typo-h2` | 2.441rem | 700 | Section headings |
| `typo-h3` | 1.563rem | 600 | Subsection headings |

### Body Text

```html
<p class="typo-p">Regular paragraph text with optimal line height.</p>
<span class="typo-muted">De-emphasized helper text.</span>
<span class="typo-label">UPPERCASE LABEL</span>
```

| Class | Size | Color | Use |
|-------|------|-------|-----|
| `typo-p` | 1rem | Secondary (60% opacity) | Body content |
| `typo-muted` | 0.9rem | Muted (25% opacity) | Captions, hints |
| `typo-label` | 0.7rem | Accent (violet) | Labels, tags |

## Text Elements

### Unordered List

```html
<ul class="typo-list">
  <li>First item with accent bullet</li>
  <li>Second item</li>
  <li>Third item</li>
</ul>
```

Renders with violet circular bullets.

### Ordered List

```html
<ol class="typo-list-ordered">
  <li>First numbered item</li>
  <li>Second numbered item</li>
  <li>Third numbered item</li>
</ol>
```

Renders with violet accent-colored numbers.

### Blockquote

```html
<blockquote class="typo-blockquote">
  "Quoted text with left border accent."
</blockquote>
```

Styled with italic text and violet left border.

### Link

```html
<a href="#" class="typo-link">Link text</a>
```

Violet underlined link that lightens on hover.

### Inline Code

```html
<p class="typo-p">Use <code class="typo-code">inline code</code> for commands.</p>
```

Monospace text with glass background.

### Code Block

```html
<pre class="typo-code-block"><span class="keyword">function</span> <span class="function">example</span>(arg) {
  <span class="comment">// This is a comment</span>
  <span class="keyword">return</span> <span class="string">"result"</span>;
}</pre>
```

Syntax highlighting classes:

| Class | Color | Use |
|-------|-------|-----|
| `.keyword` | Pink (#f472b6) | Language keywords (function, return, const) |
| `.function` | Violet (#a78bfa) | Function names |
| `.string` | Green (#86efac) | String literals |
| `.comment` | Muted gray | Comments |

## Data Display

### Statistic/Metric

```html
<div class="typo-stat">
  <span class="typo-stat-value">99<span class="unit">%</span></span>
  <span class="typo-stat-label">Success Rate</span>
</div>
```

- `typo-stat`: Container with column layout
- `typo-stat-value`: Large gradient number
- `.unit`: Smaller suffix attached to number (%, M, +, etc.)
- `typo-stat-label`: Description text below

## Components

### Badge/Tag

```html
<span class="typo-badge">Default</span>
<span class="typo-badge typo-badge--accent">Accent</span>
<span class="typo-badge typo-badge--muted">Muted</span>
```

| Variant | Class | Use |
|---------|-------|-----|
| Default | `typo-badge` | Status indicators, categories |
| Accent | `typo-badge typo-badge--accent` | Highlights, new features |
| Muted | `typo-badge typo-badge--muted` | De-emphasized tags |

Badges in context:

```html
<p class="typo-p">Use badges for <span class="typo-badge typo-badge--accent">New</span> features.</p>
```

### Card

```html
<div class="typo-card">
  <div class="typo-card-header">
    <h3 class="typo-h3">Card Title</h3>
    <span class="typo-badge typo-badge--accent">Featured</span>
  </div>
  <div class="typo-card-body">
    <p class="typo-p">Card content goes here.</p>
  </div>
  <div class="typo-card-footer">
    <span class="typo-muted">Footer metadata</span>
  </div>
</div>
```

- `typo-card`: Container with glass surface, border, shadow, and padding
- `typo-card-header`: Optional header section with column layout
- `typo-card-body`: Main content area (flex: 1)
- `typo-card-footer`: Optional footer with top padding

## Utility Classes

### Glass Effect

```html
<div class="glass">
  Frosted glass surface with blur effect
</div>
```

Creates a translucent surface with backdrop blur and subtle border.

### Glow Effect

```html
<div class="glass glow">
  Glass with violet glow
</div>
```

Adds violet box-shadow glow around element.

### Text Utilities

```html
<span class="text-gradient">Gradient text</span>
<span class="text-accent">Accent colored text</span>
<span class="text-muted">Muted text</span>
```

| Class | Effect |
|-------|--------|
| `text-gradient` | Violet gradient fill |
| `text-accent` | Solid violet color |
| `text-muted` | Low opacity gray |

### Divider

```html
<div class="divider"></div>
```

Short horizontal line (48px) for separating content.

## Section Container

```html
<div class="typo-section">
  <span class="typo-label">Label</span>
  <span class="typo-h3">Heading</span>
</div>
```

Groups related content with consistent spacing (0.5rem gap).

## Design Tokens Reference

### Colors

| Token | Value | Use |
|-------|-------|-----|
| `--accent-primary` | #a78bfa | Primary violet |
| `--accent-secondary` | #c4b5fd | Light violet |
| `--accent-tertiary` | #f472b6 | Pink (code keywords) |
| `--text-primary` | #ffffff | Main text |
| `--text-secondary` | rgba(200,195,210,0.6) | Body text |
| `--text-muted` | rgba(255,255,255,0.25) | De-emphasized text |
| `--surface-card` | rgba(255,255,255,0.03) | Card/code backgrounds |
| `--surface-card-border` | rgba(255,255,255,0.08) | Card/code borders |

### Spacing

| Token | Value |
|-------|-------|
| `--space-1` | 0.25rem |
| `--space-2` | 0.5rem |
| `--space-3` | 0.75rem |
| `--space-4` | 1rem |
| `--space-6` | 1.5rem |
| `--space-8` | 2rem |
| `--space-12` | 3rem |
| `--space-16` | 4rem |

### Border Radius

| Token | Value |
|-------|-------|
| `--radius-sm` | 8px |
| `--radius-md` | 12px |
| `--radius-lg` | 16px |
| `--radius-xl` | 24px |
