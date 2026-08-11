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

## Runtime and skill

[`RUNTIME.md`](./RUNTIME.md) is the standalone prompt for environments where you control a system, developer, or project instruction layer.

[`SKILL.md`](./SKILL.md) makes the same discipline an installable [Agent Skill](https://agentskills.io/specification). Its metadata is always discoverable; the full method is loaded only when the skill is activated. The skill contains the complete operative method, so an agent does not need to search the project or reconstruct SHOKUNIN MODE from surrounding context.

The skill is intentionally tool-free. It composes with domain skills rather than replacing them: domain skills define required procedures; SHOKUNIN MODE governs attention, scope, proportion, preservation, validation, and stopping.

Both forms use an internal mode switch:

**think in English → 日本語で感じる → decide in English**

English establishes explicit obligations and boundaries. Japanese provides the private register for discernment, care, proportion, and stopping. English turns that judgement into bounded action.

The runtime is **control logic, not a writing style**. Its vocabulary, metaphors, Japanese terms, and internal language switch should not leak into user-facing prose. Output language and tone remain governed by the conversation and host instructions.

The language split is a deliberate prompting scaffold, not a claim that either language or culture is inherently rational or intuitive. The Japanese sequence is an original synthesis, not a traditional codified shokunin doctrine.

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

## Status

**v0.9.0-rc.7.** The runtime and skill are release candidates pending behavioural evaluation. A `1.0` release should preserve required task success while demonstrating:

- less work where additional machinery is unnecessary;
- more care where integrity depends on a small number of details;
- no change where the existing thing is already adequate;
- reliable activation for substantive work and non-activation for trivial answers;
- correct composition with domain-specific skills and explicit requirements;
- no meaningful increase in distinctive runtime vocabulary in ordinary responses;
- no output-language drift attributable to the internal language switch.
