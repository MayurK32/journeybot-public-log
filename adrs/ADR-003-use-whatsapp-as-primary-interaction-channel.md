# ADR-003: Use WhatsApp as the Primary Customer Interaction Channel

**Status:** Accepted

**Date:** 2026-06-14

## Context

JourneyBot is designed to help travel agencies nurture leads from the moment a customer makes an enquiry until they complete a booking.

Potential customers already communicate with travel agencies through WhatsApp. Asking them to install another application or create an account would introduce unnecessary friction and reduce engagement.

## Decision

WhatsApp will be the primary customer interaction channel for the initial version of JourneyBot.

All core workflows including lead qualification, follow-ups, customer communication, payment notifications, and tour updates will be designed around the WhatsApp Business Platform.

## Rationale

Starting with a single communication channel keeps the product focused and reduces development complexity.

Additional reasons include:

- Customers are already familiar with WhatsApp.
- No additional application installation is required.
- Travel agencies already use WhatsApp as part of their daily workflow.
- A conversation-first experience aligns naturally with lead nurturing.
- Focusing on one channel allows faster iteration during the MVP.

## Alternatives Considered

### Multi-channel support from day one

Supporting email, SMS, Instagram, Telegram, and other messaging platforms would increase development effort and operational complexity without validating the core product.

### Build a dedicated mobile application

A custom application would provide greater control over the user experience but would create additional adoption barriers for customers.

## Consequences

### Positive

- Smaller MVP with a clear product focus.
- Faster delivery of core features.
- Lower maintenance overhead during the early stages.
- Better user adoption by using an existing communication platform.

### Negative

- JourneyBot becomes dependent on the WhatsApp Business Platform.
- Platform limitations and API changes must be considered.
- Customers who prefer other communication channels will not be supported initially.

## Future Considerations

The architecture should allow additional communication channels to be introduced in the future without changing the core business logic. WhatsApp is the starting point, not necessarily the only supported channel.
