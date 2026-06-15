# 02 — Describe Azure Architecture and Services (30–35% of the exam)

---

## Skill 2.1: Core Architectural Components of Azure

### 🌍 Azure Regions, Regional Pairs, and Sovereign Regions

**Geography** — a boundary (often a country border) that ensures data-handling regulations are met. Each geography contains two or more **regions** separated by hundreds of miles.

**Region** — a set of datacenters within a geography. Examples in the US geography: Central US (Iowa), East US (Virginia), West US (California), South Central US (Texas). When creating resources, only the region is visible to the customer.

**Regional Pair** — two regions within the same geography, at least **300 miles apart**. Microsoft updates one region in the pair at a time, so availability is maintained during platform updates.

**Region Pair Advantages (from Microsoft Learn):**
- **Prioritized restoration** — during an extensive outage, at least one region in every pair is prioritized for quick restoration.
- **Staggered updates** — planned updates rolled out to paired regions one at a time to minimize downtime.
- **Same-geography data residency** — data continues to reside within the same geography as its pair (except Brazil South).

⚠️ **Important**: Not all services automatically replicate or fail over between paired regions. In some cases, recovery and replication must be configured by the customer.

⚠️ **Edge case**: Most region pairs are bidirectional (West US ↔ East US), but some like **Brazil South** are one-direction only (paired to South Central US, but South Central US is NOT paired back to Brazil South). Some regions (Italy North, Poland Central, Israel Central) don't have a traditional pair and rely on availability zones + geo-redundant storage instead.

💡 **Tip**: Deploy resources redundantly to each region within a pair to benefit from regional pairs.

**Sovereign Regions** — isolated clouds for specific compliance requirements:

| Sovereign Cloud | Operated By | Key Requirement |
|---|---|---|
| **Azure Government** | Microsoft (screened US citizens only) | US government agencies, cities, municipalities; separate datacenters, dedicated networking; portal at portal.azure.us |
| **Azure Government (DoD)** | Subset of Azure Government | DoD Impact Level 5 compliance |
| **Azure Germany** | T-Systems International (data trustee) | EU/EFTA/UK customers; strict data residency |
| **Azure China (21Vianet)** | Shanghai Blue Cloud / 21Vianet | Chinese data regulations; limited feature set |

⚠️ **Exam Tip**: Each geography has at least two regions separated by a large physical distance — this is how Azure maintains disaster recovery.

### 🏢 Availability Zones

- At least **3 availability zones** per enabled region, each in a separate physical datacenter.
- Each zone has its own power, cooling, water supply, and network.
- Deploying in 2+ zones achieves high availability.
- Microsoft guarantees **99.99% SLA** for VMs deployed in 2+ availability zones.

⚠️ **Exam Tip**: Availability zones provide HA and fault tolerance but may not protect against large-scale regional disasters (e.g., a tornado affecting the entire region). They are one facet of a full DR design.

**Three categories of zone-aware services (from Microsoft Learn):**

| Category | Behavior | Examples |
|---|---|---|
| **Zonal services** | You pin the resource to a specific zone | VMs, managed disks, IP addresses |
| **Zone-redundant services** | Platform replicates automatically across zones | ZRS storage, SQL Database |
| **Non-regional services** | Always available from Azure geographies; resilient to zone AND region outages | Microsoft Entra ID, Traffic Manager, Azure DNS |

⚠️ **Important**: Not all Azure regions currently support availability zones. Zones are connected via **high-speed private fiber-optic networks**. There may be a cost to duplicating services and transferring data between zones.

⚠️ **Don't confuse:**
- **Availability set** = 2+ VMs in different racks within ONE datacenter → **99.95% SLA**
- **Availability zone** = 2+ VMs in different datacenters (buildings) within ONE region → **99.99% SLA**

### 🏗️ Azure Datacenters

Physical buildings in a region with climate control, isolated power supply, power generators, and Microsoft-owned fiber-optic networking. Microsoft guarantees ≤2ms round-trip network latency between regions. Data replication across regions protects against regional disasters.

### 📦 Azure Resources and Resource Groups

**Resource group** = a logical container for organizing Azure resources. Benefits: deploy/manage all resources as a single entity, ARM template deployments target a resource group, easy cost tracking, easy bulk deletion.

| Rule | Detail |
|---|---|
| One resource → one group | A resource can exist in only one resource group at a time |
| No nesting | Resource groups cannot be nested inside other groups |
| No renaming | Groups cannot be renamed after creation — choose a clear naming convention |
| Cross-region allowed | Resources in a group can span multiple Azure regions |
| Cascading actions | Deleting a group deletes ALL resources inside it; access permissions apply to all resources |
| Moving resources | You can move some resources between groups, but only one group at a time |

⚠️ **Exam Trap**: Resource groups do NOT provide a **security boundary** for inter-resource communication — any resource can access any resource in a different resource group (unless other security mechanisms like NSGs or private endpoints are in place). Resource groups control **management** and **permissions**, not network isolation. (Duffy)

### 🔑 Azure Subscriptions

A subscription provides access to Azure products/services and serves as a **billing unit**. Links to an Azure account (an identity in Microsoft Entra ID). An account can have multiple subscriptions, but only one is required.

**Two types of subscription boundaries (from Microsoft Learn):**

| Boundary Type | Purpose |
|---|---|
| **Billing boundary** | Determines how the account is billed. Separate subscriptions = separate invoices. |
| **Access control boundary** | Access-management policies applied at subscription level. Different subscriptions can have different spending limits and access rules. |

**Reasons to create additional subscriptions:** separate environments (sandbox, dev, test, prod), team/workload boundaries (per-project cost tracking), or billing separation (production vs. development invoices).

**Subscription types**: Free Trial, Pay-As-You-Go, Azure For Students.

**Azure free account**: 12 months free access to popular products, 30-day credit, 65+ always-free services. Requires phone number, credit card (verification only), and Microsoft/GitHub account.

**Azure free student account**: $100 credit, 12 months free services, free developer tools. No credit card required.

Each subscription has a **globally unique subscription ID**.

