# Hello, world 👋

## The Open Mind ecosystem

Three open-source projects that form one pipeline: **generate trusted context → expose it to agents → verify agent behavior.**

```
Source Code Repository
        │
        ▼
   Open Mind ────────────────  verification-first analysis (Python, standalone)
        │
        ▼
 .openmind artifacts ────────  versioned contract (manifest.json + schema 1.0.0, every entry carries file:line evidence)
        │
        ▼
 open-mind-mcp-server ───────  MCP integration layer (TypeScript, standalone)
        │
        ▼
 Claude / Cursor / AI agents   structured JSON tools: cited answers, honest refusals
        │
        ▼
 agent-skill-verification-template evals · citation validators · replay artifacts · release gate
        │
        ▼
 agent-skill-forge ───────────  spec-driven skill generation / packaging pipeline
```

Each project runs standalone; they integrate only through narrow, versioned contracts. No monorepo, no hidden coupling.

### 🧠 [open-mind](https://github.com/HelloThisWorld/open-mind)

**The verification-first codebase context layer.** Turns any local repository into deterministic, source-traceable knowledge that agents can query — without trusting a model's memory.

### 🔌 [open-mind-mcp-server](https://github.com/HelloThisWorld/open-mind-mcp-server)

**The agent tool integration layer.** Loads Open Mind's artifacts and exposes them to any MCP-compatible client (Claude Code, Claude Desktop, Cursor) as five structured tools.


### ✅ [agent-skill-verification-template](https://github.com/HelloThisWorld/agent-skill-verification-template)

**The quality gate for agent skills.** Treats agent skills as production components: a model-independent contract, an offline eval harness, and observability for every run.

---

## What I care about

- **Evidence over fluency** — important answers point back to real `file:line` sources or say "not found".
- **Determinism before generation** — the same input produces the same output; models refine, they don't decide.
- **Contracts over coupling** — projects integrate through versioned schemas, so each side can evolve and be tested alone.
- **Measured, not asserted** — reliability claims come with eval numbers, seeded-fault proofs, and replayable artifacts.

*All three projects are MIT-licensed. Issues and PRs welcome.*
