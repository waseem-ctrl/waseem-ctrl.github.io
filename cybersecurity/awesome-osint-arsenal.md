# Awesome OSINT Arsenal — curated 753+ tool collection and installer

Added 19 Oct 2026. Entry 211. Open-source (MIT) curated catalog and multi-distro installer for OSINT, reconnaissance, red-team, blue-team, forensics, and related tools. Source: X post by @bkdgiffug (status 2111704329111450007) linking https://github.com/rawfilejson/awesome-osint-arsenal. Previously noted in project files from earlier posts (Sammy, tom_doerr). Use only on systems the client owns, has named in a written scope, or in a controlled lab. No install steps or attack procedures in this project.

## What it is

A single repository that indexes and provides install scripts for 753+ open-source tools across approximately 50 categories. Categories cover username/social OSINT (Sherlock, Maigret), domain/IP recon, email, dark-web search, image/video, metadata, threat intel, network scanning, red-team frameworks (Sliver, BloodHound, Nuclei, Impacket, NetExec), blue-team/detection (Wazuh, Suricata, Sigma, Velociraptor, Atomic Red Team), digital forensics/reversing (Volatility 3, Ghidra, radare2, Plaso, CyberChef), hardware/RF, and lab resources.

Public claims from the repository README and project site:
- Multi-distro installers (strongest support on Kali / Debian / Ubuntu / Parrot; partial on Arch and Fedora families)
- Separate scripts for OSINT-only, red-team, blue-team, forensics, hardware, labs, and Termux (Android)
- tools.json metadata file
- Version 2.1 (as of the May 2026 badge in promotional material)
- Georgian OSINT section and Termux support
- One-command convenience is the main value; individual tools retain their own licenses and scopes

The post and repository emphasize authorized testing only. Many tools inside the collection are already present in this project's numbered catalog (tools 1–210).

## Authorized use in this project

- Treat the repository as a directory and convenience installer, not as authorization. Each tool still requires its own written permission and named scope.
- Prefer selective install scripts (osint.sh, blueteam.sh, forensics.sh) over the full installer when the engagement is defensive or intel-focused.
- Red-team and hardware scripts are limited to client-owned systems, named lab ranges, or explicit written authorization. Do not point them at assets outside the scope.
- Client domains, brands, and incident artifacts only for OSINT lookups that could identify private persons. Email remains the preferred exposure key (see phone-number-scope.md).
- Isolated runtime recommended. Human review of any findings before client reporting.
- Complements existing service lines: external attack surface and identity/exposure (tools 1–30), scanning and web (31–50), network detection and SOC (51–60, 93–100, 141–147), forensics (92, 99, 143–147), and AI red teaming when the target is client-owned.
- Do not use for unauthorized scanning, personal dossiers, or any system the client does not control.

## Inputs required

- Written authorization naming the in-scope assets, allowed techniques, and dates.
- Confirmation whether a selective category script or the full collection is appropriate.
- Runtime environment (client-owned Kali/Debian host, lab VM, or Termux device under the client's control).
- Who on the client side will receive and triage any generated output.

## Report fields for the engagement

- Scope reference
- Which category scripts or individual tools were used
- High-level findings (validated by the engagement team)
- Controls that held or failed, impact, and recommended fix
- What was not tested and confirmation that activity stayed inside the named scope

Repository: https://github.com/rawfilejson/awesome-osint-arsenal  
License: MIT
