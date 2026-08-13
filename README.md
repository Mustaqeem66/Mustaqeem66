<h1 align="center">Muhammad Mustaqeem</h1>

<p align="center">
  <b>Full-stack engineer &middot; AI coding-agent internals</b><br>
  I work on the parts of developer tools that fail quietly &mdash; sandbox policy, tool harnesses, streaming edits, and agent orchestration.
</p>

<p align="center">
  <a href="mailto:ageisnode@gmail.com"><img src="https://img.shields.io/badge/Email%20me-ageisnode@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117" alt="Email ageisnode@gmail.com"></a>
  <a href="https://github.com/Mustaqeem66"><img src="https://img.shields.io/badge/GitHub-Mustaqeem66-181717?style=for-the-badge&logo=github&logoColor=white&labelColor=0D1117" alt="GitHub profile"></a>
</p>

<p align="center">
  <a href="https://github.com/can1357/oh-my-pi/pulls?q=is%3Apr+author%3AMustaqeem66+is%3Amerged"><img src="https://img.shields.io/badge/Merged%20into%20oh--my--pi-5%20PRs-2EA043?style=for-the-badge&logo=github&logoColor=white&labelColor=0D1117" alt="5 merged PRs in oh-my-pi"></a>
  <a href="https://github.com/can1357/oh-my-pi/pulls?q=is%3Apr+author%3AMustaqeem66+is%3Aopen"><img src="https://img.shields.io/badge/Open%20in%20review-4%20PRs-D29922?style=for-the-badge&logo=git&logoColor=white&labelColor=0D1117" alt="4 open PRs in oh-my-pi"></a>
  <a href="https://github.com/search?q=is%3Apr+author%3AMustaqeem66&type=pullrequests"><img src="https://img.shields.io/badge/Public%20PRs-24-1F6FEB?style=for-the-badge&logo=git&logoColor=white&labelColor=0D1117" alt="24 public PRs"></a>
  <a href="https://github.com/Mustaqeem66?tab=repositories"><img src="https://img.shields.io/badge/Projects%20contributed-186k%20stars-8957E5?style=for-the-badge&logo=starship&logoColor=white&labelColor=0D1117" alt="186k combined stars"></a>
</p>

<p align="center">
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"></a>
  <a href="https://www.rust-lang.org/"><img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust"></a>
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"></a>
  <a href="https://www.php.net/"><img src="https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white" alt="PHP"></a>
  <a href="https://laravel.com/"><img src="https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white" alt="Laravel"></a>
  <a href="https://vuejs.org/"><img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white" alt="Vue"></a>
  <a href="https://nodejs.org/"><img src="https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js"></a>
  <a href="https://bun.sh/"><img src="https://img.shields.io/badge/Bun-000000?style=flat-square&logo=bun&logoColor=white" alt="Bun"></a>
</p>

---

## Merged upstream &mdash; [oh-my-pi](https://github.com/can1357/oh-my-pi) (23.7k&#9733;)

Code shipped into production open source. All five PRs below are merged into `can1357/oh-my-pi@main`.

