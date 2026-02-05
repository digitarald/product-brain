# Sustainability Dashboard Prototype - Data Transparency Variation

## Overview

This prototype validates the **data transparency** approach to sustainability messaging for Contoso's Performance-First customer segment (24% of base). These customers are skeptical of greenwashing and respond to verifiable, credible data over marketing language.

## What This Demonstrates

- **Editorial, magazine-quality design** - Clean typography with Source Serif 4 for large numbers
- **Methodology-forward presentation** - Calculation methods are visible, not hidden
- **Precise metrics** - 847.3 kg (not "over 800"), builds trust through specificity  
- **Breakdown visualizations** - CSS-only charts showing composition of impact
- **Expandable deep-dives** - For users who want to understand the data
- **Third-party credibility** - Certification badges prominently displayed
- **Timeline sparkline** - Shows growth trajectory of environmental impact

## Target Personas

- **Performance-First (24%)**: Skeptical of greenwashing, wants proof, responds to durability messaging
- **Conscious Considerers (44%)**: Sustainability matters but balanced with credibility needs

## Testing Goals

1. Does this design feel trustworthy (vs. marketing fluff)?
2. Are users satisfied with the level of methodology transparency?
3. Do the precise numbers increase confidence in Contoso's claims?
4. Is the information hierarchy clear for quick scanning vs. deep reading?

## Design System

Built with Contoso's **Adventure Editorial Dark Theme**:
- Colors: Dark base (#0a0c0a), glass cards, forest accent (#4ade80)
- Typography: Source Serif 4 (numbers/headers), Outfit (body)
- Tech: Tailwind CSS + Alpine.js via CDN (no build step)

## Related Spec

See [specs/sustainability-dashboard.md](../../specs/sustainability-dashboard.md) for full product requirements.

## Sample Data

- Member: Alex Rivera (Summit tier)
- CO2 offset: 847.3 kg total (312.1 shipping + 535.2 manufacturing)
- Eco purchases: 23 of 31 (74.2%)
- Trees equivalent: 12.4
- Plastic avoided: 4.21 kg
- Trade-ins: 2 items (14.2 kg diverted)

## How to View

Open `index.html` directly in a browser. No build step required.

---

*Prototype Status: Ready for user testing*  
*Last Updated: February 5, 2026*
