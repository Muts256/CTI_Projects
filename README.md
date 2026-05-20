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