⚠️ **Exam Tip**: Microsoft support can increase some limits with business justification — but some limits are hard caps.

### 🗂️ Management Groups

Containers for organizing subscriptions (or other management groups). Apply governance conditions (access policies, compliance rules) at the management group level. All subscriptions in a group automatically inherit those conditions.

**Limits**: max 10,000 groups per directory; max **6 levels deep** (excluding the root level and the subscription level); each group/subscription has only one parent.

**Default**: every Microsoft Entra tenant has a single top-level **Tenant Root Group**. All other management groups and subscriptions fold up to this root group.

**Use cases**: apply a policy across subscriptions (e.g., limit VM locations to a region), grant RBAC access to multiple subscriptions at once.

### 🔗 Hierarchy

```
Management Group (top)
  └── Subscription
        └── Resource Group
              └── Resource (bottom)
```

Policies and access applied at a higher level inherit downward. A subscription owner **cannot override** a policy set at the management group level.

📌 **Key Points — Da ricordare**
- A geography has 2+ regions; a regional pair has 2 regions **300+ miles apart**, updated sequentially.
- Region pair advantages: prioritized restoration, staggered updates, same-geography data residency.
- Availability zones = separate buildings connected by fiber-optic; availability sets = separate racks in ONE datacenter.
- **Three** zone-aware service types: Zonal, Zone-redundant, and **Non-regional** (Entra ID, Traffic Manager, Azure DNS).
- Not all regions support availability zones. Not all services auto-replicate between paired regions.
- Resource groups: no nesting, no renaming, cascading actions (delete group = delete all).
- Subscriptions have two boundaries: **billing** and **access control**. Management groups nest up to 6 levels (excluding root and subscription).
- The hierarchy is: Management Group → Subscription → Resource Group → Resource. Policies inherit downward and cannot be overridden by lower levels.

---

## Skill 2.2: Azure Compute and Networking Services

### 🖥️ Compute Types

**Container Instances (ACI)** — the fastest and simplest way to run a container in Azure. PaaS offering: upload your containers and the service runs them. No VM management. Great for simple, short-running workloads.

**Azure Container Apps** — similar to ACI but with built-in **load balancing and scaling**. PaaS offering. Removes container management overhead. Positioned as the "elastic app layer" between ACI and AKS.

**Azure Kubernetes Service (AKS)** — container **orchestration** service. Manages the lifecycle of a fleet of containers. Azure manages the control plane; you deploy containers. Best for enterprise-scale container deployments.

**Container Spectrum (from Microsoft Learn):**
```
ACI ──────────→ Container Apps ──────────→ AKS
(faster start)   (elastic app layer)       (deeper orchestration)
PaaS              built-in LB + scaling     Kubernetes control
```

**Virtual Machines** — IaaS. You control the OS and installed software. Deploy quickly from prebuilt **images** (templates with OS and tools). You still manage patching, updates, and configuration.

**Azure Functions** — event-driven, serverless compute. An event wakes the function; no need to keep resources provisioned when idle. Pay only for CPU time used while the function runs. Triggers: HTTP, Timer, Queue message. Outputs: API response, Storage write, Event publish.

- **Stateless** (default) = behaves as if it restarts every time it responds to an event.
- **Stateful** (**Durable Functions**) = the runtime passes a context to track prior activity.

💡 **Tip**: Functions are ideal when you only care about the code, not the platform. They scale automatically based on demand and can also run in non-serverless environments for more control.

### 🖥️ Azure Virtual Machine Options

**VM Use Cases (from Microsoft Learn):** testing and development, cloud application hosting, datacenter extension, disaster recovery, lift-and-shift migration.

**VM Size Families (from Microsoft Learn):**

| Family | Focus | Example Use |
|---|---|---|
| **B-series** | Burstable, cost-efficient | Dev/test workloads with occasional CPU spikes |
| **D-series** | General purpose | Web servers, small-to-medium app servers |
| **E-series** | Memory optimized | In-memory databases, analytics workloads |
| **F-series** | Compute optimized | CPU-intensive application tiers |
| **M-series** | Large memory footprint | Large enterprise databases |
| **L-series** | Storage optimized | High-throughput storage and data processing |
| **N-series** | GPU enabled | AI training/inference and graphics workloads |

**How to read a VM name** (e.g., `Standard_D2s_v5`): D = family (general purpose), 2 = vCPUs, s = premium SSD support, v5 = hardware generation.

**Availability Sets** — protect against rack failures and planned maintenance. No additional cost (you pay for the VM instances only):
- **Fault domains** (default: 2) = VMs that share a potential power or network failure point. Protects against hardware failures.
- **Update domains** (default: 5) = VMs that can be rebooted together during planned maintenance. Azure reboots one update domain at a time, waiting 30 minutes between each.

💡 **Tip**: In regions that support Availability Zones, zone-based designs are preferred because they provide broader failure isolation. Use availability sets for VM-level redundancy within a single datacenter.

**Scale Sets (VMSS)** — create and manage groups of identical, load-balanced VMs. Centralize configuration, auto-scale out/in based on demand or schedules. Integrate with load balancing for efficient traffic distribution.

**VM SLA Guarantees — Full Ladder:**

| Configuration | SLA |
|---|---|
| Single VM with **Standard HDD** managed disks | **95%** |
| Single VM with **Standard SSD** managed disks | **99.5%** |
| Single VM with **Premium SSD** or Ultra Disk | **99.9%** |
| Multi-VM with **Availability Set** | **99.95%** |
| Multi-VM with **Availability Zones** (2+ zones) | **99.99%** |

⚠️ **Exam Tip**: Know the full SLA ladder. Moving from HDD → SSD → Premium → Availability Set → Availability Zones progressively increases the SLA guarantee. Cost also increases at each step.

**Azure Virtual Desktop (AVD)** — desktop and application virtualization service. Desktops and apps stay in the cloud, not on local devices. Integrates with Microsoft Entra ID for identity/access. Supports single-session and multi-session Windows experiences. Reduces data exposure on local devices.
- Architecture: Users (laptop/tablet/web) → Entra ID (access policies) → Host pool (session hosts with cloud desktops and apps).

