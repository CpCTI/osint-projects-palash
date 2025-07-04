# Zivame.com – Credentials Exposure via Misconfigured Host

**Category:** Exposed Infrastructure  
**Date Observed:** [Insert date]  
**Target:** Zivame.com (Indian lingerie e-commerce)

---

## 🔍 Summary:
- A misconfigured server allowed public access to files containing what appeared to be internal credential sets.
- Dump included:
  - Username/password combinations
  - Email IDs from Zivame domains
  - Tokens in plaintext

## 🔬 Observations:
- Files were downloadable via direct path traversal
- No login/authentication required
- No captcha/rate-limiting visible

## 🔧 Tools Used:
- Manual enumeration
- HTTP response inspection
- Public search engine indexing (possible Google dorking)

## 🧠 Analyst Insight:
- This kind of exposed asset increases risk of:
  - Credential reuse attacks
  - Targeted phishing against Zivame employees or customers

## 📌 Recommendation:
- Zivame should rotate leaked credentials, audit systems, and secure endpoints
- Consider reporting via a responsible disclosure channel if not already known

