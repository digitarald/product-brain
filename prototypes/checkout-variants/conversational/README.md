# Conversational Checkout Prototype

**Status:** Active Prototype  
**Created:** February 2026  
**Related Spec:** [Checkout Redesign](/specs/checkout-redesign.md)  
**Supporting Research:** [Mobile Usability Study](/insights/mobile-usability-study.md)

---

## What This Demonstrates

This prototype reimagines the checkout experience as a natural conversation with a helpful store clerk, rather than a traditional form. It addresses key pain points identified in our mobile usability study, particularly the 42% checkout completion rate on mobile.

## Design Philosophy

- **Conversational, not transactional** - Feels like texting a friend who's helping you check out
- **One question at a time** - Reduces cognitive load and decision fatigue
- **Progressive disclosure** - Information appears when needed, not all at once
- **Mobile-first** - Optimized for small screens and touch interactions
- **Natural language prompts** - "Where should we send your gear?" vs "Shipping Address"

## Key Features

### Chat-Style Interface
- Message bubbles with smooth slide-up animations
- Assistant avatar (mountain emoji ⛰️) for brand personality
- Typing indicator animation for natural pacing
- Centered 600px container for optimal readability

### Interaction Patterns
- **Quick reply buttons** for common choices (shipping speed, payment method)
- **Large text inputs** with clear placeholders
- **"Continue" button** instead of generic "Submit" or "Next"
- **Natural conversation flow** - 5 steps from email to order confirmation

### Order Summary
- Presented as a chat message at the end
- Shows cart items (Tent + Backpack from existing checkout mockup)
- Includes sustainability messaging (carbon offset)
- Dynamic total calculation based on shipping choice

### Visual Design
- **Brand colors:** Sage (#7a9b7e), Earth (#8b7b6b), Cream (#fefcf7)
- **Typography:** Crimson Text (headings) + Outfit (body)
- **Shadows and depth** for bubble elevation
- **Dark mode compatible** with automatic color scheme detection

## Conversation Flow

1. **Email capture** - "Hi! Let's get your gear on the way 🏕️ First, what's your email?"
2. **Shipping address** - "Perfect! Where should we ship your gear?"
3. **Shipping speed** - Quick reply buttons for Standard/Express/Overnight
4. **Payment method** - Quick reply buttons for Credit Card/PayPal/Apple Pay
5. **Order summary & confirmation** - Shows order details with "Place Order 🎉" button, then success message with order number

## Technical Stack

- **HTML** - Single file, no build process
- **Tailwind CSS** - Via CDN for rapid styling
- **Alpine.js** - Lightweight reactivity for conversation state
- **Web Fonts** - Google Fonts CDN (Crimson Text + Outfit)

No dependencies to install. Just open `index.html` in a browser.

## Testing Notes

Test scenarios to validate:
- [ ] All 5 conversation steps flow smoothly
- [ ] Quick reply buttons update order data correctly
- [ ] Shipping cost changes based on speed selection
- [ ] Order total calculates correctly
- [ ] Typing animations feel natural (not too fast/slow)
- [ ] Mobile responsive (test on actual devices)
- [ ] Dark mode renders properly
- [ ] Keyboard navigation works (Enter to submit)

## Success Criteria

This prototype succeeds if:
- Stakeholders report it "feels like texting" vs "filling a form"
- Time-to-complete is perceived as faster (even if objective time is similar)
- Mobile users find it easier than traditional checkout
- The conversational tone aligns with Contoso's brand voice

## Next Steps

If this direction is validated:
1. Conduct A/B test against traditional checkout (10% traffic)
2. Add address autocomplete using Google Maps API
3. Integrate real payment processing
4. Build backend conversation state management
5. Add "Edit previous answer" capability
6. Implement proper error handling and validation

## Live Demo

Once published to GitHub Pages, this will be available at:
`https://digitarald.github.io/product-brain/prototypes/checkout-variants/conversational/`

---

*This is a disposable prototype for validation. Optimize for learning speed, not production quality.*
