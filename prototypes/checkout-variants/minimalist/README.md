# Minimalist Express Checkout Prototype

**What it demonstrates:** A radical single-screen checkout that challenges traditional accordion-based flows

**Related spec:** [specs/checkout-redesign.md](../../../specs/checkout-redesign.md)

## Design Philosophy

This prototype explores: "What if Amazon's 1-click was a full checkout page?"

### Key Principles

- **Everything visible** - No accordions, no steppers, no hidden steps
- **Essential fields only** - Email, card details, ZIP (billing address derives shipping)
- **Express-first** - Apple Pay & Google Pay prominent at top
- **Speed optimized** - Target: <30 seconds for returning customers
- **Smart defaults** - "Ship to billing" checked by default

## Features

1. **Cart at a glance** - Tent + backpack visible immediately
2. **Express payment buttons** - Apple Pay / Google Pay for instant checkout
3. **Minimal form** - Only 5 required fields (email, card #, expiry, CVV, ZIP)
4. **Intelligent totals** - Real-time tax estimation based on ZIP code
5. **Expandable shipping** - Different address option available but hidden by default
6. **Visual hierarchy** - Large green "Complete Purchase" button guides action

## Technical Stack

- **HTML** - Single file, no build process
- **Tailwind CSS** - Via CDN for rapid styling
- **Alpine.js** - Lightweight reactivity for form interactions
- **Fonts** - Crimson Text (headings) + Outfit (body)
- **Colors** - Contoso brand: Sage #7a9b7e, Earth #8b7b6b, Cream #fefcf7

## Testing Notes

### Simulated Behaviors

- **Express Pay** - Alert dialogs simulate native payment sheets
- **Tax calculation** - Estimates based on ZIP ranges (CA: 9.25%, TX: 8.25%, NY: 8.875%)
- **Free shipping** - Applied automatically for orders $400+
- **Form formatting** - Card number spaces, expiry auto-slash

### User Journey

1. Open file in browser
2. Review cart (2 items, $439.98)
3. Try express pay OR
4. Fill: email, card, expiry, CVV, ZIP
5. Watch total update with tax
6. Click "Complete Purchase"

## Design Rationale

### Why This Works

- **Cognitive load reduction** - All information visible reduces mental burden of multi-step flows
- **Friction removal** - No account creation, no navigation between steps
- **Trust building** - Seeing full order details upfront increases confidence
- **Mobile-friendly** - Single scroll, no tab switching

### Trade-offs

- **Longer initial page** - More scrolling on mobile (acceptable for conversion gain)
- **Less guidance** - No step-by-step flow (mitigated by visual hierarchy)
- **Billing = Shipping** - Assumes most customers ship to billing (expandable option available)

## Next Steps

If validated through user testing:
1. A/B test against current accordion checkout
2. Add autofill detection (Chrome/Safari)
3. Integrate real payment processor
4. Add address validation API
5. Implement proper accessibility features

---

**Status:** Prototype for stakeholder review  
**Created:** February 2026  
**Designer:** Product Team
