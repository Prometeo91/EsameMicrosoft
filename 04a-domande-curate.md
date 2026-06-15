# 04a — Domande Curate (Libro, Corso, Microsoft Learn)

> **~119 domande** — Sezioni A (Cloud Concepts, 12), B (Architecture & Services, 22), C (Management & Governance, 16), D (Microsoft Learn, 35), G (Scott Duffy Quiz, 34).
>
> ⚠️ **Errata**: Alcune risposte da fonti terze contengono errori noti, segnalati con ⚠️. In caso di dubbio, fare riferimento ai file di studio 01–03.

---

## Section A: Cloud Concepts (Skill 1.1 – 1.3)

### Multiple Choice

**A1.** In the shared responsibility model, which of the following is ALWAYS the cloud provider's responsibility, regardless of service type?
- a) Application code
- b) Data governance
- c) Physical infrastructure security
- d) Operating system patching

**A2.** A company needs to keep all data on a network accessible only to its own employees, with no internet exposure. Which cloud model best fits?
- a) Public cloud
- b) Hybrid cloud
- c) Private cloud
- d) Community cloud

**A3.** Which cloud model combines on-premises resources with public cloud services?
- a) Private cloud
- b) Public cloud
- c) Hybrid cloud
- d) Multi-cloud

**A4.** A company wants to deploy a custom web application to the cloud without managing the OS or middleware. Which service type is most appropriate?
- a) IaaS
- b) PaaS
- c) SaaS
- d) FaaS

**A5.** Which of the following is a characteristic of SaaS?
- a) You install and manage the application
- b) You manage the OS and middleware
- c) The provider manages everything; you use the software
- d) You have remote access to the underlying VMs

**A6.** Your company uses Azure VMs and wants to automatically add VMs when demand increases and remove them when it drops. What concept describes this?
- a) Fault tolerance
- b) Disaster recovery
- c) Elasticity
- d) High availability

**A7.** What is the key difference between scaling up and scaling out?
- a) Scaling up adds more VMs; scaling out adds more power
- b) Scaling up moves to a more powerful VM; scaling out adds more identical VMs
- c) There is no difference
- d) Scaling up is automatic; scaling out is manual

### True / False

**A8.** A private cloud must be hosted on-premises and owned by the company using it. **TRUE / FALSE**

**A9.** Fault tolerance automatically moves your workload from an unhealthy VM to a healthy one without any interaction from you. **TRUE / FALSE**

**A10.** In a PaaS service, you are responsible for the operating system and installed components. **TRUE / FALSE**

**A11.** You are charged for an Azure App Service plan even if no web apps are running in it. **TRUE / FALSE**

**A12.** The consumption-based model means you pay for cloud resources only when they are actively being used. **TRUE / FALSE**

---

### Answers — Section A

| # | Answer | Explanation |
|---|---|---|
| A1 | **c** | The cloud provider always manages physical infrastructure (servers, network hardware, datacenter facilities). OS patching depends on the service type (your responsibility in IaaS). |
| A2 | **c** | A private cloud operates on a private network accessible only to one organization, meeting the requirement for no internet exposure. |
| A3 | **c** | Hybrid cloud is a mixture of public and private clouds, often connecting on-premises systems with public cloud services. |
| A4 | **b** | PaaS manages the OS and middleware for you — you only deploy and manage your application code. |
| A5 | **c** | SaaS means the provider manages the entire stack (infrastructure, OS, middleware, application). You simply use the software. |
| A6 | **c** | Elasticity is the ability to automatically scale resources up/down and out/in based on demand. |
| A7 | **b** | Scaling up (vertical) = move to a more powerful VM. Scaling out (horizontal) = add more identical VMs. |
| A8 | **FALSE** | A private cloud can be hosted at a third-party data center. What matters is that the infrastructure is dedicated to a single organization. |
| A9 | **TRUE** | Fault tolerance is automatic — the cloud provider monitors health and moves workloads without user interaction. |
| A10 | **FALSE** | In PaaS, the cloud provider manages the OS and middleware. You are only responsible for your application code. |
| A11 | **TRUE** | App Service plans are billed as long as they exist, even with no running apps. Delete the plan to stop billing. |
| A12 | **TRUE** | The consumption-based model charges only for resources consumed (e.g., compute time, storage used). |

---

## Section B: Azure Architecture and Services (Skill 2.1 – 2.4)

### Multiple Choice

**B1.** How does Azure maintain disaster recovery across its infrastructure?
- a) By using availability sets within a single datacenter
- b) By having at least two regions per geography separated by hundreds of miles
- c) By using a single datacenter with backup generators
- d) By replicating data to third-party providers

**B2.** What is the minimum number of availability zones in an enabled Azure region?
- a) 1
- b) 2
- c) 3
- d) 5

**B3.** What SLA does Microsoft guarantee for VMs deployed across two or more availability zones?
- a) 99.9%
- b) 99.95%
- c) 99.99%
- d) 100%

**B4.** An Azure resource can belong to how many resource groups at the same time?
- a) 0
- b) 1
- c) 2
- d) Unlimited

**B5.** You need to run short-lived Docker container workloads with minimal cost. Which service should you use?
- a) Azure Virtual Machines
- b) Azure Kubernetes Service (AKS)
- c) Azure Container Instances (ACI)
- d) Azure App Service

**B6.** What is the maximum number of VMs you can deploy in a single scale set?
- a) 100
- b) 500
- c) 1,000
- d) 10,000

**B7.** Which Azure service provides a dedicated, private fiber-optic connection to Azure that does NOT traverse the public internet?
- a) Azure VPN Gateway
- b) VNet peering
- c) Azure ExpressRoute
- d) Azure DNS

