# Student Combolist Leak

**Category:** Credential Dump / Combo List  
**Date Observed:** [Insert date]  
**Type:** Student emails + passwords  

## 🔍 Overview:
- Massive combolist containing student email IDs (mostly `.edu`) leaked via underground forum.
- List included:
  - Full email addresses
  - Passwords (in plaintext or weakly hashed)
  - Sometimes with school/university name

## 🔐 Source Behavior:
- Threat actor did not mention breach origin
- Shared combo in bulk (public post)
- Claimed data “good for internships, university emails, AWS EDU credits”

## 🧠 Inference:
- Likely gathered from infostealer logs or reused credentials across platforms
- Potential for:
  - Credential stuffing
  - Social engineering
  - Access to institutional accounts

## 🔧 Next Steps:
- Analyze samples with CrackStation or Hash-Identifier
- Cross-check domains in AbuseIPDB, VirusTotal
- Prepare hashes/IPs if reportable

## ⚠️ Caution:
May contain mixed fake + real records; always verify before reporting or actioning.