### 🤖 AI, Machine Learning, and IoT/Edge Services (from Microsoft Learn)

| Service | When to Use |
|---|---|
| **Azure AI Services** | Prebuilt AI features via APIs (language, speech, vision, document processing). No custom model training needed. |
| **Azure OpenAI Service** | Generative AI scenarios (chat, content generation) with built-in security and governance. |
| **Azure Machine Learning** | Build, train, and manage **custom** ML models. For model development, experimentation, lifecycle management. |
| **IoT Hub** | Secure, bi-directional communication between cloud services and IoT devices. |
| **IoT Central** | Simplified SaaS IoT platform for solution builders. |
| **IoT Edge** | Extends cloud capabilities to edge devices — run workloads closer to where data is generated. |

**Agentic AI patterns** — combine AI models with instructions, context, and tool use for multistep goals. Built from Azure AI + OpenAI services + your application logic. It's an application pattern, not a separate compute service category.

**Decision pattern**: Use Azure AI services for prebuilt APIs → Azure ML for custom models → IoT services for connected devices and telemetry.

### ⚙️ Resources Required for VMs

Creating a VM auto-creates: virtual network, network interface, public IP address, network security group, OS disk. Plus it requires a management group, subscription, and resource group.

⚠️ **Exam Tip**: Stopping a VM from the portal (Stop button) deallocates it and stops billing. Shutting down from within the guest OS does NOT deallocate — you still pay for disk and resources.

### 🌐 Application Hosting Options

**Hosting Spectrum (from Microsoft Learn):**
```
VMs ──────────────→ Containers ──────────────→ App Service
(more control)      (component isolation,       (managed platform,
 OS + config          portable deployments,       autoscale + HA,
 you patch)           independent scaling)        integrated deployment)
                                                 (less operational effort)
```

**Azure App Service** — HTTP-based PaaS for hosting web applications, REST APIs, and mobile back ends. Supports .NET, .NET Core, Java, Ruby, Node.js, PHP, Python on Windows or Linux. Automated deployments from GitHub, Azure DevOps, or any Git repo.

**Four types of App Service:**

| Type | Purpose |
|---|---|
| **Web apps** | Full support for hosting web apps (ASP.NET, Java, Node.js, PHP, Python, Ruby) |
| **API apps** | Build REST-based web APIs with Swagger support; publish to Azure Marketplace |
| **WebJobs** | Run programs or scripts (.exe, Java, PHP, Python, Node.js, .cmd, .bat, PowerShell, Bash) as background tasks; scheduled or trigger-based |
| **Mobile apps** | Build back ends for iOS and Android apps; cloud SQL database, social auth (MSA, Google, Facebook), push notifications, custom C#/Node.js logic |

**App Service built-in features**: integrated deployment and management, endpoint security, quick scaling for high traffic, built-in load balancing and traffic manager for HA.

| Tier | Shared VMs? | Max Instances | Notes |
|---|---|---|---|
| Free / Shared | Yes | N/A | Testing only |
| Basic | No (dedicated) | 3 | |
| Standard | No | 10 | |
| Premium / PremiumV2 | No | 20 | |

⚠️ **Exam Tip**: You are charged for App Service plans even when no web apps are running. Delete the plan to stop billing.

**Containers (ACI, Container Apps, AKS)** — see compute types above for the full spectrum.

**VMs** — maximum control for app hosting, but maximum responsibility for configuration, security, and management.

### 🌐 Virtual Networking

**Azure Virtual Network (VNet)** — enables Azure resources (VMs, web apps, databases) to communicate with each other, the internet, and on-premises resources. Think of it as an extension of your on-premises network with resources that link Azure resources.

**7 Key VNet Capabilities (from Microsoft Learn):**

| Capability | Details |
|---|---|
| **Isolation and segmentation** | Create multiple isolated VNets with private IP address spaces; divide into subnets. Built-in name resolution or use internal/external DNS. |
| **Internet communications** | Assign a public IP or place resource behind a public load balancer for incoming internet connections. |
| **Communicate between Azure resources** | VNets connect VMs + other resources (App Service, AKS, Scale Sets). Service endpoints connect to Azure SQL, Storage, etc. |
| **Communicate with on-premises** | Point-to-site VPN, Site-to-site VPN, or Azure ExpressRoute (see below). |
| **Route network traffic** | Route tables (custom routing rules), BGP (propagate on-prem routes), User-defined routes (UDR) for subnet-to-subnet control. |
| **Filter network traffic** | **NSGs** (inbound/outbound rules by IP, port, protocol — evaluated by priority, **first match wins**) and **Network Virtual Appliances (NVAs)** (specialized VMs for firewall, intrusion detection, WAN optimization). |
| **Connect virtual networks** | VNet peering — private traffic on Microsoft backbone, never entering public internet. Works across regions (global peering). |

**Endpoints**: Public endpoints have a public IP (accessible from anywhere). Private endpoints exist within a VNet with a private IP from that VNet's address space, connected to a specific resource via **Azure Private Link** — traffic never touches the public internet. (Duffy)

**VNet peering** = connect two VNets directly. Traffic is private, travels on the Microsoft backbone. VNets can be in separate regions for a global interconnected network. ⚠️ VNets must have **non-overlapping IP address ranges** to peer — plan address spaces carefully. (Duffy)

**Azure DNS** — manage DNS records (A, AAAA, CNAME, MX, NS, SOA) in the Azure portal with built-in access control, logging, and policies.

| Zone Type | Purpose |
|---|---|
| **Public DNS Zone** | Internet-facing DNS records |
| **Private DNS Zone** | DNS records for Azure VNet resources (must link VNet) |

**Azure VPN Gateway** — a type of virtual network gateway deployed in a dedicated subnet. Uses encrypted tunnels (IPSec/IKE) over the public internet. Can take up to 45 minutes to create. **Only one VPN gateway per VNet**, but it can connect to multiple locations. Authentication: preshared key.

