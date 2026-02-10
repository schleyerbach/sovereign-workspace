# Sovereign Digital Workspace

This repository documents a **sovereign, browser-first digital workspace** designed as a
**reference architecture**, **learning project**, and **dogfooding environment**.

It demonstrates how collaboration, identity, and private AI capabilities can be implemented
in a **controlled, tenant-isolated, EU-based cloud setup** — without ideological constraints,
but with explicit architectural and governance decisions.

---

## Purpose

The project serves three closely related purposes:

1. **Personal dogfooding**  
   The stack is used productively by the initiator as an extended beta environment in order to
   validate architectural decisions under real-world conditions.

2. **Reference & demonstration**  
   The repository provides a structured, explainable blueprint that can be used to discuss,
   review, and demonstrate patterns for digital sovereignty, multi-tenancy, and private AI.

3. **Learning & iteration**  
   Architecture, tooling, and decisions are expected to evolve. Changes are documented,
   versioned, and refactored deliberately.

This is **not** a turnkey product, SaaS platform, or certified production environment.

---

## Scope & Non-Goals

### In scope
- Browser-first collaboration and workspace concepts
- Strong tenant isolation (tenant = technical security boundary)
- Central identity and access management (IAM-first)
- Private LLM usage with strict data boundaries (RAG, no training)
- EU-based runtime infrastructure
- Explicit governance and decision records

### Explicit non-goals
- Replacing enterprise groupware platforms (e.g. M365)
- Providing SLAs or high-availability guarantees
- Compliance certification (ISO, SOC, etc.)
- Commercial AI or SaaS product delivery

---

## Architectural Principles

The project is guided by a small set of explicit principles:

- **Conscious layering instead of dogma**  
  Reference artifacts may be hosted on non-EU platforms if runtime and data layers remain sovereign.

- **Tenant equals security boundary**  
  Each tenant is implemented as a fully isolated stack.

- **IAM-first**  
  No service is exposed without identity and access control.

- **LLM as assistive capability**  
  No training on tenant data, no cross-tenant inference, context-only usage.

- **Browser-first by design**  
  No required local clients or sync tools.

- **Demo-safe over high availability**  
  Simplicity and explainability take precedence over uptime.

- **Replaceability**  
  All components are considered replaceable; no hard vendor lock-in.

Details can be found in the governance documentation.

---

## Repository Structure

```text
docs/
  governance.md        # Governance model and guiding principles
  roadmap.md           # Versioned, high-level roadmap
  01-architecture/     # Architecture descriptions per version
  02-adrs/             # Architecture Decision Records (ADRs)
  03-runbooks/         # Operational notes (added later)
  04-threat-model/     # Trust boundaries and risks (added later)

infra/
  edge/                # Edge and ingress layer (from v0.2)
  core/                # Shared services (IAM, etc.)
  tenants/             # Tenant templates

scripts/               # Automation helpers (later)
secrets/               # Explicitly excluded from version control
```

---

## Transparency & Publication Model

This repository is **public by design**, but deliberately curated.

**Included**
- Documentation
- Architectural descriptions
- Decision records
- Sanitized templates and examples

**Explicitly excluded**
- Secrets or credentials
- Tenant-specific configuration
- Production or personal data

The goal is **explainability and reference**, not copy-paste deployment.

---

## Status

- Current version: **v0.1**
- Focus: Governance, roadmap, and architectural clarity
- No infrastructure or runtime components implemented yet

---

## License

The licensing model will be defined once the scope of reusable components becomes clearer.