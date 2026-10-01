# 50 tools that complement Bleach Security

Added 1 Oct 2026. Complements the first 100 in tools-100.md.

Bleach Security (https://bleachsecurity.com) is an SMB platform: integrate existing tech, assess, guided fix, then continuous monitoring and compliance reporting. These 50 fill the gaps that platform implies and that the first catalog under-weighted: vulnerability management, hardening, identity, email authentication, backup, asset inventory, and detection engineering.

This is not the ESP32 project named Bleach (FLOCK4H/Bleach). That firmware is a wireless and Bluetooth attack kit. It is not part of this list.

Same rule as the first 100: written scope, client-owned systems, no install steps and no attack procedures here.

## Assess and track findings

101. Greenbone OpenVAS. Authenticated vulnerability scan of hosts the client owns.
102. DefectDojo. Store and deduplicate findings from scans and pentests.
103. Faraday. Engagement workspace for a scoped assessment.
104. Lynis. Host hardening audit on a server the client owns.
105. OpenSCAP. Benchmark scan against a published policy.
106. ScubaGear. Microsoft 365 baseline check with tenant admin consent.
107. Maester. Microsoft 365 and Entra configuration tests.
108. Steampipe. SQL-style queries over cloud APIs the client connected.
109. CloudQuery. Asset inventory sync from cloud accounts in scope.
110. Sift. Secrets search across M365, Slack, and Jira the client connected.

## Endpoint and identity

111. osquery. Live endpoint queries on agents the client deployed.
112. Fleet. Manage those osquery agents.
113. ClamAV. Malware scan of mail and file shares the client owns.
114. Authentik. Identity provider for a client portal or lab.
115. Keycloak. Same, when the client already runs it.
116. CrowdSec. Collaborative blocklist on a host or reverse proxy they own.
117. Fail2ban. Login-abuse blocking on servers in scope.
118. Bitwarden. Shared vault for engagement credentials, not a findings dump.
119. Gitleaks. Secret scan of a repository the client gave you.
120. TruffleHog. Same, including verified-secret checks on that repo.

## Email, DNS, and brand

121. parsedmarc. DMARC report analysis for domains the client controls.
122. Rspamd. Mail filtering on a gateway they own.
123. MX Toolbox. DNS, blacklist, and mail-record checks for their domains.
124. URLhaus. Lookup of URLs already seen in the client's mail.
125. PhishTank. Same, for reported phishing links.
126. OpenSquat. Lookalike domain watch for a brand you are defending.
127. Cloudflare Radar. Context on an IP or ASN during a client incident.
128. Spamhaus. Reputation check on infrastructure tied to the incident.
129. Microsoft 365 Defender alerts export. Only with tenant admin consent.
130. Sigma mail rules. Detection content mapped to the client's mail logs.

## Network edge and monitoring

131. OPNsense. Firewall review or lab edge for a client site.
132. pfSense. Same.
133. ntopng. Flow visibility on a span the client provided.
134. Graylog. Log pipeline for a small SOC retainer.
135. Grafana Loki. Log store beside metrics they already run.
136. Prometheus. Metrics for the security stack itself.
137. Uptime Kuma. Availability checks on services in scope.
138. NetBox. Source of truth for assets found in the assessment.
139. GLPI. Asset and ticket tracking for an SMB retainer.
140. Shuffle. SOAR playbooks on alerts the client already collects.

## Forensics, hunting, and backup

141. OpenCTI. Threat-intel knowledge graph for a retainer.
142. DFIR-IRIS. Case system when TheHive is too heavy.
143. KAPE. Targeted collection from a Windows host the client imaged.
144. EZ Tools. Parse those artifacts in a lab.
145. Chainsaw. Hunt Windows event logs the client exported.
146. Hayabusa. Sigma-based timeline of those logs.
147. Plaso. Super-timeline of a disk image they handed over.
148. Restic. Backup of engagement evidence, encrypted, client-held keys.
149. BorgBackup. Same.
150. GoPhish. Phishing simulation only against staff the client listed in writing.

## How this maps to Bleach Security

- Integrate: CloudQuery, NetBox, GLPI, Fleet, osquery.
- Assess: OpenVAS, Lynis, OpenSCAP, ScubaGear, Maester, Gitleaks, Sift.
- Fix: DefectDojo and Faraday track the guided remediation. This catalog does not auto-remediate.
- Continuous protection: CrowdSec, Fail2ban, Graylog, Loki, Shuffle, parsedmarc, OpenCTI.
- Compliance evidence: OpenSCAP, ScubaGear, Maester, DefectDojo exports.

Practice ranges stay the same: Hack The Box, TryHackMe, PortSwigger Academy, VulnHub. They are not client targets.
