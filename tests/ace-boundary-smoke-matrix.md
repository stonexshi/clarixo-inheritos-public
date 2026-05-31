# ACE Boundary Smoke Matrix

This file records the first public smoke matrix for CLARIXO ACE — Attribution Classification Engine.

ACE is the classification direction emerging from CLARIXO InheritOS.

Its core principle is:

> Classification authority should belong to attribution structure, not keywords.

---

## Status

ACE Boundary Smoke Matrix v0:

    RESULT=OPEN_PUBLIC_DIRECTION
    CONTRACT=ACE Public Contract v0
    SOURCE=InheritOS public proof surface

This matrix documents expected boundaries.

It is not yet a standalone ACE runtime certification matrix.

---

## Purpose

The ACE boundary smoke matrix checks whether the public classification direction preserves these boundaries:

- keywords alone do not own classification authority,
- topic projection may exist without Material Review,
- Material Review requires structured attribution support,
- continuity issues should not automatically become material classifications,
- explicit material objects may trigger Material Review,
- and Chinese-language inputs preserve the same classification boundaries.

---

## Smoke cases

| Case ID | Focus | Expected Boundary |
|---|---|---|
| ace_boundary_001_keywords_only | Domain keywords only | Topic projection allowed; Material Review not expected |
| ace_boundary_002_governance_article | General governance article | Topic projection allowed; Material Review not expected |
| ace_boundary_003_explicit_governance_object | Structured governance material object | Material Review expected |
| ace_boundary_004_finance_keywords_only | Financial vocabulary without object | Topic projection allowed; Material Review not expected |
| ace_boundary_005_explicit_financial_object | Structured financial material object | Material Review expected |
| ace_boundary_006_runtime_continuity_not_material | Continuity issue without material object | Continuity issue expected; Material Review not expected |
| ace_boundary_007_chinese_keywords_only | Chinese domain keywords without object | Topic projection allowed; Material Review not expected |
| ace_boundary_008_chinese_explicit_object | Chinese structured governance object | Material Review expected |

---

## Boundary 1: Keywords are not classification authority

Domain words may help describe what a text is about.

But they should not own final classification authority.

Examples:

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

Expected behavior:

    topic_projection_allowed=true
    material_review_expected=false

---

## Boundary 2: Topic projection is not Material Review

A general article may receive topic or subtopic projection.

This helps identify the general subject of the text.

But topic projection should not be treated as Material Review.

Expected behavior:

    topic_projection_allowed=true
    material_review_expected=false
    reason=topic_projection_only

---

## Boundary 3: Material Review requires attribution support

Material Review should require a structured attribution basis.

Example:

    material_attribution:
      objects:
        - material_type: governance_policy_material
          subtype: policy_review
          confidence: 0.92

Expected behavior:

    material_review_expected=true
    classification_authority=structured_attribution_object

---

## Boundary 4: Runtime continuity is not automatically material classification

A text may describe inherited instability, responsibility rebinding, or evidence conflict.

That can create a continuity issue.

But it should not automatically create Material Review unless a structured material object is present.

Expected behavior:

    continuity_issue_expected=true
    material_review_expected=false

---

## Boundary 5: Chinese inputs preserve the same contract

Chinese-language inputs should follow the same boundary rules as English inputs.

Chinese domain keywords alone should not trigger Material Review.

Chinese explicit structured material objects may trigger Material Review.

Expected behavior:

    language_boundary_consistent=true

---

## Public contract alignment

This matrix aligns with:

    expected/ace-public-contract-v0.md
    examples/ace-boundary-examples.json
    theory/04-classification-engine-direction.md

Together, these files define the first public ACE direction inside the InheritOS proof surface.

---

## Result

ACE Boundary Smoke Matrix v0 establishes the public expected boundary:

    Keywords may support topic projection.
    Attribution structure owns classification authority.
    Material Review requires structured support.

This closes the first public ACE direction layer inside the CLARIXO InheritOS repository.
