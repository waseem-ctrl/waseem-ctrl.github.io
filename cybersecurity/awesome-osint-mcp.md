# Awesome OSINT MCP Servers — curated list of OSINT MCP tools

Added 27 Oct 2026. Entry 215. Curated directory of MCP servers for OSINT. Source: X post by @Sox0j (status 2114662320089767955) linking https://github.com/soxoj/awesome-osint-mcp-servers and the Start.me mirror https://start.me/p/aNMY5j/awesome-osint-mcp-servers. Author is Soxoj (@Sox0j), also known for Maigret. Use only on client-owned domains, brands, incident artifacts, or named lab systems. No install steps or attack procedures in this project.

## What it is

A curated list of Model Context Protocol (MCP) servers that expose OSINT tools and data sources to LLM clients (Claude, Cursor, Windsurf, and others). An MCP server lets an agent query the tool in natural language and receive structured results for flexible reporting.

Public claims from the repository and Start.me page:
- 70+ tools across 11 categories
- Categories: SOCMINT, Network Scanning, Web Scraping, Company Intelligence, Public Records & Compliance, Threat Intelligence, Geospatial & Geopolitical Intelligence, Research Intelligence, Meta / Discovery, Blockchain Intelligence, Market & Trading
- Legend marks open-source, free / free-tier, and paid / API-key required entries
- Examples include MCP wrappers for Maigret, Shodan, ZoomEye, DNSTwist, Wayback Machine, and various company/public-record lookups
- MIT license
- Pull requests welcomed; the list is actively maintained

The Start.me page is a browsable mirror of the same collection. Many individual tools inside the list already appear in this project's numbered catalog.

## Authorized use in this project

- Treat the list as a directory of MCP servers, not as authorization. Each server and the data source behind it still requires its own written permission and named scope.
- Prefer free or self-hosted entries when the engagement is defensive or intel-focused. Paid API endpoints need the client's own keys and remain subject to the provider's terms.
- Client domains, brands, and incident artifacts only for lookups that could identify private persons. Email remains the preferred exposure key (see phone-number-scope.md).
- Isolated runtime recommended. Human review of any agent-generated findings before client reporting.
- Complements existing service lines: external attack surface and identity/exposure (tools 1–30), scanning (31–38), SOC/intel (93–100, 141–147), and the Darknet MCP entry (210). Also fits AI-assisted OSINT workflows when the target is client-owned.
- Do not use for unauthorized scanning, personal dossiers, or any system the client does not control.

## Inputs required

- Written authorization naming the in-scope assets, allowed techniques, and dates.
- Confirmation of which category or specific MCP servers are appropriate.
- Runtime environment (client-owned host or lab where the MCP client and any self-hosted servers will run).
- API keys or credentials for any paid or rate-limited services, held by the client.
- Who on the client side will receive and triage the generated output.

## Report fields for the engagement

- Scope reference
- Which MCP servers or categories were used
- High-level findings (validated by the engagement team)
- Controls that held or failed, impact, and recommended fix
- What was not tested and confirmation that activity stayed inside the named scope

Repository: https://github.com/soxoj/awesome-osint-mcp-servers  
Start.me: https://start.me/p/aNMY5j/awesome-osint-mcp-servers  
License: MIT
