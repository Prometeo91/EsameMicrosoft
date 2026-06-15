# 01 — Describe Cloud Computing (15–20% of the exam)

---

## Skill 1.1: Describe Cloud Computing

### ☁️ What Is Cloud Computing?

Cloud computing means using computers and infrastructure, managed by a **cloud provider** (e.g., Microsoft Azure, AWS, Google Cloud), that are accessible over the internet. The provider takes on some responsibility for cloud resources and delivers financial benefits through a pay-for-what-you-use model.

### 🤝 Shared Responsibility Model

In an on-premises scenario, you are responsible for **everything**: hardware, networking, OS, applications, and support staff. When you move to the cloud, responsibility is **shared** between you and the cloud provider. How much you shift depends on the cloud service type you choose (IaaS, PaaS, SaaS).

| Responsibility | On-Premises | IaaS | PaaS | SaaS |
|---|---|---|---|---|
| Physical infrastructure | You | Provider | Provider | Provider |
| Networking | You | Provider | Provider | Provider |
| Operating system | You | **You** | Provider | Provider |
| Middleware / Runtime | You | **You** | Provider | Provider |
| Application | You | **You** | **You** | Provider |
| Data | You | **You** | **You** | **You*** |

> *Data is always YOUR responsibility across all service types — you own governance, classification, and access control. The provider manages the data infrastructure, not your data itself.

### 🏗️ Cloud Models

| Model | Description | Key Characteristics |
|---|---|---|
| **Public Cloud** | Shared infrastructure on a public network (e.g., Azure, AWS, GCP) | Multi-tenant; fastest to adopt; pay only for what you use; provider controls some infrastructure |
| **Private Cloud** | Dedicated environment for a single organization | Single-tenant; can be on-premises or third-party hosted; best for strict privacy/regulatory needs |
| **Hybrid Cloud** | Mixture of public and private clouds | Legacy systems stay on-prem; gradual migration; requires connectivity between environments (VPN, Hybrid Connections, Service Bus) |

⚠️ **Common Trap**: A private cloud does NOT have to be on-premises. It can be hosted at a third-party data center — what matters is that the infrastructure is dedicated to a single organization.

⚠️ **Common Trap**: A hybrid cloud does NOT always include on-premises resources. It can combine a third-party data center (private cloud) with a public cloud.

**Azure Stack** — Sold as a validated hardware + software package that lets you run Azure services on-premises, making hybrid cloud easier. You manage the on-premises hardware; the software runs Azure services.

### 💰 Consumption-Based Model

Cloud providers offer a **pay-as-you-go** approach: you pay only for the resources you consume. You can scale VMs up/down and even pay only for the time your code executes (e.g., Azure Functions). This eliminates heavy upfront capital expenditure.

### ⚖️ Comparing Cloud Models

| Factor | Public | Private | Hybrid |
|---|---|---|---|
| Cost model | Pay-as-you-go | High if on-prem; variable if hosted | Mixed |
| Control | Least (provider manages infra) | Most | Variable |
| Security | Shared; cloud provider helps | Highest (private network) | Depends on design |
| Speed of adoption | Fastest | Slowest | Moderate |
| Flexibility | Provider-defined configs | Full customization | Best of both, but complex |
| Typical concern | Lock-in to provider configs | Cost & management overhead | Data compatibility, latency, networking complexity |

### 💵 CapEx vs OpEx (from Exam Cram)

| | CapEx (Capital Expenditure) | OpEx (Operational Expenditure) |
|---|---|---|
| **What** | Upfront spending on physical infrastructure | Pay-as-you-go for services/products |
| **Associated with** | On-premises / private datacenter | Public cloud consumption |
| **Cloud impact** | **Decreases** with cloud adoption | **Increases** with cloud adoption |

💡 **Tip**: The cloud shifts spending from CapEx to OpEx. This is a frequently tested concept.

### 📊 Economies of Scale

The ability to do things more efficiently or at lower cost per unit when operating at a larger scale. Cloud providers benefit from massive scale and pass savings to customers. Cloud providers operate at large scale, which improves resource utilization compared to many isolated on-premises environments.

### 📖 NIST Definition of Cloud Computing (Reference)

