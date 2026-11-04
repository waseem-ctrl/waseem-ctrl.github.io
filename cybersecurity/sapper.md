# SAPPER (sapper-v2) — multi-agent autonomous pentest orchestration harness

Added 4 Nov 2026. Entry 219. Open-source (MIT) multi-agent orchestration harness for autonomous penetration testing. Source: X post by @MAXdeg0 (status 2117947185492807817) linking https://github.com/N1nEmAn/sapper-v2. Use only on client-owned systems, named lab ranges, or authorized CTF/competition environments. No install steps or attack procedures in this project.

## WARNING — high risk of misuse

This tool is designed for autonomous, multi-agent offensive operations that can run for hours with minimal human intervention, coordinating real security tools (including Nmap and Nuclei) via AI agents. Public claims describe an AI commander directing a swarm of worker agents (generals, scouts, soldiers) with shared memory via a layered fact-intent graph, self-healing via a watchdog, and operation inside a Kali Linux environment.

Key risks:

- Autonomous execution reduces the opportunity for real-time human oversight. Scope violations or unintended actions can propagate quickly across the agent swarm.
- It orchestrates real offensive tooling. Misconfiguration or weak scoping can lead to unauthorized scanning, exploitation attempts, or data access.
- Open-source and relatively easy to deploy. Lowers the barrier for unauthorized use compared to fully manual red-team work.
- Model-generated decisions and knowledge-base content may be incomplete, biased, or hallucinated. Findings require independent validation.
- Future versions may include accountability tracers (taggants) for attribution; current versions do not guarantee untraceability for misuse.
- Legal exposure is high. Unauthorized use against systems you do not own is illegal in most jurisdictions (e.g., computer fraud statutes, cybersecurity laws).

The project itself states: **AUTHORIZED SECURITY TESTING ONLY**. See the repository DISCLAIMER.md. The authors explicitly condemn misuse and state they will cooperate with lawful investigations. The original X post also notes: "Only use it in authorized labs and CTF environments."

In this catalog it is recorded solely for authorized defensive and assessment work. Do not use it outside written scope.

## What it is

A multi-agent orchestration harness (not a single agent) that coordinates an AI commander with a worker swarm. Public claims from the repository:

- Commander reads the board, decides, and dispatches; does not itself execute attacks.
- Worker agents (generals, scouts, soldiers, and emergent roles such as signalman) execute in parallel (typically via tmux panes).
- Layered fact-intent graph for persistent shared knowledge (title / summary / evidence layers) so findings survive individual agent sessions.
- Watchdog (script-only) for restart, key rotation, and deadline enforcement.
- Model- and CLI-agnostic: supports Claude Code, Codex, and other interactive agents; models can be swapped.
- Built for competition CTF scenarios (reported 3rd / champion in a Tencent Intelligent Attack-Defense online qualifier among 634 teams, 8 hours unattended). Also usable for ordinary multi-step agent work under proper controls.
- Pre-built Docker image available that includes a Kali toolchain and offline knowledge base.

Designed around the "Nüwa" foundation of Create / Language / History capabilities plus doctrine for division of labor.

## Authorized use in this project

- Authorized penetration testing or red-team assessment on client-owned systems or named lab ranges only. Written permission and named scope required before any activity.
- Prefer controlled lab or CTF environments for initial evaluation. Production or client systems only under explicit, narrow written authorization with continuous human oversight.
- Complements existing catalog entries such as PentAGI (209), Shannon (213), ARES (216), and traditional scanning/tools (Nmap 31, Nuclei 37). Useful when an engagement needs multi-agent coordination and persistent fact tracking.
- Isolated runtime required (prefer containerized). Human review of all findings, actions, and reports before client delivery. Do not point the system at assets outside the named scope.
- Model outputs and agent actions must be validated. Prefer modes with human checkpoints over fully unattended runs for client work.
- No unauthorized replication of third-party systems or data.

## Inputs required

- Written authorization naming the in-scope systems, allowed techniques, dates, and any constraints (e.g., no exploitation, specific ports, time windows).
- Confirmation of ownership or written permission for every target.
- Runtime environment under client control (or named lab). API keys for chosen model providers if external models are used.
- Who on the client side will receive and triage findings, and the process for stopping the run if scope risk appears.

## Report fields for the engagement

- Scope reference and confirmation that only authorized targets and techniques were used
- High-level findings with evidence citations and noted limitations or agent uncertainties
- Agent roles and tools invoked (high-level summary only)
- Fact-graph or session artifacts produced (high-level summary only)
- What was not tested and confirmation that activity stayed inside the named scope
- Any deviations from plan and how they were handled

Repository: https://github.com/N1nEmAn/sapper-v2  
License: MIT  
Disclaimer: see DISCLAIMER.md in the repository
