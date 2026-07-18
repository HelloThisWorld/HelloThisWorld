# Hello, world 👋

## Verification-first AI engineering & internal knowledge systems

I build open-source tools for AI agents that need **reliable context, explicit contracts, and measurable quality**.

The common theme across my projects is:

> **Turn engineering knowledge into source-grounded context → expose it through stable tool contracts → run governed workflows → verify the outcome.**

The goal is not another prompt wrapper or a fluent codebase chatbot. I am interested in the infrastructure required to make AI useful on real engineering systems: provenance, versioned artifacts, tool boundaries, evals, replayable failures, and evidence-backed automation.

```text
Local Source Repositories
          │
          ▼
      Open Mind ───────────────── verification-first code intelligence
          │                        deterministic extraction · file:line evidence
          ▼
   .openmind artifacts ────────── portable, versioned knowledge contract
          │
          ▼
 open-mind-mcp-server ─────────── structured MCP tools for AI agents
          │
          ├──────────────► Claude / Cursor / MCP-compatible agents
          │
          └──────────────► governed engineering workflows

Open Mind context ───────────────► SpecBridge
                                    portable specifications · verified execution

Agent Skill Verifier / Forge ───► evals · replay · repair loops · release gates
```

Each project runs independently and integrates through narrow, versioned contracts rather than hidden coupling.

---

## Featured projects

### 🧠 [Open Mind](https://github.com/HelloThisWorld/open-mind)

**A verification-first code intelligence and engineering knowledge layer for AI agents.**

Open Mind turns local repositories into deterministic, source-traceable artifacts that agents can query without relying on model memory or unsupported summaries.

Implemented capabilities include:

- a source-traceable knowledge index with portable `file:line` evidence;
- verbatim glossary extraction with honest `not found` behavior;
- module, dependency, definition, entry-point, and call/usage graphs;
- exact-token and hybrid retrieval;
- persisted solved cases with staleness detection;
- framework profiles, architectural roles, and source-derived facets;
- a versioned `.openmind` artifact contract;
- MCP, REST, CLI, and interactive inspection surfaces;
- constrained, test-gated code modification paths.

**Core principles:** evidence over fluency, deterministic extraction before generation, explicit uncertainty, local-first storage, and stable integration contracts.

#### Enterprise knowledge direction

Open Mind currently focuses on source repositories. Its architecture is intended to evolve toward a private, version-aware **internal engineering knowledge layer** that can connect code with specifications, design records, tests, operational knowledge, and historical decisions while preserving provenance and authority.

This direction is aimed at a common enterprise AI bottleneck: teams already possess large amounts of engineering knowledge, yet every AI session must repeatedly rediscover, copy, and reinterpret it. A governed internal knowledge layer can provide agents with smaller, more relevant, source-verifiable context and make AI adoption more efficient without treating model output as the source of truth.

---

### 🔌 [open-mind-mcp-server](https://github.com/HelloThisWorld/open-mind-mcp-server)

**The MCP integration boundary for Open Mind artifacts.**

The server loads a versioned `.openmind` directory and exposes structured tools for:

- searching repository context;
- retrieving symbol evidence;
- explaining architecture components;
- validating claims against source records;
- listing available knowledge artifacts.

Supported claims return evidence. Unsupported or unknown claims are rejected explicitly instead of being improvised. The server is implemented independently in TypeScript and does not import Open Mind internals.

**Core principles:** MCP tool contracts, structured JSON outputs, schema compatibility, deterministic behavior, and evidence-enforced refusal.

---

### 🌉 [SpecBridge](https://github.com/HelloThisWorld/specbridge)

**An open, model-agnostic runtime for existing Kiro specifications.**

SpecBridge keeps `.kiro/steering` and `.kiro/specs` as the source of truth while making those files usable from Claude Code, Codex, Gemini CLI, Ollama, and supported OpenAI-compatible providers.

It provides:

