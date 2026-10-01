# 100 tools for authorized cybersecurity work

Catalog for task orders from https://nmb-consulting.com (STCC Cybersecurity Advisor) and https://cybergl.com (CyberGlobal). Collected 1 Oct 2026 from X posts that list tools for assessment, SOC, OSINT, and GRC.

Use only on systems you own or that a written scope names. This file is a catalog. It has no install steps and no attack procedures.

Excluded on purpose: all-in-one hacking packs (Z4nzu/hackingtool, Manisso/fsociety), people-tracking kits (Trape), and reverse-email dossier sites. Those showed up in the same X threads and are not a baseline for client work.

Primary X sources:

- Hamza, 25 Sep 2026: https://x.com/hamzaonchain/status/2103481325348856123 and follow-up https://x.com/hamzaonchain/status/2103861759048130610
- Nitin Gavhane, 18 Sep 2026: https://x.com/NitinGavhane_/status/2100986041629098038
- Jawad, 26 Sep 2026: https://x.com/M_jawad_yasin/status/2103947149050614223
- Anastasis, 27 Sep 2026: https://x.com/Anastasis_King/status/2104140214864110063
- Cyber_Sudo, 9 Jun 2026: https://x.com/Cyber_Sudo/status/2064211111205851415
- Tom Doerr, 22 Aug 2026 and 24 Sep 2026: awesome-osint-arsenal mentions

## Recon and external attack surface

1. Shodan. Internet-exposed asset inventory on in-scope ranges.
2. Censys. Certificate and host inventory.
3. theHarvester. Passive email, host, and name collection for a named domain.
4. Maltego. Link analysis of data already collected under scope.
5. Amass. External asset and subdomain discovery.
6. Subfinder. Passive subdomain discovery.
7. WHOIS / RDAP. Registration context for in-scope domains.
8. SpiderFoot. Automated OSINT correlation for a named target.
9. Recon-ng. Modular recon against an authorized domain.
10. BBOT. Attack-surface scan of assets in the rules of engagement.
11. reNgine. Recon pipeline for a bug-bounty or pentest scope.
12. reconFTW. Bundled recon workflow for the same scope.
13. Photon. OSINT crawler for an authorized site.
14. Katana. URL crawling of in-scope web apps.
15. httpx. Probe which discovered hosts answer.
16. waymore. Historical URL collection for in-scope domains.
17. urlfinder. URL discovery from public sources.
18. Osmedeus. Workflow runner for an authorized recon engagement.
19. dnstwist. Lookalike-domain check for a brand you are defending.
20. Sn0int. Semi-automatic OSINT for a defined investigation.

## Identity and exposure checks

Lawful basis required. Prefer the client's own domains and addresses. Not for a dossier on a private person.

21. Sherlock. Username correlation when the engagement asks for it.
22. Maigret. Broader username search.
23. Blackbird. Username search across public profiles.
24. Holehe. Sites registered to an address the client owns or controls.
25. GHunt. Google-account footprint of an address in scope.
26. Have I Been Pwned. Breach exposure check for client domains and addresses.
27. ExifTool. Metadata on files the client provided.
28. Metagoofil. Public document metadata for an in-scope domain.
29. Ahmia. Public onion-index search for threat intel.
30. OSINT Framework. Directory of sources, used as a map not a scanner.

## Scanning and enumeration

31. Nmap. Host and service discovery inside the written range.
32. Masscan. Fast port sweep only on ranges the scope allows.
33. RustScan. Faster front end to Nmap, same scope rule.
34. enum4linux. SMB enumeration on in-scope Windows hosts.
35. SNMPwalk. SNMP read on devices the client owns.
36. Netcat. Connectivity checks in a lab or scoped host.
37. Nuclei. Template checks for known issues on in-scope URLs.
38. Naabu. Port discovery paired with httpx on a named scope.

## Web application testing

