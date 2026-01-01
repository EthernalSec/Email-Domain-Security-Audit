# Email & Domain Security Report — Client Version (Lab)

## Executive Summary
The domain was evaluated for protection against email spoofing and phishing. The assessment found that key email authentication controls are missing or weak, allowing attackers to impersonate the organization and send fraudulent emails.

This exposes the organization to financial fraud, account takeover, and reputational damage.

---

## Scope
Domain: nmap.org  
Testing: DNS-based email authentication review

---

## Findings

### 1) SPF is configured but not enforced
**Risk:** Medium  
**Why it matters:** Soft-fail SPF allows spoofed emails to still be delivered.

**Observed:** SPF record ends in `~all`  
**Fix:** Change to `-all` after validation.

---

### 2) DKIM is missing
**Risk:** High  
**Why it matters:** Without DKIM, email is not cryptographically signed, making spoofing easy.

**Observed:** No DKIM record for Google  
**Fix:** Enable DKIM in Google Workspace and publish DNS key.

---

### 3) DMARC is missing
**Risk:** Critical  
**Why it matters:** Without DMARC, providers do not block fake emails even when SPF/DKIM fail.

**Observed:** No `_dmarc` record  
**Fix:** Add DMARC policy with reporting and enforcement.

---

## Overall Risk
**High risk of phishing, impersonation, and fraud.**

---

## Evidence
DNS results stored in `evidence/dns-records/`
