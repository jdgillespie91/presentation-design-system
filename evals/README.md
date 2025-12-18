# Presentation Design System - Evals

This framework evaluates AI-generated presentations for content quality and design system adherence.

## Purpose

After making changes to the skill files, run these evals to catch obvious regressions in presentation quality. The prompts simulate real user requests across different complexity levels.

## Prompt Categories

| Category | Description | Count |
|----------|-------------|-------|
| `lazy/` | Minimal input, tests defaults and AI judgment | 5 |
| `detailed/` | Specific requirements, but no design system knowledge | 5 |
| `edge-cases/` | Unusual requests that stress-test the skill | 3 |

## How to Run Evals

### 1. Set Up a Run Directory

```
mkdir evals/runs/YYYY-MM-DD
```

### 2. Run Each Prompt

For each prompt in `evals/prompts/`:

1. Start a fresh conversation with the AI agent (with the skill loaded)
2. Copy the prompt text and send it
3. Save the generated HTML to `evals/runs/YYYY-MM-DD/[prompt-name].html`

### 3. Review Each Output

1. Open the HTML file in a browser
2. Click through all slides using arrow keys
3. Use the checklist below to assess quality
4. Record observations in `evals/runs/YYYY-MM-DD/notes.md`

### 4. Compare to Previous Runs (Optional)

If investigating a regression, compare outputs side-by-side with a previous run.

## Review Checklist

Copy this template for each presentation reviewed:

```markdown
## [Prompt Name]

### Renders Correctly
- [ ] Opens in browser without errors
- [ ] Navigation works (arrow keys, spacebar)
- [ ] No visual glitches or broken layouts

### Layout Selection
- [ ] Layouts are appropriate for the content type
- [ ] Good variety (not all the same layout)
- [ ] Title slide used correctly (if applicable)

### Content Quality
- [ ] Typography hierarchy makes sense (h1 > h2 > p)
- [ ] Slides are not overcrowded
- [ ] Slides are not too sparse
- [ ] Components used appropriately (badges, stats, cards, quotes)
- [ ] Content flows logically from slide to slide

### Design System Adherence
- [ ] Correct CSS classes used
- [ ] Slide structure follows the expected patterns
- [ ] Consistent styling throughout

### Overall Assessment
**Rating:** Pass / Needs Review / Fail

**Notes:**
```

## What to Look For

### Good Signs

- Appropriate layout choices for content (stats layout for metrics, quote layout for testimonials, etc.)
- Balanced slides - not too much or too little content
- Logical flow and narrative structure
- Correct use of typography hierarchy
- Creative but appropriate use of components

### Red Flags

- Same layout repeated for every slide
- Overcrowded slides with too much text
- Empty or sparse slides
- Wrong layout for content type (e.g., bullet points in a stats layout)
- Broken HTML structure or missing elements
- Inconsistent styling or class usage

## Run Log

Track your eval runs here.

**Determining skill version:** Use the short hash of the last commit that modified the skill files:

```bash
git log -1 --format="%h" -- skills/presentation-design-system/
```

| Date | Skill Version | Notes |
|------|---------------|-------|
| 2025-12-18 | `c1ddd93` | First run - quick scan only, no per-slide notes. Detailed prompts carried content correctly. Visual similarity across outputs (theming TBD). Limited layout variety - would like more options. Three-col often used where a "three-card" layout (like stats but for text) would be better. Some odd line breaks in single-col layout. |
