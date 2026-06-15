# 05 — Exam Day Cheat Sheet (AZ-900)

> Quick-reference tables, memory aids, and exam strategy — for last-minute review. All factual content is covered in depth in files 01–03.

---

## 🎯 Exam Strategy

- **~60 minutes**, roughly **40–60 questions**, multiple choice.
- **Lightly technical** — focuses on *describe*, *compare*, *identify* — not configure or code.
- Technical IT experience is NOT required, but general IT knowledge helps.
- **No award for longest study time** — be efficient with mixed sources.

### ⚠️ Exam Domain Weights (from Microsoft Learn — higher than the book)

| Domain | Microsoft Learn Weight |
|---|---|
| Describe Cloud Concepts | **25–30%** |
| Describe Azure Architecture and Services | **35–40%** |
| Describe Azure Management and Governance | **30–35%** |

💡 Cloud Concepts is worth up to 30% — study Domain 1 thoroughly.

---

## ⚡ Quick Distinction Tables

### Cloud Concepts — Easily Confused Terms

| Concept | Definition | Scope |
|---|---|---|
| **Scalability** | Handle growth of users or work | Controlled by SKU/tier; grow as demand increases |
| **Elasticity** | **Automatically** grow and shrink based on demand | Auto-provisioning and de-provisioning |
| **Agility** | Speed and ease of allocating resources | Provisioning in minutes |
| **Fault Tolerance** | Handle component faults (power, network, hardware) | **Component-level** failures |
| **High Availability** | Keep services running for long periods | **Service-level** uptime |
| **Disaster Recovery** | Recover from events taking down a service | **Site/region-level** failures |
| **Reliability** | Recover from failures and continue functioning | = Resiliency + Availability |

### Shared Responsibility — Always Yours vs Always Provider

| Always **YOUR** responsibility | Always the **PROVIDER's** responsibility |
|---|---|
| Information and data | Physical datacenter |
| Devices allowed to connect | Physical network |
| Accounts and identities | Physical hosts |

Everything else (OS, network controls, apps, identity infra) **depends on service type** (IaaS/PaaS/SaaS).

### IaaS → PaaS → SaaS — One-Line Summary

| | IaaS | PaaS | SaaS |
|---|---|---|---|
| **You manage** | OS and above | App code + data | Data + identity only |
| **Exam keyword** | Lift-and-shift | Dev framework / Analytics | Email / Productivity |
| **Billing** | Stop VM = stop billing | Plan billed even idle | Subscription |

### Serverless Services — The Trio

| Service | Purpose |
|---|---|
| **Azure Functions** | Event-driven code execution |
| **Azure Logic Apps** | Workflow automation with connectors |
| **Azure Event Grid** | Pub/sub event routing |

### Container Spectrum

```
ACI (simple, fast) → Container Apps (elastic, LB) → AKS (full K8s orchestration)
```

---

## 🔐 Security Quick References

### Authentication Strength Ranking

```
BAD:    Password only
BETTER: Password + SMS/Voice
GOOD:   Password + Authenticator/OATH
BEST:   Passwordless (Hello, Authenticator, FIDO2)
```

### Zero Trust — 3 Principles + 6 Pillars

**Principles:** Verify explicitly · Least privilege (JIT/JEA) · Assume breach

**Pillars:** Identities · Devices · Apps · Data · Infrastructure · Networks

### Defense in Depth — 7 Layers (outside → in)

```
Physical → Identity & Access → Perimeter → Network → Compute → Application → Data
```

### Azure Key Vault — What It Stores

| Type | Examples |
|---|---|
| **Secrets** | Passwords, connection strings, API keys |
| **Encryption keys** | RSA/EC key pairs, HSM-backed (Premium tier) |
| **Certificates** | TLS/SSL with auto-renewal |

**Key points**: managed identities retrieve secrets at runtime (no hard-coded credentials). Access control + key rotation + usage auditing. HSM-backed keys never leave the HSM boundary (Premium tier).

### External Identities

| Type | Who | In Your Directory? |
|---|---|---|
| **B2B Collaboration** | Partners (work/social accounts) | ✅ Guest user objects |
| **B2B Direct Connect** | Another Entra tenant (Teams) | ❌ Not in directory |
| **External ID for Customers** | Consumers of your app | Separate tenant |

