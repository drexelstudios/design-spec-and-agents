# [Project Name] — Design Spec

**Version.** v0.1 ([YYYY-MM-DD])
**Status.** [Draft / Active / Locked for build]
**Owner.** [Your name]

---

## 1. Vision and Intent

*One to three paragraphs naming what this product is, who it serves and what success looks like at a long horizon. This is the soul of the spec. Every downstream decision filters through it.*

[What problem does this product solve, for whom, and why does it matter? What does the long-horizon aspiration look like once this product is doing its job? Avoid feature language. Stay at the level of intent.]

---

## 2. User Context

*Who the product is for. The audience definition is locked at the v1 distribution level. Archetypes get added here once user modeling synthesis runs.*

### Primary audience

[Define the v1 audience. Be specific about distribution scope, e.g. "friends and family pilot," "internal beta within Company X," "open public beta." This scope is one of the most important constraints in the spec.]

### Shared trait

[The single most important characteristic this audience shares. The trait that makes the product land for them in a way it wouldn't for a broader audience.]

### Archetypes

*Populated by the user modeling agent. Each archetype names a working profile, motivation, behavioral context, frustrations and validation method.*

[To be added when the user modeling agent runs.]

### Adjacent audiences flagged

*Populated by the user modeling agent. Audiences the spec doesn't currently address but should consider.*

[To be added when the user modeling agent runs.]

---

## 3. Design Principles

*The non-negotiables. Each principle is one sentence. Principles filter every design decision. The agents read these and refuse to produce output that violates them.*

1. **[Principle name].** [One-sentence description of what this principle commits the design to. Frame in positive terms, e.g. "the design serves X" rather than "the design avoids Y."]

2. **[Principle name].** [Description.]

3. **[Principle name].** [Description.]

[Add more as needed. Five to eight principles is typical. Fewer than four risks being too vague to filter decisions. More than ten risks being too specific to enforce consistently.]

---

## 4. Scope and Constraints

### In scope for v1

- [List the design surfaces, features, behaviors that v1 commits to delivering.]
- [Be specific. "Onboarding" is too vague. "Topic-based starter pack onboarding for first-time users on mobile and desktop" is the right level.]

### Out of scope for v1

- [List the surfaces, features, behaviors that v1 explicitly does not include. Naming them as out-of-scope prevents scope creep and gives the design spec a defendable boundary.]

### Hard limits

- [Constraints the product cannot violate. Technical limits, regulatory limits, business limits, brand limits.]
- [Examples: "Must run as a PWA, no native app for v1." "All data stored in EU regions." "No advertising, ever."]

---

## 5. Competitive Landscape

*Populated by the competitive research agent. Distilled hypotheses with rationale and validation methods. Full per-competitor analysis lives in the separate competitive_analysis.md artifact.*

[To be added when the competitive research agent runs.]

---

## 6. Open Questions and Decisions Log

### Open questions

*Questions the spec has not yet resolved. Numbered for traceability. New questions surface during agent runs and get added here. Resolved questions move to the Decisions Log.*

**Q1. [Question].** [Brief context. Resolution timing if known, e.g. "Resolution before Phase 2," "Parked for v2."]

**Q2. [Question].** [Context.]

### Decisions Log

*Forward-looking decisions captured as they happen. Each entry includes what was decided, why and the date.*

**[YYYY-MM-DD] — [Decision title].**
[One paragraph capturing what was decided, what was considered, why this path was chosen.]

---

## 7. Pre-build Decision Queue

*Populated by the concept validation agent. Decisions the designer still owes themselves before build begins. Prioritized by build-blocking severity.*

[To be added when the concept validation agent runs.]

---

## 8. Artifacts

*Inventory of files produced by the workflow. Each entry names the artifact, its date and its status.*

| Artifact | Status | Date |
|----------|--------|------|
| design_spec.md (this file) | Active | [YYYY-MM-DD] |
| competitive_analysis.md | To be produced | — |
| user_modeling.md | To be produced | — |
| v1_research_plan.md | To be produced | — |
| concept_validation.md | To be produced | — |

---

## 9. Corrections Log

*Backward-looking entries. What went wrong during a workflow run, what was changed and the rule that prevents recurrence. Rules from this section can graduate to Section 3 (Design Principles) when they generalize across multiple projects.*

**[YYYY-MM-DD] — [Correction title].**

*What went wrong.* [Brief description of the failure mode. What the agent did or what the workflow produced that was incorrect, off-target or harmful.]

*What was changed.* [The fix. Updated agent file, updated principle, updated process.]

*Rule that prevents recurrence.* [The generalizable lesson, written as a rule. Candidate for graduation to Section 3 if it applies beyond this project.]

---

## How to use this template

1. **Start with Sections 1 through 4.** Vision, audience, principles, scope. These are the foundation and should be drafted before any agents run.
2. **Run the competitive research agent.** It populates Section 5 with distilled hypotheses.
3. **Run the user modeling agent.** It populates Section 2 with archetypes and adjacent audiences.
4. **Run the concept validation agent.** It populates Section 7 with the pre-build decision queue.
5. **Update Sections 6, 8 and 9 continuously.** Open questions, artifacts inventory and corrections log evolve throughout the workflow.

The spec is a living document. Every workflow run updates it. The header version bumps when material changes happen (new section content, locked decisions, scope shifts). Treat the spec as the source of truth and the artifacts as the supporting evidence.
