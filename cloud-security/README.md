#  3) Cloud Identity, Security, and Compliance

> **Goal:** Understand cloud security basics, how responsibility shifts, and how IAM + data protection + network protection + compliance fit together.

---

##  Learning Objectives
- Explain **shared responsibility** from a security perspective
- Apply **defense-in-depth** thinking to cloud environments
- Identify common **cloud attack patterns** (misconfig, credential abuse, insecure APIs)
- Understand **IAM fundamentals** across AWS/Azure/GCP
- Summarize **data protection** (encryption, backup, access control)
- Recognize **compliance** basics and provider tools/resources

---

##  One-Line Mental Model
> Cloud security = shared responsibility + strong IAM + layered controls + continuous monitoring.

---

##  Shared Responsibility 

| Category | Cloud Provider | Customer |
|---|---|---|
| Physical data centers & hardware | ✅ Always | ❌ |
| Core infrastructure & virtualization | ✅ Always | ❌ |
| Managed service platform security | ✅ Mostly | ❌ |
| Identity configuration (IAM) | ❌ | ✅ Always |
| Resource configuration (policies, firewall rules) | ❌ | ✅ |
| Data security (classification, access, encryption choices) | ❌ | ✅ |
| Application security | ❌ | ✅ |

![AWS Shared Responsibility Model](../Images/shared-responsibility-aws.png)
---

##  Defense in Depth 

| Layer | Examples  | Typical goal |
|---|---|---|
| Perimeter / Edge | DDoS protection, WAF, public firewall | Reduce internet exposure |
| Network | Segmentation, firewall rules, private endpoints | Contain lateral movement |
| Compute / Host | Patching, hardening, EDR | Protect workloads |
| Application | Secure configs, auth, scanning, CI/CD checks | Reduce app vulnerabilities |
| Data | Encryption, access control, backups | Prevent data loss/leak |
| Identity | MFA, least privilege, conditional access | Stop account takeover |

> One weak control should not be a single point of failure.

---

##  Common Cloud Attack Patterns

| Attack pattern | What it looks like | Why it works |
|---|---|---|
| **Misconfiguration** | Public buckets, open DB ports, overly-permissive policies | Defaults or mistakes |
| **Credential attacks** | Password spraying, leaked keys, stolen tokens | Weak auth / no MFA |
| **Insecure APIs** | Exposed API keys, missing auth, excessive permissions | Poor API hygiene |
| **Workload compromise** | Malware in VM/container, vulnerable app | Unpatched systems |

---

##  IAM Fundamentals (Across AWS / Azure / GCP)

### Key IAM Concepts
| Concept | Meaning |
|---|---|
| **Authentication** | Proving identity (password/MFA/SSO) |
| **Authorization** | What actions are allowed |
| **Least privilege** | Grant minimum required permissions |
| **Federation (SSO)** | Use external identity provider for access |

### IAM Building Blocks 
| Goal | AWS | Azure | GCP |
|---|---|---|---|
| Human identity | IAM User | Entra ID User (Azure AD) | Google Account |
| Group management | IAM Group | Groups | Google Groups |
| Workload identity | IAM Role | Managed Identity / Service Principal | Service Account |
| Permissions model | Policies | RBAC roles + assignments | Roles + IAM policy bindings |

---

##  IAM Best Practices 

| Practice | Why it matters |
|---|---|
| Enable **MFA** for privileged accounts | Reduces takeover risk |
| Use **roles** for services | Avoid storing keys |
| Apply **least privilege** | Limit blast radius |
| Audit permissions regularly | Remove unused access |
| Monitor auth events | Detect anomalous logins |
| Separate control-plane vs data-plane access | Reduces accidental exposure |

---

##  Basic Incident Response for Identity Compromise
1. **Revoke / disable** the identity (or remove sensitive permissions)
2. **Rotate** secrets (passwords, access keys, session tokens)
3. **Investigate**: what was accessed/changed?
4. **Remediate**: fix root cause (policy, MFA, logging)
5. **Recover & monitor**: confirm normal operations and watch for recurrence

---

##  Data Protection

| Data state | Goal | Common controls |
|---|---|---|
| **At rest** | Protect stored data | Encryption, key management, access policies, backups |
| **In transit** | Protect moving data | TLS/HTTPS, private connectivity, secure protocols |

### High-yield checklist
- Access control first (IAM + resource policies)
- Encryption at rest + in transit
- Backup/replication + tested recovery

---

##  Network Protection (Customer responsibilities)

| Provider | Typical controls (examples) |
|---|---|
| AWS | VPC, Security Groups, Network ACLs, PrivateLink |
| Azure | VNet, Network Security Groups (NSG), Private Endpoint |
| GCP | VPC, Firewall rules, VPC Service Controls |

> **Best practice:** minimize public exposure (avoid 0.0.0.0/0 for sensitive ports), and log + alert on unusual traffic.

---

##  Compute Protection (Workloads)
| Area | What to do |
|---|---|
| Patching | Keep OS and packages updated (especially in IaaS) |
| Hardening | Disable unnecessary services, secure configs |
| Monitoring | Collect logs/metrics; alert on suspicious activity |
| Reduce attack surface | Close unused ports, least privilege for services |

> **Note:** In PaaS, the provider patches more of the platform, but your code/config still matters.

---

##  Compliance (What it means in cloud)
Compliance is meeting legal/regulatory/industry requirements for data and systems.

| Common requirement type | Examples |
|---|---|
| Privacy & data protection | GDPR, CCPA |
| Security standards | ISO 27001, NIST, PCI DSS |
| Industry regulations | Healthcare/finance rules (varies by region) |
| Auditability | Logging, reporting, evidence collection |

### Provider support vs tenant responsibility
- Providers offer compliance documentation and tooling
- Customers must configure services correctly and meet their own obligations

---

##  Helpful References
- AWS Shared Responsibility Model
- Azure Shared Responsibility Model
- Google Cloud IAM Overview / Service Accounts Overview
- Google Cloud: Defense-in-depth networking principles