The NIST SP 800-145 definition: cloud computing is a model for enabling **on-demand network access** to a **shared pool of configurable computing resources** (networks, servers, storage, apps, services) that can be **rapidly provisioned and released** with minimal management effort.

📌 **Key Points — Da ricordare**
- The shared responsibility model means responsibility is always shared — never 100% on you or the provider.
- Public = multi-tenant, Private = single-tenant, Hybrid = mix of both.
- The consumption-based model lets you pay only for resources you use.
- Azure Stack enables running Azure services on-premises for easier hybrid adoption.
- Private clouds can be hosted by third parties — ownership of hardware is not the defining factor.
- The cloud shifts spending from **CapEx** (upfront infra) to **OpEx** (pay-as-you-go). Economies of scale let providers pass savings to customers.

---

## Skill 1.2: Describe the Benefits of Using Cloud Services

### 🟢 High Availability

Availability = your app/data is accessible when needed. Common causes of downtime: network outage, application failure, system outage, power outage, reliant system failure.

Cloud providers offer a **Service-Level Agreement (SLA)** guaranteeing a certain uptime percentage. The SLA only covers systems controlled by the provider.

**SLA Downtime Reference Table (from Exam Cram):**

| SLA % | Allowed Downtime per Year | Allowed Downtime per Month |
|---|---|---|
| **99%** | 3.65 days | ~7.2 hours |
| **99.9%** | 8.76 hours | ~43.8 minutes |
| **99.99%** | 52.6 minutes | ~4.38 minutes |

⚠️ **Exam Tip**: Higher SLA = less downtime, but may increase cost. Know these numbers for the exam.

**Azure Application Insights** helps diagnose application failures by providing detailed performance and reliability data.

### 📈 Scalability

| Type | Also Called | What It Does |
|---|---|---|
| **Vertical scaling** | Scaling **up** / Scaling **down** | Move to a more (or less) powerful VM (more CPU, memory, features like SSD) |
| **Horizontal scaling** | Scaling **out** / Scaling **in** | Add or remove VMs that are identical copies |

- **Elasticity** = the ability to **automatically** scale based on usage patterns, resource utilization, or time of day.
- **Auto-Scale** = Azure service that automatically scales applications based on configurable rules.
- **Cloud Agility** = the speed and flexibility to scale quickly (seconds, not hours).

⚠️ **Exam Distinction — Scalability vs Elasticity**: Scalability = the system **can** add/remove resources to meet demand (capability). Elasticity = the system **automatically** adds/removes resources based on metrics (automation). A system can be scalable without being elastic (manual scaling), but elasticity requires scalability. (Duffy)

💡 **Tip**: Scaling goes both ways — out/in and up/down. On the exam, "elasticity" refers to automatic scaling in both directions.

### 🛡️ Reliability and Predictability

- **Fault tolerance** = cloud provider automatically moves you from an unhealthy VM to a healthy one without your intervention. Do NOT confuse with scaling (which assumes all VMs are healthy).
- **Disaster recovery (BCDR)** = replicate your application's resources in an unaffected region. Business Continuity and Disaster Recovery plans protect against large-scale regional failures (e.g., natural disasters).
- **Reliability (from Microsoft Learn)** = the ability to recover from failures and continue functioning. Combines **resiliency** (return to a functioning state after failure) and **availability** (consistent access over time). A pillar of the Azure Well-Architected Framework.

⚠️ **Exam Point**: Azure provides a reliable platform, but **you** must design your application for reliability on top of it — multi-instance deployments, multi-region failover, backup/restore strategies, and health probes are your responsibility. (Duffy)

**Predictability — Two Dimensions (from Microsoft Learn):**

| Predictability Type | Focus | Enabled By |
|---|---|---|
| **Performance predictability** | Predict the resources needed for a positive customer experience | Autoscaling, load balancing, high availability |
| **Cost predictability** | Predict/forecast cloud spending | Real-time tracking, data analytics, Pricing Calculator |

### 🔒 Security and Governance

Cloud providers invest heavily in monitoring networks and eliminating security threats. **Governance features** control who can access resources and what they can do — including policies that prevent creation of expensive resources.

**Three concentric layers (from Microsoft Learn):**

