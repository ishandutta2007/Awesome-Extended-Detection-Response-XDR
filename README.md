# Awesome-Extended-Detection-Response-XDR

# Awesome Extended Detection & Response (XDR)

> A curated list of top Extended Detection and Response (XDR) platforms — both SaaS/Hosted commercial solutions and open-source alternatives for unified security telemetry correlation and response.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [CrowdStrike Falcon Insight XDR](#crowdstrike-falcon-insight-xdr)
  - [Palo Alto Cortex XDR](#palo-alto-cortex-xdr)
  - [SentinelOne Singularity XDR](#sentinelone-singularity-xdr)
  - [Microsoft Defender XDR](#microsoft-defender-xdr)
  - [Trend Micro Vision One](#trend-micro-vision-one)
  - [Sophos XDR](#sophos-xdr)
  - [Cynet 360](#cynet-360)
  - [Cisco XDR](#cisco-xdr)
  - [Trellix XDR](#trellix-xdr)
  - [Elastic Security](#elastic-security)
- [Open-Source Software](#-open-source-software)
  - [Wazuh](#wazuh)
  - [UTMStack](#utmstack)
  - [Matano](#matano)
  - [Apache Metron](#apache-metron)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted XDR platforms. These are not open-source but are included as reference points for feature comparison.

### CrowdStrike Falcon Insight XDR
**Type:** AI-native XDR with endpoint, identity, cloud, and mobile telemetry  
Unifies EDR with identity, cloud, and mobile signals into a single console. Key capabilities include Charlotte AI for automated investigation leads, Falcon Fusion native SOAR for automated response, and Real Time Response (RTR) for direct system access. Offers 10 GB/day of free third-party data ingest. Vendor-reported results include 95% reduction in mean time to respond (from 4 hours to under 10 minutes) and 100% detection with zero false positives in SE Labs ransomware testing [citation:1][citation:12].  
**Best for:** Organizations wanting an AI-driven, adversary-focused XDR deeply integrated with threat intelligence and managed hunting options.

### Palo Alto Cortex XDR
**Type:** XDR with agentic AI and endpoint governance  
Cortex XDR 6.0 introduced app control with binary inventory and execution guardrails, plus Runtime Protection and AI Detection & Response (AIDR) for monitoring AI agent activity across desktop and coding environments. A targeted sensor deployment model allows running Cortex modules alongside existing third-party EDRs. The platform also includes a fleet of specialized AI agents for triage, enrichment, and containment, with human-in-the-loop approval for impactful actions [citation:2][citation:13].  
**Best for:** Enterprises in the Palo Alto ecosystem seeking advanced AI agent security and gradual platform consolidation.

### SentinelOne Singularity XDR
**Type:** Native and open XDR with cross-surface correlation  
Ingests and normalizes data across endpoint, identity, cloud, AI systems, and third-party tools into a single correlated view. Purple AI surfaces actionable insights, and automated workflows contain threats in seconds. Recognized as a Leader in IDC MarketScape for XDR, with 100% detection accuracy and 88% less noise than the median vendor in MITRE ATT&CK evaluations [citation:3][citation:14].  
**Best for:** Teams wanting native endpoint protection with open third-party integrations and AI-driven prioritization.

### Microsoft Defender XDR
**Type:** Unified pre- and post-breach defense suite  
Coordinates natively across Defender for Endpoint, Office 365, Identity, Cloud Apps, Vulnerability Management, and Threat Intelligence. Related alerts are automatically grouped into a single incident, and automatic threat response shares detections across products (e.g., blocking a malicious file across email and endpoints). Deep integration with Microsoft Sentinel for SIEM and Security Exposure Management [citation:4][citation:15].  
**Best for:** Microsoft-centric organizations wanting native XDR tightly coupled with M365 and Azure security.

### Trend Micro Vision One
**Type:** XDR + Agentic SIEM + SOAR  
Combines XDR, Agentic SIEM, and Agentic SOAR with native sensors across endpoint (EDR), identity (ITDR), network (NDR), and email (EmDR). Trend Companion AI assists analysts with investigation and automation. In the 2024 MITRE ATT&CK Enterprise Evaluation, achieved 100% analysis coverage across all major steps (16/16) and 99% across all sub-steps (79/80) [citation:5].  
**Best for:** Organizations wanting an integrated SecOps platform with broad native sensor coverage and AI-assisted operations.

### Sophos XDR
**Type:** XDR with data lake and AI assistant  
Extends EDR with third-party integrations that feed data into Sophos Data Lake for querying and analysis. Threat Graph visualizes attack origins, propagation, and affected processes. Live Discover enables custom queries across endpoint, mobile, email, firewall, and cloud data. Sophos AI Assistant uses natural language prompts for security investigations [citation:6].  
**Best for:** Existing Sophos customers wanting to extend detection and response across their security stack.

### Cynet 360
**Type:** Unified XDR with MDR  
Integrates NGAV, EPP, EDR (Windows, Linux, Mac), NDR, and SIEM-like log analytics with MITRE ATT&CK-aligned detections in a single console. Extends to SaaS and cloud via SSPM, CSPM, and Cloud Detection & Response, plus External Attack Surface Management, email security, and identity threat detection (ITDR). Includes built-in SOAR playbooks and 24/7 CyOps MDR [citation:7].  
**Best for:** Resource-constrained teams wanting comprehensive XDR with managed detection and response included.

### Cisco XDR
**Type:** Network-centric XDR with automation  
Ingests network telemetry from on-premises (NetFlow, SPAN, NGFW logs) and public clouds (AWS, GCP, Azure) via API integrations. Asset Insights unifies device and user inventory for incident context. Cisco XDR Automation provides no- to low-code workflows with drag-and-drop interface, triggered by incidents, schedules, or webhooks [citation:8].  
**Best for:** Cisco-centric networks wanting network telemetry-driven XDR and automation.

### Trellix XDR
**Type:** Open and native XDR  
Collects data from Trellix's native security controls and 1,000+ third-party sources into a data lake for correlation. Multi-vector, multi-vendor detection with threat intelligence from Trellix Advanced Research Center. Built-in playbooks automate remediation and response across SaaS and on-premises environments [citation:9].  
**Best for:** Organizations with heterogeneous security stacks wanting broad third-party data integration.

### Elastic Security
**Type:** XDR + SIEM + SOAR in one platform  
Native endpoint protection (Elastic Defend) with kernel-level sensors for Windows, Linux, macOS, and Kubernetes. Includes XDR, SIEM, and SOAR natively without per-endpoint fees. Agentic AI for automated triage, enrichment, case creation, and response. 400+ native and third-party integrations. Detection logic is publicly shared (open rules) [citation:10].  
**Best for:** Teams wanting XDR tightly integrated with SIEM and SOAR, with transparent detection logic and no per-endpoint pricing.

---

## 🟩 Open-Source Software

Self-hosted, community-driven XDR platforms. All listed projects offer source code you can deploy on your own infrastructure.

### Wazuh
**Stack:** C++ / OpenSearch | **License:** GPL-2.0  
A unified open-source XDR and SIEM platform with a lightweight agent, central manager, and OpenSearch-based indexer/dashboard. Capabilities include file integrity monitoring with who-data attribution, vulnerability detection via software inventory correlated against CVE databases, security configuration assessment against CIS benchmarks, rootkit detection, and 3,000+ built-in detection rules mapped to MITRE ATT&CK. Active response can trigger firewall updates, account lockouts, or endpoint isolation. Native cloud modules for AWS, Azure, and GCP. Pre-built compliance dashboards for PCI DSS, HIPAA, NIST 800-53, GDPR, and TSC. All features are included in the GPL binary with no feature gating [citation:16][citation:23][citation:29].  
**Best for:** Organizations wanting a comprehensive, truly open-source XDR/SIEM platform with full telemetry ownership and no per-agent fees.

### UTMStack
**Stack:** (Check repository) | **License:** Open Source  
An open-source platform merging SIEM and XDR with real-time log correlation and threat intelligence. Version 11.0.0 introduced EventProcessor (replacing Logstash) for improved performance and horizontal scalability, mandatory MFA, a modular plugin architecture, and SOC-AI with support for user-defined machine learning models. Includes SOAR workflows with visual rule editor and centralized management for multi-instance deployments [citation:20][citation:27].  
**Best for:** Teams wanting a unified SIEM + XDR + SOAR platform with AI-assisted analysis and enterprise-grade security controls.

### Matano
**Stack:** Rust / AWS (Lambda, S3, SQS) | **License:** Apache 2.0  
A serverless security data lake and SIEM alternative for AWS. Ingests security logs from various sources, stores them in Apache Iceberg tables in S3, and enables Python-based detection-as-code for real-time alerting. All data is stored in open formats queryable from Athena, Snowflake, or other tools without vendor lock-in. Fully serverless with zero-ops and elastic scaling [citation:21].  
**Best for:** AWS-centric teams wanting a cost-effective, open-format security data platform with detection-as-code.

### Apache Metron
**Stack:** Apache Storm / Hadoop ecosystem | **License:** Apache 2.0  
Integrates big data technologies for security monitoring: log aggregation, full packet capture indexing, storage, advanced behavioral analytics, and data enrichment with threat intelligence. Uses Apache Storm for stream processing and supports machine learning models for anomaly detection via Model-as-a-Service. Provides a centralized interface for alert summaries with threat intelligence context [citation:22].  
**Best for:** Organizations with existing Hadoop/Storm infrastructure wanting a scalable, big-data-driven security analytics platform.

---

## 📊 Comparison at a Glance

| Software | License | Type | Native EDR | Open Data Format | Best For |
|----------|---------|------|------------|------------------|----------|
| **Falcon Insight XDR** | Proprietary | AI-native XDR | ✅ | Limited | CrowdStrike ecosystem |
| **Cortex XDR** | Proprietary | Agentic XDR | ✅ | Limited | AI agent security |
| **Singularity XDR** | Proprietary | Native + open XDR | ✅ | Limited | Cross-surface correlation |
| **Defender XDR** | Proprietary | Unified suite | ✅ | Limited | Microsoft ecosystem |
| **Vision One** | Proprietary | XDR + SIEM + SOAR | ✅ | Limited | Broad native sensors |
| **Sophos XDR** | Proprietary | XDR + data lake | ✅ | Limited | Sophos ecosystem |
| **Cynet 360** | Proprietary | Unified XDR + MDR | ✅ | Limited | Managed detection included |
| **Cisco XDR** | Proprietary | Network-centric XDR | Limited | Limited | Network telemetry |
| **Trellix XDR** | Proprietary | Open XDR | ✅ | Limited | Multi-vendor integration |
| **Elastic Security** | Proprietary | XDR + SIEM + SOAR | ✅ | Limited | Transparent detection logic |
| **Wazuh** | GPL-2.0 | XDR + SIEM | ✅ | ✅ OpenSearch | Full OSS telemetry ownership |
| **UTMStack** | Open Source | SIEM + XDR + SOAR | (Check) | (Check) | Unified OSS SecOps |
| **Matano** | Apache 2.0 | Security data lake | ❌ | ✅ Apache Iceberg | AWS serverless data lake |
| **Apache Metron** | Apache 2.0 | Big data security analytics | ❌ | Hadoop ecosystem | Hadoop/Storm environments |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source XDR platform that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
