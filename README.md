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

## Core idea

Modern AI systems often fail not because a single output is wrong, but because an unstable state is allowed to continue.

An error becomes more dangerous when it is inherited by the next reasoning step, the next agent, the next reviewer, the next workflow, or the next governance layer.

InheritOS focuses on the inheritance boundary:

```text
state → continuation → inheritance → instability propagation
