# T3MP3ST — autonomous red-teaming platform / multi-agent offensive-security meta-harness

Added 6 Nov 2026. Entry 220. Open-source (AGPL-3.0) self-hosted framework by elder-plinius (Pliny the elder). Source: X post by @MAXdeg0 (status 2118306509041910096) linking https://github.com/elder-plinius/T3MP3ST. Turns an existing AI coding agent into an autonomous security testing system with recon, vulnerability testing, and reporting. Use only on client-owned systems, named lab ranges, or authorized CTF environments. No install steps or attack procedures in this project.

## WARNING — high risk of misuse

This is an offensive-security tool that automates a kill-chain (recon → exploit → report) using real tools via multi-agent orchestration. Public claims describe an 8-operator model (Recon, Scanner, Exploiter, Infiltrator, Exfiltrator, Ghost, Coordinator, Analyst), a browser War Room, CLI, and an arsenal of 36–111 tools (full arsenal is opt-in and includes higher-risk items behind gates).

Key risks:

- Autonomous multi-agent execution reduces real-time human oversight. Scope violations can propagate quickly.
- It runs real security tooling (nmap, etc.) and can perform active testing. Weak scoping or misconfiguration can lead to unauthorized activity.
- Default egress filter helps contain scope, but operators must still enforce written boundaries.
- Model-generated findings require independent validation. Benchmark numbers are reproducible via `npm run verify-claims`, but live swarm exploitation remains experimental.
- Self-hosted and keyless when using local agents or local models (Ollama, LM Studio, vLLM). Lowers barrier compared to cloud-only tools.
- Legal exposure is high. Unauthorized use against systems you do not own is illegal in most jurisdictions.

The repository and original post both state: **only test systems you own or have permission to assess**. The project is provided AS-IS under AGPL-3.0 with no warranty. Review third-party terms (e.g., hosted model providers) before sending sensitive data.

In this catalog it is recorded solely for authorized defensive and assessment work. Do not use it outside written scope.

## What it is

A self-hosted, keyless multi-agent offensive-security meta-harness. Your existing AI coding agent (Claude Code, Codex, Hermes, OpenCode, Oh My Pi, or any OpenAI-compatible local model) becomes the brain; T3MP3ST supplies the War Room, mission model, evidence store, and tool arsenal.

Public claims from the repository:

- Browser-based War Room dashboard at `http://127.0.0.1:3333/ui/` (after `npm run server`) plus CLI (`npx t3mp3st`) and HTTP API.
- Op Admiral: describe an authorized target in plain English and launch a mission.
- Recon engine with live tool output (nmap, DNS, HTTP, fingerprinting). Findings trace to real evidence.
- Scope containment: default egress filter blocks off-scope public hosts; only target/subdomains and loopback allowed.
- White-box source analysis via web-tree-sitter (multiple languages).
- Coordinated-disclosure support (OSV check, PoC, CVSS drafts for human review).
- Benchmarks (recomputable): XBOW / XBEN 104-challenge suite 90.1% pass@1 (black-box), higher with white-box; Cybench and CVE-Zero results also published.
- Supports local models with no separate API keys. Optional hosted providers via environment variables.
- Docker option; server binds to 127.0.0.1 by default.

## Authorized use in this project

- Authorized penetration testing, web/API assessment, source-code review, CTF solving, or vulnerability research on client-owned systems or named lab ranges only. Written permission and named scope required before any activity.
- Prefer the War Room UI for operator visibility. Continuous human oversight recommended; avoid fully unattended production runs.
- Complements existing catalog entries such as PentAGI (209), Shannon (213), Basilisk (214), ARES (216), SAPPER (219), and traditional tools (Nmap 31, Nuclei 37, Burp 39). Useful when an engagement needs multi-agent coordination driven by an existing coding agent.
- Isolated runtime required (prefer containerized or localhost-only). Human review of all findings, actions, evidence, and reports before client delivery. Do not point the system at assets outside the named scope.
- Model outputs and agent actions must be validated against tool evidence. Prefer modes with human checkpoints.
- No unauthorized replication of third-party systems or data.

## Inputs required

- Written authorization naming the in-scope systems (URLs, hosts, repos, contracts, OT ranges), allowed techniques, dates, and constraints (e.g., no exploitation, specific ports, time windows, no production writes).
- Confirmation of ownership or written permission for every target.
- Runtime environment under client or lab control. Local agent already installed (Claude Code, Codex, etc.) or local model runtime (Ollama, etc.). Optional API keys only if using hosted models.
- Who on the client side will receive and triage findings, and the process for stopping the run if scope risk appears.
- For the War Room: after local start, open the UI, connect the agent in Settings, then launch via Op Admiral with a plain-English mission description that stays inside the written scope.

## Interface note

The tool’s primary operator interface is its own browser War Room (`http://127.0.0.1:3333/ui/` after the server is running). This catalog’s tool-input-console.html can collect the required scope fields for a T3MP3ST engagement and generate a JSON pack; it does not execute the tool.