| Layer | What It Provides |
|---|---|
| **Governance** (outer) | Templates enforce standards; update at scale as standards change |
| **Compliance** (middle) | Cloud-based auditing flags non-compliant resources; suggests mitigations |
| **Security** (inner) | DDoS protection, patches, controls; IaaS = max control; PaaS/SaaS = auto patches |

💡 **Tip**: **Establish governance early** to keep your cloud footprint updated, secure, and well managed.

### 🔧 Manageability OF the Cloud vs IN the Cloud (from Microsoft Learn)

| Manageability **of** the Cloud (WHAT you can do) | Manageability **in** the Cloud (HOW you do it) |
|---|---|
| Auto-scale based on need | Azure portal (web GUI) |
| Deploy from preconfigured templates | Command-line interface (CLI) |
| Monitor health, auto-replace failing resources | APIs |
| Receive automatic alerts on metrics | PowerShell |

### 🌿 Sustainability in the Cloud (from Microsoft Learn)

⚠️ **New learning objective** — not in the book or Exam Cram.

Cloud computing supports sustainability goals through a continuous cycle: **Right-size → Automate → Optimize → Monitor**.

| Practice | Action |
|---|---|
| **Right-size** | Match resources to actual demand; avoid overprovisioning |
| **Automate** | Scale down and shut off unused resources automatically |
| **Optimize** | Choose efficient services and configurations |
| **Monitor** | Track resource usage and spending to optimize over time |

📌 **Key Points — Da ricordare**
- SLAs guarantee uptime but only for provider-controlled systems. Know the numbers: 99% = 3.65 days/yr, 99.9% = 8.76 hrs/yr, 99.99% = 52.6 min/yr.
- Scaling up = more powerful VM. Scaling out = more VMs. **Scalability ≠ Elasticity**: scalability = CAN add resources; elasticity = AUTOMATICALLY adds/removes them.
- Fault tolerance ≠ scaling. Fault tolerance handles unhealthy resources automatically.
- Reliability = resiliency + availability. A pillar of the Azure Well-Architected Framework. Azure provides the platform, but **you** must design your app for reliability.
- Predictability has TWO aspects: **performance** (autoscaling, load balancing) and **cost** (tracking, analytics, Pricing Calculator).
- BCDR plans protect against regional disasters by replicating to other regions.
- Cloud agility = ability to scale in seconds.
- Governance → Compliance → Security (three concentric layers). Establish governance early.
- Manageability OF the cloud (what) vs IN the cloud (how: portal, CLI, APIs, PowerShell).
- **Sustainability**: right-size, automate, optimize, monitor — a new learning objective.

---

## Skill 1.3: Describe Cloud Service Types

### The Cloud Pyramid

```
        ┌───────────┐
        │   SaaS    │  ← Least control, least responsibility
        ├───────────┤
        │   PaaS    │
        ├───────────┤
        │   IaaS    │  ← Most control, most responsibility
        └───────────┘
```

### 🖥️ IaaS (Infrastructure-as-a-Service)

- Provider gives you a VM; you install OS, middleware, and applications.
- Maximum control but maximum responsibility.
- You have remote access to VMs.
- Billing stops when you stop (deallocate) the VM.
- You benefit from the provider's underlying fault tolerance and disaster recovery.

💡 **Key takeaway (from Microsoft Learn)**: "You rent hardware — what you do with it is up to you."

**You manage**: Applications, Data, Runtime, Middleware, Operating System.
**Provider manages**: Servers, Storage, Networking.

**Common IaaS scenarios:**
- **Lift-and-shift migration** — set up cloud resources similar to on-prem, then move workloads to IaaS.
- **Testing and development** — rapidly replicate dev/test environments; start up or shut down with complete control.

### ⚙️ PaaS (Platform-as-a-Service)

- Provider manages infrastructure + OS + middleware + development tools.
- You focus on your application code, data, and access controls.
- VMs exist but are managed by the provider (limited/no visibility).
- No worry about licensing or patching for OS and databases.
- Depending on config, some networking and application security settings are shared.
- Offers built-in features (e.g., social media login, backups) with minimal configuration.
- Provider controls patching/updates — you get advance notice but lose control of timing.
- Examples: Azure App Service, Azure CDN, Azure Cosmos DB, Azure SQL Database, Azure Storage, Azure Synapse Analytics.

