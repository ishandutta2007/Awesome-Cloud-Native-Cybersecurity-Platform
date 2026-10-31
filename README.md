# Awesome-Cloud-Native-Cybersecurity-Platform

# Awesome-Cloud-Native-Cybersecurity-Platform

**Top Cloud Native Cybersecurity Platform (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on CNAPP, XDR, SIEM, Runtime Security & Self-Hosted Security Operations*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud-Native Cybersecurity**. These tools enable organizations to protect cloud workloads, detect runtime threats, correlate security events, and respond to incidents—from fully managed enterprise platforms with unified CNAPP/XDR capabilities to self-hosted scanners and SIEM stacks that give security teams complete control over their detection pipelines and data.



**Examples** include CrowdStrike Falcon, Palo Alto Cortex, SentinelOne Singularity, Microsoft Defender XDR, Trend Micro Vision One, Sophos Central, Fortinet FortiCloud, Check Point Infinity, Wiz, and Cisco Security Cloud (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted cloud-native security, runtime detection, and open SIEM infrastructure. **Critical note**: No single open-source project replicates the full scope of CrowdStrike Falcon or Palo Alto Cortex—which bundle endpoint, cloud, identity, and XDR into one platform. The open-source landscape is **composable**: **Wazuh** provides XDR/SIEM foundations, **Falco** dominates runtime detection, **Deepfence ThreatMapper** approximates CNAPP, and **Prowler** handles CSPM. You assemble the stack based on your gaps.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[CrowdStrike Falcon Platform](https://www.crowdstrike.com/)**

  **Unified cloud-native security platform** combining endpoint protection, cloud security (CNAPP), identity protection, and threat intelligence. Named the **most-mentioned MLOps platform in 2026 job listings** (for AI security context) and a **Customers' Choice in Gartner Peer Insights for ASPM Tools**. **Pricing**: Quote-only; enterprise contracts. **Free tier**: None. **Best for**: enterprises wanting a single platform for endpoint, cloud, and identity security with threat graph correlation—**trade-off**: premium pricing and ecosystem lock-in.



- **[Palo Alto Cortex](https://www.paloaltonetworks.com/cortex)**

  **AI-driven security operations platform** with XDR, XSIAM, and Xpanse (ASM). Named a **Leader in Forrester's ASM evaluation** . **Pricing**: Quote-only. **Free tier**: None. **Best for**: Palo Alto customers wanting unified SecOps with AI-driven analytics and automated response.



- **[SentinelOne Singularity](https://www.sentinelone.com/)**

  **AI-native security platform** with endpoint, cloud, and identity protection. Achieved **100% detection with no delays** in MITRE ATT&CK evaluations . **Pricing**: Quote-only; tiered by endpoint count. **Free tier**: None. **Best for**: organizations wanting autonomous endpoint and cloud protection with optional expert hunting augmentation.



- **[Microsoft Defender XDR](https://www.microsoft.com/en-us/security/business/microsoft-defender)**

  **Extended detection and response** integrated across Microsoft 365, Azure, and endpoints. **Pricing**: Included with Microsoft 365 E5 or Defender suites; quote-based. **Free tier**: Limited. **Best for**: Microsoft-centric organizations wanting native XDR without third-party agents—**trade-off**: Microsoft ecosystem dependency.



- **[Trend Micro Vision One](https://www.trendmicro.com/)**

  **XDR platform** with email, endpoint, server, cloud, and network detection. **Pricing**: Quote-only. **Free tier**: None. **Best for**: enterprises wanting broad coverage across email, endpoint, and cloud with a single vendor.



- **[Sophos Central](https://www.sophos.com/)**

  **Cloud-native security management** with endpoint, firewall, and email protection. **Pricing**: Quote-only. **Free tier**: Trial available. **Best for**: mid-market organizations wanting unified security management with a single console.



- **[Fortinet FortiCloud](https://www.fortinet.com/)**

  **Cloud security management** integrated with Fortinet Security Fabric. **Pricing**: Bundled with Fortinet subscriptions. **Free tier**: Limited. **Best for**: Fortinet customers wanting cloud management of FortiGate, FortiSandbox, and other fabric components.



- **[Check Point Infinity](https://www.checkpoint.com/)**

  **Consolidated security architecture** spanning network, cloud, endpoint, and mobile. **Pricing**: Quote-only. **Free tier**: None. **Best for**: enterprises wanting a unified security architecture from a single vendor.



- **[Wiz](https://www.wiz.io/)**

  **Cloud security platform** with a unified security graph correlating cloud infrastructure, workloads, identities, and code. **Pricing**: Quote-only; enterprise contracts. **Free tier**: None. **Best for**: cloud-native organizations wanting agentless discovery and risk correlation—**trade-off**: premium pricing.



- **[Cisco Security Cloud](https://www.cisco.com/)**

  **Unified security platform** integrating network, cloud, and endpoint security. **Pricing**: Quote-only. **Free tier**: None. **Best for**: Cisco-centric organizations wanting integrated security across their network and cloud infrastructure.



## Open-Source GitHub Projects



- **[Wazuh](https://github.com/wazuh/wazuh)**

  **Open Source Security Platform: Unified XDR and SIEM** (GPLv2) — **the most complete open-source XDR/SIEM foundation**, with ~15,900 GitHub stars and active development . **Features**: **Host intrusion detection** (FIM, rootkit detection, log analysis); **vulnerability detection**; **security configuration assessment** (CIS benchmarks); **incident response** (active response, quarantine); **regulatory compliance** (PCI DSS, HIPAA, GDPR, NIST); **cloud workload protection** for AWS, Azure, GCP; **container security** for Docker and Kubernetes. **Architecture**: Wazuh agent on endpoints, Wazuh manager for analysis, Wazuh indexer (OpenSearch fork) for storage, Wazuh dashboard for visualization . **Tech stack**: C, Python, OpenSearch. **Deploy**: Self-hosted (all-in-one or distributed). **Trade-off**: **Scalability limited in single-node deployments**—cluster mode required for larger environments. UI less mature than Splunk or Elastic . **Best for**: security teams wanting a free, open-source XDR/SIEM with broad endpoint and cloud coverage—willing to operate and tune the stack.



- **[Falco](https://github.com/falcosecurity/falco)**

  **Cloud-native runtime security** (Apache 2.0, CNCF Graduated) — **the de facto standard for container and Kubernetes runtime threat detection**, upstream for Sysdig Secure's behavioral detections . **Features**: **eBPF-based** monitoring of system calls across hosts, containers, and Kubernetes; **YAML rule engine** with out-of-the-box rules for container escapes, privilege escalation, and suspicious process execution; **50+ integrations** for forwarding alerts to SIEM, Slack, and data lakes; **gVisor support**; plugins for cloud services (AWS CloudTrail, GitHub, Okta). **Tech stack**: C++, Go. **Deploy**: Self-hosted (DaemonSet on Kubernetes, Helm chart). **Trade-off**: **Runtime detection only**—no posture management, vulnerability scanning, or SIEM correlation. Requires rule tuning and maintenance. **Best for**: teams needing runtime threat detection for Kubernetes and containers—the foundation of the runtime layer in any open-source cloud-native security stack .



- **[Deepfence ThreatMapper](https://github.com/deepfence/ThreatMapper)**

  **Open Source Cloud Native Application Protection Platform (CNAPP)** (Apache 2.0, ~5,320 stars) — **the closest single open-source project to a full CNAPP**, with runtime threat mapping and attack path analysis . **Features**: **Agentless and agent-based scanning** for hosts, containers, Kubernetes, and serverless; **vulnerability scanning** for images and workloads; **runtime threat detection** via eBPF; **secrets scanning**; **compliance posture** checks; **attack path visualization**—maps how vulnerabilities chain to sensitive data. **Tech stack**: TypeScript, Go, eBPF. **Deploy**: Self-hosted (Docker, Kubernetes). **Trade-off**: **Not a complete CNAPP**—lacks deep CIEM and full code-to-runtime correlation. Heavier than single-purpose scanners. **Best for**: teams wanting CNAPP-style visibility (vulnerability + runtime + attack paths) from one open-source project—without assembling five separate tools .



- **[Prowler](https://github.com/prowler-cloud/prowler)**

  **Open-source multi-cloud security posture management** (Apache 2.0) — **the most widely adopted open-source CSPM**, with hundreds of checks across AWS, Azure, GCP, Kubernetes, and Microsoft 365 . **Features**: Checks mapped to **CIS, NIST, PCI-DSS, GDPR, HIPAA, SOC 2, FedRAMP**; **IaC scanning** via Checkov integration; **Prowler Lighthouse** AI assistant for natural language queries; **GitHub Action** for CI/CD integration with SARIF upload . **Tech stack**: Python. **Deploy**: Self-hosted (CLI, Docker) or Prowler Cloud. **Trade-off**: **CSPM only**—no runtime detection or workload protection. Findings are lists, not graph-correlated attack paths. **Best for**: security teams wanting production-ready open-source CSPM with broad compliance coverage and CI/CD integration.



- **[Matano](https://github.com/matanolabs/matano)**

  **Open-source SIEM alternative for AWS** (Apache 2.0) — **the most scalable open-source SIEM architecture**, built around a security data lake in your AWS account . **Features**: **Security data lake** on Apache Iceberg tables in S3—**petabyte-scale retention at low cost**; **detection-as-code** in Python with Git-based lifecycle; **serverless** (Lambda, S3, SQS) with zero-ops scaling; **vendor-neutral**—data queryable from Athena, Snowflake, or any Iceberg-compatible tool. **Tech stack**: Rust, Python, AWS Lambda, Apache Iceberg. **Deploy**: Self-hosted (AWS account). **Trade-off**: **AWS-specific**—not multi-cloud. Newer project with limited community validation compared to Wazuh or Elastic. **Best for**: AWS-centric security teams wanting a cost-effective SIEM with open data formats and detection-as-code—without Splunk or Elastic licensing.



- **[Security Shallots](https://pypi.org/project/security-shallots/)**

  **Lightweight, self-hosted SIEM for small environments** (PyPI) — **the easiest open-source SIEM to deploy**, running on anything from a Raspberry Pi to a full server with just Python and SQLite . **Features**: **Ingests** Suricata, Syslog, pfSense, Wazuh, CrowdSec, Pi-hole, Argus agents, and web logs; **normalizes and deduplicates** alerts; **correlates patterns** (port scans, brute force, lateral movement); **groups into incidents** with response runbooks; **AI triage** via OpenAI/Anthropic API (optional); **hardware auto-detection**—adjusts profile based on available RAM/CPU. **Tech stack**: Python, SQLite. **Deploy**: `pip install` or one-line installer; Docker optional. **Trade-off**: **Small-scale focus**—not enterprise SIEM. SQLite storage limits retention at high volume. **Best for**: homelabs, small businesses, and branch offices wanting a functional SIEM without Elastic or Splunk infrastructure.



### Additional Strong Open-Source Options



- **Elastic Security** — SIEM and XDR on Elasticsearch (Elastic License, not OSI open source). 800+ ATT&CK rules, EQL for sequence detection, ML anomaly jobs (paid tiers) . **Note**: License changed from Apache 2.0; cloud costs unpredictable; complex to operate . **Best for**: teams already running ELK wanting security analytics with strong detection rules.

- **UTMStack** — Open-source SIEM and XDR (CISA-listed). Real-time correlation and threat intelligence with compliance reporting . **Note**: Smaller community than Wazuh; less documentation. **Best for**: organizations wanting an integrated SIEM/XDR with compliance focus.

- **Trivy** — Comprehensive scanner (Apache 2.0). Vulnerability, IaC, secrets, and SBOM scanning; CI/CD native . **Note**: Scanner only—pair with runtime and SIEM for full stack. **Best for**: shift-left security in CI/CD pipelines.

- **Kyverno** — Kubernetes admission controller (Apache 2.0). Policy enforcement via CRDs; signed-image verification via Sigstore . **Note**: Admission control only—not runtime detection or posture. **Best for**: enforcing security policies at the Kubernetes admission gate.



**Frameworks for building custom systems**: Combine **Wazuh** as the XDR/SIEM foundation with **Falco** for runtime detection, **Deepfence ThreatMapper** for CNAPP-style attack path analysis, **Prowler** for CSPM, and **Trivy** for shift-left scanning—creating a composable open-source cloud-native security stack. **None of these match CrowdStrike Falcon's unified threat graph or Palo Alto Cortex's AI-driven SecOps**; those require commercial platforms or significant integration engineering.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Cloud-native security platforms handling credentials and security telemetry must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls for security data.

- **The "unified platform" vs. "composable stack" distinction is critical.** **CrowdStrike, Palo Alto, SentinelOne, Microsoft Defender XDR, Trend Micro, Sophos, Fortinet, Check Point, Wiz, and Cisco** are **unified commercial platforms**—they bundle endpoint, cloud, identity, and XDR capabilities into one console. **Wazuh** provides **XDR/SIEM foundations**—host and cloud telemetry with detection and response, but not endpoint protection . **Falco** is **runtime detection**—Kubernetes and container threats, not endpoint or posture. **Deepfence ThreatMapper** approximates **CNAPP**—vulnerability, runtime, and attack paths . **Prowler** is **CSPM**—posture only. **No single open-source project replaces a commercial platform.** Compose the stack based on your gaps and operational capacity.

- **Wazuh is the strongest open-source foundation for XDR/SIEM**—broad endpoint and cloud coverage, compliance mapping, and active community (~15,900 stars) . **The trade-off**: single-node scalability is limited; UI is less polished than Splunk; requires tuning to avoid alert fatigue.

- **Falco is the runtime detection standard**—CNCF Graduated, eBPF-based, with 50+ integrations and upstream status for Sysdig Secure . **Pair it with Wazuh for host telemetry and Prowler for posture** to approximate a full CNAPP.

- **Deepfence ThreatMapper is the closest single-project CNAPP approximation**—vulnerability scanning, runtime eBPF detection, secrets scanning, and attack path visualization . **The trade-off**: CIEM depth is limited; heavier than single-purpose tools.

- **Matano is the most architecturally interesting open-source SIEM**—petabyte-scale data lake on Iceberg, detection-as-code, and vendor-neutral data ownership . **The trade-off**: AWS-specific; newer with limited validation. **For teams frustrated by Splunk/Elastic costs and wanting open data formats, it is the most promising path.**

- **Security Shallots is the pragmatic choice for small environments**—one-line install, SQLite storage, works on a Raspberry Pi . **The trade-off**: not enterprise-scale; SQLite limits retention.

- **Pricing opacity is universal across commercial vendors.** CrowdStrike, Palo Alto, SentinelOne, Microsoft, Trend Micro, Sophos, Fortinet, Check Point, Wiz, and Cisco all require sales contact. Wazuh, Falco, ThreatMapper, Prowler, and Matano are free open source. **Validate with direct vendor conversations against your endpoint count and cloud footprint.**

- Self-hosted open-source solutions require proper infrastructure (servers for Wazuh/Matano, Kubernetes for Falco/ThreatMapper), security hardening for detection credentials, and ongoing maintenance. **Security platforms have privileged access to your environment**—ensure your deployment meets your organization's security standards before connecting production systems.



---



**Made for security engineers, SOC teams, and organizations building transparent cloud-native cybersecurity solutions.**

Let's make Cloud-Native Cybersecurity Platforms more open, data-driven, and threat-aware.