**B8.** To access a Blob stored in the Archive tier, you must first:
- a) Delete it and re-upload it
- b) Move it to the Hot or Cool tier (rehydrate it)
- c) Convert it to a Page Blob
- d) Change the storage account type

**B9.** Which storage redundancy option provides the highest durability?
- a) LRS
- b) ZRS
- c) GRS
- d) GZRS

**B10.** You need to migrate 70 TB of data from on-premises to Azure Storage quickly and securely. Which service should you use?
- a) AzCopy
- b) Azure Storage Explorer
- c) Azure Data Box
- d) Azure File Sync

**B11.** Which Azure service synchronizes on-premises Windows Active Directory with Azure AD?
- a) Azure AD B2B
- b) Azure AD DS
- c) Azure AD Connect
- d) Azure AD Conditional Access

**B12.** In RBAC, which built-in role allows a user to create and manage resources but NOT delegate access to others?
- a) Owner
- b) Contributor
- c) Reader
- d) User Access Administrator

**B13.** Which security framework assumes that every access attempt is a potential breach?
- a) Defense in depth
- b) Network perimeter security
- c) Zero Trust
- d) Shared responsibility

**B14.** Azure VPN Gateway uses which protocols to secure connections?
- a) HTTP and HTTPS
- b) IPSec and IKE
- c) SSH and TLS
- d) SMTP and FTP

### True / False

**B15.** Availability zones protect against large-scale regional disasters like earthquakes. **TRUE / FALSE**

**B16.** Deleting an Azure resource group automatically deletes all resources within it. **TRUE / FALSE**

**B17.** Management groups can contain only Azure subscriptions, not other management groups. **TRUE / FALSE**

**B18.** VNet peering traffic travels over the public internet. **TRUE / FALSE**

**B19.** You can change the redundancy type of an Azure storage account after it has been created. **TRUE / FALSE**

**B20.** Azure MFA (multifactor authentication) is three-factor authentication. **TRUE / FALSE**

**B21.** RBAC role assignments are additive — your effective permissions are the union of all assigned roles. **TRUE / FALSE**

**B22.** A single Azure subscription can have up to 980 resource groups across all regions. **TRUE / FALSE**

---

### Answers — Section B

| # | Answer | Explanation |
|---|---|---|
| B1 | **b** | Each geography contains at least two regions separated by hundreds of miles, enabling disaster recovery through geographic redundancy. |
| B2 | **c** | Enabled regions have at least 3 availability zones, each in a separate datacenter with independent infrastructure. |
| B3 | **c** | Microsoft guarantees 99.99% SLA for VMs in 2+ availability zones. Availability sets get 99.95%. |
| B4 | **b** | An Azure resource can only exist in one resource group at a time. You can move it to another group, but it can't be in two simultaneously. |
| B5 | **c** | ACI is serverless — you pay only for CPU/memory used. Ideal for short-lived, simple container workloads at minimal cost. |
| B6 | **c** | Scale sets support up to 1,000 VMs in a single deployment. |
| B7 | **c** | ExpressRoute uses dedicated fiber-optic connections via a service provider (or Direct). VPN Gateway uses the public internet with encryption. |
| B8 | **b** | Archive-tier Blobs must be rehydrated to Hot or Cool tier before they can be accessed. |
| B9 | **d** | GZRS = ZRS in primary region (3 zones) + LRS in secondary region (3 copies). Most durable option. |
| B10 | **c** | Azure Data Box (80 TB capacity) is designed for large-scale offline data migration. AzCopy and Storage Explorer are for smaller transfers. |
| B11 | **c** | Azure AD Connect (now **Microsoft Entra Connect**) synchronizes on-premises Windows AD with Azure AD (now **Microsoft Entra ID**). ⚠️ All "Azure AD" names in this question use deprecated terminology — the exam may use either form. |
| B12 | **b** | Contributor can create/manage resources but cannot assign roles to others. Owner has full access including delegation. |
| B13 | **c** | Zero Trust assumes all access is potentially malicious and enforces Conditional Access, MFA, and least-privilege. |
| B14 | **b** | VPN Gateway secures connections using IPSec (Internet Protocol Security) and IKE (Internet Key Exchange). |
| B15 | **FALSE** | Availability zones protect against datacenter-level failures within a region, but may not protect against large-scale regional disasters. For that, you need multi-region replication. |
| B16 | **TRUE** | Deleting a resource group automatically deletes all resources contained in it. |
| B17 | **FALSE** | Management groups can contain both subscriptions AND other management groups. |
| B18 | **FALSE** | VNet peering traffic travels over Microsoft's private backbone infrastructure, not the public internet. |
| B19 | **⚠️ TRUE** | ⚠️ **Correction**: The original answer was FALSE, but this is incorrect. Microsoft docs confirm you CAN change the replication setting of an existing storage account (e.g., LRS → GRS, ZRS → GZRS). Some changes require a support request or data copy. The correct answer is **TRUE**. Note: you cannot change the account *type* (Standard → Premium), which may be the source of confusion. |
| B20 | **FALSE** | Azure MFA requires two or more verification factors (not three). Categories: something you know (password) + something you have (phone/key) + something you are (biometric). MFA means at least 2 factors, not necessarily all 3. |
| B21 | **TRUE** | RBAC is additive. If you have Owner on a resource group and Contributor on a resource within it, Owner takes precedence. |
| B22 | **TRUE** | The book states a limit of 980 resource groups per subscription across all regions. |

---

## Section C: Azure Management and Governance (Skill 3.1 – 3.4)

### Multiple Choice

