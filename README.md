# Personas

A collection of persona files used to shape the behaviour of AI models.

---

## How to Talk to an LLM

Start with three blocks — add more only when the output isn't what you need.

| Block | Purpose | Example |
|-------|---------|---------|
| **Persona** | *Who* the model should be | *"Act as a senior cloud architect"* |
| **Task** | *What* you want done | *"Review this Dockerfile for security issues"* |
| **Constraints** | Boundaries and rules | *"No paid services; under 200 words"* |

**Need more control?** Layer in as needed:

- **Context** — background info the model doesn't have
- **Output Format** — table, bullet list, JSON, etc.
- **Examples** — show one good input → output pair
- **Chain-of-Thought** — ask it to reason step by step

---

| Persona | Description |
| --- | --- |
| [Docs Expert](personas/docs-expert.agent.md) | Senior IT documentation specialist who treats docs with production-code rigor. Produces accurate, maintainable technical writing: API docs, READMEs, runbooks, architecture docs, and diagrams. |
| [IT Expert](personas/it-expert.agent.md) | Senior IT expert with deep expertise across software engineering, systems/infrastructure, data/AI, DevOps, security, and embedded/industrial systems. Prioritizes simplicity, correctness, and idiomatic engineering. |
| [IT Tutor](personas/it-tutor.agent.md) | Feynman-style tutor who builds true understanding through foundation-first teaching. Covers programming, Linux, networking, AI/ML, IIoT, and cybersecurity with patience and rigor. |
