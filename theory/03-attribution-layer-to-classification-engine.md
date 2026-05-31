# Attribution Layer to Classification Engine

InheritOS uses an attribution-first approach to classification.

This means that classification should not be controlled by surface keywords alone.

A text may mention governance, legal, policy, evidence, finance, security, training, or risk without actually belonging to those material categories.

InheritOS treats classification as a structural attribution problem.

---

## The problem with keyword authority

Keyword-based classification is fragile.

If classification authority is given to keywords, the system quickly enters a keyword arms race.

Every new test case may expose another phrase, synonym, or surface expression that needs to be added.

This leads to fragile classification logic.

The deeper problem is that keywords describe language, but they do not always describe responsibility structure.

---

## Attribution-first classification

InheritOS shifts classification authority to the attribution layer.

The attribution layer examines structural signals such as:

- who or what carries responsibility,
- what authority is being invoked,
- what evidence is being used,
- whether execution is actually involved,
- whether a reasoning state is being inherited,
- whether a material object is explicitly present,
- and whether the classification has a grounded attribution source.

Classification should emerge from these attribution conditions.

It should not be assigned only because a word appeared in the text.

---

## Material Review boundary

InheritOS keeps Material Review object-bound.

This means that ordinary articles, essays, or conceptual discussions should not automatically trigger Material Review just because they contain domain words.

For example, a governance article may discuss policy, responsibility, evidence, authority, and risk.

That alone should not create a Material Review result.

Material Review should appear when there is an explicit material object or attribution structure that supports it.

---

## Topic projection vs Material Review

InheritOS separates topic projection from Material Review.

A non-object text may still receive topic or subtopic projection.

This helps the system understand what the text is generally about.

But topic projection is not the same as Material Review.

Material Review requires a stronger attribution basis.

This separation prevents general discussion from being incorrectly treated as a structured material object.

---

## Toward CLARIXO ACE

The attribution-first classification direction leads toward:

> CLARIXO ACE — Attribution Classification Engine

ACE is the future classification engine direction emerging from InheritOS.

Its purpose is to classify based on attribution structure rather than keyword authority.

For now, ACE is documented inside this InheritOS public proof surface.

It should not yet be treated as a separate repository until it has an independent API, schema, demo, or public contract.

---

## Core principle

The core principle is:

> Classification authority should belong to attribution structure, not keywords.

This is one of the central lessons from InheritOS development.

When classification logic was placed in the lower execution layer, the system became fragile.

When classification authority moved back to the attribution layer, the structure became clearer, more stable, and easier to test.

InheritOS preserves that boundary.