| Connection Type | Connects | Use Case |
|---|---|---|
| **Point-to-site** | Remote device → Azure VNet | Remote workers, mobile users |
| **Site-to-site** | On-premises VPN device → Azure VNet | Branch offices, datacenters |
| **Network-to-network** | Azure VNet A → Azure VNet B | Cross-region Azure connectivity |

**VPN Gateway Types (from Microsoft Learn):**

| Type | How It Works | When to Use |
|---|---|---|
| **Policy-based** | Statically defines which packets to encrypt by IP address | Legacy scenarios |
| **Route-based** | IPSec tunnels as network interfaces; IP routing decides the tunnel | **Preferred** — more resilient to topology changes; supports VNet-to-VNet, point-to-site, multisite, and ExpressRoute coexistence |

**VPN Gateway High Availability:**
- **Active/standby** (default) — two instances deployed automatically. Standby takes over during planned maintenance (seconds) or unplanned disruption (up to 90 seconds). No user intervention needed.
- **Active/active** — both instances active simultaneously for greater resilience.

**Azure ExpressRoute** — dedicated fiber-optic connection (not over public internet) via a third-party service provider to a Microsoft Enterprise Edge (MSEE) router. Speeds up to 10 Gbps. **ExpressRoute Direct** connects directly to the MSEE port (no service provider middleman). A connection is called a **circuit**. Each circuit uses redundant connections for HA.

### 🛡️ Additional Networking Services

**Azure Bastion** — managed PaaS service for secure RDP/SSH access to VMs directly through the Azure portal over TLS, without exposing a public IP on the VM. Eliminates the need for a jump box.

**Azure DDoS Protection:**

| Tier | What It Does |
|---|---|
| **DDoS Protection Basic** | Free, automatically enabled. Protects against common network-layer attacks. |
| **DDoS Protection Standard** | Paid. Mitigates 60+ DDoS attack types. Includes DDoS Rapid Response (DRR) team support and cost guarantee (service credit if a DDoS attack causes scale-out). |

💡 **Tip**: DDoS Protection Standard + **Web Application Firewall (WAF)** = protection at network layer (L3/L4, DDoS) + application layer (L7, WAF).

**Azure Front Door** — Microsoft's modern cloud CDN (Content Delivery Network). Provides fast, reliable, and secure access to web content globally using Microsoft's edge network with hundreds of points of presence (PoPs). Combines CDN, global load balancing, and WAF in one service.

📌 **Key Points — Da ricordare**
- Container spectrum: ACI (simple, fast) → Container Apps (elastic, load-balanced) → AKS (full Kubernetes orchestration).
- VM size families: B (burstable), D (general), E (memory), F (compute), M (large memory), L (storage), N (GPU).
- Functions: stateless (default) vs stateful (Durable Functions). Triggers: HTTP, Timer, Queue. Pay for CPU time only.
- Serverless trio: Functions (event-driven code), Logic Apps (workflow automation), Event Grid (pub/sub events).
- AI services (prebuilt APIs) vs Azure ML (custom models) vs IoT (connected devices). Agentic AI is a pattern, not a service.
- Fault domains protect from rack failures; update domains protect from reboot downtime. Availability sets are free.
- **VM SLA ladder**: Standard HDD 95% → Standard SSD 99.5% → Premium SSD 99.9% → Availability Set 99.95% → Availability Zones 99.99%.
- VNet peering uses Microsoft's backbone; **requires non-overlapping IP ranges**; VPN Gateway encrypts traffic with IPSec. (Duffy)
- Private Endpoint = specific resource, private IP via **Azure Private Link**, no public internet. Service Endpoint = all PaaS instances, still public. (Duffy)
- ExpressRoute provides dedicated, private connectivity up to 10 Gbps — not over the internet.
- Azure Bastion = secure RDP/SSH via portal without public IP. DDoS Basic (free) vs Standard (paid, 60+ attack types, DRR team).
- Azure Front Door = modern CDN + global load balancer + WAF.
- App Service plans bill even with no running apps — delete the plan to stop charges.

---

## Skill 2.3: Azure Storage Services

### 🏦 Storage Accounts

A storage account provides a **unique namespace** for your Azure Storage data, accessible from anywhere in the world over HTTP or HTTPS. Data is secure, highly available, durable, and massively scalable.

**Storage account naming rules (from Microsoft Learn):**
- **3–24 characters**, lowercase letters and numbers only
- Must be **globally unique** across all of Azure (forms part of the endpoint URL)

**Storage account endpoints (from Microsoft Learn):**

| Storage Service | Endpoint Format |
|---|---|
| **Blob Storage** | `https://<account-name>.blob.core.windows.net` |
| **Data Lake Storage Gen2** | `https://<account-name>.dfs.core.windows.net` |
| **Azure Files** | `https://<account-name>.file.core.windows.net` |
| **Queue Storage** | `https://<account-name>.queue.core.windows.net` |
| **Table Storage** | `https://<account-name>.table.core.windows.net` |

### 🏦 Storage Account Types (from Microsoft Learn)

| Type | Supported Services | Redundancy Options | Best For |
|---|---|---|---|
| **Standard general-purpose v2** | Blob (+ Data Lake), Queue, Table, Azure Files | LRS, GRS, RA-GRS, ZRS, GZRS, RA-GZRS | **Recommended** for most scenarios |
| **Premium block blobs** | Blob (+ Data Lake) | LRS, ZRS | High transaction rates, small objects, low latency |
| **Premium file shares** | Azure Files only | LRS, ZRS | High-scale or high-performance apps; supports both SMB and NFS |
| **Premium page blobs** | Page blobs only | LRS only | Page blob workloads (e.g., VM disks) |

⚠️ **Exam Tip**: You cannot change the account type after creation. Premium types only support LRS/ZRS — no geo-redundancy.

### 🔄 Redundancy Options (from Microsoft Learn)

**Key decision factors**: how data is replicated in the primary region, whether it's also replicated to a secondary region, and whether you need read access to the secondary before failover.

**Primary-region redundancy:**

