# ARES — open-source authorized red-team engagement automation platform

Added 3 Nov 2026. Entry 216. Open-source (MIT) operator-directed red team platform for authorized engagements. Source: X post by @MAXdeg0 (status 2117230634993078372) linking https://github.com/Mafifrizi/ARES. Use only on systems, domains, or cloud environments the client owns or has named in a written scope. No install steps or attack procedures in this project. Complements Active Directory tools (66–71), cloud assessment tools, and existing autonomous platforms (PentAGI 209, Shannon 213).

## What it is

An open-core platform for enterprise red teams, MSSPs, and SOCs to execute targeted offensive engagements, discover deterministic attack paths, and continuously validate defensive posture. Public claims from the repository:

- Goal-directed attack planning (e.g., domain_admin, full_compromise, cloud_audit) using DAG heuristics and optional LLM agents (Claude, OpenAI, Ollama).
- 66 active production modules (70 total catalogued) covering 60+ MITRE ATT&CK techniques across Active Directory, Windows, Linux, and cloud (AWS, Azure, GCP).
- Real-time BloodHound ingest and attack graph / shortest-path computation.
- Dual-layer Scope Firewall (application-layer ScopeGuard + OS/transport-level egress filtering) with fail-closed isolation to approved IP ranges.
- AES-256-GCM encrypted credential vault.
- Operator dashboard (React), CLI, module orchestrator, OPSEC noise profiling, RBAC, and multi-format reporting (PDF, HTML, Markdown, JSON).
- Explicit authorization warning: only test systems you own or have written permission to assess. Unauthorized use is illegal.

## Authorized use in this project

- Red team / adversary emulation on client-owned Active Directory forests, Windows/Linux hosts, or cloud accounts named in the written scope. Lab ranges only otherwise.
- Prefer controlled lab runs or scoped campaigns with the dual-layer Scope Firewall active. Goal-directed planning and active modules require explicit authorization covering those techniques.
- Complements existing catalog entries: BloodHound (66), NetExec (67), Impacket (68), Certipy (69), and cloud tools (72–82). Useful when an engagement needs automated path discovery and reporting rather than manual module chaining.
- Isolated runtime recommended. Human review of all findings, attack paths, and reports before client delivery. Do not point the platform at systems outside the named scope.
- Signed/audit trails and scope enforcement are positive controls; still require written permission and named assets.

## Inputs required

- Written authorization naming the in-scope assets (domains, hosts, cloud accounts, IP ranges), allowed techniques/goals, and dates.
- Confirmation of BloodHound data or live collection rights if graph features will be used.
- Runtime environment under client control (or named lab).
- Who on the client side will receive and triage findings and reports.

## Report fields for the engagement

- Scope reference and confirmation that Scope Firewall / egress controls remained active
- Goals tested and high-level attack paths discovered (validated by the engagement team)
- Modules or families used
- Controls that held or failed, impact, and recommended fix
- What was not tested and confirmation that activity stayed inside the named scope

Repository: https://github.com/Mafifrizi/ARES  
License: MIT
