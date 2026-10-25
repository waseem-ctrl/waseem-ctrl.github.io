# Cybersecurity project index

Master index for this project. Updated 26 Oct 2026. Use this file first.

Rule for every entry: written permission, named assets, a report. No install steps and no attack procedures in this project. Practice ranges are not client targets.

## Files

| File | What it is |
| --- | --- |
| Cybersecurity.md | Conversation record, task-order sources, excluded packs |
| tools-100.md | Tools 1-100, from X lists, for assessment, SOC, intel, GRC |
| tools-50-bleach.md | Tools 101-150, mapped to Bleach Security's integrate / assess / fix / monitor cycle |
| tools-151-190.md | Tools 151-190 from Reddit, Bellingcat categories, OWASP, abuse.ch, and X |
| phone-number-scope.md | Phone or email: client asset or incident artifact only. Email is the exposure key. No person dossier |
| oss-scanner.md | Anthropic OSS Scanner (entry 208). Free opt-in AI vulnerability scans for eligible critical open-source projects. Model-generated unreviewed reports. Client-owned or explicitly authorized only. |
| pentagi.md | PentAGI (entry 209). Open-source multi-agent autonomous penetration testing platform. Client-owned systems or named lab only. |
| darknet-mcp.md | Darknet MCP Server (entry 210). AI-assisted aggregator for dark-web and threat-intel sources via MCP. Client domains/brands only; Tor tools high-risk and out of preferred scope. Isolated runtime required. |
| awesome-osint-arsenal.md | Awesome OSINT Arsenal (entry 211). Curated catalog and multi-distro installer for 753+ OSINT, red-team, blue-team, and forensics tools. Directory and convenience installer only; each tool still needs its own written scope. Selective scripts preferred. Client-owned systems or named lab. |
| airgorah.md | Airgorah (entry 212). Rust/GTK4 WiFi security auditing GUI for Linux. Complements Aircrack-ng for authorized wireless assessments. Client-owned networks or named lab only. |
| basilisk.md | Basilisk (entry 214). Open-source AI red teaming framework with genetic prompt evolution. OWASP LLM Top 10 modules, differential testing, posture grading, signed audit logs. Client-owned LLM/agent systems or named lab only. |

GitHub copies, repo waseem-ctrl/waseem-ctrl.github.io:

- cybersecurity/tools-100.md
- cybersecurity/tools-50-bleach.md
- cybersecurity/INDEX.md
- cybersecurity/awesome-osint-arsenal.md
- cybersecurity/airgorah.md
- cybersecurity/basilisk.md

## Task-order sources

- https://nmb-consulting.com — STCC Cybersecurity Advisor. Assessment, threat report, solution catalog, global intel. Contact on the page: Waseem@STCCSolutions.com.
- https://cybergl.com — CyberGlobal. Penetration testing, SOC, application security, network security, cloud security, incident response and threat intelligence, GRC. Contact: info@cybergl.com.
- https://bleachsecurity.com — Bleach Security, SMB platform. Integrate, assess, guided fix, continuous monitoring, compliance evidence. Not the ESP32 firmware named Bleach.

## Service lines

| Line | Tool numbers |
| --- | --- |
| External attack surface | 1-20 |
| Identity and exposure, lawful basis required | 21-30 |
| Scanning | 31-38 |
| Web and mobile | 39-50 |
| Network detection | 51-60 |
| Wireless, lab unless SSIDs are named | 61-65, 212 |
| Active Directory | 66-71 |
| Cloud, containers, DevSecOps | 72-82, 108-110, 209 |
| Credentials, reversing, malware lab | 83-92, 119-120 |
| SOC, intel, forensics, reporting | 93-100, 141-147 |
| SMB assess and track | 101-107 |
| Endpoint and identity operations | 111-118 |
| Email, DNS, brand | 121-130 |
| Edge, logging, assets | 131-140 |
| Backup and awareness simulation | 148-150 |

## Tools 1-100

1 Shodan. 2 Censys. 3 theHarvester. 4 Maltego. 5 Amass. 6 Subfinder. 7 WHOIS / RDAP. 8 SpiderFoot. 9 Recon-ng. 10 BBOT. 11 reNgine. 12 reconFTW. 13 Photon. 14 Katana. 15 httpx. 16 waymore. 17 urlfinder. 18 Osmedeus. 19 dnstwist. 20 Sn0int. 21 Sherlock. 22 Maigret. 23 Blackbird. 24 Holehe. 25 GHunt. 26 Have I Been Pwned. 27 ExifTool. 28 Metagoofil. 29 Ahmia. 30 OSINT Framework. 31 Nmap. 32 Masscan. 33 RustScan. 34 enum4linux. 35 SNMPwalk. 36 Netcat. 37 Nuclei. 38 Naabu. 39 Burp Suite. 40 OWASP ZAP. 41 Nikto. 42 Gobuster. 43 ffuf. 44 Dirsearch. 45 SQLmap. 46 WPScan. 47 Searchsploit. 48 OWASP Dependency-Check. 49 Semgrep. 50 MobSF. 51 Wireshark. 52 tcpdump. 53 TShark. 54 Scapy. 55 Zeek. 56 Suricata. 57 Security Onion. 58 Arkime. 59 RITA. 60 Brim / Zui. 61 Kismet. 62 Aircrack-ng. 63 Bettercap. 64 hcxdumptool. 65 Wifite. 66 BloodHound. 67 NetExec. 68 Impacket. 69 Certipy. 70 PingCastle. 71 Purple Knight. 72 ScoutSuite. 73 Prowler. 74 Pacu. 75 Trivy. 76 kube-hunter. 77 kube-bench. 78 Checkov. 79 Dockle. 80 Docker Bench. 81 Grype. 82 Syft. 83 Hashcat. 84 John the Ripper. 85 CeWL. 86 CyberChef. 87 Ghidra. 88 IDA Free. 89 x64dbg. 90 Radare2 / Cutter. 91 YARA. 92 Volatility 3. 93 Wazuh. 94 MISP. 95 Velociraptor. 96 TheHive. 97 Sigma. 98 Sysmon. 99 Autopsy. 100 Dradis.