| Option | Copies | Placement | Durability (nines) | Protects Against |
|---|---|---|---|---|
| **LRS** (Locally Redundant) | 3 | Same datacenter (synchronous) | **11 nines** | Drive/rack failure. NOT datacenter disasters |
| **ZRS** (Zone-Redundant) | 3 | 3 availability zones (synchronous) | **12 nines** | Single datacenter failure. Data stays available for read+write even if one zone is unavailable |

💡 **Tip**: Microsoft recommends ZRS for HA in-region scenarios and when data must stay within a country or region.

**Secondary-region redundancy:**

| Option | Primary | Secondary | Durability (nines) | Notes |
|---|---|---|---|---|
| **GRS** | 3 copies via LRS | 3 copies via LRS in paired region | **16 nines** | Async replication to secondary |
| **GZRS** | 3 copies via ZRS | 3 copies via LRS in paired region | **16 nines** | Best durability — zone-level + geo-protection |

- You choose the primary region; Azure assigns the paired secondary region automatically.
- Secondary data is **not readable** by default — only after failover.
- **RA-GRS / RA-GZRS** = read-access variants; enable reading from the secondary region **before** a failover. URL uses `-secondary` suffix. Available for all services except Azure Files.
- All writes are **synchronous** within the primary region. Replication to a secondary region is **asynchronous**.

⚠️ **Exam Tip — RPO**: Because geo-replication is asynchronous, recent writes may be lost if the primary fails before replication completes. Azure Storage typically has an RPO of **< 15 minutes**, but there is no SLA on replication time. Secondary-region data may not be up-to-date due to RPO.

### 📂 Storage Services (from Microsoft Learn)

**Benefits of Azure Storage**: durable and highly available (redundancy), secure (encrypted at rest, fine-grained access control), scalable, managed (Azure handles hardware and maintenance), accessible (HTTP/HTTPS via REST APIs, SDKs, CLI, PowerShell, portal, Storage Explorer).

| Service | Purpose | Key Details |
|---|---|---|
| **Azure Blobs** | Unstructured object storage for text and binary data | Block Blobs (files), Append Blobs (logs), Page Blobs (VHDs). Organized in containers. Includes **Data Lake Storage Gen2** for big data analytics. Ideal for: serving images/docs to browsers, streaming video/audio, backup and DR, distributed file access, data for analysis. |
| **Azure Files** | Fully managed cloud file shares | Accessible via **SMB** (Windows, Linux, macOS) or **NFS** (Linux, macOS only). Mountable concurrently by cloud or on-premises. SMB shares can be cached on Windows Servers with **Azure File Sync** for fast local access. Requires TCP port 445. |
| **Azure Queues** | Message queuing for async processing | Max message: 64 KB. Accessed via authenticated HTTP/HTTPS calls. Can hold millions of messages. Commonly paired with **Azure Functions** for trigger-based background actions. |
| **Azure Disks** | Block-level storage volumes for VMs | Managed disks — virtualized and managed by Azure for improved resiliency. HDD or SSD (Standard/Premium). Max size: 32,767 GiB per disk. |
| **Azure Tables** | NoSQL structured non-relational data | Large amounts of structured data accessible through authenticated calls from cloud and hybrid environments. |

💡 **Azure Files key benefits (from Microsoft Learn)**: shared access (SMB + NFS), fully managed (no server/OS patching), scripting and tooling support (CLI, PowerShell, portal, Storage Explorer), built-in resiliency for HA, familiar programmability (standard file I/O APIs + Azure SDKs + REST APIs).

### 🌡️ Storage Tiers (Blob Storage) — from Microsoft Learn

| Tier | Optimized For | Min Retention | Storage Cost | Access Cost | Account-level Setting? |
|---|---|---|---|---|---|
| **Hot** | Frequently accessed data (e.g., website images) | None | Highest | Lowest | ✅ Yes |
| **Cool** | Infrequently accessed, stored 30+ days (e.g., invoices) | 30 days | Lower | Higher | ✅ Yes |
| **Cold** | Infrequently accessed, stored 90+ days | 90 days | Lower still | Higher still | ✅ Yes |
| **Archive** | Rarely accessed, stored 180+ days (e.g., long-term backups) | 180 days | Lowest | Highest + rehydration latency | ❌ Blob-level only |

**Tier-setting rules (from Microsoft Learn):**
- Hot, Cool, and Cold tiers can be set at the **account level** (default for new blobs).
- **Archive tier cannot be set at the account level** — blob-level only.
- All four tiers (Hot, Cool, Cold, Archive) can be set at the **blob level**, during or after upload.
- Cool and Cold tiers have lower storage costs but higher access costs and lower availability SLAs.
- From Hot → Archive: storage cost decreases, access cost and retrieval latency increase.

⚠️ **Exam Tip**: To access a Blob in the Archive tier, you must first **rehydrate** it (move it to Hot or Cool tier).

### 📤 Moving Files (from Microsoft Learn)

| Tool | Type | Sync Direction | Key Capabilities |
|---|---|---|---|
| **AzCopy** | Command-line utility | **One-way** (source → destination) | Upload, download, copy between storage accounts, synchronize files. Can work **cross-cloud provider**. Scripted/automated tasks. |
| **Azure Storage Explorer** | GUI app (Win/macOS/Linux) | Manual upload/download | Visual browsing and management of blobs and files. Uses **AzCopy on the backend** for all file/blob operations. |
| **Azure File Sync** | Agent service | **Bi-directional** (automatic) | Centralize file shares in Azure Files while keeping Windows file server flexibility. Supports SMB, NFS, FTPS protocols. **Cloud tiering** (frequent files local, infrequent files in cloud). Multisite caching. |

⚠️ **Exam Tip**: AzCopy synchronization is **one-direction only** — it does NOT sync bi-directionally. Azure File Sync IS bi-directional.

**Azure File Sync details (from Microsoft Learn):**
- Turns your Windows file server into a local cache of an Azure Files share.
- Supports any protocol available on Windows Server (SMB, NFS, FTPS).
- Unlimited caches worldwide — replace a failed server by installing File Sync on a new one.
- **Cloud tiering** = most frequently accessed files are replicated locally; infrequently accessed files are kept in the cloud until requested.

