# Microservices Notes

Microservices are useful when service boundaries solve a real organizational, scaling, deployment, or ownership problem.

They also introduce significant operational complexity, so I treat them as an architectural choice rather than a default pattern.

## Service Boundaries

A service should have a clear responsibility and a well-defined interface.

Good boundaries help reduce unnecessary coupling and make ownership clearer.

## Communication

Common communication patterns include:

- Synchronous HTTP/REST
- gRPC
- Asynchronous messaging
- Domain events

The appropriate choice depends on latency, coupling, reliability, and consistency requirements.

## Data Ownership

Each service should have clear ownership of the data it manages.

Directly sharing databases between independent services can create strong coupling and make independent evolution more difficult.

## Event-Driven Systems

Events can help services communicate asynchronously and reduce direct dependencies.

Important concerns include:

- Event schemas
- Idempotency
- Ordering
- Retry behavior
- Dead-letter handling
- Observability
- Event versioning

## Reliability

Distributed systems require explicit handling of failure.

Important patterns include:

- Timeouts
- Retries
- Circuit breaking
- Idempotency
- Backpressure
- Graceful degradation

## Deployment

Containers make it easier to package and deploy independent services consistently.

Cloud platforms and orchestration systems can then provide scheduling, scaling, networking, and operational capabilities.

## Observability

A distributed application should provide enough information to understand what happened across service boundaries.

Useful signals include:

- Logs
- Metrics
- Traces
- Correlation IDs
- Health checks

## Security

Each service should operate with appropriate authentication, authorization, and least-privilege access.

---

[Back to README](../README.md)
