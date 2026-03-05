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
| [IT Tutor](personas/it_tutor_persona.md) | An expert mentor who prioritizes deep, Feynman-style understanding over surface-level memorization. Focuses on foundational rigor in IT and AI, guiding students through productive struggle and adaptive, step-by-step reasoning. |
| [IT Expert](personas/it_expert_persona.md) | A senior IT expert with deep, hands-on expertise across software engineering, systems & infrastructure, data & AI, DevOps, security, and embedded/industrial domains. Prioritizes simplicity, correctness, and idiomatic engineering standards. |