---

## 💰 Cost & Governance Quick References

### Pricing Options — Sorted by Savings

| Option | Savings | Commitment | Best For |
|---|---|---|---|
| Pay-as-you-go | Baseline | None | Variable usage |
| Savings Plan | Up to 65% | 1–3 years | Flexible compute |
| Reservations | Up to 72% | 1–3 years | Specific resource |
| Spot | Up to 90% | None | Interruptible workloads |

### Advisor Categories (memorize — "Capacity" is NOT one)

**R**eliability · **S**ecurity · **P**erformance · **O**perational Excellence · **C**ost

### Governance Hierarchy

```
Policy     → "The rules" (individual conditions)
Initiative → "A bundle of policies" (grouped toward a goal)
Blueprint  → "The whole package" (policies + ARM + RBAC + RGs)
```

### Resource Lock Types

| Lock | Read | Modify | Delete |
|---|---|---|---|
| **Delete** | ✅ | ✅ | ❌ |
| **ReadOnly** | ✅ | ❌ | ❌ |

To modify a locked resource: remove lock → perform action. Even Owners must remove locks first.

### Service Health — Three Scopes

```
Azure Status (global) → Service Health (your services) → Resource Health (one resource)
```

### Support Plans — Who Can Open Tech Tickets?

```
Basic (FREE)  → ❌ NO tech tickets (billing/subscription only)
Developer     → ✅ Email, business hours only
Standard      → ✅ 24/7 phone+email, <1hr Sev A
Pro Direct    → ✅ 24/7 + advisory, <15min Sev A
Premier       → ✅ TAM + everything, enterprise contract
```

---

## 🏗️ Architecture Quick References

### Storage Redundancy — Durability Ladder

| Option | Copies | Durability |
|---|---|---|
| LRS | 3 in 1 datacenter | 11 nines |
| ZRS | 3 across 3 zones | 12 nines |
| GRS/GZRS | 6 (3 primary + 3 secondary) | 16 nines |

### Blob Storage Tiers

```
Hot (no min) → Cool (30d) → Cold (90d) → Archive (180d, offline, rehydrate)
```

### SLA Uptime Numbers

| SLA | Downtime/Year | Downtime/Month |
|---|---|---|
| 99% | 3.65 days | ~7.2 hours |
| 99.9% | 8.76 hours | ~43.8 min |
| 99.99% | 52.6 min | ~4.38 min |

### VM SLA by Configuration

```
Single VM (Standard HDD): 95% → Single VM (Standard SSD): 99.5% → Single VM (Premium SSD): 99.9% → Availability Set: 99.95% → Availability Zones: 99.99%
```

### Management Tools — 5 Categories

```
Portal (graphical) · Cloud Shell (browser) · PowerShell (cmdlets) · CLI (Bash) · Copilot (AI)
```

### IaC Tools

```
ARM Templates (JSON) + Bicep (simpler DSL) — both declarative, idempotent, deploy via ARM
```

---

## 🧠 Memory Aids

- **CapEx → OpEx**: Cloud shifts from upfront infrastructure spending to pay-as-you-go.
- **Sustainability cycle**: Right-size → Automate → Optimize → Monitor.
- **Manageability**: OF the cloud (what you can do) vs IN the cloud (how you do it — portal, CLI, APIs, PS).
- **Private Endpoint** = specific resource, private IP, no public internet. **Service Endpoint** = all PaaS instances, still public.
- **RBAC is additive** (allow model). Permissions = union of all role assignments. Does NOT enforce at app/data level.
- **Tags do NOT inherit** from resource groups or subscriptions.
- **Action groups are reusable** across Monitor, Service Health, and Advisor.
- **Azure Arc**: 5 resource types outside Azure — servers, K8s, data services, SQL Server, VMs (preview).
- **Purview**: data governance + risk/compliance. Three capabilities: discovery, classification, lineage.
- **Copilot in Azure**: operational assistant — humans validate and approve.
- **Basic Support = NO tech tickets**. Only Developer and above can open technical support requests.
