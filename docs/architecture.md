# Architecture Notes

These notes capture how I think about software architecture and the trade-offs that come with different system designs.

I prefer architecture discussions that start with the problem rather than the technology.

## Start With the Problem

Before choosing an architecture, I want to understand:

- What are we building?
- Who uses it?
- What constraints exist?
- What needs to scale?
- What can fail?
- What needs to remain simple?

The architecture should follow those answers.

## Boundaries

Good boundaries make systems easier to understand and change.

Depending on the application, those boundaries may exist between modules, domains, services, or independently deployed systems.

I don't split a system into services simply because the application has grown large. There should be a reason for the boundary.

## Communication

Depending on the requirements, communication may use:

- REST
- GraphQL
- gRPC
- Message brokers
- Domain events

The choice depends on coupling, latency, reliability, interoperability, and consistency requirements.

## Data Ownership

Clear data ownership becomes especially important in distributed systems.

I am interested in database-per-service designs, asynchronous data propagation, caching, and the trade-offs involved in maintaining consistency between services.

## Scalability

Scalability is more than adding machines.

It can involve:

- Stateless application design
- Database capacity
- Caching
- Asynchronous processing
- Queue-based workloads
- Horizontal scaling
- Failure isolation

## Security

Architecture should establish security boundaries early.

That includes identity, authorization, secrets, service permissions, network boundaries, and secure communication.

## Trade-offs

There is rarely one architecture that is correct for every situation.

I prefer understanding what a design makes easier, what it makes harder, and whether that trade-off is justified by the actual problem.

---

[Back to README](../README.md)
