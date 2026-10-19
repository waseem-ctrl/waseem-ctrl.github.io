# Airgorah — Rust/GTK4 WiFi security auditing GUI for Linux

Added 19 Oct 2026. Entry 212. Open-source (MIT) WiFi security auditing application. Written in Rust with a GTK4 graphical interface. Source: X post by @bkdgiffug (status 2111563148746719396). Repository: https://github.com/martin-olivier/airgorah. Complements the existing wireless tools (61–65), especially Aircrack-ng (62). Use only on wireless networks the client owns, has named in a written scope, or in a controlled lab. No install steps or attack procedures in this project.

## What it is

A Linux-only desktop application that provides a graphical workflow for common WiFi security assessment tasks. It can:

- Capture nearby WiFi traffic (monitor mode)
- Discover clients connected to access points
- Perform deauthentication to force reconnection (for testing)
- Capture WPA/WPA2 handshakes and PMKIDs
- Support password cracking against captured material

Public claims from the repository README and recent releases (0.9.0, September 2026):

- Runs the GUI as a normal user; privileged operations use a small polkit-launched agent (airgorah-agent)
- Works under X11 and Wayland
- Native capture and handshake/PMKID handling; aircrack-ng suite is now an optional dependency
- Requires a wireless adapter that supports monitor mode and packet injection
- Explicit legal warning: only for networks you own; unauthorized use is illegal

The tool is a modern GUI front-end that packages the class of operations traditionally done with the aircrack-ng command-line suite.

## Authorized use in this project

- Wireless assessment of networks the client owns or has explicitly named in the written scope (SSIDs, BSSIDs, locations). Lab ranges only otherwise.
- Complements service line “Wireless, lab unless SSIDs are named” (tools 61–65).
- Prefer passive observation and controlled testing on owned infrastructure. Deauthentication and cracking steps require explicit authorization covering those techniques.
- Client-owned systems or named lab only. Isolated runtime recommended.
- Human review of any findings before client reporting.
- Do not point the tool at networks outside the named scope.

## Inputs required

- Written authorization naming the in-scope SSIDs/BSSIDs, allowed techniques (including whether deauthentication or cracking is permitted), and dates.
- Confirmation that a suitable monitor-mode/packet-injection wireless adapter is available on a client-owned Linux host or lab system.
- Runtime environment (Linux host under client control).
- Who on the client side will receive and triage any generated output (handshakes, PMKIDs, cracked material).

## Report fields for the engagement

- Scope reference
- Which access points and clients were observed
- Whether handshakes or PMKIDs were captured (and under what authorization)
- High-level findings (e.g., weak passphrase strength if cracking was authorized and successful)
- Controls that held or failed, impact, and recommended fix
- What was not tested and confirmation that activity stayed inside the named scope

Repository: https://github.com/martin-olivier/airgorah  
License: MIT  
Latest noted release: 0.9.0 (PMKID support, reduced external dependencies)
