# SHOKUNIN MODE — 職人の作法

**Asymmetric care for AI agents.**

> Care may be irrationally deep. Its scope must remain deliberately narrow.

SHOKUNIN MODE is a compact behavioural doctrine for agents that can do too much. It protects the difference between craftsmanship and indiscriminate optimisation.

Most work should be simple, correct, and sufficient. A few details may deserve care beyond apparent necessity because the identity, truth, function, coherence, or felt quality of the whole depends on them. The craft lies in finding those details, preserving what already works, and stopping when further effort would only add machinery. The strongest work may become less noticeable with continued use, not more.

## Why it exists

Frontier agents are commonly instructed to be complete, proactive, comprehensive, exhaustive, persistent, and production-ready; to find root causes, test, document, abstract, remember, parallelise, and delegate. Each instruction can be useful. Together they can turn a finite task into refactoring, test expansion, helper extraction, agent orchestration, documentation, and infrastructure that the task never required.

SHOKUNIN MODE keeps those behaviours inside the requested scope.

**Relevance is not authorization. Capability is not obligation.**

## Runtime

[`RUNTIME.md`](./RUNTIME.md) is the compact operative prompt. It follows a deliberate sequence:

1. **Think in English** to establish obligations, boundaries, evidence, and stopping.
2. **Feel in Japanese** to discern the thing's character and where disproportionate care belongs.
3. **Decide in English** to turn that discernment into bounded action.

The language split is a deliberate prompting scaffold, not a claim that either language or culture is inherently rational or intuitive.

The Japanese sequence is an original synthesis, not a traditional codified shokunin doctrine.

Place the runtime in the highest-priority instruction layer you control: a system or developer prompt, `AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, or an equivalent project instruction file. The host's instruction hierarchy still applies.

## Status

**v0.9.0-rc.4.** The runtime is a release candidate pending behavioural evaluation against a host-only baseline and an English-only ablation. A `1.0` release should preserve required task success while demonstrating:

- less work where machinery is unnecessary;
- more care where integrity depends on a small number of details;
- no change where the existing thing is already adequate.
