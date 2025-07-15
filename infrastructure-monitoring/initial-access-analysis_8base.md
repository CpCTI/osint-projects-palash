8Base Ransomware – Initial Access and TTP Profile

⚠️ This report is created for educational and research purposes using publicly available open-source intelligence. All information here is structured for defensive CTI skill-building and portfolio representation. No live infrastructure or sensitive indicators are included.

🧾 Overview

8Base is a ransomware and extortion group that surfaced publicly in May 2023. The group is known for performing double extortion attacks — encrypting systems while also stealing and threatening to leak victim data. Their ransom notes frame them as "pentesters" offering a recovery service, but their operations suggest otherwise.

Several analysts have noted code and operational similarities between 8Base and groups like Phobos and RansomHouse. A joint takedown in February 2025 reportedly disrupted infrastructure used by both 8Base and Phobos, raising the possibility of shared tooling or infrastructure.

🎯 Initial Access Techniques

8Base does not rely on a single technique for gaining entry. Instead, it uses a mix of known tactics seen across multiple ransomware families. Documented methods include:

Phishing Emails: Initial loaders or droppers are often delivered through email attachments. These emails mimic business themes such as invoices or HR messages.

Initial Access Brokers (IABs): 8Base appears to purchase access to already-compromised environments via stolen credentials or open RDP services. This is consistent with IAB-facilitated ransomware delivery.

SmokeLoader and Similar Malware: 8Base has been observed as a second-stage payload in infection chains involving SmokeLoader, indicating it may be delivered after initial compromise by other malware.

These delivery paths suggest that 8Base functions as a payload operator, not necessarily performing its own phishing or scanning — instead relying on third-party access sellers or loaders.

🧪 Post-Access Behavior

After successful compromise, 8Base ransomware typically:

Scans local and mapped drives

Locates data based on file extensions and path structures

Encrypts files using AES-256 encryption in CBC mode

Appends the .8base extension

Exfiltrates sensitive files to prepare for leak threats

The group operates a leak site (not linked here) where they publish stolen data from victims who refuse to pay.

🔁 Similarities with Other Threat Actors

Actor

Shared Behaviors / Tools

Phobos

Overlap in encryption logic and ransom note language; similar TTPs in access and post-exploitation

RansomHouse

Positioning themselves as 'ethical hackers'; double extortion format

BlackCat (ALPHV)

Both use data leak sites and show flexibility in payload delivery methods

These overlaps do not confirm attribution but hint toward shared infrastructure or recycled playbooks common in the ransomware-as-a-service ecosystem.

🎯 MITRE ATT&CK Technique Mapping

Tactic

Technique

Technique ID

Explanation

Initial Access

Phishing: Attachment

T1566.001

Emails with malicious attachments used to deliver loaders or malware

Initial Access

Valid Accounts

T1078

Use of credentials purchased via initial access brokers (IABs)

Execution

User Execution: Malicious File

T1204.002

Victim executes a malware-laced file, often from phishing

Defense Evasion

Process Injection

T1055

SmokeLoader or similar injects into legitimate processes

Exfiltration

Exfiltration Over C2 Channel

T1041

Data exfiltration via outbound encrypted channels

Impact

Data Encrypted for Impact

T1486

AES-256 encryption of files and renaming with .8base extension

These mappings are inferred from behavior seen in multiple 8Base campaigns across open-source reporting.


References

SentinelOne Blog on 8Base

TrendMicro Writeup

CloudSEK: 8Base Infrastructure Analysis

CISA Alerts (for TTP inference)
