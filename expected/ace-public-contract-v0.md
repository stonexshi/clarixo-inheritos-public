# ACE Public Contract v0

ACE stands for Attribution Classification Engine.

ACE is the classification direction emerging from CLARIXO InheritOS.

Its purpose is to classify reasoning material, governance material, continuity states, and human-AI interaction material based on attribution structure rather than surface keywords.

---

## Core principle

Classification authority should belong to attribution structure, not keywords.

A word appearing in a text should not automatically create a final classification.

A classification should be supported by reconstructable attribution conditions.

---

## What ACE may do

ACE may support classification of:

- reasoning continuity states,
- inherited instability patterns,
- responsibility boundaries,
- authority boundary conditions,
- evidence conflict states,
- execution-continuation risks,
- handoff and inheritance risks,
- topic and subtopic projection,
- material review objects,
- governance material,
- compliance material,
- audit-oriented review categories,
- and human-AI interaction states.

ACE should classify only when the attribution structure supports the classification.

---

## What ACE should not do

ACE should not act as:

- a keyword tagging system,
- a shallow topic model,
- a generic content classifier,
- a final legal authority,
- a final medical authority,
- a final financial authority,
- a final governance authority,
- or a replacement for human review.

ACE should provide classification support.

It should not pretend that a classification is valid without reconstructable support.

---

## Topic projection

Topic projection is allowed when the system can reasonably identify what a text is generally about.

For example, a text may discuss:

- governance,
- responsibility,
- auditability,
- evidence preservation,
- policy,
- risk,
- security,
- finance,
- healthcare,
- education,
- or compliance.

ACE may project topic or subtopic labels for such material.

But topic projection is not the same as Material Review.

---

## Material classification

Material classification requires a stronger attribution basis.

A Material Review result should require an explicit structured material object or equivalent attribution structure.

Domain vocabulary alone should not trigger Material Review.

For example, a text that only mentions governance, legal, finance, healthcare, policy, evidence, security, training, audit, or risk should not automatically become a material review case.

---

## Positive boundary

Material Review may be generated when a payload contains an explicit structured object such as:

    material_attribution:
      objects:
        - material_type: governance_policy_material
          subtype: policy_review
          confidence: 0.92

In this case, the classification has a structured attribution basis.

---

## Negative boundary

Material Review should not be generated only because a text says:

    governance
    legal
    finance
    healthcare
    policy
    security
    training
    evidence
    audit
    risk

These words may support topic projection.

They should not own final material classification authority.

---

## Topic projection vs Material Review

ACE separates two layers:

    topic projection
    → describes what the text is generally about

    material classification
    → requires stronger attribution structure

This separation prevents ordinary conceptual writing from being incorrectly treated as a structured material object.

---

## InheritOS relationship

InheritOS detects inherited instability and reasoning-continuity risks.

ACE extends this direction into attribution-first classification.

The relationship is:

    InheritOS detects unstable inheritance.
    Attribution structure explains why the state is classified.
    ACE turns attribution structure into classification support.

ACE should grow from InheritOS without replacing InheritOS.

---

## Public contract v0

ACE Public Contract v0 establishes these boundaries:

1. Keywords alone do not own classification authority.
2. Topic projection may exist without Material Review.
3. Material Review requires structured attribution support.
4. Classification should be reconstructable.
5. Attribution structure is stronger than surface vocabulary.
6. ACE supports classification, but does not replace final human or institutional judgment.

---

## Status

ACE is currently a public direction documented inside the CLARIXO InheritOS proof surface.

It should become a separate repository only after it has an independent schema, API, demo, or public test matrix.
