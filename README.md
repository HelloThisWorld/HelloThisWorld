# Hello, world 👋

## Spec-driven AI agent engineering

I build open-source tools for production-grade AI agent workflows:  
**generate trusted context → expose it as tools → verify agent behavior → package reliable skills.**

The focus is not prompt-and-pray demos.  
The focus is **source-grounded context, MCP tool integration, evals, replayable failures, and verification-gated agent skills.**

```text
Source Code Repository
        │
        ▼
   Open Mind ───────────────────── verification-first codebase analysis
        │                           Python · standalone
        ▼
 .openmind artifacts ───────────── versioned schema contract
        │                           manifest.json · file:line evidence
        ▼
 open-mind-mcp-server ──────────── MCP tool integration layer
        │                           TypeScript · standalone
        ▼
 Claude / Cursor / AI agents ──── structured tools, cited answers, honest refusals
        │
        ▼
 agent-skill-verification-template
        │                           evals · validators · replay artifacts · quality gates
        ▼
 agent-skill-forge ─────────────── spec-driven skill generation and packaging pipeline
```

Each project runs standalone. They integrate through narrow, versioned contracts — no monorepo, no hidden coupling.

---

## Projects

### 🧠 [Open Mind](https://github.com/HelloThisWorld/open-mind)

**Verification-first codebase context for AI agents.**

Open Mind turns local repositories into deterministic, source-traceable knowledge artifacts with `file:line` evidence.  
It is designed for agents that need to understand codebases without relying on model memory or unsupported summaries.

**Core ideas:** source grounding, deterministic extraction, codebase context engineering, honest refusal when evidence is missing.

---

### 🔌 [open-mind-mcp-server](https://github.com/HelloThisWorld/open-mind-mcp-server)

**MCP tools for source-grounded codebase understanding.**

This server loads `.openmind` artifacts and exposes them to MCP-compatible clients such as Claude Code, Claude Desktop, and Cursor.

It provides structured tools for:

- searching codebase context
- retrieving symbol evidence
- explaining architecture components
- validating claims against source references
- listing available artifacts

**Core ideas:** MCP integration, tool contracts, structured JSON outputs, agent-callable evidence.

---

### ✅ [agent-skill-verification-template](https://github.com/HelloThisWorld/agent-skill-verification-template)

**A quality gate for AI agent skills.**

This project treats agent skills as production components.  
It provides an offline eval harness, validators, replay artifacts, metrics, static reports, and release gates.

**Core ideas:** evals, golden cases, negative cases, citation validation, replayable failures, model-independent skill contracts.

---

### ⚒️ [agent-skill-forge](https://github.com/HelloThisWorld/agent-skill-forge)

**A spec-driven pipeline for generating, testing, repairing, and packaging AI agent skills.**

agent-skill-forge turns a structured skill requirement into a verified skill package:

```text
skill requirement
  → skill spec
  → generated skill files
  → eval cases
  → verification
  → repair loop
  → quality gate
  → installable package
```

**Core ideas:** agent skill generation, skill SDLC, verification-gated packaging, model-agnostic skill development.

---

## What I care about

- **Evidence over fluency**  
  Important answers should point back to real sources or clearly say that evidence is missing.

- **Specs before generation**  
  AI is an execution accelerator, not the source of truth. Requirements, contracts, tests, and quality gates come first.

- **Contracts over coupling**  
  Tools and agents should integrate through explicit schemas, not hidden assumptions.

- **Measured, not asserted**  
  Reliability should be demonstrated through evals, reports, replay artifacts, and failure analysis.

- **Production-minded AI**  
  Agent workflows need observability, permission boundaries, partial failure handling, and release gates.

---

## Keywords

`AI agents` · `MCP` · `Claude skills` · `agent skills` · `LLM evals` · `tool calling` · `context engineering` · `verification-first systems` · `source-grounded AI` · `production AI workflows`

---

MIT-licensed. Issues and PRs welcome.
