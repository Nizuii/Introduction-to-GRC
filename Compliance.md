# What is Compliance?

In cybersecurity compliance means making sure your organization handles data and systems in ways that meet laws and industry standards. Think of it like driving: there are traffic laws (speed limits, stop signs) that everyone must follow. If you break them you get fined. Cybersecurity compliance works the same way - Except the "traffic laws" are rules about how you protect peoples infrormation. It does matter because:
- **Legal penalties**: Fines, Lawsuits, even criminal charges.
- **Reputation**: Customers lose trust if you leak their data.
- **Business requirements**: Many partners won't work with you unless you're compliant

Now lets take a look at 3 big frameworks:

## 1. GDPR - General Data Protection Regulation

It is made by the European Union (EU), but it affects companies worldwide. It protects personal data of any citizens living or residing under EU. Here the core idea is people own their data. You can't just collect it, use it, or share it however you want. You need their permission and a good reason. The key rules are:

- **Consent**: You must clearly ask before collecting data. No pre-checked boxes buried in fine print.
- **Right to be forgotten**: People can demand you delete their data.
- **Data breach notification**: If you get hacked and personal data leaks, you must tell authorities within 72 hours.
- **Privacy by design**: Don't bolt on security later—build it in from the start.

**Real world example**: A fitness app tracks your running routes. Under GDPR, it must:

- Ask if it can collect your location
- Explain why it needs it
- Let you download all your data
- Let you delete your account and wipe your data
- Protect that route data so hackers can't see where you live

**Penalties**: Up to €20 million or 4% of global revenue (whichever is higher). Meta was fined over €1 billion for GDPR violations.

## 2. HIPAA — Health Insurance Portability and Accountability Act

It is made by the US government. Its main goal is to protect health information. Anything about your health, medical records, insurance, doctor visits, prescribtions, mental health notes etc... HIPAA should only be followed by companies that handle US patients data. The core idea is that your medical information is incredibly sensitive. It should be shared only with people who need it for your care, and it must be locked down tight. The key rules are:

- **Minimum necessary**: Staff should only access the minimum patient info needed for their job.
- **Access controls**: Strong passwords, role-based permissions (a billing clerk sees bills, not diagnoses).
- **Audit logs**: Track who looked at what record, when.
- **Encryption**: Scramble data so it's useless if stolen.
- **Business Associate Agreements (BAAs)**: If you hire a vendor to handle health data, they must also follow HIPAA.

**Real world example**: A hospital uses a cloud service to store X-rays. HIPAA requires:

- The cloud provider to sign a BAA
- The images to be encrypted
- Access logs showing which radiologist viewed which image
- Staff training so a receptionist can't browse celebrity patients' records

**Penalties**: Fines range from $100 to $50,000 per violation, up to $1.5 million per year for the same issue. Criminal charges possible for intentional misuse.

## 3. PCI-DSS - Payment Card Industry Data Security Standard

Unlike GDPR or HIPAA, it is not made by a government. It is an industry standard created by major credit card companies (Visa, Mastercard, Amex, Discover, JCB). Its main goal is to protect the card holder data like credit card numbers, expiration dates, security codes (CVV), PIN's. It should be followed by any organization that accepts, processes, stores, or transmits credit card payments. This includes:

- Online stores
- Restaurants with point-of-sale terminals
- Hotels
- Even small Etsy sellers using certain payment setups

**The core idea**: Credit card fraud hurts everyone. This standard makes sure companies handle card data safely. Key requirements are:

- **Firewalls**: Block unauthorized network access
- **No default passwords**: Change factory passwords on all systems
- **Protect stored card data**: If you must store it, encrypt it heavily (best practice: don't store it at all)
- **Encrypt data in transit**: Scramble card numbers when sending them over the internet
- **Anti-virus**: Keep malware protection updated
- **Secure Systems**: Regularly patch and update software
- **Restrict access**: Only need-to-know staff can access card data
- **Unique IDs**: Every user has their own login—no shared "admin/admin" accounts
- **Physical Security**: Lock up servers and paper records
- **Monitor networks**: Log and review all access to card data
- **Regular testing**: Run vulnerability scans and penetration tests
- **Policy Documentation**: Write down your security rules and train employees

**Real world example**: A coffee shop takes credit cards. PCI DSS requires:
- The payment terminal to be tamper-proof
- The shop's Wi-Fi to be separate from the payment network
- No writing card numbers on sticky notes
- Quarterly security scans by an approved vendor

**Penalties**: Fines from $5,000 to $100,000 per month by the card brands. Worse: you can lose the ability to accept credit cards entirely.
