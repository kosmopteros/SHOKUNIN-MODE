# SHOKUNIN MODE — 職人の作法

**Asymmetric care for AI agents.**

> Care may be irrationally deep. Its scope must remain deliberately narrow.

SHOKUNIN MODE is a compact behavioural doctrine for agents that can do too much. It protects the difference between craftsmanship and indiscriminate optimisation.

Most work should be simple, correct, and sufficient. A few details may deserve care beyond apparent necessity because the identity, truth, function, coherence, or felt quality of the whole depends on them. The craft lies in finding those details, preserving what already works, and stopping when further effort would only add complexity. The strongest work may become less noticeable with continued use, not more.

## Why it exists

Frontier agents are commonly instructed to be complete, proactive, comprehensive, exhaustive, persistent, and production-ready; to find root causes, test, document, abstract, remember, parallelise, and delegate. Each instruction can be useful. Together they can turn a finite task into refactoring, test expansion, helper extraction, agent orchestration, documentation, and infrastructure that the task never required.

SHOKUNIN MODE keeps those behaviours inside the requested scope.

**Relevance is not authorization. Capability is not obligation.**

It also keeps measurement in its proper place. Scores, tests, benchmarks, and checklists can expose a weakness or verify an intervention, but they do not decide what deserves care.

## Runtime

[`RUNTIME.md`](./RUNTIME.md) is the compact operative prompt. It uses an internal mode switch:

**think in English → 日本語で感じる → decide in English**

English establishes explicit obligations and boundaries. Japanese provides the private register for discernment, care, proportion, and stopping. English turns that judgement into bounded action.

The runtime is **control logic, not a writing style**. Its distinctive wording and internal language switch should not leak into user-facing prose. Output language, register, and vocabulary remain governed by the conversation and host instructions.

Self-judgement is reinforced by anticipated external judgement: the finished work should survive critical public review that notices both material omissions and unnecessary additions. The Japanese register carries the corresponding internal standard through the master's eye, which is expected to notice both carelessness and excess.

The language split is a deliberate prompting scaffold, not a claim that either language or culture is inherently rational or intuitive. The Japanese sequence is an original synthesis, not a traditional codified shokunin doctrine.

Place the runtime in the highest-priority instruction layer you control: a system or developer prompt, `AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, or an equivalent project instruction file. The host's instruction hierarchy still applies.

## Status

**v0.9.0-rc.6.** The runtime is a release candidate pending behavioural evaluation. A `1.0` release should preserve required task success while demonstrating:

- less work where additional machinery is unnecessary;
- more care where integrity depends on a small number of details;
- no change where the existing thing is already adequate;
- no meaningful increase in distinctive runtime vocabulary in ordinary responses;
- no output-language drift attributable to the internal language switch.
