# Product

## Register

brand

## Users

Two families sharing one vacation: the Ma family (Eric Ma, Nan Li, kids Deborah and Philip) and the Chen family (Eric Chen, Tianyi Zhang, child Luke Chen). Six people, three young-ish kids, one 3-bedroom apartment at InnSeason Resorts Pollard Brook in Lincoln, NH.

Contexts of use:

- **Pre-trip (desktop, shared link):** both families review the plan, see what's booked, start packing against the list.
- **On-trip (phone, often one-handed, sometimes spotty mountain signal):** "what's next?", "where do we drive?", "what time is dinner?" — glanceable, fast, no fumbling.
- **Afterward:** a keepsake — the page the trip lived on.

## Product Purpose

A single-page trip hub for the White Mountains family trip (Aug 24–27, 2026). It replaces the PDF itinerary with something faster, prettier, and phone-friendly: the day-by-day plan, every stop with a tap-to-navigate address, the packing list, the crew, and the weather-contingency notes. Success = nobody has to ask "what's the plan today?" for four days, and the page still feels worth opening a year later.

## Brand Personality

Modern travel editorial. Calm, warm, confident — a magazine feature about a week in the mountains, not a travel-agency template. Three words: **editorial, warm, unhurried**. The design should feel like the trip's rhythm: nature first, easy mornings, one big thing a day.

## Anti-references

- Travel-agency / booking-site templates (search bars, deal badges, stock-photo carousels)
- Cheesy kids-party aesthetics (clipart bears, bubble fonts, rainbow confetti)
- Corporate SaaS dashboards (card grids, KPI tiles)
- Generic AI slop: cream-sand backgrounds by default, eyebrow labels on every section, identical card grids, gradient text

## Design Principles

1. **The itinerary is the hero.** Everything else (crew, packing, tips) supports the four days. Navigation and hierarchy serve the schedule first.
2. **Thumb-reach on the mountain.** Mobile is the primary reading surface: big tap targets for maps links, glanceable day structure, readable at arm's length. Desktop gets the editorial spread.
3. **One big thing a day.** Let each day read as a story with a single headline act (Clark's, Flume + Echo Lake, Santa's Village, home) rather than a uniform grid of four identical day-cards.
4. **Paper-trail honesty.** Real addresses, real times, real tips from the plan — no invented content, no decorative filler.
5. **Built to travel well.** No build step, no framework, one HTML file plus one stylesheet — copy and structure render even when the mountain signal eats the fonts and photos.

## Accessibility & Inclusion

- WCAG 2.2 AA: ≥4.5:1 body contrast, ≥3:1 large text; hit targets ≥44px on mobile links/buttons
- Full keyboard navigation; semantic landmarks and headings
- `prefers-reduced-motion` respected for all motion
- Content readable at 200% zoom on mobile
