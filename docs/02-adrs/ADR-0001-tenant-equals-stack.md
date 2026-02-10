ADR-0001 — Tenant Equals Stack

Status: Accepted

Context:
The platform must support multiple tenants in a demo-safe manner without complex authorization logic.

Decision:
Each tenant is implemented as a fully isolated application stack, including its own services and data stores.

Consequences:
	•	Strong technical isolation
	•	Simplified reasoning about data boundaries
	•	Higher resource usage, accepted by design

⸻