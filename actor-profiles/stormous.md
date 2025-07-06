# Threat Actor Profile: STORMOUS

> ⚠️ **Note**: This profile is created for practice and learning purposes using publicly available information. No live infrastructure, identifiers, or sensitive data is included.

---

## 1. Summary
Stormous is a ransomware/extortion group that started showing activity in early 2022. The group is known for posting polls to select future targets and leaking stolen data through Telegram and other channels. Their claims are not always verified, but they have gained attention for their bold announcements and collaborations.

---

## 2. Motivation & Targeting
They seem to be financially motivated, using a ransomware-as-a-service (RaaS) model. While they target a mix of global organizations, reports and some behavior suggest interest in regions like the Middle East, India, and Europe. Some sources suggest a possible pro-Russian stance, but this remains unconfirmed.

---

## 3. Known Operations (Self-Claimed)
- **July 2023** – Claimed to have leaked internal data from **Epic Games**.
- **July 2023** – Announced joint attacks on **Cuba**, in collaboration with another actor called GhostLocker.
- **March 7, 2024** – Posted data from a reported breach of **Duvel Beer**.
- **May 2024** – Claimed breach of a **UAE-based government organization**, possibly linked to poll results.

These claims were posted by the group itself and haven't been publicly verified by third-party security companies.

---

## 4. Attribution & Language
There's no confirmed identity of the group or its members. Based on communication patterns and language in their posts, CloudSEK suggested the group might be Arabic-speaking. Some reports connect them loosely with pro-Russian motives, but none of this is confirmed.

---

## 5. TTPs (How They Operate - Inferred)
Exact tools used by Stormous are not known, but based on typical extortion behavior and patterns seen in similar groups, the following techniques are likely:

- `T1566.002` – Phishing links (Initial Access)
- `T1486` – File encryption (Impact)
- `T1041` – Data exfiltration over web channels (Exfiltration)
- `T1105` – File transfer (Command and Control)

These are inferred using the MITRE ATT&CK framework.

---

## 6. Infrastructure Overview (No Links Included)
- Public leak site (onion address not listed here)
- Telegram channel for updates and polls (handle redacted)
- Mostly Arabic language used in announcements, some English posts

---

## 7. Sources Used
- BleepingComputer (re: Coca-Cola incident)
- CloudSEK (on targeting and IOC observation)
- Ransomfeed (for activity logs)
- Public GitHub repos mentioning the actor

**Source Reliability**:  
Medium confidence – most of the group's activity is self-reported, so information should be considered with caution.

---

## Final Notes (Personal Commentary)
This profile is part of my learning journey into CTI. While Stormous is not widely analyzed in professional reports, studying them helped me understand how actor profiling, source validation, and behavior mapping work in real investigations.

---

📁 _Created as part of a personal OSINT project to practice cyber threat profiling using open data._