**C1.** Which calculator helps you estimate how much money you'll save by migrating from on-premises to Azure?
- a) Pricing Calculator
- b) TCO Calculator
- c) Cost Management
- d) Azure Advisor

**C2.** Tags applied to a resource group are automatically inherited by the resources inside it.
- a) True
- b) False

**C3.** Which Azure Policy effect will block a resource from being created if it doesn't comply with the policy?
- a) Audit
- b) Append
- c) Deny
- d) Disabled

**C4.** You need to ensure that a critical database in Azure cannot be deleted by anyone, even users with the Owner RBAC role. What should you use?
- a) Azure Policy with Deny effect
- b) A delete resource lock
- c) Remove delete permissions from the Owner role
- d) Move the database to a different subscription

**C5.** Which tool provides personalized recommendations for cost savings, security, reliability, and performance?
- a) Azure Monitor
- b) Azure Service Health
- c) Azure Advisor
- d) Azure Policy

**C6.** What is the primary purpose of ARM templates?
- a) Monitor Azure resources
- b) Define declarative, repeatable resource deployments in JSON
- c) Create budgets and alerts
- d) Manage user identities

**C7.** Azure Arc extends Azure management features to:
- a) Only Azure resources
- b) Only on-premises Windows servers
- c) On-premises servers, VMs, and Kubernetes clusters in any cloud
- d) Only Kubernetes clusters

**C8.** Which Azure monitoring feature uses KQL (Kusto Query Language) for querying data?
- a) Azure Advisor
- b) Application Insights
- c) Log Analytics
- d) Azure Service Health

**C9.** What RBAC role is required to create a resource lock?
- a) Reader
- b) Contributor
- c) Owner or User Access Administrator
- d) Any role

**C10.** You want to package ARM templates, policies, RBAC assignments, and resource groups into a reusable deployment definition. Which service should you use?
- a) Azure Policy
- b) Azure Blueprints
- c) Azure Resource Manager
- d) Azure Advisor

### True / False

**C11.** Inbound network traffic to an Azure datacenter is free. **TRUE / FALSE**

**C12.** Azure Reservations allow you to save money by committing to resource usage over 1 or 3 years. **TRUE / FALSE**

**C13.** Azure Blueprints are a replacement for ARM templates. **TRUE / FALSE**

**C14.** Azure Cloud Shell requires a storage account to persist settings and files. **TRUE / FALSE**

**C15.** A read-only resource lock prevents both modifications and deletion of the locked resource. **TRUE / FALSE**

**C16.** Azure Service Health shows the status of ALL Azure services globally, not just yours. **TRUE / FALSE**

---

### Answers — Section C

| # | Answer | Explanation |
|---|---|---|
| C1 | **b** | The TCO (Total Cost of Ownership) Calculator compares on-premises costs with Azure costs and shows projected savings over 5 years. ⚠️ **Note**: The TCO Calculator was deprecated in August 2025. The Pricing Calculator is now the recommended tool for all cost estimation including migration scenarios. This question may still appear on the exam during the transition period. |
| C2 | **b (False)** | Tags on a resource group are NOT inherited by the resources inside it. Tags must be applied individually. |
| C3 | **c** | The Deny effect blocks the resource creation or update if it violates the policy. Audit only logs a warning. |
| C4 | **b** | A delete lock prevents deletion regardless of RBAC role. Even Owners cannot delete a locked resource without first removing the lock. |
| C5 | **c** | Azure Advisor analyzes your resources and provides personalized recommendations across cost, security, reliability, performance, and operational excellence. |
| C6 | **b** | ARM templates are declarative JSON files that define what resources to create and their configurations. ARM handles the how. |
| C7 | **c** | Azure Arc extends management to servers and Kubernetes clusters running on-premises or in other cloud providers (not limited to Azure or Windows). |
| C8 | **c** | Log Analytics uses KQL for querying aggregated monitoring data. KQL can handle massive datasets. |
| C9 | **c** | Creating resource locks requires the Owner or User Access Administrator RBAC role (or a custom role with lock permissions). |
| C10 | **b** | Azure Blueprints package ARM templates, policies, role assignments, and resource groups into reusable, versioned deployment definitions. ⚠️ **Note**: Azure Blueprints is being retired — replaced by **Template Specs** + **Deployment Stacks**. May still appear on the exam during the transition period. |
| C11 | **TRUE** | Inbound (ingress) traffic to Azure is free. You're charged for outbound (egress) traffic after the first 100 GB. |
| C12 | **TRUE** | Azure Reservations offer significant discounts for committing to 1-year or 3-year resource usage upfront. |
| C13 | **FALSE** | Blueprints are NOT a replacement for ARM templates. Most blueprints use ARM templates as artifacts. |
| C14 | **TRUE** | Cloud Shell requires a storage account to persist files, extensions, and settings across devices and sessions. |
| C15 | **TRUE** | A read-only lock is the most restrictive — it prevents both changes to properties AND deletion of the resource. |
| C16 | **FALSE** | Service Health shows the status of Azure services specific to YOUR resources and regions, not the global view (that's the Azure Status page). |

---

## Section D: Microsoft Learn Official Questions

> These questions come directly from the Microsoft Learn module assessments ("Check your knowledge").

**D1.** What is cloud computing?
- a) Delivery of storage services over the internet
- b) Delivery of computing services over the internet
- c) Delivery of websites accessible via the internet

**D2.** Which cloud model uses some datacenters focused on providing cloud services to anyone that wants them, and some data centers that are focused on a single customer?
- a) Public cloud
- b) Hybrid cloud
- c) Multicloud

**D3.** According to the shared responsibility model, which cloud service type places the most responsibility on the customer?
- a) Infrastructure as a Service (IaaS)
- b) Software as a Service (SaaS)
- c) Platform as a Service (PaaS)

