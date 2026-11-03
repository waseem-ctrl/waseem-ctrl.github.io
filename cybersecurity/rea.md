# REA — Reverse Engineer Anything (MCP orchestrator for authorized reverse engineering)

Added 3 Nov 2026. Entry 218. Open-source (MIT) MCP server and CLI that connects AI agents to reverse-engineering tools for analyzing software artifacts without source code. Source: X post by @HoodieFade_ (status 2117258560270655816) linking the stack including https://github.com/morluto/rea. Use only on client-owned binaries, applications, firmware, or named lab ranges. No install steps or attack procedures in this project. Complements reverse engineering and malware lab service lines (tools 87–92) and AI-assisted analysis.

## What it is

An orchestration layer (MCP + CLI) that lets coding agents (Claude Code, Codex, Cursor, Gemini CLI, Grok Build, and other MCP clients) inspect native binaries, JavaScript/Electron apps, .NET assemblies, Android APKs, firmware, websites, and other targets. Public claims from the repository and secondary sources:

- Unified interface over established engines (Ghidra free; Hopper or IDA Pro require valid licenses).
- Evidence-backed results: findings include evidence identifiers, limitations, and unknowns rather than unverified claims.
- Local analysis. Supports native binaries (pseudocode, assembly, symbols, xrefs via configured provider), Electron/JS, .NET, APKs (JADX), firmware, network captures, and more.
- CLI and MCP modes. Does not replace decompilers; it drives them and structures output for agents.
- High star count on GitHub (hundreds of thousands) reflecting rapid adoption in 2026.

The X post also lists complementary tools in the same stack: radare2 (already cataloged as 90), Ghidra (87), LLM4Decompile (neural decompilation models), r2ai (LLM plugin for radare2), reverse-engineering-assistant / ReVa (Ghidra MCP), and ida-pro-mcp. Each still requires its own written scope.

## Authorized use in this project

- Reverse engineering and malware analysis on client-owned binaries, applications, firmware images, or incident artifacts. Named lab only otherwise.
- Prefer Ghidra as the free native backend. Commercial engines (IDA, Hopper) only with valid client licenses.
- Complements existing catalog entries: Ghidra, IDA Free, radare2/Cutter, and AI red-teaming lines. Useful when an engagement needs agent-assisted analysis of closed-source targets with evidence trails.
- Isolated runtime required. Human review of all findings and reports before client delivery. Do not point the tool at systems or binaries outside the named scope.
- Model-generated analysis must be validated against engine evidence. No unauthorized replication of third-party features.

## Inputs required

- Written authorization naming the in-scope binaries, applications, firmware, or artifacts, allowed analysis goals, and dates.
- Confirmation of ownership or written permission for every target.
- Runtime environment under client control (or named lab). Configured analysis engine (Ghidra preferred) and any required licenses.
- Who on the client side will receive and triage findings.

## Report fields for the engagement

- Scope reference and confirmation that only authorized targets were analyzed
- High-level findings with evidence citations and noted limitations
- Engines and target types used
- Artifacts or session bundles produced (high-level summary only)
- What was not tested and confirmation that activity stayed inside the named scope

Repository: https://github.com/morluto/rea  
License: MIT (third-party components retain their own licenses)  
Website: https://rea.tools
