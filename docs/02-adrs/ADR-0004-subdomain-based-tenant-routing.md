# ADR-0004: Subdomain-Based Tenant Routing

## Status
Accepted

## Context
The platform must support multiple tenants in a demo-safe and explainable manner.
Tenant isolation is a core principle, and routing decisions must not rely on
application-level logic alone.

Path-based multi-tenancy increases coupling between routing and application logic
and makes isolation harder to reason about and demonstrate.

## Decision
Tenant routing is implemented using **subdomain-based addressing**.

The naming pattern is defined as:
- `iam.<domain>` for central identity services
- `<tenant>.workspace.<domain>` for tenant workspaces
- `<service>.<tenant>.workspace.<domain>` for tenant-local services

Routing decisions are made at the edge layer based on the requested hostname.

## Consequences
- Strong visual and technical separation between tenants
- Clear certificate and DNS boundaries per tenant
- Simplified reasoning about trust boundaries
- Easier tenant onboarding and removal

Trade-offs include increased DNS management effort and a larger number of hostnames,
which are accepted in favor of isolation and clarity.