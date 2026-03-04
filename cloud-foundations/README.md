# Cloud Foundations 

## Learning Goals
- Define **cloud computing** and distinguish it from **on-premises** environments  
- Identify common **cloud service models** and **management tools**  
- Explain **why organizations adopt cloud** and what changes in responsibility

---

## Core Idea
Cloud computing means running workloads on infrastructure owned and operated by a cloud provider, instead of building and maintaining your own data center.

> **Simple mental model:** the cloud is someone else’s infrastructure that you manage through software (console/CLI/API).

---

## On-Prem vs Cloud (What changes?)
**On-premises**: you own and maintain the full stack (facility, power, racks, hardware, networking, security, upgrades).  
**Cloud**: the provider handles the **physical layer** at scale (data centers, hardware, redundancy, physical security), while you manage your **cloud resources and configurations**.

---

## Cloud Architecture (High-level)
Cloud environments follow similar layers as on-prem, but add a key concept:

- **Management Plane**: control and management layer used for  
  provisioning, monitoring, configuration, access control, troubleshooting, and automation.

---

## Cloud Service Models
### IaaS — Infrastructure as a Service
- Provider offers virtualized infrastructure: **VMs, storage, networking**
- You manage: OS, configurations, applications, and most security settings

### PaaS — Platform as a Service
- Provider offers a managed runtime/platform to build and deploy apps
- You manage: application code and configuration (less infrastructure work)

### SaaS — Software as a Service
- Provider delivers a complete application over the internet
- You manage: usage, access, and app-level settings

<img width="1638" height="1046" alt="image" src="https://github.com/user-attachments/assets/3a91d8a1-8790-4506-9dd4-bd061d533d27" />


> **Rule of thumb:** moving from **IaaS → SaaS** increases ease of administration but reduces control.

---

## How Cloud Services Are Accessed
- Typically over the internet  
- Sometimes through private connectivity (e.g., VPN/private links), depending on the environment

---

## Why Cloud?
Common benefits include:
- **Scalability**: adjust resources quickly based on demand  
- **Cost efficiency**: pay-as-you-go instead of large upfront purchases  
- **Availability & reliability**: built-in redundancy and managed infrastructure  
- **Security & compliance tooling**: strong security capabilities (responsibility is shared)  
- **Backup/DR**: easier disaster recovery options and automation  
- **Speed & agility**: faster experimentation and deployment

---

## CapEx vs OpEx (Quick)
- **CapEx (On-prem)**: upfront investment in hardware/licensing
- **OpEx (Cloud)**: ongoing spending based on consumption

> Cloud is not always the best fit (e.g., strict regulatory constraints, data residency requirements, or heavy existing long-term investments).

---

## Cloud Management Tools (Very Common Exam Topic)
- **Web Console** (GUI): fast navigation and manual actions  
- **CLI / PowerShell**: repeatable tasks, scripting, automation workflows  
- **Cloud Shell**: browser-based CLI without local setup  
- **REST APIs**: programmatic access and integrations (infrastructure automation)

---

## Shared Responsibility Model (Must Know)
Responsibility depends on the service model:
- Provider is responsible for the **security of the cloud** (physical facilities, hardware, core infrastructure)
- Customer is responsible for the **security in the cloud** (configurations, IAM, data protection, and workloads)