---

### Answers — Section D

| # | Answer | Explanation |
|---|---|---|
| D1 | **b** | Cloud computing is the delivery of computing services (not just storage or websites) over the internet — including VMs, storage, databases, networking, IoT, ML, and AI. |
| D2 | **b** | Hybrid cloud combines public datacenters (for anyone) with private/dedicated datacenters (for a single customer) in an interconnected environment. |
| D3 | **a** | IaaS places the most responsibility on the customer (OS, middleware, apps, data). SaaS places the least; PaaS is in the middle. |

**D4.** Which type of scaling involves adding or removing resources (such as virtual machines or containers) to meet demand?
- a) Vertical scaling
- b) Horizontal scaling
- c) Direct scaling

**D5.** What is characterized as the ability of a system to recover from failures and continue to function?
- a) Reliability
- b) Predictability
- c) Scalability

**D6.** Which cloud practice most directly supports sustainability by reducing unnecessary resource use?
- a) Automatically scaling down resources when demand drops
- b) Deploying every workload as always-on peak capacity
- c) Using only on-premises hardware

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D4 | **b** | Horizontal scaling = adding or removing resources (VMs, containers). Vertical scaling = adding CPU/RAM to a single resource. |
| D5 | **a** | Reliability is the ability to recover from failures and continue to function. Predictability is about forecasting cost and performance. Scalability is about handling growth. |
| D6 | **a** | Automatically scaling down when demand drops reduces waste and supports sustainability. Always-on peak capacity is the opposite of efficient. On-premises hardware doesn't inherently support sustainability. |

**D7.** Which cloud service type is most suited to a lift-and-shift migration from an on-premises datacenter to a cloud deployment?
- a) Infrastructure as a Service (IaaS)
- b) Platform as a Service (PaaS)
- c) Software as a Service (SaaS)

**D8.** What type of cloud service type would a Finance and Expense tracking solution typically be in?
- a) Infrastructure as a Service (IaaS)
- b) Platform as a Service (PaaS)
- c) Software as a Service (SaaS)

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D7 | **a** | Lift-and-shift migration means setting up cloud resources similar to on-prem and moving workloads — this requires IaaS (you manage OS and above, like on-prem). |
| D8 | **c** | Finance and expense tracking is a fully developed application you rent — a classic SaaS scenario. You don't manage the infrastructure or platform. |

**D9.** How many resource groups can a resource be in at the same time?
- a) One
- b) Two
- c) Three

**D10.** What happens to the resources within a resource group when an action or setting at the Resource Group level is applied?
- a) Current resources inherit the setting, but future resources don't
- b) Future resources inherit the setting, but current ones don't
- c) The setting is applied to current and future resources

**D11.** What Azure feature replicates resources across regions that are at least 300 miles away from each other?
- a) Region pairs
- b) Availability Zones
- c) Sovereign regions

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D9 | **a** | A resource can belong to exactly one resource group at a time. You can move it, but it's always in only one group. |
| D10 | **c** | Actions at the resource group level (access permissions, policies, deletion) apply to ALL resources inside — both current and future. |
| D11 | **a** | Region pairs are two regions within the same geography, at least 300 miles apart, designed for disaster recovery through replication and failover. Availability Zones are within a single region. Sovereign regions are isolated for compliance. |

**D12.** Which Azure Virtual Machine feature staggers updates across VMs based on their update domain and fault domain?
- a) Availability sets
- b) Scale sets
- c) Update sets

**D13.** Which Azure compute option is event-driven and serverless, so you can run code without managing virtual machines?
- a) Azure Functions
- b) Azure Virtual Machines
- c) Azure Container Instances

**D14.** Which Azure service lets organizations host web apps and APIs without managing the underlying infrastructure?
- a) Azure App Service
- b) Azure Virtual Machines
- c) Azure ExpressRoute

**D15.** Which Azure service category provides prebuilt APIs for capabilities like vision, speech, and language without training your own model from scratch?
- a) Azure AI services
- b) Azure Virtual Machines
- c) Azure Virtual Networks

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D12 | **a** | Availability sets use update domains (for planned maintenance) and fault domains (for hardware failures) to stagger updates and protect VM availability. Scale sets manage identical VMs for scaling. |
| D13 | **a** | Azure Functions is event-driven and serverless — code runs only when triggered, with no VM management required. VMs and ACI both require some infrastructure management. |
| D14 | **a** | Azure App Service is an HTTP-based PaaS for hosting web apps, REST APIs, and mobile back ends without managing infrastructure. VMs require full infrastructure management. ExpressRoute is a networking service. |
| D15 | **a** | Azure AI services provides prebuilt APIs for vision, speech, language, and document processing. No custom model training required. VMs and VNets are compute and networking services. |

**D16.** Which Azure networking feature lets you divide a virtual network into smaller logical segments?
- a) Subnets
- b) Availability sets
- c) Resource locks

**D17.** If a company needs private, predictable connectivity between an on-premises datacenter and Azure, which service is the best fit?
- a) Azure ExpressRoute
- b) Azure Front Door
- c) Azure Load Balancer

**D18.** Which VPN gateway type is recommended in Azure for connections between virtual networks and for multisite scenarios?
- a) Route-based VPN gateway
- b) Policy-based VPN gateway
- c) Point-based VPN gateway

