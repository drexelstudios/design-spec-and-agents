# Design Spec and Agents

A starter kit for building agentic AI workflows in product design. Developed as part of the IxDF Master Class #2 — *How to Build Agentic AI Workflows for Product Design*.

---

## What this is

Most designers use AI by prompting. This kit teaches you to design workflows.

The difference: a workflow has memory. It has principles. It has a persistent document that every AI session and every agent reads before doing anything. The output compounds across sessions. The system gets smarter with every run.

This kit gives you the foundation layer — the design spec template — and three starter agents that run on top of it.

---

## What is in this repo

### `design_spec_template.md`
The foundation. A tool-agnostic planning document written in plain language, structured for both human readability and AI context. Eight sections covering vision, audience, principles, scope, competitive landscape, open questions, artifacts and a corrections log.

Write Sections 1–4 first — vision, audience, principles, scope. These are the foundation and should exist before any agent runs. The remaining sections are populated by agents and updated continuously as the project moves.

**The corrections log (Section 9) is the most important section.** It is the mechanism that makes the system improve over time. Every time an agent gets something wrong, you log the fix. Every future session reads that log and does not repeat the mistake.

### `competitive_research_agent.md`
A first-pass competitive analysis agent. It reads your design spec, derives analysis dimensions from your design principles, proposes a competitive set for your approval, then produces hypotheses — not conclusions — grounded in what is observable.

Every output is labeled as a hypothesis with a validation method. The agent refuses to produce feature matrices or confidence-dressed-as-fact analysis.

Run this after Sections 1–4 of the spec exist.

### `user_modeling_agent.md`
A directional user modeling agent. It generates primary archetypes for the audience defined in your spec, surfaces adjacent audiences worth considering, and produces a research plan you can actually run with real users.

This agent does not simulate users or generate user quotes. It models hypothesized behavior and motivation, then tells you exactly how to validate each hypothesis with real people. The research plan is the artifact that earns this agent's place in the workflow.

Run this after the competitive research agent has produced its synthesis.

### `concept_validation_agent.md`
A pre-research concept validation agent. It reads everything the workflow has produced — spec, competitive analysis, user modeling — and evaluates whether the design decisions cohere against criteria it derives from the spec's own purpose and principles.

It tells you what the workflow already supports, what is at risk and what only real users can answer. The handoff to user research is explicit. The designer decision queue surfaces what you still owe yourself before build begins.

Run this after both the competitive research and user modeling agents have run.

### `IxDF_Agentic_Workflows_Design_Spec_Agents.zip`
A packaged download of all the above files. Use this if you want everything in one place.

---

## How to use this kit

**1. Copy `design_spec_template.md` into your project.** Rename it to reflect your project. Start filling in Sections 1 through 4.

**2. Copy whichever agent files apply.** Paste them into your AI tool of choice — Claude, ChatGPT, Gemini, Copilot, or any tool with a system prompt or agent file capability. The agents are tool-agnostic by design.

**3. Run agents in sequence.** Competitive research first. User modeling second. Concept validation third. Each agent reads what the previous one produced. The outputs compound.

**4. Update the spec after every run.** Sections 5, 6, 7, 8 and 9 evolve as agents produce outputs and you make decisions. The spec is not a one-time artifact — it is a living document.

**5. Log corrections.** Every time an agent gets something wrong, add an entry to Section 9. Write what happened, what you changed and the rule that prevents it from happening again. This is how the system improves.

---

## The four-component agent anatomy

Every agent in this kit follows the same structure. When you modify them or write your own, use this as the skeleton:

| Component | What it does |
|---|---|
| **Purpose** | One paragraph. What job does this agent do, and why does it exist in the workflow? |
| **Scope** | What the agent covers, what it deliberately does not touch, and what it refuses to produce. |
| **Instructions** | Step-by-step logic. The agent follows these in order. Each step either reads something, produces something or asks the designer a question. |
| **Output format** | Exactly what the agent returns — structure, length, tone. Removes ambiguity about what a successful run looks like. |

---

## Design principles this kit is built on

These are not rules for using the kit. They are the principles baked into how the kit was designed. They are worth knowing.

**The design spec is the system.** Prompts are instructions. A design spec is a system. One persists. The other resets.

**Plan before you execute.** The first prompt should ask AI to help you plan the work, not do it. The plan reveals the bottlenecks. The bottlenecks tell you where human judgment is required.

**Every output is a hypothesis.** No agent in this kit produces conclusions. Every output comes with a validation method. Confidence dressed as fact is a liability in design work.

**Human judgment is the product.** AI handles the volume. You handle what it means. The workflow is only as good as the principles you put into the spec.

---

## Context

This kit was built and demonstrated live during IxDF Master Class #2. The RSS feed aggregator walkthrough — competitive research, user modeling and concept validation run end-to-end using these exact files — is the reference implementation.

The design spec format is adapted from [Kiro's steering file pattern](https://kiro.dev), a structured approach to persistent agent context developed for software engineering workflows and applied here to product design.

---

## License

MIT. Use it, modify it, build on it. If you improve the agent files in ways that would help other designers, consider contributing back.
