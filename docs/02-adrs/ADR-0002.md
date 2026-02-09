ADR-0002 — IAM-First Architecture

Status: Accepted

Context:
Multiple services, including AI components, require consistent and enforceable access control.

Decision:
All user and service access is mediated through a central IAM, with tenant-specific identity domains.

Consequences:
	•	Consistent authentication and authorization
	•	Mandatory integration effort for new services
	•	Clear security model for demos and explanations

⸻