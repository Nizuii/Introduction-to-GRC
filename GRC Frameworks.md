# Understanding Common GRC Frameworks

Before understanding these frameworks lets first categorize them:

<table>
  <tr>
    <th>Category</th>
    <th>What It Answers</th>
    <th>Key Frameworks</th>
  </tr>
  <tr>
    <td>Enterprise Risk</td>
    <td>"What could go wrong across the whole business?"</td>
    <td>COSO ERM, ISO 31000</td>
  </tr>
  <tr>
    <td>Information Security</td>
    <td>"How do we protect data and systems?"</td>
    <td>ISO 27001, NIST CSF, NIST 800-53</td>
  </tr>
  <tr>
    <td>IT Governance</td>
    <td>"How do IT decisions support business goals?"</td>
    <td>COBIT</td>
  </tr>
  <tr>
    <td>Audit & Controls</td>
    <td>"Are we doing what we say we do?"</td>
    <td>COSO Internal Control</td>
  </tr>
</table>

These frameworks often overlap and complement each other. No single framework does everything.

## 1. COSO (Committee of Sponsoring Organizations).

COSO is about making sure an organization is honest, well-managed and not commiting fraud. It started in the finance/accounting world but expanded to enterprise risk management. COSO has 2 major models:

1. **COSO Internal Control Focuses on 5 components:**

   <table>
     <tr>
       <th>Component</th>
       <th>What it means</th>
     </tr>
     <tr>
       <td>Control Environment</td>
       <td>Culture & tone set by leadership</td>
     </tr>
     <tr>
       <td>Risk Assessment</td>
       <td>Identify and analyze risks</td>
     </tr>
     <tr>
       <td>Control Activities</td>
       <td>Policies and procedures to reduce risk</td>
     </tr>
     <tr>
       <td>Information & Communication</td>
       <td>Right info reaches right people</td>
     </tr>
     <tr>
       <td>Monitoring</td>
       <td>Continuously check if controls work</td>
     </tr>
   </table>

2. **COSO ERM - Enterprise Risk Management (2017) Expands to the full organization's strategy and covers:**

   - Strategy & Goal Setting
   - Identifying risks across the entire enterprise
   - Responding to risk
   - Reviewing and reporting
  
COSO is used by:
- Large corporations.
- Finance and accounting departments
- Organizations dealing with SOX (Sarbanes-Oxley Act) compliance

Real world example: "*A bank uses COSO ERM to identify the risk that a rogue employee could manipulate financial records. They put controls in place — like requiring two people to approve large transactions.*"

> COSO = Making sure the whole organization is managed with integrity and risk-awareness.

## 2. NIST Cybersecurity Framework (NIST CSF)

**NIST** STANDS FOR **National Institute of Standards and Technology**. It is a flexible, plain-English guide for any organization to manage cybersecurity risks. It is the most widely used cybersecurity framework in the world. NIST CSF is built around 6 core functions:

```bash
GOVERN → IDENTIFY → PROTECT → DETECT → RESPOND → RECOVER
```
Lets break each down:

<table>
  <tr>
    <th>Function</th>
    <th>Question it answers</th>
    <th>Example activity</th>
  </tr>
  <tr>
    <td>Govern</td>
    <td>Who is responsible for cybersecurity decisions?</td>
    <td>Create security policies, assign roles.</td>
  </tr>
  <tr>
    <td>Identify</td>
    <td>What assets do we have and what are the risks?</td>
    <td>Asset inventory, risk assessment</td>
  </tr>
  <tr>
    <td>Protect</td>
    <td>How do we stop attacks from happening?</td>
    <td>Firewalls, MFA, access controls</td>
  </tr>
  <tr>
    <td>Detect</td>
    <td>How do we know when something bad is happening?</td>
    <td>SIEM, intrusion detection systems</td>
  </tr>
  <tr>
    <td>Respond</td>
    <td>What do we do when an attack happens?</td>
    <td>Incident response plans</td>
  </tr>
  <tr>
    <td>Recover</td>
    <td>How do we get back to normal after an attack?</td>
    <td>Backups, disaster recovery</td>
  </tr>
</table>

Lets look at a real worl example of a hospital that uses NIST CSF:
- **Identify**: Lists all medical devices and patient databases
- **Protect**: Encrypts patient records, enforces MFA
- **Detect:** Sets up a SOC that monitors network traffic 24/7
- **Respond:** Has an IR team ready when ransomware is detected
- **Recover:** Restores from clean backups within 4 hours

## 3. NIST SP 800-53 
NIST SP 800-53 is basically a giant catalog of security controls. Think of it as a checklist of specific things you can do to protect a computer system or network. The U.S. government needed a standard way to secure all its IT systems. So NIST built this document to say, "Here are all the security measures you should consider." It's grouped into "families" of related controls. A few examples:

<table>
  <tr>
    <th>Family</th>
    <th>What it covers</th>
  </tr>
  <tr>
    <td>AC (Access Control)</td>
    <td>Who can log in, what they can access</td>
  </tr>
  <tr>
    <td>AU (Audit)</td>
    <td>Logging what happens on the system</td>
  </tr>
  <tr>
    <td>CM (Configuration Management)</td>
    <td>Keeping systems properly configured</td>
  </tr>
  <tr>
    <td>IA (Identification & Authentication)</td>
    <td>Passwords, multi-factor auth, etc.</td>
  </tr>
  <tr>
    <td>RA (Risk Assessment)</td>
    <td>Finding and evaluating risks</td>
  </tr>
  <tr>
    <td>SC (System & Communications Protection)</td>
    <td>Encryption, firewalls, network security</td>
  </tr>
</table>

Not every system needs every control. SP 800-53 defines three tiers:

- Low impact systems → fewer controls
- Moderate impact systems → more controls
- High impact systems → the full set

If NIST CSF is the strategy ("we need to protect our data"), SP 800-53 is the tactics ("here are the 200+ specific things we can do").
