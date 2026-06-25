# ADR-004: Start Development Using .NET

**Status:** Accepted

**Date:** 2026-06-25

## Context

JourneyBot requires a backend capable of handling REST APIs, background processing, integrations with external services, and future support for asynchronous messaging and AI workloads.

The technology stack should enable rapid development today while remaining suitable as the product grows.

## Decision

JourneyBot will be developed using ASP.NET Core and C#.

The initial version will be built as a modular monolith, with the architecture designed so that components can be extracted into separate services if future requirements justify it.

## Rationale

.NET is a good fit for JourneyBot because it provides:

- Excellent performance for API development.
- A mature ecosystem for enterprise applications.
- Strong support for dependency injection, background services, and asynchronous programming.
- First-class tooling for building reliable web applications.
- Flexibility to support both a modular monolith and future service-oriented architectures.

Using a technology stack that I know well also allows me to spend more time solving product and architecture problems rather than learning a new framework.

## Alternatives Considered

### Node.js

A strong option for API development with a large ecosystem. It was not selected because .NET provides a better fit for my experience and the type of backend architecture I want to build.

### Java with Spring Boot

A mature enterprise platform with many of the same strengths as .NET. It was not selected because it would increase the learning curve without providing a significant advantage for the initial version of JourneyBot.

## Consequences

### Positive

- Faster development of the MVP.
- Mature tooling and libraries.
- Excellent support for scalable backend services.
- Reduced implementation risk by using a familiar platform.

### Negative

- Team members unfamiliar with .NET may require additional onboarding in the future.
- Future technology choices should continue to be evaluated based on requirements rather than this initial decision.

## Future Considerations

This decision applies to the backend implementation. Future components may use different technologies where there is a clear technical or business benefit, provided they integrate cleanly with the overall architecture.