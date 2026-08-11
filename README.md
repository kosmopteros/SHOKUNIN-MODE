# SHOKUNIN MODE — 職人の作法

**A portable craft discipline for AI agents.**

> Care may be irrationally deep. Its scope must remain deliberately narrow.

AI agents are increasingly capable of doing far more than a task requires. A local fix can become a refactor. A review can become a new framework. Diligence can become extra tests, documentation, orchestration, and infrastructure. The work grows while the result does not necessarily improve.

SHOKUNIN MODE is an installable Agent Skill and standalone runtime for controlling that tendency without reducing craftsmanship to minimal effort. It keeps the requested outcome and scope fixed, gives most parts the simplest adequate treatment, and concentrates unusual care on the very few details that determine the integrity of the whole. It also asks what should remain untouched and makes stopping an explicit judgment.

Use it alongside domain-specific skills for substantive work — creating, changing, reviewing, diagnosing, designing, planning, researching, or evaluating — whenever judgment is needed about what matters, what to preserve, how much validation is enough, or when to stop.

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

The language split is a deliberate prompting scaffold, not a claim that either language or culture is inherently rational or intuitive. The Japanese sequence is an original synthesis, not a traditional codified shokunin doctrine.

## Origin

SHOKUNIN MODE is the public, portable expression of the methodology [Alexander Pichugin](https://pichugin.me/) works from across his projects.

The common thread is craft quality and care for the result, regardless of medium — whether the thing is software, a simulation system, a product, a piece of writing, or something made by hand. Most work should remain simple and sufficient; a few details deserve disproportionate attention because they decide whether the whole actually works, holds together, and feels right in use.

This repository translates that working discipline into instructions AI agents can use.

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

SHOKUNIN MODE is released under the [MIT License](./LICENSE). It may be used, copied, modified, distributed, sublicensed, and sold, provided the copyright and license notice are retained.

MIT was chosen because SHOKUNIN MODE is distributed as an installable agent skill as well as a written doctrine. The license keeps it straightforward to embed and adapt across open-source and commercial agent environments.

## Status

**v0.9.0-rc.8.** The runtime and skill are release candidates pending behavioural evaluation. A `1.0` release should preserve required task success while demonstrating:

- less work where additional machinery is unnecessary;
- more care where integrity depends on a small number of details;
- no change where the existing thing is already adequate;
- reliable activation for substantive work and non-activation for trivial answers;
- correct composition with domain-specific skills and explicit requirements;
- no meaningful increase in distinctive runtime vocabulary in ordinary responses;
- no output-language drift attributable to the internal language switch.
