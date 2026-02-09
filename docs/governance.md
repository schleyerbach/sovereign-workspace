# Sovereign Digital Workspace – Governance & Principles (v0.1)

## 1. Purpose & Scope

This project defines and implements a **reference architecture for a sovereign, browser‑first digital workspace** with strong identity control, tenant isolation, and private LLM usage.

The stack is:

* **Actively used in production by the initiator** (dogfooding / extended beta)
* **Demo‑ and reference‑ready** for explaining, sharing, and discussing architectural patterns
* **Not** operated as a customer production platform with SLAs or certifications

The primary goals are learning, architectural clarity, and demonstrability — not product commercialization at this stage.

---

## 2. Guiding Principles

### P1 — Conscious Layering, Not Ideology

Digital sovereignty is achieved through **clear separation of layers**, not absolute exclusion of all non‑EU tools.

* **Reference Layer**: Documentation, architecture, and templates may be hosted on non‑EU platforms if this improves reach and explainability.
* **Runtime Layer**: All running services, workloads, and processing occur in EU‑based, self‑controlled infrastructure.
* **Data Layer**: All operational data remains under full control of the operator and is never stored in third‑party SaaS platforms.

---

### P2 — Tenant = Security Boundary

Each tenant is treated as a **technical security perimeter**.

* One tenant equals one isolated application stack
* No shared databases or storage across tenants
* Full visibility within a tenant; zero visibility across tenants

This approach prioritizes clarity and safety over resource efficiency.

---

### P3 — IAM‑First Architecture

Identity and access management is foundational.

* No service is exposed without authentication
* All user and API access is validated through a central IAM
* Authorization is enforced server‑side, not only at UI level

Identity is the single source of truth for access decisions.

---

### P4 — LLM as Assistive Capability

LLM functionality is designed as **assistive intelligence**, not autonomous execution.

* No training on tenant data
* Tenant data is used only as ephemeral context (RAG)
* No cross‑tenant inference or data sharing
* No autonomous agents performing actions in v1

---

### P5 — Browser‑First by Design

All functionality is accessible via the browser.

* No required desktop or mobile clients
* No local sync or offline copies
* Reduced attack surface and simpler governance

This is a conscious trade‑off against convenience.

---

### P6 — Demo‑Safe Over High Availability

The system prioritizes **understandability and correctness** over availability.

* Planned downtime is acceptable
* No high‑availability or multi‑region setup
* Operational simplicity is favored

---

### P7 — Replaceability of Components

No component is considered irreplaceable.

* Container‑based deployment
* Open data formats
* Clear exit paths for all core services

Sovereignty is defined as the ability to change, not permanence.

---

### P8 — Dogfooding with Explicit Risk Acceptance

The initiator uses the stack productively for daily work.

* This increases realism and architectural rigor
* Operational risk is consciously accepted
* This does **not** imply customer‑grade production readiness

---

## 3. Transparency & Publication Model

### Public Reference Repository

This project is published as a **curated public repository**.

The repository contains:

* Architecture documentation
* Governance principles
* Decision records (ADRs)
* Templates and examples

The repository explicitly excludes:

* Secrets or credentials
* Tenant‑specific configuration
* Production data

The purpose of publication is **explainability and reference**, not turnkey reuse.

---

## 4. Data Classification

| Classification | Description                  | Repository Allowed |
| -------------- | ---------------------------- | ------------------ |
| Public         | Architecture, docs, diagrams | Yes                |
| Internal       | Templates, scripts           | Yes (sanitized)    |
| Restricted     | Tenant data, secrets         | Never              |

---

## 5. Change & Versioning Model

* Semantic Versioning (MAJOR.MINOR.PATCH)
* MINOR versions indicate architectural evolution
* Architecture changes require an ADR
* Refactoring is expected and documented

---

## 6. Explicit Non‑Goals

This project does **not** aim to:

* Replace enterprise groupware platforms
* Provide certified compliance (ISO, SOC, etc.)
* Act as a commercial AI or SaaS product

---

## 7. Outlook

Future evolution may include:

* Productization of selected components
* Migration of the reference layer to EU‑hosted git platforms
* Advanced LLM workflows

Such steps require explicit architectural and governance decisions.

---

**Status:** Accepted
**Version:** v0.1
