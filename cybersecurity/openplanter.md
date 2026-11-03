# OpenPlanter — recursive AI investigation agent for OSINT and entity resolution

Added 3 Nov 2026. Entry 217. Open-source (MIT) recursive language-model investigation agent with desktop GUI and terminal interface. Source: X post by @three_cube (status 2116927473703379133) linking https://github.com/ShinMegamiBoson/OpenPlanter. Use only on public records, client-owned or authorized datasets, or named lab ranges. No install steps or attack procedures in this project. Complements OSINT and entity-resolution workflows (tools 21–30, SpiderFoot, Maltego, OpenCTI) and AI-assisted investigation service lines.

## What it is

A recursive investigation agent that ingests heterogeneous datasets (corporate registries, campaign finance records, lobbying disclosures, government contracts, and similar public or client-supplied sources), resolves entities across them, and surfaces non-obvious connections through evidence-backed analysis. Public claims from the repository:

- Autonomous operation with file I/O, shell execution, web search (Exa), and recursive sub-agent delegation (default max-depth 4).
- Live knowledge graph visualization (Cytoscape.js) with force-directed, hierarchical, and circular layouts.
- Wiki source drawer and background wiki curator for persistent, cross-linked markdown documentation of findings.
- Session persistence and multi-provider LLM support (OpenAI, Anthropic, OpenRouter, Cerebras, Ollama).
- 19 tools organized around ingestion, shell, web, planning, and delegation.
- Desktop app (Tauri) and terminal/TUI interfaces.

Described in secondary sources as an open-source alternative focused on entity resolution and connection mapping for analysts who do not have access to commercial platforms such as Palantir.

## Authorized use in this project

- OSINT investigations and entity resolution on public records or datasets the client owns or has written authorization to analyze. Named lab only otherwise.
- Prefer public corporate, campaign, lobbying, contract, or similar open datasets. Do not use for personal dossiers, people-search, or unauthorized individual profiling.
- Complements existing catalog entries: theHarvester, Maltego, SpiderFoot, OpenCTI, and AI-assisted OSINT directories (Awesome OSINT Arsenal 211, Awesome OSINT MCP 215). Useful when an engagement needs automated cross-source entity resolution and evidence-backed connection mapping.
- Isolated runtime recommended. Human review of all findings, knowledge graphs, and reports before client delivery. Do not point the agent at private systems or data outside the named scope.
- Web search and shell capabilities require explicit scope covering those actions. Model-generated analysis must be validated.

## Inputs required

- Written authorization naming the in-scope datasets, public sources, or client-owned records, allowed investigation goals, and dates.
- Confirmation that any datasets are public or client-supplied and authorized for analysis.
- Runtime environment under client control (or named lab). API keys for chosen providers and optional Exa search.
- Who on the client side will receive and triage findings, graphs, and reports.

## Report fields for the engagement

- Scope reference and confirmation that only authorized datasets and public sources were used
- High-level entities resolved and connections surfaced (with evidence citations and confidence notes)
- Datasets or source categories ingested
- Knowledge-graph or wiki artifacts produced (high-level summary only)
- What was not tested and confirmation that activity stayed inside the named scope

Repository: https://github.com/ShinMegamiBoson/OpenPlanter  
License: MIT
