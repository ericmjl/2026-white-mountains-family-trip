# Design

## Theme

**Modern travel editorial.** A magazine feature about four days in the White Mountains, built as one long single-purpose scroll. Physical scene: a family of six unfolding a paper trail map on a picnic table at dawn — cool violet shadow still filling the notch, first gold light on the ridge, coffee steam.

Color strategy: **Committed** — alpine-dusk violet carries the hero, the day sequence markers, and the Wednesday poster section (30–60% of emotional surface); everything else is pure white paper and ink. Goldenrod appears only as light: rules, markers, numerals, the sun on the ridge. Never as body text on white.

## Palette (OKLCH)

| Token | Value | Role |
|---|---|---|
| `--bg` | `oklch(1 0 0)` | Pure white paper |
| `--surface` | `oklch(0.965 0.012 294)` | Violet-tinted panels, timeline wells |
| `--ink` | `oklch(0.25 0.03 294)` | Body text (≈10:1 on white) |
| `--muted` | `oklch(0.43 0.03 294)` | Secondary text (≈5:1 on white) |
| `--dusk` | `oklch(0.42 0.12 294)` | Primary violet; white text on it (≈5.5:1) |
| `--dusk-deep` | `oklch(0.31 0.09 294)` | Hero overlay, Wednesday drench, footer |
| `--gold` | `oklch(0.74 0.14 78)` | Accent light: rules, markers, large numerals on deep violet only |
| `--line` | `oklch(0.88 0.015 294)` | Hairlines |

No gradients on text. No glassmorphism. Surfaces are flat and printed.

## Typography

- **Display:** Vollkorn (500–900, +italic) — warm German book face, "field guide" weight. Fallback: Georgia, serif.
- **Text / UI:** Schibsted Grotesk (400–800) — news-heritage grotesque. Fallback: system sans.
- Pairing axis: sturdy bookish serif vs. newsy grotesque.
- Scale ≈ 1.3 modular, fluid clamps. Hero display max 5.5rem, letter-spacing -0.01em (serif wants air, not crunch). Body 17px/1.65, measure ≤ 68ch.
- `text-wrap: balance` on headings; `pretty` on prose.

## Layout

- One long editorial scroll: hero → base camp → four day spreads → crew → packing → footer.
- Day spreads alternate composition (photo left / photo right / drenched / photo band) — a sequence, not a card grid.
- Timeline = ruled rows (time column + description), never cards.
- Mobile-first: sticky day nav with scrollspy; every map link a ≥44px tap target.
- Desktop: 72rem measure, asymmetric two-column day spreads, huge date numerals as section anchors.

## Components

- **Sticky day nav**: solid white, hairline bottom, scrollspy underline, `aria-current`.
- **Timeline row**: time (grotesk, tabular) + entry; map links as underlined text-links with pin glyph.
- **Tip callouts**: surface tint + full hairline border, no side-stripes.
- **Packing checklist**: real checkboxes, localStorage persistence, progress rule in gold.
- **Photo figures**: full-bleed with caption + credit; violet duotone only on the hero.
- **Wednesday poster**: drenched `--dusk-deep`, white Vollkorn display, gold rules.

## Motion

- Page-load: hero title clip-path reveal + staggered meta (one well-orchestrated load, not scattered effects).
- Scroll: subtle 12px rise + fade via IntersectionObserver — content visible by default; the reveal only enhances.
- Scrollspy underline follows section; checklist strikes through with a 200ms width animation.
- All motion gated by `prefers-reduced-motion: reduce` → instant/crossfade.
- Easing: `cubic-bezier(0.22, 1, 0.36, 1)` (ease-out-quint family). No bounce.

## Imagery

Verified Wikimedia Commons photography (the actual places), credited in the footer:

- Hero: Presidential Range from Cherry Valley, Jefferson NH — EgorovaSvetlana, CC BY-SA 4.0
- Loon Mountain across from the resort — EgorovaSvetlana, CC BY-SA 4.0
- Franconia Notch Parkway (Monday drive) — EgorovaSvetlana, CC BY-SA 4.0
- Flume Gorge (Tuesday AM) — EgorovaSvetlana, CC BY-SA 4.0
- Echo Lake (Tuesday PM) — Robert Linsdell, CC BY 2.0
- Kancamagus Highway (Thursday) — Bob Linsdell, CC BY 3.0

Wednesday gets no photograph — it gets the violet poster treatment (art direction per section).

## Voice

Specific, warm, unhurried. Copy speaks to the six travelers ("us"), never to tourists. Alt text is part of the voice.
