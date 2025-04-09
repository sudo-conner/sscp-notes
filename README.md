# SSCP Study Notes

Notes I used while studying for ISC2 Systems Security Certified Practitioner. 

*These notes don't cover everything you need to know to take the test, these are just some of the things I wanted to write down to review again.*

## Table of Contents

1. [ISC2 Code of Ethics Four Canons](#isc2-code-of-ethics-four-canons)
2. [CIANA+PS Security Principles](#cianaps-security-principles)
3. [SOC 1 vs. SOC 2 (Service Organization Controls)](#soc-1-vs-soc-2-service-organization-controls)
4. [FISMA & PCI DSS](#fisma--pci-dss)
5. [Software Licenses](#software-licenses)
6. [Legal Stuff](#legal-stuff)
7. [Access Controls](#access-controls)
8. [Biometric Metrics](#biometric-metrics)
9. [Account Provisioning](#account-provisioning)
10. [Active Directory Trusts](#active-directory-trusts)
11. [Federation vs. Single Sign-On (SSO)](#federation-vs-single-sign-on-sso)
12. [SAML, SOAP, SPML, XACML](#saml-soap-spml-xacml)
13. [Comparison of RADIUS, TACACS+, and Kerberos](#comparison-of-radius-tacacs-and-kerberos)
14. [Firewall Comparison](#firewall-comparison)
15. [STRIDE Threat Assessment Framework](#stride-threat-assessment-framework)
16. [Quantitative vs. Qualitative Risk Analysis](#quantitative-vs-qualitative-risk-analysis)
17. [Disaster Recovery Test Types](#disaster-recovery-test-types)
18. [Recovery Metrics](#recovery-metrics)
19. [RAID (Redundant Array of Independent Disks)](#raid-redundant-array-of-independent-disks)
20. [Backup Types](#backup-types)
21. [DES Modes of Operation](#des-modes-of-operation)
22. [3DES (Triple Data Encryption Standard)](#3des-triple-data-encryption-standard)
23. [RC4 (Rivest Cipher 4)](#rc4-rivest-cipher-4)
24. [AES (Advanced Encryption Standard)](#aes-advanced-encryption-standard)
25. [RSA (Rivest-Shamir-Adleman)](#rsa-rivest-shamir-adleman)
26. [ECC (Elliptic Curve Cryptography)](#ecc-elliptic-curve-cryptography)
27. [Diffie-Hellman (DH)](#diffie-hellman-dh)
28. [Symmetric vs. Asymmetric Cryptography](#symmetric-vs-asymmetric-cryptography)
29. [Asymmetric Cryptography](#asymmetric-cryptography)
30. [Cloud Service Models](#cloud-service-models)

## ISC2 Code of Ethics Four Canons

### Protect society, the common good, necessary public trust, and confidence
- Prioritize the security and safety of people and organizations
- Promote responsible and ethical cybersecurity practices

### Act honorably, honestly, justly, responsibly, and legally
- Maintain integrity and uphold professional standards
- Follow laws, policies, and ethical guidelines in all actions

### Provide diligent and competent service to principals
- Serve clients, employers, and the public with professionalism
- Continuously improve skills and knowledge to perform duties effectively

### Advance and protect the profession
- Support the development of cybersecurity as a respected profession
- Mentor, educate, and contribute to ethical cybersecurity practices

## CIANA+PS Security Principles

### Confidentiality  
- Ensures that **only authorized users** can access sensitive data
- Protects against **unauthorized disclosure**
- **Example:** Encryption is used to protect stored passwords

### Integrity
- Ensures that **data is accurate, complete, and unaltered**
- Protects against **modification, tampering, or corruption**
- **Example:** Checksums and hashing ensure that files have not been modified

### Availability
- Ensures that **systems, services, and data are accessible** when needed
- Protects against **downtime, denial-of-service (DoS) attacks, and hardware failures**
- **Example:** Redundant servers prevent service outages

### Non-Repudiation
- Ensures that a **user cannot deny** performing an action
- Uses **digital signatures and logging** to provide proof of actions taken
- **Example:** A signed email ensures the sender **cannot deny** sending it

### Accountability
- Ensures that **users are responsible for their actions** within a system
- Requires **audit logs, access controls, and user authentication**
- **Example:** Admin accounts are tracked through **audit logs**

### Privacy
- Ensures that **personal and sensitive data is collected, stored, and used responsibly**
- Protects users from **unauthorized access to their personal information**
- **Example:** GDPR and HIPAA regulations enforce strict **data privacy protections**

### Safety
- Ensures that **systems and policies protect human lives** and prevent harm
- Focuses on **physical security, fail-safes, and emergency response**
- **Example:** Industrial control systems in a power plant have **fail-safe mechanisms** to prevent accidents

### **Key Takeaways**
- **Confidentiality** → Prevents **unauthorized access**
- **Integrity** → Ensures **data accuracy and trustworthiness**
- **Availability** → Ensures **systems and services are operational**
- **Non-Repudiation** → Provides **proof of actions taken**
- **Accountability** → Tracks **who did what and when**
- **Privacy** → Protects **sensitive personal data**
- **Safety** → Protects **human life and physical systems**

## SOC 1 vs. SOC 2 (Service Organization Controls)

SOC (Service Organization Control) reports are **auditing standards** developed by the **AICPA (American Institute of Certified Public Accountants)** to assess the security and compliance of service providers.

### SOC 1 (Financial Reporting Controls)
- Focuses on **internal controls over financial reporting (ICFR)**
- Ensures that financial transactions and data processing **do not introduce risks to customers**
- **Example:** A payroll processing company (like ADP) undergoes a **SOC 1 audit** to ensure financial data integrity

### **SOC 2 (Security & Compliance Controls)**
- Focuses on **security, availability, processing integrity, confidentiality, and privacy**
- Ensures a company’s **IT systems** meet security and compliance standards
- **Example:** A cloud provider (like AWS or Google Cloud) undergoes a **SOC 2 audit** to prove it follows strong security controls

### **SOC 1 vs. SOC 2 Comparison**  
| **Aspect** | **SOC 1** | **SOC 2** |
|------------|-----------|-----------|
| **Purpose** | Financial reporting controls | IT security & compliance |
| **Focus** | Ensures accurate financial processing | Ensures secure handling of customer data |
| **Who Needs It?** | Banks, payroll processors, financial services | Cloud providers, SaaS companies, IT service providers |
| **Trust Principles** | Financial controls | Security, availability, confidentiality, privacy, processing integrity |

### **Key Takeaways**
- **SOC 1** → Focuses on **financial reporting accuracy**
- **SOC 2** → Focuses on **security and compliance of IT systems** 

## FISMA & PCI DSS

### FISMA (Federal Information Security Management Act)
- **US federal law** that mandates security requirements for government agencies and contractors
- Requires agencies to **develop, document, and implement** security controls
- Uses **NIST frameworks** to define security standards
- **Example:** A federal agency must follow **FISMA guidelines** to secure sensitive government data

### PCI DSS (Payment Card Industry Data Security Standard)
- **Industry standard** for protecting **credit card data**
- Applies to any organization that **stores, processes, or transmits** payment card information
- Requires controls like **encryption, access control, and vulnerability management**
- **Example:** A retail company must comply with **PCI DSS** to securely handle customer credit card transactions

## Legal Stuff

- **Testimonial Evidence**
  - Evidence provided by a witness under oath, usually in the form of spoken statements in court or during a legal proceeding

- **Parol Evidence Rule**
  - Principle that prevents parties in a contract dispute from introducing outside statements that contradict the final written agreement
  - If two parties enter written agreement, document is assumed to contain **all** rules of agreement

- **Best Evidence Rule**
  - Rule requiring that the original document, must be presented in court when the content of that document is disputed
  - Copies can't be used if originals are available

- **Hearsay Rule**
  - Rule that excludes second-hand statements from being used as evidence unless they fall under an exception

## Access Controls

### Rule-Based Access Control

- Access is determined by **predefined rules and conditions**
- Rules are based on **attributes like time, location, or device**
- **Example:** Employees can only access certain systems during business hours
- Often used in **firewalls, intrusion prevention systems, and network security**

### Role-Based Access Control (RBAC)

- Access is granted based on **user roles** within an organization
- Users inherit permissions based on their assigned role
- **Example:** A system admin role has access to network settings, while a regular user does not
- Common in **enterprise environments** where access is structured around job functions

### Resourse-Based/ Discretionary Access Control (DAC)

- **Resource owners** decide who has access to their files or systems
- Users can modify access permissions for resources they control
- **Example:** A user grants read/write permissions to another user for a shared document
- More **flexible but less secure** than non-discretionary models

### Non-Discretionary Access Control

- Centralized enforcement of security policies, typically managed by **system administrators**
- Includes **RBAC** and **mandatory access control (MAC)**
- Used in **high-security environments** where access must be strictly enforced

 ### Mandatory Access Control (MAC)
- Access is enforced by **a central authority based on security classifications**
- Users and resources are assigned **labels** (e.g., "Confidential," "Top Secret")
- **Users cannot modify access permissions** – only administrators can
- **Example:** Government and military systems where data access is based on security clearance levels
- Highly **secure but rigid**, making it less flexible for general use

## Biometric Metrics

### False Acceptance Rate (FAR)
- Probability that a biometric system **incorrectly** authenticates an **unauthorized** user
- Higher FAR means the system is more likely to allow **unauthorized** access

### False Rejection Rate (FRR)
- Probability that a biometric system **incorrectly** rejects an **authorized** user
- Higher FRR means **legitimate** users are more likely to be denied access

### Crossover Error Rate (CER)
- Point where the **FAR** and **FRR** are equal
- Used as a measure of a biometric system's accuracy
- Lower CER values indicate better system performance

### Equal Error Rate (ERR)
- Another term for **Crossover Error Rate (CER)**
- Used interchangeably in some contexts to describe the balance between false acceptances and false rejections

## Account Provisioning

### Discretionary Account Provisioning
- Manual process where an administrator grants access to accounts based on individual requests
- Prone to human error and inconsistent application of security policies

### Workflow-Based Account Provisioning
- Structured approach that follows predefined workflows for account creation, modification, and deletion
- Involves approvals and role-based access control to enforce security policies

### Automated Account Provisioning
- System-driven process that automatically creates, modifies, or removes accounts based on predefined rules and data from authoritative sources such as HR databases or identity management systems

### Self-Service Account Provisioning
- Allows users to request or create their own accounts with minimal administrative intervention
- Often requires identity verification and approval before granting access

## Active Directory Trusts

Trusts in Active Directory (AD) allow authentication between different domains, forests, or Kerberos realms

### Realm Trust
- Connects **AD with a non-Windows Kerberos v5 (K5) realm**
- **One-way or two-way**
- **Non-transitive** (applies only between the specified AD domain and Kerberos realm)
- Used for **integrating AD with UNIX-based Kerberos environments**

### External Trust
- Connects **two separate AD domains or forests that are not part of the same AD forest**
- **One-way or two-way**
- **Non-transitive** (trust applies only between the two specified domains)
- Used when **two organizations need authentication between AD domains**

### Forest Trust
- Connects **two entire AD forests**
- **One-way or two-way**
- **Transitive** (trust applies across all domains within both forests)
- Used when **organizations need authentication across all domains in separate forests**

### Parent-Child Trust
- Automatically created when a **new child domain is added to an existing AD domain**
- **Two-way by default**
- **Transitive** (trust applies up and down the hierarchy)
- Used when **an organization expands its AD structure with child domains**

### **Summary Table**  
| Trust Type        | Use Case | Direction | Transitivity |
|------------------|----------|-----------|-------------|
| **Realm Trust** | AD ↔ Non-Windows Kerberos | One-way or two-way | **Non-transitive** |
| **External Trust** | AD ↔ AD (separate forests) | One-way or two-way | **Non-transitive** |
| **Forest Trust** | Entire AD forest ↔ Another AD forest | One-way or two-way | **Transitive** |
| **Parent-Child Trust** | Parent AD domain ↔ Child AD domain | Two-way (default) | **Transitive** |

## Federation vs. Single Sign-On (SSO)

Federation and SSO are related but serve different purposes in authentication and identity management

### Single Sign-On (SSO)
- Allows a user to **log in once** and access multiple applications without re-entering credentials
- Works **within the same organization or domain**
- Managed by a **centralized identity provider (IdP)** (e.g., Microsoft Entra ID, Okta, Google Identity)
- **Example:** Logging into Google once and accessing Gmail, Drive, and YouTube

### Federation
- Enables authentication across **different organizations** without requiring separate accounts
- Establishes **trust relationships** between identity providers (IdPs) and service providers (SPs)
- Allows a user from one organization to access services in another using their home credentials
- **Example:** A university student logs into a library system from another university using their home institution’s login

### How Federation and SSO Work Together
- **Federation enables SSO across multiple organizations**
- **Example:** Using **SAML** to authenticate with a corporate identity provider (Microsoft Entra ID) and access multiple third-party services without re-entering credentials

### Key Takeaways
- **SSO** allows users to log in once and access multiple apps **within an organization**
- **Federation** enables authentication **between different organizations** (cross-domain SSO)
- Federation often **uses SSO**, but SSO alone **does not imply federation**
- **SAML, OAuth, and OpenID Connect** are common protocols for federated authentication

Federation and SSO improve **user experience, security, and centralized authentication** across different environments

## SAML, SOAP, SPML, XACML

### SAML (Security Assertion Markup Language)
- XML-based **authentication and authorization framework**
- Used for **Single Sign-On (SSO)** between identity providers (IdPs) and service providers (SPs)
- Common in **web-based authentication (e.g., logging into cloud apps with corporate credentials)**

### SOAP (Simple Object Access Protocol)
- **Messaging protocol** that allows applications to communicate over the internet using XML
- Used for **web services** and **secure API communications**
- Supports **encryption, authentication, and integrity** for transmitting structured data

### SPML (Service Provisioning Markup Language)
- XML-based framework for **automated user provisioning and deprovisioning**
- Used to **create, manage, and delete user accounts across multiple systems**
- Helps in **identity lifecycle management** for cloud and enterprise applications

### XACML (eXtensible Access Control Markup Language)
- XML-based **policy language for access control decisions**
- Defines **fine-grained permissions** for users and resources based on attributes
- Common in **role-based and attribute-based access control (RBAC/ABAC) systems**

### **Summary Table**  
| Standard | Purpose | Use Case |
|----------|---------|----------|
| **SAML** | Authentication & SSO | Logging into cloud apps using corporate credentials |
| **SOAP** | Secure web service communication | Sending encrypted API requests between applications |
| **SPML** | Automated user provisioning | Creating and managing user accounts across systems |
| **XACML** | Access control policies | Defining permissions for users and resources |

These standards help facilitate secure authentication, authorization, and identity management in enterprise and cloud environments

## Comparison of RADIUS, TACACS+, and Kerberos

| Feature       | RADIUS | TACACS+ | Kerberos |
|--------------|--------|---------|----------|
| **Protocol** | UDP | TCP | TCP |
| **Encryption** | Encrypts only passwords | Encrypts the entire payload | Uses ticket-based encryption |
| **Authentication Model** | Centralized authentication for network access | Centralized authentication for devices & commands | Ticket-based authentication (Single Sign-On) |
| **Usage** | Network access control (VPN, Wi-Fi) | Device administration (routers, switches) | Secure authentication for users & services |
| **Authentication, Authorization, Accounting (AAA)** | Combines authentication & authorization, separate accounting | Separates authentication, authorization, and accounting | Focuses on authentication only |
| **Best Used For** | Remote access and network authentication | Administrative access control | Secure login in enterprise environments |

### **Summary**
- **RADIUS**: Used for network authentication, operates over **UDP**, and encrypts only passwords
- **TACACS+**: Used for device administration, operates over **TCP**, and encrypts the entire payload
- **Kerberos**: Used for secure authentication via **tickets**, supports **Single Sign-On (SSO)**, and is commonly used in enterprise environments

## Firewall Comparison

| Firewall Type               | How It Works | Connection Tracking | State Tracking |
|-----------------------------|-------------|--------------------|---------------|
| **Static Packet Filtering** | Examines individual packets based on rules (IP, port, protocol) | Basic tracking based on IP, port, and protocol | No state awareness, treats each packet separately |
| **Stateful Inspection** | Tracks active connections and only allows expected packets in a session | Tracks active connections based on IP and port pairs | Tracks session states (e.g., established, closing) to prevent unexpected packets |
| **Application Level** | Acts as an intermediary, analyzing and relaying traffic at the application layer | Re-establishes connections between client and server | Deep state tracking at the application layer, ensures full session security |
| **Next-Generation Firewall (NGFW)** | Combines stateful inspection with deep packet inspection, IDS/IPS, and application awareness | Tracks connections across multiple layers, including user identity and application | Tracks session state across protocols, inspects packets for threats, and applies dynamic security policies |

## STRIDE Threat Assessment Framework

STRIDE is a **threat modeling framework** used to identify and categorize security threats in applications and systems

| **Threat Category** | **Description** | **Example Attack** |
|---------------------|----------------|---------------------|
| **Spoofing** | Impersonating a legitimate user or system | **Credential theft, IP spoofing** |
| **Tampering** | Modifying data in transit or at rest | **Altering database records, injecting malicious code** |
| **Repudiation** | Denying having performed an action | **User denies making a transaction, logs are erased** |
| **Information Disclosure** | Unauthorized access to sensitive data | **Data leaks, exposed API keys, eavesdropping** |
| **Denial of Service (DoS)** | Disrupting system availability | **DDoS attacks, resource exhaustion** |
| **Elevation of Privilege** | Gaining higher access than intended | **Privilege escalation, root access exploits** |

### How STRIDE is Used
- Helps identify **potential security risks** during system design
- Used in **threat modeling** to define **mitigation strategies**

STRIDE is widely used in **application security** and **network security** to proactively address threats before deployment

## Quantitative vs. Qualitative Risk Analysis

Risk analysis helps organizations assess security risks by using **quantitative (measurable) or qualitative (subjective) methods**.

### Quantitative Risk Analysis
- Uses **numerical values and financial metrics** to calculate risk
- Based on measurable factors such as **cost, probability, and impact**
- Often involves formulas like:
  - **Single Loss Expectancy (SLE) = Asset Value × Exposure Factor (EF)**
  - **Annualized Loss Expectancy (ALE) = SLE × Annualized Rate of Occurrence (ARO)**
- **Example:** Determining that a cyberattack could cause **$500,000 in annual losses**

### Qualitative Risk Analysis
- Uses **subjective assessments** instead of numerical data
- Risk is categorized as **high, medium, or low** based on expert judgment
- Commonly used when precise data is unavailable or impractical
- **Example:** Evaluating a security vulnerability as **high risk** due to potential reputational damage

## Disaster Recovery Test Types

### Checklist Review
- Simple review of disaster recovery plans, procedures, and resources to ensure they are accurate and up-to-date
- Usually the least disruptive and easiest to perform

### Tabletop Exercise
- Discussion-based exercise where team members review disaster scenarios and response plans in a structured meeting
- Focuses on coordination, decision-making, and identifying gaps in planning

### Parallel Test
- Test where backup systems are activated alongside live systems to verify that they can handle operations
- Ensures that backup systems work without disrupting the primary environment

### Full Interruption Test
- Hands-on test where teams simulate a real disaster scenario to validate the recovery process
- Involves physically executing recovery procedures without impacting actual operations

## Recovery Metrics

### Recovery Point Objective (RPO)
- Maximum acceptable data loss measured in time
- Determines how frequently backups should be taken

### Recovery Time Objective (RTO)
- Maximum time allowed to restore systems after a disruption
- Defines how quickly operations must resume to minimize impact

### Maximum Tolerable Downtime (MTD)
- Longest period a system or service can be unavailable before causing unacceptable damage
- Includes both RTO and additional time for full recovery

### Work Recovery Time (WRT)
- Time required after systems are restored to return business operations to normal
- Accounts for data validation, application testing, and user accessibility

### Mean Time Between Failures (MTBF)
- Average time between system failures
- Measures reliability and helps predict maintenance needs

### Mean Time to Repair (MTTR)
- Average time required to fix and restore a failed system
- Includes troubleshooting, repair, and system verification

### Single Loss Expectancy (SLE)
- Expected monetary loss from a single security incident
- Calculated as **Asset Value (AV) × Exposure Factor (EF)**

### Annualized Loss Expectancy (ALE)
- Estimated financial impact of a security risk over a year
- Calculated as **Single Loss Expectancy (SLE) × Annualized Rate of Occurrence (ARO)**

## RAID (Redundant Array of Independent Disks)

### RAID 0 (Striping)
- Data is split across multiple disks for **high performance**
- **No redundancy** – a single disk failure results in total data loss
- Used for **speed**, not fault tolerance

### RAID 1 (Mirroring)
- Data is duplicated across two disks for **high redundancy**
- If one disk fails, the other contains a full copy of the data
- Slower write speeds due to duplication but **strong fault tolerance**

### RAID 5 (Striping with Parity)
- Data is striped across multiple disks with **parity information** stored on each disk
- Can tolerate **one** disk failure by reconstructing lost data using parity
- Requires at least **three** disks and balances **speed, storage efficiency, and fault tolerance**

### RAID 10 (1+0, Mirrored Striping)
- Combines **RAID 1 (mirroring)** and **RAID 0 (striping)** for **speed and redundancy**
- Requires at least **four** disks and can survive multiple failures (as long as one disk in each mirrored pair survives)
- **Best for performance and reliability but uses more storage**

## Backup Types

### Full Backup
- Copies **all data** to the backup storage
- **Slowest backup**, but fastest to restore
- Requires **large storage space**
- Sets **Archive Bit** to 0

### Incremental Backup
- Backs up **only data that changed** since the last backup (full or incremental)
- **Fastest backup**, but slower to restore since multiple backups are needed
- Requires **less storage** than full or differential backups
- Sets **Archive Bit** to 0

### Differential Backup
- Backs up **all data changed since the last full backup**
- **Faster restore** than incremental (requires only the last full + latest differential)
- Takes **more storage** than incremental but less than full backups
- Doesn't reset **Archive Bit**

## DES Modes of Operation

### Electronic Codebook (ECB)
- Encrypts each block **independently**
- **Weakest mode** – identical plaintext blocks produce identical ciphertext blocks
- **Not recommended** for secure encryption

### Cipher Block Chaining (CBC)
- Each plaintext block is **XORed with the previous ciphertext block** before encryption
- Uses an **Initialization Vector (IV)** for the first block
- **Fixes ECB's weakness** but susceptible to padding oracle attacks

### Cipher Feedback (CFB)
- Converts a block cipher into a **stream cipher**
- Encrypts small segments of data, making it **useful for real-time encryption**
- Errors propagate but only affect a limited portion of the ciphertext

### Output Feedback (OFB)
- Also turns a block cipher into a **stream cipher**
- Errors do **not** propagate like in CFB
- Vulnerable to **bit-flipping attacks** if keystream is reused

### Counter (CTR)
- Encrypts a **numeric counter value** instead of plaintext directly
- Parallelizable, making it **fast and efficient**
- Used in **modern encryption algorithms** like AES

## 3DES (Triple Data Encryption Standard)

### Encryption Method
- Symmetric-key block cipher
- Applies DES encryption three times to each data block

### Keying Options
- **3-Key (K1, K2, K3)** → **168-bit security** (strongest)
- **2-Key (K1, K2, K1)** → **112-bit security** (minimum for strong security)
- **1-Key (K1 = K2 = K3)** → **56-bit security (same as DES, weak)**

### Why 2 Keys is the Minimum for Strong Security
- Using **1 key** reduces 3DES to standard DES, which is weak
- **2 keys (K1, K2, K1)** provide 112-bit security, strong enough for most cases
- **3 keys (K1, K2, K3)** offer more security but with minimal real-world benefit

## RC4 (Rivest Cipher 4)

### Encryption Method
- Symmetric-key **stream cipher** that encrypts data one byte at a time
- Generates a **pseudo-random keystream** based on a variable-length key and internal state array

### Key Sizes
- Variable key lengths from **40 to 2048 bits**
- Most common implementations used **128-bit keys**

### Security
- Fast and efficient, especially in software-based implementations
- Vulnerable to **key scheduling weaknesses** and **biased keystream output**
- Susceptible to several practical attacks (e.g., RC4 bias, Fluhrer–Mantin–Shamir attack)
- **Deprecated** in modern protocols like TLS and WPA due to weak cryptographic strength

## AES (Advanced Encryption Standard)

### Encryption Method
- Symmetric-key block cipher that encrypts data in **128-bit blocks**
- Uses the **Rijndael algorithm** with multiple encryption rounds

### Key Sizes
- **128-bit** → 10 rounds (fastest, still secure)
- **192-bit** → 12 rounds
- **256-bit** → 14 rounds (strongest, preferred for high security)

### Security
- Resistant to brute-force attacks due to large key sizes
- No practical attacks against AES when properly implemented

## RSA (Rivest-Shamir-Adleman)

### Encryption Method
- Asymmetric **public-key cryptosystem**
- Uses **two keys**: a **public key** for encryption and a **private key** for decryption

### Key Sizes
- Common sizes: **2048-bit, 3072-bit, 4096-bit**
- **Larger keys provide stronger security** but increase computational overhead

### Security
- Based on the difficulty of **factoring large prime numbers**
- Secure against brute-force attacks, but **vulnerable to quantum computing** in the future

### Performance
- **Slower** than symmetric encryption (AES) due to complex mathematical operations
- Typically used for **key exchange**, not for encrypting large amounts of data

## ECC (Elliptic Curve Cryptography)

#### Encryption Method
- Asymmetric (public-key) encryption based on the mathematics of **elliptic curves over finite fields**
- Provides **key exchange, digital signatures, and encryption** using small key sizes

### Key Sizes
- **256-bit ECC** offers similar security to **3072-bit RSA**
- Common sizes: **160, 224, 256, 384, and 521 bits** depending on security needs

### Security
- Strong cryptographic strength even with small keys
- Resistant to known classical attacks (but vulnerable to future quantum attacks like Shor’s algorithm)
- Ideal for **low-power or resource-constrained devices** due to efficiency
- Widely used in **TLS, cryptocurrencies, secure messaging, and mobile apps**

## Diffie-Hellman (DH)

### Encryption Method
- Asymmetric **key exchange protocol** that allows two parties to establish a shared secret over an insecure channel
- Does **not** encrypt data directly, only establishes a shared encryption key

### Key Exchange Process
- Each party generates a **private key** and a **public key**
- Public keys are exchanged, and each party computes the shared secret using their private key

### Security
- Based on the difficulty of solving the **discrete logarithm problem**
- **Vulnerable to man-in-the-middle (MITM) attacks** if authentication is not used
- Variants like **Elliptic Curve Diffie-Hellman (ECDH)** offer stronger security with smaller key sizes

### Performance
- **Faster** than RSA for key exchange
- Used for **establishing secure connections quickly**

## Symmetric vs. Asymmetric Cryptography  

| Feature            | Symmetric Cryptography | Asymmetric Cryptography |
|-------------------|---------------------|----------------------|
| **Key Usage**     | Uses **one** shared key for encryption and decryption | Uses a **key pair** (public key for encryption, private key for decryption) |
| **Speed**        | **Faster**, requires less computational power | **Slower**, due to complex mathematical operations |
| **Security**     | Secure if the key is protected, but key distribution is a risk | More secure for key exchange, as private key never needs to be shared |
| **Use Cases**    | Bulk data encryption (AES, 3DES) | Secure key exchange, digital signatures, authentication (RSA, ECC) |
| **Examples**     | AES, DES, RC4 | RSA, ECC, Diffie-Hellman |

### **Summary**
- **Symmetric:** Faster, but key distribution is a challenge
- **Asymmetric:** More secure for communication, but slower due to complex encryption
- **Often used together:** Asymmetric encryption secures the key exchange, and symmetric encryption handles bulk data encryption

## Asymmetric Cryptography

Asymmetric encryption uses a **public-private key pair** where data encrypted with one key can only be decrypted with the other. It is commonly used for **secure communication** and **digital signatures**.

### Encrypted Messaging (Confidentiality)
- Sender **encrypts** the message using the **recipient’s public key**
- Only the recipient can **decrypt** it using their **private key**
- Ensures that only the intended recipient can read the message

### Digital Signatures (Authentication & Integrity)
- Sender **hashes** the message and **encrypts the hash with their private key** (digital signature)
- Recipient **decrypts the signature with the sender’s public key** and verifies the hash
- Ensures the message was **sent by the claimed sender** (authentication) and was **not altered** (integrity)

### **Key Usage Summary**  
| Purpose | Key Used to Encrypt | Key Used to Decrypt |
|---------|----------------------|----------------------|
| **Confidentiality** (keeping data secret) | **Recipient’s public key** | **Recipient’s private key** |
| **Authentication & Integrity** (digital signatures) | **Sender’s private key** | **Sender’s public key** |

Asymmetric cryptography allows **both secure communication and sender verification** by using the correct key pair for encryption and decryption.

## Cloud Service Models

Cloud computing services are categorized into different models based on **what is managed by the provider vs. the customer**.

### 1. IaaS (Infrastructure as a Service)
- Provides **virtualized computing resources** (servers, storage, networking)
- Customers manage **OS, applications, and configurations**
- **Example:** AWS EC2, Microsoft Azure Virtual Machines, Google Compute Engine

### 2. PaaS (Platform as a Service)
- Provides a **managed development platform** with OS, runtime, and tools
- Customers manage **applications and data**, while the provider handles the infrastructure
- **Example:** Google App Engine, Microsoft Azure App Services, AWS Elastic Beanstalk

### 3. SaaS (Software as a Service)
- Provides **fully managed software applications** accessible over the internet
- Customers only manage **user settings and data**
- **Example:** Google Workspace (Gmail, Docs), Microsoft 365, Salesforce

### 4. IDaaS (Identity as a Service)
- Provides **cloud-based identity and authentication services**
- Used for **Single Sign-On (SSO), Multi-Factor Authentication (MFA), and identity federation**
- **Example:** Okta, Microsoft Entra ID (Azure AD), Google Identity

### **Comparison Table**  
| Model | Customer Manages | Provider Manages | Example Services |
|--------|------------------|------------------|------------------|
| **IaaS** | OS, apps, configurations | Hardware, networking | AWS EC2, Azure VMs, Google Compute Engine |
| **PaaS** | Apps, data | OS, runtime, infrastructure | Google App Engine, Azure App Services |
| **SaaS** | User settings, data | Everything else | Google Workspace, Microsoft 365 |
| **IDaaS** | Identity policies, users | Authentication, directory services | Okta, Azure AD |