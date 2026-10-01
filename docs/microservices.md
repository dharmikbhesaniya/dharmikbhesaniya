# Microservices Notes

I don't start with microservices.

For many applications, a well-structured modular system is enough. I consider microservices when independent ownership, deployment, scaling, reliability, or domain boundaries justify the additional complexity.

## Service Boundaries

A service should have a clear responsibility and a well-defined interface.

A useful boundary should reduce unnecessary coupling rather than simply move code into another repository.

## Communication

Common patterns include:

- REST
- gRPC
- Asynchronous messaging
- Domain events

The right choice depends on latency, coupling, reliability, and consistency requirements.

## Data Ownership

Each service should have clear ownership of the data it manages.

Sharing the same database directly between independent services can create strong coupling and make independent evolution difficult.

## Event-Driven Systems

Events can reduce direct dependencies and allow services to communicate asynchronously.

Important concerns include:

- Event schemas
- Idempotency
- Ordering
- Retry behavior
- Dead-letter handling
- Observability
- Event versioning

## Reliability

Distributed systems make failure more visible.

Important patterns include:

- Timeouts
- Retries
- Circuit breaking
- Idempotency
- Backpressure
- Graceful degradation

## Deployment

Containers provide a consistent way to package services.

Orchestration platforms can then handle scheduling, networking, scaling, and other operational concerns.

## Observability

Once an application is distributed, it becomes important to understand what happened across service boundaries.

Useful signals include:

- Logs
- Metrics
- Traces
- Correlation IDs
- Health checks

## Security

Each service should have appropriate authentication, authorization, and least-privilege access.

---

[Back to README](../README.md)
