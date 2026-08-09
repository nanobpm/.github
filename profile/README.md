<div align="center">

<sub>ADVANCED RESEARCH PROTOTYPE</sub>

# Nano BPM

### Agent Graph Orchestration for the Developer Workstation

**Graphs that run the loops.**

A **RAAD** — Rapid Agent Application Development — environment that runs on your machine.
Compose coding agents, tools, and human approvals into durable workflows.
**Code-first or Model-first**, provider-agnostic, and small enough to start on a Raspberry Pi.

[![Website](https://img.shields.io/badge/nanobpm.io-38bdf8?style=for-the-badge&logo=firefox&logoColor=052e1a)](https://nanobpm.io)
[![Demo](https://img.shields.io/badge/Browser_demo-34d399?style=for-the-badge&logo=webassembly&logoColor=052e1a)](https://nanobpm.io/demo/)
[![Docs](https://img.shields.io/badge/Docs-e4e4e7?style=for-the-badge&logo=readthedocs&logoColor=08080a)](https://nanobpm.io/docs/)
[![Architecture](https://img.shields.io/badge/Architecture-a1a1aa?style=for-the-badge&logo=buffer&logoColor=08080a)](https://nanobpm.io/architecture/)

</div>

---

## What is Nano?

Nano is a high-performance, **Camunda 8-compatible** process automation engine, wrapped in a
Rapid Agent Application Development environment. It carries the ideas pioneered by Zeebe and
Camunda 8 forward — durable, event-sourced orchestration — and makes them reachable from a
single self-contained binary that scales **both ways**: from a multi-node cluster down to a
Raspberry Pi.

On top of that engine, Nano lets you **compose coding agents, tools, and human approvals into
durable graphs** — the loops that plan, implement, review, and merge software — that survive
crashes, latency, and failure.

```bash
npm i -g @camunda8/cli
c8ctl load plugin c8ctl-plugin-nano
c8ctl nano start
```

---

## Code-first *or* Model-first Graphs

> One app — two authoring surfaces, the same engine.

Write the workflow as **code** with `@nanobpm/workflow`'s `defineFlow`, or draw it as **BPMN** in
the modeller — the same durable engine runs both. Nano derives the model, job types, correlation,
and workers from a single source of truth, so there's no copy-paste orchestration to drift. Switch
surfaces without re-platforming: the model and the code are two views of one runtime.

- **DRY your agent SDLC** — declare durable steps with `w.run` and durable waits with `w.signal`; Nano derives the rest.
- **Durable by default** — SIGKILL → cold restart → completed steps are never replayed. Delivery is at-least-once; make activities idempotent and they run effectively once.
- **Provider-agnostic** — frontier or local LLMs, and any coding-agent CLI harness (e.g. the GitHub Copilot CLI) as an external worker you "hire".
- **Self-optimizing** — backpressure, memory spill, and cluster placement tune themselves from live metrics. One business decision, not a hundred knobs.

---

## Explore the org

| Repository | What it is |
|---|---|
| **[nano-workforce](https://github.com/nanobpm/nano-workforce)** | **Agent Graph Orchestration for the Agentic SDLC.** Hand it an issue: it plans the work, fans a graph of coding agents out to implement it, drives every PR to **review convergence** against an automated reviewer, and merges it — escalating to a human only when stuck. A Nano Urban app built from durable BPMN processes. |
| **[nano-ide](https://github.com/nanobpm/nano-ide)** | The **Nano RAD console IDE** monorepo — language/app/example **extension packs** plus the **Urban** code-first stack: `@nanobpm/urban` (runtime + derivation toolkit + CLI), `@nanobpm/workflow` (`defineFlow`), and the `create-urban-app` scaffolder. |
| **[bojtos](https://github.com/nanobpm/bojtos)** | The **in-browser BPMN demo framework**. Runs the real Nano engine compiled to WebAssembly entirely in the browser — deploy a process, start instances, complete/fail jobs, advance the clock, and render a live token/incident diagram, with **no backend**. `bojtos-kit` + `bojtos-react`. |
| **The Nano engine** | A **Rust research engine** exploring high-performance BPMN execution behind a Camunda 8-compatible v2 REST API — deterministic event-sourced core, crash-durable journal, SQLite read model, optional Raft replication, and a built-in web console in one binary with no runtime dependencies. Ships to the browser as **[`@nanobpm/engine-wasm`](https://www.npmjs.com/package/@nanobpm/engine-wasm)**; run it via **[nanobpm.io](https://nanobpm.io)**. |

---

## Why Nano exists

Many teams want the Camunda 8 model but are blocked from it — by operational complexity, resource
footprint, cost, or migration friction. Nano exists to remove those blockers:

1. **Unblock migration to Camunda 8** — name and systematically remove the barriers to the modern process-orchestration model.
2. **Be a drop-in replacement** — existing BPMN models, client SDKs, and job workers keep working. Switching should feel like an upgrade, not a rewrite.
3. **Overmatch on the features that decide real evaluations** — clear the bar, then raise it.
4. **Enter new markets through scale — up *and* down** — from large clusters to the edge and the developer workstation.

<div align="center">
<sub>Built with reverence for the ideas pioneered by Zeebe and Camunda 8 — and the confidence that the next order of magnitude of scale, simplicity, and delight is still ahead.</sub>

<br><br>

**[nanobpm.io](https://nanobpm.io)** · [Demo](https://nanobpm.io/demo/) · [Docs](https://nanobpm.io/docs/) · [Schemas](https://nanobpm.io/schemas/)

</div>
