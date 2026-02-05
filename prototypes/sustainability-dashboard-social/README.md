# Sustainability Dashboard - Social-Community Variation

**Prototype**: `prototypes/sustainability-dashboard-social/index.html`

**Specification**: [Sustainability Dashboard PRD](../../specs/sustainability-dashboard.md)

## Variation Focus

This prototype implements the **social-community variation** specifically targeting **Morgan the Conscious Consumer** (25-45, urban professional who shares brand partnerships on social media).

## Key Features Demonstrated

### 1. Hero Impact Card
- Instagram/LinkedIn-ready shareable design
- Prominent display of lifetime CO₂ offset (847 kg)
- Visual hierarchy optimized for screenshots
- 4-metric grid: Trees planted, Eco purchases, Purchase %, Trade-ins
- Member since badge for credibility

### 2. Social Proof & Motivation
- "Top 15% of mindful members" badge prominently displayed
- "3.2x more impact than average" comparison insight
- Positive reinforcement (not shaming)
- Distance to next tier: "353 kg away from top 5%"

### 3. Share & Download CTAs
- Primary "Download Card" button with Forest green CTA
- Secondary "Share Story" button
- Share modal with platform options:
  - Instagram Story (gradient icon)
  - LinkedIn (professional context)
  - Twitter/X (social sharing)
  - Copy link functionality
- Toast notifications for user feedback

### 4. Community Impact
- Collective stats: 127,432 members, 2.4M kg CO₂, 34,000+ trees
- Animated stat pulses to draw attention
- "Together we're making a difference" messaging

### 5. Monthly Challenge
- February Offset Challenge: 50kg goal
- Visual progress bar: 34kg current (68% complete)
- Days remaining counter: 23 days left
- Motivational progress tracking
- Clear CTA to view details

### 6. Benchmark Comparisons
- Visual bar chart comparisons:
  - Your impact: 847 kg (100% baseline)
  - Average member: 265 kg
  - Top 5%: 1,200 kg
- Encouraging messaging about reaching next tier

### 7. Recent Eco-Actions Feed
- Activity timeline with icons
- CO₂ impact per action
- Mix of purchases and trade-ins
- Reinforces positive behaviors

## Design System Compliance

✅ **Colors**:
- Page background: `#0a0c0a`
- Card background: `rgba(17, 20, 17, 0.85)` with backdrop blur
- Border: `rgba(163, 171, 163, 0.12)`
- Forest: `#4ade80` (primary CTAs)
- Sage: `#7a9b7e` (secondary accents)
- Ember: `#f97316` (challenges, urgency)
- Earth: `#8b7b6b` (benchmarks)

✅ **Typography**:
- Display/Headers: Source Serif 4
- Body text: Outfit
- Text colors: `#e8ebe8` (primary), `#a3aba3` (secondary)

✅ **Effects**:
- Ambient background glows (Forest and Ember radial gradients)
- Glass morphism on cards
- Shimmer effect on hero card
- Pulse animations on key stats

## Sample Data

- **Member**: Alex Rivera (Summit tier, member since 2023)
- **Lifetime CO₂**: 847 kg offset
- **Eco Purchases**: 23 (74% of orders)
- **Trees Planted**: 12
- **Trade-ins**: 2 items
- **Percentile**: Top 15%
- **vs Average**: 3.2x more impact
- **Community**: 127,432 members, 2.4M kg CO₂ total

## Technical Implementation

- **Single HTML file** - no build process required
- **Tailwind CSS** via CDN for rapid styling
- **Alpine.js** for interactivity:
  - Modal state management
  - Toast notifications
  - Dynamic data binding
  - Platform share handlers
- **Google Fonts** for Source Serif 4 and Outfit
- **Responsive design** - mobile-first with breakpoints

## Interaction States

1. **Default state**: Hero card with all stats visible
2. **Share modal**: Opens on "Share Story" click
3. **Download action**: Shows success toast
4. **Platform sharing**: Mock handlers for Instagram, LinkedIn, Twitter
5. **Copy link**: Clipboard simulation with feedback

## To Preview

### Option 1: Simple HTTP Server
```bash
cd prototypes/sustainability-dashboard-social
python3 -m http.server 8000
```
Then open: http://localhost:8000

### Option 2: NPX Serve
```bash
npx serve prototypes/sustainability-dashboard-social
```

### Option 3: Direct File
Simply open `index.html` in any modern browser (Chrome, Firefox, Safari, Edge)

## Limitations

This is a **prototype for stakeholder review**, not production code:

- ❌ No actual social media API integrations
- ❌ No real download/screenshot functionality
- ❌ Mock data only (not connected to backend)
- ❌ Share buttons log to console instead of posting
- ❌ No authentication or user management
- ❌ No analytics tracking
- ❌ No accessibility audit performed
- ❌ No cross-browser testing completed

## Success Criteria Met

✅ Impact Card is hero element and highly shareable  
✅ Social proof is motivating, not shaming  
✅ Mobile responsive design  
✅ No Lorem ipsum - all real content  
✅ Mock share/download buttons functional  
✅ Follows design system exactly  
✅ Targets Morgan persona specifically  

## Screenshot Documentation

All key states and interactions have been verified with Playwright testing:

- **[View All Screenshots](./SCREENSHOTS.md)** - Comprehensive testing documentation with images
- [Desktop Initial State](https://github.com/user-attachments/assets/63d4fc19-3357-45cc-bf2c-7d3e9065bbd6)
- [Download Toast](https://github.com/user-attachments/assets/b9ba421e-825e-442c-b179-ed7ea4a6d737)
- [Share Modal](https://github.com/user-attachments/assets/7a959b86-3694-499f-aeef-c83806c0785d)
- [Mobile View (375px)](https://github.com/user-attachments/assets/6ed0c4d4-7472-4a20-93f8-306a0ccaa8d7)
- [Tablet View (768px)](https://github.com/user-attachments/assets/c8d702f4-72a8-4d78-a38e-77415e47bf70)

## Next Steps for Production

1. Integrate with Sustainability API for real user data
2. Implement actual canvas-to-image download for Impact Card
3. Add Web Share API for native sharing
4. Connect to authentication system
5. Add analytics events for share/download tracking
6. Accessibility audit and WCAG compliance
7. Cross-browser and device testing
8. Legal review of environmental claims
9. A/B testing for share conversion optimization

## Related Specs

- [Loyalty Program v2](../../specs/loyalty-program-v2.md) - Trail Points integration with trade-ins
- [Search Personalization](../../specs/search-personalization.md) - Eco-product boost in rankings

---

**Last Updated**: February 2026  
**Status**: Ready for stakeholder review
