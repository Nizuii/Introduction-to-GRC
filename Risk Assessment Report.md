# IT System Implementation: Risk Assessment Report

**Scenario**: HealthBridge India Pvt. Ltd. A healthcare company based in Bangalore planning to implement a new cloud-based Electronic Health Record (EHR) system to digitize all patient records across 15 hospital branches. What is changing is:
```bash
Current State                    New State
─────────────                    ─────────
Paper-based records         →    Cloud EHR system (AWS)
Local file servers          →    Centralized cloud database
Manual staff access         →    Role-based web portal access
No mobile access            →    Mobile app for doctors
Third-party lab integration →    API-based lab data exchange
```

Regulations they must comply with:

- IT Act 2000 (India)
- GDPR (some EU patients)
- HIPAA principles (best practice)
- ISO 27001 (company goal)

## GRC Governance Structure First

Before any risk assessment begins, Governance defines the boundaries.

```bash
RISK APPETITE STATEMENT
───────────────────────
"HealthBridge will accept LOW operational risks
 but will NOT accept any risk that exposes patient
 data or violates compliance obligations."

RISK ASSESSMENT OWNER: CISO — Arjun Menon
REVIEW FREQUENCY: Quarterly + after every major change
ESCALATION PATH: Risk Owner → CISO → Board
```

## RISK ASSESSMENT REPORT

**Organization**: HealthBridge India Pvt. Ltd.  
**Project**: Cloud EHR System Implementation  
**Report Date**: June 2026  
**Classification**: Confidential  
**Prepared by**: GRC & Information Security Team  

### 1. Asset Identification

```bash
ASSETS INTRODUCED BY THE NEW SYSTEM
─────────────────────────────────────
A1 — Cloud EHR Application (AWS hosted)
A2 — Patient Health Records Database
A3 — Doctor/Staff Web Portal
A4 — Mobile Application (iOS & Android)
A5 — API Integration (Labs, Pharmacies)
A6 — Admin Console (System configuration)
A7 — Data Migration Pipeline (old → new)
A8 — Employee Credentials & Access Accounts
A9 — Network Infrastructure (VPN, Firewall)
A10 — Backup & Disaster Recovery System
```

### 2. Threat Identification

Using STRIDE Threat Model — a structured way to identify threats:

```bash
S — Spoofing        (pretending to be someone else)
T — Tampering       (modifying data without authorization)
R — Repudiation     (denying you did something)
I — Information     (unauthorized data exposure)
    Disclosure
D — Denial of       (making system unavailable)
    Service
E — Elevation of    (gaining higher privileges than allowed)
    Privilege
```
