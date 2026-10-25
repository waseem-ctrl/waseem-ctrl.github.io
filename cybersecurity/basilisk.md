# Basilisk — open-source AI red teaming framework with genetic prompt evolution

Added 26 Oct 2026. Entry 214. Open-source (AGPL-3.0) AI red teaming and LLM security testing framework. Source: X post by @MAXdeg0 (status 2114247743531012339) linking https://github.com/regaan/basilisk. Developed by Regaan (ROT Independent Security Research Lab). Use only on LLM systems, agents, or endpoints the client owns or has named in a written scope. No install steps or attack procedures in this project. Complements the AI red teaming service line (artifacts/ai-red-team.md).

## What it is

An automated offensive security framework for AI/LLM red teaming. It uses evolutionary prompt search (Smart Prompt Evolution / SPE-NL genetic algorithm) to generate and refine adversarial prompts. Public claims from the repository and documentation:

- 33 attack modules across categories mapped to OWASP LLM Top 10 (prompt injection, system prompt extraction, data exfiltration, tool abuse, guardrail bypass, DoS, multi-turn manipulation, RAG attacks, multimodal injection, and others). Modules have trust tiers (production / beta / research).
- Reconnaissance modules for model fingerprinting, guardrail profiling, tool discovery, context window measurement, and RAG detection.
- Differential testing across providers (OpenAI, Anthropic, Google, xAI/Grok, GitHub Models, Ollama, vLLM, custom endpoints via litellm).
- Guardrail posture assessment with A+ to F grading (non-destructive recon-only mode available).
- Evidence-backed findings, signed audit logs (Ed25519 / SHA-256 chain integrity), and reports in HTML, JSON, SARIF, Markdown, and PDF.
- CLI, Electron desktop app, Docker image, PyPI package (`basilisk-ai`), and native GitHub Action for CI/CD with regression detection.
- Explicit authorization warning: only test systems you own or have written permission to assess.

## Authorized use in this project

- AI red teaming of client-owned staging agents, models, or retrieval systems only (see artifacts/ai-red-team.md).
- Prefer posture / recon-only modes or controlled lab runs when possible. Active attack modules (including evolutionary jailbreak generation) require explicit authorization covering those techniques.
- Client-owned systems or named lab only. Isolated runtime recommended. Human review of all findings and evidence before any client report.
- Complements existing AI red teaming entries (PentAGI 209, Shannon 213) and the service line method. Do not use for public chatbots, third-party models outside scope, or any system the client does not control.
- Signed audit logs and SARIF output are useful for engagement evidence and CI regression checks when the client wants them.

## Inputs required

- Written authorization naming the in-scope model/agent/endpoint, allowed techniques (including whether evolutionary attacks or specific module families are permitted), and dates.
- Staging endpoint or configuration export (default: no production data).
- Provider credentials or local model access under client control.
- Policy the system is supposed to enforce (for pass/fail evaluation).
- Who on the client side will receive and triage findings and signed logs.

## Report fields for the engagement

- Scope reference
- Modules or scan modes used (posture vs. full scan, trust tiers included)
- High-level findings (validated by the engagement team; evidence references only)
- Guardrail posture grade if assessed
- Controls that held or failed, impact, and recommended fix
- Confirmation that activity stayed inside the named scope and that audit logs were retained as required

Repository: https://github.com/regaan/basilisk  
License: AGPL-3.0  
Website: https://basilisk.rothackers.com
