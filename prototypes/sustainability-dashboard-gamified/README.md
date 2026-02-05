# Sustainability Dashboard — Gamified Achievements Variation

## What This Demonstrates

This prototype explores a **gamified approach** to the personal sustainability dashboard specified in [specs/sustainability-dashboard.md](../../specs/sustainability-dashboard.md).

**Hypothesis:** Achievement hunters engage more when environmental impact is framed as unlockable milestones, badges, and progress bars — similar to earning achievements in a game.

## Key Features

### Trail Badges System
- **Earned badges** displayed prominently with glow effects
- **Next achievement** highlighted with animated progress ring
- Clear visual hierarchy focusing on gamification elements

### Achievement Types Shown
- **First Step** — First eco-certified purchase
- **Climate Keeper** — 100kg CO₂ offset milestone
- **Eco Explorer** — 10 eco-purchases milestone
- **Forest Guardian** (locked) — 1,000kg CO₂ target with 84.7% progress

### Visual Design
- **Animated progress bars** using CSS transitions
- **Glowing badge effects** for earned achievements
- **Circular progress rings** for CO₂ offset visualization
- **Shimmer animations** on impact metrics
- Fully responsive mobile layout

## Sample Data

Member: Alex Rivera (Summit tier)
- 847 kg CO₂ offset (84.7% toward Forest Guardian badge)
- 23 of 31 purchases eco-certified (74%)
- 12 trees planted equivalent
- 4.2 kg plastic avoided
- 2 trade-ins completed

## Tech Stack

- **HTML** — Single file, no build step required
- **Tailwind CSS** — Via CDN for styling
- **Alpine.js** — Lightweight reactivity for badge data
- **Google Fonts** — Source Serif 4 (display) + Outfit (body)

## Design System Compliance

Follows **Adventure Editorial Dark Theme** exactly:
- Dark base: `#0a0c0a`
- Glass cards: `rgba(17, 20, 17, 0.85)` with backdrop blur
- Forest green (`#4ade80`) for achievements and progress
- Ember orange (`#f97316`) for tier badges
- Typography: Source Serif 4 for headers, Outfit for body

## How to View

Open `index.html` directly in any modern browser — no server or build process needed.

## Target Personas

- **Jordan the Gear Enthusiast** — Wants to quantify and share impact
- **Eco-Champions segment** (23% of customers) — Sustainability drives purchases

## Research Context

Based on insight that 67% of customers rate sustainability as very/extremely important, but 88% are unaware of Contoso's trade-in program. This variation makes impact highly visible and rewarding.

## Next Steps

If validated through user testing:
1. A/B test against non-gamified version
2. Add social sharing for earned badges
3. Integrate with loyalty program rewards
4. Add more badge tiers and categories

---

**Prototype Status:** Ready for stakeholder review  
**Created:** Feb 2026  
**Spec:** [sustainability-dashboard.md](../../specs/sustainability-dashboard.md)
