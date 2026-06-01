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

Applying STRIDE to each asset:

<table>
 <tr>
   <th>Asset</th>
   <th>STRIDE Threat</th>
   <th>Example</th>
 </tr>
 <tr>
   <td>Web Portal</td>
   <td>Spoofing</td>
   <td>Attacker logs in as a doctor using stolen credentials</td>
 </tr>
 <tr>
   <td>Patient Database</td>
   <td>Information Disclosure</td>
   <td>Unencrypted records leaked in a breach</td>
 </tr>
 <tr>
   <td>API Integration</td>
   <td>Tampering</td>
   <td>Attacker modifies lab results via unsecured API</td>
 </tr>
 <tr>
   <td>Mobile App</td>
   <td>Elevation of Privilege</td>
   <td>Nurse gains admin-level access through app bug</td>
 </tr>
 <tr>
   <td>Admin Console</td>
   <td>Spoofing + Elevation</td>
   <td>Attacker gains admin access, modifies system config</td>
 </tr>
 <tr>
   <td>Data Migration</td>
   <td>Tampering</td>
   <td>Records corrupted or stolen during migration process</td>
 </tr>
 <tr>
   <td>Cloud Infrastructure</td>
   <td>Denial of Service</td>
   <td>DDoS attack takes down EHR system hospital-wide</td>
 </tr>
 <tr>
   <td>Employee Accounts</td>
   <td>Spoofing</td>
   <td>Phishing attack steals staff credentials</td>
 </tr>
</table>

### 3. Risk Identification
Based on threat modeling, here are all identified risks:
<table>
 <tr>
  <th>Risk ID</th>
  <th>Risk Description</th>
  <th>Affected Asset</th>
  <th>Source</th>
 </tr>
 <tr>
  <td>R1</td>
  <td>Unauthorized access to patient records</td>
  <td>A2, A3</td>
  <td>External</td>
 </tr>
 <tr>
  <td>R2</td>
  <td>Ransomware encrypting cloud database</td>
  <td>A1, A2</td>
  <td>External</td>
 </tr>
 <tr>
  <td>R3</td>
  <td>Insecure API allowing data manipulation</td>
  <td>A5</td>
  <td>External</td>
 </tr>
 <tr>
  <td>R4</td>
  <td>Data breach during migration</td>
  <td>A7</td>
  <td>Internal/External</td>
 </tr>
 <tr>
  <td>R5</td>
  <td>Weak employee passwords / credential theft</td>
  <td>A8</td>
  <td>Internal/External</td>
 </tr>
 <tr>
  <td>R6</td>
  <td>Misconfigured AWS cloud storage (public bucket)</td>
  <td>A1, A2</td>
  <td>Internal</td>
 </tr>
 <tr>
  <td>R7</td>
  <td>Insider threat — employee stealing records</td>
  <td>A2, A3</td>
  <td>Internal</td>
 </tr>
 <tr>
  <td>R8</td>
  <td>Mobile app storing data insecurely on device</td>
  <td>A4</td>
  <td>Internal/External</td>
 </tr>
 <tr>
  <td>R9</td>
  <td>Mobile app storing data insecurely on device</td>
  <td>A1, A9</td>
  <td>External</td>
 </tr>
 <tr>
  <td>R10</td>
  <td>No disaster recovery — data loss after failure</td>
  <td>A10</td>
  <td>Internal</td>
 </tr>
 <tr>
  <td>R11</td>
  <td>Third party vendor compromise (supply chain)</td>
  <td>A5</td>
  <td>External</td>
 </tr>
 <tr>
  <td>R12</td>
  <td>Non-compliance with GDPR data residency rules</td>
  <td>A2</td>
  <td>Internal</td>
 </tr>
</table>