| # | PR | Area | What it fixes | Merged |
|---|---|---|---|---|
| 1 | [#8213](https://github.com/can1357/oh-my-pi/pull/8213) &mdash; `fix: OSC 133 command start` | TUI / terminal | `133;B` latches a sticky `.input` cursor semantic in Ghostty-derived terminals, so every later painted cell is tagged as prompt input and click-to-move injects arrow keys into the pty. Emits a balanced `133;C` + `133;D;0` inside the same render, clearing the state without regrouping later output (#8030, #6115). +45 / &minus;7 across 2 files | 2026-08-11 |
| 2 | [#7853](https://github.com/can1357/oh-my-pi/pull/7853) &mdash; `fix(extensions): roll back providers after load failure` | Extension loader | A partially registered extension could leave the provider registry inconsistent; providers are now rolled back on load failure | 2026-08-07 |
| 3 | [#7849](https://github.com/can1357/oh-my-pi/pull/7849) &mdash; `fix(catalog): enrich Alibaba Token Plan discovered model limits` | Model catalog | Discovered model limits for the Alibaba Token Plan were incomplete in the catalog | 2026-08-07 |
| 4 | [#7536](https://github.com/can1357/oh-my-pi/pull/7536) &mdash; `perf(fuzzy-find): retain only the bounded top-K scored matches` | Fuzzy find | Bounded fuzzy-find to the top-K scored matches instead of retaining the full candidate set | 2026-08-05 |
| 5 | [#7515](https://github.com/can1357/oh-my-pi/pull/7515) &mdash; `feat(browser): auto-detect Ungoogled Chromium on Linux` | Browser tool | Ungoogled Chromium installs on Linux were not discovered by the browser tool | 2026-08-05 |

### Open in review &mdash; same repo

| PR | What it does | Size |
|---|---|---|
| [#8215](https://github.com/can1357/oh-my-pi/pull/8215) &mdash; `fix: missing-usage resume crash` | Resume path crashes when usage data is absent (#8142) | +108 / &minus;23, 8 files |
| [#7899](https://github.com/can1357/oh-my-pi/pull/7899) &mdash; `fix(task): dedupe parallel fallback selector resolution` | Parallel Task siblings stampede unknown fallback selectors; adds an in-flight coordinator that dedupes concurrent resolution, clears settled entries so retries still work, and keeps caller abort isolated (#7484). 6 unit tests | +224 / &minus;13, 5 files |
| [#7855](https://github.com/can1357/oh-my-pi/pull/7855) &mdash; `fix(shell): deterministic native session close` | `Shell` had no explicit `close()`, so callers relied on GC to release pty and child-process handles. Adds an idempotent async close that aborts active execution and drops the session core (#7491) | +98, 4 files |
| [#7512](https://github.com/can1357/oh-my-pi/pull/7512) &mdash; `fix(bash-interceptor): don't block grep as a pipeline stdin filter` | `printf 'x' \| grep x` was blocked with "use the grep tool", but the grep tool searches disk and cannot read pipeline stdout. Narrow exemption for grep-family stages that consume pipeline stdin and take no path operand (#7496). 19 new assertions | +193 / &minus;16, 3 files |

Also working across [openhuman](https://github.com/tinyhumansai/openhuman) (36k&#9733;), [graphify](https://github.com/Graphify-Labs/graphify) (105k&#9733;), [prime-agent](https://github.com/PrimeIntellect-ai/prime-agent) (13k&#9733;) and [forgecode](https://github.com/tailcallhq/forgecode) (7k&#9733;).

---

## What I actually work on

**Agent safety and sandboxing.** Most agent bugs are not crashes &mdash; they are guards that fail *open*. A permission check that returns `0` on an unreadable file reads as "clean." A `Math.max(0, NaN)` passes every threshold. I audit for the failure mode where a system reports success while doing nothing.

**Tool harness correctness.** Command interception that blocks `grep` when it is a legitimate pipeline stage. Shell sessions that never deterministically close. Fallback selectors resolved twice in parallel. These are the defects that make an agent feel unreliable without ever producing an error.

**Retrieval and grounding.** Claim extraction, evidence verification, and the reranking logic that decides whether a generated answer is actually supported by its sources.

---

## Selected work

### OrkaNode

An autonomous CLI development environment built on a dual-model split &mdash; a reasoning model that plans and a fast model that executes &mdash; with an organ-based internal architecture and a gated policy layer between the agent and the host machine.

Focus areas: workspace path confinement, single-use consent tokens for privileged operations, command allowlisting, and a response-path gate that verifies generated claims against retrieved evidence before they reach the user.

*Currently private. Happy to walk through the architecture.*

### Contributions to agent tooling

Ongoing upstream work on `oh-my-pi`, `openhuman`, `graphify` and `prime-agent` &mdash; mostly correctness fixes in extension loading, terminal shell integration, memory and embedding resolution, parser edge cases, and concurrency.

---

## Currently

- Auditing agent security boundaries: sandbox escape paths, path traversal in workspace policy, and fail-open guards in permission checks
- Building retrieval-grounding verification that catches unsupported claims before they are returned
- Contributing fixes upstream to open-source coding agents

---

## Contact

<p align="center">
  <a href="mailto:ageisnode@gmail.com"><img src="https://img.shields.io/badge/Get%20in%20touch-ageisnode@gmail.com-EA4335?style=for-the-badge&logo=maildotru&logoColor=white&labelColor=0D1117" alt="Email ageisnode@gmail.com"></a>
</p>

<p align="center">
  <sub>Open to collaboration on developer tooling and AI agent infrastructure.</sub>
</p>
