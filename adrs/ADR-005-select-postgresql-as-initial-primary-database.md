# ADR-005: Select PostgreSQL as the Initial Primary Database

**Status:** Accepted

**Date:** 2026-06-25

## Context

JourneyBot needs to store users, conversations, messages, subscriptions, payments, invoices, lead information, customer preferences, intent history, and AI metadata.

The primary database should provide strong support for relational business data while remaining flexible enough to accommodate evolving AI features.

The options evaluated were SQL Server, PostgreSQL, and MongoDB.

## Decision

PostgreSQL has been selected as the initial primary database for JourneyBot.

## Rationale

The decision was based on the application's requirements rather than the popularity of a particular database.

PostgreSQL provides:

- A mature relational database for highly connected business entities.
- Native JSON support for customer preferences, AI metadata, and other evolving data.
- Support for extensions such as pgvector, making it possible to introduce semantic search later without adding another database during the MVP.
- An open source ecosystem with excellent tooling and cloud support.
- A clear path to scale while keeping the initial architecture simple.

## Alternatives Considered

### SQL Server

Pros

- Excellent relational capabilities.
- Strong .NET ecosystem.
- Mature tooling.
- Excellent transaction support.

Reason not selected

Although SQL Server satisfies the current requirements, PostgreSQL offers additional flexibility through JSON support, extensions, and its open source ecosystem.

### MongoDB

Pros

- Flexible document model.
- Rapid schema evolution.

Reason not selected

JourneyBot's core domain is relationship heavy. Customers, subscriptions, payments, invoices, conversations, and leads naturally fit a relational model and benefit from strong transactional guarantees.

## Consequences

### Positive

- One database can support both relational and semi-structured data.
- Infrastructure remains simple during the MVP.
- Future AI capabilities can be added without immediately introducing a dedicated vector database.

### Negative

- Some AI workloads may eventually benefit from a dedicated vector database.
- JSON data may need to be normalized as reporting requirements evolve.

## Future Considerations

This decision applies to the initial version of JourneyBot.

As the platform grows, additional storage technologies may be introduced where they provide a clear technical benefit. PostgreSQL will remain the primary transactional database unless future requirements justify a different approach.