**D19.** What is a primary benefit of Azure DNS?
- a) You can manage DNS records using Azure credentials and tools
- b) It provides a built-in domain registrar for all domains
- c) It removes the need for all network security controls

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D16 | **a** | Subnets divide a virtual network into smaller logical segments. Availability sets protect VMs from hardware failures. Resource locks prevent modification or deletion. |
| D17 | **a** | Azure ExpressRoute provides a private, dedicated connection between on-premises and Azure — not over the public internet. Front Door is a global load balancer for web apps. Load Balancer distributes traffic within Azure. |
| D18 | **a** | Route-based VPN gateways are preferred and more resilient to topology changes. They support VNet-to-VNet connections, point-to-site, multisite, and ExpressRoute coexistence. Policy-based is for legacy scenarios only. |
| D19 | **a** | Azure DNS integrates with the Azure portal, using the same credentials, support contracts, and billing as other Azure services. Azure DNS cannot buy domain names (not a registrar). It does not replace network security controls. |

**D20.** Which tool automatically keeps files between an on-premises Windows server and an Azure cloud environment updated?
- a) Azure File Sync
- b) Azure Storage Explorer
- c) AzCopy

**D21.** Which storage redundancy option provides the highest degree of durability, with 16 nines of durability?
- a) Locally redundant storage
- b) Zone-redundant storage
- c) Geo-zone-redundant storage

**D22.** Which Azure Storage service supports big data analytics, as well as handling text and binary data types?
- a) Azure Blobs
- b) Azure Files
- c) Azure Disks

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D20 | **a** | Azure File Sync automatically keeps files bi-directionally synced between on-premises Windows servers and Azure Files. Storage Explorer is a manual GUI tool. AzCopy is a CLI tool with one-way sync only. |
| D21 | **c** | GZRS provides the highest durability at 16 nines (99.99999999999999%). It combines ZRS in the primary region with LRS geo-replication to a secondary region. LRS = 11 nines, ZRS = 12 nines. |
| D22 | **a** | Azure Blobs is a massively scalable object store for text and binary data. It also includes Data Lake Storage Gen2 for big data analytics. Azure Files is for managed file shares. Azure Disks provides block-level storage for VMs. |

**D23.** Which Microsoft Entra tool can vary the credentials needed to log in based on signals, such as where the user is located?
- a) Conditional Access
- b) Guest access
- c) Passwordless

**D24.** Which security model assumes the worst-case security scenario, and protects resources accordingly?
- a) Zero Trust
- b) Defense-in-depth
- c) Role-based access control

**D25.** A user is simultaneously assigned multiple roles that use role-based access control. The role permissions are: Role 1 - read, Role 2 - write, Role 3 - read and write. What are their actual permissions?
- a) Read only
- b) Write only
- c) Read and write

**D26.** Which Azure service is designed to securely store secrets, certificates, and encryption keys for your applications?
- a) Azure Key Vault
- b) Azure Policy
- c) Azure Monitor

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D23 | **a** | Conditional Access evaluates identity signals (user identity, location, device, app, risk level) at sign-in time to decide whether to allow, require MFA, or block access. Guest access is for external users. Passwordless is an authentication method, not a signal-based access tool. |
| D24 | **a** | Zero Trust assumes breach at the outset and verifies every request regardless of origin. Its three principles are: verify explicitly, use least privilege access (JIT/JEA), and assume breach. Defense-in-depth is a layered strategy. RBAC controls what users can do, not the security model. |
| D25 | **c** | Azure RBAC uses an allow (additive) model. When assigned multiple roles, effective permissions are the union of all role assignments. Role 1 (read) + Role 2 (write) + Role 3 (read+write) = read and write. |
| D26 | **a** | Azure Key Vault is the primary Azure service for securely storing secrets (passwords, connection strings), encryption keys (RSA/EC), and certificates (TLS/SSL). Azure Policy enforces rules on resources. Azure Monitor is for metrics and alerts. |

**D27.** What Azure feature can help stay organized and track usage based on metadata associated with resources?
- a) Tags
- b) Tracers
- c) Values

**D28.** Which tool helps estimate the cost of deploying Azure services before implementation?
- a) Azure Cost Analysis
- b) Azure Pricing Calculator
- c) Azure Advisor

**D29.** You have a workload that can tolerate interruptions and should run at the lowest possible compute cost. Which option is typically the best fit?
- a) Spot Virtual Machines
- b) Reservations
- c) Pay-as-you-go only

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D27 | **a** | Tags are name/value pairs that provide metadata about Azure resources. They help with resource management, cost tracking, operations, security, governance, and workload automation. |
| D28 | **b** | The Azure Pricing Calculator estimates potential costs before deployment — nothing is provisioned. Cost Analysis views actual costs after resources are deployed. Advisor provides optimization recommendations, not cost estimates. |
| D29 | **a** | Spot VMs use unused Azure capacity at up to 90% discount — ideal for interruptible/fault-tolerant workloads (batch, test jobs). Azure can reclaim the capacity when needed. Reservations are for stable, predictable workloads. |

**D30.** *(Module 11 — Governance and Compliance)* How can you prevent creation of non-compliant resources, without having to manually evaluate each resource?
- a) Azure Policy
- b) Microsoft Purview
- c) Azure Resource Monitor

**D31.** *(Module 11 — Governance and Compliance)* What's the best way to prevent inadvertent deletion of a resource?
- a) Azure Policy
- b) Microsoft Purview
- c) Azure resource locks

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D30 | **a** | Azure Policy lets you define rules that are automatically enforced when resources are created or updated — it can prevent noncompliant resources from being created without manual evaluation. Microsoft Purview is for data governance (discovery, classification, lineage). Azure Resource Monitor is not a real Azure service name. |
| D31 | **c** | Azure resource locks prevent resources from being accidentally deleted or changed. A Delete lock blocks deletion while still allowing read and modify. Locks apply regardless of RBAC — even an Owner must remove the lock first. Azure Policy enforces configuration standards, not deletion prevention. Microsoft Purview is for data governance. |