- zero-migration access to existing Kiro projects;
- requirements, design, task, approval, and drift workflows;
- deterministic reusable specification templates;
- capability-gated model and coding-agent runners;
- a Claude Code plugin with a local MCP server;
- Git evidence and trusted verification before task completion;
- explicit human approval and provider-independent quality gates.

Open Mind and SpecBridge are designed to complement each other: Open Mind can provide grounded repository knowledge and impact context before requirements, design, and task execution, reducing repeated codebase discovery and making specification workflows faster and safer.

**Core principles:** portable specifications, human-controlled approval, bounded execution, model independence, and verification-backed completion.

---

### ✅ [Agent Skill Verifier](https://github.com/HelloThisWorld/agent-skill-verification-template)

**A model-independent quality gate for AI agent skills.**

One command runs evaluation cases repeatedly, validates schema and citations, checks unsupported claims and tool-call order, stores replay artifacts, and fails CI when reliability drops below the configured threshold.

It ships as a CLI with cross-platform release artifacts and supports terminal, JSON, JUnit, and HTML reports.

**Core principles:** repeated evals, source-citation validation, replayable failures, CI release gates, and model-independent contracts.

---

### ⚒️ [agent-skill-forge](https://github.com/HelloThisWorld/agent-skill-forge)

**A pipeline for generating, testing, repairing, and packaging production-ready agent skills.**

```text
Skill requirement
    → behavioral contract
    → generated skill package
    → eval cases
    → verification
    → failure analysis
    → repair loop
    → quality gate
    → installable package
```

It treats agent skills as engineered components rather than prompt files, with explicit safety requirements, tool boundaries, acceptance criteria, provenance, and release evidence.

**Core principles:** contract-driven generation, pluggable verification, typed failure analysis, repair loops, and gated packaging.

---

### 🖥️ [winTerm](https://github.com/HelloThisWorld/winTerm)

**An independent open-source terminal application based on Microsoft Windows Terminal.**

winTerm explores production desktop engineering beyond AI projects: packaged Windows releases, workspace recovery, safe command compatibility, themes, private fonts, paste protection, privacy controls, accessibility checks, security review, and reproducible release verification.

**Core principles:** reliable desktop delivery, privacy by default, explicit feature gates, release evidence, and responsible upstream reuse.

---

## What I care about

- **Evidence over fluency**  
  Important answers should point back to real sources or clearly state that the available evidence is insufficient.

- **Knowledge as infrastructure**  
  Code, specifications, tests, decisions, and operational experience should become durable assets that approved AI tools can query safely.

- **Contracts over coupling**  
  Tools and agents should integrate through explicit, versioned schemas instead of importing each other's internal assumptions.

- **Governed automation**  
  AI may propose, analyze, and execute, while permissions, approvals, test gates, and rollback boundaries remain explicit.

- **Measured, not asserted**  
  Reliability should be demonstrated through evals, reports, replay artifacts, CI checks, and failure analysis.

- **Production-minded AI**  
  Useful agent systems need observability, partial-failure handling, privacy boundaries, source provenance, and maintainable integration surfaces.

---

## Current direction

I am currently exploring how verification-first code intelligence can grow into a broader engineering knowledge system:

- ingesting specifications and other engineering documents alongside repositories;
- preserving document structure, revision history, source authority, and provenance;
- detecting conflicting or stale engineering knowledge;
- linking requirements, design, implementation, tests, and operational evidence;
- exposing compact evidence packets to AI agents through provider-neutral contracts;
- using grounded repository context to accelerate specification and implementation workflows.

Future capabilities are kept separate from implemented claims: roadmap ideas are not presented as finished product behavior.

---

## Keywords

`AI agents` · `MCP` · `context engineering` · `engineering knowledge systems` · `source-grounded AI` · `code intelligence` · `enterprise AI` · `LLM evals` · `tool calling` · `verification-first systems` · `requirements traceability` · `production AI workflows`

---

MIT-licensed projects. Issues and PRs are welcome.
