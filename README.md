# NO-MERCY

A brutalist design system. Harsh grids, oversized type, no mercy.

Three colors and the truth: near-black ink, bone paper, safety orange used like a weapon. No border-radius — ever. Hard shadows with zero blur. Display type is Anton at violent sizes, always uppercase. Mono labels do the paperwork.

## The doctrine

| # | Rule | Exceptions |
|---|------|-----------|
| 1 | `border-radius: 0` everywhere | None. Ever. |
| 2 | Borders are always ink, 2px minimum | None |
| 3 | Shadows are hard offsets, zero blur (`6px 6px 0`) | None — blur is cowardice |
| 4 | Display type always uppercase, line-height 0.85 | Whispers don't convert |
| 5 | One accent (`#FF4D00`), used sparingly | One loud thing per view |
| 6 | Grids are visible — borders, not gutters | The grid IS the design |

## Files

```
tokens.css      — every design decision as a CSS custom property
components.css  — nav, hero, marquee, cards, table, buttons, inputs, footer, utilities
index.html      — live demo showcasing every token and component
```

## Usage

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Anton&family=Archivo:wght@400;500;700;900&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">

<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/legobele/no-mercy@main/tokens.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/legobele/no-mercy@main/components.css">
```

Or vendor the two CSS files into your project.

## Tokens

### Color

| Token | Value | Role |
|-------|-------|------|
| `--nm-ink` | `#0d0d0d` | Everything structural |
| `--nm-paper` | `#f2efe6` | Default surface |
| `--nm-accent` | `#ff4d00` | The weapon |
| `--nm-gray` | `#8b8b85` | Meta text only |

### Type

| Token | Value | Role |
|-------|-------|------|
| `--font-display` | Anton | Violent headlines, always uppercase |
| `--font-body` | Archivo | Quiet body copy, max 62ch |
| `--font-mono` | Space Mono | Labels, buttons, data |

### Violence, as numbers

| Token | Value |
|-------|-------|
| `--nm-radius` | `0` |
| `--nm-border` | `2px solid ink` |
| `--nm-border-thick` | `4px solid ink` |
| `--nm-shadow` | `6px 6px 0 ink` |

## Components

| Class | What |
|-------|------|
| `.nm-display-1/2/3` | Oversized Anton headlines |
| `.nm-outline-text` | Hollow stroke-only type |
| `.nm-label` / `.nm-label-accent` / `.nm-sticker` | Paperwork, violence, sticker |
| `.nm-btn` / `.nm-btn-ghost` / `.nm-btn-ink` | Buttons that physically move when pressed |
| `.nm-nav` | Bordered bar, sticky |
| `.nm-hero` | Type does all the work |
| `.nm-marquee` / `.nm-marquee-accent` | The ticker never stops |
| `.nm-grid` + `.nm-card` | Boxes with borders and opinions (hover = orange) |
| `.nm-table` | Data with borders |
| `.nm-input` | Inputs are boxes too |
| `.nm-invert` | The black room |
| `.nm-blink` | Mechanical blink for status dots |

## Rules for implementers

1. **Never add border-radius.** The token exists to forbid it.
2. **Display type is always uppercase Anton.** Tight leading, no exceptions.
3. **One accent per view.** If everything screams, nothing does.
4. **Hover states commit.** Cards go full orange, buttons physically depress.
5. **Respect `prefers-reduced-motion`.** The marquee stops; the attitude doesn't.
