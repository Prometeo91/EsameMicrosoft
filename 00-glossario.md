# 00 — Glossary of Key Terms (AZ-900)

> Alphabetically sorted. Duplicates consolidated. Cross-references marked with "→ See".

---

| Term | Definition |
|---|---|
| **ACI (Azure Container Instances)** | Serverless service for running Docker containers without managing VMs; pay only for CPU/memory used. Fastest and simplest container option in Azure. |
| **AKS (Azure Kubernetes Service)** | Managed Kubernetes cluster service; Azure manages the control plane, you deploy containers. Best for enterprise-scale container deployments. |
| **Alias Record** | Azure DNS record set that points directly to an Azure resource (public IP, Traffic Manager, CDN). Seamlessly updates when the resource's IP address changes — no manual DNS change needed. |
| **Anycast** | Networking technique used by Azure DNS where each DNS query is answered by the closest available server, providing fast performance and high availability. |
| **Application Insights** | Azure Monitor feature for monitoring web app performance and usage (Azure, on-prem, other clouds). Setup via SDK or agent (no code changes). Tracks requests, dependencies, page loads, server perf. Availability tests send synthetic requests. |
| **ARM (Azure Resource Manager)** | Deployment and management service for Azure. Management layer that authenticates, authorizes, and routes all requests — whether from portal, CLI, PowerShell, APIs, or SDKs. Six benefits: declarative templates, group management, consistent re-deployment, dependency ordering, native RBAC, tagging. |
| **ARM Template** | Declarative JSON file that defines Azure resources and their properties for repeatable deployments. Idempotent. ARM validates before deployment and orchestrates in the right order and in parallel when possible. |
| **Auto-Scale** | Azure feature that automatically adds or removes resources based on usage patterns, metrics, or schedules. |
| **Availability Set** | Logical grouping of VMs across fault domains (racks) and update domains within a single datacenter; guarantees **99.95% SLA**. No additional cost (you pay for VM instances only). |
| **Availability Zone** | Physically separate datacenter within an Azure region with independent power, cooling, and networking; guarantees **99.99% SLA** for multi-zone VMs. Minimum 3 zones per enabled region. |
| **AVD (Azure Virtual Desktop)** | PaaS desktop virtualization service; users access OS and apps remotely via clients or web browser. Supports single-session and multi-session Windows. Integrates with Entra ID. |
| **Azure Activity Log** | Platform log recording who did what and when on Azure resources (ARM-level operations). Retained for 90 days. Shows create, update, delete, and other management operations. |
| **Azure AD** | → See **Microsoft Entra ID** (former name). |
| **Azure AD Connect** | → See **Microsoft Entra Connect** (former name). |
| **Azure AD DS** | → See **Microsoft Entra Domain Services** (former name). |
| **Azure Advisor** | Personalized best-practices guide built into the portal. Five categories: **Reliability, Security, Performance, Operational Excellence, Cost** ("Capacity" is NOT a category). Recommendations can be taken, postponed, or dismissed. Filterable by subscription, resource group, or service. Notifications available for new recommendations. |
| **Azure App Service** | HTTP-based PaaS for hosting web applications, REST APIs, and mobile back ends. Supports .NET, Java, Ruby, Node.js, PHP, Python on Windows or Linux. Four types: Web apps, API apps, WebJobs, Mobile apps. Built-in auto-scaling, load balancing, deployment slots. ⚠️ Plans bill even with no running apps — delete the plan to stop charges. |
| **Azure Arc** | Service that extends Azure management and governance (RBAC, Policy, tags) to on-premises and multi-cloud resources via ARM. Five resource types: servers, Kubernetes clusters, Azure data services, SQL Server, VMs (preview). Supports custom locations on Arc-enabled K8s. |
| **Azure Bastion** | Managed PaaS service for secure RDP/SSH access to VMs directly through the Azure portal over TLS, without exposing a public IP on the VM. Eliminates the need for a jump box. |
| **Azure Blob Storage** | Storage service for unstructured data (Block Blobs, Append Blobs, Page Blobs) organized in containers. Includes Data Lake Storage Gen2 for big data analytics. |
| **Azure Blueprints** | Service for packaging ARM templates, policies, RBAC, and resource groups into reusable, versioned deployment definitions. ⚠️ **Being retired** — replaced by **Template Specs** + **Deployment Stacks**. Existing content may still appear on the exam during transition. |
| **Azure CLI** | Cross-platform command-line interface (Bash-based) for managing Azure resources; functionally equivalent to PowerShell. |
| **Azure Cloud Shell** | Browser-based shell (PowerShell or Bash) accessible from the portal or Azure mobile app; auto-authenticated, no local install required; persists files in Azure Storage. |
| **Azure Container Apps** | Managed container hosting PaaS between ACI and AKS. Built-in load balancing and scaling. Elastic app layer for containers. |
| **Azure Cost Management and Billing** | Portal tool for analyzing costs, creating budgets, and setting spending alerts. Three components: Cost Analysis (view/explore), Cost Alerts (budget + credit + dept quota), Budgets (spending limits + automation). |
| **Azure Data Box** | Offline data migration service (Disk: ~35 TB, Data Box: 80 TB, Heavy: ~770 TB) for transferring large datasets to/from Azure. Device wiped per NIST 800-88r1 standards. |
| **Azure DDoS Protection** | Network protection service. **Basic** (free, automatic, common attacks). **Standard** (paid, 60+ attack types, DDoS Rapid Response team, cost guarantee/service credit). Combine with WAF for L3/L4 + L7 protection. |
| **Azure Disks** | Managed block-level storage volumes for VMs; available as HDD or SSD (Standard/Premium). Max size 32,767 GiB per disk. |
| **Azure DNS** | Service for hosting and managing DNS records (public and private zones) within Azure. ⚠️ Azure DNS cannot buy domain names (not a registrar). |
| **Azure Event Grid** | Serverless event routing service using pub/sub model; push events to destinations; pay per use. |
| **Azure ExpressRoute** | Dedicated, private fiber-optic connection to Azure (up to 10 Gbps) via a service provider or ExpressRoute Direct. A connection is called a **circuit**. Each circuit uses redundant connections for HA. Does NOT traverse the public internet. |
| **Azure File Sync** | Service that synchronizes Azure Files shares with on-premises Windows servers for local caching. **Bi-directional** sync. Supports cloud tiering (frequent files local, infrequent in cloud). |
| **Azure Files** | Fully managed cloud file share; mountable on Windows (SMB), Linux, and macOS (SMB + NFS). Requires TCP port 445. |
| **Azure Firewall** | Cloud-native, stateful network firewall for protecting Azure VNet resources. Filters traffic across multiple VNets and subscriptions centrally. |
| **Azure Front Door** | Modern cloud CDN (Content Delivery Network). Combines CDN, global load balancing, and WAF in one service using Microsoft's global edge network. |
| **Azure Functions** | Serverless compute service for running event-driven microservices; pay only for execution time. **Stateless** by default; **Durable Functions** add stateful capabilities. Triggers: HTTP, Timer, Queue. ⚠️ Cold start penalty after idle periods. |
| **Azure Hybrid Benefit** | Program to bring your own Windows Server or SQL Server license to Azure for significant cost savings (40%+). |
| **Azure Key Vault** | Centralized service for securely storing and controlling access to **secrets** (passwords, connection strings), **encryption keys** (RSA/EC, HSM-backed), and **certificates** (TLS/SSL with auto-renewal). Eliminates hard-coded credentials via managed identities. |
| **Azure Logic Apps** | Serverless service for automating and orchestrating tasks, workflows, and business processes using prebuilt connectors. Foundation for Power Automate. |
| **Azure Machine Learning** | Platform for building, training, and managing custom ML models. For model development, experimentation, and lifecycle management. |
| **Azure Marketplace** | Online store for purchasing Azure-based solutions and services from third-party vendors. All solutions certified and compliant with Azure policies. You pay Azure costs plus vendor costs (billing structures set by vendor). |
| **Azure Migrate** | Unified migration hub to assess and migrate on-premises infrastructure to Azure. Single portal to start, run, and track migration. Includes discovery and assessment, server/DB/web app migration, ISV tool integration. |
| **Azure Mobile App** | iOS/Android app for managing, monitoring, and troubleshooting Azure resources; includes Cloud Shell access. |
| **Azure Monitor** | Platform for collecting, analyzing, and acting on data from Azure, on-prem, and multicloud. Data platform: Metrics, Logs, Traces. Outputs: Experiences, Visualize (Workbooks, Dashboards, Power BI, Grafana), Analyze (Metric Explorer, Log Analytics), Respond (Alerts & Actions, Autoscale), Integrate (Event Hubs, Logic Apps). |
| **Azure OpenAI Service** | Azure-hosted access to OpenAI's generative AI models (chat, content generation) with built-in security and governance controls. |
| **Azure Policy** | Service for creating, assigning, and managing policies that control or audit Azure resources. Can prevent noncompliant resources from being created and auto-remediate. Policies are inherited downward. Supports initiatives (groups of policies). Evaluates existing resources retroactively. Enforces standards even for AI-assisted/Copilot changes. |
| **Azure Queues** | Message queue storage service for decoupling application components; max message 64 KB, max queue ~500 TiB. Commonly paired with Azure Functions for trigger-based processing. |
| **Azure Reservations** | Commitment to 1- or 3-year resource usage for discounted pricing (up to 72% off vs. pay-as-you-go). Applies to specific resource types. |
| **Azure Savings Plan** | Commitment-based pricing for compute services. Commit to an hourly spend amount for 1 or 3 years across eligible compute services (flexible across VM families). Up to 65% savings. |
| **Azure Service Health** | Three views narrowing in scope: **Azure Status** (global, all services/regions) → **Service Health** (your services/regions, with alerts for outages/maintenance/advisories) → **Resource Health** (individual resource — running normally or problem, Azure's side or yours). Historical alerts retained for trends. |
| **Azure Spot VMs** | VMs running on Microsoft's unused capacity at deep discount (up to 90% off) for interruptible/fault-tolerant workloads. Azure can reclaim at any time. |
| **Azure Spring Cloud** | PaaS for hosting Java Spring applications with Azure integration. (Niche — renamed Azure Spring Apps.) |
| **Azure Stack** | Validated hardware + software package for running Azure services on-premises (hybrid cloud). |
| **Azure Support Plans** | Five tiers: **Basic** (free, NO tech tickets) → **Developer** (email, biz hours, ~$29/mo) → **Standard** (24/7 phone+email, <1hr Sev A, ~$100/mo) → **Professional Direct** (24/7+advisory, <15min Sev A, ~$1K/mo) → **Premier/Unified** (TAM, enterprise contract). |
| **Azure Tables** | NoSQL storage service for large amounts of structured, non-relational data. Accessible through authenticated calls from cloud and hybrid environments. |
| **Azure VMware Solution** | Service that lets you run VMware workloads in Azure with seamless integration and scalability. For migrating from VMware private cloud to Azure. |
| **Azure VPN Gateway** | Service for creating encrypted VPN connections (IPSec/IKE) between VNets or to on-premises networks. Also called virtual network gateway. Only one VPN gateway per VNet. Default: active/standby (auto failover). Can take up to 45 min to create. |
| **B2B Direct Connect** | Microsoft Entra External ID capability for cross-tenant collaboration via mutual two-way trust. Currently supports Teams shared channels. Users are NOT represented in your directory. |
| **BCDR** | Business Continuity and Disaster Recovery — planning for data backup and application replication across regions. |
| **BGP (Border Gateway Protocol)** | Dynamic routing protocol used by ExpressRoute and active/active VPN gateways to exchange routes between on-premises and Azure networks. |
| **Bicep** | Declarative language for deploying Azure resources through ARM. Simpler and more concise than JSON ARM templates. Idempotent. Supports modularity via Bicep modules. |
| **Billing Zone** | One of four geographic groups of Azure regions used to determine network egress pricing. Different from availability zones. |
| **Budgets** | Feature within Azure Cost Management for setting spending limits by subscription, resource group, or service type. Triggers budget alerts + email notifications. Can configure automation to suspend/modify resources at thresholds. |
| **CapEx** | Capital Expenditure — upfront spending on physical infrastructure. Associated with on-premises/private datacenter scenarios. Decreases with cloud adoption. |
| **Cloud Adoption Framework** | Microsoft's guidance for business and technology strategies for Azure adoption; includes five disciplines of cloud governance. |
| **Cloud Agility** | The speed and ease with which cloud resources can be provisioned or scaled (seconds vs. hours). |
| **Cold Tier** | Blob storage tier between Cool and Archive. Min 90 days retention. Online (fast retrieval). Lower storage cost than Cool, higher access cost. |
| **Composite SLA** | The effective SLA when an application depends on multiple Azure services. Calculated by multiplying the individual SLAs (e.g., 99.95% × 99.99% = 99.94%). |
| **Conditional Access** | Microsoft Entra ID tool that allows or denies access to resources based on identity signals. Three-step flow: **Signals** (user, location, device, app, risk) → **Decision** (allow/MFA/block) → **Enforcement** (grant with conditions/block). Premium tier only. |
| **Consumption-Based Model** | Pricing model where you pay only for the resources you actually consume. Cloud shifts from CapEx to OpEx. |
| **Copilot in Azure** | AI assistant experience in Azure that provides contextual guidance in natural language. Helps with exploring services, understanding configurations, and drafting commands/scripts. Some workflows are agent-like (multi-step). Treat as operational assistant — humans validate and approve changes. |
| **Cost Analysis** | Feature within Azure Cost Management that provides a visual overview of costs by billing cycle, region, resource group, or service. Used to explore, aggregate, and estimate spending trends. |
| **CSPM (Cloud Security Posture Management)** | Capability of Defender for Cloud that assesses multicloud resources agentlessly for security posture and compliance. |
| **Data Lake Storage Gen2** | Big data analytics capability built on top of Azure Blob Storage. Endpoint: `<account>.dfs.core.windows.net`. |
| **Data Lineage** | Tracking how data flows from source to destination across systems. A core capability of Microsoft Purview for understanding data provenance and transformations. |
| **Defense in Depth** | Multi-layered security strategy. Seven layers (outside→in): Physical → Identity & Access → Perimeter → Network → Compute → Application → Data. No single layer provides complete protection. |
| **Deployment Stacks** | ARM feature for managing groups of resources as a single unit. Replacement (with Template Specs) for retiring Azure Blueprints. |
| **Durable Functions** | Stateful extension of Azure Functions. The runtime passes a context to track prior activity across invocations. |
| **Economies of Scale** | Doing things more efficiently or at lower cost per unit when operating at larger scale. Drives cloud pricing advantages. |
| **Elasticity** | Ability to **automatically** scale resources up/down or out/in based on demand. Requires scalability but adds automation. |
| **ExpressRoute Circuit** | A private connection between your on-premises network and the Microsoft cloud via a connectivity provider. Does not travel over the public internet. |
| **ExpressRoute Global Reach** | Feature that connects your on-premises sites to each other through ExpressRoute circuits via the Microsoft backbone — private site-to-site path without public internet. |
| **Fault Domain** | Logical representation of a physical server rack in an availability set; protects against hardware failures. Default: 2 per availability set. |
| **Fault Tolerance** | Automatic movement from unhealthy to healthy resources without user intervention. Handles component-level failures. ≠ scaling (which assumes all VMs are healthy). |
| **FIDO2** | Security key standard for passwordless authentication. External USB/Bluetooth/NFC device. Unphishable (WebAuthn). Best for shared workstations and high-security environments. |
| **Geography** | Azure boundary (often a country) that ensures data-handling regulations are met. Contains two or more regions. |
| **GRS** | Geo-Redundant Storage — 3 LRS copies in primary region + 3 LRS copies in a secondary region (async). 16 nines durability. |
| **GZRS** | Geo-Zone-Redundant Storage — 3 ZRS copies in primary + 3 LRS copies in a secondary region. 16 nines durability. Highest redundancy option. |
| **IaaS** | Infrastructure-as-a-Service — provider manages hardware; you manage OS, middleware, and apps. Most control, most responsibility. "You rent hardware — what you do with it is up to you." |
| **IaC (Infrastructure as Code)** | Managing infrastructure through code (e.g., ARM templates, Bicep). Same code produces the same environment every time (idempotent). Key DevOps practice. |
| **Idempotent** | Property of ARM templates and Bicep: deploying the same template multiple times always produces the same result without duplicates. |
| **Initiative** | A group of related Azure Policy definitions applied together to track compliance toward a larger goal. Example: "Enable Monitoring in Security Center" contains 100+ policy definitions. |
| **IoT Central** | Simplified SaaS IoT platform for solution builders. |
| **IoT Edge** | Extends Azure cloud capabilities to edge devices so workloads run closer to where data is generated. |
| **IoT Hub** | Azure service for secure, bi-directional communication between cloud services and IoT devices. Supports millions of simultaneously connected devices. |
| **JIT/JEA (Just-In-Time / Just-Enough-Access)** | Zero Trust principles for limiting user access: grant permissions only when needed (JIT) and only the minimum required (JEA). Risk-based adaptive policies. |
| **Kill-chain Analysis** | Defender for Cloud feature that automatically correlates related security alerts to show the full story of an attack — where it started, which resources were affected, and impact. |
| **KQL (Kusto Query Language)** | Query language used in Azure Log Analytics for analyzing large-scale monitoring data. |
| **Lift-and-Shift** | Migrating an existing application to the cloud with minimal or no code changes. Common with **IaaS** — set up cloud resources similar to on-prem, then move workloads. |
| **Log Analytics** | Azure portal tool for writing and running queries (KQL) against data Azure Monitor collects. Simple filtering to advanced trend analytics. |
| **LRS** | Locally Redundant Storage — 3 copies in the same datacenter (synchronous). Cheapest, least durable (11 nines). NOT recommended for high-availability applications. |
| **Managed Identity** | Azure AD identity automatically managed by Azure for service-to-service authentication. Eliminates hard-coded credentials. |
| **Management Group** | Logical container for organizing Azure subscriptions; max 10,000 groups, **6 levels deep** (excluding root and subscription level). Policies and RBAC applied at MG level inherit downward. |
| **MCSB (Microsoft Cloud Security Benchmark)** | Security guidance framework used by Defender for Cloud to evaluate resources and surface prioritized recommendations. Controls scoped at management group, subscription, or tenant level. |
| **MFA** | Multifactor Authentication — requires two or more verification factors: something you **know** (password) + something you **have** (phone/key) + something you **are** (biometric). |
| **Microsoft Defender for Cloud** | Security posture management and threat protection service. Three pillars: **Assess** (vulnerabilities, Secure Score) → **Secure** (MCSB, Azure Policy) → **Defend** (alerts, kill-chain, JIT VM access). Covers Azure + hybrid (Arc) + multicloud (AWS, GCP). |
| **Microsoft Entra Connect** | Tool that synchronizes user identities **bi-directionally** between on-premises Active Directory and Microsoft Entra ID. Enables SSO, MFA, and password reset across both environments. (Formerly Azure AD Connect.) |
| **Microsoft Entra Domain Services** | Managed domain services (domain join, group policy, LDAP, Kerberos/NTLM) without deploying domain controllers. **One-way sync** from Entra ID down. Ideal for legacy app lift-and-shift. (Formerly Azure AD DS.) |
| **Microsoft Entra External ID** | Umbrella for external identity capabilities: **B2B collaboration** (guest users in your directory), **B2B Direct Connect** (Teams shared channels, NOT in directory), and **External ID for Customers** (consumer apps, separate tenant; formerly Azure AD B2C). |
| **Microsoft Entra ID** | Cloud-based identity and access management service for authentication and authorization. Provides: authentication (MFA, password reset, smart lockout), SSO, application management, device management. (Formerly Azure Active Directory / Azure AD.) |
| **Microsoft Purview** | Family of data governance, risk, and compliance solutions providing a unified view of data across on-premises, multicloud, and SaaS. Three capabilities: automated data discovery, sensitive data classification, end-to-end data lineage. Two solution areas: Risk and Compliance (powered by M365) and Unified Data Governance. |
| **Multi-tenant** | Public cloud environment where infrastructure is shared among multiple organizations. |
| **Multicloud** | Cloud deployment model using two or more public cloud providers simultaneously. Azure Arc helps manage multicloud environments. |
| **Non-regional Services** | Azure services that are always available from Azure geographies and resilient to both zone-wide and region-wide outages. Examples: Microsoft Entra ID, Traffic Manager, Azure DNS. |
| **NSG (Network Security Group)** | Firewall rules for allowing/denying traffic to Azure resources based on IP, port, and protocol. Rules evaluated by priority; **first match wins**. Default action if no rule matches: **deny**. |
| **NVA (Network Virtual Appliance)** | Specialized VM that performs a network function such as firewall, intrusion detection, or WAN optimization. |
| **OATH Token** | Open Authentication standard for generating time-based one-time passwords (TOTP). Available as software (Authenticator app) or hardware (key fob). |
| **OpEx** | Operational Expenditure — pay-as-you-go spending on services/products. Associated with cloud consumption. Increases with cloud adoption. |
| **PaaS** | Platform-as-a-Service — provider manages infrastructure + OS + middleware; you manage your application code and data. "Balanced" control and responsibility. |
| **Passwordless Authentication** | Authentication using a device/key + biometrics (or PIN) instead of a password. Three options: Windows Hello for Business (PC), Microsoft Authenticator (phone), FIDO2 security keys (external device). Highest security AND convenience. |
| **Predictability** | Two dimensions in cloud: **Performance predictability** (autoscaling, load balancing, HA) and **Cost predictability** (real-time tracking, analytics, Pricing Calculator). |
| **Pricing Calculator** | Tool for estimating potential Azure expenses before deployment (https://azure.microsoft.com/pricing/calculator). Nothing is provisioned. Also serves as the current tool for migration cost estimation since TCO Calculator was retired. |
| **Private Endpoint** | Grants access to a specific PaaS resource instance via a **private IP** in your VNet, connected through **Azure Private Link**. Not accessible from public internet. Enables on-prem access without public endpoint. |
| **RA-GRS** | Read-Access Geo-Redundant Storage — GRS with read access to the secondary region **before failover**. URL uses `-secondary` suffix. Not available for Azure Files. |
| **RA-GZRS** | Read-Access Geo-Zone-Redundant Storage — GZRS with read access to the secondary region before failover. Highest availability option. |
| **RBAC** | Role-Based Access Control — controls what users can do with Azure resources based on role assignments. **Additive** (allow model): effective permissions = union of all assigned roles. Inherited downward. Does NOT enforce at application or data level. |
| **Region** | A set of Azure datacenters in a specific geographic area, connected by a dedicated low-latency network. |
| **Regional Pair** | Two regions in the same geography, at least **300 miles apart**, updated sequentially by Microsoft. Advantages: prioritized restoration, staggered updates, same-geography data residency. |
| **Rehydration** | Process of moving a Blob from Archive tier to Hot or Cool tier for access. Required before any read operation on archived data. |
| **Resource Group** | Logical container for organizing related Azure resources. One resource → one group. No nesting. No renaming. Cross-region allowed. Delete group = delete ALL resources inside. ⚠️ NOT a security boundary — controls management and permissions, not network isolation. |
| **Resource Health** | Azure Service Health view that zooms in on individual resources (e.g., a specific VM). Shows whether a resource is running normally or experiencing a problem, and whether the issue is on Azure's side or yours. |
| **Resource Lock** | Prevents accidental deletion (**Delete** lock) or modification (**ReadOnly** lock) of an Azure resource regardless of RBAC. Inherited by child resources. To modify a locked resource: remove lock first, then act. Requires Owner or User Access Administrator role. |
| **RPO (Recovery Point Objective)** | The interval between the most recent write to the primary region and the last write replicated to the secondary. Azure Storage RPO is typically < 15 minutes (no SLA). |
| **SaaS** | Software-as-a-Service — provider manages everything; you use the software (e.g., M365, Gmail). Least control, least responsibility. You manage data + identity only. |
| **Scalability** | The system **can** add/remove resources to meet demand (capability). Vertical = more powerful VM. Horizontal = more VMs. ≠ Elasticity (which adds automation). |
| **Scale Set (VMSS)** | Service for deploying and auto-scaling up to 1,000 identical, load-balanced VMs. Supports distribution across availability zones. |
| **Secure Score** | Metric in Defender for Cloud that groups security recommendations into controls and calculates a score so teams can quickly understand posture and prioritize improvements. |
| **Service Endpoint** | Locks down access to all instances of a PaaS service to a VNet. Still accessible from public internet. (Compare with Private Endpoint = specific resource, fully private.) |
| **Service Principal** | An application identity in Azure AD used for app-to-resource authentication via RBAC. |
| **Service Trust Portal** | Microsoft's portal for security, privacy, and compliance information (https://servicetrust.microsoft.com/). Requires Microsoft Entra work/school account + NDA. Menus: Service Trust Portal, My Library (pin + notifications), All Documents. Reports available 12+ months. |
| **Shared Responsibility Model** | Principle that cloud responsibility is always shared between you and the cloud provider. How much shifts depends on service type (IaaS/PaaS/SaaS). Always yours: data, identities, devices. Always provider's: physical DC, network, hosts. |
| **Single-tenant** | Private cloud environment dedicated to a single organization. |
| **SLA** | Service-Level Agreement — provider's guarantee of a certain uptime percentage. Key numbers: 99% = 3.65 days/yr, 99.9% = 8.76 hrs/yr, 99.99% = 52.6 min/yr. |
| **Sovereign Region** | Isolated Azure cloud for specific government or regulatory compliance (e.g., Azure Government, Azure China 21Vianet). |
| **SSO** | Single Sign-On — access multiple resources with one set of credentials. Only as secure as the initial authenticator. |
| **Storage Account** | Provides a unique namespace (3–24 chars, lowercase + numbers, globally unique) for Azure Storage data accessible via HTTP/HTTPS. Contains one or more services and is protected by a redundancy option. |
| **Subscription** | Azure billing and access-control boundary with a unique subscription ID and resource quotas. Two boundaries: **billing** (separate invoices) and **access control** (separate policies). An account can have multiple subscriptions. |
| **Sustainability** | Cloud computing supports sustainability via: **Right-size** → **Automate** → **Optimize** → **Monitor**. A new AZ-900 learning objective. |
| **Tag** | Name/value pair applied to Azure resources for categorization, cost tracking, and filtering. ⚠️ Tags do NOT inherit from resource groups or subscriptions. Max 50 tags per resource. Six use cases: resource management, cost management, operations management, security, governance/compliance, workload optimization. |
| **TCO Calculator** | Tool for estimating cost savings when migrating from on-premises to Azure. ⚠️ **Deprecated August 2025.** The Pricing Calculator is now the recommended tool for all cost estimation scenarios. May still appear on the exam during transition. |
| **Template Specs** | Pre-built ARM templates stored in Azure for reuse across deployments. Replacement (with Deployment Stacks) for retiring Azure Blueprints. |
| **UDR (User-Defined Routes)** | Custom routing rules that control traffic flow between subnets within or between virtual networks. |
| **Update Domain** | Logical grouping in an availability set ensuring Azure reboots only one group at a time during updates. Default: 5 per availability set. Azure waits 30 minutes between each. |
| **VNet (Virtual Network)** | Azure virtual network enabling communication between Azure services, the internet, and on-premises. Supports isolation, segmentation (subnets), and connectivity (peering, VPN, ExpressRoute). |
| **VNet Peering** | Connection between two VNets over Microsoft's backbone. Global VNet peering = across regions. ⚠️ Requires **non-overlapping IP address ranges**. Traffic is private, never enters public internet. |
| **WAF (Web Application Firewall)** | Application-layer (L7) protection for web apps against common exploits (SQL injection, XSS). Complements Azure DDoS Protection (L3/L4). Available in Azure Front Door and Application Gateway. |
| **Well-Architected Framework** | Microsoft's set of guiding tenets for improving workload quality. Five pillars: Reliability, Security, Cost Optimization, Operational Excellence, Performance Efficiency. Reliability = resiliency + availability. |
| **Zero Trust** | Security framework that assumes every access attempt is a potential breach. Three principles: **Verify explicitly**, **Use least privilege access** (JIT/JEA), **Assume breach**. Identity-based, not location-based. |
| **ZRS** | Zone-Redundant Storage — 3 copies across 3 availability zones in the same region (synchronous). 12 nines durability. Data stays available for read+write even if one zone is unavailable. |