### 🚚 Migrating to Azure (from Microsoft Learn)

**Azure Migrate** — a unified migration hub to assess and migrate on-premises infrastructure to Azure. Functions as a single portal to start, run, and track your migration.

| Capability | Detail |
|---|---|
| **Unified migration platform** | Single portal to start, run, and track migration |
| **Range of tools** | Includes Discovery and assessment + Server Migration. Integrates with other Azure services and **ISV tools** |
| **Integrated tools** | Discovery and assessment, server migration, database migration, web app migration |
| **Assessment and migration** | Assess and migrate on-premises infrastructure from the Migrate hub |

**Azure Data Box** — physical migration service for transferring large amounts of data when network bandwidth is limited. Ships a proprietary storage device (max **80 TB** usable capacity) via regional carrier in a rugged case. Ordered via Azure portal; entire process tracked end-to-end in the portal.

**Data Box use cases (from Microsoft Learn):** one-time bulk migration of on-premises data, periodic large uploads where online transfer is too slow, exporting large data sets from Azure for recovery or regulatory needs.

**Data Box workflow**: Order in portal → Receive device → Set up via local web UI → Connect to network → Transfer data → Return device → Data auto-uploaded to Azure → Device wiped per **NIST 800-88r1** standards. For export orders, disks are erased when the device reaches the Azure datacenter.

**Data Box variants:**

| Variant | Capacity | Interface | Notes |
|---|---|---|---|
| **Data Box Disk** | ~35 TB (5 SSDs) | USB (430 MB/s) | 1 storage account only |
| **Data Box** | 80 TB | 2x GbE + 2x GbE (data) | Up to 10 storage accounts; AES 256; tamper-resistant |
| **Data Box Heavy** | ~770 TB | 2x 40 GbE (data) | Shipped via freight carrier |

📌 **Key Points — Da ricordare**
- Storage account name: 3–24 chars, lowercase + numbers, globally unique. Each service has its own endpoint subdomain.
- Four storage account types: Standard GP v2 (recommended, all redundancy), Premium block blobs (LRS/ZRS), Premium file shares (LRS/ZRS, SMB+NFS), Premium page blobs (LRS only).
- Redundancy durability: LRS = 11 nines, ZRS = 12 nines, GRS/GZRS/RA-GRS/RA-GZRS = 16 nines. Geo-replication is async with RPO < 15 minutes (no SLA).
- Five storage services: Blobs (+ Data Lake Gen2), Files (SMB/NFS), Queues (async messaging, pairs with Functions), Disks (managed, block-level for VMs), Tables (NoSQL structured).
- Blob storage tiers: Hot → Cool (30d) → Cold (90d) → Archive (180d, rehydration needed). Archive cannot be set at account level.
- AzCopy = CLI, **one-way** sync, works cross-cloud. Storage Explorer = GUI, uses AzCopy on backend. Azure File Sync = **bi-directional**, cloud tiering, multisite caching.
- Azure Migrate = online, unified hub (discovery, assessment, server/DB/web app migration, ISV tools). Data Box = offline/physical, up to 80 TB (Heavy: ~770 TB), NIST 800-88r1 wipe.

---

## Skill 2.4: Azure Identity, Access, and Security

### 🆔 Directory Services (from Microsoft Learn)

**Authentication** = verifying identity (who are you?). **Authorization** = checking permissions (what can you do?).

**Microsoft Entra ID** (formerly Azure Active Directory) — Microsoft's cloud-based identity and access management service. Lets you sign in and access both Microsoft cloud applications and your custom applications. Key difference from on-premises AD: you control the identity accounts, Microsoft ensures the service is available globally. Connecting on-prem AD to Entra ID unlocks suspicious sign-in detection at no extra cost.

**Who uses Microsoft Entra ID (from Microsoft Learn):**

| Audience | How They Use It |
|---|---|
| **IT administrators** | Control access to apps and resources based on workload and security requirements |
| **App developers** | Add standards-based functionality (SSO, credential integration) to applications |
| **Users** | Manage their own identities (self-service password reset) |
| **Online service subscribers** | M365, Office 365, Azure, Dynamics CRM subscribers already authenticate via Entra ID |

**What Microsoft Entra ID provides (from Microsoft Learn):**

| Service | Detail |
|---|---|
| **Authentication** | Identity verification, self-service password reset, MFA, banned password lists, smart lockout |
| **Single sign-on (SSO)** | One identity to access multiple applications, fewer credentials to manage |
| **Application management** | Manage cloud and on-prem apps via Application Proxy, SaaS app integration, My Apps portal |
| **Device management** | Device registration via Microsoft Intune, device-based Conditional Access policies |

**Microsoft Entra Connect** — bridges on-premises Active Directory with Microsoft Entra ID. Synchronizes user identities **bi-directionally** between both systems. Users get a consistent experience including SSO, MFA, and self-service password reset for both on-prem and cloud resources.

**Microsoft Entra Domain Services** (formerly Azure AD DS) — provides managed domain services: **domain join, group policy, LDAP, and Kerberos/NTLM authentication** without deploying or maintaining domain controllers. Microsoft manages the DCs (a **replica set** of 2 Windows Server DCs). Especially useful for **legacy applications** that can't use modern authentication — lift-and-shift to a managed domain. Integrates with existing Entra tenant (existing groups and user accounts carry over).

**Sync direction (from Microsoft Learn)**: Entra ID performs a **one-way synchronization** down to Entra Domain Services. Resources created directly in the managed domain are NOT synced back to Entra ID. In hybrid environments: On-prem AD ↔ Entra Connect (bi-directional) → Entra ID → Entra Domain Services (one-way down).

### 🔐 Authentication Methods (from Microsoft Learn)

**Authentication Methods: Security vs Convenience (from Microsoft Learn):**

