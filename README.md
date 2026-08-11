<h1 align="center">Muhammad Mustaqeem</h1>

<p align="center">
  <b>Full-stack engineer &middot; AI coding-agent internals</b><br>
  I work on the parts of developer tools that fail quietly &mdash; sandbox policy, tool harnesses, streaming edits, and agent orchestration.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Merged%20upstream-4%20PRs-2EA043?style=for-the-badge&logo=github&logoColor=white&labelColor=0D1117" alt="4 merged PRs">
  <img src="https://img.shields.io/badge/Public%20PRs-24-1F6FEB?style=for-the-badge&logo=git&logoColor=white&labelColor=0D1117" alt="24 public PRs">
  <img src="https://img.shields.io/badge/Projects%20contributed-186k%20stars-8957E5?style=for-the-badge&logo=starship&logoColor=white&labelColor=0D1117" alt="186k combined stars">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white" alt="PHP">
  <img src="https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white" alt="Laravel">
  <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white" alt="Vue">
  <img src="https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Bun-000000?style=flat-square&logo=bun&logoColor=white" alt="Bun">
</p>

---

## Merged upstream

Code shipped into production open-source projects.

| Project | Stars | Contribution |
|---|---|---|
| [**oh-my-pi**](https://github.com/can1357/oh-my-pi) | 23.7k | [#7853](https://github.com/can1357/oh-my-pi/pull/7853) &mdash; roll back extension providers after a load failure, so a partially-registered extension cannot leave the registry inconsistent |
| [**oh-my-pi**](https://github.com/can1357/oh-my-pi) | 23.7k | [#7536](https://github.com/can1357/oh-my-pi/pull/7536) &mdash; bound fuzzy-find to the top-K scored matches instead of retaining the full candidate set |
| [**oh-my-pi**](https://github.com/can1357/oh-my-pi) | 23.7k | [#7515](https://github.com/can1357/oh-my-pi/pull/7515) &mdash; auto-detect Ungoogled Chromium on Linux in the browser tool |
| [**oh-my-pi**](https://github.com/can1357/oh-my-pi) | 23.7k | [#7849](https://github.com/can1357/oh-my-pi/pull/7849) &mdash; enrich discovered model limits for Alibaba Token Plan in the catalog |

Open work in review across [openhuman](https://github.com/tinyhumansai/openhuman) (36k&#9733;), [graphify](https://github.com/Graphify-Labs/graphify) (105k&#9733;), [prime-agent](https://github.com/PrimeIntellect-ai/prime-agent) (13k&#9733;) and [forgecode](https://github.com/tailcallhq/forgecode) (7k&#9733;).

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

Ongoing upstream work on `oh-my-pi`, `openhuman`, `graphify` and `prime-agent` &mdash; mostly correctness fixes in extension loading, memory and embedding resolution, parser edge cases, and concurrency.

---

## Currently

- Auditing agent security boundaries: sandbox escape paths, path traversal in workspace policy, and fail-open guards in permission checks
- Building retrieval-grounding verification that catches unsupported claims before they are returned
- Contributing fixes upstream to open-source coding agents

---

<p align="center">
  <sub>Open to collaboration on developer tooling and AI agent infrastructure.</sub>
</p>