**D32.** *(Module 10 — Managing and Deploying Resources)* What service helps you manage your Azure, on-premises, and multicloud environments?
- a) Azure Arc
- b) Azure Policy
- c) Azure Cloud Manager

**D33.** *(Module 10 — Managing and Deploying Resources)* What two components could you use to implement an "infrastructure as code" deployment?
- a) Bicep and ARM Templates
- b) Azure Policy and Azure Arc
- c) Azure Monitor and Azure Arc

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D32 | **a** | Azure Arc extends Azure management and governance to on-premises and multicloud environments by projecting non-Azure resources into Azure Resource Manager. Azure Policy enforces rules on Azure resources but doesn't manage external environments. Azure Cloud Manager is not a real Azure service. |
| D33 | **a** | Bicep and ARM Templates are both declarative IaC tools that deploy Azure resources through Azure Resource Manager. Both are idempotent. Azure Policy enforces governance rules and Azure Arc extends management — neither is an IaC deployment tool. Azure Monitor is for observability. |

**D34.** *(Module 12 — Monitoring Tools)* Which is NOT one of the recommendation categories for Azure Advisor?
- a) Reliability
- b) Capacity
- c) Cost

**D35.** *(Module 12 — Monitoring Tools)* You receive an email notification that virtual machines (VMs) in an Azure region where you have VMs deployed is experiencing an outage. Which component of Azure Service Health will let you know if your application is impacted?
- a) Azure Status
- b) Service Health
- c) Resource Health

### Answers — Section D (continued)

| # | Answer | Explanation |
|---|---|---|
| D34 | **b** | "Capacity" is not an Azure Advisor category. The five categories are: Reliability, Security, Performance, Operational Excellence, and Cost. This is a common exam trap — "Capacity" sounds plausible but is not one of them. |
| D35 | **c** | Resource Health zooms in on individual resources (e.g., a specific VM) and tells you whether it is running normally or experiencing a problem — and whether the issue is on Azure's side or yours. Azure Status is global (all services, all regions). Service Health shows outages for your services/regions but not individual resource impact. |

---

## Section G — Scott Duffy Quiz Questions

> **Source**: Scott Duffy — AZ-900 Microsoft Azure Fundamentals (Udemy, v4.0)

**G1.** What are the responsibilities of the customers according to the shared responsibility model?
- a) Patching and fixing flaws in the infrastructure
- b) Patching guest OS and applications
- c) Physical and environmental controls
- d) Configuration of Azure infrastructure devices

**G2.** Which cloud deployment model enables an organization to eliminate all on-premises hardware by migrating its infrastructure to cloud-based resources managed by a third-party provider?
- a) Public Cloud
- b) On-premises private cloud
- c) Hybrid cloud with private cloud deployed within this organization's data center
- d) Infrastructure as a Service (IaaS)

**G3.** A company has distributed its workload on both the Azure Cloud and some on-premises servers. What type of architecture is this?
- a) Virtual private network
- b) Virtual private cloud
- c) Hybrid cloud
- d) Private cloud

**G4.** Which of the following is the correct description of the Azure Cloud Services benefit of scalability?
- a) A cloud service that can be accessed quickly from the Internet
- b) A cloud service that can be recovered after a failure occurs
- c) A cloud service that remains available after a failure occurs
- d) A cloud service that maintains fast performance as demand increases

**G5.** A company runs an application that has low usage most of the month but experiences high demand during the final week. Which cloud benefit best helps the company manage costs for this usage pattern?
- a) High availability
- b) Disaster recovery
- c) Elasticity
- d) Fault tolerance

**G6.** A system in the Azure Cloud is designed to withstand the failure of one or more components. What is this an example of?
- a) Elasticity
- b) High Availability
- c) Scalability
- d) Agility

**G7.** Which resource is an example of Infrastructure as a Service (IaaS) in Azure?
- a) An Azure web app
- b) An Azure virtual machine
- c) An Azure logic app
- d) An Azure SQL database

**G8.** Which service type is a complete development and deployment environment in the cloud?
- a) Infrastructure as a Service (IaaS)
- b) Platform as a Service (PaaS)
- c) Software as a Service (SaaS)
- d) Public Cloud

**G9.** Microsoft Office 365 is an example of which service type?
- a) Private Cloud
- b) Infrastructure as a Service (IaaS)
- c) Platform as a Service (PaaS)
- d) Software as a Service (SaaS)

**G10.** True or False: An Azure region contains a set of data centers that are connected by using a low-latency network.
- a) True
- b) False

**G11.** A company with seven departments has a plan to implement an Azure environment. To ensure that each department can use a different payment option for the Azure services it consumes, what should be created for each department?
- a) A reservation
- b) A subscription
- c) A resource group
- d) A container instance

**G12.** When you need to delegate permissions to several Azure VMs simultaneously, you must deploy the Azure VMs to the same ___.
- a) Azure region
- b) Azure Resource Manager template
- c) Resource group
- d) Availability zone

**G13.** An organization plans to migrate all its data and resources to Azure. The organization's migration plan states that only Platform-as-a-Service (PaaS) solutions be used in Azure. Which Azure service should be used?
- a) Azure virtual machines
- b) Azure Storage accounts
- c) Azure App Service
- d) Azure Virtual Networks

**G14.** What is Azure Virtual Network?
- a) Microsoft's cloud-based email service
- b) A framework for managing physical network devices
- c) An isolated network environment within Microsoft Azure
- d) A service for managing virtual machines

