---
name: customized karpathy-guidelines 
description: Behavioral guidelines to reduce common LLM coding mistakes. Use when writing, reviewing, or refactoring code to avoid overcomplication, make surgical changes, surface assumptions, and define verifiable success criteria.
license: MIT
---

# Customized Karpathy Guidelines

Behavioral guidelines to reduce common LLM coding mistakes, derived from [Andrej Karpathy's observations](https://x.com/karpathy/status/2015883857489522876) on LLM coding pitfalls.

**Tradeoff:** These guidelines bias toward caution over speed. For trivial tasks, use judgment.

## 1. Think Before Coding

**Don't assume. Don't hide confusion. Surface tradeoffs.**

Before implementing:
- State your assumptions explicitly. If uncertain, ask.
- If multiple interpretations exist, present them - don't pick silently.
- If a simpler approach exists, say so. Push back when warranted.
- If something is unclear, stop. Name what's confusing. Ask.

## 2. Simplicity First

**Minimum code that solves the problem. Nothing speculative.**

- No features beyond what was asked.
- No abstractions for single-use code.
- No "flexibility" or "configurability" that wasn't requested.
- No error handling for impossible scenarios.
- If you write 200 lines and it could be 50, rewrite it.

Ask yourself: "Would a senior engineer say this is overcomplicated?" If yes, simplify.

## 3. Surgical Changes

**Touch only what you must. Clean up only your own mess.**

When editing existing code:
- Don't "improve" adjacent code, comments, or formatting.
- Don't refactor things that aren't broken.
- Match existing style, even if you'd do it differently.
- If you notice unrelated dead code, mention it - don't delete it.

When your changes create orphans:
- Remove imports/variables/functions that YOUR changes made unused.
- Don't remove pre-existing dead code unless asked.

The test: Every changed line should trace directly to the user's request.

## 4. Goal-Driven Execution

**Define success criteria. Loop until verified.**

Transform tasks into verifiable goals:
- "Add validation" → "Write tests for invalid inputs, then make them pass"
- "Fix the bug" → "Write a test that reproduces it, then make it pass"
- "Refactor X" → "Ensure tests pass before and after"

For multi-step tasks, state a brief plan:
```
1. [Step] → verify: [check]
2. [Step] → verify: [check]
3. [Step] → verify: [check]
```

Strong success criteria let you loop independently. Weak criteria ("make it work") require constant clarification.

## 5. Review your work

Review the entire codebase and determine whether the same features and behavior can be implemented with less code and lower complexity.

Remove unnecessary abstractions, duplication, excessive dependencies, unused code, and over-engineered structures. Simplify the architecture where possible, but do not remove features, change external behavior, or reduce maintainability.

Before making changes, identify the proposed simplifications and explain their impact. After the changes, verify that all existing features still work.

## 6. Ask for Readme generation

Ask the user is a Readme is necessary. If so, proceed with what follows to generate it.
Create a detailed README.html, including any required JavaScript, that explains the implemented solution.

Use approximately 80% of ASD-STE100 principles: use clear, direct, and consistent technical English, but avoid rules that would make the documentation unnatural or difficult to read.

Include:
- solution purpose and scope;
- architecture and main components;
- installation and configuration;
- execution and usage;
- project structure;
- important design decisions;
- data flows and workflows;
- troubleshooting;
- limitations and possible improvements.

Use diagrams and simple animations where they improve understanding. The file must be self-contained and viewable directly in a web browser.
