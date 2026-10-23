<h1 align="center">Mehrdad Touraji</h1>

<p align="center">
  <strong>Python Systems & Platform Engineer</strong><br />
  Building reliable Python, cloud, and distributed systems with strong operational boundaries.
</p>

**Portfolio & documentation:** [Mehridian](https://mehridian.tech/) · [Edge Evidence case study](https://mehridian.tech/projects/edge-evidence) · [Technical Docs](https://docs.mehridian.tech/edge-evidence/)

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

## How I work

I use agent-assisted engineering workflows to increase throughput on bounded implementation, testing, documentation, repository maintenance, and verification tasks.

I retain responsibility for architecture, requirements, system boundaries, acceptance criteria, review, validation, and publication decisions. Generated work is treated as a candidate until it passes the relevant checks and review gates.

This workflow can produce unusually high GitHub activity, including coordinated changes across repositories, generated public projections, validation passes, and documentation synchronization. I do not use commit count as a productivity metric; evaluate the work through the resulting code, tests, CI, reproducibility, review history, and documented boundaries.

See **[Engineering Workflow](ENGINEERING-WORKFLOW.md)** for the operating model behind the activity graph.

## Featured model release

### [YOLO11n AOD4 v6 — airborne-object detection](https://github.com/Seemorghdev/yolo11n-aod4-v6)

**[GitHub release](https://github.com/Seemorghdev/yolo11n-aod4-v6)** · **[Hugging Face model](https://huggingface.co/Seemorgh/yolo11n-aod4-v6)** · **[Training report](https://github.com/Seemorghdev/drone-detection-showcase/blob/main/docs/training-report.md)**

A reviewed archival release of a four-class Ultralytics YOLO11n checkpoint for **airplane, bird, drone, and helicopter** detection. The public release includes recovered weights (Git LFS), sanitized notebooks, provenance records, and SHA-256 checksums.

The retained validation record reports **mAP50 0.96518** and **mAP50–95 0.66663** across **4,514 images**, aggregated over all four classes. These are historical validation results, not independently reproduced measurements, drone-only scores, or evidence of field reliability. The original application and raw dataset are not published. The release preserves the model's **AGPL-3.0** notice, with separate **CC BY 4.0** dataset attribution.

## Current flagship work

### Edge Evidence — flagship

Edge Evidence explores how to preserve evidence, process it reliably, and verify that copies match the original.

**[Open the live Visual Gateway](https://edge-evidence-visual-gateway-2e3eaeb86f95.herokuapp.com/)** — start here. Explore three synthetic examples in a Web UI backed by an Evidence API and a read-only Edge Agent. Click **Explain this example** to understand each state and what a reviewer can inspect. This page inspects example states; it does not execute the complete processing and replication workflow.

**[Deeper technical proof — Processor + Replication (JSON/API)](https://seemorgh-evidence-showcase-45655632eff2.herokuapp.com/api/demo)** — view a synthetic processing result, a verified handoff to replication, independent readback of the copied bytes, and replay with no new writes. This endpoint returns JSON, not a visual application. Both demos use synthetic data and make no production-service claim.

**Explore the public code:** [Processor](https://github.com/Seemorghdev/edge-evidence-processor-public) · [Replication](https://github.com/Seemorghdev/edge-evidence-replication-projection) · [Reference Platform: UI, API, Agent and gateway](https://github.com/Seemorghdev/edge-evidence-reference-platform-public). The [Showcase repository](https://github.com/Seemorghdev/edge-evidence-showcase) explains how to reproduce the technical proof.

Earlier GKE and Cloud Run deployments are retained as historical engineering evidence. They are not presented as currently operational demos; the Heroku links above are the current visitor entry points.

Edge Evidence is one flagship ecosystem, split by authority so each layer has a clear engineering role:

- **Reliable Engine — Processor + Replication.** Deterministic processing, checkpoint/recovery, lineage verification, replay-safe behavior, immutable replication, collision refusal, independent readback, and deterministic convergence. Canonical implementation authority remains private. Recruiters can review the current public **[Processor projection](https://github.com/Seemorghdev/edge-evidence-processor-public)** and **[Replication projection](https://github.com/Seemorghdev/edge-evidence-replication-projection)**. The older processor/replication worker repositories remain legacy generated demo exports, not headline portfolio projects.
- **[Reference Platform](https://github.com/Seemorghdev/edge-evidence-reference-platform-public) — application/product layer.** Web UI, Evidence API, and read-only Edge Agent provide the visual inspection experience. The live Heroku gateway combines these responsibilities in one runtime for this synthetic demonstration; it does not claim production-grade service isolation. Historical cloud validation is separate from today's live demo. Canonical source and private provider details remain private.
- **[Infrastructure](https://github.com/Seemorghdev/edge-evidence-infrastructure) — reviewed desired state + platform guardrails.** This is the direct public technical surface for what reviewed platform state should exist; Terraform/CI and desired state do not grant themselves live execution authority.
- **[Operations](https://github.com/Seemorghdev/edge-evidence-operations-public) — control plane + evidence governance.** Reviewed changes follow a compact control path: `intent → identity → duplicate/history check → policy → runbook binding → one attempt → receipt → verification → evidence`. The public projection is recruiter-facing; canonical execution/governance authority remains private and separate from Infrastructure desired state.
- **Showcase — technical execution proof + reproducibility.** It provides the deeper synthetic Processor + Replication JSON/API demonstration and instructions for running that proof locally.

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