**G15.** What does Azure ExpressRoute provide?
- a) Improved storage solutions in the cloud
- b) Direct connectivity to Azure services
- c) Automated scaling of virtual machines
- d) Data encryption for virtual networks

**G16.** Which type of storage is NOT supported by Azure Storage Account?
- a) Blob storage
- b) Table storage
- c) Queue storage
- d) Cosmos DB
- e) Azure File

**G17.** Which Azure service can be used to synchronize data between an organization's on-premises Windows servers and an Azure file share?
- a) Azure Storage Explorer
- b) Azure File Sync
- c) AzCopy
- d) Azure Storage Account

**G18.** Which Azure service can NOT be used to move individual files back and forth between Clouds?
- a) Azure Storage Account
- b) Azure Storage Explorer
- c) Azure File Sync
- d) AzCopy

**G19.** Microsoft Entra Multi-Factor Authentication (MFA) typically includes any or all of the following methods, EXCEPT:
- a) Something you know
- b) Something you have
- c) Something you are
- d) Someone you know

**G20.** An organization plans to modernize its applications and network infrastructure in Cloud by migrating all network resources to Azure and decommissioning its on-premises data centre. What solution should be used to minimize the impact on users after the planned migration?
- a) Enable Microsoft Entra ID Protection
- b) Implement Azure Multi-Factor Authentication (MFA)
- c) Create a guest user account in Microsoft Entra ID for each user
- d) Sync all the on-premises Active Directory user accounts to Microsoft Entra ID

**G21.** Which tool can continually assess your cross-cloud resources for security issues and allows you to review your secure score?
- a) Azure Monitor
- b) Azure Advisor
- c) Microsoft Defender for Cloud
- d) Help + Support

**G22.** Which Azure service provides network traffic filtering across multiple subscriptions and virtual networks?
- a) Azure Firewall
- b) An application security group
- c) Azure DDoS protection
- d) A network security group (NSG)

**G23.** Which of the following is NOT a factor that users can consider affecting costs in Azure?
- a) Consumption
- b) Data Center maintenance
- c) Geography
- d) Resource type

**G24.** Which tool should be used to estimate and compare the costs of migrating workloads from on-premises to Azure, based on Microsoft's current recommendations?
- a) Pricing Calculator
- b) Azure Monitor
- c) Azure Cost Management
- d) Azure Advisor

**G25.** An organization has five branches. The organization plans to generate billing reports with Azure resource utilization of each branch from the Azure portal. Which tool can be used before the organization generates the reports?
- a) Policies
- b) Templates
- c) Locks
- d) Tags

**G26.** Which tool is NOT designed for Azure users for resource governance and compliance purposes?
- a) Microsoft Purview
- b) Azure Policy
- c) Resource Locks
- d) Azure Support Portal

**G27.** What is the purpose of Azure Role-Based Access Control (RBAC)?
- a) To manage virtual networks and subnet configurations
- b) To control who has access to Azure resources and what they can do with those resources
- c) To monitor and analyze security threats across Azure resources
- d) To automate the deployment of resources in Azure

**G28.** If you want to ensure your team deploys Azure resources only to allowed regions, what Azure service should be used?
- a) Role-Based Access Control
- b) Resource Locks
- c) Azure Policy
- d) Service Trust Portal

**G29.** An Azure administrator plans to run a script to create virtual machines. Which method is NOT available to run the scripts directly?
- a) Azure Cloud Shell
- b) Azure PowerShell
- c) Azure CLI
- d) Windows Command Prompt (CMD)

**G30.** Which Azure service can you use to manage on-premises and multi-cloud servers as Azure resources?
- a) Azure Advisor
- b) Azure Arc
- c) Azure Monitor
- d) Azure Blueprints

**G31.** What file format do Azure Resource Manager (ARM) templates use?
- a) XML
- b) YAML
- c) JSON
- d) CSV

**G32.** Azure Advisor evaluates your Azure resources and makes recommendations. Which of the below recommendations can't be found in the Advisor dashboard?
- a) Recommendations on how to configure the network settings on an Azure VM
- b) Recommendations on how to optimize and reduce your overall Azure spending
- c) Recommendations on how to improve the speed of your applications
- d) Recommendations on detect threats and vulnerabilities that might lead to security breaches

**G33.** Which Azure service is a customizable dashboard tool that allows you to track the health of any service issues on the Azure platform, including your Azure services in regions where they are used?
- a) Azure Advisor
- b) Azure Monitor
- c) Azure Arc
- d) Azure Service Health

**G34.** Which of the following statements is INCORRECT about Azure Monitor?
- a) You can monitor the performance of on-premises servers.
- b) You can monitor resources across multiple Azure subscriptions and tenants.
- c) You can't monitor the performance of VMs hosted in other clouds.
- d) You can create alerts in Azure Monitor.

### Answers — Section G