39. Burp Suite. Manual web testing inside a pentest or bounty scope.
40. OWASP ZAP. Automated and manual web assessment.
41. Nikto. Legacy web misconfiguration check.
42. Gobuster. Content discovery on an authorized app.
43. ffuf. Fuzzing of in-scope parameters and paths.
44. Dirsearch. Directory discovery on an authorized app.
45. SQLmap. Injection testing only where the scope allows active tests.
46. WPScan. WordPress assessment of a site the client owns.
47. Searchsploit. Local lookup of public advisories while writing findings.
48. OWASP Dependency-Check. Library review of code the client gave you.
49. Semgrep. Static review of an authorized codebase.
50. MobSF. Mobile app review of a build the client provided.

## Network analysis and detection

51. Wireshark. Packet analysis on a span, tap, or capture the client owns.
52. tcpdump. Same, from the command line.
53. TShark. Scripted packet analysis of those captures.
54. Scapy. Packet crafting in a lab or on an explicitly allowed segment.
55. Zeek. Network security monitoring on client sensors.
56. Suricata. IDS on client traffic.
57. Security Onion. Sensor and hunting distro for a SOC engagement.
58. Arkime. Full packet retention and search for an incident.
59. RITA. Beacon detection on Zeek logs the client exported.
60. Zui. Log and pcap review during an investigation.

## Wireless, lab only unless the scope names the SSIDs

61. Kismet. Wireless survey of a site the client asked you to assess.
62. Aircrack-ng. Lab or owned-network wireless assessment.
63. Bettercap. Lab exercises on owned gear.
64. hcxdumptool. Capture for an authorized wireless test.
65. Wifite. Automated lab workflow for that test.

## Active Directory, only on a domain the client owns

66. BloodHound. Attack-path mapping from data collected in the engagement.
67. NetExec. Authentication and enumeration tests in scope.
68. Impacket. Protocol-level checks against in-scope Windows services.
69. Certipy. AD CS review when identity is in the rules of engagement.
70. PingCastle. AD hygiene report for the client's domain.
71. Purple Knight. Identity security assessment for that domain.

## Cloud, containers, and DevSecOps

72. ScoutSuite. Multi-cloud configuration review with client credentials.
73. Prowler. AWS, Azure, and GCP benchmark checks.
74. Pacu. AWS framework, lab or explicit cloud scope only.
75. Trivy. Image, filesystem, and IaC vulnerability scan.
76. kube-hunter. Kubernetes assessment of a cluster the client owns.
77. kube-bench. CIS benchmark for that cluster.
78. Checkov. Policy-as-code scan of IaC the client provided.
79. Dockle. Container image lint.
80. Docker Bench. Host Docker configuration review.
81. Grype. Vulnerability match on SBOMs and images.
82. Syft. SBOM generation for a build in scope.

## Credential testing, reverse engineering, and malware lab

83. Hashcat. Password audit of hashes the client exported.
84. John the Ripper. Same.
85. CeWL. Wordlist from the client's own site, for that audit.
86. CyberChef. Encode, decode, and transform data in a report.
87. Ghidra. Reverse engineering of a sample the client owns.
88. IDA Free. Same.
89. x64dbg. Debugger for that lab sample.
90. Radare2 / Cutter. Same.
91. YARA. Signature match on files in an incident.
92. Volatility 3. Memory forensics on a capture the client provided.

## SOC, intel, forensics, GRC, and reporting

93. Wazuh. Endpoint detection, file integrity, and log analysis.
94. MISP. Threat-intel sharing for indicators the engagement may use.
95. Velociraptor. Endpoint hunting on agents the client deployed.
96. TheHive. Case management for an incident.
97. Sigma. Detection rules mapped to the client's SIEM.
98. Sysmon. Windows telemetry the client installed.
99. Autopsy. Disk forensics on media the client handed over.
100. Dradis. Findings and report assembly for the engagement.

Practice ranges, not client targets: Hack The Box, TryHackMe, PortSwigger Academy, VulnHub.

Directories, not extra tools: OSINTRack, OSINT Tools Library, Bellingcat Toolkit, OSINT Library, OSINT Framework. awesome-osint-arsenal is a 750-tool installer. An installer is not authorization.