| Method | Factors Used | Security | Convenience | Key Risk/Benefit |
|---|---|---|---|---|
| **Password only** | Something you know | Low | High | Can be phished or guessed; reused across sites |
| **Multifactor (MFA)** | Something you know + something you have/are | Medium-High | Low | Blocks most credential attacks; extra step slows sign-in |
| **Passwordless** | Something you have + something you are/know | **Highest** | **Highest** | No password to steal; fast and convenient |

**Single Sign-On (SSO)** — lets a user sign in once and access multiple trusted applications. Reduces password sprawl, lowers credential-related incidents, decreases account lockout and reset overhead. Simplifies lifecycle management — access is tied to one identity, making it easier to update or remove access when roles change.

⚠️ **Exam Tip**: SSO is only as secure as the initial authenticator — all subsequent connections rely on that initial sign-in's security.

**Multifactor Authentication (MFA)** — prompts for an extra factor during sign-in so a compromised password alone isn't enough. Three factor categories: something the user **knows** (password/challenge), something the user **has** (phone code), something the user **is** (biometric/fingerprint/face scan). **Microsoft Entra multifactor authentication** is Microsoft's MFA service (phone call or mobile app notification as second factor).

**Passwordless Authentication (from Microsoft Learn)** — eliminates the password entirely, replacing it with a trusted device plus a biometric signal or PIN.

| Option | Authentication | Form Factor | Best For | Key Feature |
|---|---|---|---|---|
| **Windows Hello for Business** | Biometric or PIN | Built into Windows PC | Information workers with a dedicated PC | PKI + SSO integrated |
| **Microsoft Authenticator** | Number match + biometric/PIN | iOS or Android phone | Mobile and frontline workers (any platform) | Also supports MFA mode |
| **FIDO2 security keys** | Hardware cryptographic key | External USB/Bluetooth/NFC device | Shared workstations, high-security environments | Unphishable open standard (WebAuthn) |

### 👥 External Identities and Guest Access (from Microsoft Learn)

An **external identity** is a person, device, or service that exists outside your tenant. Microsoft Entra External ID includes the capabilities to interact with users beyond your tenant boundary. External identity providers handle **authentication**; your tenant (Entra ID or Azure AD B2C) handles **authorization**.

**Three External ID capabilities (from Microsoft Learn):**

| Capability | Who | How | Directory Presence | Best For |
|---|---|---|---|---|
| **B2B collaboration** | Partners, vendors, suppliers (work or social accounts) | Invitation or self-service sign-up into your tenant | ✅ Represented as **guest user objects** in your directory | Sharing internal apps, SaaS apps, custom apps |
| **B2B Direct Connect** | Users from another Microsoft Entra tenant | Mutual **two-way trust** between Entra tenants | ❌ Not in your directory; visible in Teams admin center reports only | **Teams shared channels** across organizations |
| **External ID for Customers** (formerly Azure AD B2C) | Consumers of your published SaaS or custom app | Sign-up/sign-in user flows with custom policies | Managed in a **separate** dedicated External ID tenant | Consumer-facing apps (excluding Microsoft apps) |

**Managing guest access over time**: use **access reviews** to recertify guest users' continued need for access. Reviewers provide input; after the review you can remove access for guests who no longer need it.

### 🚦 Conditional Access (from Microsoft Learn)

Conditional Access is a tool that Microsoft Entra ID uses to allow or deny access to resources based on **identity signals**. It evaluates every sign-in against your policies in real time.

**Three-step flow (from Microsoft Learn):**

**Signals** (input) → **Decision** (evaluate) → **Enforcement** (action)

| Step | Components |
|---|---|
| **Signals** | User or group membership, IP location, device platform, application targeted, real-time sign-in risk |
| **Decision** | Allow full access, require MFA, or block access |
| **Enforcement** | Grant with conditions, require compliant device, limit session, or block |

**Common Conditional Access scenarios (from Microsoft Learn):**
- Require MFA for admin roles from any location
- Allow email service only through approved client apps
- Require managed/compliant devices for sensitive apps
- Block access from unknown IP + high risk (sign-in denied)

⚠️ **Exam Tip**: Conditional Access provides granular MFA — a user may not be challenged from a known location but will be challenged from an unusual or high-risk location.

### 🎭 Role-Based Access Control (RBAC) — from Microsoft Learn

The **principle of least privilege**: grant access only to the level needed to complete a task. Azure RBAC provides built-in roles with predefined permissions. You can also define custom roles. When you assign individuals or groups to roles, they receive all the associated permissions.

Four elements: **Security principal** (user/group/app/managed identity) + **Role** (defines allowed actions) + **Scope** (management group/subscription/resource group/resource) + **Role assignment** (ties it all together).

| Built-in Role | Access Level |
|---|---|
| **Owner** | Full access + can delegate |
| **Contributor** | Can create/manage, but cannot delegate |
| **Reader** | View only |

- Role assignments are **additive** — your effective permissions are the union of all your role assignments.
- Enforced by ARM. A token with your identity and roles is checked on every operation.
- Scope: narrower scope = more specific control (resource > resource group > subscription > management group). Permissions assigned at a parent scope are **inherited by all child scopes** (e.g., Owner at management group → manages everything in all subscriptions below).
- **Group-based assignment**: add a new team member to the RBAC group → they automatically get the same access as other group members. Add a new resource to the group → everyone in the group gets permissions on the new resource.
- Azure RBAC uses an **allow model** — when assigned a role, you can perform actions within that role's scope. Multiple role assignments are additive (read + write = read and write).
- RBAC is enforced on any action through **Azure Resource Manager** (portal, Cloud Shell, PowerShell, CLI). It does **NOT** enforce access permissions at the application or data level — application security must be handled by your application.

### 🏰 Zero Trust Model (from Microsoft Learn)

Zero Trust assumes the worst-case scenario and verifies each request as though it originated from an uncontrolled network. Access decisions are **continuous and context-aware**, not based only on where the request originates.

**Three guiding principles (from Microsoft Learn):**

| Principle | What It Means |
|---|---|
| **Verify explicitly** | Always authenticate and authorize based on all available data points (identity, location, device, service, data classification) |
| **Use least privilege access** | Limit user access with **Just-In-Time and Just-Enough-Access (JIT/JEA)**, risk-based adaptive policies, and data protection |
| **Assume breach** | Limit the potential impact and segment access. Verify end-to-end encryption. Use analytics for visibility, threat detection, and defense improvement |

