# Email-Domain-Security-Audit
This project shows how EthernalSec evaluates whether attackers can send fake emails that appear to come from an organization. By reviewing SPF, DKIM, and DMARC records, the assessment identifies phishing and impersonation risk and provides clear steps to block fraudulent emails before they reach staff, donors, or customers.
# Email & Domain Security Audit

## What this project shows
This project demonstrates how EthernalSec evaluates whether a domain is protected against email spoofing, phishing, and impersonation.

Email fraud is one of the most common ways organizations lose money, accounts, and trust. This assessment checks whether attackers can send fake emails that appear to come from the organization.

---

## Why this matters
Without proper email authentication:
- Fake invoices get paid
- Donation scams succeed
- Password reset emails are spoofed
- Social media and bank accounts are taken over

This project shows how those risks are identified.

---

## What was performed
- Mail server discovery (MX)
- Sender Policy Framework (SPF) analysis
- DomainKeys Identified Mail (DKIM) checks
- Domain-based Message Authentication, Reporting & Conformance (DMARC) evaluation
- Risk interpretation and remediation guidance

All checks are passive and non-intrusive.

---

## Who this is for
- Churches
- Nonprofits
- Businesses
- Influencers
- Anyone who uses email

---

## Deliverables
- Client-style report → `docs/report.md`
- Remediation playbook → `docs/remediation-playbook.md`
- Evidence → `evidence/dns-records/`

---

## Ethics & Authorization
Only audit domains you own or have permission to review.  
This lab uses the public test domain `nmap.org`.
