# Engineering Workflow

## Why this document exists

Some of the repositories on this profile have unusually dense commit and review activity.

That activity reflects an agent-assisted engineering workflow rather than an attempt to use commit volume as a measure of productivity.

The purpose of this document is to make the operating model explicit: what is automated, what remains under human control, how changes are reviewed, and what evidence should actually be used to evaluate the work.

## Operating model

I use software agents and automation as engineering executors for bounded tasks.

Typical delegated work includes:

- scoped implementation
- tests and regression checks
- documentation updates
- repository maintenance
- generated public-safe projections
- validation and inspection tasks
- repetitive synchronization work

The agents are not the authority for the system.

I remain responsible for:

- architecture and technical direction
- requirements and task boundaries
- security and publication boundaries
- acceptance criteria
- deciding what claims are supported
- reviewing generated changes
- verification and release decisions
- merges and publication
- provider/cloud actions that require explicit authority

A generated change is a candidate, not an accepted result.

## Typical change flow

The general control path is:

```text
inspect
→ define the task and boundaries
→ delegate bounded work
→ review the result
→ run tests and CI
→ verify evidence and claims
→ accept or reject
→ publish when explicitly authorized
```

Different repositories use different mechanics, but the principle is consistent: implementation throughput may be automated while authority remains explicit.

## Why the commit volume is high

This workflow can create substantially more Git activity than a traditional one-person, one-terminal development process.

Several factors contribute:

1. Multiple bounded tasks can progress independently.
2. Implementation, tests, documentation, and validation may be committed separately.
3. Review corrections create additional iterations.
4. Some portfolio components maintain private canonical source and separate public-safe projections.
5. Generated or synchronized presentation surfaces may receive their own commits.
6. CI and verification feedback can trigger small corrective passes.
7. Publication itself is treated separately from implementation.

As a result, raw commit counts are not a meaningful estimate of manual typing time or engineering productivity.

They should not be interpreted that way.

## Canonical source and public projections

Some projects separate implementation authority from recruiter-facing publication.

For example, the Edge Evidence portfolio keeps selected canonical repositories private while exposing reviewed public projections for inspection.

The public projection is not automatically the implementation authority. It exists to make relevant engineering evidence reviewable without publishing private state, credentials, provider details, or other material outside the public boundary.

This separation also creates additional repository activity because publication is an explicit engineering step rather than a side effect of development.

## Review and verification

Agent-produced work is expected to be inspectable.

Depending on the task, acceptance can include:

- code review
- exact commit or tree identity checks
- automated tests
- CI results
- deterministic/reproducible runs
- integration tests
- security or publication-boundary checks
- documentation/implementation consistency checks
- independent review of a publication candidate

The important artifact is therefore not the number of commits.

It is the accepted system state and the evidence supporting it.

## What I consider my work

Using agents changes the mechanics of implementation, but it does not remove engineering responsibility.

My contribution is primarily in:

- defining the problem
- designing the architecture
- decomposing work into safe boundaries
- specifying interfaces and invariants
- deciding what automation may and may not do
- evaluating proposed implementations
- resolving failures and conflicts
- validating the integrated system
- controlling publication and operational authority

Where agents produce implementation or documentation, I do not represent the process as entirely manual development.

Likewise, I do not treat generated output as correct merely because it was generated.

## How to evaluate these repositories

I recommend evaluating the portfolio through:

- architecture and system boundaries
- implementation quality
- tests
- CI
- failure and recovery behavior
- reproducibility
- public claim boundaries
- review history
- runnable demonstrations
- consistency between documentation and actual behavior

I do not consider contribution counts, streaks, or raw commit volume meaningful engineering metrics.

The GitHub activity graph is a by-product of the workflow, not its objective.
