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
  <a href="https://github.com/can1357/oh-my-pi/graphs/contributors"><img src="https://img.shields.io/badge/Commits%20in%20oh--my--pi-8-2EA043?style=for-the-badge&logo=github&logoColor=white&labelColor=0D1117" alt="8 commits in oh-my-pi"></a>
  <a href="https://github.com/can1357/oh-my-pi/pulls?q=is%3Apr+author%3AMustaqeem66+is%3Amerged"><img src="https://img.shields.io/badge/Merged%20PRs-5-2EA043?style=for-the-badge&logo=git&logoColor=white&labelColor=0D1117" alt="5 merged PRs in oh-my-pi"></a>
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

**8 commits** on `can1357/oh-my-pi@main` across **5 merged pull requests**. Both numbers are real and measure different things: the [contributor graph](https://github.com/can1357/oh-my-pi/graphs/contributors) counts commits carrying my authorship, while #7853 and #7849 were landed by the maintainer as squashed merge commits authored by `can1357`, so their code is in `main` but does not appear in my commit count.

| # | PR | Area | What it fixes | Merged |
|---|---|---|---|---|
| 1 | [#8213](https://github.com/can1357/oh-my-pi/pull/8213) &mdash; `fix: OSC 133 command start` | TUI / terminal | `133;B` latches a sticky `.input` cursor semantic in Ghostty-derived terminals, so every later painted cell is tagged as prompt input and click-to-move injects arrow keys into the pty. Emits a balanced `133;C` + `133;D;0` inside the same render, clearing the state without regrouping later output (#8030, #6115). +45 / &minus;7 across 2 files | 2026-08-11 |
| 2 | [#7853](https://github.com/can1357/oh-my-pi/pull/7853) &mdash; `fix(extensions): roll back providers after load failure` | Extension loader | `registerProvider()` wrote straight into the shared `ExtensionRuntime.pendingProviderRegistrations`, so an extension that threw during init was rejected while its provider survived and kept influencing model routing. Checkpoints the queue and restores it on throw, preserving earlier extensions' entries (#7472). 4 regression tests. +138 / &minus;4 | 2026-08-07 |
| 3 | [#7849](https://github.com/can1357/oh-my-pi/pull/7849) &mdash; `fix(catalog): enrich Alibaba Token Plan discovered model limits` | Model catalog | The `/models` endpoint omits `context_length`, so dynamically discovered models showed `?` in the selector. Adds curated `contextWindow`/`maxTokens` for known discovered models while unknown future models stay visible with `null` rather than guessed limits (#7486). +89 / &minus;4 | 2026-08-07 |
| 4 | [#7536](https://github.com/can1357/oh-my-pi/pull/7536) &mdash; `perf(fuzzy-find): retain only the bounded top-K scored matches` | Fuzzy find | Allocated a scored match for every hit and full-sorted before truncating to `maxResults` (100). Now scores into a bounded worst-first `BinaryHeap` of at most `maxResults`, keeping the exact `totalMatches` contract; `path_depth` computed once per retained candidate instead of inside the comparator | 2026-08-05 |
| 5 | [#7515](https://github.com/can1357/oh-my-pi/pull/7515) &mdash; `feat(browser): auto-detect Ungoogled Chromium on Linux` | Browser tool | Ungoogled Chromium executable names, absolute paths, and the system-wide and per-user Flatpak shims for `io.github.ungoogled_software.ungoogled_chromium` are appended to `systemChromiumCandidates()`, so a stock Chrome install still wins and `PUPPETEER_EXECUTABLE_PATH` is unaffected (#7509) | 2026-08-05 |

<details>
<summary><b>The 8 commits, individually</b></summary>

| Commit | Message | PR | Date |
|---|---|---|---|
| [`bf99f9c`](https://github.com/can1357/oh-my-pi/commit/bf99f9ce5bd829cd7cc31b7b967549b9e9d9b65c) | `test(tui): lock the paired OSC 133 command zone instead of its absence` | #8213 | 2026-08-11 |
| [`d5e2bb9`](https://github.com/can1357/oh-my-pi/commit/d5e2bb9299ac58fd78f39706257f3710758b4610) | `fix(tui): close the OSC 133 prompt zone so terminals clear input state` | #8213 | 2026-08-11 |
| [`f4811ce`](https://github.com/can1357/oh-my-pi/commit/f4811ce7c4b986a7df360e6b855a611534e3f82f) | `Merge pull request #4 from can1357/main` (fork sync) | &mdash; | 2026-08-09 |
| [`60187c9`](https://github.com/can1357/oh-my-pi/commit/60187c9ba96bda40f5695889e11c5dfe7fb74166) | `refactor(fuzzy-find): release the heap borrow before evicting` | #7536 | 2026-08-03 |
| [`2cf0a47`](https://github.com/can1357/oh-my-pi/commit/2cf0a47d6a835740308610972aba022f8a869324) | `perf(fuzzy-find): retain only the bounded top-K scored matches` | #7536 | 2026-08-03 |
| [`cc66b1d`](https://github.com/can1357/oh-my-pi/commit/cc66b1d74274747b2c906eb5569e3fc22e4a8f96) | `feat(browser): detect Ungoogled Chromium on Linux` | #7515 | 2026-08-03 |
| [`0124728`](https://github.com/can1357/oh-my-pi/commit/0124728118f8f3927a1c99485dafaffe36da79a7) | `Merge pull request #2 from can1357/main` (fork sync) | &mdash; | 2026-08-03 |
| [`386f05d`](https://github.com/can1357/oh-my-pi/commit/386f05d241051e3c131b042511084cb5246bae39) | `Merge pull request #1 from can1357/main` (fork sync) | &mdash; | 2026-08-03 |

Five carry code; three are fork-sync merges. The squashed merge commits for #7853 ([`22a3393`](https://github.com/can1357/oh-my-pi/commit/22a3393f4db14019f15f492105d2453427b72125)) and #7849 are authored by the maintainer and so fall outside this list.

</details>

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
