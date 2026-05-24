#### CTI_Projects
Levels of Threat Intelligence

| Level | Audience | Focus | Typical Output |
|---|---|---|---|
| Strategic Intelligence | Executives, boards, policymakers | Big-picture risks, business impact, geopolitical trends | Risk reports, executive briefings, threat landscape assessments |
| Operational Intelligence | Security managers, incident response leads | Specific campaigns, adversary operations, intent, and capability | Campaign analysis, threat actor tracking, attack timelines |
| Tactical Intelligence | SOC analysts, defenders | TTPs (Tactics, Techniques, and Procedures) used by attackers | Detection guidance, MITRE ATT&CK mappings, defensive recommendations |
| Technical Intelligence (often added separately) | Security tools and automation systems | Atomic indicators and machine-readable data | IPs, hashes, domains, YARA/Sigma rules, IOC feeds |

A common way to think about them:

  - Strategic = Why should leadership care?
  - Operational = What are attackers planning or running?
  - Tactical = How do attackers behave?
  - Technical = What exact indicators can we block or detect?

These levels align closely with frameworks like MITRE ATT&CK and intelligence lifecycle models used in enterprise security, military intelligence, and government cyber defense programs.

---
#### Diamond Model

The Diamond model is a threat intelligence framework used to analyse and model cyber intrusions by examining the relationships among adversaries, capabilities, infrastructure, and victims.

| Diamond Model Component | Description | Example |
|---|---|---|
| Adversary | The threat actor or group responsible for the activity | APT29, cybercriminal group, insider threat |
| Capability | The tools, malware, exploits, or techniques used by the adversary | Phishing kit, ransomware, PowerShell scripts, zero-day exploit |
| Infrastructure | The systems or resources used to deliver or support the attack | Command-and-control (C2) servers, malicious domains, VPS hosting, email servers |
| Victim | The target of the attack | Organization, employee, government agency, industrial control system |

#### *Meta-Features Often Associated with the Diamond Model*

| Meta-Feature | Description |
|---|---|
| Timestamp | When the activity occurred |
| Phase | Stage of the intrusion lifecycle or attack campaign |
| Result | Outcome or impact of the activity |
| Direction | Relationship between attacker and victim |
| Methodology | Techniques or procedures used during the attack |

#### *Example Mapping*

| Component | Example Scenario |
|---|---|
| Adversary | FIN7 |
| Capability | Malicious Microsoft Office macro delivering malware |
| Infrastructure | hxxp://malicious-update.com |
| Victim | Financial department employee at a retail company |

---

#### *Cyber Kill Chain vs Cyber Defence Model*


#### *Overview*

This project maps the **Cyber Kill Chain (attacker lifecycle model)** against the **defensive strategy model** used in cybersecurity operations.

The goal is to translate theoretical frameworks into **SOC-relevant defensive actions**, showing how analysts can detect, disrupt, and respond to adversary activity across the attack lifecycle.

> Note: This is not a hacking or offensive guide. “Destroy” in this context refers to eradication and recovery within the defender’s environment only.

---

#### Cyber Kill Chain vs Defence Model Mapping

| Cyber Kill Chain Phase | Attacker Objective |  Defensive Control | SOC / CTI Interpretation |
|------------------|-------------------|----------------------|---------------------------|
| Reconnaissance | Gather information about targets | **Detect** | Identify scanning, OSINT activity, anomalous enumeration, and threat intelligence matches via SIEM/EDR/cloud logs |
| Weaponization | Build or prepare exploit payloads | **Deceive** | Deploy honeypots, canary tokens, decoy services, and fake assets to mislead attacker preparation |
| Delivery | Transmit malicious payload | **Deny** | Block malicious emails, URLs, files, and downloads using email gateways, proxies, firewalls, and web filters |
| Exploitation | Trigger vulnerability exploitation | **Disrupt** | Prevent exploitation via patching, EDR exploit mitigation, sandboxing, and runtime protection |
| Installation | Establish persistence | **Degrade** | Limit attacker capability using least privilege, application control, endpoint protection, and containment policies |
| Command & Control (C2) | Maintain remote access | **Disrupt / Deny** | Detect and block beaconing, DNS tunneling, proxy abuse, and outbound C2 communication |
| Actions on Objectives | Achieve final goal (exfiltration, sabotage, etc.) | **Destroy** | Eradicate attacker presence through host isolation, credential resets, session revocation, malware removal, and system recovery |

---

#### Key Interpretation Notes

#### 1. Kill Chain Perspective
The Cyber Kill Chain represents the **attacker’s lifecycle**, helping defenders understand the progression of an intrusion.

#### 2. Defensive Perspective
The 6Ds represent **defensive interventions** that aim to interrupt attacker progress at each stage.

#### 3. SOC Reality Mapping
In a real SOC environment, these models are applied using:
- SIEM platforms (e.g., Splunk, Microsoft Sentinel)
- EDR solutions (e.g., Microsoft Defender for Endpoint)
- Threat intelligence feeds (IOC + TTP enrichment)
- Incident response playbooks

---

#### Important Clarification: “Destroy” in SOC Context

The term **“Destroy” does NOT refer to offensive cyber operations or hacking back**.

In enterprise security operations, it means:
- Removing malware and persistence mechanisms
- Reimaging or restoring compromised systems
- Revoking credentials and access tokens
- Restoring systems from known-good backups

All actions remain within the **defender’s authorized environment and legal scope**.

---

#### Why This Matters

This mapping helps SOC and CTI practitioners:
- Understand attacker progression

---

#### OODA
```
flowchart LR
    A[Observe] --> B[Orient]
    B --> C[Decide]
    C --> D[Act]
    D --> A
```


































- Align detection engineering with attack stages
- Improve response speed and decision-making
- Translate threat intelligence into actionable defense