**Common PaaS scenarios:**
- **Development framework** — build cloud-based apps using built-in software components with scalability, HA, and multitenant capability included.
- **Analytics or business intelligence** — PaaS tools let teams analyze data, find patterns, and predict outcomes.

### 📦 SaaS (Software-as-a-Service)

- Provider manages almost all of the application stack — infrastructure, platform, and application maintenance.
- Access typically via web browser; works on almost any device.
- Least flexible, but easiest to get up and running. Requires least technical knowledge.
- Pay-as-you-go rental model.

💡 **Key takeaway (from Microsoft Learn)**: "You use the app — the provider handles everything else."

**You manage**: Data, identity and access settings, device access posture.
**Provider manages**: Everything else (Applications, Runtime, Middleware, OS, Servers, Storage, Networking).

**Common SaaS scenarios:** email and messaging (M365, Teams, Outlook), productivity applications (Word, Excel online), finance and expense tracking.

### 📊 Responsibility Stack — 8 Layers (from Microsoft Learn)

| Layer | IaaS | PaaS | SaaS |
|---|---|---|---|
| Applications | **You** | **You** | Provider |
| Data | **You** | **You** | **You** |
| Runtime | **You** | Provider | Provider |
| Middleware | **You** | Provider | Provider |
| Operating System | **You** | Provider | Provider |
| Servers | Provider | Provider | Provider |
| Storage | Provider | Provider | Provider |
| Networking | Provider | Provider | Provider |

⚠️ **Exam Tip**: IaaS = "most control", PaaS = "balanced", SaaS = "least control". In SaaS, Data is the ONLY layer you fully manage.

### Comparison Table

| Factor | IaaS | PaaS | SaaS |
|---|---|---|---|
| Control level | Highest | Medium | Lowest |
| Responsibility | OS + apps + data | Apps + data | Data + identity only |
| Management burden | Highest | Medium | Lowest |
| VM visibility | Full | Limited/None | None |
| Customization | Full | App-level only | None |
| Cost management | Stop VM = stop billing | Always billed for plan | Subscription model |
| Best for | Lift-and-shift, dev/test, full control | Dev frameworks, analytics/BI, quick deployment | Email, Office, finance tracking, CRM |

### ☁️ Serverless Computing (from Duffy)

**Serverless** does NOT mean "no servers" — it means **you don't manage the servers**. You provide code; the cloud runs it on a shared resource pool. Key characteristics: consumption-based pricing (zero usage = zero cost), no reservation needed, auto-scales automatically.

⚠️ **Exam Concept — Cold Start**: After a period of inactivity, serverless resources are paused. The first request after idle takes extra seconds to respond while the environment spins up. This is a known trade-off of serverless. (Duffy)

**Serverless Azure services**: Azure Functions, Azure SQL Database (serverless tier), Cosmos DB (serverless throughput). (Duffy)

### 🎯 Service Classification — Exam Quick Reference (from Duffy)

| Service | Type | Why |
|---|---|---|
| Azure Virtual Machine | **IaaS** | You manage OS and everything above |
| Azure Web App (App Service) | **PaaS** | Managed platform, you provide code |
| Azure Logic App | **PaaS** | Managed integration platform |
| Azure SQL Database | **PaaS** | Managed database, you provide data/queries |
| Azure Functions | **Serverless** | Event-driven code, no infra management |
| Microsoft Office 365 | **SaaS** | Ready-to-use application |

📌 **Key Points — Da ricordare**
- IaaS = you rent hardware and manage OS and above. "What you do with it is up to you."
- PaaS = you manage your app code + data only. Provider manages OS, middleware, dev tools.
- SaaS = provider manages everything. "You use the app — the provider handles everything else." You manage data + identity only.
- Lift-and-shift migration → IaaS. Development framework / Analytics → PaaS. Email / Productivity / Finance → SaaS.
- In IaaS, stop VM = stop billing. In PaaS (e.g., App Service), you're billed for the plan even if no apps are running.
- **Serverless ≠ "no servers"** — you don't manage them. Consumption-based, auto-scales, but has **cold start** penalty after idle. (Duffy)
- Know which services map to which type: VM = IaaS, Web App/Logic App/SQL DB = PaaS, Functions = Serverless, O365 = SaaS. (Duffy)