| # | Answer | Explanation |
|---|---|---|
| G1 | **b** | The cloud provider is always responsible for the physical infrastructure and devices. In an IaaS model, the customer is responsible for patching guest OS and applications. (Duffy) |
| G2 | **a** | An organization can close its datacenter by hosting infrastructure in a public cloud. Public cloud = third-party services over the public Internet. Private cloud = select users only. Hybrid = both. IaaS is a service model, not a deployment model. (Duffy) |
| G3 | **c** | A hybrid cloud combines on-premises infrastructure (or a private cloud) with a public cloud. Workloads split between Azure and on-prem = hybrid. (Duffy) |
| G4 | **d** | Scalability = adjusting resources to meet demand while maintaining performance. Not about recovery (reliability) or access speed. (Duffy) |
| G5 | **c** | Elasticity = automatically grow and shrink based on demand. For fluctuating workloads, you pay only for peak resources during peak times and scale down otherwise. (Duffy) |
| G6 | **b** | High availability = technologies that minimize IT disruptions through redundant, fault-tolerant, or failover-protected components. Withstanding component failure = HA. (Duffy) |
| G7 | **b** | Azure web app, logic app, and SQL database are all PaaS. A virtual machine is IaaS because you manage the OS and everything above it. (Duffy) |
| G8 | **b** | PaaS is a complete development and deployment environment in the cloud — supports building, testing, deploying, managing, and updating applications. IaaS is raw infrastructure; SaaS is ready-to-use apps; Public Cloud is a deployment model, not a service type. (Duffy) |
| G9 | **d** | SaaS = cloud-based apps used over the Internet. Office 365 (email, calendaring, office tools) is a classic SaaS example. Private Cloud is a deployment model; IaaS/PaaS require you to manage more. (Duffy) |
| G10 | **a** | True. An Azure region is a set of data centers deployed within a dedicated regional low-latency network. (Duffy) |
| G11 | **b** | Azure costs are billed per subscription. To use different payment options per department, create a separate subscription per department. Payment options: PAYG, EA, MCA. (Duffy) |
| G12 | **c** | Permissions applied to a resource group apply to all resources within it — delegate access to multiple VMs at once by placing them in the same resource group. (Duffy) |
| G13 | **c** | Azure App Service is PaaS — managed development/deployment platform. VMs and VNets are IaaS; Storage accounts are infrastructure. Only App Service abstracts the underlying server. (Duffy) |
| G14 | **c** | VNet is an isolated network environment in Azure. It allows resources to communicate securely with each other, the internet, and on-premises networks using private IP addresses. (Duffy) |
| G15 | **b** | ExpressRoute provides a private dedicated connection from on-premises to Azure, bypassing the public internet. It's not about storage, scaling, or encryption. (Duffy) |
| G16 | **d** | Storage Account (GPv2) supports Blob, Queue, Table, and Azure Files. Cosmos DB is a separate standalone database service, not part of a storage account. (Duffy) |
| G17 | **b** | Azure File Sync synchronizes files between on-premises Windows servers and Azure file shares. Storage Explorer is a GUI; AzCopy is a CLI tool; Storage Account is the resource itself. (Duffy) |
| G18 | **c** | File Sync synchronizes entire shares — not designed for moving individual files between clouds. Storage Account (portal), Storage Explorer (GUI), and AzCopy (CLI) can all move individual files. (Duffy) |
| G19 | **d** | MFA factors: something you know (password), something you have (phone/key), something you are (biometric). "Someone you know" is not an authentication factor. (Duffy) |
| G20 | **d** | Syncing on-prem AD to Entra ID ensures same credentials work in both environments — minimal user disruption during cloud migration. (Duffy) |
| G21 | **c** | Defender for Cloud provides a secure score and continuously evaluates resources across Azure, on-prem, and other clouds (AWS, GCP). Azure Monitor monitors performance; Advisor gives optimization tips; Help+Support is for tickets. (Duffy) |
| G22 | **a** | Azure Firewall filters traffic across multiple VNets and subscriptions (stateful, centralized). NSGs work at subnet/NIC level; DDoS protects against volumetric attacks; ASGs group VMs for rules. (Duffy) |
| G23 | **b** | Data center maintenance (power, cooling, security) is the cloud provider's responsibility — not billed separately. Consumption, geography, and resource type all directly affect your bill. (Duffy) |
| G24 | **a** | Pricing Calculator is now the recommended tool for all cost estimation including migration scenarios. TCO Calculator was deprecated August 2025. (Duffy) |
| G25 | **d** | Tags (key-value metadata) let you label resources by branch/department, then filter cost reports by tag in Cost Management. Policies enforce rules; Templates deploy resources; Locks prevent changes. (Duffy) |
| G26 | **d** | Azure Support Portal is for creating support tickets, not governance. Azure Policy, Resource Locks, and Microsoft Purview are all governance/compliance tools. (Duffy) |
| G27 | **b** | RBAC controls who can access Azure resources and what actions they can perform. It's not for networking, threat monitoring, or deployment automation. (Duffy) |
| G28 | **c** | Azure Policy with "Allowed locations" enforces where resources can be created. RBAC controls who, not where. Locks prevent changes/deletion. Service Trust Portal is for compliance documentation. (Duffy) |
| G29 | **d** | Azure scripts run via Cloud Shell (browser-based), PowerShell, or CLI. Windows Command Prompt (CMD) is NOT a supported method for running Azure management scripts. (Duffy) |
| G30 | **b** | Azure Arc manages non-Azure resources (on-prem, AWS, GCP) as Azure resources. Advisor gives recommendations; Monitor tracks performance; Blueprints is being retired. (Duffy) |
| G31 | **c** | ARM templates use JSON format. Bicep is a simpler DSL that compiles to ARM JSON. Terraform uses HCL. ARM does not use XML, YAML, or CSV. (Duffy) |
| G32 | **a** | Advisor's 5 categories: Cost, Security, Reliability, Operational Excellence, Performance. VM network configuration is operational guidance, not an Advisor category. (Duffy) |
| G33 | **d** | Service Health tracks Azure platform issues (outages, maintenance, advisories) filtered by region/service. Advisor = recommendations; Monitor = resource metrics/logs; Arc = multi-cloud management. (Duffy) |
| G34 | **c** | INCORRECT statement. Azure Monitor CAN monitor VMs in other clouds (AWS, GCP) and on-premises via agents. It supports multi-subscription, multi-tenant, and multi-cloud monitoring. (Duffy) |

---