**Traditional Perimeter vs. Zero Trust (from Microsoft Learn):**
- Traditional: trust based on network location → firewall is the primary boundary → VPN grants full internal access → once inside, lateral movement is free.
- Zero Trust: never trust, always verify → identity-based, not location-based → continuous, context-aware decisions → every access request is evaluated.

### 🛡️ Defense in Depth (from Microsoft Learn)

A layered strategy that slows the advance of an attack aimed at acquiring unauthorized data access. No single layer provides complete protection — if one layer is breached, a subsequent layer is already in place.

**Seven layers (from Microsoft Learn — outermost to innermost):**

| Layer | Role | Key Actions |
|---|---|---|
| **Physical security** | Protect datacenter hardware | Building access controls, hardware security |
| **Identity and access** | Control who gets in | SSO, MFA, audit events and changes |
| **Perimeter** | Filter large-scale attacks | DDoS protection, perimeter firewalls |
| **Network** | Limit lateral movement | Deny by default, restrict inbound/outbound access, segment communication |
| **Compute** | Secure VMs and hosts | Secure VM access, endpoint protection, keep systems patched |
| **Application** | Secure by design | Secure development lifecycle, store secrets in **Azure Key Vault** |
| **Data** (center) | Ultimate target — protect confidentiality, integrity, availability | Encryption at rest and in transit, access controls, regulatory compliance |

### 🔐 Encryption and Key Management (from Microsoft Learn)

| Type | Protects Data | How | Examples |
|---|---|---|---|
| **Encryption at rest** | While stored | AES-256 / service-managed keys | Databases, disks, storage accounts |
| **Encryption in transit** | While moving between services, apps, and users | TLS / HTTPS / VPN tunnels | App tier ↔ API/service, user device ↔ Azure Storage |

A strong security posture uses **both** at-rest and in-transit encryption.

**Azure Key Vault** — centralized service for securely storing and controlling access to:

| What It Stores | Examples |
|---|---|
| **Secrets** | Connection strings, passwords, API keys — stored securely, never in code |
| **Encryption keys** | RSA and EC key pairs — HSM-backed key protection for at-rest and in-transit encryption |
| **Certificates** | TLS/SSL certificates — auto-renewal and lifecycle management |

**Why key management matters**: access control (who can view and use keys), key rotation (rotate and update keys over time with alerting before expiry), usage auditing (track key and secret usage). Managed identities retrieve secrets from Key Vault at runtime, eliminating hard-coded credentials. Separation of duties limits who can view, use, and rotate keys.

### 🛡️ Microsoft Defender for Cloud (from Microsoft Learn)

Security posture management and threat protection service. Monitors cloud, on-premises, hybrid, and multicloud resources. Provides recommendations and alerts to improve security posture. Azure-native — many Azure services monitored without extra deployment. **Azure Arc** extends Defender to non-Azure machines; **CSPM** capabilities assess multicloud resources agentlessly.

**Three pillars — Assess, Secure, Defend (from Microsoft Learn):**

| Pillar | Goal | Key Actions |
|---|---|---|
| **Continuously Assess** | Know your security posture | Identify and track vulnerabilities, VM vulnerability scans, container registry assessments, SQL server assessments, Defender for Endpoint integration |
| **Secure** | Harden resources and services | **MCSB** security policies, Azure Policy integration, prioritized recommendations, **Secure Score** tracking; scoped at management group / subscription / tenant |
| **Defend** | Detect and resolve threats | Security alert generation, kill-chain attack correlation, remediation guidance, advanced threat protection, **just-in-time VM access** |

**Coverage**: Azure-native, hybrid (Azure Arc), multicloud (AWS: CSPM + EKS containers + EC2 servers; GCP: similar).

**Azure-native protections (from Microsoft Learn)**: threat detection for Azure PaaS services (App Service, Azure SQL, Storage), data security assessments and recommendations for Azure SQL and Storage, network protections including just-in-time VM access and restrictive port policies.

**Security alerts**: describe affected resources, suggest remediation steps, can trigger a Logic App in response. Uses **kill-chain analysis** to correlate related alerts and show the full attack story.

📌 **Key Points — Da ricordare**
- Microsoft Entra ID provides: authentication (MFA, password reset, smart lockout), SSO, app management, device management.
- Entra Connect syncs on-prem AD ↔ Entra ID (bi-directional). Entra Domain Services syncs one-way DOWN from Entra ID (domain join, LDAP, Kerberos/NTLM, group policy — no DCs to manage).
- Auth spectrum: Password (low security, high convenience) → MFA (medium-high security, low convenience) → Passwordless (highest security AND convenience).
- Three passwordless options: Windows Hello (PC, PKI+SSO), Authenticator app (phone, also does MFA), FIDO2 keys (USB/BT/NFC, unphishable, shared workstations).
- External ID: B2B collaboration (guest users in directory), B2B Direct Connect (Teams shared channels, NOT in directory), External ID for Customers (consumer apps, separate tenant).
- Conditional Access flow: Signals (user/location/device/app/risk) → Decision (allow/MFA/block) → Enforcement (grant with conditions/require compliant device/block).
- RBAC: least privilege, additive (allow model), hierarchical inheritance. Does NOT enforce at app or data level.
- Zero Trust 3 principles: verify explicitly, least privilege access (JIT/JEA), assume breach. Identity-based, not location-based.
- Defense in Depth 7 layers (outside→in): physical → identity → perimeter → network → compute → application → data.
- Encryption: at rest (AES-256) + in transit (TLS/HTTPS/VPN). Azure Key Vault stores secrets, keys, certificates centrally.
- Defender for Cloud: Assess (vulnerabilities, Secure Score) → Secure (MCSB, Azure Policy) → Defend (alerts, kill-chain, JIT VM access). Covers Azure + hybrid (Arc) + multicloud (AWS, GCP).
