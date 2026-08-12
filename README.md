# SHOKUNIN MODE — 職人の作法

**A portable craft discipline for AI agents.**

> Care may be irrationally deep. Its scope must remain deliberately narrow.

SHOKUNIN MODE grew out of a working discipline [Alexander Pichugin](https://pichugin.me/) had already been applying across software, simulation systems, products, research, writing, design, and physical making.

Across those very different kinds of work, the same pattern kept appearing: most things need to be simply right. A few deserve care beyond apparent necessity because the quality, coherence, usefulness, or character of the whole depends on them. Craft lies in finding those few places, preserving what already works, and knowing when enough is enough.

This repository translates that practice into an installable Agent Skill and standalone runtime so AI agents can apply the same judgment. It keeps the requested outcome and scope fixed, gives most parts the simplest adequate treatment, concentrates unusual care where the result actually depends on it, and makes stopping an explicit decision.

That matters because capable agents can easily turn diligence into expansion: a local fix becomes a refactor, a review becomes a framework, and a finite task accumulates tests, documentation, orchestration, or infrastructure without a corresponding improvement in the result.

Use SHOKUNIN MODE alongside domain-specific skills for substantive work — creating, changing, reviewing, diagnosing, designing, planning, researching, or evaluating — whenever judgment is needed about what matters, what to preserve, how much validation is enough, or when to stop.

## Core premise

Most work should be simple, correct, and sufficient. A few details may deserve care beyond apparent necessity because the identity, truth, function, coherence, or felt quality of the whole depends on them. The craft lies in finding those details, preserving what already works, and stopping when further effort would only add complexity. The strongest work may become less noticeable with continued use, not more.

**Relevance is not authorization. Capability is not obligation.**

## What it counters

Frontier agents are commonly instructed to be complete, proactive, comprehensive, exhaustive, persistent, and production-ready; to find root causes, test, document, abstract, remember, parallelise, and delegate. Each instruction can be useful. Together they can turn a finite task into work the task never required.

SHOKUNIN MODE keeps those behaviours inside the requested scope. It also keeps measurement in its proper place: scores, tests, benchmarks, and checklists can expose a weakness or verify an intervention, but they do not decide what deserves care.

## Runtime and skill

[`RUNTIME.md`](./RUNTIME.md) is the standalone prompt for environments where you control a system, developer, or project instruction layer.

[`SKILL.md`](./SKILL.md) makes the same discipline an installable [Agent Skill](https://agentskills.io/specification). Its metadata is always discoverable; the full method is loaded only when the skill is activated. The skill contains the complete operative method, so an agent does not need to search the project or reconstruct SHOKUNIN MODE from surrounding context.

The skill is intentionally tool-free. It composes with domain skills rather than replacing them: domain skills define required procedures; SHOKUNIN MODE governs attention, scope, proportion, preservation, validation, and stopping.

Both forms use an internal mode switch:

**think in English → 日本語で感じる → decide in English**

English establishes explicit obligations and boundaries. Japanese provides the private register for discernment, care, proportion, and stopping. English turns that judgement into bounded action.

The runtime is **control logic, not a writing style**. Its vocabulary, metaphors, Japanese terms, and internal language switch should not leak into user-facing prose. Output language and tone remain governed by the conversation and host instructions.

The name draws on **職人 (shokunin)** — the craftsperson — while the language split and Japanese sequence are an original prompting synthesis, not a traditional codified shokunin doctrine. They are not a claim that either language or culture is inherently rational or intuitive.

## Install

### Codex

Codex discovers user skills from `$CODEX_HOME/skills`, or `~/.codex/skills` when `CODEX_HOME` is unset. Clone the repository into a directory named `shokunin-mode`.

macOS / Linux:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/kosmopteros/SHOKUNIN-MODE.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/shokunin-mode"
```

Windows PowerShell:

```powershell
$codexHome = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $HOME ".codex" }
$skillsHome = Join-Path $codexHome "skills"
New-Item -ItemType Directory -Force -Path $skillsHome | Out-Null
git clone https://github.com/kosmopteros/SHOKUNIN-MODE.git (Join-Path $skillsHome "shokunin-mode")
```

Start a new Codex session. Invoke it explicitly with `$shokunin-mode`, or allow Codex to activate it automatically for matching substantive work. Codex-specific UI metadata lives in [`agents/openai.yaml`](./agents/openai.yaml).

### Gemini CLI

```bash
gemini skills install https://github.com/kosmopteros/SHOKUNIN-MODE --scope user
```

Gemini can then activate the skill when its description matches the task, subject to its normal activation consent.

### Other Agent Skills hosts

Install or link the repository root as a skill directory named `shokunin-mode`. The skill requires no tools, scripts, network access, or platform-specific dependencies.

### Optional bootstrap

When a host needs a persistent nudge to use the installed skill, add only this to its project instruction file:

```md
For substantive work, use the `shokunin-mode` skill when available. Skip it for trivial direct answers.
```

This bootstrap handles activation. The skill handles the method. Do not paste the full runtime into permanent context when on-demand skills are available.

## License

© 2026 Alexander Pichugin.

Except where otherwise noted, SHOKUNIN MODE — including `RUNTIME.md`, `SKILL.md`, this documentation, and the accompanying Agent Skill metadata — is licensed under the [Creative Commons Attribution 4.0 International License](./LICENSE).

You may copy, redistribute, translate, adapt, and use the material for any purpose, including commercially, provided that you give appropriate credit, link to the license, and indicate whether changes were made.

Suggested attribution:

> [SHOKUNIN MODE](https://github.com/kosmopteros/SHOKUNIN-MODE) by [Alexander Pichugin](https://pichugin.me/), licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

For adaptations, add: “Adapted from the original; changes were made.”

CC BY 4.0 does not grant patent or trademark rights or imply endorsement. Versions published before this relicensing remain available under the MIT License that accompanied them. Any executable source code added in the future may use a separate software license, identified alongside that code.

## Status

**v0.9.0-rc.8.** The runtime and skill are release candidates pending behavioural evaluation. A `1.0` release should preserve required task success while demonstrating:

- less work where additional machinery is unnecessary;
- more care where integrity depends on a small number of details;
- no change where the existing thing is already adequate;
- reliable activation for substantive work and non-activation for trivial answers;
- correct composition with domain-specific skills and explicit requirements;
- no meaningful increase in distinctive runtime vocabulary in ordinary responses;
- no output-language drift attributable to the internal language switch.
