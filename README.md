# CLARIXO InheritOS

**CLARIXO InheritOS is a cross-human-and-AI OS for detecting inherited instability in reasoning.**

It focuses on a simple but important governance question:

> When a reasoning process continues, is it still allowed to inherit the previous state?

InheritOS is designed to detect where unstable reasoning states begin to be inherited across human reasoning, AI reasoning, agent workflows, governance processes, and classification systems.

Public demo:

https://tgtracing.com/go/app/public/?p=inheritos

---

## What this repository is

This repository is a public proof surface for CLARIXO InheritOS.

It is intended to document:

- the core theory behind inherited instability detection,
- example inputs,
- expected outputs,
- public smoke-test matrices,
- attribution-first classification boundaries,
- and the transition from Attribution Layer to Classification Engine.

This repository is not the private commercial runtime implementation.

---

## ACE direction

InheritOS has also opened a public direction toward:

> CLARIXO ACE — Attribution Classification Engine

ACE is not a keyword classifier.

ACE is an attribution-first classification engine.

Its core principle is:

> Classification authority should belong to attribution structure, not keywords.

This direction is documented in:

- `theory/04-classification-engine-direction.md`
- `expected/ace-public-contract-v0.md`
- `examples/ace-boundary-examples.json`
- `tests/ace-boundary-smoke-matrix.md`

ACE remains inside this InheritOS public proof surface for now.

It should become a separate repository only after it has an independent schema, API, demo, or public test matrix.

---

## Core idea

Modern AI systems often fail not because a single output is wrong, but because an unstable state is allowed to continue.

An error becomes more dangerous when it is inherited by the next reasoning step, the next agent, the next reviewer, the next workflow, or the next governance layer.

InheritOS focuses on the inheritance boundary:

    state → continuation → inheritance → instability propagation

The central question is not only:

    Is this answer correct?

but also:

    Should this reasoning state be allowed to continue?

---

## Why inheritance matters

A reasoning state may become unstable when:

- responsibility is not properly attributed,
- authority is unclear,
- evidence is missing or contradicted,
- execution continues from an unresolved boundary,
- classification is assigned by keywords instead of structure,
- or a previous conclusion becomes silently inherited without revalidation.

InheritOS treats these as continuity and attribution problems.

---

## Attribution-first classification

InheritOS does not treat keyword matching as final classification authority.

A text mentioning words such as governance, legal, policy, risk, evidence, security, training, or finance should not automatically be classified into those domains.

Classification should come from attribution structure.

InheritOS uses attribution signals such as:

- responsibility,
- authority,
- evidence,
- execution,
- continuity,
- inheritance,
- and material object boundaries.

This leads toward a broader component:

> CLARIXO ACE — Attribution Classification Engine

ACE is not yet separated into its own repository. For now, the attribution-to-classification direction is documented inside this InheritOS public proof surface.

---

## Public status

Current public state:

- CLARIXO InheritOS Early Public Access is live.
- Launch-R1 public access smoke matrix is closed.
- Public launch smoke result: `PASS_COUNT=7`, `FAIL_COUNT=0`.
- Topic classification is now bound to attribution output.
- Material Review remains object-only.
- Non-object governance articles use attribution topic projection and do not trigger Material Review.
- Explicit material objects can trigger Material Review and lower-level topic classification.
- ACE public direction layer v0 is documented inside this repository.

---

## Repository structure

    theory/

Theory notes and boundary explanations.

    examples/

Input examples for reasoning continuity, inherited instability, and attribution-first classification.

    expected/

Expected output examples and public contract expectations.

    tests/

Smoke matrices and public test descriptions.

---

## Design principle

A useful governance theory should work across both AI systems and human reasoning systems.

If a theory only works for AI, it may be an application-layer framework.

If it works across AI and human society, it may be closer to a bottom-layer theory.

InheritOS explores that lower layer.

---

## Slogan

**Make the world more orderly.**