## Tools 101-150

101 Greenbone OpenVAS. 102 DefectDojo. 103 Faraday. 104 Lynis. 105 OpenSCAP. 106 ScubaGear. 107 Maester. 108 Steampipe. 109 CloudQuery. 110 Sift. 111 osquery. 112 Fleet. 113 ClamAV. 114 Authentik. 115 Keycloak. 116 CrowdSec. 117 Fail2ban. 118 Bitwarden. 119 Gitleaks. 120 TruffleHog. 121 parsedmarc. 122 Rspamd. 123 MX Toolbox. 124 URLhaus. 125 PhishTank. 126 OpenSquat. 127 Cloudflare Radar. 128 Spamhaus. 129 Microsoft 365 Defender export. 130 Sigma mail rules. 131 OPNsense. 132 pfSense. 133 ntopng. 134 Graylog. 135 Grafana Loki. 136 Prometheus. 137 Uptime Kuma. 138 NetBox. 139 GLPI. 140 Shuffle. 141 OpenCTI. 142 DFIR-IRIS. 143 KAPE. 144 EZ Tools. 145 Chainsaw. 146 Hayabusa. 147 Plaso. 148 Restic. 149 BorgBackup. 150 GoPhish.

## Tools 151-190

151 VirusTotal. 152 MalwareBazaar. 153 ThreatFox. 154 Feodo Tracker. 155 AlienVault OTX. 156 Malpedia. 157 REMnux. 158 CAPE sandbox. 159 urlscan.io. 160 GreyNoise. 161 OWASP Dependency-Track. 162 OWASP Threat Dragon. 163 osv-scanner. 164 SonarQube. 165 Bandit. 166 Opengrep. 167 Sigstore / cosign. 168 HashiCorp Vault. 169 SOPS. 170 OWASP CRS with Coraza or ModSecurity. 171 MITRE ATT&CK Navigator. 172 Atomic Red Team. 173 Caldera. 174 Canarytokens. 175 OpenCanary. 176 Tracebit Community Edition. 177 Falco. 178 Tracee. 179 Snort. 180 Malcolm. 181 Obsidian. 182 ArchiveBox. 183 Wayback Machine. 184 crt.sh. 185 SecurityTrails. 186 BGPView. 187 InVID / WeVerify. 188 KeePassXC. 189 Open Policy Agent. 190 Open Security Architecture patterns.

Authorized use for 151-190 is in tools-151-190.md. Sources: r/netsec, r/osinttools, Bellingcat toolkit categories, OWASP, abuse.ch, and X posts naming Wazuh, VirusTotal, and OpenCTI.

## Practice ranges, not targets

Hack The Box. TryHackMe. PortSwigger Academy. VulnHub.

## Directories, not tools

OSINTRack. OSINT Tools Library. Bellingcat Toolkit. OSINT Library. OSINT Framework. awesome-osint-arsenal is an installer, not authorization.

## X sources already reviewed

- https://x.com/maxdeg0/status/2104824972770197707
- https://x.com/hack_git/status/1685552127513411584
- https://x.com/he1s_sammy/status/2104935190602637567
- https://x.com/hamzaonchain/status/2103481325348856123
- https://x.com/hamzaonchain/status/2103861759048130610
- https://x.com/NitinGavhane_/status/2100986041629098038
- https://x.com/M_jawad_yasin/status/2103947149050614223
- https://x.com/Anastasis_King/status/2104140214864110063
- https://x.com/Cyber_Sudo/status/2064211111205851415
- https://x.com/MAXdeg0/status/2105187330390712653
- https://x.com/tom_doerr/status/2091139865920377225
- https://x.com/simplifyinAI/status/2109475720015851688 (PentAGI)
- LinkedIn post by Kenny Felix (https://lnkd.in/p/dFkzqhGN) on Darknet MCP Server (entry 210)
- https://x.com/bkdgiffug/status/2111704329111450007 (Awesome OSINT Arsenal, entry 211)
- https://x.com/bkdgiffug/status/2111563148746719396 (Airgorah, entry 212)
- https://x.com/MAXdeg0/status/2114247743531012339 (Basilisk, entry 214)

## Excluded from the index

Z4nzu/hackingtool. Manisso/fsociety and forks. Trape. emailosint.org as a dossier site. FLOCK4H/Bleach ESP32 attack firmware. Recycled "feels illegal" posts that only repeat those three links.

## What would unblock the next pass

Nothing else is required to keep indexing public tools. Useful if you want the index tied to live work:

- A written scope: client name, in-scope assets, allowed techniques, dates.
- Access to a private repo if this catalog should not sit on the public GitHub Pages repo.
- Google Drive, if engagement notes already live there.
- A CyberGlobal or STCC statement of work, if task orders should be matched to a service line.
