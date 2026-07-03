# Hello, world 👋

**Senior Software Engineer — AI agent infrastructure, verification-first systems, context engineering, MCP tool integration, and production-grade software reliability.**

I build the layer between AI agents and real codebases: systems that give agents **verifiable context** instead of confident guesses, and harnesses that **measure** whether agent skills actually work before they ship.

> A fluent but unsupported answer about a production system is not intelligence — it is a production risk.
> My work treats evidence, determinism, and honest refusal as engineering requirements, not aspirations.

---

## The Open Mind ecosystem

Three open-source projects that form one pipeline: **generate trusted context → expose it to agents → verify agent behavior.**

```
Source Code Repository
        │
        ▼
   Open Mind ────────────────  verification-first analysis (Python, standalone)
        │
        ▼
 .openmind artifacts ────────  versioned contract (manifest.json + schema 1.0.0,
        │                      every entry carries file:line evidence)
        ▼
 open-mind-mcp-server ───────  MCP integration layer (TypeScript, standalone)
        │
        ▼
 Claude / Cursor / AI agents   structured JSON tools: cited answers, honest refusals
        │
        ▼
 agent-skill-verification-template
                               evals · citation validators · replay artifacts · release gate
```

Each project runs standalone; they integrate only through narrow, versioned contracts. No monorepo, no hidden coupling.

### 🧠 [open-mind](https://github.com/HelloThisWorld/open-mind)

**The verification-first codebase context layer.** Turns any local repository into deterministic, source-traceable knowledge that agents can query — without trusting a model's memory.

- **Verbatim glossary** — terms and acronyms extracted by boundary-checked pattern matching, never rewritten by a model; every definition carries `source_file`, `line_number`, and a content hash. Absent terms return an honest "not found", never a guess.
- **Source-derived structure** — module trees, definition indexes, import/dependency and call graphs from deterministic static analysis across 13 languages; ambiguous call edges are *flagged*, not invented.
- **Portable artifact export** — a versioned `.openmind` directory (schema 1.0.0) as the stable integration contract, verified by a 29-check acceptance suite including **byte-identical determinism** across runs.
- **Local-first** — audited egress, exact-token search, grounded Q&A with a local LLM; the deterministic layers need no model at all.

`Python` · `FastAPI` · `deterministic static analysis` · `local-first`

### 🔌 [open-mind-mcp-server](https://github.com/HelloThisWorld/open-mind-mcp-server)

**The agent tool integration layer.** Loads Open Mind's artifacts and exposes them to any MCP-compatible client (Claude Code, Claude Desktop, Cursor) as five structured tools.

- Every factual answer cites `{file, line, snippet}` evidence; explanations are served **verbatim from artifacts, never generated**.
- **Refusal is a feature** — unknown symbols and unbackable claims return `insufficient_evidence` or `unsupported`, with the missing terms named so the agent knows *what* it couldn't verify.
- Deterministic claim validation with three honest verdicts; schema-version gating; per-call structured telemetry.
- Fully offline demo and CI — 44 tests including an in-memory MCP protocol round-trip and an output-determinism check. No API keys, no network.

`TypeScript` · `MCP SDK` · `zod` · `vitest`

### ✅ [agent-skill-verification-template](https://github.com/HelloThisWorld/agent-skill-verification-template)

**The quality gate for agent skills.** Treats agent skills as production components: a model-independent contract, an offline eval harness, and observability for every run.

- Four validators per run: **schema**, **citation** (independently re-reads every cited `file:line` and fails fabricated citations), **unsupported-claim honesty**, and **tool-call order**.
- Drove Open Mind's skills to **250/250 green runs** (10 runs per case, 90% gate) — and proved the gate *works* with a flaky-twin methodology: seeded faults (dropped citations, shifted line numbers, invented claims) push pass rates to 33–59% and fail the gate exactly as designed.
- Every failed run leaves a replay artifact with the exact input, output, tool trace, and verdict; reports ship as HTML, JSON summaries, Prometheus metrics, and structured JSONL events.

`TypeScript` · `eval harness` · `observability` · `release gates`

---

## What I care about

- **Evidence over fluency** — important answers point back to real `file:line` sources or say "not found".
- **Determinism before generation** — the same input produces the same output; models refine, they don't decide.
- **Contracts over coupling** — projects integrate through versioned schemas, so each side can evolve and be tested alone.
- **Measured, not asserted** — reliability claims come with eval numbers, seeded-fault proofs, and replayable artifacts.

## Stack

`Python` · `TypeScript` · `Node.js` · `FastAPI` · `MCP (Model Context Protocol)` · `LLM tooling & evals` · `static analysis` · `CI/CD & release gates`


*All three projects are MIT-licensed. Issues and PRs welcome.*
