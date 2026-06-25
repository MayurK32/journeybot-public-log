# ADR-002: Keep Source Code Private

**Status:** Accepted

**Date:** 2026-06-14

## Context

JourneyBot is intended to become a commercial product rather than an open source project. While I want to share the engineering journey publicly, I also want the freedom to experiment, iterate quickly, and potentially launch the product without exposing its implementation.

## Decision

The JourneyBot source code will remain private.

Only architecture decisions, technical trade-offs, lessons learned, diagrams, and progress updates will be shared publicly through this repository.

## Rationale

Keeping the implementation private provides a balance between transparency and product ownership.

It allows me to:

- Share the engineering thought process without exposing the implementation.
- Refactor and experiment without worrying about breaking a public API.
- Protect commercially valuable parts of the product.
- Build a public portfolio focused on engineering decisions instead of code volume.

## Alternatives Considered

### Make the entire repository public

This would allow others to review the implementation, but it would also expose business logic and reduce flexibility as the product evolves.

## Consequences

### Positive

- Freedom to iterate quickly.
- Commercial flexibility for the future.
- Public documentation remains useful to other engineers.

### Negative

- Developers cannot inspect the implementation directly.
- Feedback will focus on architecture rather than code.

## Future Considerations

Some standalone libraries, utilities, or reusable components developed during the JourneyBot journey may be open sourced in the future if they are independent of the core product.
