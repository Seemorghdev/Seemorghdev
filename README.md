<h1 align="center">Mehrdad Touraji</h1>

<p align="center">
  <strong>Python Systems & Platform Engineer</strong><br />
  Building reliable Python, cloud, and distributed systems with strong operational boundaries.
</p>

```text
$ whoami
Mehrdad Touraji

$ focus
platforms · automation · reliable systems

$ status
building
```

<p align="center">
  <img alt="Python" src="https://img.shields.io/badge/Python-111827?style=flat-square&logo=python&logoColor=white" />
  <img alt="Google Cloud" src="https://img.shields.io/badge/Google_Cloud-111827?style=flat-square&logo=googlecloud&logoColor=white" />
  <img alt="Terraform" src="https://img.shields.io/badge/Terraform-111827?style=flat-square&logo=terraform&logoColor=white" />
  <img alt="Kubernetes" src="https://img.shields.io/badge/Kubernetes-111827?style=flat-square&logo=kubernetes&logoColor=white" />
  <img alt="Linux" src="https://img.shields.io/badge/Linux-111827?style=flat-square&logo=linux&logoColor=white" />
  <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub_Actions-111827?style=flat-square&logo=githubactions&logoColor=white" />
</p>

---

## What I build

I work on systems where correctness, reproducibility, and operational clarity matter.
My current focus includes:

- deterministic processing and replication workflows
- bounded worker services with explicit authority boundaries
- Python automation and command-line tooling
- cloud infrastructure and deployment foundations
- CI-backed validation, regression testing, and release evidence
- framework-neutral contracts for controlled agent workflows

I care about software that is understandable under pressure: clear ownership, safe retries, observable state transitions, and documentation that matches the running system.

## Current flagship work

### Edge Evidence — flagship

**[Edge Evidence Showcase](https://github.com/Seemorghdev/edge-evidence-showcase)** is the public front door: recruiter navigation, reproducible proof, synthetic integration, and explicit claim boundaries.

Edge Evidence is one flagship ecosystem, split by authority so each layer has a clear engineering role:

- **Reliable Engine — Processor + Replication.** Deterministic processing, checkpoint/recovery, lineage verification, replay-safe behavior, immutable replication, collision refusal, independent readback, and deterministic convergence. The canonical Processor and Replication products remain private. The public **[processor-worker](https://github.com/Seemorghdev/edge-evidence-processor-worker)** and **[replication-worker](https://github.com/Seemorghdev/edge-evidence-replication-worker)** repositories are legacy generated inspection windows only — not canonical authorities or separate headline projects.
- **Reference Platform — application/product layer.** Web UI, Evidence API, and Edge Agent compose browser/application interaction, artifact access, bounded inspection, and accepted local/containerized and cloud reviewer evidence around the deterministic components. Canonical source and private provider details remain private.
- **[Infrastructure](https://github.com/Seemorghdev/edge-evidence-infrastructure) — reviewed desired state + platform guardrails.** This is the direct public technical surface for what reviewed platform state should exist; Terraform/CI and desired state do not grant themselves live execution authority.
- **Operations — control plane + evidence governance.** Reviewed changes follow a compact control path: `intent → identity → duplicate/history check → policy → runbook binding → one attempt → receipt → verification → evidence`. Execution authority remains separate from Infrastructure desired state.
- **Showcase — public proof + navigation + reproducibility.** It is the recruiter-facing entry point and evidence boundary, not a replacement implementation authority for the layers above.

## Engineering approach

```text
inspect → classify → propose → authorize → execute → verify → record
```

- Prefer explicit contracts over hidden behavior
- Design retries to be safe and deterministic
- Keep infrastructure, application, and authority boundaries visible
- Treat tests and documentation as part of the product
- Fail closed when identity, provenance, or state cannot be verified
- Use automation and agent-assisted workflows for throughput while keeping architecture, boundaries, acceptance criteria, verification, and merge decisions under explicit owner control

## Selected technologies

**Languages:** Python, HCL, Bash  
**Infrastructure:** Google Cloud, Terraform, Kubernetes, Cloud Run  
**Systems:** Linux, SQLite, immutable object workflows, distributed workers  
**Delivery:** GitHub Actions, CI/CD, automated validation, reproducible builds  
**Current interests:** platform engineering, infrastructure automation, reliable agent systems, evidence pipelines

## Open to opportunities

I am open to remote, hybrid, and relocation opportunities across:

- Platform Engineering
- Cloud / DevOps Engineering
- Infrastructure Automation
- Python Systems Engineering
- Site Reliability and Technical Operations
- QA Automation and Developer Support
- AI infrastructure and controlled agent platforms

I value practical teams, clear ownership, and work that ships.

---

<p align="center">
  <em>Seemorgh: a symbol of wisdom, resilience, and guidance — reflected here as careful engineering and systems that can be trusted.</em>
</p>
