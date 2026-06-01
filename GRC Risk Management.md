Risk Management within GRC is not a one-time event. It is a continuous cycle that never stops as long as the organization exists.
```bash
        IDENTIFY
       (What can go wrong?)
            ↓
        ASSESS
       (How bad? How likely?)
            ↓
        MITIGATE
       (What do we do about it?)
            ↓
        MONITOR
       (Is our response working?)
            ↓
      back to IDENTIFY
       (New risks emerged?)
```

## Phase 1 - Risk Identification

It means finding everything that could possibly go wrong — before it actually goes wrong. This is the most important phase. You cannot manage a risk you don't know exists.

```bash
INTERNAL RISKS                    EXTERNAL RISKS
──────────────                    ──────────────
Misconfigured systems             Hackers & cybercriminals
Untrained employees               Nation-state attackers
Weak passwords                    Natural disasters
Insider threats                   Vendor/supply chain attacks
Shadow IT (unauthorized apps)     New malware & zero-days
Poor patch management             Regulatory changes
```
methods used to identify risks are:

1. **Asset Inventory**: We cannot protect what we dont know we have.

   ```bash
   MediPay's assets:
        ├── Patient records database
        ├── Payment processing servers
        ├── Employee laptops (200 units)
        ├── Cloud storage (AWS)
        ├── Web application (patient portal)
        └── Third-party integrations (labs, pharmacies)
   ```
3. **Threat Modeling**: For each asset: "Who would want to attack this and how?"

   <table>
           <tr>
                   <th>Asset</th>
                   <th>Threat Actor</th>
                   <th>Attack Method</th>
           </tr>
           <tr>
                   <td>Patient database</td>
                   <td>Cyber Criminal</td>
                   <td>Ransomware</td>
           </tr>
           <tr>
                   <td>Payment server</td>
                   <td>Fraudster</td>
                   <td>Card skimming malware</td>
           </tr>
           <tr>
                   <td>Employee laptops</td>
                   <td>Insider</td>
                   <td>Data exfiltration</td>
           </tr>
           <tr>
                   <td>Web portal</td>
                   <td>Hacker</td>
                   <td>SQL injection</td>
           </tr>
           <tr>
                   <td>Cloud storage</td>
                   <td>Attacker</td>
                   <td>Misconfiguration exploit</td>
           </tr>
   </table>

3. **Vulnerability Scanning**: Use tools to find technical weakness:

   - **Nessus / OpenVAS**: scan systems for known vulnerabilities
   - **Nikto**: scan web applications
   - **Nmap**:  discover open ports and services

4. **Previous Incident Review**: Look at past security incidents — they reveal recurring risks.
5. **Staff Interview**: Talk to employees — they often know about risky processes that IT doesn't see.
6. **Compliance Gap Analysis**: Compare current state against framework requirements — gaps = risks.

## Phase 2 - Risk Assessment

Not all risks are equal. Assessment helps you figure out which risks to tackle first. There are 2 types of risk assessment:

- **Qualitative Assessment**: Uses descriptive labels — Low, Medium, High, Critical. Faster but less precise. Good for initial assessments.
- **Quantitative Assessment**: Uses actual numbers and financial values. More precise but takes longer. Used for high-stakes decisions.
