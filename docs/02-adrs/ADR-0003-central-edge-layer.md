# ADR-0003: Central Edge Layer

## Status
Accepted

## Context
The platform consists of multiple isolated tenant stacks and shared core services.
A consistent, secure, and explainable ingress mechanism is required to control how
external traffic enters the system and is routed to internal components.

Without a clearly defined edge layer, responsibilities such as TLS termination,
routing, and baseline protection would be duplicated across services or mixed with
business logic.

## Decision
A **central edge layer** is introduced as the single controlled entry point into the platform.

The edge layer is responsible for:
- TLS termination
- Host- and path-based routing
- Basic request validation and rate limiting
- Forwarding traffic to tenant stacks or core services

The edge layer explicitly does **not**:
- Implement business logic
- Perform tenant authorization decisions
- Persist data
- Make identity decisions (delegated to IAM)

## Consequences
- Clear separation of concerns between ingress, identity, and application logic
- Reduced blast radius: compromise of the edge does not directly expose tenant data
- Simplified tenant onboarding and refactoring
- Slightly increased infrastructure complexity due to an additional layer

This trade-off is accepted in favor of clarity, security, and explainability.