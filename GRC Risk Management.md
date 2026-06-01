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

### Qualitative Assessment — The Risk Matrix

Every risk is scored on two dimensions:
- **LIKELIHOOD** - How probable is this risk occuring?
- **IMPACT** - How damaging would it be if it occurs?

```bash
LIKELIHOOD
              Low      Medium      High
           ┌─────────┬─────────┬─────────┐
    High   │ MEDIUM  │  HIGH   │CRITICAL │
I          ├─────────┼─────────┼─────────┤
M Medium   │   LOW   │ MEDIUM  │  HIGH   │
P          ├─────────┼─────────┼─────────┤
A  Low     │   LOW   │   LOW   │ MEDIUM  │
C          └─────────┴─────────┴─────────┘
T
```

Applying this to thehospitals risk register:

<table>
        <tr>
                <th>ID</th>
                <th>Risk</th>
                <th>Likelihood</th>
                <th>Impact</th>
                <th>Rating</th>
        </tr>
        <tr>
                <td>R1</td>
                <td>Ransomware attack</td>
                <td>High</td>
                <td>High</td>
                <td>Critical</td>
        </tr>
        <tr>
                <td>R2</td>
                <td>Employee phishing</td>
                <td>High</td>
                <td>Medium</td>
                <td>High</td>
        </tr>
        <tr>
                <td>R3</td>
                <td>SQL injection</td>
                <td>Medium</td>
                <td>High</td>
                <td>High</td>
        </tr>
        <tr>
                <td>R4</td>
                <td>Insider data theft</td>
                <td>Low</td>
                <td>High</td>
                <td>Medium</td>
        </tr>
        <tr>
                <td>R5</td>
                <td>Unpatched servers</td>
                <td>High</td>
                <td>Medium</td>
                <td>High</td>
        </tr>
</table>

### Quantitative Assessment — ALE Formula

Used when we need to justify security spending to management. Key terms are:
- SLE = Single Loss Expectency (How much one incident costs).
- ARO = Annualized rate of occurrence (How much times per year it happens).
- ALE = Annualized Loss Expectancy (Total expected loss per year)

Formula: ALE x ARO.

Now lets take a real example for hospital:

```bash
Risk: Ransomware attack on patient database

SLE = ₹50,00,000  (cost of one ransomware incident
                   — recovery, downtime, fines)

ARO = 0.3         (30% chance it happens once per year)

ALE = ₹50,00,000 × 0.3
ALE = ₹15,00,000 per year
```
Now the hospital knows: "This risk costs us ₹15 lakhs per year on average." If a security solution costs ₹5 lakhs/year — it's clearly worth buying. This is how risk management justifies security budgets to CEOs.

## Phase 3 - Risk Mitigation

It means deciding what to do about each risk — and actually doing it. The 4 Risk Response Strategies are:

1. **MITIGATE** - Reduce the risk. Implement controls that lower likelihood or impact.
   
   ```bash
   Risk: Ransomware attack
        Mitigation controls:
                ├── Deploy EDR (Endpoint Detection & Response)
                ├── Enforce MFA on all accounts
                ├── Regular offline backups (3-2-1 rule)
                ├── Network segmentation
                └── Employee phishing awareness training
   ```
2. **Avoid** - Eliminate the risk entirely. Stop doing the risky activity altogether.
   
   ```bash
   Risk: Sensitive data stored in unencrypted spreadsheets
   Avoidance: Delete all spreadsheets, move to
           encrypted database — risk no longer exists
   ```

3. **Transfer** - Move the risk to someone else. Buy insurance or outsource the risky function.

   ```bash
   Risk: DDoS attack taking down payment portal
   Transfer: 
        ├── Buy cyber insurance (covers financial loss)
        └── Use Cloudflare DDoS protection (transfer
            technical burden to them)
   ```

4. **ACCEPT** - Live with the risk. Used when risk is low enough or too costly to fix.

   ```bash
   Risk: Old internal printer has a minor vulnerability
           Fix cost: ₹2,00,000
           Potential damage: ₹10,000
      
   Decision: Accept — not worth fixing.
           Document the decision formally.
   ```
