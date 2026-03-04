# 📒 1) Cloud Foundations

> **Goal:** Understand what cloud is, how it differs from on-prem, and how service models (IaaS/PaaS/SaaS) change responsibility.

---

## Learning Objectives
- Define **cloud computing** and contrast it with **on-premises**
- Identify **service models** (IaaS / PaaS / SaaS) and **management tools** (Console / CLI / API)
- Explain **why organizations adopt cloud** and how **responsibilities shift**

---

## One-Line Mental Model
> Cloud = infrastructure you *don’t own* but can *control* through software (Console/CLI/API).

---

## On-Prem vs Cloud (What changes?)

| Aspect | On-Premises | Cloud |
|---|---|---|
| Hardware & data center | You buy and maintain | Provider owns and maintains |
| Scaling capacity | Slow (procurement) | Fast (on-demand) |
| Cost model | Upfront investment (CapEx) | Pay-as-you-go (OpEx) |
| Physical security | Your responsibility | Provider responsibility |
| Configuration security | Your responsibility | Still your responsibility (in most cases) |
| Redundancy & availability | You build it | Often built-in options |

**Key idea:** Cloud removes heavy physical overhead, but you still must secure configurations, identities, and data.

---

## Cloud Architecture (High-Level)
Cloud environments mirror on-prem layers, but add a critical layer:

### Management Plane (Must-Know)
The **management plane** is how you control the cloud:
- Provision resources
- Monitor health and usage
- Configure services
- Apply security controls (IAM, policies)
- Troubleshoot and automate

---

## Service Models (IaaS vs PaaS vs SaaS)

### Quick Definitions
- **IaaS:** provider gives infrastructure (VMs, networking, storage); you manage OS + apps
- **PaaS:** provider gives platform/runtime; you deploy code
- **SaaS:** provider gives full application; you configure and use it

### Responsibility Comparison (Exam-Friendly)
| Layer / Responsibility | IaaS | PaaS | SaaS |
|---|---:|---:|---:|
| Physical data center, hardware | Provider | Provider | Provider |
| Virtualization / core platform | Provider | Provider | Provider |
| OS patching | **You** | Provider | Provider |
| Runtime/middleware | **You** | Provider | Provider |
| Application code | **You** | **You** | Provider |
| Data & access control | **You** | **You** | **You (mostly)** |

<img width="1638" height="1046" alt="image" src="https://github.com/user-attachments/assets/2054e323-ba9a-44be-93c1-4d6c480a2ea8" />


> **Rule of thumb:** Moving from **IaaS → SaaS** increases convenience, but reduces control.

---

## How Cloud Services Are Accessed
| Method | When used |
|---|---|
| Public internet | Default for most services |
| VPN / private connectivity | Extra privacy, compliance, or enterprise environments |

---

## Why Cloud? (Benefits)
| Benefit | What it means (simple) |
|---|---|
| Scalability | Add/remove resources quickly |
| Cost efficiency | Pay for what you use |
| High availability | Redundancy options across zones/regions |
| Faster delivery | Launch environments in minutes |
| Backup & DR | Easier automation and recovery options |
| Security tooling | Strong native security features (still needs correct setup) |

---

## CapEx vs OpEx (Quick)
| Term | Meaning | Typical example |
|---|---|---|
| **CapEx** | Upfront spending | Buying servers + licenses |
| **OpEx** | Ongoing spending | Monthly cloud usage bills |

> Cloud is not always ideal (e.g., strict data residency, legacy constraints, or heavy existing investments).

---

## 🛠 Cloud Management Tools (Very Common in Exams)

| Tool | Best for | Example actions |
|---|---|---|
| **Web Console (GUI)** | Quick setup & visibility | Create resources, view configs |
| **CLI / PowerShell** | Repeatable tasks, scripting | Automate creation, bulk changes |
| **Cloud Shell** | CLI without local install | Run commands in browser |
| **REST API** | Integrations & automation | Programmatic provisioning |

**Tip:** Many “management tools” questions are basically: *GUI vs CLI vs API*.

---

## Shared Responsibility Model (Must-Know)
The provider secures **the cloud** (facilities, hardware, core infrastructure).  
You secure **what you put in the cloud** (IAM, configs, data, workloads).

### Quick Example
- Provider: physical servers, data center security
- You: IAM permissions, storage access policies, encryption choices, exposed keys, misconfigurations

---

## Quick Check (Mini Self-Test)
- Can you explain **IaaS vs PaaS vs SaaS** in one sentence each?
- Do you know what **management plane** means and what it controls?
- Can you describe what *you* are responsible for in the shared responsibility model?

---
