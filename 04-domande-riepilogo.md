# 04 — Review Questions (AZ-900 Self-Assessment)

> **~1264 questions** across 14 sections. Sections A–C: book-based questions by exam domain (50). Section D: official Microsoft Learn module assessments (35). Section E: practice questions from IPSpecialist 4th ed. 2024 (416). Section F: ExamTopics & practice quiz questions (120). Sections G–N: standalone mock exams — G: Scott Duffy Quiz (34), H: Scott Duffy Practice Test (50), I: Practice Test 3 (82), J: Practice Test 4 (125), K: Practice Test 5 (90), L: Practice Test 6 (89), M: Practice Test 7 (86), N: Practice Test 8 (87).
>
> ⚠️ **Errata**: Some answers from third-party sources contain known errors, flagged with ⚠️ correction notes. Cross-reference with study files 01–03 when in doubt.

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
| B11 | **c** | Azure AD Connect synchronizes on-premises Windows AD with Azure AD. |
| B12 | **b** | Contributor can create/manage resources but cannot assign roles to others. Owner has full access including delegation. |
| B13 | **c** | Zero Trust assumes all access is potentially malicious and enforces Conditional Access, MFA, and least-privilege. |
| B14 | **b** | VPN Gateway secures connections using IPSec (Internet Protocol Security) and IKE (Internet Key Exchange). |
| B15 | **FALSE** | Availability zones protect against datacenter-level failures within a region, but may not protect against large-scale regional disasters. For that, you need multi-region replication. |
| B16 | **TRUE** | Deleting a resource group automatically deletes all resources contained in it. |
| B17 | **FALSE** | Management groups can contain both subscriptions AND other management groups. |
| B18 | **FALSE** | VNet peering traffic travels over Microsoft's private backbone infrastructure, not the public internet. |
| B19 | **⚠️ TRUE** | ⚠️ **Correction**: The original answer was FALSE, but this is incorrect. Microsoft docs confirm you CAN change the replication setting of an existing storage account (e.g., LRS → GRS, ZRS → GZRS). Some changes require a support request or data copy. The correct answer is **TRUE**. Note: you cannot change the account *type* (Standard → Premium), which may be the source of confusion. |
| B20 | **FALSE** | Azure MFA is two-factor authentication (2FA): something you know + something you have. A device's built-in biometrics may add a third factor, but Azure itself doesn't require it. |
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
| C10 | **b** | Azure Blueprints package ARM templates, policies, role assignments, and resource groups into reusable, versioned deployment definitions. |
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

## Section E: IPSpecialist Practice Questions (428 Questions)

> From *AZ-900: Microsoft Azure Fundamentals — 400+ Exam Practice Questions with Detailed Explanations*, 4th Edition (February 2024, IPSpecialist LTD). Questions renumbered E1–E416.

**E1.** What is the maximum usable storage capacity of a Data Box device?
- a) 50 TB
- b) 80 TB
- c) 100 TB
- d) 120 TB

**E2.** In which scenarios is Data Box ideally suited for transferring data to Azure?
- a) Data sizes less than 20 TB
- b) Limited network connectivity scenarios
- c) Real-time data transfers
- d) Both A and C

**E3.** What is the primary purpose of the local web UI for Data Box?
- a) Daily administration tasks
- b) Data encryption
- c) Network configuration
- d) Disk erasure

**E4.** How is the security of data ensured during the transit of a Data Box device?
- a) GPS tracking
- b) Tamper-resistant screws and stickers
- c) Firewall protection
- d) Data Box encryption key

**E5.** What is Azure Resource Manager (ARM)?
- a) A virtual machine resource provider.
- b) A programming language for Azure resources.
- c) The deployment and management service for Azure.
- d) An authentication and authorization service for Azure.

**E6.** What is a resource group in Azure?
- a) A group of virtual machines.
- b) A container for managing related Azure resources.
- c) A specific location within a data center.
- d) A collection of Azure policies.

**E7.** What is the purpose of a resource group's location in Azure?
- a) It determines the geographic location of resources.
- b) It stores metadata about the resources for compliance reasons.
- c) It specifies the location for deploying resources.
- d) It defines the access control for resources.

**E8.** How are ARM templates different from scripts for managing Azure resources?
- a) ARM templates use declarative syntax to define resource properties. B. Scripts are dependencies. more efficient in managing resource
- c) ARM templates are written in a scripting language.
- d) Scripts have a graphical user interface for resource management.

**E9.** What is the maximum number of instances of a resource type allowed in a resource group?
- a) 500 instances
- b) 800 instances
- c) Unlimited instances
- d) 1000 instances

**E10.** How does Azure Resource Manager ensure resiliency?
- a) By depending on a single logical data center.
- b) By taking down for maintenance activities regularly.
- c) By being distributed across regions and availability zones.
- d) By relying on a backup control plane.

**E11.** What is an extension resource in Azure?
- a) A resource with limited capabilities.
- b) A resource that adds to another resource's capabilities.
- c) A resource that exists outside of a resource group.
- d) A standalone resource without dependencies. 12 What happens when you delete a resource group in Azure? A: Only metadata is deleted. B: All resources in the resource group are also deleted. C: Resource group location is changed. D: Only tags associated with the resource group are deleted.

**E13.** How can you manage access control for administrative actions in Azure Resource Manager?
- a) Apply tags to resources.
- b) Assign Azure Policies, Azure roles, or resource locks to a resource group.
- c) Use PowerShell commands.
- d) Configure access in the Azure portal settings.

**E14.** What is the purpose of applying tags to a resource group in Azure?
- a) To define the location of the resource group.
- b) To organize resources logically.
- c) To specify the deployment sequence of resources.
- d) To define resource dependencies.

**E15.** What is the primary purpose of a Disaster Recovery (DR) plan?
- a) To automate routine tasks in the cloud environment.
- b) To store data in a secure data store.
- c) To define strategies for recovering from large-scale disasters.
- d) To conduct regular performance audits.

**E16.** What types of incidents are considered disasters in the context of a DR plan?
- a) Minor resource failures.
- b) Regional outages, service outages, and malicious attacks.
- c) Routine maintenance activities.
- d) Network latency issues.

**E17.** Why is it essential to clearly define roles and responsibilities in a DR plan?
- a) To assign blame in case of a failure.
- b) To streamline day-to-day operations.
- c) To ensure efficient communication and coordination during a disaster.
- d) To reduce the need for regular updates to the plan.

**E18.** What is the importance of separating the failback plan from the DR plan?
- a) To confuse operators during the recovery process.
- b) To streamline the overall DR procedures.
- c) To avoid potential confusion and replicate necessary steps.
- d) To minimize the need for automation.

**E19.** How can automation be a risk in the context of a DR plan?
- a) Automation always slows down the recovery process.
- b) Trained operators need to carefully monitor automated processes.
- c) Automation is not suitable for large-scale disasters. D. Automation is only effective in nonproduction environments.

**E20.** What is the purpose of conducting regular DR drills?
- a) To meet compliance requirements.
- b) To confuse operators.
- c) To replace the need for a formal DR plan.
- d) To test the validity of the DR plan and recovery metrics.

**E21.** What is the primary purpose of redundancy in Azure Storage?
- a) To increase data access speed.
- b) To reduce storage costs.
- c) To protect data from planned and unplanned events.
- d) To limit the number of data copies.

**E22.** What are the key factors to consider when choosing a redundancy option for Azure Storage?
- a) Speed and capacity.
- b) Cost and compliance.
- c) Availability and durability.
- d) Latency and throughput.

**E23.** Which redundancy option is the least expensive but not recommended for high-availability applications?
- a) Zone-redundant storage (ZRS).
- b) Geo-redundant storage (GRS).
- c) Locally redundant storage (LRS).
- d) Geo-zone-redundant storage (GZRS).

**E24.** How many times is data replicated within the primary region in Locally Redundant Storage (LRS)?
- a) Once.
- b) Twice.
- c) Three times.
- d) Four times.

**E25.** Which redundancy option is recommended for Azure Data Lake Storage Gen2 workloads?
- a) Locally redundant storage (LRS).
- b) Zone-redundant storage (ZRS).
- c) Geo-redundant storage (GRS).
- d) Geo-zone-redundant storage (GZRS)

**E26.** What does Zone-redundant storage (ZRS) replicate data across in the primary region?
- a) Multiple countries.
- b) Multiple data centers.
- c) Three Azure availability zones.
- d) Different storage accounts.

### Answers — Section E (Batch 1)

| # | Answer | Explanation |
|---|---|---|
| E1 | **b** | Each Data Box storage device has a maximum usable storage capacity of 80 TB |
| E2 | **b** | Data Box is ideally suited for data sizes larger than 40 TB in scenarios with limited or no network connectivity |
| E3 | **c** | The local web UI is used to configure the device for network connectivity and register the device with the Data Box service |
| E4 | **b** | The device has a rugged casing secured by tamper-resistant screws and tamper-evident stickers to protect and secure data during transit |
| E5 | **c** | Azure Resource Manager is the deployment and management service for Azure. |
| E6 | **b** | A resource group is a container that enables you to manage related resources for an Azure solution. |
| E7 | **b** | The resource group's location stores metadata about the resources for compliance reasons. |
| E8 | **a** | ARM templates use declarative syntax to state, "Here's what I intend to create," without writing the sequence of programming commands. |
| E9 | **b** | A resource group can deploy up to 800 instances of a resource type. |
| E10 | **c** | Azure Resource Manager ensures resiliency by being distributed across regions and availability zones. |
| E11 | **b** | An extension resource's capabilities. resource adds to another |
| E13 | **b** | You can manage access control by assigning Azure Policies, Azure roles, or resource locks to a resource group. |
| E14 | **b** | Tags are applied to a resource group to logically organize resources in your subscription. |
| E15 | **c** | The primary purpose of a DR plan is to define strategies for recovering from large-scale disasters. |
| E16 | **b** | Disasters include regional outages, service outages, and severe malicious attacks in the context of a DR plan. |
| E17 | **c** | Clearly defined roles ensure efficient communication and coordination during a disaster. |
| E18 | **c** | Separating failback from the DR plan avoids potential confusion and ensures that necessary steps are mirrored. |
| E19 | **b** | Trained operators need to carefully monitor automated processes to avoid risks during a DR scenario. |
| E20 | **d** | Regular DR drills are conducted to test the validity of the DR plan and recovery metrics. |
| E21 | **c** | Redundancy in Azure Storage protects data from planned and unplanned events. |
| E22 | **c** | Consider availability and durability when choosing a redundancy option for Azure Storage. |
| E23 | **c** | Locally redundant storage (LRS) is the least expensive but not recommended for high availability applications. |
| E24 | **c** | Data in LRS is replicated three times within a single data center in the primary region. |
| E25 | **b** | Zone-redundant storage (ZRS) is recommended for Azure Data Lake Storage Gen2 workloads. |
| E26 | **c** | ZRS replicates data synchronously across three Azure availability zones in the primary region. |

**E27.** What is the durability percentage provided by Zoneredundant storage (ZRS) over a given year?
- a) At least 99.9%.
- b) At least 99.999999999%.
- c) At least 99.9999999999%.
- d) At least 99.99999999999999%.

**E28.** What is the primary difference between Geo-redundant storage (GRS) and Geo-zone-redundant storage (GZRS)?
- a) The number of data copies.
- b) The use of availability zones.
- c) The geographic distance between replicas.
- d) The replication latency.

**E29.** What happens during a failover in Geo-redundant storage (GRS) or Geo-zone-redundant storage (GZRS)?
- a) Data becomes inaccessible.
- b) The secondary region becomes the new primary region.
- c) Data is asynchronously replicated to the secondary region.
- d) Data in the secondary region is directly accessible.

**E30.** What does Read-access geo-redundant storage (RA-GRS) provide in addition to Geo-redundant storage (GRS)?
- a) Reduced latency.
- b) Read access to the secondary region.
- c) Increased durability.
- d) Automatic failover.

**E31.** Which Azure Storage service does not support Readaccess geo-redundant storage (RA-GRS)?
- a) Blob storage.
- b) Queue storage.
- c) Table storage.
- d) Azure Files.

**E32.** How can applications be designed to seamlessly shift to reading data from the secondary region?
- a) Enable Geo-redundant storage (GRS).
- b) Configure Read-access geo-redundant storage (RA-GRS).
- c) Use Locally redundant storage (LRS).
- d) Implement an automatic failover.

**E33.** What is the recovery point objective (RPO) in asynchronous geo-replication?
- a) The point at which the failover occurs.
- b) The interval between the most recent writes to the primary and the last write to the secondary.
- c) The time taken to replicate data to the secondary region.
- d) The latency in accessing data during failover.

**E34.** Which redundancy option is designed for maximum consistency, durability, and availability in disaster recovery scenarios?
- a) Locally redundant storage (LRS).
- b) Zone-redundant storage (ZRS).
- c) Geo-redundant storage (GRS).
- d) Geo-zone-redundant storage (GZRS).

**E35.** Which Azure Storage service does NOT support Geozone-redundant storage (GZRS)?
- a) Azure Blob storage.
- b) Azure Queue storage.
- c) Azure Table storage.
- d) Azure Files.

**E36.** What is the primary purpose of defining a naming convention for Azure resources, including virtual networks?
- a) To reduce costs.
- b) To ensure uniqueness.
- c) To improve performance.
- d) To enhance security.

**E37.** In which Azure region and subscription must a resource be created to ensure compatibility with a virtual network?
- a) Any region and subscription.
- b) Same region, different subscription.
- c) Different region, same subscription.
- d) Same region, same subscription

**E38.** What should be considered when deciding on Azure regions for resource deployment?
- a) Network latency only.
- b) Data residency, sovereignty, and compliance only.
- c) Availability zones support only.
- d) Network latency, data residency, sovereignty, compliance, and availability zone support.

**E39.** What is a consideration when deciding the number of virtual networks in a subscription?
- a) Maximum subscription limit.
- b) Organizational security requirements.
- c) Availability zone support.
- d) Data residency.

**E40.** What does a virtual network in Azure represent?
- a) A physical network infrastructure.
- b) An isolated portion of the Azure public network.
- c) A collection of on-premises servers.
- d) A dedicated network for Azure support.

**E41.** When connecting virtual networks, what appliance can be used to control traffic flow between them?
- a) Load Balancer.
- b) Firewall.
- c) Gateway.
- d) Virtual Machine.

**E42.** How can traffic filtering be achieved between resources in a virtual network?
- a) Using network latency.
- b) Using Azure Policy.
- c) Using a Network Security Group (NSG) or Network Virtual Appliance (NVA).
- d) Using naming conventions.

**E43.** What is the purpose of a Network Security Group (NSG) in Azure?
- a) Load balancing.
- b) Traffic filtering.
- c) Resource naming.
- d) Traffic routing.

**E44.** How can Azure's default routing between subnets be overridden?
- a) By using a Network Security Group (NSG).
- b) By deploying a Virtual Machine.
- c) By creating a route table and associating it with a subnet.
- d) By enforcing naming conventions.

**E45.** What is the purpose of virtual network peering in Azure?
- a) Load balancing between virtual networks.
- b) Enabling connectivity between on-premises and Azure.
- c) Connecting virtual networks within the same or different regions.
- d) Enforcing naming conventions.

**E46.** How can an Azure VPN Gateway be used in the context of virtual networks?
- a) To filter network traffic.
- b) To enforce naming conventions.
- c) To connect a virtual network to an on-premises network.
- d) To create a route table.

**E47.** What is required for name resolution between resources in peered virtual networks?
- a) Azure's built-in DNS.
- b) Azure DNS private domains.
- c) A Network Security Group (NSG).
- d) A Virtual Machine.

**E48.** Which Azure service is used for assigning permissions and roles for virtual network capabilities?
- a) Azure Policy.
- b) Azure AD Identity Protection.
- c) Azure RBAC (Role-Based Access Control).
- d) Azure Policy.

**E49.** What does Azure Policy enable in the context of virtual networks?
- a) Traffic filtering.
- b) Route table creation.
- c) Enforcing organizational standards and service level agreements.
- d) Virtual network peering.

**E50.** When deploying Azure Policy, what does it evaluate in your resources?
- a) Network latency.
- b) Resource compliance with policy definitions.
- c) Availability zones support.
- d) Naming convention adherence.

**E51.** To what should an application connect to retrieve security tokens?
- a) Azure Storage account
- b) Microsoft Entra ID
- c) Certificate store
- d) Azure Key Vault

### Answers — Section E (Batch 2)

| # | Answer | Explanation |
|---|---|---|
| E27 | **c** | ZRS offers durability for storage resources of at least 99.9999999999% over a given year. |
| E28 | **b** | GZRS combines availability zones with protection from regional outages. |
| E29 | **b** | During failover, the secondary region becomes the new primary region. |
| E30 | **b** | Read-access geo-redundant storage (RA-GRS) provides the capability to read data from the secondary region in addition to geo-redundancy, allowing users to access their data even if the primary region is unavailable. |
| E31 | **d** | RA-GRS provides read access to the data in the secondary location in addition to geo-redundancy, and as of now, Azure Files does not offer this feature. |
| E32 | **b** | Applications can be designed to shift to reading data from the secondary region by configuring RAGRS. |
| E33 | **b** | The recovery point objective (RPO) in asynchronous geo-replication is the interval between the most recent writes to the primary region and the last write that has been successfully replicated to the secondary region. |
| E34 | **d** | Geo-zone-redundant designed maximum for storage consistency, (GZRS) durability, is and availability. |
| E35 | **d** | Azure Files does not support Geo-zoneredundant storage (GZRS). GZRS is a replication option that provides redundancy across availability zones within a region, but Azure Files currently does not offer support for this level of redundancy. |
| E36 | **b** | Naming conventions help ensure the uniqueness of resource names within a given scope. |
| E37 | **d** | A resource can only be created in a virtual network that exists in the same region and subscription. |
| E38 | **d** | Consider factors like network latency, data residency, sovereignty, compliance, and availability zone support when deciding on Azure regions. |
| E39 | **b** | Organizational security requirements may influence the decision on the number of virtual networks. |
| E40 | **b** | A virtual network in Azure represents an isolated portion of the Azure public network. It allows users to securely connect and isolate their Azure resources, providing control over IP address blocks, routing, and network security settings. |
| E41 | **b** | A network virtual appliance (NVA), such as a firewall, can be used to control traffic flow between connected virtual networks. |
| E42 | **c** | Traffic filtering between resources in a virtual network in Azure can be achieved using a Network Security Group (NSG) or Network Virtual Appliance (NVA). NSGs allow you to control inbound and outbound traffic to network interfaces (NIC), VMs, and subnets by defining security rules. At the same time, NVAs are third-party appliances or virtual ma... |
| E43 | **b** | The purpose of a Network Security Group (NSG) in Azure is traffic filtering. NSGs are used to control inbound and outbound traffic to network interfaces (NIC), virtual machines, and subnets. |
| E44 | **c** | Azure's default routing between subnets can be overridden by creating a route table and associating it with a subnet. |
| E45 | **c** | Virtual network peering connects virtual networks within the same or different regions. |
| E46 | **c** | An Azure VPN Gateway is used to connect a virtual network to an on-premises network. |
| E47 | **b** | For name resolution between resources in peered virtual networks, deploy your own DNS server or use Azure DNS private domains. |
| E48 | **c** | Azure RBAC (Role-Based Access Control) is the Azure service used for assigning permissions and roles for virtual network capabilities. Azure RBAC allows you to control access to Azure resources by assigning roles to users, groups, or applications at a certain scope, such as a subscription, resource group, or individual resources. |
| E49 | **c** | Azure Policy enables enforcing organizational standards and service level agreements for virtual networks. |
| E50 | **b** | Azure Policy evaluates resource compliance with policy definitions to ensure adherence to organizational standards. |
| E51 | **b** | Applications typically connect to Microsoft Entra ID to retrieve security tokens. |

**E52.** You have several virtual machines in an Azure subscription. You create a new subscription.
- a) No change is needed.
- b) VMs can transfer to the new subscription.
- c) The virtual machines can be moved to the new subscription-only if they are all in the same resource group.
- d) Windows Server 2016 is a prerequisite for transferring virtual machines to the new subscription.

**E53.** Your company plans to deploy an Artificial Intelligence (AI) solution in Azure. To develop, test, and deploy predictive analytics solutions, the company should leverage a platform designed for data science and machine learning, such as Azure Machine Learning, AWS SageMaker, or Google Cloud AI Platform.?
- a) Azure Logic Apps
- b) Azure Machine Learning Studio
- c) Azure Batch
- d) Azure Cosmos DB

**E54.** To establish a network drive mapping from multiple Windows 10 computers to Azure Storage, you should set up an Azure File Share. This solution enables the creation of a shared storage location in Azure, which can be accessed and mapped as a network drive by multiple Windows 10 machines, providing a centralized and scalable file storage solution in the cloud.
- a) Azure SQL database
- b) Virtual machine data disk
- c) Files service in a storage account
- d) Blobs service in a storage account

**E55.** What is required to use Azure Cost Management?
- a) Dev/Test subscription
- b) Software Assurance
- c) Enterprise Agreement (EA)
- d) Pay-as-you-go subscription

**E56.** What is the main purpose of deciding the cloud deployment type or architecture?
- a) To determine the cost
- b) To decide the cloud pricing model
- c) To meet business requirements for cloud computing
- d) To choose the cloud service provider

**E57.** In a public cloud, who owns and manages the resources such as servers and disks?
- a) The organization using the cloud
- b) The government
- c) The cloud provider
- d) Azure Stack

**E58.** What is the primary advantage of using the public cloud approach?
- a) Higher security
- b) Localized data storage
- c) Lower cost, scalability, and flexibility
- d) Complete control over physical hardware

**E61.** What does a hybrid cloud allow users to access within a single environment?
- a) Only public cloud resources
- b) Only private cloud resources
- c) Both public and private cloud resources
- d) Only community cloud resources 62 What is the primary advantage of a multi-cloud strategy?
- a) Vendor lock-in
- b) Enhanced redundancy
- c) Limited performance optimization
- d) Cost predictability

**E63.** What is Azure Arc, and how does it extend Azure's services?
- a) Azure pricing model
- b) A cloud deployment model
- c) A Microsoft service extending management and services to any infrastructure
- d) A hybrid cloud service

**E64.** What is the Azure service designed for running, managing, and migrating Azure?
- a) Azure Stack
- b) Azure Logic Apps
- c) Azure Batch VMware-based workloads in
- d) Azure VMware Solution

**E65.** Which model involves a cloud computing strategy where an organization uses services and resources from multiple cloud providers?
- a) Public Cloud
- b) Private Cloud
- c) Hybrid Cloud
- d) Multi-cloud

**E66.** What does the consumption-based model in cloud computing mean?
- a) Upfront expenses
- b) Pay-as-you-go pricing
- c) Unlimited resources
- d) Fixed costs

**E67.** In cloud computing, what is the main advantage of not having to predict future resource requirements accurately?
- a) Vendor lock-in
- b) Cost predictability
- c) Scalability
- d) Agility

**E68.** Which cloud deployment model allows access to a group of organizations for its services and provides a sharing mechanism?
- a) Public Cloud
- b) Private Cloud
- c) Hybrid Cloud
- d) Community Cloud 69 What is the main advantage of using the consumptionbased model in cloud computing?
- a) Upfront expenses
- b) Predictable costs
- c) Pay-as-you-go pricing
- d) Fixed resource allocation

**E70.** In the context of cloud computing, what does elasticity refer to?
- a) Dynamically extending or minimizing network resources
- b) Quick and efficient adaptation to changes in the business environment
- c) Adding more resources to a single server
- d) Predicting future resource requirements

**E71.** What is the main benefit of Azure Virtual Machine regarding resource management?
- a) Fixed resource allocation
- b) Pay-per-usage model
- c) Dynamic scaling up and down
- d) High availability guarantee

**E72.** Which protocol is commonly used to connect to Azure Virtual Machines for Windows-based machines?
- a) Remote Desktop Protocol (RDP)
- b) Secure Shell (SSH)
- c) Telnet
- d) FTP

**E73.** What do Azure Virtual Machine Scale Sets allow you to do?
- a) Manage individual VMs manually
- b) Create and manage a group of identical load-balanced VMs
- c) Automatically adjust VM resources based on demand
- d) Limit the number of VM instances to 1000

**E74.** How do Azure Virtual Machine Scale Sets handle fluctuations in demand?
- a) By manually adding or removing VM instances
- b) By automatically adjusting the number of VM instances
- c) By limiting the number of VM instances to a predefined threshold
- d) By shutting down VM instances during low-demand periods

**E75.** What is a key feature of Azure Virtual Desktop in terms of management?
- a) Custom monitoring solutions
- b) Centralized security management
- c) Advanced networking configurations
- d) Multi-cloud integration

**E76.** How can organizations reduce costs when using Azure Virtual Desktop?
- a) Pay for Azure resources only
- b) Opt for a monthly subscription model
- c) Utilize Bring Your License (BYOL)
- d) Reduce the number of users accessing virtual desktops

**E77.** Which protocol is used for connecting to another computer through a network connection in Azure Virtual Desktop?
- a) FTP
- b) Telnet
- c) Secure Shell (SSH)
- d) Remote Desktop Protocol (RDP)

**E78.** What is a recommended method to connect to Azure Virtual Machines using RDP?
- a) Use a dynamic IP address for flexibility
- b) Download the .rdp file each time before connecting
- c) Use a static IP address to prevent changes
- d) Connect directly using the VM's name

**E79.** What security measure can be activated in Azure Virtual Desktop to fortify user sign-ins?
- a) Single sign-on (SSO)
- b) Multifactor authentication
- c) Role-based access controls (RBAC)
- d) Virtual private network (VPN)

**E81.** What is the primary advantage of committing to an Azure reserved VM instance?
- a) Immediate VM deployment
- b) Automatic application of reservation discounts
- c) Exclusive access to new VM sizes
- d) Fixed monthly subscription cost

### Answers — Section E (Batch 3)

| # | Answer | Explanation |
|---|---|---|
| E52 | **b** | If you create a new subscription, the virtual machines can be moved to the new subscription. |
| E53 | **b** | Azure Machine Learning Studio is suitable for building, testing, and deploying predictive analytics solutions. |
| E54 | **c** | Creating a Files service in a storage account allows you to use Azure Storage as a file share for mapping network drives. |
| E55 | **⚠️ d** | ⚠️ **Correction**: The original answer (c = EA) is incorrect. Azure Cost Management is available to ALL Azure subscription types — Pay-As-You-Go, EA, MCA, and CSP. It is a free, built-in feature. The correct answer is **d) Pay-as-you-go subscription** (or any subscription type). |
| E56 | **c** | Deciding architecture is crucial the cloud to deployment meet specific type or business requirements for cloud computing. |
| E57 | **c** | In a public cloud, the cloud provider owns and manages the resources. Users or organizations leverage the services provided by the cloud provider, and the provider takes care of the underlying infrastructure, maintenance, and management of the physical resources, allowing users to focus on deploying and managing their applications and services. |
| E58 | **c** | The primary advantages of the public cloud approach are lower cost, scalability, and flexibility. |
| E61 | **c** | A hybrid cloud allows users to access both public and private cloud resources within a single environment. |
| E63 | **c** | Azure Arc is a Microsoft service that extends Azure's management and services to any infrastructure. |
| E64 | **d** | Azure VMware Solution is designed for running, managing, and migrating VMware-based workloads in Azure. |
| E65 | **d** | Multi-cloud involves using resources from multiple cloud providers. services and |
| E66 | **b** | Consumption-based model in cloud computing refers to pay-as-you-go pricing. |
| E67 | **c** | Not having to predict future resource requirements accurately enables scalability. |
| E68 | **d** | Community Cloud allows access to a group of organizations, providing a sharing mechanism. |
| E70 | **a** | Elasticity refers to dynamically extending or minimizing network resources to respond to workload adjustments. |
| E71 | **c** | Azure Virtual Machine allows dynamic scaling of resources up and down according to demand, ensuring efficient resource management. For further result you can visit the given URL. |
| E72 | **a** | Remote Desktop Protocol (RDP) is commonly used to connect to Windows-based Azure Virtual Machines. |
| E73 | **b** | Azure Virtual Machine Scale Sets allow you to create and manage a group of identical load-balanced VMs. |
| E74 | **b** | Azure Virtual Machine Scale Sets automatically adjust the number of VM instances based on fluctuations in demand. |
| E75 | **b** | Azure Virtual Desktop offers centralized security management as a key feature. |
| E76 | **c** | Organizations can reduce costs by utilizing Bring Your License (BYOL) for Azure Virtual Desktop. |
| E77 | **d** | Remote Desktop Protocol (RDP) is used for connecting to another computer through a network connection in Azure Virtual Desktop. |
| E78 | **c** | It is recommended to use a static IP address to prevent changes when connecting to Azure Virtual Machines using RDP. |
| E79 | **b** | Multifactor authentication can be activated in Azure Virtual Desktop to fortify user sign-ins. |
| E81 | **b** | Committing to a reserved VM instance provides an automatic discount to running VMs that match the reservation scope and attributes. |

**E82.** What does an Azure reserved VM instance purchase cover specifically for Windows VMs?
- a) Compute and storage costs
- b) Windows server license only
- c) Both Windows server license and compute costs.
- d) Software costs only

**E83.** How can you determine the right VM size before buying a reservation? A. Use reservation recommendations and check ConsumedService value
- b) Analyze daily usage data without checking VM sizes
- c) Rely on Meter subcategory and Product fields in usage data
- d) Purchase a reservation first and then determine VM size

**E84.** What is the purpose of the instance size flexibility setting in Azure VM reservations? A: Determines the VM size for discounts B: Enables discounts only for specific VM series C: Controls which services get reserved instance discounts D: Adjusts VM flexibility during runtime

**E85.** Which services can benefit from VM reservation discounts according to the instance size flexibility setting being 'on'?
- a) Microsoft. Compute only
- b) Microsoft.ClassicCompute only
- c) Microsoft. Compute, Microsoft. Batch, and more
- d) Microsoft.VirtualMachines

**E86.** What should you avoid when determining the VM size for reservation purchases to ensure correct discounts?
- a) Analyzing daily usage data
- b) Referring to the AdditionalInfo field
- c) Checking Meter subcategory
- d) Using Product fields in usage data

**E87.** Which VM sizes are exceptions where reservation discounts don't apply?
- a) DS-series, ES-series, FS-series
- b) A-series, Av2-series, G-series
- c) HBv2 VMs
- d) D-series, F-series

**E88.** What are the considerations for purchasing Reserved VM Instances regarding insufficient quota?
- a) Quota doesn't affect reservations
- b) Quota should be exceeded for better discounts
- c) Quota must be available for the new reservation
- d) Quota is only applicable to a single subscription scope

**E89.** In which cases can Azure limit the purchase of new reservations due to low capacity in a region?
- a) Only for specific VM series
- b) During the preview or promo period
- c) With insufficient quota
- d) In rare circumstances

**E90.** What roles are required to buy Reserved VM Instances in the Cloud Solution Provider (CSP) program?
- a) Owner role and EA Admin
- b) Admin agents or sales agents
- c) Reader role and service admin
- d) Contributor role and enterprise admin

**E91.** What are the required steps to buy a Reserved VM Instance in the Azure portal?
- a) All services > Reservations > Add > Virtual machine
- b) Virtual machines > Add reservation > Select subscription
- c) Azure portal > Reservations > Add > Compute
- d) Reservations > Add > Cloud services > Virtual machine

**E92.** What is the significance of the 'Scope' field when purchasing a Reserved VM Instance?
- a) Determines the region covered by the reservation
- b) Identifies the VM size for the reservation
- c) Specifies the subscription or resource group scope
- d) Sets the number of instances for the reservation

**E93.** What does the 'Optimize for' option in the 'Advanced settings' refer to when purchasing a Reserved VM Instance?
- a) Optimizes for cost efficiency
- b) Adjusts VM instance size flexibility
- c) Prioritizes data center capacity
- d) Enables daily usage analysis

**E94.** What are the available terms for purchasing Reserved VM Instances?
- a) One year and two years
- b) Two years and five years
- c) One year, three years, and five years
- d) One year, three years, and ten years

**E95.** How is the quantity determined when purchasing a Reserved VM Instance?
- a) The number of VMs currently running
- b) A fixed quantity set by Microsoft
- c) The subscription quota
- d) It is user-defined based on running VM instances

**E96.** How is the quantity determined when purchasing a Reserved VM Instance?
- a) The number of VMs currently running
- b) A fixed quantity set by Microsoft
- c) The subscription quota
- d) It is user-defined based on running VM instances

**E97.** What can you change after purchasing a Reserved VM Instance without causing a new commercial transaction?
- a) Billing period
- b) Ownership and scope
- c) End date of the reservation
- d) Compute and storage costs

**E98.** What is the purpose of splitting reservations after purchase?
- a) To create new commercial transactions
- b) To change the end date of the reservation and merging
- c) To adjust ownership and scope
- d) To optimize billing and discount distribution

**E99.** Which field in the usage file or usage API provides correct information about VM size for reservation purchase?
- a) Meter subcategory
- b) Product fields
- c) additionalinfo
- d) ConsumedService

**E100.** For which type of subscription is the Add More option available when buying Reserved VM Instances?
- a) Enterprise Agreement (EA)
- b) Pay-as-you-go with monetary commitment
- c) Cloud Solution Provider (CSP)
- d) Microsoft Customer Agreement (MCA)

**E101.** What is the primary focus of the three basic concepts of fiscal conversation mentioned in the article?
- a) Employee satisfaction
- b) Customer engagement
- c) Revenue, Cost, and Profit
- d) Product innovation

**E102.** What does a profit outcome in fiscal conversation signify?
- a) High risk and failure
- b) Increase in revenue and decrease in costs
- c) Decrease in revenue and increase in costs
- d) Status quo in financial terms

**E103.** Why are the examples provided in the article labeled as hypothetical?
- a) To guarantee returns
- b) To prevent roadblocks
- c) Due to their innovative nature
- d) To emphasize the cloud strategy's uniqueness

**E104.** What is the significance of partnering with a proven innovator when proposing new revenue streams prone to failure?
- a) Avoiding revenue increases
- b) Adding credibility to proposed outcomes
- c) Encouraging resistance
- d) Preventing fiscal transformation

**E105.** In the context of fiscal outcomes, what do new revenue streams represent?
- a) Reduction in existing products
- b) Low-risk opportunities
- c) High-risk ventures
- d) Opportunities to deliver products differently

**E106.** How can cloud computing contribute to revenue increases for existing products?
- a) Through cost avoidance
- b) By reducing capital expenses
- c) Via global scale and digital reach
- d) By avoiding data center shutdown

### Answers — Section E (Batch 4)

| # | Answer | Explanation |
|---|---|---|
| E82 | **c** | The purchase covers only the compute part of your VM usage, including the Windows server license cost. |
| E83 | **a** | Reservation recommendations and checking ConsumedService value help in determining the right VM size. |
| E84 | **c** | Instance size flexibility determines which services get the reserved instance discounts. |
| E85 | **c** | With the setting 'on', reservation discounts apply to various services, including Microsoft. Compute, Microsoft. Batch, and others. |
| E86 | **c** | The meter subcategory doesn't distinguish between VM sizes using premium storage; use the AdditionalInfo field for correct VM size determination. |
| E87 | **b** | Reservation discounts don't apply to A-series, Av2-series, and G-series VMs. |
| E88 | **c** | A quota must be available in the subscription for the new Reserved VM Instance. |
| E89 | **d** | Azure may limit the purchase of new reservations for a subset of VM sizes due to low capacity in rare circumstances. |
| E90 | **b** | In the CSP program, only admin agents or sales agents can buy Reserved VM Instances. |
| E91 | **a** | The correct steps are All Reservations > Add > Virtual machine. |
| E92 | **c** | The 'Scope' field specifies the reservation's scope, such as a single subscription or shared scope. |
| E93 | **b** | 'Optimize for' refers to adjusting VM instance size flexibility. |
| E94 | **c** | Available terms for purchasing are one year, three years, and five years. |
| E95 | **a** | The quantity is the number of running VM instances that can get the billing discount. |
| E96 | **d** | The effective price of zero indicates that the usage gets a reservation discount. |
| E97 | **b** | Ownership and scope can be changed without causing a new commercial transaction. |
| E98 | **d** | Splitting and merging reservations help optimize billing and discount distribution. |
| E99 | **c** | The AdditionalInfo field provides correct information about VM size for reservation purchase. |
| E100 | **a** | The Add More option is available for Enterprise Agreement (EA) subscriptions. |
| E101 | **c** | The three basic concepts are Revenue, Cost, and Profit. |
| E102 | **b** | Profit outcome indicates both an increase in revenue and a decrease in costs. |
| E103 | **b** | The examples are labeled as hypothetical to emphasize that they should not be considered a guarantee of returns. |
| E104 | **b** | Partnering with a proven innovator adds credibility to proposed outcomes, helping prevent roadblocks. |
| E105 | **d** | New revenue streams represent innovative opportunities to deliver products differently. |
| E106 | **c** | Cloud computing can help businesses increase revenues from existing revenue streams through global scale and digital reach. |

**E107.** What is the outcome when cloud computing helps reduce capital expenses for hardware and software?
- a) New revenue streams157
- b) Cost avoidance
- c) Profit increases
- d) Cost reduction

**E108.** In fiscal terms, what is the focus of cost avoidance?
- a) Reducing current budget commitments
- b) Preventing future refresh cycles
- c) Increasing server capacity
- d) Ongoing operational costs

**E109.** What is the primary difference between capital expenses and operating expenses in the context of fiscal conversation?
- a) Capital expenses are ongoing costs, and operating expenses are long-term investments.
- b) Capital expenses contribute to a particular purpose, and operating expenses generate benefits over a long period.
- c) Capital expenses are non-recurring, and operating expenses are recurring costs.
- d) Capital expenses are assets, and operating expenses are liabilities.

**E110.** How does the article describe Sentara Healthcare's fiscal outcome after moving its data to Azure?
- a) Guaranteed profit
- b) Hypothetical and high-risk
- c) Record cost savings
- d) Minimal impact on IT team costs

**E111.** What does Azure Virtual Network enable regarding networking environments?
- a) Integration with public IP addresses
- b) Creation of isolated virtual networks
- c) Internet profitability for IP address spaces
- d) Exclusive use of private IP addresses 112 How is granularity achieved in Azure Virtual Network regarding IP address spaces?
- a) Public IP address ranges
- b) Private IP address ranges
- c) Subnet division
- d) External DNS configuration

**E113.** What is the purpose of assigning a public IP address to an Azure resource or using a public load balancer?
- a) Isolation of resources
- b) Incorporating Internet connections
- c) Enabling secure communication
- d) Enhancing internal DNS configuration

**E114.** How can secure communication between Azure resources be achieved, according to the article?
- a) Through external DNS servers
- b) By using private IP addresses
- c) Via virtual networks and service endpoints
- d) By isolating resources within subnets

**E115.** What are the three mechanisms that Azure Virtual Networks support for communication with on-premises resources?
- a) Internal DNS, VPN, and BGP
- b) Subnets, Site-to-Site VPN, and Point-to-Site VPN
- c) ExpressRoute, DNS resolution, and Route Tables D. Point-to-Site ExpressRoute VPN, Site-to-Site VPN, and Azure

**E116.** What is the primary function of Route Tables in Azure Virtual Networks?
- a) Filtering network traffic
- b) Establishing internet connections
- c) Defining rules for traffic direction
- d) Configuring internal DNS servers

**E117.** What Azure resource contains inbound and outbound security rules, allowing the definition of rules based on factors like source/destination IP address, port, and protocol?
- a) VPN Gateway
- b) Network Security Groups
- c) Virtual Cross-Connection
- d) Network Virtual Appliances

**E118.** What does Virtual Network Peering enable in Azure? A. Direct networks connection between Azure and on-premises
- b) Private network traffic over the public internet
- c) Secure communication between subnets
- d) Global interconnection of Azure resources

**E119.** What is the main purpose of a VPN gateway in Azure?
- a) Securely connect Azure resources to the public internet
- b) Establish private and secure connections between Azure and on-premises environments
- c) Provide high-speed internet connectivity to Azure VMs D. Facilitate communication between Azure Virtual Networks

**E120.** What is the significance of the "Gateway Type" in VPN Gateway configuration?
- a) It determines the Azure region.
- b) It specifies the hardware used for the gateway.
- c) It defines how the gateway will function.
- d) It selects the VPN encryption method.

**E122.** What is the purpose of PolicyBased VPN in Azure?
- a) Efficient traffic routing
- b) Avoiding overlapping subnets
- c) Facilitating dynamic routing
- d) Ensuring encrypted connections

**E123.** What is the default configuration for VPN gateways concerning resiliency?
- a) Active/Standby
- b) Active/Active with BGP support
- c) ExpressRoute Failover
- d) Zone-Redundant

**E124.** What is the purpose of ExpressRoute Failover with a VPN gateway in Azure?
- a) Enhance global connectivity
- b) Provide additional bandwidth
- c) Ensure continuous connectivity during ExpressRoute outages
- d) Facilitate VPN connectivity to on-premises resources

**E125.** In regions supporting availability zones, how are VPN gateways deployed for enhanced resiliency?
- a) Active/Standby
- b) Active/Active with BGP support
- c) ExpressRoute Failover
- d) Zone-Redundant configuration

**E126.** What does Azure ExpressRoute provide in terms of network connectivity?
- a) Dedicated private connection to Microsoft Cloud
- b) Secure internet connectivity
- c) Public internet routes for data transfer
- d) Dynamic IP addressing for on-premises networks

**E127.** What is the role of ExpressRoute Global Reach in connectivity?
- a) Enhancing global security
- b) Direct communication between on-premises sites
- c) Providing dynamic routing with BGP
- d) Ensuring redundancy for ExpressRoute

**E128.** What dynamic routing protocol does ExpressRoute use for efficient traffic routing?
- a) VPN
- b) DNS
- c) BGP (Border Gateway Protocol)
- d) HTTP

**E129.** Which connectivity model is described as treating Azure as one of the branch offices in an IPVPN network?
- a) Any-to-Any (IPVPN) Networks
- b) Virtual Cross-Connection
- c) Point-to-Point Ethernet Connection
- d) Layer 3 Connectivity

**E130.** What is the primary advantage of co-locating a facility at a cloud exchange with ExpressRoute?
- a) Increased internet speed
- b) Enhanced security through encryption
- c) Efficient public internet connectivity
- d) Establishing a virtual cross-connect to the Microsoft cloud

**E131.** What is the primary focus of Azure Cosmos DB, as mentioned in the article?
- a) Gaming applications
- b) Web development
- c) AI-powered applications
- d) IoT solutions

**E132.** Which operational data models does Azure Cosmos DB support?
- a) Relational and document only
- b) Relational, document, vector, key-value, graph, and table
- c) NoSQL and MongoDB only
- d) Table and PostgreSQL only

**E133.** What key benefit does Azure Cosmos DB offer for app development?
- a) Low latency and high availability
- b) Single-digit millisecond response times
- c) Automatic management and updates
- d) Turnkey multi-region data distribution

### Answers — Section E (Batch 5)

| # | Answer | Explanation |
|---|---|---|
| E107 | **d** | Cost reduction is the outcome when cloud computing reduces capital expenses. |
| E108 | **b** | Cost avoidance focuses on preventing future refresh cycles. |
| E109 | **c** | Capital expenses are generally non-recurring while operating expenses are recurring costs. |
| E110 | **c** | Sentara Healthcare achieved record cost savings with Azure, eliminating $54,000 USD in monthly costs. |
| E111 | **b** | Azure Virtual Network enables the creation of multiple isolated virtual networks. |
| E113 | **b** | Assigning a public IP address or using a public load balancer incorporates internet connections. |
| E114 | **c** | Secure communication is achieved through virtual networks and service endpoints. |
| E115 | **d** | The three mechanisms are Point-to-Site VPN, Site-to-Site VPN, and Azure ExpressRoute. |
| E116 | **c** | Route Tables allow the definition of rules governing traffic direction. |
| E117 | **b** | Network Security Groups contain multiple inbound and outbound security rules. |
| E118 | **d** | Virtual Network Peering enables a direct connection between two virtual networks, creating a globally interconnected network. |
| E119 | **b** | A VPN gateway helps establish private and secure connections between Azure and on-premises environments. |
| E120 | **c** | The "Gateway Type" determines how the VPN gateway will function. |
| E122 | **b** | PolicyBased VPN restricts traffic flow to particular network subnets, avoiding overlapping subnets. |
| E123 | **a** | By default, VPN gateways are deployed in an Active/Standby configuration. |
| E124 | **c** | ExpressRoute Failover ensures continuous connectivity during ExpressRoute outages. |
| E125 | **d** | In regions supporting availability zones, VPN gateways can be deployed in a Zone-Redundant configuration. |
| E126 | **a** | Azure ExpressRoute provides a dedicated private connection to Microsoft Cloud. |
| E127 | **b** | ExpressRoute Global Reach facilitates direct communication between on-premises sites. |
| E128 | **c** | ExpressRoute uses the Border Protocol (BGP) for dynamic routing. |
| E129 | **a** | In an IPVPN network, Azure is treated as one of the branch offices. |
| E130 | **d** | Co-locating at a cloud exchange allows establishing a virtual cross-connect to the Microsoft cloud through ExpressRoute. |
| E131 | **c** | Azure Cosmos DB is highlighted as an AI database in the context of AI-powered applications. |
| E132 | **b** | Azure Cosmos DB accommodates all operational data models, including relational, document, vector, key-value, graph, and table. |
| E133 | **a** | Azure Cosmos DB offers low latency, high availability, and automatic management development. |

**E134.** Which feature enables guaranteed speed at any scale in Azure Cosmos DB?
- a) Automatic scaling
- b) Real-time access
- c) Fast global access
- d) Serverless model

**E135.** How does Azure Cosmos DB achieve multi-region writes and data distribution?
- a) By using PostgreSQL
- b) By leveraging Azure AI Services
- c) By pressing a button
- d) Through manual configuration

**E137.** What is the primary advantage of using Azure Cosmos DB for IoT and telematics applications?
- a) High throughput
- b) Low latency
- c) Guaranteed speed
- d) Multi-region writes

**E138.** Which of the following is not mentioned as one of the Azure Cosmos DB's key benefits?
- a) Serverless model
- b) Real-time access
- c) Unlimited scale worldwide
- d) Manual patching and updates

**E139.** What is the purpose of the Azure AI Advantage offer mentioned in the article?
- a) Free trial for Azure Cosmos DB with 40,000 RU/s throughput
- b) Discounts for existing Azure AI or GitHub Copilot customers
- c) A lifetime free tier for Azure Cosmos DB
- d) 30-day Free Trial for non-Azure customers

**E140.** What does the term "RU/s" stand for in the context of Azure Cosmos DB?
- a) Real-time Units per Second
- b) Requested Units per Second
- c) Readability Units per Second
- d) Reliable Units per Second

**E141.** What is the lifetime free tier offering for Azure Cosmos DB?
- a) 40,000 RU/s for 90 days
- b) 30-day Free Trial without Azure subscription
- c) 1000 RU/s and 25 GB storage for free
- d) Serverless and automatic scaling options

**E142.** Which feature makes it easy to track and manage changes to database containers in Azure Cosmos DB?
- a) Real-time access
- b) Change feed
- c) Automatic scaling
- d) Multi-region writes

**E143.** What does the "schema-less service" in Azure Cosmos DB automatically index?
- a) Only document data
- b) Only relational data
- c) All data, regardless of the data model
- d) Only key-value data

**E144.** What is the cost-effective model in Azure Cosmos DB for unpredictable or sporadic workloads?
- a) Automatic scaling
- b) Serverless model
- c) Capacity planning
- d) Manual scaling

**E145.** What does the "30-day Free Trial" without an Azure subscription offer to users?
- a) 40,000 RU/s throughput for 30 days
- b) Free access to Azure Cosmos DB for 30 days
- c) 30 days of unlimited storage
- d) 30 days of automatic scaling
- e) Enforcing naming.

**E146.** What is the purpose of Azure Cosmos DB Live TV sessions every Thursday at 1 PM Pacific?
- a) Free training on Azure Cosmos DB
- b) Troubleshooting sessions
- c) Live coding sessions
- d) Learning more about Azure Cosmos DB

**E147.** Which Azure Cosmos DB functionality is mentioned for seamless integration with Azure AI Services?
- a) Automatic scaling
- b) Turnkey multi-region data distribution
- c) Native vector search
- d) Real-time access

**E148.** What does the Azure Cosmos DB "Change feed" feature facilitate?
- a) Automatic database backups
- b) Real-time access with low latencies
- c) Tracking and managing changes to database containers
- d) Schema-based data indexing

**E149.** What is the primary goal of integrating Azure Cosmos DB with Azure AI Services?
- a) Enhanced serverless model
- b) Improved change feed functionality
- c) Seamless integration with Azure AI Services
- d) Cost-effective scaling options

**E150.** Which key benefit does Azure Cosmos DB provide for application development?
- a) Automatic backup scheduling
- b) Single-region data distribution
- c) Schema-based data modeling
- d) Open-source APIs and multiple SDKs

**E151.** What is the purpose of the Control node in Synapse SQL's dedicated SQL pool architecture?
- a) Manage data storage
- b) Execute parallel queries
- c) Coordinate data movements
- d) Distribute compute power

**E152.** What is the role of the Compute nodes in Synapse SQL's dedicated SQL pool architecture?
- a) Distributing data across Azure Storage
- b) Executing parallel queries and providing computational power
- c) Managing data-sharding patterns
- d) Coordinating data movements

**E153.** Which technology coordinates data movement between Compute nodes in Synapse SQL?
- a) Control node
- b) Azure Storage
- c) Data Movement Service (DMS)
- d) Distributed query engine

**E154.** What is the basic unit of storage and processing for parallel queries in Synapse SQL?
- a) Control node
- b) Compute node
- c) Distribution
- d) Data Movement Service (DMS)

**E155.** How can you independently size compute power in Synapse SQL's dedicated SQL pool?
- a) By resizing Azure Storage
- b) By choosing a sharding pattern
- c) Independently of your storage needs
- d) By increasing Data Movement Service (DMS) capacity

**E156.** What is the purpose of the Data Movement Service (DMS) in Synapse SQL?
- a) Execute T-SQL commands
- b) Coordinate data movement between Compute nodes
- c) Manage Azure Storage
- d) Distribute compute power

**E157.** Which table distribution strategy provides the highest query performance for joins and aggregations on large tables in Synapse SQL?
- a) Round-robin
- b) Replicated
- c) Hash-distributed
- d) Sharded

**E158.** When is a round-robin distributed table suitable for optimal performance in Synapse SQL?
- a) Always
- b) For small tables and fast data loading
- c) For hash-based queries
- d) For caching purposes

**E159.** What does a replicated table do in Synapse SQL?
- a) Distributes data evenly
- b) Provides fast query performance for small tables
- c) Executes parallel queries
- d) Coordinates data movements

### Answers — Section E (Batch 6)

| # | Answer | Explanation |
|---|---|---|
| E134 | **a** | Automatic scaling enables guaranteed speed at any scale in Azure Cosmos DB. |
| E135 | **c** | Azure Cosmos DB achieves multi-region writes and data distribution with just a button. |
| E137 | **d** | Azure Cosmos DB's guaranteed high availability, high throughput, low latency, and tunable consistency are advantageous for IoT and telematics applications. |
| E138 | **d** | Manual patching and updates are not mentioned as a key benefit; Azure Cosmos DB offers automatic management. |
| E139 | **b** | The Azure AI Advantage offer provides a free trial with 40,000 RU/s throughput for existing Azure AI or GitHub Copilot customers. |
| E140 | **b** | RU/s stands for Requested Units per Second, representing the throughput in Azure Cosmos DB. |
| E141 | **c** | The lifetime free tier for Azure Cosmos DB includes the first 1000 RU/s of throughput and 25 GB of storage for free. |
| E142 | **b** | Change feed makes it easy to track and manage changes to database containers. |
| E143 | **c** | The schema-less service automatically indexes all data, regardless of the data model. |
| E144 | **b** | The serverless model offers a cost-effective option for unpredictable or sporadic workloads. |
| E145 | **b** | The 30-day Free Trial without an Azure subscription allows users to access Azure Cosmos DB for 30 days |
| E146 | **d** | Azure Cosmos DB Live TV sessions provide an opportunity to learn more about Azure Cosmos DB. |
| E147 | **c** | Native vector search is mentioned as an Azure Cosmos DB functionality for seamless integration with Azure AI Services, supporting Retrieval Augmented Generation. |
| E148 | **c** | The Change feed feature in Azure Cosmos DB makes it easy to track and manage changes to database containers, enabling the creation of triggered events with Azure Functions. |
| E149 | **c** | Azure Cosmos DB's integration with Azure AI Services aims for seamless integration to functionalities like native vector search. |
| E150 | **d** | Azure Cosmos DB offers open-source APIs, multiple SDKs, and schemaless data, making it easier for developers to build applications. The use of open-source APIs allows flexibility in language choice, and SDKs are available for .NET, Java, Node.js, and Python. |
| E151 | **c** | The Control node is responsible for coordinating parallel queries and optimizing their execution by interacting with the distributed query engine. |
| E152 | **b** | Compute nodes provide the computational power and execute parallel queries in the distributed SQL pool architecture. |
| E153 | **c** | responsible The for Data Movement coordinating data Service movement (DMS) is between Compute nodes. |
| E154 | **c** | A distribution is the basic unit of storage and processing for parallel queries in Synapse SQL. |
| E155 | **c** | Compute power can be sized independently of storage needs in Synapse SQL's dedicated SQL pool. |
| E156 | **b** | DMS coordinates data movement between Compute nodes to ensure accurate parallel query results. |
| E157 | **c** | Hash-distributed tables provide the highest query performance for joins and aggregations on large tables. |
| E158 | **b** | Round-robin tables are suitable for fast data loading, especially for staging tables. |
| E159 | **b** | A replicated table provides fast query performance for small tables by caching a full copy on each compute node. |

**E160.** Which sharding patterns are supported for distributions in Synapse SQL's dedicated SQL pool?
- a) Hash, Round Robin, and Replicate
- b) Linear, Circular, and Spiral
- c) Random, Sequential, and Weighted
- d) Redundant, Balanced, and Dynamic

**E161.** What is the Internet of Things (IoT)?
- a) A cloud hosting service
- b) A network of physical devices exchanging data
- c) A machine learning framework
- d) A programming language 162 What is Azure IoT Hub, and what role does it play in IoT applications?
- a) A cloud-based sensor service
- b) An authentication service for IoT devices
- c) A central message hub for IoT communication
- d) An IoT device manufacturing platform

**E163.** How many connected devices can Azure IoT Hub support simultaneously?
- a) Thousands
- b) Millions
- c) Hundreds
- d) Billions

**E164.** Which messaging patterns are supported by IoT Hub?
- a) Cloud-to-device telemetry only
- b) Device-to-cloud telemetry, file uploads, and request-reply methods
- c) Cloud-to-cloud communication only
- d) Device-to-device communication

**E165.** What is the purpose of IoT Hub monitoring?
- a) Tracking device creation
- b) Monitoring backend solutions
- c) Identifying device failures
- d) All of the above

**E166.** Which Azure service can be integrated with IoT Hub for quick reactions to critical events?
- a) Azure Machine Learning
- b) Azure Event Grid
- c) Azure Logic Apps
- d) Azure Stream Analytics

**E167.** What are the characteristics of IoT devices compared to other clients?
- a) Always have a human operator
- b) Require constant physical access
- c) Can be embedded, have limited power, and might have intermittent connectivity
- d) Use standard application protocols

**E168.** What is the identity registry in IoT Hub used for?
- a) Storing device telemetry
- b) Managing device modules
- c) Storing information about devices and modules
- d) Authenticating cloud applications 169 Which authentication methods are supported for deviceto-IoT Hub communication?
- a) JWT token-based authentication
- b) OAuth-based authentication
- c) SAS token-based and X.509 certificate authentication
- d) API key-based authentication

**E170.** What is the purpose of the IoT Hub Device Provisioning Service?
- a) Authenticating devices
- b) Scaling device communication
- c) Setting up and provisioning many devices at a time
- d) Monitoring device telemetry

**E171.** How is the internet connection between IoT devices and IoT Hub secured?
- a) Using a proprietary encryption method
- b) Using OAuth 2.0
- c) Utilizing Transport Layer Security (TLS)
- d) Employing device-specific encryption keys

**E172.** Which versions of TLS does Azure IoT support for communication with IoT Hub?
- a) TLS 1.3 only
- b) TLS 1.2, TLS 1.1, and TLS 1.0
- c) TLS 2.0 only
- d) TLS 1.1 and TLS 1.0 only

**E173.** What types of communication are possible between IoT devices and backend services?
- a) Only telemetry from sensors
- b) Telemetry, file uploads, and request-reply methods
- c) Only cloud-to-cloud communication
- d) Device-to-device communication

**E174.** What is the purpose of device telemetry in IoT applications?
- a) Sending commands to devices
- b) Tracking device creation
- c) Monitoring device health and receiving sensor data
- d) Authenticating devices

**E175.** What are examples of telemetry received from IoT devices?
- a) Web pages and images
- b) SQL database queries
- c) Sensor data, error messages, and information messages
- d) Device commands and properties

**E176.** How are IoT device properties used in IoT Hub?
- a) For storing device telemetry
- b) As a part of device authentication
- c) To send notifications when actions have been completed
- d) Only for device provisioning

**E177.** What are IoT Device Twins and Plug and Play used for in IoT Hub?
- a) Device authentication
- b) Telemetry encryption
- c) Enabling device properties
- d) Setting up device provisioning

**E178.** What is the purpose of IoT Hub Device Commands?
- a) Sending telemetry from devices to the cloud
- b) Executing direct methods on devices
- c) Authenticating devices
- d) Storing device properties

**E179.** How does IoT Hub unlock the value of device data with other Azure services?
- a) By storing all data within the IoT Hub
- b) By sending device data to Azure Machine Learning
- c) By integrating with Azure services for machine learning, analytics, and AI
- d) By routing all data to a central endpoint

**E181.** What is the purpose of Azure Machine Learning Designer?
- a) To write code for ML models
- b) To train ML models without writing code
- c) To deploy ML models automatically
- d) To visualize ML data

**E182.** What is the benefit of Automated machine learning UI?
- a) It allows for manual optimization of hyperparameters
- b) It automates the process of training ML models
- c) It provides advanced visualization tools for ML data
- d) It enables direct integration with Azure services

**E183.** What is the purpose of Data labeling in Machine Learning?
- a) To preprocess data before training models
- b) To efficiently coordinate image or text labeling projects
- c) To optimize hyperparameters in ML models
- d) To visualize the performance metrics of ML models

**E184.** Which Azure service can be used to save security secrets for ML projects?
- a) Azure Storage
- b) Azure Key Vault
- c) Azure Event Grid
- d) Azure Synapse Analytics

**E185.** What is the purpose of Azure Synapse Analytics in ML projects?
- a) To process and stream data with Spark
- b) To automate ML model training
- c) To visualize ML data metrics
- d) To manage ML experiments

**E186.** Which stage of the machine learning project lifecycle involves automating users' work in an ML pipeline?
- a) Model Deployment
- b) Data labeling
- c) Model training
- d) Project operationalization

**E187.** What types of models can be brought into Azure Machine Learning for operationalization?
- a) Only models trained in Azure ML Studio
- b) Only models built from scratch in Azure ML
- c) Models trained in open-source frameworks like PyTorch and TensorFlow
- d) Models built using Azure Machine Learning Designer only

### Answers — Section E (Batch 7)

| # | Answer | Explanation |
|---|---|---|
| E160 | **a** | Synapse SQL supports sharding patterns such as Hash, Round Robin, and Replicate for distributions. |
| E161 | **b** | IoT is a network of physical devices that connect and exchange data over the internet. |
| E163 | **b** | Azure IoT Hub scales to support millions of simultaneously connected devices. |
| E164 | **b** | IoT Hub supports device-to-cloud telemetry, file uploads, and request-reply methods. |
| E165 | **d** | IoT Hub monitoring helps track device creation, connections, and failure |
| E166 | **b** | Azure Event Grid enables quick reactions to critical events in a scalable and secure manner. |
| E167 | **c** | IoT devices are often embedded, have limited power, and might have intermittent, slow, or expensive network connectivity. |
| E168 | **c** | The identity registry stores information about devices and modules permitted to connect to the IoT Hub. |
| E170 | **c** | The Device Provisioning Service is used to set up and provision many devices at a time |
| E171 | **c** | The internet connection is secured using Transport Layer Security (TLS). For further result. You can visit the given URL |
| E172 | **b** | Azure IoT supports TLS 1.2, TLS 1.1, and TLS 1.0 for communication. For further result. You can visit the given URL |
| E173 | **b** | Various communication types include telemetry, file uploads, and request-reply methods. |
| E174 | **c** | Device telemetry involves receiving sensor data and monitoring device health |
| E175 | **c** | Telemetry can include sensor data, error messages, and information messages from IoT devices. |
| E176 | **c** | Device properties can be used to send notifications when actions have been completed. |
| E177 | **c** | IoT Device twins and Plug and Play enable the use of properties in IoT Hub |
| E178 | **b** | Device Commands involve executing direct methods on devices |
| E179 | **c** | IoT Hub integrates with Azure services for machine learning, analytics, and AI. |
| E181 | **b** | Azure Machine Learning Designer allows users to train and deploy ML models without writing any code by using a drag-and-drop interface. |
| E182 | **b** | The Automated machine learning UI simplifies the process of creating automated ML experiments with an easy-to-use interface. |
| E183 | **b** | Data labeling in Machine Learning is used to efficiently coordinate image labeling or text projects, making data annotation easier. |
| E184 | **b** | Azure Key Vault can be used to save security secrets, such as access information for storage accounts, in ML projects. |
| E185 | **a** | Azure Synapse Analytics is used to process and stream data with Spark in ML projects |
| E186 | **d** | Project operationalization involves automating users' work in an ML pipeline and triggering it on a schedule or HTTPS request. |
| E187 | **c** | Models created in common Python frameworks like PyTorch, TensorFlow, scikit-learn, XGBoost, and others can be operationalized in Azure Machine Learning. |

**E188.** What is the purpose of Automated ML (AutoML) in Azure Machine Learning?
- a) To optimize hyperparameters manually
- b) To speed up the process of selecting data featurization and algorithms
- c) To visualize ML data
- d) To deploy ML models to production

**E189.** Which Azure service enables multi-node distributed training for deep learning jobs?
- a) Azure Event Grid
- b) Azure Container Registry
- c) Azure Synapse Analytics
- d) Azure Machine Learning compute clusters

**E190.** What is the purpose of Real-time and batch scoring (inferencing) in ML projects?
- a) To visualize model performance metrics
- b) To train ML models with new data
- c) To automate model deployment
- d) To obtain predictions from trained models in real-time or batch mode

**E191.** What does the NIST CSF (Cybersecurity Framework) aim to achieve?
- a) Establish additional regulatory requirements
- b) Maintain measurement standards and guidance C. Enforce cybersecurity policies on private sector organizations
- d) Focus exclusively on government cybersecurity

**E192.** What was the main priority of the Framework for Improving Critical Infrastructure Cybersecurity (FICIC)?
- a) Imposing regulatory requirements
- b) Enabling business efficiency
- c) Restricting government cybersecurity
- d) Standardizing global cybersecurity practices

**E193.** Which standards are referenced in the FICIC framework, and what are they mapped to in NIST SP 80053?
- a) ISO 27001, mapped to FedRAMP High Baseline
- b) NIST SP 800-53, mapped to FedRAMP Moderate Baseline
- c) GDPR, mapped to HIPAA requirements
- d) CIS Controls, mapped to PCI DSS

**E194.** How long is the NIST CSF certification of Office 365 valid?
- a) One year
- b) Two years
- c) Three years
- d) Indefinitely

**E195.** Which independent organization provided the NIST CSF letter of certification for Office 365?
- a) NIST
- b) FedRAMP
- c) ISO
- d) HITRUST

**E196.** How can Microsoft demonstrate compliance with the NIST Framework for Improving Critical Infrastructure Cybersecurity?
- a) Through internal audits only
- b) By obtaining FedRAMP accreditation
- c) By participating in FICIC on a voluntary basis
- d) By excluding non-compliant services from the offering

**E197.** What does Microsoft's participation in the FICIC involve?
- a) Mandatory regulatory compliance
- b) Voluntary participation
- c) Exclusively for government organizations
- d) Direct integration with NIST SP 800-53

**E198.** Who is responsible for ensuring compliance with all applicable laws and regulations according to the provided information?
- a) Microsoft
- b) HITRUST
- c) United States Government
- d) Respective organizations

**E199.** Why might some Office 365 services not be in the scope of NIST CSF certification?
- a) Lack of demand from customers
- b) Limited market availability
- c) Regulatory restrictions
- d) Continuous expansion of compliance offerings

**E200.** What is the purpose of Microsoft Purview Compliance Manager in relation to NIST CSF?
- a) To enforce regulatory requirements
- b) To build ML models for compliance
- c) To assess an organization's compliance posture
- d) To replace NIST CSF certification

**E201.** The Software Architect of an organization is responsible for managing and developing the Azure resources, such as Virtual Machine (VM) on Android OS/Linux. Due to the wide responsibilities, the Software Architect wants an automated and authenticated management tool to configure the VM. Which of the following can Software Architect use to configure a VM?
- a) Azure CLI
- b) Microsoft PowerApps
- c) Azure Cloud Shell
- d) Azure Power Shell

**E202.** Which statement is valid for the Software as a Service (SaaS) model?
- a) You are responsible for configuring the solution
- b) You are responsible for the high availability of the solution
- c) You are responsible for deploying the solution
- d) You are responsible for the scalability of the solution

**E203.** Harry, an App developer, is working with Azure services. He is planning to build a real-time application that enables event-based reactive programming. Which of the following Azure service helps implement this type of application?
- a) Azure Kubernetes
- b) Azure Event Grid
- c) Azure DevTest Labs
- d) Azure DevOps

**E204.** An organization is recently shifting its resources from on-premises to Azure. The organisation's owner needs to give business justification for this migration, showing the expenses of “Software Licensing” as a part of the justification. Which of the following category includes this type of expense?
- a) Capital Expenditure
- b) Secondary Expenditure
- c) Operating Expenditure
- d) Primary Expenditure

**E205.** Mark is an IT Engineer using Azure resources. He deploys an Azure Virtual Machine with the following set of configuration details. The Premium disk sized 128 GB is attached to the deployed machine. The Premium SSD disk with a size of 127 GiB is attached to the VM, as shown in the figure. The deployed machine is in the “Stopped (Deallocated)” state. Would he still be charged for the disk attached to the machine?
- a) Yes
- b) No

**E206.** A company plans to design a secure network and share the application secrets with a third party without revealing the actual secret. Which of the following Azure services is used for the sharing of secrets?
- a) Azure Network Security Group
- b) Azure DDoS Protection
- c) Azure Key Vault
- d) Azure Multi-Factor Authentication

**E207.** An organization starts using Azure resources and has a pay-as-you-go subscription. The organization has a private cloud model for sensitive and critical applications. The organization wants to implement a hybrid cloud infrastructure for some purpose. Would they need to shift their private cloud model into a hybrid one?
- a) Yes
- b) No

**E208.** Olivia is working on cloud services and finds some benefits in this regard. Which of the following is best suited for the given statement? “The users with the minimum time can access all Cloud services”.
- a) Low Latency
- b) Dynamic Scalability
- c) Fault Tolerance
- d) Disaster Recovery

**E209.** The owner of a company calls a meeting to find the solution to the given scenario: “There is a web server that receives consecutive requests from different sources simultaneously; these continuous requests stop the server from working abruptly”. One of their employees suggested using the Azure Information Protection service. Is this suggestion helpful for the given scenario?
- a) Yes
- b) No

**E210.** An IT company deploys many Azure Virtual Machines. Before deployment, an Account Administrator implemented a manual draft of the cost that is incurred for these VMs. Which of the following Azure services recommend reducing the cost of these VMs?
- a) Cost Management + Billing
- b) Virtual Machines
- c) Help + Support
- d) Advisor

**E211.** An IT Engineer implements a set of Virtual Machines (VMs) on which critical application is installed. To ensure the availability of the application 99.99% of the time and protection of the application from any data center failure, they decide to implement a set of VMs in more than one availability zone. Would this approach help improve the performance of an application?
- a) Yes
- b) No

**E212.** An organization found issues in their Azure resource using Azure Service Health. Would an IT Admin be able to use Azure Service Health to create some rules that protect their Azure resources from issues?
- a) Yes
- b) No

### Answers — Section E (Batch 8)

| # | Answer | Explanation |
|---|---|---|
| E188 | **b** | Automated ML (AutoML) speeds up the process of selecting data featurization and algorithms by automating repetitive tasks. |
| E189 | **d** | Azure Machine Learning compute clusters enable multi-node distributed training for deep learning jobs. |
| E190 | **d** | Real-time and batch scoring (inferencing) involves obtaining predictions from trained models in realtime or batch mode, depending on the deployment scenario. |
| E191 | **b** | The NIST CSF aims to maintain measurement standards and guidance to help organizations assess cybersecurity risk. |
| E192 | **b** | The main priority of FICIC was to establish standards and practices to manage cybersecurity risk while enabling business efficiency. |
| E193 | **b** | The FICIC framework references NIST SP 800-53, which is mapped to FedRAMP Moderate Baseline controls. |
| E194 | **b** | The NIST CSF certification of Office 365 is valid for two years. |
| E195 | **d** | HITRUST provided the NIST CSF letter of certification for Office 365 in July 2019. |
| E196 | **b** | Microsoft can demonstrate compliance through formal audit reports prepared by third parties for the FedRAMP accreditation. |
| E197 | **b** | Participation in the FICIC is voluntary for organizations like Microsoft. |
| E198 | **d** | Organizations are wholly responsible for ensuring compliance with all applicable regulations. |
| E199 | **d** | Services are included in the scope based on market demand, customer feedback, and product lifecycle. |
| E200 | **c** | Microsoft Purview Compliance Manager helps organizations understand their compliance posture and reduce risks by offering assessment templates, including for NIST CSF. |
| E201 | **c** | Azure Cloud Shell is a browser-based workstation that provides an automated and authenticated way of managing and deploying Azure resources. It saves the user from manual monitoring and installation of resources. Option A is not used for the given situation because it is only specific to the command line. Option B is invalid because it is used f... |
| E202 | **a** | Software as a Service (SaaS) delivers the service that the user demands. Cloud runs a single instance of the software and makes it available for all users. Examples of such service delivery models are Google, Dropbox, etc. All the remaining options are invalid because SaaS is a service used by end customers via a browser. The end-user or custome... |
| E203 | **b** | Azure Event Grid is a beneficial service for any App developer building a real-time application that needs to react to events being in Azure services. Azure Event Grid is a cheap and reliable Azure service that manages the full event routing services. All the remaining options are invalid for the given situation. |
| E204 | **c** | In cloud computing, the software, cloud applications, storage, IT operations, and rented hardware are Operation Expenditures. The usage of the Azure resources, services, deployment of the networks, and building of applications all come in operational expenditure. |
| E205 | **a** | Azure Virtual Machines do not charge in the “Stopped (Deallocated)” state. The disk associated with a virtual machine is always charged whether the VM is in its current state or not. |
| E206 | **c** | Azure Key Vault stores the secret and password. It allows the sharing of passwords and secrets with others in a hidden form so that nobody can view the actual secret. Option A is invalid because the Network Security Group (NSG) acts as a resource firewall to prevent network resources from unwanted traffic loads. Option B is invalid because the D... |
| E207 | **b** | If an organization wants to deploy a hybrid cloud model, there is no need to shift private model because a hybrid cloud is a combination of public and private clouds. Hybrid cloud infrastructure makes applications and data features publicly and privately available to users. It offers a multi-tenancy approach with secure and private features. |
| E208 | **a** | The main benefit of cloud service is that it is free for hardware implementation. All the implementation is done in a cloud environment for acceptable low latency and the fastest service response. Internet users can achieve reliable access to the applications available on the internet with low latency. Option B is invalid because scalability is ... |
| E209 | **b** | Azure Information Protection (AIP) provides a way of protecting sharing of resources. Azure Information Protection enables the sharing of files, documents, and sensitive information inside and outside Azure while maintaining full control over that data. It does not protect the server from consecutive user requests simultaneously. |
| E210 | **d** | Azure Advisor optimizes Azure resources for high availability, performance, security, and cost. It enables quick access recommendations to personalized and from the dashboard. Advisor actionable Azure Advisor tool presents recommendations to improve security and reduce the cost of Azure resources. All the remaining options are invalid, as no one... |
| E211 | **a** | Availability Zones are present within Azure regions. These zones provide highly available protected areas to run applications and data. By using more than one availability zone, the application performance is improved, and the application is protected from data center failure. |
| E212 | **b** | The scale set service can be used to prevent the Azure resources from failing. Suppose there is an issue found in Azure Virtual Machine; then, virtual machine scale sets can be used to scale VMs and prevent failure. Azure Service Health cannot be used in the given situation; service health is only responsible for the issues alert. |

**E213.** Access protection is crucial when data is stored on the company’s server. For this, a company plans to study the use of the Azure Information Protection service. Which of the following is Azure Information Protection service used for?
- a) Documents and Email Messages
- b) Network Traffic
- c) Azure Storage Accounts
- d) Microsoft Entra ID Identities

**E214.** Frankel is a Data Engineer in an IT company. The company uses Azure resources for its pay-as-you-go Azure subscription. He deploys Azure Cosmos DB. Would he need to manage the index of data whenever he stores data in Azure Cosmos DB?
- a) Yes
- b) No

**E215.** Marc is an IT Engineer in an organization. He developed an Azure Resource Group named “Ips” with the following resources. Currently, a complex application is running on the “ips-vm”, a virtual machine in “Ips”. The company makes a policy that “ips-vm” is not an allowed resource type of resource group “Ips”. What would happen when the company assigns this policy to the resource group “Ips”?
- a) The network is moved to the different resource group
- b) The network is automatically deleted
- c) The virtual machine would continue to exist as it is
- d) The network resources would become a read-only resource

**E216.** An IT company wants to deploy a set of Virtual Machines (VMs) on which sensitive data application is installed. The IT Engineer implements the same set of VMs in different Azure regions to improve the application performance and availability. Would the approach of using multiple regions help improve availability?
- a) Yes
- b) No

**E217.** An organization assigns a task to the Resource Manager to implement the service alerts highlighting the issues in Azure services. Would Azure Service Health be used for creating the service health alerts?
- a) Yes
- b) No

**E218.** Mark is a Data Engineer in an organization using Azure resources and services due to its big data-wide response services. Mark wants to find the solution for the following requirements: “Provide a solution to perform big data analytics of data stored on Azure blob storage”. Which service is used as a solution for the given requirement?
- a) Azure Storage Accounts
- b) Azure SQL Data Warehouse
- c) Azure Data Lake Storage
- d) Azure Application Gateway

**E219.** An IT Engineer of an organization creates an Azure Cosmos DB due to its multiple data stores and continuous availability capabilities. Would the IT Engineer be able to deploy custom software using Azure Cosmos DB?
- a) Yes
- b) No

**E220.** An IT company uses Azure resources and has several Azure storage accounts for data storage. One of the employees deploys a web application that stores user profile information. The company decides to use table storage for storing the user profile information. Would the decision of the company be correct?
- a) Yes
- b) No

**E221.** An organization wants to create a set of Virtual Machines (VM) on which a complex application is installed. The Network Engineer wants to ensure an application's availability even if one of the data centers goes down. They use Azure virtual machine scale sets to ensure the application's availability in the availability zone. Would this Azure service help to increase the VM instance for high availability?
- a) Yes
- b) No

**E222.** A company is using Azure resources, and one of the implemented Azure VM went down due to some incident. An IT Admin wants to find the incident in their Azure Virtual Machine named “ips-vm”. Would Azure Service Health be used to highlight the issues in Azure Virtual Machine “ips-vm”?
- a) Yes
- b) No

**E223.** Johnny is a Data Engineer in an organization. The organization wants to set up a solution that stores petabytes of data and can run queries on relational and non-relational data. Which Azure service can be used to meet the organisation's requirements?
- a) Azure Storage Accounts
- b) Azure Synapse
- c) Azure Firewall
- d) Azure Application Gateway

**E224.** An organization is using Azure Cosmos DB for its database requirement. Does Azure Cosmos DB provide the functionality of a multi-model database?
- a) Yes
- b) No

**E225.** An organization has a different storage account to store data in Azure. The IT Engineer of the organization implemented an application that required user-related information. They use a File storage service to store user-related information on Azure. Is their decision correct?
- a) Yes
- b) No

**E226.** A networking company implemented a network using Azure resources on which complex and sensitive applications are running. A Security Engineer is tasked with protecting the application’s secret when applications are running. Which Azure service can be used in the given situation?
- a) Azure Storage Account
- b) Azure Identity Protection
- c) Microsoft Defender for Cloud
- d) Azure Key Vault

**E227.** An organization wants to implement a network on which multiple applications are running. An IT Engineer of the organization wants to highlight the impact of the availability zone. Could an availability zone be used to reproduce data in multiple regions?
- a) Yes
- b) No

**E228.** An organization creates a network with different Azure resources and services. A web application is installed on the VMs. A network must be able to store data that the user over the internet can access. Which of the following Azure services is responsible for providing the given demand?
- a) Azure Storage Accounts
- b) Azure Application Gateway
- c) Azure SQL Data Warehouse
- d) Azure Data Lake Storage

**E229.** An IT company is using Azure resources. The company has a Windows Server license as a part of a Software Assurance agreement. Would the company benefit from deploying the Azure Virtual Machines?
- a) Yes
- b) No

**E230.** An organization chooses Azure services to run an application. This application requires the profile information of the user. The organization decides to use an Azure storage account for data storage and Azure blob storage for user profiles. Would this storage option be valid for storing the user profile information?
- a) Yes
- b) No

**E231.** An organization is using Azure resources for its pay-asyou-go subscription. There are multiple Azure customers associated with an organization. An IT Admin needs to monitor the record that shows the actions done on resources in the last 24 hours. Which of the following Azure services will help an IT Admin to find the changes done by the customer in particular Azure resources?
- a) Azure Activity Logs
- b) Azure Advisor
- c) Azure Service Health
- d) Azure Event Hubs

**E232.** An organization wants to create a network with Linux and Windows-based Virtual Machines. The organization deployed machines in different availability zones to ensure high availability. Is it possible to have multiple availability zones for both Linux and Windows-based Virtual Machines?
- a) Yes
- b) No

**E233.** A company wants to find out the Azure solution for the given situation. “Enables the balancing of web traffic to manage the web applications using an HTTP request.”. Which of the following Azure services will provide the best solution?
- a) Azure Application Gateway
- b) Azure Data Lake Storage
- c) Azure SQL Data Warehouse
- d) Azure Storage Accounts

**E234.** An organization is shifting all on-premises resources to Azure. To migrate the on-premises SQL server 2005 database to Azure SQL Database, the organization decides to use Azure Database Migration Service. Would their decision be correct for the database migration?
- a) Yes
- b) No

**E235.** An organization decides to implement a network with two virtual machines. The machines host web applications, and users can access these applications via the internet. Would it be possible to use Azure virtual machine scale sets service to ensure the availability of applications?
- a) Yes
- b) No

**E236.** A company wants to deploy an Azure solution platform that serves as an online place for buying and selling the product, application, and solution discovered for a cloud solution. What helps the company view the available products and allows the company to search for the resource?
- a) In Azure Monitor
- b) In Microsoft Defender for Cloud
- c) In the Azure Marketplace
- d) In Azure Advisor

**E237.** James is a Data Engineer in an organization. The organization has a pay-as-you-go subscription. They created a Virtual Network (VNet) in Azure, linked onpremises using a virtual private network connection. James prepared a report that contains the worth of data transfer from the Azure cloud to the on-premises network. The worth is about 20GB per month. Would an organization need to pay additional charges for this outbound data transfer?
- a) Yes
- b) No

### Answers — Section E (Batch 9)

| # | Answer | Explanation |
|---|---|---|
| E213 | **a** | Azure Information Protection provides a way of protecting the sharing of resources. Azure Information Protection (AIP) enables the sharing of files, documents, and sensitive information more securely outside the organization. All the remaining options are invalid because no one is used for sharing the document and email messages. |
| E214 | **b** | Azure Cosmos DB is responsible for the entire global distribution of data, and it can automatically scale to meet the demands. Cosmos DB promises a maximum of 9millisecond latency anywhere in the world. In addition, Azure Cosmos DB can provide various data stores like Mongo DB, Cassandra, etc. It automatically implements schema for applications ... |
| E215 | **c** | When an Azure Policy is assigned to a particular resource group. The resources in the resource group would remain to exist as it is. The figure shows the policy and assignment details assigned to the resource group “Ips”. All the remaining options are invalid for assignment |
| E216 | **a** | Azure region contains multiple data centers for high availability. Applications are running in the network present in the Azure cloud. A company can deploy a set of VMs in multiple regions for high availability. It gives the advantage of improving application performance so that whenever one set of VMs goes down in the region, the other region w... |
| E217 | **a** | Azure Service Health allows monitoring and alerting the issues to Microsoft Azure. Azure Service Health provides complete information about different issues that happen to the Azure resources of an organization. Service Health provides a customizable dashboard that tracks the health of organization resources. This service allows the creation of ... |
| E218 | **c** | Azure Data Lake Storage is a service specifically designed for big data analytics of data stored on Azure blob storage. Data Lake Storage allows storing relational and non-relational data from any device, video, or web application. All the remaining options are invalid because no one provides relational and non-relational data analytics. |
| E219 | **b** | Azure Cosmos DB is responsible for the entire global distribution of data, and it can automatically scale to meet the demands. Cosmos DB promises a maximum of 9millisecond latency anywhere in the world. In addition, Azure Cosmos DB can provide various data stores like Mongo DB, Cassandra, etc. That’s why this database is also called a multi-mode... |
| E220 | **a** | Table storage is a highly available and cheap data-storing solution in Azure. It is a NoSQL database for every day and is used for serverless applications. designed for high volumes of data, storing key/attributes. |
| E221 | **a** | Azure Virtual Machine Scale Sets is an Azure compute resource that deploys the set of Virtual Machines for the high availability of applications during its peak time. It automatically scales up the group of VMs according to the demands and scales down when needed. |
| E222 | **a** | Azure Service Health allows monitoring and alerting the issues to Microsoft Azure. Azure Service Health provides complete information about different issues that happen to a company's Azure resource. Azure Service Health provides a customizable dashboard that tracks the health of the company’s resources. |
| E223 | **b** | Azure Synapse is a data warehouse that blends the data warehouse, big data analytics, and data integration into a unified service that provides end-to-end analytics at a cloud scale. It stores big data of size petabytes and runs queries on relational and non-relational data. |
| E224 | **a** | Azure Cosmos DB is responsible for the entire global distribution of data, and it can automatically scale to meet the demands. Cosmos DB promises a maximum of 9millisecond latency anywhere in the world. In addition, Azure Cosmos DB can provide various data stores like Mongo DB, Cassandra, etc. That is why this database is also called a multi-mod... |
| E225 | **b** | Azure file storage service is responsible for files and folders shared in the cloud or on-premises network. These files contain the company’s assets. Azure file storage allows the provision of file storage in which we can deploy shares, which can be from Windows, Linux, and Mac operating system machines. |
| E226 | **d** | Azure Key Vault stores the secret and password. It allows sharing of passwords and secrets with others in a hidden form so that nobody can view the actual secret. Azure Key Vault has two primary purposes: centralization and the protection of application secrets, certificates, encryption keys, and secrets backed by using a Hardware Security Modul... |
| E227 | **b** | Microsoft Azure provides a high-availability option for hosting applications across the entire Azure region. The availability zone protects applications and data within a region from data center-level failure. To ensure the 99.99% availability of the application, an application should be made available in multiple zones. If one zone goes down fo... |
| E228 | **a** | Azure Storage Account is a storage service that stores and manages data in Azure. Azure Storage Account stores application data and objects that can be accessed by the user over the internet using HTTP commands. There are four types of storage services available in Azure that store different types of data objects. |
| E229 | **a** | Azure Hybrid Benefit is a discount program that allows Azure users to get cost benefits when running the Azure virtual machines. This program provides up to 40% discount on the running cost and a discount on Azure Database service. |
| E230 | **b** | Blob storage contains the data in the form of blobs. These blobs are stored in a container within a storage account. The blob stores objects like images, audio, video, and files. Blob storage has different pricing tiers depending on the type of data usage. |
| E231 | **a** | Azure Activity Logs is a great tool to tell who, what and when the operation has been done on Azure resources. A range of data is present in Azure Activity Logs, from Azure Resource Manager operations logs to updates in Azure service health events. This service shows the number of actions that is happened in the last 24 hours. The following figu... |
| E232 | **a** | Organizations can deploy different Azure services for their requirement. Multiple Azure services are available within the same availability zones. The availability zone protects applications and data within a region from data center-level failure. The advantage of multiple availability zones is that the application will not be affected by downti... |
| E233 | **a** | Azure Application Gateway is a layer 7-based load balancer that manages web applications using HTTPS requests. It is more efficient in delivering web application services than other gateways. It works on HTTPS rather than IP address/port. All the remaining options are invalid as no one service is responsible for routing web traffic. |
| E234 | **a** | Azure Database Migration Service is a PaaS service offered by Microsoft. This service allows database migration not only from on-premises to Azure but also between the Azure databases. Free and premium tiers are available for database migration. Organizations can migrate databases online or offline depending on the requirement. |
| E235 | **a** | Azure Virtual Machine Scale Sets is an Azure compute resource that deploys the set of Virtual Machines for the high availability of applications during its peak time. It automatically scales up the group of VMs according to the demands and scales down when needed. |
| E236 | **c** | Azure Marketplace is an online store with thousands of VMs, developer services, and applications. Cloud-based solutions can easily sell to others using Azure Marketplace. It also enables to development of the applications by seeking help and using tools available in Azure Marketplace. It is clear from the explanation that all the remaining optio... |
| E237 | **a** | If an organization wants to transfer considerable amounts of data from Azure to an on-premises network, they need to pay extra charges defined by Microsoft Azure pricing. According to pricing details, Azure allows inbound data transfer free of cost. For the outbound transfer of data, the cost is required. Azure allows only the first 5GB of data ... |

**E238.** A new Azure user logs in to the Azure portal and deploys the following Azure resources: Azure Kubernetes Azure Storage Account The creation of Azure Storage Account belongs to which one of the following deployment models?
- a) Platform as a Service
- b) Software as a Service
- c) Hardware as a Service
- d) Infrastructure as a Service

**E239.** Alexander is an Account Administrator in an organization. The organization is using Azure resources and has a pay-as-you-go subscription. Alexander designs rules and regulations for the organization. One of the rules is that the Azure virtual machine must be deployed on a separate network portion. Which of the following is used to fulfill this rule?
- a) A separate account for the server
- b) A separate resource group
- c) A separate network interface for the server
- d) A separate virtual network

**E240.** An organization is running critical applications with sensitive data. A security engineer wants to monitor anything impacting the application performance and create troubleshooting alerts. Which of the following services is used for monitoring the app availability?
- a) Microsoft Entra ID
- b) Azure Advisor
- c) Microsoft Defender for Cloud
- d) Azure Monitor

**E241.** Jacobs is a Software Engineer in an IT Company. He implemented a web application that is running on two Azure Virtual Machines. Users can access this application via the internet. For a large number of users, he decides to add a load balancer to ensure the availability of the application. Is his decision correct?
- a) Yes
- b) No

**E242.** An organization decides to start using Azure. To try the Azure service and resources, an organization created an Azure Free Account. Which statements are true regarding the use of Azure Free Account? Choose two options from the given:
- a) You get USD 200 worth of credit that you can spend during the first 30 days of sign-up
- b) You only need to have a valid mobile number to sign up for the account
- c) You get free access to all services for 12 months.
- d) After the 30 days of USD 200 worth of credit, you need to convert to a Pay-As-You-Go Account for continuous usage.

**E243.** Mark is a Software Architect in an organization. He configures a hybrid cloud infrastructure, as shown in the given figure. The organization is using Azure resources for its Azure subscription. Mark wants to transfer big data (gigabytes) from an on-premises network to an Azure cloud using a VPN gateway. Would the organization need to pay extra charges for this transfer of data?
- a) Yes
- b) No

**E244.** A newly established company created the following resources using a pay-as-you-go Azure subscription. Azure Kubernetes Azure Storage Account The Azure Kubernetes service belongs to which of the following deployment models?
- a) Hardware as a Service
- b) Infrastructure as a Service
- c) Platform as a Service
- d) Software as a Service

**E245.** An organization is going to plan a project using Azure tools. The project must fulfill the following requirement: “Ability to instantly redirect the user request even if the network component fails”. Which of the following features is best suited for the defined statement?
- a) Low Latency
- b) Dynamic Scalability
- c) Disaster Recovery
- d) High Availability

**E246.** A company is using Azure resources. One of its customers deployed an Azure Virtual Machine named “ips-vm”. After the process of configuration details, which of the following options declares the confirmation of deployment?
- a) Using Link 4
- b) Using Link 3
- c) Using Link 2
- d) Using Link 1

**E247.** A company has deployed two Azure Virtual Machines on which a web application runs. The users can access this application from the internet. Could a VPN gateway be used to ensure an application's high availability?
- a) Yes
- b) No

**E248.** A company has a pay-as-you-go subscription and has built different resources in its Azure account. They want to be informed about the charges, cost reduction in Azure resources, and optimization of resources. How can the company achieve such a system that provides visibility of cost incurred to Azure resources?
- a) Create an alert in Azure Advisor
- b) Create an alert in Azure Monitor
- c) Create a cost tag for the resource group
- d) Create a budget in Azure Cost Management

**E249.** An IT Company has started using Azure services for their Azure subscription, creating different resource groups. Various resources have been created for several company departments within each resource group. Would the company need to give additional charges for creating multiple resource groups in Azure?
- a) Yes
- b) No

**E250.** An organization has an Azure subscription. Several users and customers are associated with this organization and use Azure resources. Is it possible to manage the organization’s guest list from Business to Customer “B2C” feature of Azure AD service?
- a) Yes
- b) No

**E251.** A company plans to adopt a feature that ensures network availability even in sudden damage. Which of the following features is best suited for the given statement? “Ensure to protect the network prevent from disastrous damage.”
- a) Fault Tolerance
- b) Low Latency
- c) Disaster Recovery
- d) Dynamic Scalability

**E252.** Alex is working as an IT Engineer for an organization. With his team, he decides to implement the package for the implementation of Azure service. For the implementation, he needs a plan; one of his team members suggested using Azure AD Privileged Identity Management. Is this suggestion helpful?
- a) Yes
- b) No

**E253.** Jack is an App developer for an organization. He deployed an Azure Web Application. The application is deployed with Azure Web App Service and Azure SQL Database service. The defined SLA for Azure Web App service is 99.95%, and the Azure SQL Database is 99.99%. What is the composite SLA for this application?
- a) 99.95% x 99.99% = 99.94%
- b) 99.95%
- c) (99.94% + 99.99%)/2 = 99.97%
- d) 99.99%

**E254.** A resource group, “Ips”, is created by Azure users. The resource group has the following Azure resources. The resource group “Ips” is locked with the type “Delete”. Would an Azure user be able to delete any resource present within the “Ips”?
- a) Yes
- b) No

**E255.** An organization decides to explore Azure service using Azure Free Account. Does Azure Free Account allow using Azure resources and services for a specific time?
- a) Yes
- b) No

**E256.** An organization starts using Azure resources. They have an on-premises network. Would Azure help extend the on-premises infrastructure using the hybrid approach?
- a) Yes
- b) No

**E257.** Thomas is studying some cloud services that make any network more reliable and flexible and provide throughput with acceptable low latency. Which of the following is best suited to the given statement? “Able to perform as per SLA (Service Level Agreement), either the network traffic load increases or decreases”.
- a) Disaster Recovery
- b) Dynamic Scalability
- c) Fault Tolerance
- d) Low Latency

**E258.** An organization calls up a meeting to discuss how to publicly announce the rules and regulations for creating a set of requirements that are used for the implementation of Azure service, such as Azure Resource Manager (ARM) template, role-based access control, policy, etc. One of the employees suggested using the Azure blueprint for this purpose. Is this suggestion helpful?
- a) Yes
- b) No

**E259.** Charlie is a Software Engineer in an organization. The organization creates an Azure application by keeping the importance of business metrics. Azure application is implemented using Azure App Service with 99.95% SLA and Azure SQL Database with 99.99% SLA. Which of the following is correct in ensuring customer feedback regarding the SLA? Choose two options to form the following:
- a) Mean time to failure (MTTF)
- b) Mean time to recover (MTTR)
- c) Mean time to success (MTTS)
- d) Mean time between failures (MTBF)

**E260.** A company is planning to deploy a set of Azure Virtual Machines. They want the cost estimate for deploying these Machines. Which of the following factors affect the compute cost of Virtual Machines? Choose two answers from the options given below:
- a) The data center where the Virtual Machine is located
- b) The Resource Group where the Virtual Machine is located
- c) The size (instance specification) of the Virtual Machine
- d) The region the Virtual Machine is located in

**E261.** A company has a set of Virtual Machines defined in Azure. They want to explore options on how costs can be cut down for the running cost of the Virtual Machines. Which of the following is an option that can be considered for cutting down the costs without affecting the services running on the Virtual Machine?
- a) Look at buying Reserved Instances
- b) Change the Resource Group of the Virtual Machine
- c) Stop the Virtual Machines
- d) Deallocate the public IP address from the Virtual Machine

**E262.** A company is looking to expand its current on-premises infrastructure by setting up Azure Virtual Machines and Storage Accounts. Which expenses decrease when a company considers using services such as the Virtual Machine and Storage Account?
- a) Operating Expense
- b) Petty Expenses
- c) Capital Expense
- d) Secondary Expenses

### Answers — Section E (Batch 10)

| # | Answer | Explanation |
|---|---|---|
| E238 | **d** | The company's resources and services come in the computing infrastructure and architecture category, which is customarily called Infrastructure as a Service (IaaS) in cloud computing. Azure Storage Account is an IaaS service. A first storage account must be created to use the storage services. The storage account is used to store and manage data... |
| E239 | **d** | A separate virtual network must be implemented to deploy a remote machine. An organization has its own Azure network with different Azure resources. Organizations deploy resources in the network that follow the defined rules and regulations and fulfill the requirements. All the remaining options are invalid as no one provides the deployment of t... |
| E240 | **d** | Azure Monitor is a service that provides a single source for monitoring Azure resources. With Azure Monitor, visualization, and route, the query is possible. We can easily take action on the metrics and logs coming from the resource in Azure. |
| E241 | **a** | Azure load balancer serves the load-balancing feature to the connected virtual machines within Microsoft Azure. It is responsible for managing the network traffic load and enables the use of all VMs for processing. It distributes the traffic load to the Virtual Machine present in the network. The Azure load balancer also delivers high availabili... |
| E242 | **a and d** | Azure Free Account offers $200 credit for the first 30 days to new Azure users. In the last 12 months of the most popular Azure services like Virtual Machines (VM), Databases, Storage accounts, etc., users can always access 25 Azure services for free. It is an excellent option for new Azure users to explore Azure services. Option B is invalid be... |
| E243 | **b** | According to the Azure pricing, no charge is required for inbound data transfer. Within the hybrid cloud infrastructure, a large amount of data can be easily transferred from on-premises to Azure cloud free of cost. |
| E244 | **⚠️ b** | ⚠️ **Correction**: The original answer classifies AKS as IaaS, but this is incorrect. AKS is **PaaS** — Azure manages the Kubernetes control plane; you deploy and manage containers. This is consistent with N80 in this file which correctly identifies AKS as PaaS. The original IPSpecialist source is wrong here. It also makes sure that the container is configured correctly and working together. ... |
| E245 | **d** | High Availability is the feature that makes the application available to end-users. This means one application should be implemented in more than one server. If any of the servers go down for some reason, the backup server with the same application immediately starts working. Therefore, the application remains available 24/7 hours. Option A is i... |
| E246 | **b** | The notification tab shows all the deployment and deletion of actions to Azure resources available in the portal. In the given situation, when the deployment of ips-vm is done, the notification tab shows the notice “Deployment succeeded is shown”. It is clear from the explanation that all the remaining options are invalid as no one provides the ... |
| E247 | **b** | A VPN gateway helps establish a private connection between Azure resources and an on-premises environment, offices, the cloud, or other premises within the cloud to establish a private, secure connection. |
| E248 | **d** | Azure Cost Management is an Azure service designed to allow the user to gain complete control and visibility of cost spending across Azure resources. This tool also provides cost analysis, cost alerts, Advisor recommendations, and Cloudyn services. The advantage of the budget is to inform the company about the cost spent on Azure resources. Budg... |
| E249 | **b** | Azure Resource Group provide a managed group of Azure resources like Virtual Machine, SQL Database, storage account, etc. Resource groups allow an easy add and removal of resources and apply role-based access information. Within a resource group, the same type of resources is created depending upon the company’s requirements. There is no extra c... |
| E250 | **b** | Business-to-Customer “B2C” is a customer identity and access management solution. “B2C” is an authentication method that enables businesses and other organizations to provide their customers and consumers access to public-facing web and mobile applications. Business to Business “B2B” feature provides services to external partners and guest users... |
| E251 | **c** | Disaster Recovery is a mandatory plan adopted by each IT organization to protect its IT majors. It keeps the running applications available during recovery time and does not harm any other service, whether running on-premises or Azure. Option A is invalid because Fault tolerance refers to the ability to provide guaranteed services during downtim... |
| E252 | **b** | Azure AD Privileged Identity Management is a part of the directory service. It is responsible for managing and monitoring essential resources for a limited period. Azure AD Privileged Identity Management service enables us not to give permanent access to Azure resources. Instead, we can make a user eligible for privileged access. |
| E253 | **a** | When an application is run with different services. Different types of SLAs are defined for each service. This does not mean that the entire application goes down if one of the services fails. The new SLA is involved in an application with a different SLA-based service to ensure high availability. This SLA is called composite SLA. The composite ... |
| E254 | **b** | Azure Lock is the resource that protects the Resource group from any unwanted incident. Azure has two types of locks. ReadOnly lock, which allows authorized users to read the resources only. They are unable to make changes to the resources. The second type of lock is Delete, to ensure that the user is not allowed to delete the resource. In the g... |
| E255 | **a** | According to the Microsoft documentation, Azure offers a free trial using Azure Free Account. It offers a $200 credit for the first 30 days to new Azure customers. To explore the Azure service, customers need more time to use these services, which is a reason Microsoft created an Azure free account. With this account, Azure customers use service... |
| E256 | **a** | An organization can integrate on-premises networking, identity compute, and data resources with Azure. The hybrid approach brings an advantage when an organization uniquely hosts infrastructure and service in the on-premises network. Azure integration with on-premises comprises those features that can be scaled out and provision the hybrid cloud... |
| E257 | **b** | Scalability is the ability that manages the traffic load and makes the provision of service without affecting network performance. This feature automatically allocates resources to meet the performance requirement defined in the Service Level Agreement (SLA). Option A is invalid because Disaster Recovery is a mandatory plan adopted by each IT or... |
| E258 | **a** | Azure Blueprint enables us to design and package the entire Azure environment, including preferred policy, ARM template, and role-based access assignment. These blueprints are assigned to many subscriptions, which can help us to scale up the use of Azure. |
| E259 | **b and d** | To meet the business requirements, the two metrics that ensure the customer SLA are Mean time to recover (MTTR) and Mean time between failures (MTBF). All the remaining options are invalid. |
| E260 | **c and d** | If you look at the pricing calculator for an Azure Virtual Machine, you see the different parameters that make up the cost of the Virtual Machine. There as aspects such as the region, the operating system, the type, the tier, and instance size. |
| E261 | **a** | The Company can consider buying Reserved Instances to get discounts on the virtual machines’ running costs The Microsoft documentation mentions the following. You can save money when you commit to an Azure-reserved VM instance. The reservation discount is applied automatically to the number of Virtual Machines matching the reservation scope and ... |
| E262 | **c** | By using Azure resources such as Virtual Machines and Storage accounts, you can completely dismiss the need to buy any physical infrastructure. This helps you not have any capital expenses when moving to the cloud. The Microsoft documentation mentions the following. Cloud computing can reduce capital expenses for hardware and software, setting u... |

**E263.** A company has a set of resources in Azure. They want to get reports of “Costs incurred by resource”. Where should they go to get this information?
- a) Azure Monitor
- b) Azure Virtual Machines
- c) Azure Cost Management
- d) Azure Advisor

**E264.** A company wants to start moving its resources to Azure. They have an on-premises data center and want to migrate their workloads to Azure. They need to estimate the costs and provide a business case for moving the workloads to Azure. Which of the following can they use to help justify the costs?
- a) Azure TCO calculator
- b) Azure cost management
- c) Azure pricing calculator
- d) Azure Advisor

**E265.** A company is planning to deploy an application onto Azure. They have set up an Azure subscription and an Azure tenant and want to implement disaster recovery for the application. Which of the following aspects of Azure could be used for disaster recovery purposes?
- a) Azure Regions
- b) Azure Data centers
- c) Azure subscriptions
- d) Azure resource groups

**E266.** A company plans to deploy an application on Azure Virtual Machines. They have set up an Azure subscription and an Azure AD tenant. Would adding an Azure Load Balancer to the application architecture increase the overall availability of the application?
- a) Yes
- b) No

**E267.** A company wants to deploy a web application and a database backend to Azure. They need to decide on the services that can be used to host the different parts of the application. Which of the following can be used to host the web application?
- a) Azure Functions
- b) Azure Logic Apps
- c) Azure Load Balancer
- d) Azure App Service

**E268.** A company is planning to deploy a set of applications to Azure. They are trying to design the application architectures when migrated to Azure. Which of the following reference sites can they refer to when designing architectures on Azure?
- a) Azure Portal
- b) Microsoft support
- c) Azure Architectures site
- d) Azure support

**E269.** A company is planning to deploy a set of repeatable resources to Azure. They want to deploy the resources in the most efficient way possible. Which of the following could they use for this requirement?
- a) Resource groups
- b) Resource providers
- c) Management groups
- d) Resource Manager templates

**E270.** A company wants to deploy small pieces of code onto Azure. They want to cut the costs of hosting the code. Which of the following could they consider for hosting the code?
- a) Azure Virtual Machines
- b) Azure Functions
- c) Azure Batch service
- d) Azure Logic Apps

**E271.** You want to deploy a virtual machine scale set to Azure. Could you deploy the scale set using the Azure command-line interface?
- a) Yes
- b) No

**E272.** A company is planning to set up a Microservices-based application on Azure. They want to use a service that could be used to orchestrate the deployment of container-based applications. Which of the following could be used for this purpose?
- a) Azure Functions
- b) Azure Logic Apps
- c) Azure Kubernetes
- d) Azure SQL Database

**E273.** A company has just set up an Azure subscription and an Azure tenant. The company is exploring the different compute options available in Azure. Which of the following is NOT a compute option available in Azure?
- a) Azure SQL database
- b) Azure Functions
- c) Azure Container Instances
- d) Azure App Service

**E274.** Which of the following services allows for events generated from Azure resources to be sent to applications?
- a) Azure Event Hubs
- b) Azure Notification Hubs
- c) Azure Logic Apps
- d) Azure Event Grid

**E275.** A company wants to store data in a place used to store video files. Users will upload these video files. Which of the following would you use for this purpose?
- a) Data Box Edge
- b) Storage Account
- c) Azure Data Box
- d) Backup and Site Recovery

**E276.** A company plans to set an Azure Synapse Analytics (formerly SQL Data Warehouse). Is it possible to visualize the data in the warehouse with Power BI?
- a) Yes
- b) No

**E277.** A company plans to set up a series of Azure SQL Databases. Which feature can they use to reduce the overall cost if the databases have unpredictable usage demands?
- a) Elastic Pools
- b) Azure Reservation
- c) Clustered databases
- d) Single databases

**E278.** Suppose you want to create a Virtual Machine in Azure. You need to allocate around 30 GB of storage for the Virtual Machine. Which of the following disks would you use for this purpose?
- a) The OS disk
- b) The temporary disk
- c) The local disk
- d) A new data disk

**E279.** A company is planning to create a Cosmos DB account. Which of the following is used as a measurement of cost for the Cosmos DB account? Select two options from the list.
- a) The number of clusters
- b) The storage
- c) The throughput
- d) The number of nodes

**E280.** A company has created a virtual network and launched a Virtual Machine set in the Virtual Network. They want to change how traffic is routed in the Virtual Network. Which of the following could be used to fulfill this requirement?
- a) Application Security Groups
- b) Network Security Groups
- c) User-Defined Routes
- d) Azure DDoS Protection

**E281.** A company currently has an Azure subscription and an Azure tenant. They want to implement Azure Multifactor authentication. Is it possible to add an SMS as a second means of authentication for a user?
- a) Yes
- b) No

**E282.** A company is planning on using Microsoft Defender for Cloud. They already have a set of resources defined on the Azure platform. Is the company limited to using Microsoft Defender for Cloud to secure its Virtual Machines ONLY in Azure Cloud?
- a) Yes
- b) No

**E283.** A company wants to have a service that could fulfil the below requirement. “Provide the ability to generate keys in hardware security modules that never leave the hardware security module boundary.” Which of the following services could be used for this requirement?
- a) Microsoft Defender for Cloud
- b) Azure Key Vault
- c) Azure Network Security Groups
- d) Azure Advisor

**E284.** A company is planning to create several policies in the Azure Policy service. These policies are all meant to achieve a particular goal. Which of the following could be used to organize these policies into one group?
- a) Subscriptions
- b) Resource Groups
- c) Management Groups
- d) Initiative Definition

**E285.** A company has deployed a virtual machine in Azure to enable communication with other resources. A Network Security Group is created. While creating the Network Security Group, the following text is entered into the Tags Text box: Tag:Name: CrossSiteScript Value: <script>Alert(‘CrossSiteScript’)</script> What happens while deploying the NSG?
- a) Deploys successfully
- b) Throws error during deployment
- c) Input Validation has to be enabled on the controls to avoid error
- d) Input Validation has to be disabled on the controls to avoid error

**E286.** A company has deployed a Virtual Machine in Azure, and to filter the network traffic, an Application Security Group is created through CLI using a template. Which of the following is a valid Application Security Group template? A. A. B. C.

**E287.** A company has a Virtual Network and wants to implement the following requirements: To create 2 subnets and 2 VM’s in each subnet To create a user-defined route to enable the 2 subnet resources to communicate Can a user-defined route be created without creating a Subnet?
- a) UDR cannot be created without creating Subnet
- b) At least one UDR is required to create a Subnet
- c) UDR can be created without creating Subnet
- d) There is no relation between Route and Subnet

### Answers — Section E (Batch 11)

| # | Answer | Explanation |
|---|---|---|
| E263 | **c** | If you go to Cost Management, you will get a Cost breakdown by resource. Since this is clear from the implementation, all other options are incorrect. |
| E264 | **a** | You can use the Total Cost of Ownership calculator to see the cost savings you can achieve by moving workloads to Azure. A snapshot of the TCO Calculator is shown below. The other options are invalid because they help cost management after moving to Azure. |
| E265 | **a** | You can deploy your resources across multiple regions. If a disaster and one region go down, you will still have another available. The Microsoft documentation mentions the following. Disaster recovery also refers to minimizing IT services disruption and recovery, but across various data centers that might be hundreds of miles away from one anot... |
| E266 | **a** | With the Azure Load Balancer, you can increase the overall availability of your applications. The Microsoft documentation mentions the following. With Azure Load Balancer, you can scale your applications and create highly available services. Load Balancer supports both inbound and outbound scenarios. A load balancer provides low latency and high... |
| E267 | **d** | When deciding on the support for which service to use for web applications, consider using the Azure App Service. The Microsoft documentation mentions the following. Azure App Service is an HTTP-based service for hosting web applications, REST APIs, and mobile backends. You can develop in your favorite language, be it .NET, .NET Core, Java, Ruby... |
| E268 | **c** | The Azure Architectures site has a whole list of reference architectures. Since this is clear from the documentation, all other options are incorrect. |
| E269 | **d** | If you want to deploy a repeatable set of resources, consider using the Azure Resource Manager template. The Microsoft documentation mentions the following. Resource Manager Template - A JavaScript Object Notation (JSON) file that defines one or more resources to deploy to a resource group, subscription, management group, or tenant. The template... |
| E270 | **b** | You can use Azure functions to save costs if you want to run small pieces of code. The Microsoft documentation mentions the following. Azure Functions is a serverless solution that allows you to write less code, maintain less infrastructure, and save on costs. Instead of worrying about deploying and maintaining servers, the cloud infrastructure ... |
| E271 | **a** | The Microsoft documentation also has a quick start section on achieving this. A virtual machine scale set allows you to deploy and manage a set of auto-scaling virtual machines. You can manually scale the number of VMs in the scale set or define rules to autoscale based on resource usages like CPU, memory demand, or network traffic. An Azure loa... |
| E272 | **c** | You can use Azure Kubernetes to deploy and maintain Microservices-based applications. The Microsoft documentation mentions the following. Kubernetes is a rapidly evolving platform that manages container-based applications and their associated networking and storage components. Kubernetes focuses on the application workloads, not the underlying i... |
| E273 | **a** | Below is the list of compute options available in Azure as given in the Microsoft documentation. Azure SQL database is not part of the list. If you are unfamiliar with the Azure service selected in the previous step, read the overview documentation to understand the basics of the service. App Service: A managed service for hosting web apps, mobi... |
| E274 | **d** | This can be accomplished with the help of the Azure Event Grid service. The Microsoft documentation mentions the following. Azure Event Grid allows you to build applications with eventbased architectures easily. First, select the Azure resource you would like to subscribe to, and then give the event handler or WebHook endpoint to send the event ... |
| E275 | **b** | You can use the Blob service in Azure storage accounts to store video files. The Microsoft documentation mentions the following. Azure Blob storage is Microsoft's object storage solution for the cloud. Blob storage is optimized for storing massive amounts of unstructured data. Unstructured data is data that does not adhere to a particular data m... |
| E276 | **a** | Yes, this is possible. The Microsoft documentation also has an article on this. Azure Synapse Analytics (formerly SQL Data Warehouse) with DirectQuery allows you to create dynamic reports based on data and metrics you already have in Azure Synapse Analytics. DirectQuery sends queries back to your Azure Synapse Analytics in real-time as you explo... |
| E277 | **a** | You can use Elastic pools to efficiently use the costs when having databases with unpredictable usage demands. The Microsoft documentation mentions the following. Azure SQL Database elastic pools are a simple, cost-effective solution for managing and scaling multiple databases with varying and unpredictable usage demands. The databases in an ela... |
| E278 | **d** | You would use or create a new data disk. These disks have a maximum capacity of around 32 TIB. The Microsoft documentation mentions the following. A data disk is a managed disk attached to a virtual machine to store application or other data you need to keep. Data disks are registered as SCSI drives and labeled with your chosen letter. Each data... |
| E279 | **b and c** | You are charged based on the amount of throughput you assign for the Cosmos DB account and the Storage. |
| E280 | **c** | You can create your network routes using User Defined Routes. The Microsoft documentation mentions the following. You can create custom or user-defined (static) routes in Azure to override Azure's default system routes or add additional routes to a subnet's route table. In Azure, you create a route table and then associate the route table with z... |
| E281 | **a** | Azure provides the following authentication methods for both Multi-Factor authentication and selfservice password reset. In this, SMS is an authentication method available. For more information on authentication methods, please visit the below URL- |
| E282 | **b** | Microsoft Defender for Cloud supports VMs and other components like Azure SQL and Storage services, etc. The Microsoft documentation mentions the following. Microsoft Defender for Cloud supports virtual machines and servers in different types of hybrid environments: Only Azure Azure and on-premises Azure and other clouds Azure, other clouds, and... |
| E283 | **b** | You can achieve this requirement with the help of the Azure Key Vault service. The Microsoft documentation mentions the following. Azure Key Vaults may be either software-protected or, with the Azure Key Vault Premium tier, hardware-protected by hardware security modules (HSMs). Software-protected keys, secrets, and certificates are safeguarded ... |
| E284 | **d** | You can club the policy definitions into one Initiative Definition. The Microsoft documentation mentions the following. An initiative definition is a collection of policy definitions tailored to achieve a singular overarching goal. Initiative definitions simplify managing and assigning policy definitions. They simplify by grouping a set of polic... |
| E285 | **a** | The input validation is taken care of in Azure. The script entered in Tags Text Control does not throw any error and would be treated as raw text. Please see the screenshot showing the validation result while creating the Network Security Group. |
| E286 | **b** | Option A is incorrect because the template is in json format and has an invalid @ character. Option B is CORRECT as it has a valid json. Option C is incorrect because the template is in json format and has an invalid # character. Option D is incorrect because the template is in json format and has an invalid $ character. |
| E287 | **c** | UDR can be created before the creation of the Subnet. But it would be effective only once the route is associated with Subnet. |

**E288.** A company has a Virtual Network with 2 subnets; Subnet1 and Subnet2. A Virtual Machine with a Web Server is created in Subnet1, while another Virtual Machine with a Database Server is created in Subnet2. A Firewall is created in the Virtual Network. The company’s Firewall policy is set to get alerts for the Threat Intelligence mode. Does the Threat Intelligence mode of the newly created Firewall override the parent Policy?
- a) Parent policy is overridden with stricter setting
- b) Parent policy can be overridden
- c) Parent policy cannot be overridden
- d) Parent policy is overridden, and threat intelligence can be turned off

**E289.** A company is planning to implement an Azure DDoS protection plan. The company has multiple subscriptions The total number of resources across subscriptions is 75 Does the DDoS Protection Standard Plan meet the above requirements?
- a) DDoS Protection Standard Plan does not meet the first requirement
- b) DDoS Protection Standard Plan does not meet the second requirement
- c) DDoS Protection Standard Plan meets both requirements
- d) Multiple DDoS Protection Standard Plans are required, one for each requirement

**E290.** A company wants to know how well security practices are implemented in Azure. Which security feature would help identify the current Identity practices and advise improvements?
- a) Azure Information Protection
- b) Azure AD Identity Secure Score
- c) Azure AD Identity Protection
- d) Microsoft Defender for Cloud

**E291.** A company wants to implement Azure AD Identity Protection. The following are the essential requirements: Prompt users if the credentials are compromised Identify suspicious login attempts Which of the following policies implements the above requirements? Choose two answers.
- a) Azure policy
- b) User risk policy
- c) Sign-in risk policy
- d) MFA registration policy

**E292.** A company wants to move all its employees to Microsoft Entra ID. What is the initial domain where the tenant is created?
- a) portal.azure.com
- b) onmicrosoft.com
- c) azurewebsites.com
- d) microsoft.com

**E293.** A company wants to implement Azure Multi-Factor Authentication. Which of the following is the recommended policy?
- a) Enable per-user
- b) Enable per-session
- c) Enable Security Defaults
- d) Enable Conditional Access

**E294.** A company wants to create an IP Group to configure with an Azure Firewall. The company has 3 branches, each in a different region. Which of the following is the right option to create an IP Group?
- a) IP Group can be created in any region
- b) IP Group has to be created for each subscription
- c) IP Group has to be created for each branch
- d) IP Group has to be created in each region

**E295.** Your Company has multiple subscriptions and wants to implement a custom Dashboard that displays the Secure Score for each subscription. Which of the following is a valid option?
- a) Can be implemented for only a single subscription
- b) Can be implemented using Secure Score REST API
- c) Not possible to implement Secure Score onto a custom Dashboard
- d) Not possible, Secure score is only accessible through the Azure Portal

**E296.** A company wants to create an automated workflow to send notifications for specific Threats. While creating the workflow, is it mandatory to use a Logic App?
- a) Yes, it is mandatory to use a Logic App while creating an automation workflow
- b) No, to create an automation workflow, a Logic App is not mandatory
- c) No, there is no relation between Automation Workflow and Logic App
- d) No, the Logic App has to be created after creating Automation Workflow

**E297.** A company has multiple subscriptions and many resources assigned to each; the administrator wants to know the count of Key Vaults across all the subscriptions; what is the quick way of getting the result?
- a) Open the Key Vault and Count manually
- b) Use the Manage view option of Key Vault
- c) Open the Key Vault and Apply Filters
- d) Use Azure Resource Graph Explorer Query feature

**E298.** A company has implemented Azure Information Protection, but a newly joined user is unable to access Azure Information Protection. Which two roles would enable Azure Information Protection access to the user?
- a) Cloud Application Administrator
- b) Information Protection Administrator
- c) Group Administrator
- d) Security Administrator

**E299.** Your company wants to implement a security solution for users who are on the on-premises Active directory and has the following requirement: Monitor User login/logout Monitor Active Directory User account changes Monitor Machine Account Which is the best option to requirements?
- a) Azure AD Password Protection implement the above
- b) Microsoft Defender for Identity (formerly Azure Advanced Threat Protection, also known as Azure ATP)
- c) Azure AD Identity Protection
- d) Azure AD Privileged Identity Management

**E300.** A company wants to implement an Azure policy to monitor Virtual Machines whose disk encryption is not enabled. How can a policy assignment be created? Please select three options.
- a) Azure Monitor
- b) Azure Portal, ARM Template
- c) Python, REST
- d) Azure CLI, Azure PowerShell

**E301.** A company with a healthcare application has added a newly joined user to the Application Developer role. When does the user role take effect?
- a) For the role to be effective, it might take up to 15 minutes
- b) The role will be effective immediately
- c) For the role to be effective, it might take up to 1 hour
- d) For the role to be effective, it might take up to 2 hours

**E302.** A company hosts a load-balanced web application (2 Web Servers and 2 App Servers). The application uses Azure SQL Database. To avoid accidental deletion of the Database, a ReadOnly lock is applied to the Database. An application user wants to update a transaction through the Web application. Which of the following is a valid action?
- a) An update transaction is not allowed since the ReadOnly lock is applied on the Database
- b) Only Select statements are valid. Update/Delete actions are invalid
- c) An update transaction is a valid action
- d) Only Select/Delete statements are valid. The Update action is invalid

**E303.** A company wants to integrate its ITSM tool Service Now with Azure and automatically create incidents for the Azure Advisor recommendations; what is the best way to achieve this in Azure?
- a) Integrate with ITSM tool using ITSM Connector
- b) Integrate with ITSM tool using Azure Function
- c) Integrate with ITSM tool using Logic App
- d) Cannot integrate Azure Advisor with ITSM Tool

**E304.** A company plans to deploy multiple resources using Azure Blueprints. While creating the BluePrint by the administrator, what are the Lock Assignment options available while assigning a Blueprint?
- a) Not Locked; Cannot Edit/Delete; Read Only; Cannot Delete
- b) Delete; ReadOnly
- c) Do not Lock; Do Not Delete; Read Only
- d) Update; ReadOnly

**E305.** A company wants to purchase an Azure support plan. Which of the following is the most cost-effective plan that has the following embedded into the plan? Access to the full set of Azure Advisor Recommendations. Business hours access to support engineers via email.
- a) Basic
- b) Developer
- c) Standard
- d) Professional Direct
- e) Premier

**E306.** You have set up an Azure Free Account. Will you have access to the Knowledge Center?
- a) Yes
- b) No

**E307.** You are reviewing the Service Level Agreement for various services on the Azure platform. How does Azure calculate the availability of all services?
- a) In a yearly billing cycle
- b) In a monthly billing cycle
- c) In a weekly billing cycle
- d) In a daily billing cycle

**E308.** Which of the following URLs can be used to create an Azure support request?
- a) https://portal.azure.com
- b) https://support.azure.com
- c) https://support.microsoft.com
- d) https://dev.azure.com

**E309.** Which users get access to raise an Azure support request by default? Choose 3 answers from the options given below.
- a) Account Administrator
- b) Service Administrator
- c) Co-Administrator
- d) Billing Administrator

**E310.** You want to build an application that would have some basic level of artificial intelligent modules. You do not have the required Artificial Intelligence skills. Which of the following can you still use to build these applications?
- a) Azure Machine Learning Studio
- b) Azure HD Insights
- c) Azure AI Services
- d) Azure Functions

**E311.** A company has just set up an Azure account. The developers want to use a service that will easily allow them to do the following: Create Virtual Machines from pre-created custom images with all the software and tools installed. Set auto-shutdown and auto-start schedules on Virtual Machines. Which of the following service could they use for these requirements?
- a) Azure DevOps
- b) Azure DevTest Labs
- c) Azure Functions
- d) Azure Logic Apps

**E312.** You are planning to use the IoT Hub service in Azure. Does this service allow for communication from a device to the cloud and from the cloud to the device?
- a) Yes
- b) No

### Answers — Section E (Batch 12)

| # | Answer | Explanation |
|---|---|---|
| E288 | **a** | The newly created Firewall policy can be overridden with the stricter setting. |
| E289 | **c** | By default, DDoS Protection Standard Plan meets both requirements. |
| E290 | **b** | Azure AD Identity Secure Score helps identify the identity secure score to provide recommendations. The identity secure score is a percentage that indicates how aligned you are with Microsoft's best practice recommendations for security. Each improvement action in the identity secure score is tailored to your specific configuration. |
| E291 | **b and c** | Option A is incorrect as it is a Service to create policies in Azure Option B is CORRECT; it is used if the credentials are compromised Option C is CORRECT; it is considered for any suspicious sign-ins like multiple incorrect login attempts Option D is incorrect; it ensures that the user registers for MFA |
| E292 | **b** | Option A is incorrect as portal.azure.com is used for login into the Azure portal. Option B is correct as is used for the initial domain name should be onmicrosoft.com, and even the diagram included in the explanation indicates the initial domain is onmicrosoft.com. Option C is incorrect, as azurewebsites.com is used to host the web application ... |
| E293 | **d** | To secure user sign-in events in Azure AD, you can require Multi-Factor Authentication (MFA). Enabling Azure AD Multi-Factor Authentication using Conditional Access policies is the recommended approach to protect users. Conditional Access is an Azure AD Premium P1 or P2 feature that lets you apply rules to require MFA as needed in specific scena... |
| E294 | **a** | IP Groups allow you to group and manage IP addresses for Azure Firewall rules in the following ways: As a source address in DNAT rules As a source or destination address in network rules As a source address in application rules An IP Group can have a single IP address, multiple IP addresses, or one or more IP address ranges. IP Groups can be reu... |
| E295 | **b** | Option A is incorrect because, using REST API, Secure Score can be retrieved for multiple subscriptions Option B is CORRECT; please see the reference URL accessing your secure score section Option C is incorrect because a secure score can be accessed using the REST API Option D is incorrect because the secure score can be accessed through the RE... |
| E296 | **a** | Option A is CORRECT, as the Logic App has to be selected while creating an Automation Workflow. Please view the diagram below. Option B is incorrect because an existing Logic App has to be selected while creating the Automation Workflow. Option C is incorrect because a Logic App is required during automation workflow creation. Option D is incorr... |
| E297 | **d** | Option A is incorrect because if there are multiple subscriptions, manual counting is not efficient. Option B is incorrect because manual counting is required even for the Manage view. Option C is incorrect because Applying Filters would again lead to a manual count. Option D is CORRECT because the total count can be retrieved using Azure Resour... |
| E298 | **b and d** | Application Option A is Administrator incorrect because is of part Cloud Application Administrators. Option B is CORRECT because please see the referring URL for the AIP roles list. Option C is incorrect because the Group Administrator has access to Administrative features. Option D is CORRECT because please see the referring URL for the AIP rol... |
| E299 | **b** | Option A is CORRECT because all the 3 requirements can be implemented using Monitored activities. Option B is incorrect because only Password Protections options are available. Option C is incorrect because it is used for Identity Protection only. Option D is incorrect because it is used only for important resources. Microsoft Defender for Ident... |
| E300 | **b** | Option A is incorrect because Azure Monitor primarily analyzes the telemetry data. Option B is CORRECT because please view the reference URL for creating policy assignments. Option C is CORRECT because please view the reference URL for creating policy assignments. Option D is CORRECT because please view the reference URL for creating policy assi... |
| E301 | **a** | Option A is CORRECT because please view the reference URL, Active Directory limits section. Option B is incorrect because it would be effective immediately only on logout\login. Option C is incorrect because please view the reference URL, Active Directory limits section. Option D is incorrect because please view the reference URL, Active Directo... |
| E302 | **c** | There are two types of locks available: delete and read-only. A Read-only lock on an SQL Database prevents you from deleting or modifying the database. It does not prevent you from creating, updating, or deleting data in the database. |
| E303 | **a** | Option A is CORRECT because ITSM Connector exists to integrate Azure with Service now. Option B is incorrect because it requires custom requires custom development to achieve the integration. Option C is incorrect because it development to achieve the integration. Option D is incorrect because a connector exists to integrate Azure and specific I... |
| E304 | **c** | Option A is incorrect because these are the locks for the resources and not modes. Option B is incorrect because these are the states of the resources and not modes. Option C is CORRECT because please see the diagram below. Option D is incorrect because “Update” is an invalid lock option, and ReadOnly is a lock on a resource. |
| E305 | **b** | The most cost-effective plan with these points is the Developer plan. The Microsoft documentation mentions the following. |
| E306 | **a** | Yes, everyone has access to the Knowledge Center. |
| E307 | **b** | Azure Service Level Agreements (SLAs) are formal commitments made by Microsoft Azure to ensure the reliability and availability of its cloud services. These SLAs specify the guaranteed uptime percentage for each Azure service, such as Virtual Machines, Blob Storage, and SQL Database, among others. The uptime percentages typically range from 99.9... |
| E308 | **a** | You can launch a support request via the Azure portal. The Microsoft documentation mentions the following. Azure portal for commercial use is: |
| E309 | **a** | This is provided in the FAQ section for Azure support. |
| E310 | **c** | You can easily make use of Azure AI Services. The Microsoft documentation mentions the following. Azure AI Services are cloud-based services with REST APIs and client library SDKs available to help you build cognitive intelligence into your applications. You can add cognitive features to your applications without having artificial intelligence (... |
| E311 | **b** | You can make use of Azure DevTest Labs for this requirement. The Microsoft documentation mentions the following. DevTest Labs provides the following capabilities to developers working with VMs: Create VMs quickly by following fewer than five simple steps. Choose from a curated list of VM bases configured, approved, and authorized by the team lea... |
| E312 | **a** | Yes, this is possible with this service. The Microsoft documentation mentions the following. IoT Hub is a managed service hosted in the cloud that acts as a central message hub for communications in both directions between an IoT application and its attached devices. You can connect millions of devices and their backend solutions reliably and se... |

**E313.** You are planning to use the Azure Cloud Shell service. Which of the following is required by Azure Cloud Shell to work? Choose 3 answers from the options given below:
- a) A resource group
- b) A storage account
- c) A file share
- d) A virtual machine

**E314.** A company needs to deploy a solution to Azure. They want a solution that can distribute content to users worldwide with the least amount of latency. Which of the following could they use for this requirement?
- a) Azure Virtual Network
- b) Azure Content Delivery Network
- c) Azure Load Balancer
- d) Azure Application Gateway

**E315.** A company has just set up an Azure Free account. Is it TRUE that only Azure Virtual Machines and Azure storage accounts can be deployed to the Azure Free Account?
- a) Yes
- b) No

**E316.** Your company has a set of resources defined as part of a subscription. If they delete a resource group, would the resources in the Resource Group also get deleted?
- a) Yes
- b) No

**E317.** Your company has a set of resources defined as part of a subscription. Is it TRUE that Azure resources can only access other resources in the same Resource Group?
- a) Yes
- b) No

**E318.** Your company has a set of resources and resource groups defined as part of a subscription. Can you nest Resource Groups in Azure?
- a) Yes
- b) No

**E319.** A company wants to create an Azure Virtual Machine as part of its subscription. Can the Azure Virtual Machine be a part of multiple Resource Groups?
- a) Yes
- b) No

**E320.** You have to specify whether the following statement is TRUE or FALSE: “General Data Protection Regulation (GDPR) defines data protection and privacy rules”.
- a) True
- b) False

**E321.** You have to specify whether the following statement is TRUE or FALSE: “General Data Protection Regulation (GDPR) only applies to companies that offer goods or services to individuals in the EU”.
- a) Yes
- b) No

**E322.** You have data that is stored in the Archive access tier of an Azure Storage account. Which of the following must be done before you can access the data in the storage account?
- a) The data must be restored
- b) The data must be backed up with Azure Backup
- c) The data needs to be copied by using the azcopy.exe tool
- d) The data needs to be rehydrated

**E323.** Which of the following services would you enable "justin-time VM access"?
- a) Azure Bastion
- b) Azure Firewall
- c) Azure Front Door
- d) Microsoft Defender for Cloud

**E324.** Which is a customer’s responsibility in the cloud (VM services)?
- a) Maintaining the underlying physical servers
- b) Security of data hosted on Azure Virtual Machines
- c) Uptime of the Virtual Machine service
- d) Cooling in the data center

**E325.** A company is planning on hosting Virtual Machines across multiple Availability zones. Which of the following is the company trying to achieve with this implementation?
- a) Better elasticity
- b) Reduction in costs
- c) Better Availability
- d) Disaster Recovery

**E326.** Which one of the following services falls under the category of serverless computing?
- a) Azure virtual machines
- b) Azure SQL database – Elastic pool
- c) Azure Functions
- d) Availability sets

**E327.** Which of the following is used to group subscriptions together?
- a) Resource groups
- b) Region pairs
- c) Management Groups
- d) Availability sets

**E328.** Your company is planning on hosting resources using Azure services. You must decide on the right service for the desired requirement. Which would you use for the following requirement? “Provide the ability to host a private network in Azure”.
- a) Azure App Service
- b) Azure Kubernetes
- c) Windows Virtual Desktop
- d) Azure Virtual Network

**E329.** Your company is planning on hosting resources using Azure services. You must decide on the right service for the desired requirement. Which would you use for the following requirement? “Provide the ability to deploy and orchestrate containerbased applications”.
- a) Azure App Service
- b) Azure Kubernetes
- c) Windows Virtual Desktop
- d) Azure Virtual Network

**E330.** Your company is planning on hosting resources using Azure services. You must decide on the right service for the desired requirement. Which would you use for the following requirement? “Provide the ability to host web-based applications. The platform should provide the ability to host applications based on different programming frameworks”.
- a) Azure App Service
- b) Azure Kubernetes
- c) Windows Virtual Desktop
- d) Azure Virtual Network

**E331.** Your company is planning on hosting resources using Azure services. You must decide on the right service for the desired requirement. Which of the following would you use for the following requirement? “Provide an environment for desktop and application virtualization”.
- a) Azure App Service
- b) Azure Kubernetes
- c) Windows Virtual Desktop
- d) Azure Virtual Network

**E332.** A company is planning on using the Azure Storage Account service. They are going to create a General Purpose V2 storage account and are going to use the Blob service in the storage account. Can they set the objects to use the Archive access tier at the storage account level?
- a) Yes
- b) No

**E333.** Your company is planning on hosting resources using Azure services. You must decide on the right service for the desired requirement. Which would you use for the following requirement? “Provide a service that can host a data warehouse”.
- a) Azure AI Service
- b) Azure DevOps
- c) Azure Bot service
- d) Azure Synapse Analytics

**E334.** Your company plans on hosting resources using Azure services. You must decide on the right service for the desired requirement. Which would you use for the following requirement? “Provide a service to add artificial intelligence features to applications”.
- a) Azure AI Service
- b) Azure DevOps
- c) Azure Bot Service
- d) Azure Synapse Analytics

**E335.** Your company is planning on hosting resources using Azure services. You must decide on the right service for the desired requirement. Which would you use for the following requirement? “Provide a service that is used to integrate bots with applications”.
- a) Azure AI Service
- b) Azure DevOps
- c) Azure Bot service
- d) Azure Synapse Analytics

**E336.** Your company wants to start working with Azure. They want to create and manage resources in Azure. Would you be able to create resources using the Azure CLI?
- a) Yes
- b) No

**E337.** Your company wants to start working with Azure. They want to create and manage resources in Azure. Would you be able to create resources using PowerShell?
- a) Yes
- b) No

### Answers — Section E (Batch 13)

| # | Answer | Explanation |
|---|---|---|
| E313 | **a** | Azure Cloud Shell needs the following to operate. A resource group A storage account A file share You will be prompted for these resources when you start Azure Cloud Shell. |
| E314 | **b** | You can use the Azure Content Delivery Network for this purpose. The Microsoft documentation mentions the following. A content delivery network (CDN) is a distributed network of servers that can efficiently deliver web content to users. CDNs store cached content on edge servers in point-ofpresence (POP) locations close to end users to minimize l... |
| E315 | **b** | We can also utilize other Azure services with the Azure Free Account. We are not restricted to the Azure virtual machine or the Azure storage account service. |
| E316 | **a** | Yes, all of the underlying resources get deleted if a resource group is deleted. |
| E317 | **b** | Azure resources can also reach resources in other resource groups. A resource can connect to resources in other resource groups. This situation is expected when the two resources are related but do not share the same lifecycle. For example, you can have a web app that connects to a database in a different resource group. |
| E318 | **b** | You cannot nest resource groups together. Resource groups cannot be nested inside resource groups. |
| E319 | **b** | A resource in Azure cannot be part of multiple resource groups; it can only be a part of a singular resource group. When we establish a resource such as an Azure virtual machine, it would be a component of a particular resource group. |
| E320 | **a** | The whole purpose of the General Data Protection Regulation is to represent the way personal data is obtained and managed by organizations. Companies must conduct Data Protection Impact Assessments to guarantee compliance with the regulation. |
| E321 | **b** | The General Data Protection Regulation (GDPR) includes new rules for organizations that contribute goods and services to people in the European Union (EU) or that gather and examine data for EU residents no matter where you or your enterprise are established. This document provides information to assist you in honoring rights and performing obli... |
| E322 | **d** | When we have an object in the Archive access tier, to access the object, it requires to be rehydrated. The data needs to be rehydrated and not restored; hence Option A is incorrect. We do not need to back up the data; hence Option B is incorrect. We cannot access objects in the Archive access tier; hence, Option C is incorrect. All the remaining... |
| E323 | **d** | We can allow the just-in-time feature in Microsoft Defender for Cloud, as shown in the picture below. We are required to go to Azure Defender and then access the just-in-time feature. As this is clear from the implementation, all other options are incorrect. |
| E324 | **b** | The customer is only responsible for the security of the data hosted on the Azure virtual machines. All of the other options are the obligation of Azure. |
| E325 | **c** | Option A is incorrect because Elasticity can promptly expand or lower computer processing, memory, and storage resources to satisfy demand. Option B is incorrect because there will be extra costs for more virtual machines and the bandwidth communication within the virtual machines. Option D is incorrect because this is an idea used to recover ag... |
| E326 | **c** | An example of serverless computing is Azure Functions. In this scenario, the underlying compute and the service itself manages infrastructure. Option A is incorrect because the virtual machine service is an Infrastructure as a Service. Option B is incorrect because the Azure SQL database – Elastic pool is a platform as a service. Option D is inc... |
| E327 | **c** | Management groups are used to arrange subscriptions together. We can then manage access and compliance of the subscription components of the management group. Option A is incorrect because this is applied to logical group resources Option B is incorrect because this is applied by Azure to match regions together Option D is incorrect because this... |
| E328 | **d** | The Azure virtual network allows us to host a virtual network in Azure. We can host virtual machines in the virtual network here. Option A is incorrect because this is utilized for hosting web applications. Option B is incorrect because this is applied for orchestrating container-based applications. Option C is incorrect because this is employed... |
| E329 | **b** | We can apply the Azure Kubernetes service to host and orchestrate container-based applications. Option A is incorrect because this is utilized for hosting web applications. Option D is incorrect because this is applied to host a private network in Azure. Option C is incorrect because this is employed for desktop and application virtualization. H... |
| E330 | **a** | We can apply the Azure App service or Web Apps to host web applications. We also can host web applications based on various programming languages. Option D is incorrect because this is applied to host a private network in Azure. Option B is incorrect because this is applied for orchestrating container-based applications. Option C is incorrect be... |
| E331 | **c** | We can apply Windows Virtual Desktop for desktop and application virtualization. Option A is incorrect because this is utilized for hosting web applications. Option B is incorrect because this is applied for orchestrating container-based applications. Option D is incorrect because this is applied to host a private network in Azure. Hence, Option... |
| E332 | **b** | The Archive Access tier can solely be set at the object level and not at the storage account level. If we move to the configuration segment of a storage account, you can arrange the Blob access tier to either hot or cool. The hot access tier has higher storage costs than the cool and archive tiers but the lowest access costs. The cool access tie... |
| E333 | **d** | We can use Azure Synapse Analytics to host a data warehouse. We can host our Big Data warehouse and also perform big data analytics. Option A is incorrect because this is utilized to develop cognitive intelligence in applications. Option B is incorrect because this is a set of tools for implementing DevOps. Option C is incorrect because this is ... |
| E334 | **a** | You can utilize the Azure AI service to develop applications with artificial intelligence capabilities. There are several services available in Azure AI services based on the following classifications Vision Speech Language Decision Search Option D is incorrect because this applies when we host a data warehouse. Option B is incorrect because thi... |
| E335 | **c** | We can build bots within applications using the Azure Bot service. Option A is incorrect because this is utilized to develop cognitive intelligence in applications. Option B is incorrect because this is a set of tools for implementing DevOps. Option D is incorrect because this applies when we host a data warehouse. Hence, Option C is the correct... |
| E336 | **a** | Yes, the Azure command-line interface is intended for generating and managing resources in Azure. |
| E337 | **a** | Yes, with PowerShell, we can install the Azure PowerShell modules and work with resources in Azure. |

**E338.** Your company wants to host a set of Azure Virtual Machines. However, they want to ensure that only their virtual machines are hosted on the underlying physical server. Which of the following would you make use of for this requirement?
- a) Azure App Service
- b) Azure Kubernetes
- c) Azure Functions
- d) Azure Dedicated Hosts

**E339.** A company wants to make use of the various security services in Azure. They want the ability to store secrets and certificates in the Azure cloud. They decide to use the Azure Key Vault service. Would this fulfill the requirement?
- a) Yes
- b) No

**E340.** A company wants to make use of the various security services in Azure. They want to get security recommendations for resources deployed to their Azure subscription. They decide to use the Azure Key Vault service. Would this fulfill the requirement?
- a) Yes
- b) No

**E341.** A company wants to make use of the various security services in Azure. They want to restrict the inbound traffic to Azure Virtual Machines. They decide to use Microsoft Defender for Cloud service. Would this fulfill the requirement?
- a) Yes
- b) No

**E342.** A company has just set up an Azure subscription and an Azure tenant. They want to use services that would fulfill different requirements. Which can be used for the following requirement? “Ensure that only Virtual Machines of a particular SKU size can be launched within an Azure subscription”.
- a) Azure resource locks
- b) Azure Policies
- c) Azure Blueprints
- d) Azure resource tags

**E343.** A company has just set up an Azure subscription and an Azure tenant. They want to use services that would fulfill different requirements. Which can be used for the following requirement? “Be able to organize resources for billing purposes”.
- a) Azure resource locks
- b) Azure Policies
- c) Azure Blueprints
- d) Azure resource tags

**E344.** A company has just set up an Azure subscription and an Azure tenant. They want to use services that would fulfill different requirements. Which can be used for the following requirement? “Provide a declarative way to orchestrate the deployment of various resources”.
- a) Azure resource locks
- b) Azure Policies
- c) Azure Blueprints
- d) Azure resource tags

**E345.** Which service in Azure can be used to enable MultiFactor Authentication for Azure users?
- a) Azure Sentinel
- b) Azure Key Vault
- c) Microsoft Defender for Cloud
- d) Microsoft Entra ID

**E346.** Your company wants to use the Total Cost of Ownership (TCO) calculator to assess the costs of moving its existing resources to the cloud. Could you see the TCO for server workloads that need to be migrated to Azure?
- a) Yes
- b) No

**E347.** Your company wants to use the Total Cost of Ownership calculator to assess the costs of moving its existing resources to the cloud. Can you download the report to share with other stakeholders?
- a) Yes
- b) No

**E348.** Your company wants to deploy a set of Azure virtual machines and increase the availability of the underlying machines. You decide to deploy the machines across multiple Resource Groups. Would this fulfill the requirement?
- a) Yes
- b) No

**E349.** Your company wants to deploy a set of Azure virtual machines and increase the availability of the underlying machines. You decide to deploy the machines across multiple subscriptions. Would this fulfill the requirement?
- a) Yes
- b) No

**E350.** Your company wants to deploy a set of Azure virtual machines and increase the availability of the underlying machines. You decide to deploy the machines across multiple availability zones. Would this fulfill the requirement?
- a) Yes
- b) No

**E351.** Your company has just set up an Azure account. They also have resources deployed in their on-premises data center. They want to connect their Azure virtual network to their on-premises data center. Can they consider using Azure virtual network peering for this requirement?
- a) Yes
- b) No

**E352.** Your company has just set up an Azure account. They also have resources deployed in their on-premises data center. They want to connect their Azure virtual network to their on-premises data center. Can they consider using Azure ExpressRoute for this requirement?
- a) Yes
- b) No

**E353.** Your company has just set up an Azure account. They also have resources deployed in their on-premises data center. They want to connect their Azure virtual network to their on-premises data center. Can they consider using Azure Site-to-Site VPN for this requirement?
- a) Yes
- b) No

**E354.** Your company is trying to assess the benefits of using the Azure Cosmos DB service. Can they migrate their existing MongoDB database onto Azure Cosmos DB?
- a) Yes
- b) No

**E355.** Your company is trying to assess the benefits of using the Azure Cosmos DB service. Can they migrate their SQL Server workloads to Azure Cosmos DB?
- a) Yes
- b) No

**E356.** Your company is trying to assess the benefits of using the Azure Cosmos DB service. Can data in an Azure Cosmos DB account be available in multiple Azure locations?
- a) Yes
- b) No

**E357.** Your company wants to make use of the Azure storage account service. They have provisioned a General Purpose V2 storage account. Which service in the storage account is used for storing hard disk files for Azure virtual machines?
- a) File
- b) Blob
- c) Queue
- d) Table

**E358.** Your company wants to make use of the Azure storage account service. They have provisioned a General Purpose V2 storage account. Which service in the storage account is used for storing objects?
- a) File
- b) Blob
- c) Queue
- d) Table

**E359.** Your company wants to make use of the Azure storage account service. They have provisioned a General Purpose V2 storage account. Which service in the storage account is used for storing files that can be accessed via the Server Message Block protocol?
- a) File
- b) Blob
- c) Queue
- d) Table

**E360.** A company has a set of Azure Virtual Machines hosting web servers. The web servers need to send logs to a central log store. What can be used for this requirement?
- a) Azure Advisor
- b) Azure Monitor
- c) Azure Service Health
- d) Azure DevOps

**E361.** Which of the following is used as a secured, high-level application platform with built-in communication and security features for internet-connected devices?
- a) Azure Synapse
- b) Azure Sphere
- c) Azure Databricks
- d) Azure HDInsight

**E362.** Your company is planning on hosting a set of Virtual Machines in Azure. They want to save on the running compute costs for the Virtual Machines. Can they consider using reserved instances for this requirement?
- a) Yes
- b) No

### Answers — Section E (Batch 14)

| # | Answer | Explanation |
|---|---|---|
| E338 | **d** | We can allocate the underlying physical server as a resource with Azure Dedicated Hosts. We can then host virtual machines on the underlying physical server. Option A is invalid since this is utilized for hosting web applications. Option B is invalid since this is employed for hosting container-based applications. Option C is invalid since this ... |
| E339 | **a** | Yes, this is the correct service to fulfill this condition. With the aid of the Azure Key Vault service, the company can store secrets, encryption keys, and certificates. |
| E340 | **b** | The company should adopt the Microsoft Defender for Cloud service for this specification. The Azure Key Vault service is adopted to store secrets, encryption keys, and certificates. We can get many recommendations using Microsoft Defender for Cloud service. An example is shown in the picture below. |
| E341 | **b** | The company should use Network Security Groups to fulfill this condition. With Network Security Groups, we can append inbound rules to limit the inbound traffic to virtual machines. The Microsoft Defender for Cloud service is adopted to strengthen the security posture of resources created as part of our Azure subscription. |
| E342 | **b** | This requirement can be fulfilled by the use of Azure Policies. With Azure policies, we can apply an in-built policy to define the SKU size that can be used to launch an Azure virtual machine. As shown in the figure below, an inbuilt policy can already be utilized for this purpose. Option A is invalid because this is used to shield resources fro... |
| E343 | **d** | Azure resource tags can be utilized to organize resources. We can then observe the billing aspect of the resources based on resource tags. Option B is invalid because this is used as a governance service for our resources. Option C is invalid because this is applied to orchestrate the deployment of resources. Option A is invalid because this is ... |
| E344 | **c** | Azure Blueprints can be adopted to orchestrate the deployment of multiple resource templates and artifacts. Role Assignments Policy Assignments Azure Resource templates) Resource Groups Manager templates (ARM Option B is invalid because this is used as a governance service for our resources. Option D is invalid because this is adopted to organiz... |
| E345 | **d** | Azure Multi-Factor Authentication can be enabled in a couple of ways. This can be done from Microsoft Entra ID. As shown in the figure below, if we go to the Users section, we can enable Multi-Factor Authentication. The other options are invalid because we cannot enable Multi-Factor Authentication in the other services. |
| E346 | **a** | Using the Total Cost of Ownership calculator, we can understand the TCO for server workloads. |
| E347 | **a** | We can scroll down and then download the report in the Final Report section for the TCO Calculator. It is also shown in the figure below. |
| E348 | **b** | For the logical grouping of resources, we use resource groups. For availability, we can deploy either across Availability sets or Availability zones. |
| E349 | **b** | Subscriptions are applied more from a billing aspect for Azure resources. For availability, we can deploy either across Availability sets or Availability zones. |
| E350 | **a** | Yes, this is the correct strategy. We can apply either Availability sets or zones to enhance the availability of our virtual machines. |
| E351 | **b** | Azure virtual network peering connects two Azure virtual networks. To fulfill the given requirement, the company should consider a Site-to-Site VPN connection or adopting Azure ExpressRoute. |
| E352 | **a** | Yes, this is the correct approach. Azure ExpressRoute can connect an Azure virtual network to our on-premises data center. |
| E353 | **a** | Yes, this is the correct approach. An Azure Site-to-Site VPN can be utilized to connect an Azure virtual network to our on-premises data center. |
| E354 | **a** | There are various APIs available with Azure Cosmos DB. One of the APIs that can be utilized is the MongoDB API. We can transfer our current MongoDB workloads to Azure Cosmos DB as well. |
| E355 | **a** | The Cosmos DB Data Migration tool is an executable tool that needs no installation to commence the migration process. Double-click on the tool's executable file to launch the Data Migration tool, and it will start immediately. When the Data Migration tool launches, the Welcome page will present a section of basic information about that tool, giv... |
| E356 | **a** | We can replicate our data to multiple locations using Azure Cosmos DB. In an Azure Cosmos DB account, we can replicate the data onto another location if we go to the “Replicate data globally” section. It is shown in the figure below. |
| E357 | **b** | The given requirement can be fulfilled through the use of the Blob service. Using the Blob service, we can store hard disk files for our virtual machines. Option A is invalid because this is utilized for storing files that can be accessed through the server message block protocol. Option C is invalid because this is employed as a messaging servi... |
| E358 | **b** | The given requirement can be fulfilled through the use of the Blob service. This is the object-level storage service implemented in Azure. Option A is invalid because this is utilized for storing files that can be accessed through the server message block protocol. Option C is invalid because this is employed as a messaging service. Option D is ... |
| E359 | **a** | Using the file service, we can host file shares that can be accessed through the Server Message Block protocol. Option B is invalid because this is an object-level storage service implemented in Azure. Option C is invalid because this is employed as a messaging service. Option D is invalid because this is used for the storage of key/value pairs.... |
| E360 | **b** | We can apply the Log Analytics workspace feature in Azure Monitor to store the logs. Option A is invalid because this is a recommendation engine in Azure. Option C is invalid because this is applied to present the health of the underlying Azure services. Option D is invalid because this is utilized as a toolset for implementing DevOps. Hence, Op... |
| E361 | **b** | Azure Sphere is a secured, high-level application platform with built-in communication and safety characteristics for internet-connected devices. Option A is invalid because this is utilized for hosting a data warehouse. Option C is invalid because this is a data analytics platform. Option D is invalid because this is an open-source analytics se... |
| E362 | **a** | Yes, this option can be considered. The company can get discounts on costs for Azure virtual machines by using reserved instances. |

**E363.** Your company is planning on hosting a set of Virtual Machines in Azure. They want to save on the running compute costs for the Virtual Machines. Can they consider using Spot VMs for this requirement?
- a) Yes
- b) No

**E364.** Your company is planning on hosting a set of Virtual Machines in Azure. (the application must reside on Virtual Machines) They want to save on the running compute costs for the Virtual Machines. Can they consider using Azure Functions for this requirement?
- a) Yes
- b) No

**E365.** Which of the following services is a cloud-based network security service that helps protect the resources stored in an Azure Virtual Network?
- a) Azure Sentinel
- b) Azure Key Vault
- c) Azure Dedicated Host
- d) Azure Firewall

**E366.** Your company's data centers are in New York and Los Angeles. The business subscribes to Microsoft Azure. You set up the two data centers for site resilience as geoclustered sites. You must suggest a redundant Azure storage solution. You need to store the following types of data: Multiple nodes must be used to store data. Data must be kept on nodes at different places geographically. Both the primary location and the secondary site can read data. Which option for Azure stored redundancy would you suggest?
- a) Zone-Redundant Storage
- b) Geo-Redundant Storage
- c) Locally Redundant Storage
- d) Read-Access Geo-Redundant Storage

**E367.** Ten web applications made by your developers must be hosted on Azure. Which Azure web tier plan will be used to host the web apps? The web tier plan needs to fulfill the following criteria: Custom domains will be used by the web apps. Each web application needs 10 GB of storage. Each of the web applications needs its own dedicated computing instance It is necessary to implement load balancing between instances Costs must be kept to a minimum Which web tier plan ought to be utilized?
- a) Standard
- b) Basic
- c) Both A and B can be used
- d) Shared

**E368.** Microsoft Azure hosts Virtual Machines (VMs) for your business. A single Azure Virtual Network called VNet1 contains all of the VMs. Some users work remotely for the company. The VMs on VNet1 must be accessible to these remote workers. You must make access available to the remote workers. What should you do?
- a) Configure Site-to-Site VPN
- b) Configure Point-to-Site VPN
- c) Configure VNet-to-VNet VPN
- d) Configure a Multi-Site VPN

**E369.** According to organizational policies, which Microsoft Entra ID functionality grants access to resources?
- a) Conditional Access
- b) Administrative Units
- c) Multi-Factor Authentication
- d) Single Sign-On (SSO)

**E370.** Which cloud strategy is employed by businesses to fully leverage their on-premises IT investments and enable the sharing of data and applications between two environments?
- a) Private Cloud
- b) Public Cloud
- c) On-premises Databases
- d) Hybrid Cloud

**E371.** Which setting enables encrypted internet-based communication between an on-premises VPN device and an Azure VPN gateway?
- a) Site-to-Site VPN
- b) Point-to-Site VPN
- c) VNet-to-VNet VPN
- d) ExpressRoute

**E372.** Which of the following Azure features allows you to place Azure resources close to users?
- a) Elasticity
- b) Scalability
- c) High Availability
- d) Geo-distribution

**E373.** Which of the following allows you to create a collection of synchronized, load-balanced Virtual Machines in Azure?
- a) Azure Logic Apps
- b) Azure Virtual Machine Scale Set
- c) Availability set
- d) Azure Load Balancer

**E374.** Which of the following allows for scaling up to thousands of Virtual Machines for high-performance computing and massively parallel tasks?
- a) Azure Batch
- b) Azure Virtual Machine Scale Set
- c) Availability set
- d) Availability zone

**E375.** Which layer of defense in depth protects against Distributed Denial of Service (DDoS)?
- a) Physical Security Layer
- b) Application Layer
- c) Perimeter Layer
- d) Network Layer

**E376.** In addition to 50 Virtual Machines hosted in Azure, you also have 50 Virtual Machines hosted on-site. The virtual computers in Azure and on-premises are connected. Which cloud model is this?
- a) Public Cloud
- b) Private Cloud
- c) Hybrid Cloud
- d) None of the above

**E377.** Your business intends to upload several original applications to Azure. The company's clients will receive invoicing services from the applications. There will be some required applications and services installed for each application. For each application, you must suggest a cloud deployment solution. What should you suggest?
- a) Software as a Service
- b) Infrastructure as a Service
- c) Platform as a Service
- d) None of the above

**E378.** What does a customer provide in a Software as a Service (SaaS) model?
- a) Application Data
- b) Application software
- c) Data Storage
- d) Compute resources

**E379.** Your business intends to move all of its resources and data to Azure. According to the company's migration strategy, Azure can only be used for Platform as a Service (PaaS) solutions. Deploy an Azure environment organization's migration strategy. What ought you to produce? that adheres to the
- a) Azure storage accounts, Azure Virtual Machines, and Azure SQL databases
- b) Microsoft SQL Server-equipped Azure Virtual Machine and an Azure App Service
- c) Azure SQL databases and an Azure App Service
- d) Azure Virtual Machines house the web server and storage accounts

**E380.** Several servers are part of your on-premises network. You intend to move every server to Azure. If a single Azure data center falls unavailable for an extended period, you must provide a method to guarantee that some servers are still operational. What should the recommendation contain?
- a) Elasticity
- b) Fault Tolerance
- c) Low Latency
- d) Scalability

**E381.** What two features do public clouds have?
- a) Dedicated Hardware
- b) Unsecure connections
- c) Limited Storage
- d) Self-Service Management
- e) Metered Pricing

**E382.** All of the clients of your business utilize an accounting application called App1 that is hosted by your business. The first three weeks of every month see little usage of App1, whereas the last week of every month sees exceptionally high usage. Which Azure Cloud Services feature helps with cost management for this usage pattern?
- a) Elasticity
- b) High Latency
- c) High Availability
- d) Load balancing

**E383.** An existing online application will be moved to Azure. External users can access the online application. You must suggest a cloud deployment option to reduce the administrative work required to manage application. What should the recommendation contain? the online
- a) Database as a Service
- b) Platform as a Service
- c) Infrastructure as a Service
- d) Software as a Service

**E384.** You have a network on your premises with 100 servers. You must advise your users to use a solution that gives them more resources. The answer must reduce both capital and operating expense costs. What ought to be contained in the recommendation?
- a) Private Cloud
- b) Public Cloud
- c) Hybrid Cloud
- d) None of the above

**E385.** From an on-premises network, you intend to move a number of servers to Azure. What benefits do public cloud services provide over an onpremises network for the servers?
- a) The public, not a private company, is the owner of the public cloud
- b) A public cloud is a crowdsourcing tool that gives businesses a chance to improve the cloud
- c) Everybody in public has free access to all public cloud resources
- d) The public cloud is a shared resource that is utilized by numerous businesses, each of which uses a fraction of the cloud's resources

**E386.** Which cloud model allows several tenants to share one set of hardware resources owned by a third party?
- a) Public Cloud
- b) Private Cloud
- c) Hybrid Cloud
- d) None of the Above

**E387.** In a data center, 1,000 virtual machines are housed on Hyper-V hosts. All Virtual Machines will be switched to an Azure pay-as-yougo subscription. You must decide which spending model to use for the envisioned Azure solution. Which spending model should you choose?
- a) Capital
- b) Operational
- c) Elastic
- d) Scalable

### Answers — Section E (Batch 15)

| # | Answer | Explanation |
|---|---|---|
| E363 | **a** | We can run virtual machines at a lower price using Spot VMs. The only concern is that this is based on unused capacity in Azure. And the virtual machine can be taken back anytime if Azure runs out of space. |
| E364 | **b** | Azure Functions is a serverless compute service. In this scenario, we need to use Azure virtual machines. Therefore, Azure Functions cannot be utilized as a possibility. You can utilize either reserved instances or Spot VMs. |
| E365 | **d** | The Azure Firewall is a cloud-based service that can defend resources in an Azure virtual network. In this scenario, you can specify network rules and application rules to preserve your Azure Virtual Network. Option A is invalid since this is employed for threat detection. Option B is invalid since this is utilized for storing secrets, encryptio... |
| E366 | **d** | With the added benefit that the secondary copies stored in paired Azure regions are readable, RA-GRS replicates data with the same level of redundancy as normal GRS replication. In other words, you can use a variety of readable endpoints if your application is configured correctly. As a result, read operations now have a 99.99% SLA. Although a s... |
| E367 | **c** | Storage capacity is provided in 50 GB for S6tandard and 10 GB for Basic. |
| E368 | **b** | You can establish a secure connection to your virtual network from a single client computer using a Pointto-Site (P2S) VPN gateway connection. Start the P2S connection from the client's computer to establish it. Telecommuters who want to access Azure VNets from a distant place, such as their home or a conference, can take advantage of this optio... |
| E369 | **b** | Based on identification signals, Microsoft Entra ID uses Conditional Access as a tool to provide (or restrict) access to resources. A more advanced form of MFA (multifactor authentication) is conditional access. After first-factor authentication is complete, conditional access rules are put into effect. In situations like Denial-ofService (DoS) ... |
| E370 | **d** | Public Cloud: Third-party cloud service providers use public clouds (like Microsoft Azure) that are owned and maintained by them to distribute their computing resources, such as servers and storage, over the Internet. The cloud provider manages all equipment, software, and other supporting infrastructure. Private Cloud: Cloud computing services ... |
| E371 | **a** | Your on-premises network and an Azure virtual network are connected via a Site-to-Site VPN gateway connection using an IPsec/IKE (IKEv1 or IKEv2) VPN tunnel. An on-site VPN device with a public IP address visible from the outside is necessary for this kind of connection. |
| E372 | **d** | You can deploy apps and data to regional data centers worldwide due to geo-distribution, guaranteeing that your clients always have the greatest performance in their area. |
| E373 | **b** | Using virtual machine scale, you can set up a collection of matched and load-balanced virtual machines in Azure. Imagine that you are in charge of a website where researchers can submit processing-required astronomy photographs. To route requests among many instances of the website, you would typically need to establish an additional service if ... |
| E374 | **a** | For High-Performance Computing (HPC) and massively parallel applications, Azure Batch enables scaling to thousands of virtual machines. Only Azure Batch will support thousands of VMs for HPC, despite other Azure functions allowing you to scale numerous VMs. |
| E375 | **c** | The perimeter layer employs Distributed Denial-of-Service (DDoS) protection against massive attacks before they can deny users access to services. |
| E376 | **c** | A hybrid cloud that mixes on-site infrastructure or a private cloud with a public cloud is known as hybrid cloud computing. Data and apps can travel between the two environments with hybrid clouds. |
| E377 | **b** | IaaS, or infrastructure as a service, is a computing infrastructure that can be provided and controlled instantly through the Internet. While you buy, install, set up, and maintain your own software, the IaaS service provider looks after the infrastructure. Incorrect responses Option A is incorrect; users can access and use cloud-based applicati... |
| E378 | **a** | SaaS offers a complete software solution from a cloud service provider that you can pay for as you go. Your users connect to an app you rented for your business over the Internet, typically using a web browser. The service provider's data center houses the supporting infrastructure, middleware, app software, and app data. With a suitable service... |
| E379 | **c** | Examples of Azure PaaS products include Azure App Service and Azure SQL databases. As a result, the goal is achieved by this solution. |
| E380 | **b** | The ability of a system to continue operating even if some of its components fail is known as fault tolerance. You might have servers replicated across different data centers in this scenario. The level of control you have over ensuring that the data and apps on your virtual machines are always accessible is increased by availability zones. With... |
| E381 | **d and e** | With the public cloud, you can get pay-as-yougo pricing, which means you only pay for the services you actually use. Self-service administration is available with public clouds. You are responsible for setting up and deploying cloud resources like websites or virtual machines. The cloud provider is responsible for maintaining the underlying hard... |
| E382 | **a** | Elasticity in this context refers to the capacity to increase compute resources when necessary and decrease them when not required to lower costs. Elasticity is demonstrated by autoscaling. Elastic computing refers to swiftly increasing or decreasing computer processor, memory, and storage capabilities to suit changing demands without worrying a... |
| E383 | **b** | With the help of the Platform as a Service (PaaS) Azure App Service, you can build web and mobile applications for any device or platform and access data stored everywhere, including on-premises or in the cloud. Web and mobile functionality formerly provided separately as Azure Websites and Azure Mobile Services are now included in App Service. |
| E384 | **c** | Private and public clouds are combined to form a hybrid cloud. The upfront infrastructure purchase, such as new servers, is a capital investment. Using a hybrid cloud, you can keep using your on-premises servers while adding new ones to the public cloud (Azure, for example). By deploying new servers in Azure rather than on-premises, you can expa... |
| E385 | **d** | The public cloud is a shared resource utilized by numerous organizations, each using a fraction of its resources. The cloud service provider manages the hardware resources (servers, infrastructure, etc.). On top of the hardware resources, several companies produce resources like virtual machines and networks. Incorrect Responses Option A is inco... |
| E386 | **a** | Microsoft Azure, Amazon Web Services, and Google Cloud are three public cloud services. Google, Amazon, and Microsoft own the hardware. Customers who use public cloud services are known as tenants. |
| E387 | **b** | When switching from an on-premises cloud to a public cloud, you will experience the biggest shift from capital expenditures (purchasing hardware) to operating expenditures (paying for service as you use it). Additionally, this changeover necessitates more careful cost management. The advantage of using the cloud is that you may significantly red... |

**E388.** One hundred servers are part of your on-premises network. You must advocate for a solution that gives your users more resources. Costs associated with capital and operating expenditures must be kept to a minimum. What should the recommendation contain?
- a) Complete migration to the public cloud
- b) An additional data center
- c) Private cloud
- d) Public cloud

**E389.** From an on-premises network, you intend to move a number of servers to Azure. What benefits do public cloud services provide over an onpremises network for the servers?
- a) The public, not a private company, is the owner of the public cloud
- b) The public cloud is a crowdsourcing tool that gives businesses a chance to improve the cloud
- c) Everybody in public has free access to all public cloud resources
- d) The public cloud is a shared resource that is utilized by numerous businesses, each of which uses a fraction of the cloud's resources

**E390.** What Azure feature allows resources to be replicated between regions even when 300 miles apart?
- a) Sovereign Regions
- b) Region Pair
- c) Availability Zone
- d) Availability Set

**E391.** Which Azure service enables customers to log in using most contemporary browsers and enjoy a cloud-hosted version of Windows from any location?
- a) Azure Virtual Machine
- b) Azure Logic Apps
- c) Azure Virtual Desktop
- d) Azure Functions

**E392.** What attribute of an Azure virtual machine staggers updates among VMs according to their update domain and fault domain?
- a) Availability Sets
- b) Scale Sets
- c) Availability Zone
- d) Region

**E393.** Which Azure Storage service can handle text, binary data formats, and big data analytics?
- a) Table Storage
- b) Blob Storage
- c) Queue Storage
- d) Archive

**E394.** Which of the following enables the automated updating of files between an on-premises Windows server and an Azure cloud environment?
- a) Storage Explorer
- b) AzCopy
- c) Azure Sync File
- d) Archive

**E395.** Depending on signals like the user's location, which Microsoft Entra ID tool can change the login credentials required?
- a) Conditional Access
- b) Passwordless
- c) Guest Access
- d) None of the above

**E396.** Which security approach protects resources assuming the worst-case security scenario? by
- a) Defender
- b) Role-Based Access Control
- c) Defense-in-depth
- d) Zero Trust Model

**E397.** Multiple roles are simultaneously assigned to users when role-based access control is used. What actual permissions do they have? These are the role permissions: Role – 1: Read Role – 2: Write Role – 3: Read and Write
- a) Read and write
- b) Write only
- c) Read only
- d) None of the above

**E398.** How can you avoid manually assessing each resource as it is being created and prevent the creation of noncompliant resources?
- a) Azure Policy
- b) Azure Blueprint
- c) Azure Resource Manager
- d) Role-Based Access Control

**E399.** How many parameters are required for an Azure Blueprint Artifact to be functional?
- a) 3
- b) 0
- c) 1
- d) 2

**E400.** What service aids in managing your on-premises, multi-cloud, and Azure environments?
- a) Azure Resource Manager
- b) Azure Policy
- c) Azure Blueprint
- d) Azure Arc

**E401.** What two elements can you employ to implement an "infrastructure as code" deployment?
- a) Azure Policy and Azure Arc
- b) Azure Policy and Azure Blueprint
- c) Azure Blueprint and ARM Templates
- d) Azure Arc and Azure Monitor

**E402.** Which does not fall under recommended categories? the Azure Advisor
- a) Capacity
- b) Performance
- c) Reliability
- d) Cost

**E403.** You get a message through email that one of the Virtual Machines (VMs) you have deployed in an Azure region is suffering an outage. What part of Azure Service Health will inform you if your application is impacted?
- a) Service Health
- b) Performance
- c) Resource Health
- d) Azure Monitor

**E404.** What phase of the Microsoft Framework for Azure is the first? Cloud Adoption
- a) Make a plan
- b) Build organization
- c) Start using Cloud
- d) Design Strategy

**E405.** Which of the following best describes a virtual machine's ability to expand its computational power by adding memory or CPUs?
- a) Vertical Scaling
- b) Horizontal Scaling
- c) Elasticity
- d) Agility

**E406.** Which of the following are the features of Azure Virtual Network?
- a) Packet Inspection
- b) Geo-Redundancy
- c) Resource Cost Analysis
- d) Isolation
- e) Segmentation

**E407.** The kind of failure for which an Azure Availability Zone can be utilized to safeguard access to Azure services must be determined. What ar you supposed to notice in this case?
- a) Azure Region Failure
- b) Data center Failure
- c) Physical Server Failure
- d) Storage Failure

**E408.** Your business intends to switch to Azure. The business has numerous departments. A department administrator will oversee each department's utilization of all Azure resources. What two methods might be used to divide Azure into departments?
- a) Multiple Regions
- b) Multiple Tenants
- c) Multiple Resource Groups
- d) Multiple Azure Ad Directories
- e) Multiple Subscriptions

**E409.** You have several Azure Virtual Machines in your Azure setup. The client computers on your on-premises network will be able to communicate with the Azure Virtual Machines with a solution you intend to build. Which Azure resources should be developed for the intended solution must be suggested. Which two Azure resources ought to be mentioned in the suggestion?
- a) VNet Gateway
- b) Gateway Subnet
- c) Application Gateway
- d) Load Balancer
- e) Azure Virtual Network

**E410.** You attempt to set up multiple managed Microsoft SQL Server instances in Azure but are informed that your Azure subscription limits need to be increased. What actions are necessary to raise the limits?
- a) Create a new support request
- b) Modify an Azure Policy
- c) Create service health alert
- d) Upgrade support plan

**E411.** Your business intends to transfer several servers to Azure. According to the company's compliance guidelines, FinServer must be located on a different network segment. The Azure services that can be leveraged to satisfy the compliance policy requirements are being evaluated. Which Azure product would you suggest?
- a) FinServer has its own resource group, and all the other servers have their own resource group
- b) A separate Virtual Network for all the other servers and one for FinServer Manyest Votes
- c) A Virtual Network gateway for every other server and a VPN for FinServer
- d) A resource lock for FinServer and a single resource group for all servers

**E412.** You want to map a network drive from several Windows 10 computers to Azure Storage. You must construct a storage solution in Azure for the anticipated mapped disk. What ought you to produce?
- a) Blob Service in Storage Account
- b) Virtual Machine Data Disk
- c) Azure SQL Database
- d) File Service in Storage Account

### Answers — Section E (Batch 16)

| # | Answer | Explanation |
|---|---|---|
| E388 | **d** | A hybrid cloud is made up of both private and public clouds. Spending money in advance on infrastructure, such as new servers, is known as capital expenditure. With a hybrid cloud, you can keep using the on-premises servers while adding new servers to the public cloud (Azure, for example). As you are not paying for new servers as you would if yo... |
| E389 | **d** | The resources in the public cloud are shared by several businesses, each using a piece of them. The cloud provider manages the hardware resources (servers, infrastructure, etc.). On the hardware resources, numerous businesses produce resources like virtual machines and virtual networks. Option A is incorrect, as the general public does not own t... |
| E390 | **b** | Most Azure region are paired with a neighboring region at least 300 miles distant and located in the same geographic area (such as the US, Europe, or Asia). |
| E391 | **c** | Most current browsers are compatible with Azure Virtual Desktop, which gives access to a hosted version of Windows in the cloud. |
| E392 | **a** | In accordance with their update and fault domains, availability settings space out VM updates. |
| E393 | **b** | Azure Blobs is a highly scalable object store for text and binary data. Azure Blobs offers Data Lake Storage Gen2 capabilities for large data analytics. |
| E394 | **c** | Your on-premises and cloud Windows servers are kept in bidirectional synchronization with Azure File Sync. |
| E395 | **a** | Microsoft Entra ID employs Conditional Access as a mechanism to provide (or prohibit) access to resources in accordance with identification signals. If your sign-in signals are irregular or originate from an unexpected location, Conditional Access may request authentication factor from you. |
| E396 | **d** | A security concept known as "Zero Trust" guards resources by preparing for the worst-case situation. |
| E397 | **c** | All permissions assigned in the given roles are granted via role-based access control using an allowed model. |
| E398 | **a** | Azure policy enables you to define initiatives (groups of rules) and policies that forbid the creation of noncompliant resources. |
| E399 | **b** | Artifacts might not have any additional parameters. For example, the "Deploy threat detection on SQL servers" policy needs no additional settings. |
| E400 | **d** | You may expand your Azure compliance and monitoring to your hybrid and multi-cloud deployments using Azure Arc in conjunction with Azure Resource Manager. |
| E401 | **c** | You can publish your resource as code using ARM Templates and Azure Blueprints, which automatically apply policies. Combining the two makes it easier to ensure you are deploying reliable legal resources. |
| E402 | **a** | The five suggestion categories for Azure Advisor are cost, operational excellence, performance, security, and reliability. |
| E403 | **c** | Resource Health is an accurate representation of your actual Azure resources. It gives details on the state of each of your particular cloud resources. |
| E404 | **d** | Multiple steps are involved in migrating to Microsoft Azure Cloud Adoption Framework; these are: 1. Define Strategy 2. Plan 3. Ready 4. Adopt 5. Govern 6. Manage The strategy for the adoption should include the following: 1. Recognize motivations Learn about cloud economics and obtain the technical and financial advice you need to create your cl... |
| E405 | **a** | Vertical scaling, sometimes called scale up and down, changes the size of a Virtual Machine (VM) in response to a workload. Contrast this behavior with horizontal scaling, often known as scale out and scale in, which changes the number of VMs based on the workload. |
| E406 | **d and e** | Apply Azure network segmentation patterns. A standardized enterprise segmentation strategy directs technical teams to systematically segment access using identity, networking, apps, and other access restrictions. By establishing perimeters, segment your network footprint. These are the main justifications for segmentation: The capacity to organi... |
| E407 | **b** | The level of control you have over ensuring that the data and apps on your virtual machines are always accessible is increased by availability zones. Within an Azure region, an Availability Zone is a physically distinct zone. Each supported Azure region has three Availability Zones. Power, networking, and cooling are all unique to each Availabil... |
| E408 | **c and e** | A container for Azure resources is called an Azure subscription. Additionally, it serves as a limit for billing and resource access permissions. All of the resources in a subscription are billed monthly. Multiple Azure subscriptions may be included in a single Azure tenant (Microsoft Entra ID). For an Azure solution, a resource group is a contai... |
| E409 | **a and b** | You must set up a VPN (Virtual Private Network) to link the on-premises network to the Azure virtual network to deploy a solution that allows the client computers on your on-premises network to communicate with the Azure virtual machines. A virtual network gateway is the name of the Azure VPN device. The Azure virtual network must have a specifi... |
| E410 | **c** | There are quotation limits on several Azure resources. The quota restrictions are there to aid you in keeping tabs on your Azure expenses. The default quota frequently needed to be increased, though. By submitting a support request, you can ask for an increase in the quota limit. Select "Service and subscription limits (quotas)" as the issue typ... |
| E411 | **b** | Virtual networks are the name given to networks in Azure. A virtual network may contain numerous subnets and IP address spaces. Within a virtual network, Azure automatically manages traffic routing across several subnets. According to the query, FinServer has to be on a different network segment. Regarding networking, the only method to distingu... |
| E412 | **d** | Microsoft's user-friendly cloud file system is called Azure Files. The use of Azure file sharing with Windows and Windows Server is straightforward. You must either mount an Azure file share, which entails giving it a drive letter, or mount a point path or access it via its UNC path to use it with Windows. Although this is a feature we are worki... |

**E413.** Your business intends to switch to Azure and move all its network resources there. Investigating Azure is where you should start the planning process. What should you produce initially?
- a) Virtual Network
- b) Management Group
- c) Subscription
- d) Resource Group

**E414.** What Azure service should you use to consolidate events from several resources into one location?
- a) Azure Event Hub
- b) Defender for Cloud
- c) Azure Policy
- d) Azure Data Analytics

**E415.** You must be informed when Microsoft intends to perform maintenance that can impact the resources deployed to an Azure subscription. Which of the following should you employ?
- a) Azure Trust Center
- b) Azure Service Health
- c) Azure Advisor
- d) Azure Resource Health

**E416.** A third-party virtual security appliance must be purchased before it can be installed on an Azure subscription. Which should you employ?
- a) Microsoft Store
- b) Azure Defender for Cloud
- c) Azure Marketplace
- d) Azure Subscription

**E417.** You are going to use Azure Virtual Machines to deploy a service. If a data center fails, you must ensure the service is still available. Which of the following should you employ in the deployment of Virtual Machines?
- a) Availability Zone
- b) Host groups
- c) Availability Set
- d) Placement Group

**E418.** Your business has an Azure subscription with resources spread across various locations. Administrators can use only those regions to build resources. Which of the following should you employ to ensure this?
- a) Management Group
- b) Read-Only Lock
- c) Azure Policy
- d) Reservation

**E419.** What purpose does a site-to-site VPN serve?
- a) Establishes a secure link between a computer connected to a public network and the company network
- b) Offers a private connection to Azure that is dedicated and DOES NOT use the Internet
- c) Establishes a connection between an Azure VPN gateway and an on-premises VPN device
- d) None of the above

**E420.** Container management is necessary. Which two services are available for use?
- a) Azure Virtual Machine
- b) Azure Kubernetes Service
- c) Azure Functions
- d) Azure Virtual Desktop
- e) Azure Container Instance

**E421.** The fact that high availability is a feature of the Azure SQL Data Warehouse platform is one of its advantages. True or False?
- a) True
- b) False

**E422.** You have an on-premises program that automatically sends email notifications under a rule. The application will be moved to Azure For the application, you must suggest a serverless computing solution What should the recommendation contain?
- a) Azure Logic App
- b) Azure Web App
- c) API App
- d) Server Image in Azure Marketplace

**E423.** A website will be deployed to Azure by you. Users from all over the world can visit the website, which will host big video files. Which Azure feature should be utilized to deliver the greatest video playback experience? Which of the following would you suggest?
- a) Application Gateway
- b) ExpressRoute Circuit
- c) Azure Traffic Manager Profile
- d) Content Delivery Network

**E424.** Your business intends to deploy millions of sensors that will provide data to Azure. Which Azure resources must be established to support the intended solution must be determined. Which two Azure resources are you supposed to name?
- a) Azure Queue Storage
- b) ExpressRoute Circuit
- c) Azure IoT Hub
- d) Azure File Storage
- e) Azure Data Lake

**E425.** You have a web app for Azure. The web app's settings must be managed from an iPhone. Which two Azure management tools are available for use?
- a) Azure Portal
- b) Azure Storage Explorer
- c) Azure CLI
- d) Azure Cloud Shell
- e) WindowsPowerShell

**E426.** Your business intends to deploy millions of sensors that will provide data to Azure. Which Azure resources must be established to support the intended solution. Which two Azure resources are you supposed to name?
- a) Azure Data Lake
- b) Azure Queue Storage
- c) Azure File Storage
- d) Azure Notification Hubs
- e) Azure IoT Hub

**E427.** Your business intends to use Azure to deploy an Artificial Intelligence (AI) solution. How should the business develop, test, and implement predictive analytics solutions?
- a) Azure Batch
- b) Azure Cosmos DB
- c) Azure Logic Apps
- d) Azure Machine Learning Designer

**E428.** What can you use to have an Azure virtual machine shutdown warning sent to you automatically?
- a) Azure Service Health
- b) Azure Monitor
- c) Azure Network Watcher
- d) Azure Advisor ANSWERS

### Answers — Section E (Batch 17)

| # | Answer | Explanation |
|---|---|---|
| E413 | **c** | A subscription is the first item you generate in Azure. An Azure subscription can be compared to an "Azure account." You are charged according to your subscription. A subscription is a contract with Microsoft for using one or more of its cloud platforms or services, for which fees depend on the number of users or cloud resources used. Office 365... |
| E414 | **a** | Big data streaming platform and event ingestion service Azure Event Hubs. Millions of events can be received and processed in a single second. Any real-time analytics provider or batching/storage adaptor can transform and store data supplied to an event hub. To obtain valuable insights, you may ingest, buffer, store, and process your stream in r... |
| E415 | **b** | The health of the Azure services and regions you are utilizing is shown to you personally through Azure Service Health. The authenticated Service Health experience understands which services and resources you use. This is the best location for information about outages, planned maintenance, and other health advisories that may impact your service. |
| E416 | **c** | Azure Marketplace is an online store with thousands of IT software applications and services created by top-tier tech firms. The software and services you require to develop new solutions and manage your cloud infrastructure can be found, tested, purchased, and deployed in Azure Marketplace. |
| E417 | **a** | Azure availability zones are geographically distinct areas within each Azure region that can withstand minor setbacks. Failures can include hardware and software issues to calamities like earthquakes, floods, and fires. Redundancy and logical isolation of Azure services allow for failure tolerance. All availability zone-enabled regions have a mi... |
| E418 | **c** | Azure Policy supports organizational standards enforcement and at-scale compliance evaluation. With the ability to drill down to the per-resource and perpolicy granularity, it offers an aggregated view for assessing the overall condition of the environment compliance dashboard. |
| E419 | **c** | Your on-premises network is linked to an Azure virtual network via an IPsec/IKE (IKEv1 or IKEv2) VPN tunnel using a site-to-site VPN gateway connection. This kind of connection requires a VPN device that is on-site and has been given a public IP address visible from the outside. |
| E420 | **b and e** | Run Docker containers as needed in a serverless, managed Azure environment. Azure Container Instances provides a solution for any situation that may run in separate containers without orchestration. Run eventdriven applications, carry out data processing, launch build jobs, and swiftly deploy from your container development pipelines. You can ma... |
| E421 | **b** | Microsoft's PaaS product is called Azure Data Warehouse, which is currently called Azure Synapse Analytics. Like all Microsoft PaaS services, SQL Data Warehouse has a 99.9% SLA for availability. Because its platform includes high availability features, Microsoft can guarantee 99.9% availability. |
| E422 | **a** | Azure When you need to integrate apps, data, systems, and services across businesses or organizations, Logic Apps is a cloud solution that can help you schedule, automate, and orchestrate tasks, business processes, and workflows. Whether in the cloud, on-premises, or both, Logic Apps makes it easier to design and develop scalable solutions for a... |
| E423 | **d** | Users worldwide will download big video files, according to the query. If people could download the video from servers in their home area, the video playback experience would be better. By utilizing a content delivery network, we can do this. A dispersed network of servers known as a Content Delivery Network (CDN) can deliver web material to use... |
| E424 | **c and e** | Data from millions of sensors is provided by IoT Hub (Internet of Things Hub). A managed service called IoT Hub is hosted in the cloud. It serves as a central messaging node for two-way communication between your IoT application and the devices it controls. Building IoT systems with dependable and secure connections between millions of IoT devic... |
| E425 | **a and d** | The web-based management portal for Azure is called the Azure portal. The Azure portal can be used on an iPhone because it is web-based. An online command-line called Azure Cloud Shell is used to manage Azure. The Azure portal is where you access the Azure Cloud Shell. The Azure Cloud Shell can be used on an iPhone because it is web-based. Optio... |
| E426 | **a and e** | Data from millions of sensors is provided by IoT Hub (Internet of Things Hub). A managed service called IoT Hub is hosted in the cloud. It serves as a central messaging node for two-way communication between your IoT application and the devices it controls. Building IoT systems with dependable and secure connections between millions of IoT devic... |
| E427 | **d** | You can graphically connect datasets and modules on an interactive canvas using Azure Machine Learning Designer to build machine learning models. |
| E428 | **b** | You can increase the availability and efficiency of your applications and services with the aid of Azure Monitor. With this comprehensive solution, the telemetry from your cloud and on-premises systems can be collected, analyzed, and used to take action. With this data, you may better comprehend how your apps operate and proactively spot problem... |

---

## Section F: ExamTopics Community Questions

> Questions from the ExamTopics AZ-900 discussion forums.

**F1.** Your company has datacenters in Los Angeles and New York. You are configuring the two datacenters as geo-clustered sites for site resiliency. You need to recommend an Azure storage redundancy option. You have the following data storage requirements: (1) Data must be stored on multiple nodes. (2) Data must be stored on nodes in separate geographic locations. (3) Data can be read from the secondary location as well as from the primary location. Which Azure storage redundancy option should you recommend?
- a) Geo-redundant storage (GRS)
- b) Read-access geo-redundant storage (RA-GRS)
- c) Zone-redundant storage (ZRS)
- d) Locally redundant storage (LRS)

**F2.** Your company intends to subscribe to an Azure support plan. The support plan must allow for new technical support requests to be opened. Which of the following support plans allow this? (Select all that apply)
- a) Basic
- b) Developer
- c) Standard
- d) Professional Direct
- e) Premier

**F3.** Your company's Azure subscription includes a Basic support plan. They would like to request an assessment of an Azure environment's design from Microsoft. This is, however, not supported by the existing plan. You want to make sure that the company subscribes to a support plan that allows this functionality, while keeping expenses to a minimum. Solution: You recommend that the company subscribes to the Professional Direct support plan. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F

| # | Answer | Explanation |
|---|---|---|
| F1 | **b** | All options store on multiple nodes (requirement 1). LRS and ZRS are single-region, so they fail requirement 2 (separate geographic locations). GRS replicates to a secondary region but the secondary is NOT readable before failover — fails requirement 3. Only RA-GRS (Read-Access Geo-Redundant Storage) meets all three: geo-replicated across regions AND readable from the secondary via the `-secondary` URL suffix. RA-GZRS would also work but is not listed. |
| F2 | **b, c, d, e** | Basic does NOT allow opening technical support tickets — only billing and subscription requests. Developer, Standard, Professional Direct, and Premier/Unified all allow opening technical support tickets. This is a common exam trap. |
| F3 | **b** | No. A formal assessment of an Azure environment's design (architecture review) requires **Premier/Unified Support** with a designated Technical Account Manager (TAM). Professional Direct offers advisory and proactive guidance but not formal design assessments. This "Does the solution meet the goal?" format appears in series on the exam — same scenario, different proposed solutions. |

**F4.** You are tasked with deploying Azure virtual machines for your company. You need to make use of the appropriate cloud deployment solution. Solution: You should make use of Software as a Service (SaaS). Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F4 | **b** | No. Azure Virtual Machines are **IaaS** (Infrastructure as a Service) — you rent the hardware and manage the OS and above. SaaS is a fully managed application you consume (e.g., Microsoft 365, Outlook). You cannot "deploy VMs" with SaaS because SaaS abstracts away all infrastructure. The correct answer in this scenario series would be IaaS. |

**F5.** *(Same series as F4)* You are tasked with deploying Azure virtual machines for your company. You need to make use of the appropriate cloud deployment solution. Solution: You should make use of Platform as a Service (PaaS). Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F5 | **b** | No. PaaS abstracts the OS and infrastructure — you deploy application code, not VMs. Azure VMs require **IaaS**, where you control the OS and above. PaaS examples: App Service, Azure SQL Database. In this question series, only IaaS meets the goal. |

**F6.** *(Same series as F4–F5)* You are tasked with deploying Azure virtual machines for your company. You need to make use of the appropriate cloud deployment solution. Solution: You should make use of Infrastructure as a Service (IaaS). Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F6 | **a** | Yes. Azure Virtual Machines are **IaaS** — you rent the hardware and manage the OS, middleware, and applications. IaaS is the correct service type for deploying VMs. This completes the series: SaaS (No) → PaaS (No) → **IaaS (Yes)**. |

**F7.** Your developers have created 10 web applications that must be hosted on Azure. The web tier plan must meet the following requirements: (1) The web apps will use custom domains. (2) The web apps each require 10 GB of storage. (3) The web apps must each run in dedicated compute instances. (4) Load balancing between instances must be included. (5) Costs must be minimized. Which web tier plan should you use?
- a) Standard
- b) Basic
- c) Free
- d) Shared

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F7 | **a** | Standard. Free and Shared use shared VMs (fail requirement 3) and have only 1 GB storage (fail requirement 2). Basic has dedicated instances and custom domains, but only 10 GB total storage (not enough for 10 apps × 10 GB) and lacks auto-scale/load balancing. Standard provides 50 GB storage, dedicated compute, custom domains, auto-scale with built-in load balancing, and is the cheapest tier meeting all five requirements. |

**F8.** You are planning to migrate a company to Azure. Each of the company's numerous divisions will have an administrator in place to manage the Azure resources used by their respective division. You want to make sure that the Azure deployment allows for Azure to be segmented for the divisions, while keeping administrative effort to a minimum. Solution: You plan to make use of several Azure Active Directory (Azure AD) directories. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F8 | **b** | No. Multiple Azure AD (Entra ID) directories would **increase** administrative effort — you'd have to manage users, policies, and sync across each directory separately. The correct approach is to use **Management Groups** or **multiple Subscriptions** within a single Entra ID tenant, with RBAC to give each division's admin the right scope. This segments resources while minimizing overhead. |

**F9.** Your developers have created a portal web app for users in the Miami branch office. You plan to host the web app on Azure. The web tier plan must meet the following requirements: (1) The website will use the miami.weyland.com URL. (2) The website will be deployed to two instances. (3) SSL support must be included. (4) The website requires 12 GB of storage. (5) Costs must be minimized. Which web tier plan should you use?
- a) Standard
- b) Basic
- c) Free
- d) Shared

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F9 | **a** | Standard. Free and Shared lack SSL, dedicated instances, and have only 1 GB storage. Basic supports custom domains, SSL, and up to 3 instances — but only has **10 GB storage**, which is less than the 12 GB required. Standard provides 50 GB storage, SSL, custom domains, up to 10 instances, and is the cheapest tier meeting all five requirements. |

**F10.** Your company is planning to migrate all their virtual machines to an Azure pay-as-you-go subscription. The virtual machines are currently hosted on the Hyper-V hosts in a data center. You are required to make sure that the intended Azure solution uses the correct expenditure model. Solution: You should recommend the use of the elastic expenditure model. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F10 | **b** | No. "Elastic expenditure model" does not exist as a cloud pricing concept — elasticity describes auto-scaling behavior, not a spending model. Migrating from on-prem Hyper-V to Azure pay-as-you-go shifts spending from **CapEx** (upfront hardware) to **OpEx** (Operational Expenditure — pay for what you use). The correct answer in this series would be OpEx. |

**F11.** *(Same series as F10)* Your company is planning to migrate all their virtual machines to an Azure pay-as-you-go subscription. The virtual machines are currently hosted on the Hyper-V hosts in a data center. You are required to make sure that the intended Azure solution uses the correct expenditure model. Solution: You should recommend the use of the scalable expenditure model. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F11 | **b** | No. "Scalable expenditure model" does not exist — scalability is a cloud capability, not a spending model. The two expenditure models are **CapEx** (upfront) and **OpEx** (pay-as-you-go). Azure pay-as-you-go = OpEx. In this series: elastic (No) → scalable (No) → the correct answer is **OpEx**. |

**F12.** *(Same series as F10–F11)* Your company is planning to migrate all their virtual machines to an Azure pay-as-you-go subscription. The virtual machines are currently hosted on the Hyper-V hosts in a data center. You are required to make sure that the intended Azure solution uses the correct expenditure model. Solution: You should recommend the use of the operational expenditure model. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F12 | **a** | Yes. Azure pay-as-you-go is **OpEx** (Operational Expenditure) — you pay for resources as you consume them, no upfront hardware investment. This completes the series: elastic (No, not a real model) → scalable (No, not a real model) → **operational (Yes, OpEx = pay-as-you-go)**. |

**F13.** You are required to deploy an Artificial Intelligence (AI) solution in Azure. You want to make sure that you are able to build, test, and deploy predictive analytics for the solution. Solution: You should make use of Azure Cosmos DB. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F13 | **b** | No. Azure Cosmos DB is a globally distributed **NoSQL database** — it stores data, not builds AI models. To build, test, and deploy predictive analytics, you need **Azure Machine Learning**, which provides the full ML lifecycle (experimentation, training, deployment). Azure AI Services would also be wrong here — those are prebuilt APIs, not custom model building. |

**F14.** Your company's Active Directory forest includes thousands of user accounts. You have been informed that all network resources will be migrated to Azure. Thereafter, the on-premises data center will be retired. You are required to employ a strategy that reduces the effect on users, once the planned migration has been completed. Solution: You plan to sync all the Active Directory user accounts to Azure Active Directory (Azure AD). Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F14 | **a** | Yes. Syncing on-prem AD accounts to Azure AD (Entra ID) via **Microsoft Entra Connect** preserves user identities, credentials, and SSO experience. When the on-prem datacenter is retired, users already have their accounts in the cloud — minimal disruption. This is exactly what Entra Connect is designed for. |

**F15.** *(Same series as F13)* You are required to deploy an Artificial Intelligence (AI) solution in Azure. You want to make sure that you are able to build, test, and deploy predictive analytics for the solution. Solution: You should make use of Azure Machine Learning Studio. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F15 | **a** | Yes. Azure Machine Learning Studio (now part of Azure Machine Learning) provides the full ML lifecycle: build, train, test, and deploy predictive models. This is the correct service for predictive analytics. Compare with F13 where Cosmos DB (a database) was incorrect for this same scenario. |

**F16.** Your company's infrastructure includes a number of business units that each need a large number of various Azure resources for everyday operation. The resources required by each business unit are identical. You are required to sanction a strategy to create Azure resources automatically. Solution: You recommend that the Azure API Management service be included in the strategy. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F16 | **b** | No. Azure API Management is for publishing, securing, and managing APIs — it does not create or deploy Azure resources. To automatically create identical resources across business units, use **ARM templates** or **Bicep** (Infrastructure as Code). These are declarative, reusable, and idempotent — deploy the same template per business unit for identical results. |

**F17.** *(Same series as F16)* Your company's infrastructure includes a number of business units that each need a large number of various Azure resources for everyday operation. The resources required by each business unit are identical. You are required to sanction a strategy to create Azure resources automatically. Solution: You recommend that management groups be included in the strategy. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F17 | **b** | No. Management Groups organize subscriptions and apply governance (policies, RBAC) at scale — they do not create resources. To automatically create identical resources, use **ARM templates** or **Bicep**. In this series: API Management (No, manages APIs) → Management Groups (No, organizes subscriptions) → the correct answer is ARM templates/Bicep. |

**F18.** *(Same series as F16–F17)* Your company's infrastructure includes a number of business units that each need a large number of various Azure resources for everyday operation. The resources required by each business unit are identical. You are required to sanction a strategy to create Azure resources automatically. Solution: You recommend that the Azure Resource Manager templates be included in the strategy. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F18 | **a** | Yes. ARM templates are declarative JSON files (IaC) that define Azure resources for automated, repeatable deployment. Deploy the same template per business unit → identical resources every time. They are idempotent and reusable. This completes the series: API Management (No) → Management Groups (No) → **ARM templates (Yes)**. |

**F19.** You are tasked with deploying a critical LOB application, which will be installed on a virtual machine, to Azure. You are informed that the application deployment strategy should allow for a guaranteed availability of 99.99 percent. You need to make sure that the strategy requires as little virtual machines and availability zones as possible. Solution: You include two virtual machines and one availability zone in your strategy. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F19 | **b** | No. Two VMs in ONE availability zone only provides Availability Set-level protection (99.95% SLA). For 99.99% SLA, VMs must be deployed across **at least 2 availability zones**. The minimum solution is 2 VMs × 2 availability zones. SLA ladder: Single VM (Premium SSD) = 99.9% → Availability Set = 99.95% → Availability Zones = 99.99%. |

**F20.** *(Same series as F19)* You are tasked with deploying a critical LOB application, which will be installed on a virtual machine, to Azure. The strategy should allow for a guaranteed availability of 99.99 percent with as few VMs and availability zones as possible. Solution: You include one virtual machine and two availability zones in your strategy. Does the solution meet the goal?
- a) Yes
- b) No

### Answers — Section F (continued)

| # | Answer | Explanation |
|---|---|---|
| F20 | **b** | No. A single VM cannot span two availability zones — it lives in one zone and is a single point of failure. You need at least **2 VMs across 2 availability zones** for the 99.99% SLA. In this series: 2 VMs × 1 zone (No, only 99.95%) → 1 VM × 2 zones (No, impossible/single point of failure) → the correct answer is 2 VMs × 2 zones. |

**F21.** To transition from CapEx to OpEx, Contoso's CIO suggests moving VM workloads to Azure. The CFO argues this will result in unpredictable OpEx spending. What pricing option reduces costs and makes predicting future spending easier?
- a) Azure Reservations
- b) Pay-as-you-go (PAYG)
- c) Azure VM Scale Sets
- d) Azure in CSP

**F22.** Tailspin Toys, a small startup, chooses to rely on Office 365 and Microsoft Azure for all services. Which cloud model have they chosen?
- a) Private Cloud
- b) Public Cloud
- c) Hybrid Cloud
- d) Government Cloud

**F23.** Which of the following statements are true of a Software as a Service solution?
- a) You are responsible for maintaining the solution infrastructure
- b) You are responsible for deploying updates to the solution
- c) You are responsible for solution availability and scalability
- d) You are responsible for configuring the solution features

**F24.** Contoso currently hosts business applications in a shared virtualization infrastructure on-premises, utilizing Hyper-V. This is an example of which cloud computing model?
- a) Hybrid Cloud
- b) Private Cloud
- c) Public Cloud
- d) Government Cloud

**F25.** Azure SQL Database and an on-premises SQL cluster represent a(n) ___ expense and a(n) ___ expense, respectively.
- a) Capital, Capital
- b) Capital, Operational
- c) Operational, Operational
- d) Operational, Capital

**F26.** In Azure, you are charged only for what you use. This is known as a
- a) Fixed-price model
- b) Consumption based model

**F27.** Contoso runs several business applications in Azure VMs. Which cloud computing model best categorizes Azure VMs?
- a) Software as a service (SaaS)
- b) Platform as a service (PaaS)
- c) Infrastructure as a service (IaaS)
- d) Function as a service (FaaS)

**F28.** Azure App Service, Azure SQL Database, and Cosmos DB are examples of which category of cloud computing service?
- a) Function as a Service (FaaS)
- b) Software as a Service (SaaS)
- c) Platform as a Service (PaaS)
- d) Infrastructure as a Service (IaaS)

**F29.** You need to provide additional capacity beyond your on-premises datacenter. The solution must minimize capital expense (CapEx) and operational expense (OpEx). Which solution should you recommend?
- a) Migration to public cloud
- b) A private cloud
- c) A hybrid cloud
- d) Additional on-premises servers

**F30.** Office 365, Azure VMs, and Event Grid represent, _____, _____, and _____, respectively.
- a) SaaS, PaaS, IaaS
- b) PaaS, IaaS, SaaS
- c) SaaS, IaaS, PaaS

**F31.** Contoso hosts databases for customer-facing web applications in Azure MySQL Database. Which cloud computing model best categorizes this service?
- a) Software as a service (SaaS)
- b) Platform as a service (PaaS)
- c) Infrastructure as a service (IaaS)
- d) Function as a service (FaaS)

**F32.** Contoso hosts a legacy CRM on an Azure VM scale set. It runs at 30% utilization normally but spikes to 90% during month-end. Azure allows Contoso to meet these spikes, paying for additional capacity only when needed. This is an example of:
- a) Scalability
- b) Elasticity
- c) Fault Tolerance
- d) High Availability

**F33.** Contoso plans to migrate their existing on-premises SQL VMs to Azure. Which expenditure model does this implement?
- a) Capital (CAPEX)
- b) Operational (OPEX)
- c) Subscription
- d) Elastic

**F34.** A financial analysis showed that storing 2TB of archived data in Azure would be less expensive than on-premises. The report also showed unit cost would decrease further as the archive grows. This is an example of cloud
- a) Elasticity
- b) Economies of scale
- c) Scalability
- d) High Availability

**F35.** Contoso Financial Services needs to automate business processes in a low-code environment with a visual interface, with built-in connectivity to SalesForce and SAP. The team members are citizen developers. Which service best fits?
- a) Power Automate
- b) Logic Apps
- c) Azure Automation
- d) Azure Functions

**F36.** Kelly in IT Operations wants to automate a task using a script she wrote, with minimum expense and maintenance effort. She selected Azure Functions instead of Azure VMs (IaaS). Does this service meet the solution criteria?
- a) Yes
- b) No

**F37.** Contoso has a line-of-business application that requires access to a file share. You need to host this share in Azure with minimum cost and administration effort. Which service would best fulfill this requirement?
- a) Azure Files
- b) Azure Blob Storage
- c) Azure VMs
- d) VM Scale Sets

**F38.** Contoso IT needs to ensure deployments of like Azure resources are the same for every deployment. Which of the following could be used to automate resource deployment?
- a) Azure API Management
- b) Management Groups
- c) Azure Resource Manager (ARM) templates
- d) Azure Synapse

**F39.** You are testing new software in an Azure VM. When you are done testing, you shut down the VM, which shows a state of "Stopped" in the Azure portal. Will you incur additional costs while the VM is in this state?
- a) Yes
- b) No

**F40.** You are deploying multiple instances of a custom Contoso web application. The instances share a common management lifecycle, but will be located in different Azure regions. Can you deploy resources across multiple Azure regions in a single resource group?
- a) Yes
- b) No

**F41.** You are responsible for recommending infrastructure architectures for applications at Contoso. Which solution would you recommend for on-demand execution of automated tasks in Python for minimum expense?
- a) Azure Monitor
- b) Azure Cloud Shell
- c) Azure Automation
- d) Azure Functions

**F42.** Which Azure service would you use to correlate events from multiple Azure resources in a central repository?
- a) Azure Data Lake
- b) Azure Log Analytics
- c) Azure Event Grid
- d) Azure Event Hub

**F43.** An _____ protects against datacenter-level failures.
- a) Availability Set
- b) Availability Zone
- c) VM scale set
- d) Azure VM

**F44.** Contoso has messages from a variety of sources (many Azure services) that need to be relayed to an application. Which Azure service would be best suited?
- a) Azure Functions
- b) Azure Event Grid
- c) Azure IoT Hub
- d) Azure Service Bus

**F45.** You can monitor health and availability of your Azure Kubernetes Service (AKS) cluster with:
- a) Azure Monitor
- b) Azure App Insights
- c) Microsoft Sentinel
- d) Microsoft Defender for Cloud

**F46.** Which storage tier in Azure Storage delivers the highest cost of data storage?
- a) Hot
- b) Cool
- c) Cold
- d) Archive

**F47.** Contoso is planning to move several SQL databases to Azure SQL Database. The CIO has asked for a tool to estimate the cost of hosting these resources in Azure. Sally suggests using the Azure Pricing Calculator. Does Sally's solution meet the criteria?
- a) Yes
- b) No

**F48.** Which storage tier in Azure Storage delivers the lowest cost of data storage?
- a) Hot
- b) Cool
- c) Cold
- d) Archive

**F49.** You have a mobile application that exchanges large numbers of messages with customer devices. Which Azure storage type is optimized for storing large numbers of messages, accessible from anywhere via authenticated HTTP or HTTPS calls?
- a) Blob Storage
- b) Queue Storage
- c) Table Storage
- d) File Storage

**F50.** Contoso's Security team wants to apply policy-based configuration across deployments in multiple Azure subscriptions. Which of the following can help achieve this?
- a) Resource Groups
- b) Management Groups
- c) Role Based Access Control (RBAC)
- d) Access Policies

**F51.** Contoso plans to implement a hybrid cloud architecture. They need to connect on-premises application resources. The solution should minimize latency and maximize security. Which option should they choose?
- a) Point-to-Site VPN
- b) Site-to-Site VPN
- c) ExpressRoute
- d) Azure Application Gateway

**F52.** As part of a hybrid cloud deployment, you need to connect Contoso's on-premises datacenter to Azure. The solution should minimize expense during the low-scale pilot deployment. Which option will you choose?
- a) Point-to-Site VPN
- b) Site-to-Site VPN
- c) ExpressRoute
- d) Azure Application Gateway

**F53.** For regulatory compliance, you need to ensure Contoso's corporate web apps use TLS 1.2 for encryption. Does Azure App Service support enforcing this specific requirement?
- a) Yes
- b) No

**F54.** Contoso wants to migrate a legacy application that requires an SMB file share accessible on a UNC path. The solution should minimize administrative effort. Which service will you use?
- a) OneDrive
- b) SharePoint
- c) Azure VM with a file share
- d) Azure Files

**F55.** Storage for Azure VMs is hosted in which Azure Storage type?
- a) File
- b) Table
- c) Disk
- d) Blob

**F56.** Contoso IT wants to configure separate Azure subscriptions for different environments (production, development, test) and products. Can they associate multiple Azure subscriptions to the same Entra ID tenant?
- a) Yes
- b) No

**F57.** Contoso Financial Services regularly creates documents containing sensitive customer data, including personally identifiable information. You need to ensure access is restricted to finance personnel, regardless of where the document travels. Which service should you use to classify and protect these documents?
- a) Microsoft Defender for Cloud Apps
- b) Microsoft Defender for Endpoint
- c) Microsoft Purview
- d) Entra ID Conditional Access

### Answers — Section F (Batch 2)

| # | Answer | Explanation |
|---|---|---|
| F21 | **a** | Azure Reservations provide 1-3 year commitments at up to 72% discount — predictable costs and savings vs. PAYG. VM Scale Sets handle scaling, not pricing. |
| F22 | **b** | Office 365 and Azure are public cloud services — shared infrastructure, multi-tenant, pay-as-you-go. |
| F23 | **d** | In SaaS, the provider manages infrastructure, updates, availability, and scalability. You only configure features and manage your data/identity. |
| F24 | **b** | On-premises Hyper-V with shared virtualization = Private Cloud — dedicated infrastructure for a single organization. |
| F25 | **d** | Azure SQL Database = cloud = OpEx (pay-as-you-go). On-premises SQL cluster = physical hardware = CapEx (upfront investment). |
| F26 | **b** | Pay only for what you use = consumption-based model. This is the fundamental cloud pricing principle. |
| F27 | **c** | Azure VMs = IaaS. You rent the hardware and manage the OS and above. |
| F28 | **c** | App Service, SQL Database, and Cosmos DB are all PaaS — provider manages infrastructure, you manage app code and data. |
| F29 | **c** | Hybrid cloud minimizes both CapEx (burst to public cloud instead of buying hardware) and OpEx (keep existing on-prem for baseline). Public cloud alone wouldn't minimize OpEx for the existing on-prem workload. |
| F30 | **c** | Office 365 = SaaS (you use the app), Azure VMs = IaaS (you manage the OS), Event Grid = PaaS (serverless event routing). |
| F31 | **b** | Azure MySQL Database is a managed database service = PaaS. Provider handles OS, patching, backups. |
| F32 | **b** | Elasticity = automatically scale up/down based on demand. Scalability is the general ability to handle growth; elasticity is the automatic response to spikes. |
| F33 | **b** | Moving to Azure = pay-as-you-go = OpEx (Operational Expenditure). On-prem hardware = CapEx. |
| F34 | **b** | Unit cost decreases as scale increases = economies of scale. Cloud providers pass savings from massive scale to customers. |
| F35 | **a** | Power Automate = low-code, visual interface, built-in connectors (SalesForce, SAP), designed for citizen developers. Logic Apps is similar but more developer-oriented. |
| F36 | **a** | Yes. Functions are serverless — pay per execution, no VM management, ideal for running scripts with minimum expense and maintenance. |
| F37 | **a** | Azure Files = fully managed SMB file share. Lower cost and admin effort than running a VM with a file share. |
| F38 | **c** | ARM templates are declarative IaC — define resources once, deploy identically every time. Idempotent and repeatable. |
| F39 | **a** | Yes. A "Stopped" VM (not deallocated) still incurs costs for storage (VM disks). To fully stop billing, you must **deallocate** the VM. |
| F40 | **a** | Yes. A resource group is a logical container — resources in it can be in different Azure regions. The resource group itself has a location (for metadata only). |
| F41 | **d** | Azure Functions = serverless, on-demand execution, pay-per-use, supports Python. Cheapest option for automated task execution. |
| F42 | **b** | Azure Log Analytics (part of Azure Monitor) is the central repository for querying and correlating logs from multiple Azure resources using KQL. |
| F43 | **b** | Availability Zone = physically separate datacenter within a region. Protects against datacenter-level failures. Availability Set protects against rack-level failures within one datacenter. |
| F44 | **b** | Azure Event Grid = pub/sub event routing from multiple sources to applications. Designed for reactive event-driven architectures. |
| F45 | **a** | Azure Monitor provides container insights for monitoring AKS health and availability. App Insights monitors web apps, not K8s clusters. |
| F46 | **a** | Hot tier = highest storage cost but lowest access cost. Designed for frequently accessed data. |
| F47 | **a** | Yes. The Azure Pricing Calculator estimates costs before deployment — exactly what the CIO needs. |
| F48 | **d** | Archive = lowest storage cost but highest access cost and latency (offline, requires rehydration). Min retention 180 days. |
| F49 | **b** | Queue Storage stores large numbers of messages accessible via HTTP/HTTPS. Designed for asynchronous message processing between app components. |
| F50 | **b** | Management Groups sit above subscriptions and allow applying policies and RBAC across multiple subscriptions at once. |
| F51 | **c** | ExpressRoute = dedicated private connection, lowest latency, highest security (no public internet). Best for performance + security requirements. |
| F52 | **b** | Site-to-Site VPN = encrypted tunnel over internet, lower cost than ExpressRoute. Best for pilot/small-scale hybrid deployments. |
| F53 | **a** | Yes. Azure App Service supports enforcing minimum TLS version (1.0, 1.1, 1.2) in its configuration settings. |
| F54 | **d** | Azure Files = fully managed SMB file share, accessible via UNC path. Minimum admin effort compared to managing a VM with a share. |
| F55 | **c** | Azure Disk Storage (managed disks) hosts VM OS and data disks. Available as HDD, Standard SSD, or Premium SSD. |
| F56 | **a** | Yes. Multiple Azure subscriptions can be associated with the same Entra ID tenant. This is the standard way to segment environments (prod, dev, test). |
| F57 | **c** | Microsoft Purview classifies and protects sensitive data (including PII) with sensitivity labels that travel with the document regardless of location. |

**F58.** An Azure _____ is a set of datacenters deployed within a latency-defined perimeter and connected through a dedicated regional low-latency network.
- a) Availability Zone
- b) Region
- c) Geography
- d) Datacenter

**F59.** Which Azure storage redundancy option does Microsoft recommend for maximum redundancy and recoverability?
- a) LRS
- b) GRS
- c) ZRS
- d) Geo Zone Redundant Storage (GZRS)

**F60.** An _____ protects against VM failures due to failures in updates, power, or network connectivity.
- a) Availability Set
- b) Availability Zone
- c) VM scale set
- d) Azure VM

**F61.** You need to manage your Azure VMs using the Azure portal. Which URL would you use?
- a) https://portal.azurewebsites.net
- b) https://portal.microsoft.com
- c) https://portal.azure.microsoft.com
- d) https://portal.azure.com

**F62.** Contoso IT wants to develop modern application components using a serverless architecture. Which Azure service is best for hosting code as part of a services infrastructure?
- a) Azure Logic Apps
- b) Azure Functions
- c) Azure Service Bus
- d) Azure Automation

**F63.** You can monitor health and performance of microservices applications running on Azure Kubernetes Service (AKS) with:
- a) Azure Monitor
- b) Azure App Insights
- c) Azure Sentinel
- d) Microsoft Defender for Cloud

**F64.** You need to store unstructured data, such as images, video files, social media posts on Azure Storage. Which type is optimized for large amounts of unstructured data?
- a) Table Storage
- b) Queue Storage
- c) Disk Storage
- d) Blob Storage

**F65.** Contoso IT has deployed a group of Azure VMs for hosting production. They want best practices recommendations for high availability. Will Azure Advisor provide recommendations for these existing resources?
- a) Yes
- b) No

**F66.** The Contoso IT Operations team needs to monitor their customer-facing web apps for performance anomalies. Which Azure service will best fulfill this need?
- a) Azure WebJobs
- b) Azure Application Insights
- c) Azure Automation
- d) Azure Sentinel

**F67.** You need to automate responses to some alerts from Azure Monitor. Which service supports automating responses and corrective actions?
- a) Power Automate
- b) Azure Logic Apps
- c) Azure Web Jobs
- d) Azure Automation

**F68.** The Contoso IT Operations team needs to aggregate events from a large number of resources hosted in Azure for correlation, alerting, and reporting. Which Azure service would you use to centrally collect, store, and act on events?
- a) Azure App Insights
- b) Azure Monitor
- c) Azure Data Lake
- d) Azure Event Hub

**F69.** You need to alert on service failures in your Azure services, such as web app instances hosted in App Service, and Azure VMs that stop running. Which tool should you use?
- a) Azure App Insights
- b) Azure Log Analytics
- c) Azure Monitor
- d) Microsoft Defender for Cloud

**F70.** You can find recommendations for security best practices and security configuration for Azure Kubernetes Service (AKS) with:
- a) Azure Monitor
- b) Azure App Insights
- c) Microsoft Sentinel
- d) Microsoft Defender for Cloud

**F71.** Azure VMs in different virtual networks can communicate by default.
- a) True
- b) False

**F72.** Which Microsoft solution provides support for passwordless authentication on Windows 10 and 11 systems?
- a) Entra ID Conditional Access
- b) Microsoft Authenticator
- c) Windows Hello for Business
- d) Microsoft Purview

**F73.** You have deployed an Azure VM hosting a LOB web application. You need to provide access over the Internet via HTTP/S. You add a security rule to the NSG to allow inbound traffic from the Internet. Does this solution meet the requirement?
- a) Yes
- b) No

**F74.** Contoso IT has deployed multiple Azure VMs across 15 virtual networks. How can you most securely limit inbound traffic and protect these VMs from unwanted inbound requests?
- a) Create a network security group (NSG)
- b) Deploy an Azure Firewall
- c) Deploy an Azure Load Balancer
- d) Deploy a virtual network gateway

**F75.** You need to define and enforce corporate standards for new and existing Azure resource deployments in all of Contoso's Azure subscriptions. What should you use?
- a) Azure Policy
- b) Microsoft Defender for Cloud
- c) Microsoft Sentinel
- d) Azure Advisor

**F76.** Tailspin Toys relies heavily on Entra ID for cloud identity. They want to more effectively protect their identities from external threats. Which service should they choose?
- a) Azure Identity Protection
- b) Microsoft Defender for Endpoint
- c) Azure DDoS
- d) Microsoft Information Protection

**F77.** In a Site-to-Site VPN, the ___ is the cross-premises gateway that connects your Azure Virtual Network with your on-premises VPN appliances.
- a) Azure Application Gateway
- b) Azure Virtual Network Gateway
- c) Local Network Gateway
- d) Private Endpoint

**F78.** You need to prevent accidental deletion of Azure resources in your subscription. Which feature will meet this requirement?
- a) RBAC
- b) Resource Locks
- c) Security groups
- d) Azure policies

**F79.** You are creating Azure resources using ARM templates. You need to ensure resources are only created in approved regions. What should you use to enforce this?
- a) Azure locks
- b) Azure Policy
- c) Azure Blueprint
- d) Microsoft Defender for Cloud

**F80.** Contoso IT assigns permissions at the resource group level. Will resources in the resource group inherit these permissions?
- a) Yes
- b) No

**F81.** Contoso has implemented a hybrid, synchronized identity model (on-prem AD + Entra ID). They want to more effectively protect their on-premises identities from external threats. Which service should they choose?
- a) Azure Identity Protection
- b) Microsoft Defender for Endpoint
- c) Azure DDoS
- d) Microsoft Information Protection

**F82.** You need to implement MFA for your Entra ID users, but only prompt for an additional factor when users are not in a trusted location on an unmanaged device. Which feature should you implement?
- a) Microsoft Purview
- b) Identity Protection
- c) Conditional Access
- d) Privileged Identity Management

**F83.** When users connect from outside corporate offices, they must be prompted for MFA. Which feature will you implement?
- a) Entra ID Privileged Identity Management
- b) One Time Passwords (OTP)
- c) Entra ID Identity Protection
- d) Entra ID Conditional Access

**F84.** You need to support OATH tokens (one-time password) as a second authentication factor for Entra ID. Which Microsoft solution enables OATH tokens?
- a) Entra ID Identity Protection
- b) Microsoft Authenticator
- c) Conditional Access
- d) Entra ID Multi-Factor Authentication

**F85.** The Contoso Legal Department has asked IT to verify whether Contoso's Azure environment meets regulatory requirements. Which service should you use?
- a) Azure Advisor
- b) Microsoft Defender for Cloud
- c) Microsoft Purview
- d) Azure Policy

**F86.** What are the three foundational principles of Zero Trust?
- a) Verify explicitly, Use least privilege access, Assume breach
- b) Verify explicitly, Use defense in depth, Assume breach
- c) Verify explicitly, Trust but verify, Assume breach
- d) Verify explicitly, Use least privilege access, Trust must be earned

**F87.** Contoso needs to simplify deployments of new environments including ARM templates, role-based access, and policies. Which Azure service enables repeatable deployment and configuration of new subscriptions and environments?
- a) Azure Policy initiatives
- b) Azure Policy
- c) ARM templates
- d) Azure Blueprints

**F88.** Your company wants to leverage Entra ID but still support on-premises AD identities. Can you support SSO and MFA for both on-premises and cloud with Entra ID?
- a) Yes
- b) No

**F89.** You need to configure access to Office 365 resources. To group users for assignment of permissions, which option would you use?
- a) Microsoft 365 group
- b) Resource group
- c) Security group
- d) Management group

**F90.** Implementing Azure MFA will ensure we know who the user is who they claim to be. This is an example of:
- a) Authorization
- b) Authentication
- c) Integrity
- d) Confidentiality

**F91.** You need to ensure on-premises file shares and Azure Files remain in sync in both directions, regardless of where the file was changed. Which tool would you choose?
- a) AzCopy
- b) Azure Storage Explorer
- c) Azure File Sync
- d) Azure Data Box

**F92.** Contoso's Security team wants to implement selective use of MFA based on multiple factors related to the authentication request, such as device health and sign-in risk. Which services should they implement?
- a) Conditional Access and Identity Protection
- b) Identity Protection and Entitlement Management
- c) MFA and Identity Protection
- d) Windows Hello for Business and Conditional Access

**F93.** Contoso has deployed resources across multiple Azure regions for multiple business units. They need to generate cost and chargeback reporting to track Azure costs charged back to each business unit. Which Azure feature should they use?
- a) Tags
- b) Resource Locks
- c) Resource Groups
- d) Management Groups

### Answers — Section F (Batch 3)

| # | Answer | Explanation |
|---|---|---|
| F58 | **b** | An Azure Region = set of datacenters within a latency-defined perimeter connected by a dedicated low-latency network. Availability Zones are physically separate buildings within a region. |
| F59 | **d** | GZRS (Geo-Zone-Redundant Storage) combines ZRS in the primary region (3 zones) + GRS replication to a secondary region = maximum redundancy (16 nines durability). |
| F60 | **a** | Availability Set distributes VMs across fault domains (power/network) and update domains (patching). Protects against rack-level and update failures within a datacenter. Availability Zone protects against datacenter-level failures. |
| F61 | **d** | The Azure portal URL is https://portal.azure.com. Know this for the exam. |
| F62 | **b** | Azure Functions = serverless code execution. Logic Apps = workflow orchestration (low-code). Service Bus = messaging. Automation = runbooks for IT tasks. |
| F63 | **b** | App Insights monitors application performance including microservices on AKS. Azure Monitor monitors infrastructure-level health. Note: Q25 (F45) asked about AKS health/availability = Monitor; this asks about microservices performance = App Insights. |
| F64 | **d** | Blob Storage is optimized for massive amounts of unstructured data (images, videos, documents, social media). |
| F65 | **a** | Yes. Azure Advisor evaluates existing deployed resources and provides recommendations across Reliability, Security, Performance, Operational Excellence, and Cost. |
| F66 | **b** | Application Insights monitors web app performance and detects anomalies automatically. It's an Azure Monitor feature designed specifically for web applications. |
| F67 | **d** | Azure Automation supports runbooks that can be triggered by Azure Monitor alerts for automated corrective actions (e.g., restart a VM, scale resources). |
| F68 | **b** | Azure Monitor centrally collects, stores, and acts on events from Azure resources. It includes Log Analytics for querying and Alerts for acting on conditions. |
| F69 | **c** | Azure Monitor provides alerts for service failures across resource types (App Service, VMs, etc.). App Insights focuses on web apps only; Log Analytics is for querying, not alerting. |
| F70 | **d** | Microsoft Defender for Cloud provides security recommendations and best practices for Azure resources including AKS. Azure Monitor/App Insights focus on performance, not security config. |
| F71 | **b** | False. VMs in different VNets cannot communicate by default — VNets are isolated. You need VNet Peering or a VPN Gateway to connect them. |
| F72 | **c** | Windows Hello for Business provides passwordless authentication on Windows 10/11 using biometrics or PIN tied to the device. Authenticator is for mobile; FIDO2 is for external keys. |
| F73 | **a** | Yes. Adding an inbound NSG rule for HTTP (80) and HTTPS (443) from the Internet will allow web traffic to reach the VM. NSGs control network traffic at the NIC or subnet level. |
| F74 | **b** | Azure Firewall is a centralized, managed network firewall that protects across multiple VNets. NSGs work per-subnet/NIC — managing them across 15 VNets is complex. Firewall provides centralized control. |
| F75 | **a** | Azure Policy defines and enforces standards across all Azure resource deployments. It evaluates existing and new resources against your rules. |
| F76 | **a** | Azure Identity Protection detects identity-based threats (risky sign-ins, leaked credentials) and automates risk remediation for Entra ID identities. |
| F77 | **b** | Azure Virtual Network Gateway is the Azure-side cross-premises gateway for S2S VPN connections. The Local Network Gateway represents the on-premises VPN device. |
| F78 | **b** | Resource Locks (Delete or ReadOnly) prevent accidental deletion regardless of RBAC permissions. Even Owners must remove the lock first. |
| F79 | **b** | Azure Policy with an "Allowed locations" policy definition restricts resource creation to approved regions only. Locks prevent deletion, not location control. |
| F80 | **a** | Yes. RBAC permissions are inherited downward: Management Group → Subscription → Resource Group → Resources. Permissions assigned at RG level apply to all resources within. |
| F81 | **b** | Microsoft Defender for Endpoint protects on-premises servers and endpoints from threats. Azure Identity Protection focuses on cloud identities in Entra ID, not on-prem AD directly. |
| F82 | **c** | Conditional Access creates policies based on conditions (location, device state, risk level) to control when additional authentication is required. |
| F83 | **d** | Entra ID Conditional Access with a location-based policy can require MFA when users connect from outside corporate (trusted) locations. |
| F84 | **b** | Microsoft Authenticator app supports OATH TOTP tokens as a second factor. It works with Entra ID and other identity providers. |
| F85 | **b** | Microsoft Defender for Cloud provides a regulatory compliance dashboard that checks your Azure environment against industry standards (ISO, PCI DSS, SOC, etc.). |
| F86 | **a** | Zero Trust's three principles: 1) Verify explicitly (always authenticate/authorize), 2) Use least privilege access (JIT/JEA), 3) Assume breach (minimize blast radius). |
| F87 | **d** | Azure Blueprints bundle ARM templates, RBAC, policies, and resource groups into a reusable, versioned package for repeatable environment deployment. |
| F88 | **a** | Yes. Entra ID Cloud Sync (or Entra Connect) synchronizes on-prem AD with Entra ID, enabling SSO and MFA across both environments. |
| F89 | **c** | Security groups in Entra ID are used to group users and assign permissions to resources (including O365). Resource groups organize Azure resources; Management groups organize subscriptions. |
| F90 | **b** | Authentication = verifying identity ("who are you?"). MFA adds extra verification factors. Authorization = "what can you do?" after identity is confirmed. |
| F91 | **c** | Azure File Sync provides bidirectional sync between on-prem file shares and Azure Files. AzCopy is one-way copy; Storage Explorer is a GUI tool; Data Box is for offline bulk transfer. |
| F92 | **a** | Conditional Access defines the policies (when to require MFA based on conditions), and Identity Protection evaluates risk signals (device health, sign-in risk) that feed into those policies. |
| F93 | **a** | Tags (name-value pairs like "BusinessUnit:Finance") enable cost tracking and chargeback reporting. Filter Cost Analysis by tags to see spending per business unit. |

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

## Section H — Scott Duffy Practice Test

> **Source**: Scott Duffy — AZ-900 Udemy Course Practice Test (50 scenario-based questions)

**H1.** Your organization is deploying a web application to Azure. The application must be accessible to users worldwide over the internet without requiring a VPN connection or private network configuration. Which cloud deployment model best describes this accessibility requirement?

- A) Hybrid cloud
- B) Private cloud
- C) Community cloud
- D) Public cloud

**H2.** IT manager wants automatic email notification when CPU on VMs exceeds 85% for 5+ minutes. Which Azure Monitor capability?

- A) Azure Monitor alert rule
- B) Application Insights availability test
- C) Azure Monitor metrics chart
- D) Log Analytics workspace query

**H3.** Dev team deploys resources manually via portal. Manager wants consistency, fewer errors, version control. Which approach?

- A) Detailed documentation with screenshots
- B) Multiple admin reviewers
- C) ARM templates
- D) Azure Backup

**H4.** A US government agency needs to host apps that process sensitive federal data, requiring physical/logical isolation within the US, screened US personnel, and FedRAMP High compliance. Which Azure deployment option?

- A) Azure Arc on-premises
- B) Azure public cloud US regions
- C) Azure Government
- D) Azure China (21Vianet)

**H5.** User1 needs to start/stop VMs in RG-Production but NOT delete or modify configurations. What to do?

- A) Reader role
- B) Custom RBAC role with only VM start/stop actions
- C) Virtual Machine Contributor role (too broad — includes delete/modify)
- D) Contributor role (too broad — includes everything)

**H6.** IT manager wants to demo deploying a VM using a GUI in any web browser, no installs. Which tool?

- A) Azure PowerShell
- B) Azure Mobile App
- C) Azure Portal
- D) Azure CLI

**H7.** 500 employees need SSO to M365 + custom Azure apps. One sign-in for all. Which service?

- A) Azure Key Vault
- B) Windows Server AD on Azure VMs
- C) Microsoft Entra ID
- D) Azure AD DS

**H8.** Your company migrates a web app to Azure VMs (IaaS). Which security task remains the company's responsibility?

- A) Hypervisor security
- B) Physical network infrastructure
- C) Physical datacenter security
- D) Security patches and updates for the operating system

**H9.** A retail company runs a critical e-commerce application that must remain available to customers even if an Azure datacenter experiences an outage. The company wants to leverage Azure's infrastructure to ensure the application continues operating during such failures. Which Azure reliability benefit directly addresses this requirement?

- A) Azure's ability to deploy resources across multiple availability zones within a region
- B) Azure's pay-as-you-go pricing model
- C) Azure's support for automatic horizontal scaling
- D) Azure's compliance certifications

**H10.** A company has servers on-premises, VMs in AWS, and resources in Azure. The IT director wants Azure management tools, Azure policies, and a single control plane for all. Which service?

- A) Azure Arc
- B) Azure Resource Manager
- C) Azure Monitor
- D) Microsoft Defender for Cloud

**H11.** Users outside corporate network must use MFA; users on corporate network just username/password. Which Entra feature?

- A) Entra ID Protection
- B) Entra PIM
- C) Entra Conditional Access
- D) Entra MFA (alone)

**H12.** A company deploying a business-critical app needs protection against datacenter-level failures within a single region with 99.99% SLA. Which feature to distribute VMs?

- A) Multiple resource groups
- B) Availability zones
- C) Multiple Azure regions
- D) Single datacenter with backup copies

**H13.** A retail company manages its own data center with physical servers that sit idle during off-peak hours, paying fixed costs for hardware, cooling, and maintenance. Which characteristic of cloud computing would most directly address their concern about paying for unused capacity?

- A) High availability
- B) Pay-as-you-go pricing
- C) Disaster recovery
- D) Geo-distribution

**H14.** A retail company runs an e-commerce app serving ~1,000 users normally but 50,000 during seasonal sales. They want to handle traffic spikes while minimizing costs during normal periods. Which cloud capability best addresses this?

- A) Horizontal scaling (scaling out)
- B) Vertical scaling (scaling up)
- C) Geo-distribution
- D) High availability

**H15.** A dev team needs to deploy a small app processing HTTP requests, running seconds per request, sporadic traffic, minimize management, pay only for compute time used. Which service?

- A) Azure Virtual Machines
- B) Azure Container Instances
- C) Azure Functions
- D) Azure App Service

**H16.** Azure security benefit: how does Azure reduce security management burden vs. on-prem?

- A) Azure eliminates ALL security responsibilities
- B) Customers must install own security software
- C) Azure provides security tools managed/updated by Microsoft, reducing org's security infrastructure burden
- D) Azure only secures Microsoft-managed services

**H17.** Developers want to deploy code directly without managing VMs, OS, or hardware. Need auto-scaling and load balancing. Which service model?

- A) IaaS — VM Scale Sets
- B) PaaS — Azure App Service
- C) IaaS — Virtual Machines
- D) SaaS — Microsoft 365

**H18.** Deploy 15 identical VMs across 3 regions. Ensure consistency. Simplify deployment. Which ARM capability?

- A) Resource groups (organize only)
- B) Resource locks (protect, not deploy)
- C) RBAC (permissions, not deploy)
- D) ARM templates

**H19.** Customer data across SQL DB, Storage, Data Lake. Compliance team needs to discover sensitive data, classify it, track access centrally. Which service?

- A) Azure Policy
- B) Microsoft Purview
- C) Microsoft Defender for Cloud
- D) Microsoft Entra ID

**H20.** IT security team needs continuous security posture assessment, recommendations, and threat alerts across VMs, storage, and databases. Which service?

- A) Azure Policy
- B) Entra ID Protection
- C) Azure Monitor
- D) Microsoft Defender for Cloud

**H21.** A company has 5 branch offices with local Windows file servers. Need to centralize in Azure Files while ensuring fast local access even with slow internet. Which service?

- A) Azure Blob Storage + CDN
- B) Azure File Sync
- C) Azure Files + geo-replication
- D) Azure NetApp Files

**H22.** Web app on Azure App Service has slow page loads but team can't identify which components cause it. Need automatic anomaly detection, user behavior tracking, dependency identification. Which service?

- A) Azure Service Health
- B) Application Insights
- C) Microsoft Defender for Cloud
- D) Azure Monitor Logs

**H23.** All VMs across multiple subscriptions must deploy only in East US and West Europe (data residency). What to enforce?

- A) RBAC
- B) Resource locks
- C) Azure Policy
- D) Defender for Cloud

**H24.** RG-Prod with critical VMs/storage. Prevent accidental deletion by Contributor-level admins while still allowing config changes. What to implement?

- A) Delete lock on RG-Prod
- B) Read-only lock (too restrictive — blocks config changes)
- C) Defender for Cloud (security, not deletion prevention)
- D) Remove Contributor, assign Reader (too restrictive)

**H25.** A company is migrating from on-premises to Azure. Currently they pay fixed monthly datacenter costs regardless of usage. How will the consumption-based model change their cost structure?

- A) Pay upfront capital expenses before deploying
- B) Same total costs, distributed differently
- C) Fixed monthly subscription fee
- D) Pay only for Azure resources actually used, with costs varying based on consumption

**H26.** Defense-in-depth for an app using VMs + SQL DB + sensitive customer data. Which approach?

- A) Only NSGs
- B) Only perimeter firewall + VM patches
- C) Only RBAC + Entra auth
- D) Multiple layers: NSGs + encryption at rest + MFA + Defender for Cloud monitoring

**H27.** A manufacturing company must keep proprietary production control systems on-premises (regulatory + ultra-low latency) but wants to migrate some workloads to Azure with consistent management tools and seamless connectivity. Which cloud model?

- A) Hybrid cloud
- B) Community cloud
- C) Public cloud
- D) Private cloud

**H28.** Dev environment used 9 AM–5 PM Mon–Fri only. Which pricing model for greatest savings?

- A) Pay-as-you-go with automated shutdown/startup schedules
- B) Azure Hybrid Benefit (saves on licensing, not usage hours)
- C) 1-year Reserved Instance (pays for 24/7 — wastes 76% of hours)
- D) 3-year Reserved Instance (same problem as 1-year)

**H29.** Development team needs to deploy a web app focused on writing code, not managing infrastructure. Needs auto-scaling and built-in load balancing. Which service?

- A) Azure Functions
- B) Azure Virtual Machines
- C) Azure Container Instances
- D) Azure App Service

**H30.** Migrating 50 physical servers. Need to discover dependencies, get Azure cost estimates, right-sizing recommendations. Which service?

- A) Azure Migrate
- B) Azure Advisor
- C) Defender for Cloud
- D) Azure Monitor

**H31.** Allow users from a partner company to access your app without creating accounts in your directory. Partner manages their own credentials. Which Entra feature?

- A) Conditional Access
- B) Entra B2C
- C) Entra B2B collaboration
- D) Entra Domain Services

**H32.** A company needs to store large amounts of unstructured data (images, videos, logs). Frequently accessed first month, rarely after. Want to minimize costs. Which solution?

- A) Azure Files Premium → Standard
- B) Azure Queue Storage
- C) Azure Table Storage
- D) Azure Blob Storage with lifecycle management policy (move to Cool after 30 days)

**H33.** Multiple departments (Marketing, Finance, IT). CFO needs monthly cost reports broken down by department. Most effective way?

- A) Apply tags with department names → filter cost analysis by tag
- B) Defender for Cloud (wrong tool)
- C) Separate resource groups + manual calculation
- D) Separate subscriptions per department (overkill)

**H34.** A company wants to provide 500 remote employees with Windows 11 desktops and M365 apps, centrally managed, consistent security, minimal device hardware. Which solution?

- A) Azure VMs with RDP per user
- B) Azure App Service
- C) M365 Business Premium with local installs
- D) Azure Virtual Desktop

**H35.** Migrating from on-prem. IT director wants to understand potential 5-year cost savings comparing on-prem vs. Azure. Which tool?

- A) Azure Pricing Calculator
- B) TCO Calculator (deprecated August 2025)
- C) Azure Cost Management (for existing resources only)
- D) Azure Advisor (for existing resources only)

**H36.** All VMs across multiple subscriptions must have specific tags (Department, CostCenter, Owner) before creation. Which governance feature?

- A) Resource locks
- B) RBAC
- C) Azure Policy
- D) Management groups (organize subscriptions, not enforce tags directly)

**H37.** Company keeps some apps on-prem (regulatory) and migrates others to Azure with seamless auth. Which deployment model?

- A) Public cloud
- B) Hybrid cloud
- C) Private cloud
- D) Community cloud

**H38.** IT director wants authentication that eliminates passwords while providing strong auth. Which method?

- A) Security questions
- B) Windows Hello for Business
- C) Username + complex password + rotation
- D) MFA via SMS

**H39.** Deploy identical dev, test, prod environments. Same VMs, storage, VNets. Ensure consistency, minimize manual errors. Which feature?

- A) Azure Portal dashboard
- B) Azure Policy
- C) Resource groups
- D) ARM templates

**H40.** Two VNets in different regions need direct communication via private IPs. Which solution?

- A) Azure DNS
- B) Shared subnet
- C) Virtual network peering
- D) Azure VPN Gateway site-to-site

**H41.** A retail company needs to forecast annual cloud spending accurately (within 5% variance) for budget planning. Which Azure benefit of cloud computing best addresses this?

- A) High availability
- B) Disaster recovery
- C) Performance predictability
- D) Cost predictability

**H42.** IT manager wants notification when Azure plans maintenance affecting VMs + root cause analysis for service interruptions. Which service?

- A) Azure Service Health
- B) Defender for Cloud
- C) Azure Monitor
- D) Azure Advisor

**H43.** On-prem app server migration: needs 8 vCPUs, 32 GB RAM, Windows Server 2022, full OS control, custom software. What to recommend?

- A) Azure Virtual Machines
- B) Azure Functions
- C) Azure Container Instances
- D) Azure App Service

**H44.** Multiple microservices with unpredictable traffic, need independent scaling, containerized with dependencies, minimize management. Which compute option?

- A) Azure App Service (single web app)
- B) Azure Kubernetes Service (AKS) with auto-scaling
- C) Azure VMs with manual scaling
- D) Azure Container Instances

**H45.** Mobile app processing image uploads, unpredictable spikes, pay only when processing. Which compute solution?

- A) Azure VMs with auto-scaling
- B) Azure Container Instances (continuous)
- C) Azure App Service (Always On)
- D) Azure Functions with consumption plan

**H46.** Need to estimate monthly cost for 5 VMs, 2 SQL DBs, 10 TB blob storage across 2 regions BEFORE deploying. Which tool?

- A) Azure Pricing Calculator
- B) Azure Cost Management (for existing resources)
- C) Azure Advisor (for existing resources)
- D) TCO Calculator (deprecated)

**H47.** Business-critical app, must survive datacenter failure but NOT regional disaster. Minimize costs. Which storage redundancy?

- A) LRS
- B) ZRS (Zone-Redundant Storage)
- C) GRS
- D) GZRS

**H48.** Business-critical app must remain available even if entire Azure REGION fails. Need automatic replication to secondary location. Which feature?

- A) Azure region pairs
- B) Availability Sets in multiple regions
- C) Resource groups spanning regions
- D) Availability Zones within a region

**H49.** Running multiple Azure resources for 6 months. IT manager wants to identify opportunities to reduce costs, improve security, and optimize performance. Which service?

- A) Azure Advisor
- B) Azure Service Health
- C) Azure Monitor
- D) Defender for Cloud

**H50.** Retail company building a mobile app for customer accounts using social media logins (Facebook, Google, email). No corporate credentials. Which service?

- A) Microsoft Entra B2B
- B) Microsoft Entra B2C
- C) Microsoft Entra Domain Services
- D) Microsoft Entra ID (standard tenant)

### Answers — Section H

| # | Answer | Explanation |
|---|---|---|
| H1 | **d** | Public cloud services are delivered over the public internet, accessible to anyone worldwide. Hybrid combines public + private. Private is dedicated/restricted. Community is shared by organizations... (Duffy PT) |
| H2 | **a** | Alert rules = define conditions + automated responses (email via action groups). Metrics charts only visualize. Log Analytics only queries. App Insights tests endpoint availability, not VM CPU. (Duffy PT) |
| H3 | **c** | ARM templates = Infrastructure as Code. JSON files. Version controlled in Git. Consistent, repeatable deployments. Reduces human error. (Duffy PT) |
| H4 | **c** | Azure Government = sovereign cloud for US government agencies. Physically and logically isolated. Screened US personnel. FedRAMP High + DoD standards. Public US regions don't offer the same isolati... (Duffy PT) |
| H5 | **b** | Principle of least privilege. Custom RBAC role = grant exactly the permissions needed. VM Contributor allows delete. Contributor allows everything. (Duffy PT) |
| H6 | **c** | Portal = web-based GUI at portal.azure.com. No install needed. Step-by-step wizards for creating resources. (Duffy PT) |
| H7 | **c** | Entra ID = cloud identity + SSO. Token-based. Register apps with Entra. One login = access to all registered apps (M365, custom, third-party). (Duffy PT) |
| H8 | **d** | Shared responsibility model: IaaS = customer manages from OS up (patches, apps, data). Microsoft manages physical infrastructure + hypervisor. (Duffy PT) |
| H9 | **a** | Availability zones = physically separate datacenters within a region with independent power/cooling/networking. Deploying across zones provides datacenter-level fault tolerance = reliability. (Duffy PT) |
| H10 | **a** | Azure Arc = extend Azure management to on-prem + multi-cloud. Single pane of glass. Apply Azure Policy, Monitor, and Sentinel across all platforms. (Duffy PT) |
| H11 | **c** | Conditional Access = location-based (and other signal-based) access policies. MFA is the technology; Conditional Access decides WHEN to apply it. (Duffy PT) |
| H12 | **b** | Availability zones = physically separate datacenters within a region. 99.99% SLA when VMs deployed across 2+ zones. Multiple regions would be overkill for within-region datacenter failures. (Duffy PT) |
| H13 | **b** | Consumption-based pricing = pay only for resources actually used. Eliminates paying for idle capacity. Shifts from fixed CapEx to variable OpEx. (Duffy PT) |
| H14 | **a** | Horizontal scaling = add/remove instances based on demand. Best for dramatic traffic fluctuations (1K→50K). Vertical scaling has limits and doesn't optimize costs during quiet periods. (Duffy PT) |
| H15 | **c** | Azure Functions (consumption plan) = serverless, event-driven, pay-per-execution. Ideal for short-lived, sporadic HTTP workloads. Zero cost when idle. (Duffy PT) |
| H16 | **c** | Shared responsibility model. Microsoft manages infrastructure security + provides tools (Defender, Entra, DDoS). Customer manages apps/data. Not ALL responsibilities eliminated. (Duffy PT) |
| H17 | **b** | PaaS = managed platform; deploy code, not infrastructure. App Service provides auto-scaling, load balancing, deployment slots, CI/CD. (Duffy PT) |
| H18 | **d** | ARM templates = define once, deploy many times. Parameterized (different regions, names). Consistent configuration guaranteed. (Duffy PT) |
| H19 | **b** | Purview = data governance. Discovery, classification (sensitivity labels), lineage tracking across the entire data estate. (Duffy PT) |
| H20 | **d** | Defender for Cloud = security posture (secure score + recommendations) + threat detection. Covers VMs, storage, databases, multi-cloud. (Duffy PT) |
| H21 | **b** | Azure File Sync = local cache of frequently accessed files + centralized storage in Azure Files. Bidirectional sync. Cloud tiering (20 GB local, 20 TB cloud). (Duffy PT) |
| H22 | **b** | Application Insights = APM feature of Azure Monitor. Auto-detects anomalies, tracks dependencies, monitors user behavior, identifies performance bottlenecks. (Duffy PT) |
| H23 | **c** | Azure Policy = enforce where resources can be deployed. "Allowed locations" policy definition. Assign across subscriptions. (Duffy PT) |
| H24 | **a** | Delete lock = prevents deletion, allows modifications. Read-only lock prevents both. Delete lock = the right balance for this scenario. (Duffy PT) |
| H25 | **d** | Consumption-based = pay for what you use. Shifts from fixed CapEx to variable OpEx. Costs scale with actual business demand. (Duffy PT) |
| H26 | **d** | Defense in depth = security at EVERY layer (network + data + identity + monitoring). Single-layer approaches are insufficient. (Duffy PT) |
| H27 | **a** | Hybrid = on-premises + public cloud with integration. Meets regulatory requirements for keeping some workloads local while leveraging cloud for others. (Duffy PT) |
| H28 | **a** | PAYG + auto-shutdown = pay only for 40 hours/week (not 168). 76% savings on compute. Reserved Instances pay for 24/7 regardless. (Duffy PT) |
| H29 | **d** | App Service = PaaS for web apps. No infrastructure management. Built-in auto-scaling, load balancing, deployment slots, CI/CD. Focus on code. (Duffy PT) |
| H30 | **a** | Azure Migrate = discover, assess, and migrate. Discovery tool for on-prem. Dependency mapping. Cost estimates. Readiness scoring. (Duffy PT) |
| H31 | **c** | B2B = invite external partners as guest users. They use their own company credentials. You control access to your resources. B2C is for consumers, not partners. (Duffy PT) |
| H32 | **d** | Blob Storage = designed for unstructured data. Lifecycle management auto-transitions blobs from Hot → Cool → Cold → Archive based on rules. (Duffy PT) |
| H33 | **a** | Tags = key-value metadata. Cost Management natively supports filtering/grouping by tags. Most efficient and scalable. (Duffy PT) |
| H34 | **d** | AVD = virtualized Windows desktop in Azure. Multi-session Win 11. Central management. Any device access. Minimal client hardware. (Duffy PT) |
| H35 | **a** | Pricing Calculator is now the recommended tool for ALL cost estimation including migration scenarios. TCO Calculator has been retired. (Duffy PT) |
| H36 | **c** | Azure Policy = enforce required tags. Built-in policy: "Require a tag on resources". Prevent non-compliant resources from being created. (Duffy PT) |
| H37 | **b** | Hybrid = on-prem + public cloud. Integration via Entra Connect for seamless authentication. (Duffy PT) |
| H38 | **b** | Windows Hello = passwordless. Biometric (face/fingerprint) or device-bound PIN. Credentials never leave device. Phishing-resistant. (Duffy PT) |
| H39 | **d** | ARM templates = IaC. Define once, deploy identically across environments. Version-controlled. Eliminates manual configuration errors. (Duffy PT) |
| H40 | **c** | VNet peering (global) = connect VNets across regions via Azure backbone. Private IPs. Low latency. High bandwidth. Simpler and cheaper than VPN Gateway for Azure-to-Azure connections. (Duffy PT) |
| H41 | **d** | Cost predictability = ability to forecast and control cloud spending through tools like Azure Cost Management, pricing calculators, and cost alerts. (Duffy PT) |
| H42 | **a** | Service Health = Azure platform status. Service issues, planned maintenance, health advisories. Root cause analysis (RCA) reports after incidents. (Duffy PT) |
| H43 | **a** | VMs = IaaS. Full OS control. Custom software installation. Choose exact specs. Ideal for lift-and-shift of traditional servers. (Duffy PT) |
| H44 | **b** | AKS = enterprise-grade container orchestration. Independent scaling per microservice. Auto-scaling. Service discovery. Self-healing. Managed service. (Duffy PT) |
| H45 | **d** | Functions consumption = serverless, pay-per-execution. Zero cost when idle. Auto-scales on demand. Perfect for event-driven image processing. (Duffy PT) |
| H46 | **a** | Pricing Calculator = estimate costs BEFORE deployment. Add services, configure regions/tiers/sizes, get monthly estimate. (Duffy PT) |
| H47 | **b** | ZRS = 3 copies across availability zones in same region. Survives datacenter failure. Cheaper than GRS/GZRS (no cross-region replication needed). (Duffy PT) |
| H48 | **a** | Region pairs = two regions paired for DR. Azure auto-replicates certain services (GRS). Sequential updates. Fastest connection between paired regions. (Duffy PT) |
| H49 | **a** | Advisor = personalized recommendations across 5 categories (Cost, Security, Reliability, Operational Excellence, Performance) based on YOUR actual usage. Free. Automatic. (Duffy PT) |
| H50 | **b** | B2C = business-to-consumer. Social identity providers (Facebook, Google, LinkedIn). Self-service customer sign-up. No corporate credentials needed. (Duffy PT) |
---

## Section I — Practice Test 3

> **Source**: AZ-900 Udemy Practice Test 3 (82 scenario/concept questions)

**I1.** Azure VMs are classified as which service model? → ||IaaS||

**I2.** Creating a resource group requires specifying a location? → ||Yes||

**I3.** Deleting a resource group deletes all resources inside? → ||Yes||

**I4.** Create/manage load-balanced VMs, distribute across AZs, auto-scale. Which service? → ||Azure Scale Sets (VMSS)||

**I5.** Which cloud service model places the GREATEST security responsibility on the customer? → ||IaaS||

**I6.** Azure service incidents, planned maintenance, notifications via email/SMS/push? → ||Azure Service Health||

**I7.** Is internet connection necessary for cloud computing? → ||No||

**I8.** Personalized view of health of Azure services/regions/resources you rely on? → ||Azure Service Health||

**I9.** Tags don't inherit from resource groups to resources? → ||True||

**I10.** Recommendation to deal with unexpected Azure outage in a DC/AZ? → ||Fault Tolerance||

**I11.** In PaaS, which security responsibility falls on the Cloud Service Provider? → ||Protecting the underlying infrastructure||

**I12.** SaaS consumer responsibility: "configuring high availability" is incorrect. Correct answer → ||Configuring the SaaS solution||

**I13.** University streams lectures: uninterrupted playback during finals + cost savings during summer. Best cloud benefit pair? → ||Elasticity and consumption-based pricing||

**I14.** Startup with unpredictable traffic spikes. Best pricing model? → ||Pay-as-you-go||

**I15.** Reduce costs up to 72% vs. PAYG by ___? → ||Using Reserved Instances||

**I16.** Estimate cost savings of migrating to Azure? → ||Azure TCO Calculator||

**I17.** Web app for employees (Python preferred) to enter vacation details + backend storage. Which service? → ||Azure App Service||

**I19.** Permissions assigned to a resource group are inherited by all resources inside it? → ||Yes||

**I20.** Hybrid cloud definition includes using multiple public clouds + private cloud? → ||Yes||

**I21.** Azure ExpressRoute description? → ||Dedicated, private network connectivity between on-prem and Azure DCs||

**I22.** Agreement with Microsoft for cloud platform/services, charges based on per-user or consumption? → ||A Subscription||

**I23.** Why is the shared responsibility model important? → ||It clearly defines the roles of CSP and customer in security||

**I24.** Small dev team building a POC, need rapid experimentation with technologies. Best service model? → ||PaaS||

**I25.** Migrate on-prem app to Azure, be relieved of manual admin/maintenance. Best model? → ||PaaS||

**I26.** Which is NOT a CSP responsibility in shared responsibility? → ||Ensuring data privacy||

**I27.** Inter-region data transfer always free? → ||No||

**I28.** Migrate VMs to PAYG subscription. Which expenditure model? → ||Operational (OpEx)||

**I29.** Primary purpose of Microsoft Purview? → ||Manage and govern data across on-prem, multi-cloud, and SaaS||

**I30.** Management group tree max depth (excluding root + subscription level)? → ||6 levels||

**I31.** Factors that influence Azure costs? Select all → ||Geography||

**I32.** Colleague creates App Service + 3 VMs for a PaaS POC. Agree? → ||No||

**I33.** Protocol Microsoft Entra ID primarily uses for SSO? → ||SAML||

**I34.** Deploy Azure resources from a Tablet using Bash in Cloud Shell? → ||Yes||

**I35.** Serverless solution: write less code, less infrastructure, save costs? → ||Azure Functions||

**I36.** All resource types support Tags? → ||No||

**I37.** Migrating website to Azure — PAYG pricing is a benefit? → ||True (the statement is correct)||

**I38.** Fully managed file shares via SMB or NFS, replace on-prem file servers? → ||Azure Files||

**I39.** IaaS: which is primarily the customer's responsibility? → ||Patching the OS of virtual machines||

**I40.** Gaming company uses Azure Functions triggered by game events. Serverless traits? → ||Costs only during execution + Azure auto-adjusts capacity||

**I41.** Service that provides recommendations to optimize cloud spending based on usage? → ||Azure Cost Management and Billing||

**I42.** When should you scale OUT? → ||When you need additional VMs/compute to speed up your application||

**I43.** Industries with highly sensitive data (banking, government, healthcare) — best cloud option? → ||Hybrid||

**I44.** Mission-critical cloud for US government, screened US citizens, dedicated instance? → ||Azure Government||

**I45.** Restrict access to Azure resources based on departmental requirements? → ||Subscriptions||

**I46.** NOT a benefit of Microsoft Entra ID? → ||Unlimited data storage||

**I47.** Large enterprise migrating legacy on-prem apps with minimal changes. Best model? → ||IaaS||

**I48.** On-prem capacity exceeded → instantly scale up/down using _____ cloud? → ||Public||

**I49.** Collect, analyze, act on metric/logging data from entire Azure + on-prem environment? → ||Azure Monitor||

**I50.** Startup building custom e-commerce platform needing high scalability + flexibility for rapid growth. Best model? → ||IaaS||

**I51.** Live football streaming — massive spikes when goals scored. Best for expected demand? → ||Serverless Computing||

**I52.** Defense-in-depth: how does it enhance cybersecurity vs. perimeter-only? → ||Protects against both external and internal threats||

**I53.** What is Microsoft Entra ID? → ||Cloud-based identity and access management service||

**I54.** Primary goal of defense-in-depth? → ||Establish multiple layers of security controls to mitigate risks||

**I55.** Advantage of public cloud for migration? → ||Near unlimited scalability with on-demand resources||

**I56.** Apply read-only lock to resource that already has delete lock? → ||Yes, but only by the subscription owner||

**I57.** How does Defender for Cloud contribute to Azure-native service security? → ||Natively integrates with Azure services for monitoring and protection||

**I58.** File share accessible from multiple VMs without separate file server? → ||Azure Storage Account||

**I59.** Deploy VMs to 2+ Availability Zones to ensure availability if single DC fails? → ||Yes||

**I60.** Factors affecting Azure service availability under SLA? Select all → ||Natural disasters||

**I61.** Resource group can contain resources from multiple Azure regions? → ||Yes||

**I62.** Shared responsibility for retail chain migrating to Azure VMs + managed DB: select all that apply → ||Customer applies OS updates to VMs||

**I63.** Defense-in-depth: role of the "network" layer? → ||Limits communication between resources and enforces access controls||

**I64.** Can a resource belong to more than one resource group? → ||No||

**I65.** Strict governance, right people, right resources, right time? → ||Microsoft Entra ID||

**I66.** Can anyone modify a resource with a delete lock? → ||Yes, admin can modify||

**I67.** Significance of "data" layer in defense-in-depth? → ||Protects sensitive data; ensures confidentiality, integrity, and availability||

**I68.** Personalized recommendations for all subscriptions, filterable by subscription/RG/service? → ||Azure Advisor||

**I69.** Determine estimated monthly cost of Azure service/resource? → ||Azure Pricing Calculator||

**I70.** Data in Azure storage replicated 3 times in primary region? → ||Yes||

**I71.** Migrate CRM to cloud: need customization + minimize IT overhead. Best model? → ||PaaS||

**I72.** Factors affecting Azure costs? Choose 2 → ||Instance size||

**I73.** Feature of Microsoft Entra ID? → ||Managed Identities||

**I74.** Primary purpose of Defender for Cloud? → ||Monitor security posture and protect against threats (cloud, on-prem, hybrid, multi-cloud)||

**I75.** Logistics company uses Azure Functions triggered by shipments, scales with order volume, pay per execution. Serverless + consumption-based? → ||Yes||

**I76.** Default maximum capacity for storage accounts? → ||5 PiB||

**I77.** Full control of underlying OS in PaaS? → ||No||

**I78.** Permissions assigned to resource group inherited by all resources inside? → ||Yes||

**I79.** RBAC at management group level: what occurs? → ||Permissions inherited by all sub-MGs, subscriptions, RGs, and resources||

**I80.** Action to reduce Azure costs? → ||Reduce data transferred between Azure regions||

**I81.** Public cloud characteristics: select all → ||Metered pricing||

**I82.** Unstructured data, auto-index all data, multi-region writes. Which service? → ||Azure Cosmos DB||

**I83.** Auto sign-in when on corporate device + corporate network? → ||Single Sign-On (SSO)||

### Answers — Section I

| # | Answer | Explanation |
|---|---|---|
| I1 | **IaaS** | VMs provide virtualized compute resources. You manage OS and apps. IaaS = renting infrastructure. (PT3) |
| I2 | **Yes** | RG location = where metadata is stored. Resources inside can be in different regions. (PT3) |
| I3 | **Yes** | Delete RG = delete everything inside. Useful for cleanup. Be cautious. (PT3) |
| I4 | **Azure Scale Sets (VMSS)** | VMSS = group of identical VMs + load balancer + auto-scaling + AZ distribution. (PT3) |
| I5 | **IaaS** | IaaS = customer manages OS, apps, data, network config. SaaS = least responsibility. PaaS = middle ground. (PT3) |
| I6 | **Azure Service Health** | Service Health = platform status + alerts. Not Monitor (resource metrics). Not Advisor (recommendations). (PT3) |
| I7 | **No** | ExpressRoute = private connection. Azure Stack/Azure Local = on-prem cloud without internet. Edge computing. (PT3) |
| I8 | **Azure Service Health** | Personalized to YOUR resources and regions. Not Advisor. Not Monitor. Not Resource Health (individual resources only). (PT3) |
| I9 | **True** | Tags must be applied individually to each resource. Use Azure Policy to auto-apply/inherit. (PT3) |
| I10 | **Fault Tolerance** | Fault tolerance = system remains operational when components fail. Redundancy, failover, backups. (PT3) |
| I11 | **Protecting the underlying infrastructure** | CSP manages servers, networks, storage. Customer manages app code, user identities, data. (PT3) |
| I12 | **Configuring the SaaS solution** | SaaS: provider manages HA, infrastructure, updates. Consumer configures settings and manages their data. (PT3) |
| I13 | **Elasticity and consumption-based pricing** | Elasticity = auto-scale to demand. Consumption-based = pay only for what you use. (PT3) |
| I14 | **Pay-as-you-go** | PAYG = highest flexibility. No commitment. Scale up/down freely. Pay only for usage. (PT3) |
| I15 | **Using Reserved Instances** | 1-year or 3-year commitment. Up to 72% savings. Combine with Hybrid Benefit for up to 80%. (PT3) |
| I16 | **Azure TCO Calculator** | ⚠️ Note: TCO Calculator was deprecated August 2025. Current answer: **Pricing Calculator** is now recommended. This question reflects older exam content. (PT3) |
| I17 | **Azure App Service** | App Service = PaaS for web apps. Supports Python. No infrastructure management. (PT3) |
| I19 | **Yes** | RBAC permissions at RG level inherit to all contained resources. (PT3) |
| I20 | **Yes** | Microsoft docs define hybrid cloud as including "multicloud" configurations with multiple public clouds + on-premises. (PT3) |
| I21 | **Dedicated, private network connectivity between on-prem and Azure DCs** | Not public internet. Not backup/DR. Not a management dashboard. (PT3) |
| I22 | **A Subscription** | Subscription = billing unit + access control boundary. (PT3) |
| I23 | **It clearly defines the roles of CSP and customer in security** | Establishes accountability. Doesn't guarantee prevention but clarifies who handles what. (PT3) |
| I24 | **PaaS** | PaaS = rapid development environment. Pre-configured tools. No infrastructure management. Focus on building. (PT3) |
| I25 | **PaaS** | PaaS = managed platform. No OS patching, no infrastructure management. Focus on app. (PT3) |
| I26 | **Ensuring data privacy** | Data privacy = customer responsibility. CSP handles physical DC, network, infrastructure. (PT3) |
| I27 | **No** | Inter-region transfer is charged. Inbound = free. First ~5 GB outbound = free. Beyond that = charged. (PT3) |
| I28 | **Operational (OpEx)** | PAYG = operational expenditure. No upfront CapEx. Pay monthly based on consumption. (PT3) |
| I29 | **Manage and govern data across on-prem, multi-cloud, and SaaS** | Unified data governance. Discovery, classification, lineage tracking. (PT3) |
| I30 | **6 levels** | 6 levels of nesting for management groups. (PT3) |
| I31 | **Geography** | NOT: Maintenance (not a direct cost factor). (PT3) |
| I32 | **No** | App Service = PaaS ✓. VMs = IaaS ✗. VMs violate the PaaS-only requirement. (PT3) |
| I33 | **SAML** | SAML = Security Assertion Markup Language. Also supports OAuth 2.0 and OpenID Connect. (PT3) |
| I34 | **Yes** | Cloud Shell = browser-based. Any device with a browser. Bash or PowerShell. No install needed. (PT3) |
| I35 | **Azure Functions** | Functions = serverless compute. Event-triggered. Pay per execution. No infra management. (PT3) |
| I36 | **No** | Not all resource types support tags. Check documentation for specific resources. (PT3) |
| I37 | **True (the statement is correct)** | PAYG = pay for what you use. Major advantage of cloud migration. (PT3) |
| I38 | **Azure Files** | Azure Files = SMB + NFS. Mountable as drive letter. Replace/supplement on-prem file servers. (PT3) |
| I39 | **Patching the OS of virtual machines** | IaaS = customer manages from OS up. CSP handles physical infra, network, platform. (PT3) |
| I40 | **Costs only during execution + Azure auto-adjusts capacity** | Serverless = no server management, auto-scaling, pay-per-execution. NOT dedicated hardware. NOT VM OS config. (PT3) |
| I41 | **Azure Cost Management and Billing** | Cost Management = spending analysis, budgets, cost optimization. Advisor also recommends but Cost Management is the primary cost tool. (PT3) |
| I42 | **When you need additional VMs/compute to speed up your application** | Scale out = add more instances. Scale up = bigger instance. Scale out ≠ reduce cost or get stronger CPU. (PT3) |
| I43 | **Hybrid** | Hybrid = keep regulated data on-prem + leverage cloud for less sensitive workloads. (PT3) |
| I44 | **Azure Government** | Sovereign cloud. Federal/state/local/tribal governments + partners only. (PT3) |
| I45 | **Subscriptions** | Subscriptions = access management policies at subscription level. Different departments = different subscriptions for access control. (PT3) |
| I46 | **Unlimited data storage** | Entra ID = identity + access management. Benefits: SSO, MFA, centralized identity. NOT storage. (PT3) |
| I47 | **IaaS** | IaaS = most flexibility to replicate on-prem environment. Lift-and-shift. PaaS/SaaS require app changes. (PT3) |
| I48 | **Public** | Public cloud provides instant scalability without hardware purchases. (PT3) |
| I49 | **Azure Monitor** | Monitor = centralized monitoring platform. Metrics, logs, alerts, dashboards. (PT3) |
| I50 | **IaaS** | IaaS = highest flexibility and control for custom platform. Full customization of infrastructure. (PT3) |
| I51 | **Serverless Computing** | Serverless = auto-scales instantly, event-driven, no server management, cost-efficient for spikes. (PT3) |
| I52 | **Protects against both external and internal threats** | Multiple layers. Not just perimeter. Internal threats (insiders) also covered. (PT3) |
| I53 | **Cloud-based identity and access management service** | Not storage, not network security, not app deployment. (PT3) |
| I54 | **Establish multiple layers of security controls to mitigate risks** | Not single layer. Not physical only. Not outsourcing. (PT3) |
| I55 | **Near unlimited scalability with on-demand resources** | NOT: resources not shared (that's private). NOT: full customization (that's private). NOT: hardware shipped to you. (PT3) |
| I56 | **Yes, but only by the subscription owner** | Multiple locks can coexist. Subscription owner/authorized users can add locks. (PT3) |
| I57 | **Natively integrates with Azure services for monitoring and protection** | Built-in. No separate agent deployment needed for Azure-native services. (PT3) |
| I58 | **Azure Storage Account** | Storage Account provides Azure Files. Tricky: Azure Files would be ideal but Storage Account is the best available option. (PT3) |
| I59 | **Yes** | AZs = physically separate DCs within a region. 99.99% SLA across 2+ zones. (PT3) |
| I60 | **Natural disasters** | NOT: Network disruptions outside Azure (external, not Microsoft's control). (PT3) |
| I61 | **Yes** | RG stores metadata in one location. Resources inside can be in any region. (PT3) |
| I62 | **Customer applies OS updates to VMs** | Customer: OS updates, app logic, data encryption. Azure: physical infra, virtualization. NOT: Azure enforces encryption without input. NOT: customer secures physical server rooms. (PT3) |
| I63 | **Limits communication between resources and enforces access controls** | Network segmentation, firewalls, NSGs. Not physical security (physical layer). Not app access (app layer). (PT3) |
| I64 | **No** | 1 resource = 1 resource group. Always. (PT3) |
| I65 | **Microsoft Entra ID** | Identity + access management. SSO, MFA, conditional access. Governance through identity. (PT3) |
| I66 | **Yes, admin can modify** | Delete lock = prevents deletion only. Modifications still allowed. Read-only lock prevents both. (PT3) |
| I67 | **Protects sensitive data; ensures confidentiality, integrity, and availability** | Data layer = control access to business/customer data. Compliance. Encryption. (PT3) |
| I68 | **Azure Advisor** | Advisor = personalized recommendations. 5 categories: Cost, Security, Reliability, OpEx, Performance. (PT3) |
| I69 | **Azure Pricing Calculator** | Pricing Calculator = pre-deployment cost estimation. Input service details → get monthly estimate. (PT3) |
| I70 | **Yes** | LRS = 3 copies in same DC. ZRS = 3 copies across zones. Always minimum 3 copies. (PT3) |
| I71 | **PaaS** | PaaS = customization options + managed infrastructure. IaaS = too much overhead. SaaS = limited customization. (PT3) |
| I72 | **Instance size** | NOT: AZ (no direct cost). NOT: Knowledge center (free). (PT3) |
| I73 | **Managed Identities** | Managed Identities = identity for services to authenticate to Azure resources without storing credentials in code. (PT3) |
| I74 | **Monitor security posture and protect against threats (cloud, on-prem, hybrid, multi-cloud)** | Security posture + threat detection. Not network segmentation. Not VM deployment. Not physical security. (PT3) |
| I75 | **Yes** | PaaS abstracts the OS. Provider manages infrastructure, OS, middleware. You manage apps and data. (PT3) |
| I76 | **5 PiB** | 5 PiB = ~5 petabytes. Massive capacity per account. (PT3) |
| I77 | **No** |  (PT3) |
| I78 | **Yes** | Same as Q19. RBAC inheritance from RG to resources. (PT3) |
| I79 | **Permissions inherited by all sub-MGs, subscriptions, RGs, and resources** | Full inheritance down the hierarchy. (PT3) |
| I80 | **Reduce data transferred between Azure regions** | Inter-region transfer = charged. Reducing it = cost savings. NOT: more VMs (more cost). NOT: 24/7 VMs (more cost). (PT3) |
| I81 | **Metered pricing** | NOT: hardware purchase, unsecured connections, customer hardware maintenance. (PT3) |
| I82 | **Azure Cosmos DB** | Cosmos DB = multi-model (document, graph, key-value), auto-indexing, global distribution, multi-region writes. (PT3) |
| I83 | **Single Sign-On (SSO)** | SSO = authenticate once, access all registered apps. Seamless SSO = auto sign-in on corporate devices. (PT3) |
---

## Section J — Practice Test 4

> **Source**: AZ-900 Udemy Practice Test 4 (90 questions)

**J1.** Azure VMs classified as? → ||IaaS||

**J2.** CLI utility to copy blobs/files to/from storage account? → ||AzCopy||

**J3.** Connection between two Azure regions in same geography for DR? → ||Region Pair||

**J4.** RG requires a location on creation? → ||Yes||

**J5.** For all cloud deployment types, you always own your ___ and ___? → ||Data and Identities||

**J6.** Deleting RG deletes all resources inside? → ||Yes||

**J7.** Azure resource type that does NOT support tagging? → ||Azure Container Registry||

**J8.** Which service model places GREATEST security responsibility on customer? → ||IaaS||

**J9.** Defense-in-depth security layer example? → ||Dedicated intrusion detection system (IDS)||

**J10.** Service incidents + planned maintenance + email/SMS notifications? → ||Azure Service Health||

**J11.** JSON strings to exceed max tag limit? → ||Include multiple values for a single tag name||

**J12.** Extends Azure to on-prem, edge, multi-cloud? → ||Azure Arc||

**J13.** Personalized health view of Azure services/regions/resources you rely on? → ||Azure Service Health||

**J14.** Budgets: notify when spending reaches threshold? → ||Budgets||

**J15.** Appropriate use cases — select all: → ||Private cloud for financial institution||

**J16.** Tags inherit from RG to resources? → ||No (True)||

**J17.** Unexpected Azure DC/AZ outage — recommendation? → ||Fault Tolerance||

**J18.** External Identities in Microsoft Entra ID? → ||External Identities||

**J19.** Azure services in China operated by? → ||21Vianet||

**J20.** Cloud services provide greater control over physical security vs on-prem? → ||No||

**J21.** Consumption-based pricing — most immediate cost benefit for 30% utilized servers? → ||Pay only for resources actually consumed||

**J22.** Private connection to Azure, no public internet? → ||Azure ExpressRoute||

**J23.** Startup, unpredictable traffic spikes, best pricing? → ||Pay-as-you-go||

**J24.** Microservices, independent scaling, event-driven code? → ||AKS + Azure Functions||

**J25.** Primary purpose of resource locks? → ||Prevent accidental deletion or modification||

**J26.** Lightweight containers + event-driven code snippets, no server management? → ||Azure Container Instances||

**J27.** Defender for Cloud detects threats targeting? → ||Azure App Service, Azure SQL, Azure Storage||

**J28.** Deploy Azure VM from Chromebook using PowerAutomate? → ||No||

**J29.** DNS hosting using Azure infrastructure? → ||Azure DNS||

**J30.** Hybrid cloud includes using multiple public clouds + private? → ||Yes||

**J31.** Can Azure DNS buy a domain name? → ||No||

**J32.** Scale Set solves DC failure for critical VMs? → ||No||

**J33.** Defense-in-depth "compute" layer role? → ||Securing VMs and access to them||

**J34.** Shared responsibility model is important because? → ||Clearly defines roles of CSP and customer in security||

**J35.** Healthcare: classify data, monitor VMs, assess security posture? → ||Purview||

**J36.** Small dev team POC, rapid experimentation? → ||PaaS||

**J37.** Free tool to manage storage from desktop? → ||Azure Storage Explorer||

**J38.** Migrate on-prem app, no manual admin/maintenance? → ||PaaS||

**J39.** Cross-VNet connectivity between subnets in different regions? → ||Virtual Network Peering||

**J40.** PaaS for web app deployment + SaaS for managed email? → ||PaaS, SaaS||

**J41.** Multiple business units, unified governance, separate access? → ||Management Groups with Resource Groups by business unit||

**J42.** ExpressRoute goes over public internet? → ||No||

**J43.** Verifying user credentials? → ||Authentication||

**J44.** Azure PowerShell uses ___ commands; Azure CLI uses ___ commands? → ||PowerShell; Bash||

**J45.** "Secure" aspect of Defender for Cloud? → ||Ensure secure configurations of workloads and resources||

**J46.** Quickly provision/deprovision resources with minimal management? → ||Scalability||

**J47.** Protocol Entra ID uses for SSO? → ||SAML||

**J48.** Advisor provides cloud score + step-by-step guidance? → ||Yes||

**J49.** Sharing resources among multiple users/tenants for cost savings? → ||Multi-Tenancy||

**J50.** Serverless, write less code, less infra, save costs? → ||Azure Functions||

**J51.** Gaming company: query VM logs, CPU alerts, diagnose crashes? → ||Log Analytics||

**J52.** All resource types support Tags? → ||No||

**J53.** Service Health can define critical resources that should never be impacted? → ||No||

**J54.** Resource can only access other resources in same RG? → ||No||

**J55.** Fully managed file shares via SMB/NFS? → ||Azure Files||

**J56.** Region selection affects Azure costs? → ||Yes||

**J57.** Isolated DCs with independent power/cooling/networking? → ||Availability Zone||

**J58.** Serverless traits for Azure Functions? → ||Costs only during execution||

**J59.** When budget alert level reached, what happens? → ||Budget alert is triggered||

**J60.** When to scale OUT? → ||When you need additional VMs/compute||

**J61.** Prevent accidental deletion of mission-critical resources? → ||CanNotDelete Lock||

**J62.** Industries with highly sensitive data (banking, gov, healthcare)? → ||Hybrid cloud||

**J63.** Service incidents + planned maintenance notifications? → ||Azure Service Health||

**J64.** Mission-critical cloud for US government? → ||Azure Government||

**J65.** Azure Blueprints: included artifacts? → ||Policy assignments||

**J66.** NOT a benefit of Entra ID? → ||Unlimited data storage||

**J67.** First thing to create when migrating to Azure? → ||A Subscription||

**J68.** Migrate legacy on-prem apps with minimal changes? → ||IaaS||

**J69.** Identify user who made unapproved VM size change? → ||Azure Activity Log||

**J70.** On-prem capacity exceeded → instantly scale using ___ cloud? → ||Public||

**J71.** Seamlessly connect two VNets? → ||Virtual Network Peering||

**J72.** Centralize file shares in Azure Files + Windows file server compatibility? → ||Azure File Sync||

**J73.** Custom e-commerce platform, high scalability + flexibility? → ||IaaS||

**J74.** On-prem + AWS Kubernetes, Azure policies, single portal? → ||Azure Arc||

**J75.** Live football streaming, massive spikes on goals? → ||Serverless Computing||

**J76.** West Europe resilience across 3 isolated DCs? → ||Availability Zones||

**J77.** Advisor categories relevant to oversized VMs + unused disks + security vulnerability? → ||Cost Optimization||

**J78.** Data transfer when busy networks aren't an option? → ||Azure Data Box||

**J79.** Azure native IaC support via? → ||Azure Resource Manager||

**J80.** Store videos, audios, text — cost-effective and scalable? → ||Azure Blob Storage||

**J81.** Link virtual networks together? → ||Virtual Network Peering||

**J82.** Read-only lock on resource with existing delete lock? → ||Yes, subscription owner can||

**J83.** Developer forgets to deallocate VM — most direct cost impact? → ||Resource usage||

**J84.** Copies data across 3 AZs in primary region? → ||Zone Redundant Storage (ZRS)||

**J85.** Deploy VMs to 2+ AZs for DC failure protection? → ||Yes||

**J86.** TCO Calculator for long-term on-prem vs cloud savings pitch? → ||TCO Calculator||

**J87.** Hybrid cloud useful when regulations don't permit moving specific data to cloud? → ||Yes||

**J88.** RG can contain resources from multiple regions? → ||Yes||

**J89.** Shared responsibility for retail chain (VMs + managed DB): → ||Customer applies OS updates||

**J90.** Min distance between DCs in region pairs? → ||300 miles||

**J91.** Network segmentation between subnets, no VPN/public IPs? → ||VNet with NSGs applied to subnets||

**J92.** Resource can belong to more than one RG? → ||No||

**J93.** University: group VMs/storage, billing, campus-wide policies? → ||Resource Groups||

**J94.** Cloud Shell: Bash + PowerShell, browser-based, no local tools? → ||Full support for both Azure CLI and PowerShell||

**J95.** Max tags per Azure resource? → ||50||

**J96.** Blueprints: how it monitors deployments? → ||Preserves relationship between definition and assignment||

**J97.** Cost Management alert types? → ||Budget alerts||

**J98.** Filter network traffic between subnets? → ||Network Security Group (NSG)||

**J99.** Migrate CRM, need customization + minimize overhead? → ||PaaS||

**J100.** ARM template = JSON file auto-deploying resources? → ||ARM templates||

**J101.** Tags applied to RG inherited by resources? → ||No||

**J102.** Run legacy apps in cloud without modern auth? → ||Microsoft Entra Domain Services||

**J103.** VM → DB private connection, no public internet? → ||Private endpoint for DB + private IP for VM||

**J104.** Azure Functions: serverless + consumption-based? → ||Yes||

**J105.** Conditional Access for location-based policies (clients IP-restricted, staff stricter)? → ||Entra Conditional Access||

**J106.** Deploy Azure VM from macOS — which tools? → ||All: CLI, PowerShell, Cloud Shell, Portal||

**J107.** Full OS control in PaaS? → ||No||

**J108.** Fine-grained access management built on ARM? → ||RBAC||

**J109.** Retailer: single login + text code for sensitive data + biometric pilot? → ||SSO + MFA + Passwordless Authentication||

**J110.** Branch offices share sensitive info between locations? → ||VPN||

**J111.** RBAC at management group level: what occurs? → ||Permissions inherited by all sub-MGs, subscriptions, RGs, resources||

**J112.** High-availability VDI with scaling based on demand? → ||Azure Virtual Desktop + Scale Sets||

**J113.** Action to reduce Azure costs? → ||Reduce data transferred between regions||

**J114.** Public cloud characteristics: → ||Metered pricing||

**J115.** Service Health: configure alerts for active + upcoming issues? → ||Yes||

**J116.** Unstructured data, auto-index, multi-region writes? → ||Azure Cosmos DB||

**J117.** Pricing Calculator for monthly estimates + TCO for 5-year savings? → ||Pricing, TCO||

**J118.** Azure VNet + 3 VMs = IaaS implementation? → ||Yes||

**J119.** Streaming site with traffic bursts on new releases? → ||Elasticity||

**J120.** How do resource locks affect resources? → ||Prevent modifications but allow read access||

**J121.** Good usage of tags? → ||All of the above||

**J122.** Group/organize policies together? → ||Initiatives||

**J123.** Key difference between vertical and horizontal scaling? → ||Horizontal adjusts number of resources; vertical adjusts capabilities||

**J124.** Sudden high demand — adding more VMs/containers? → ||Horizontal scaling||

**J125.** Copies data 3× within single physical location? → ||LRS (Locally Redundant Storage)||

### Answers — Section J

| # | Answer | Explanation |
|---|---|---|
| J1 | **IaaS** | VMs = virtualized compute. You manage OS and apps. IaaS = renting infrastructure. (PT4) |
| J2 | **AzCopy** |  (PT4) |
| J3 | **Region Pair** |  (PT4) |
| J4 | **Yes** | Location = where metadata is stored. Resources inside can be in any region. (PT4) |
| J5 | **Data and Identities** | Regardless of IaaS/PaaS/SaaS, customer always owns data and identities. (PT4) |
| J6 | **Yes** |  (PT4) |
| J7 | **Azure Container Registry** |  (PT4) |
| J8 | **IaaS** | IaaS = customer manages OS, apps, data, network config. SaaS = least. PaaS = middle. (PT4) |
| J9 | **Dedicated intrusion detection system (IDS)** | Defense-in-depth = multiple layers. IDS monitors network for suspicious activity. (PT4) |
| J10 | **Azure Service Health** |  (PT4) |
| J11 | **Include multiple values for a single tag name** |  (PT4) |
| J12 | **Azure Arc** |  (PT4) |
| J13 | **Azure Service Health** |  (PT4) |
| J14 | **Budgets** | Budgets = set limits + alert notifications. NOT: auto-increase, suspend usage, or generate invoices. (PT4) |
| J15 | **Private cloud for financial institution** | Hospital needing full control over patient data → private/hybrid, not public. (PT4) |
| J16 | **No (True)** | Must apply individually or use Azure Policy for auto-tagging. (PT4) |
| J17 | **Fault Tolerance** | Redundancy, failover, backups = keep running when components fail. (PT4) |
| J18 | **External Identities** | B2B + B2C capabilities for managing outside users (customers, partners). (PT4) |
| J19 | **21Vianet** |  (PT4) |
| J20 | **No** | On-prem = direct physical control. Cloud = trust the provider for physical security. (PT4) |
| J21 | **Pay only for resources actually consumed** |  (PT4) |
| J22 | **Azure ExpressRoute** |  (PT4) |
| J23 | **Pay-as-you-go** |  (PT4) |
| J24 | **AKS + Azure Functions** |  (PT4) |
| J25 | **Prevent accidental deletion or modification** |  (PT4) |
| J26 | **Azure Container Instances** |  (PT4) |
| J27 | **Azure App Service, Azure SQL, Azure Storage** |  (PT4) |
| J28 | **No** | PowerAutomate ≠ PowerShell. PowerAutomate isn't an Azure deployment tool. (PT4) |
| J29 | **Azure DNS** |  (PT4) |
| J30 | **Yes** |  (PT4) |
| J31 | **No** | Azure DNS hosts domains, doesn't sell them. Buy from App Service domains or third-party registrar. (PT4) |
| J32 | **No** | Question doesn't specify cross-zone/cross-DC config. VMSS alone doesn't guarantee DC fault tolerance without explicit AZ configuration. (PT4) |
| J33 | **Securing VMs and access to them** |  (PT4) |
| J34 | **Clearly defines roles of CSP and customer in security** |  (PT4) |
| J35 | **Purview** |  (PT4) |
| J36 | **PaaS** |  (PT4) |
| J37 | **Azure Storage Explorer** |  (PT4) |
| J38 | **PaaS** |  (PT4) |
| J39 | **Virtual Network Peering** |  (PT4) |
| J40 | **PaaS, SaaS** |  (PT4) |
| J41 | **Management Groups with Resource Groups by business unit** |  (PT4) |
| J42 | **No** | ExpressRoute = dedicated private connection. NOT public internet. (PT4) |
| J43 | **Authentication** |  (PT4) |
| J44 | **PowerShell; Bash** |  (PT4) |
| J45 | **Ensure secure configurations of workloads and resources** |  (PT4) |
| J46 | **Scalability** |  (PT4) |
| J47 | **SAML** |  (PT4) |
| J48 | **Yes** |  (PT4) |
| J49 | **Multi-Tenancy** |  (PT4) |
| J50 | **Azure Functions** |  (PT4) |
| J51 | **Log Analytics** |  (PT4) |
| J52 | **No** |  (PT4) |
| J53 | **No** | Service Health notifies and advises. Cannot prevent service failures. (PT4) |
| J54 | **No** | Resources can connect to resources in other RGs. (PT4) |
| J55 | **Azure Files** |  (PT4) |
| J56 | **Yes** |  (PT4) |
| J57 | **Availability Zone** |  (PT4) |
| J58 | **Costs only during execution** |  (PT4) |
| J59 | **Budget alert is triggered** | NOT: auto-increase, suspend usage, or send invoice. (PT4) |
| J60 | **When you need additional VMs/compute** |  (PT4) |
| J61 | **CanNotDelete Lock** |  (PT4) |
| J62 | **Hybrid cloud** |  (PT4) |
| J63 | **Azure Service Health** |  (PT4) |
| J64 | **Azure Government** |  (PT4) |
| J65 | **Policy assignments** |  (PT4) |
| J66 | **Unlimited data storage** |  (PT4) |
| J67 | **A Subscription** | Hierarchy: Tenant → Subscription → Resource Group → Resource. (PT4) |
| J68 | **IaaS** |  (PT4) |
| J69 | **Azure Activity Log** |  (PT4) |
| J70 | **Public** |  (PT4) |
| J71 | **Virtual Network Peering** |  (PT4) |
| J72 | **Azure File Sync** |  (PT4) |
| J73 | **IaaS** |  (PT4) |
| J74 | **Azure Arc** |  (PT4) |
| J75 | **Serverless Computing** |  (PT4) |
| J76 | **Availability Zones** |  (PT4) |
| J77 | **Cost Optimization** |  (PT4) |
| J78 | **Azure Data Box** |  (PT4) |
| J79 | **Azure Resource Manager** |  (PT4) |
| J80 | **Azure Blob Storage** |  (PT4) |
| J81 | **Virtual Network Peering** |  (PT4) |
| J82 | **Yes, subscription owner can** |  (PT4) |
| J83 | **Resource usage** |  (PT4) |
| J84 | **Zone Redundant Storage (ZRS)** |  (PT4) |
| J85 | **Yes** |  (PT4) |
| J86 | **TCO Calculator** | ⚠️ Note: TCO Calculator deprecated August 2025. Current answer: Pricing Calculator. (PT4) |
| J87 | **Yes** |  (PT4) |
| J88 | **Yes** |  (PT4) |
| J89 | **Customer applies OS updates** |  (PT4) |
| J90 | **300 miles** |  (PT4) |
| J91 | **VNet with NSGs applied to subnets** |  (PT4) |
| J92 | **No** |  (PT4) |
| J93 | **Resource Groups** |  (PT4) |
| J94 | **Full support for both Azure CLI and PowerShell** |  (PT4) |
| J95 | **50** |  (PT4) |
| J96 | **Preserves relationship between definition and assignment** |  (PT4) |
| J97 | **Budget alerts** |  (PT4) |
| J98 | **Network Security Group (NSG)** |  (PT4) |
| J99 | **PaaS** |  (PT4) |
| J100 | **ARM templates** |  (PT4) |
| J101 | **No** |  (PT4) |
| J102 | **Microsoft Entra Domain Services** |  (PT4) |
| J103 | **Private endpoint for DB + private IP for VM** |  (PT4) |
| J104 | **Yes** |  (PT4) |
| J105 | **Entra Conditional Access** |  (PT4) |
| J106 | **All: CLI, PowerShell, Cloud Shell, Portal** |  (PT4) |
| J107 | **No** |  (PT4) |
| J108 | **RBAC** |  (PT4) |
| J109 | **SSO + MFA + Passwordless Authentication** |  (PT4) |
| J110 | **VPN** |  (PT4) |
| J111 | **Permissions inherited by all sub-MGs, subscriptions, RGs, resources** |  (PT4) |
| J112 | **Azure Virtual Desktop + Scale Sets** |  (PT4) |
| J113 | **Reduce data transferred between regions** |  (PT4) |
| J114 | **Metered pricing** |  (PT4) |
| J115 | **Yes** |  (PT4) |
| J116 | **Azure Cosmos DB** |  (PT4) |
| J117 | **Pricing, TCO** | ⚠️ TCO deprecated August 2025. (PT4) |
| J118 | **Yes** |  (PT4) |
| J119 | **Elasticity** |  (PT4) |
| J120 | **Prevent modifications but allow read access** |  (PT4) |
| J121 | **All of the above** |  (PT4) |
| J122 | **Initiatives** |  (PT4) |
| J123 | **Horizontal adjusts number of resources; vertical adjusts capabilities** |  (PT4) |
| J124 | **Horizontal scaling** |  (PT4) |
| J125 | **LRS (Locally Redundant Storage)** |  (PT4) |
---

## Section K — Practice Test 5

> **Source**: AZ-900 Udemy Practice Test 5 (90 questions)

**K1.** Optimize VM costs for resource-intensive workload? → ||Enable automatic scaling||

**K2.** Set up alerts for outages or autoscaling new instances? → ||Azure Monitor||

**K3.** SaaS allows access to underlying OS? → ||No||

**K4.** Deploy VMs to multiple RGs for DC failure protection? → ||No||

**K5.** Key advantage of ZRS? → ||Data accessible even if a zone becomes unavailable||

**K6.** Two options for replicating data within primary region? → ||LRS + ZRS||

**K7.** When is GRS recommended? → ||When protection from regional disasters is required||

**K8.** Valid Blob Storage tiers? → ||Hot||

**K9.** Notify when Azure spending reaches threshold? → ||Budgets||

**K10.** Migrate on-prem app, no manual admin/maintenance? → ||PaaS||

**K11.** NOT a cost-saving solution? → ||Load balancing VMs||

**K12.** DR replication cost factors? → ||All: # VMs, data amount, VM types, network bandwidth||

**K13.** Cloud services provide greater control over physical security vs on-prem? → ||No||

**K14.** Private connection to Azure, no public internet? → ||Azure ExpressRoute||

**K15.** Retailer automates VM deployments via standardized JSON config? → ||Azure Resource Manager (ARM)||

**K16.** Default spending limit for Azure Free account? → ||Yes||

**K17.** Prevent deletion OR modification of mission-critical resources? → ||ReadOnly lock||

**K18.** Azure free trial provides? → ||Credit for 30 days||

**K19.** Hybrid network: encrypted public internet + high-speed private? → ||Azure VPN Gateway||

**K20.** Gaming company: managed environment with databases/middleware, focus on coding? → ||PaaS||

**K21.** Main purpose of Pricing Calculator? → ||Estimate cost of provisioning resources||

**K22.** Diagnose VPN gateway connectivity issues? → ||Azure Network Watcher||

**K23.** Research institute: custom VMs with specific OS/libraries, fully managed by IT? → ||IaaS||

**K24.** Retailer: auto-scaling VMs + high outbound data to Asia + premium storage. Cost drivers? → ||Data egress||

**K25.** Each Azure subscription can trust multiple Active Directories? → ||False||

**K26.** Cloud Shell: run `az vm create` + PowerShell from browser, no local tools? → ||Yes||

**K27.** Sovereign regions: government agency, data within national boundaries, dedicated isolated region? → ||Sovereign||

**K28.** Resource locks: most restrictive lock in inheritance takes precedence? → ||Yes||

**K29.** Data transfer between two Azure regions free? → ||No||

**K30.** Example of IaaS in Azure? → ||Azure Virtual Machine||

**K31.** Track spending, set budgets, identify usage trends? → ||Azure Cost Analysis||

**K32.** Resource lock: prevent deletion + restrict to storage accounts during audit? → ||Resource locks||

**K33.** Real-time alerts about regional outage + tracks service issues/maintenance? → ||Azure Service Health — Yes||

**K34.** Create, assign, manage policies for compliance? → ||Azure Policy||

**K35.** Does NOT affect Azure costs? → ||Tags||

**K36.** Compare on-prem costs vs Azure costs? → ||TCO Calculator||

**K37.** University: tag VMs by department + analyze usage + recommend resizing? → ||Tags||

**K38.** Browser dashboard + CLI scripting + declarative resource definition? → ||Portal||

**K39.** Extend governance to on-prem + AWS Kubernetes? → ||Azure Arc||

**K40.** Create/manage private networks + connect to on-prem via VPN gateway? → ||Azure Virtual Network||

**K41.** Defender for Cloud: free assessments + paid threat detection if DC outage? → ||No||

**K42.** Suppliers use corporate credentials + customers use social media logins? → ||Entra B2B||

**K43.** Greatest security effort on customer? → ||IaaS||

**K44.** Provider ensures availability of underlying infrastructure? → ||Yes||

**K45.** Financial institution: hardware physically isolated, own data center, cloud-like virtualization? → ||Private cloud||

**K46.** TCO Calculator inputs? → ||Current infrastructure config||

**K47.** Web-based interface: monitor VMs, create storage, review costs? → ||Azure Portal||

**K48.** Store unstructured/semi-structured data? → ||Blob Storage||

**K49.** Tags automatically reduce expenses during low activity? → ||No||

**K50.** Streaming service: globally accessible during events + handle viewer spikes? → ||High availability + Scalability||

**K51.** Resiliency during planned maintenance? → ||Availability Zones||

**K52.** Track performance of VMs, containers, databases, apps? → ||Azure Monitor||

**K53.** VPN between two Azure VNets in different regions? → ||Site-to-Site (IPsec)||

**K54.** IaaS best for? → ||Lift-and-shift migration||

**K55.** Healthcare provider: rapid deployment + elasticity during surges + reduced costs from shared infra? → ||Agility||

**K56.** VMSS solves DC failure without specifying cross-DC config? → ||No||

**K57.** Isolate VM running mission-critical DB from other services? → ||Deploy to subnet + restrict with NSG||

**K58.** Finance team applies metadata labels for department cost tracking? → ||Tags||

**K59.** Delete lock on resource → attempt to delete RG → all resources deleted? → ||No||

**K60.** E-commerce: unpredictable surges, dynamic provisioning, release post-event? → ||Elasticity||

**K61.** Enforce all VMs must use specific OS version (hybrid)? → ||Azure Policy||

**K62.** Healthcare: compliance across resources + governance for SQL + SaaS apps? → ||Azure Policy||

**K63.** Entra ID can restrict access to known devices only? → ||True||

**K64.** 3 physically separate DCs in East US for streaming resilience? → ||Availability Zones||

**K65.** E-commerce: deploy VMs across isolated locations + group related resources? → ||Availability Zones||

**K66.** Cloud model eliminating upfront hardware purchases, charging on consumption? → ||Capital expenditure avoidance||

**K67.** Log in once, access multiple apps from different providers? → ||SSO||

**K68.** Data ingress to Azure is free — migration cost concern valid? → ||No||

**K69.** Advisor provides recommendations for ExpressRoute? → ||Yes||

**K70.** Best illustration of economy of scale? → ||Large provider offers lower per-unit costs serving millions||

**K71.** Multinational: sync on-prem AD to cloud + legacy apps via domain-joined protocols? → ||Entra ID||

**K72.** Every Azure region composed of a set of datacenters? → ||Yes||

**K73.** Resource can connect to resources in other RGs? → ||Yes||

**K74.** Multinational: data residency compliance + legacy on-prem integration + third-party infra for non-sensitive? → ||Hybrid cloud||

**K75.** Classify sensitive data + enforce retention + integrate on-prem file shares? → ||Microsoft Purview||

**K76.** Pricing Calculator details Azure costs; TCO compares cloud vs on-prem? → ||Yes||

**K77.** Azure Cost Management sets $5K cap and automatically halts resources? → ||No||

**K78.** PaaS can't be scaled without re-deploying? → ||False||

**K79.** Retailer: single login + text code + biometric pilot? → ||SSO + MFA + Passwordless||

**K80.** Reserved capacity vs consumption-based? → ||Reserved = consistent workloads; consumption = variable demand||

**K81.** Government agencies: shared cloud, stringent security, pooled resources? → ||Resources shared among specific group||

**K82.** Network traffic cost affected by? → ||Geography||

**K83.** Bank: corporate credentials + phone verification from trusted locations + developer VM rights? → ||Entra Conditional Access||

**K84.** Streaming site traffic bursts? → ||Elasticity||

**K85.** Cancel Azure subscription → resources immediately deleted? → ||No||

**K86.** Gaming company: VM logs + CPU alerts + app crash analysis? → ||Log Analytics||

**K87.** Moving VM from one region to another requires brief downtime? → ||Yes||

**K88.** Primary purpose of redundancy in Azure Storage? → ||High availability and durability in face of failures||

**K89.** Serverless characteristics? → ||Provider auto-scales based on events||

**K90.** Physical buildings housing networked servers globally? → ||Datacenters||

### Answers — Section K

| # | Answer | Explanation |
|---|---|---|
| K1 | **Enable automatic scaling** | Auto-scale adjusts VM instances/size based on demand. (PT5) |
| K2 | **Azure Monitor** |  (PT5) |
| K3 | **No** | SaaS = least control. Users interact with the app only. No OS access. (PT5) |
| K4 | **No** | RGs are logical containers, not physical redundancy. Use AZs or regions. (PT5) |
| K5 | **Data accessible even if a zone becomes unavailable** |  (PT5) |
| K6 | **LRS + ZRS** |  (PT5) |
| K7 | **When protection from regional disasters is required** |  (PT5) |
| K8 | **Hot** | NOT: Deep Sleep. NOT: Infrequently Accessed. (PT5) |
| K9 | **Budgets** |  (PT5) |
| K10 | **PaaS** | PaaS = managed platform. Provider handles OS, middleware, patching. (PT5) |
| K11 | **Load balancing VMs** | Load balancing = performance optimization, not cost saving. (PT5) |
| K12 | **All: # VMs, data amount, VM types, network bandwidth** |  (PT5) |
| K13 | **No** | On-prem = direct physical control. Cloud = trust the provider. (PT5) |
| K14 | **Azure ExpressRoute** |  (PT5) |
| K15 | **Azure Resource Manager (ARM)** |  (PT5) |
| K16 | **Yes** | $200 credit valid for 30 days. (PT5) |
| K17 | **ReadOnly lock** | CanNotDelete = prevents deletion only. ReadOnly = prevents both deletion AND modification. (PT5) |
| K18 | **Credit for 30 days** | NOT: unlimited access to all services. (PT5) |
| K19 | **Azure VPN Gateway** |  (PT5) |
| K20 | **PaaS** | PaaS reduces admin overhead. Agility = faster development cycles. (PT5) |
| K21 | **Estimate cost of provisioning resources** |  (PT5) |
| K22 | **Azure Network Watcher** |  (PT5) |
| K23 | **IaaS** | IaaS = max control + customization. Avoid physical server procurement delays. (PT5) |
| K24 | **Data egress** |  (PT5) |
| K25 | **False** | One subscription = one trusted Entra directory. Multiple subscriptions CAN trust the same directory. (PT5) |
| K26 | **Yes** |  (PT5) |
| K27 | **Sovereign** | Azure Government (US), Azure China (21Vianet), Azure Germany. (PT5) |
| K28 | **Yes** |  (PT5) |
| K29 | **No** |  (PT5) |
| K30 | **Azure Virtual Machine** | Event Hubs, Machine Learning, HDInsight = PaaS. (PT5) |
| K31 | **Azure Cost Analysis** |  (PT5) |
| K32 | **Resource locks** |  (PT5) |
| K33 | **Azure Service Health — Yes** |  (PT5) |
| K34 | **Azure Policy** |  (PT5) |
| K35 | **Tags** | Tags organize resources but don't incur costs or affect pricing. (PT5) |
| K36 | **TCO Calculator** | ⚠️ TCO deprecated August 2025. Use Pricing Calculator. (PT5) |
| K37 | **Tags** |  (PT5) |
| K38 | **Portal** |  (PT5) |
| K39 | **Azure Arc** |  (PT5) |
| K40 | **Azure Virtual Network** |  (PT5) |
| K41 | **No** | Defender detects security threats (malware, unauthorized access), NOT datacenter outages. (PT5) |
| K42 | **Entra B2B** |  (PT5) |
| K43 | **IaaS** | Shared responsibility: provider = physical infra + virtualization. Customer = app code + data. (PT5) |
| K44 | **Yes** |  (PT5) |
| K45 | **Private cloud** |  (PT5) |
| K46 | **Current infrastructure config** | NOT: subscription type. (PT5) |
| K47 | **Azure Portal** |  (PT5) |
| K48 | **Blob Storage** | NOT: Queue Storage (message queuing, not data storage). (PT5) |
| K49 | **No** | Tags = organizational metadata only. Don't affect resource behavior or costs. (PT5) |
| K50 | **High availability + Scalability** |  (PT5) |
| K51 | **Availability Zones** |  (PT5) |
| K52 | **Azure Monitor** |  (PT5) |
| K53 | **Site-to-Site (IPsec)** |  (PT5) |
| K54 | **Lift-and-shift migration** |  (PT5) |
| K55 | **Agility** |  (PT5) |
| K56 | **No** |  (PT5) |
| K57 | **Deploy to subnet + restrict with NSG** |  (PT5) |
| K58 | **Tags** |  (PT5) |
| K59 | **No** | Delete lock blocks the entire RG deletion. No partial deletion. (PT5) |
| K60 | **Elasticity** |  (PT5) |
| K61 | **Azure Policy** |  (PT5) |
| K62 | **Azure Policy** |  (PT5) |
| K63 | **True** | Device-based Conditional Access policies. (PT5) |
| K64 | **Availability Zones** |  (PT5) |
| K65 | **Availability Zones** |  (PT5) |
| K66 | **Capital expenditure avoidance** | CapEx → OpEx shift. (PT5) |
| K67 | **SSO** |  (PT5) |
| K68 | **No** |  (PT5) |
| K69 | **Yes** |  (PT5) |
| K70 | **Large provider offers lower per-unit costs serving millions** |  (PT5) |
| K71 | **Entra ID** |  (PT5) |
| K72 | **Yes** |  (PT5) |
| K73 | **Yes** |  (PT5) |
| K74 | **Hybrid cloud** |  (PT5) |
| K75 | **Microsoft Purview** |  (PT5) |
| K76 | **Yes** | ⚠️ TCO deprecated August 2025. (PT5) |
| K77 | **No** | Budgets send alerts only. Do NOT stop/pause resources. Need Azure Automation for that. (PT5) |
| K78 | **False** | PaaS can scale up/out dynamically without re-deployment. (PT5) |
| K79 | **SSO + MFA + Passwordless** |  (PT5) |
| K80 | **Reserved = consistent workloads; consumption = variable demand** |  (PT5) |
| K81 | **Resources shared among specific group** | = Community cloud characteristics. NOT: broadest public accessibility. NOT: necessarily third-party managed. (PT5) |
| K82 | **Geography** |  (PT5) |
| K83 | **Entra Conditional Access** |  (PT5) |
| K84 | **Elasticity** |  (PT5) |
| K85 | **No** | Resources deactivated, not immediately deleted. Waiting period before permanent deletion. (PT5) |
| K86 | **Log Analytics** |  (PT5) |
| K87 | **Yes** |  (PT5) |
| K88 | **High availability and durability in face of failures** |  (PT5) |
| K89 | **Provider auto-scales based on events** | NOT: customer manages OS. NOT: dedicated VMs per function. (PT5) |
| K90 | **Datacenters** |  (PT5) |
---

## Section L — Practice Test 6

> **Source**: AZ-900 Udemy Practice Test 6 (95 questions)

**L1.** Defender for Cloud alert — suspicious activity detected. What to do? → ||Investigate and take action to remediate||

**L2.** Azure Arc description? → ||Bridge extending Azure to datacenters, edge, multi-cloud||

**L3.** Key benefit of RBAC over traditional access control? → ||Assign permissions to roles, not individual users||

**L4.** Cloud Shell: run both Bash and PowerShell? → ||Yes||

**L5.** Resources managed by Azure Arc? → ||All: Windows/Linux servers, Kubernetes clusters, VMs||

**L6.** Automate deployments + IaC? → ||ARM Templates||

**L7.** Extremely strict data security + compliance requirements → best deployment model? → ||Private cloud||

**L8.** Migrate on-prem app, no manual admin? → ||PaaS||

**L9.** Download cost/usage data for monthly invoice? → ||Azure Cost Management||

**L10.** NSG associated with private endpoint — purpose? → ||Enforce access control rules on inbound/outbound traffic||

**L11.** Pay only for resources used, adjusting based on demand? → ||Consumption-based model||

**L12.** Cloud provides greater physical security control than on-prem? → ||No||

**L13.** Does NOT directly impact Azure costs? → ||Number of resources in same VNet||

**L14.** Two NoSQL storage solutions? → ||Azure Cosmos DB||

**L15.** Prevent deletion AND modification of mission-critical resources? → ||ReadOnly lock||

**L16.** Defense in depth: multiple layers to slow attack advance? → ||Defense in Depth||

**L17.** Collection of policy definitions grouped toward specific goal? → ||Azure Initiative||

**L18.** Explicit verification + least privilege + assume breach? → ||Zero Trust||

**L19.** Deploy VNet using PowerAutomate on Chromebook? → ||No||

**L20.** Custom VMs with specific OS/libraries, full IT management? → ||IaaS||

**L21.** Blob in archive tier — first action before accessing? → ||Rehydrate it||

**L22.** Planned maintenance in East US — real-time notifications? → ||Azure Service Health||

**L23.** If-then statements: if user wants resource, must complete action? → ||Conditional Access||

**L24.** Variable workloads + unpredictable spikes — best pricing combo? → ||Consumption-based for unpredictable + Reserved Instances for long-term predictable||

**L25.** Segment VNet into ___ + connect to another VNet via ___? → ||Subnet, Peering||

**L26.** NOT a feature of Azure Monitor? → ||Database management||

**L27.** Long-term predictable needs, fixed payments, avoid overpaying? → ||Reserved pricing model||

**L28.** Repeatedly deploy infrastructure consistently? → ||ARM templates||

**L29.** Set spending thresholds? → ||Azure Cost Management + Billing||

**L30.** Benefit of Azure Cloud Shell? → ||Eliminates need to install CLI locally||

**L31.** Trust users inside network by default, verify only external? → Zero Trust? → ||No||

**L32.** Public cloud = dedicated hardware per tenant? → ||No||

**L33.** Host web apps, API apps, WebJobs, mobile apps? → ||Azure App Service||

**L34.** Unified cloud-native app protection platform (CSPM + CWPP)? → ||Microsoft Defender for Cloud||

**L35.** Event-driven code, no server management, billed on execution time? → ||Serverless with consumption pricing||

**L36.** NOT a benefit of Azure Arc? → ||Centralized billing and cost management||

**L37.** Immutable infrastructure in IaC context? → ||Infrastructure recreated rather than modified in place||

**L38.** Support migration of Windows/SQL/Linux servers, databases, web apps, virtual desktops? → ||Azure Migrate||

**L39.** Best PaaS use case? → ||Deploy web app, developer focuses only on coding||

**L40.** Block employees from accessing apps from specific locations? → ||Entra Conditional Access||

**L41.** Implement system logic into code blocks triggered by events? → ||Azure Functions||

**L42.** Benefit of security + governance in cloud? → ||Enhanced ability to monitor and enforce policies for data access and compliance||

**L43.** Apply resource lock how? → ||Azure portal or Azure PowerShell||

**L44.** Analyzing logs + memory alerts + web app diagnostics? → ||Log Analytics||

**L45.** Default NSG rule action if none specified? → ||Deny||

**L46.** Enforce all VMs must have specific antivirus? → ||Azure Policy||

**L47.** Offline tier, rarely accessed, flexible latency? → ||Archive Tier||

**L48.** Archival data + minimal access + ZRS within region? → ||Archive tier with ZRS||

**L49.** External identities in Entra ID — primary purpose? → ||Allow external partners/customers to access your Azure resources||

**L50.** IaaS best for? → ||Lift-and-shift migration||

**L51.** Absorb unexpected traffic bursts, prevent server overload? → ||Azure Queue Storage||

**L52.** Government: dedicated region, screened personnel, strict compliance? → ||Sovereign Region||

**L53.** Multiple subscriptions inside a Management Group? → ||Yes||

**L54.** Subscriptions can be moved to another MG AND merged into one? → ||No||

**L55.** Streaming platform traffic spikes on new releases? → ||Elasticity||

**L56.** Suitable use case for resource lock? → ||Prevent accidental deletion of critical storage account||

**L57.** Lock: modify but not delete? → ||CanNotDelete lock||

**L58.** Manage multiple subscriptions? → ||Management Groups||

**L59.** Many subscriptions — efficiently manage access/policies/compliance? → ||Azure Management Groups||

**L60.** Auto-scaling web servers + fault-tolerant DB VMs + remote desktops? → ||VMSS||

**L61.** Imperative IaC: Bash/PowerShell scripts, explicit commands? → ||Imperative||

**L62.** Async replication across Azure regions for DR? → ||Cross-region replication||

**L63.** NOT a feature of Service Health? → ||Tracks and resolves performance issues for applications||

**L64.** Shared responsibility: cloud provider responsible for? → ||Physical security of data centers||

**L65.** B2B collaboration use case? → ||Granting external vendors access to shared project workspace||

**L66.** Azure Pay-As-You-Go = which expenditure model? → ||Operational (OpEx)||

**L67.** Network interface using private IP from your VNet? → ||Private endpoint||

**L68.** Control underlying OS and middleware? → ||IaaS||

**L69.** Alert rule in Azure Monitor: monitors telemetry, checks condition, triggers action? → ||Alert rule||

**L70.** Understand app performance + proactively identify issues? → ||Azure Monitor||

**L71.** Resource lock can block subscription cancellation? → ||False||

**L72.** Adjusting capabilities (CPU/RAM) of resources? → ||Vertical scaling||

**L73.** Services accessible through private endpoints? → ||All: Storage, Key Vault, App Service, SQL Database||

**L74.** Reserved capacity vs consumption-based? → ||Reserved = consistent workloads; consumption = variable demand||

**L75.** CSPM + CWPP for Azure, on-prem, AWS, GCP? → ||Microsoft Defender for Cloud||

**L76.** Classify sensitive data across Blob Storage + on-prem SQL for compliance? → ||Azure Purview||

**L77.** Protocol for federated authentication in Entra ID? → ||SAML||

**L78.** Migrate web app, no manual admin? → ||PaaS||

**L79.** Extend on-prem networks to Microsoft cloud over private connection? → ||Azure ExpressRoute||

**L80.** Government = private cloud for isolation; media company = public cloud for global reach? → ||Private, Public||

**L81.** Unstructured data + blobs + file shares + single region + high performance? → ||General-purpose v2 with LRS||

**L82.** IaC independent files containing resources to deploy together? → ||Modules||

**L83.** Declarative IaC: specify desired outcome, not how? → ||Declarative||

**L84.** Resources provisioned only when needed, auto-scale, costs tied to usage? → ||Azure Functions with serverless compute||

**L85.** Transfer on-prem data to Blob storage when network constraints make wire upload unrealistic? → ||Azure Data Box||

**L86.** Reduce overhead of manually assigning permissions to resources? → ||Azure Resource Manager||

**L87.** Migrate on-prem VMs to Azure without downtime? → ||Azure Site Recovery||

**L88.** DSL with declarative syntax to deploy Azure resources? → ||Bicep||

**L89.** Calculate estimated hourly/monthly Azure costs? → ||Azure Pricing Calculator||

### Answers — Section L

| # | Answer | Explanation |
|---|---|---|
| L1 | **Investigate and take action to remediate** |  (PT6) |
| L2 | **Bridge extending Azure to datacenters, edge, multi-cloud** |  (PT6) |
| L3 | **Assign permissions to roles, not individual users** |  (PT6) |
| L4 | **Yes** |  (PT6) |
| L5 | **All: Windows/Linux servers, Kubernetes clusters, VMs** |  (PT6) |
| L6 | **ARM Templates** |  (PT6) |
| L7 | **Private cloud** |  (PT6) |
| L8 | **PaaS** |  (PT6) |
| L9 | **Azure Cost Management** |  (PT6) |
| L10 | **Enforce access control rules on inbound/outbound traffic** |  (PT6) |
| L11 | **Consumption-based model** |  (PT6) |
| L12 | **No** |  (PT6) |
| L13 | **Number of resources in same VNet** |  (PT6) |
| L14 | **Azure Cosmos DB** |  (PT6) |
| L15 | **ReadOnly lock** |  (PT6) |
| L16 | **Defense in Depth** |  (PT6) |
| L17 | **Azure Initiative** |  (PT6) |
| L18 | **Zero Trust** |  (PT6) |
| L19 | **No** | PowerAutomate ≠ PowerShell. Not an Azure deployment tool. (PT6) |
| L20 | **IaaS** |  (PT6) |
| L21 | **Rehydrate it** |  (PT6) |
| L22 | **Azure Service Health** |  (PT6) |
| L23 | **Conditional Access** |  (PT6) |
| L24 | **Consumption-based for unpredictable + Reserved Instances for long-term predictable** |  (PT6) |
| L25 | **Subnet, Peering** |  (PT6) |
| L26 | **Database management** |  (PT6) |
| L27 | **Reserved pricing model** |  (PT6) |
| L28 | **ARM templates** |  (PT6) |
| L29 | **Azure Cost Management + Billing** |  (PT6) |
| L30 | **Eliminates need to install CLI locally** |  (PT6) |
| L31 | **No** | Zero Trust = never trust, always verify — regardless of location. (PT6) |
| L32 | **No** | Public cloud = shared infrastructure among tenants. (PT6) |
| L33 | **Azure App Service** |  (PT6) |
| L34 | **Microsoft Defender for Cloud** |  (PT6) |
| L35 | **Serverless with consumption pricing** |  (PT6) |
| L36 | **Centralized billing and cost management** |  (PT6) |
| L37 | **Infrastructure recreated rather than modified in place** |  (PT6) |
| L38 | **Azure Migrate** |  (PT6) |
| L39 | **Deploy web app, developer focuses only on coding** |  (PT6) |
| L40 | **Entra Conditional Access** |  (PT6) |
| L41 | **Azure Functions** |  (PT6) |
| L42 | **Enhanced ability to monitor and enforce policies for data access and compliance** |  (PT6) |
| L43 | **Azure portal or Azure PowerShell** |  (PT6) |
| L44 | **Log Analytics** |  (PT6) |
| L45 | **Deny** |  (PT6) |
| L46 | **Azure Policy** |  (PT6) |
| L47 | **Archive Tier** |  (PT6) |
| L48 | **Archive tier with ZRS** |  (PT6) |
| L49 | **Allow external partners/customers to access your Azure resources** |  (PT6) |
| L50 | **Lift-and-shift migration** |  (PT6) |
| L51 | **Azure Queue Storage** |  (PT6) |
| L52 | **Sovereign Region** |  (PT6) |
| L53 | **Yes** |  (PT6) |
| L54 | **No** | Can move between MGs, but CANNOT merge subscriptions. (PT6) |
| L55 | **Elasticity** |  (PT6) |
| L56 | **Prevent accidental deletion of critical storage account** |  (PT6) |
| L57 | **CanNotDelete lock** |  (PT6) |
| L58 | **Management Groups** |  (PT6) |
| L59 | **Azure Management Groups** |  (PT6) |
| L60 | **VMSS** |  (PT6) |
| L61 | **Imperative** |  (PT6) |
| L62 | **Cross-region replication** |  (PT6) |
| L63 | **Tracks and resolves performance issues for applications** | That's Application Insights / Azure Monitor, not Service Health. (PT6) |
| L64 | **Physical security of data centers** |  (PT6) |
| L65 | **Granting external vendors access to shared project workspace** |  (PT6) |
| L66 | **Operational (OpEx)** |  (PT6) |
| L67 | **Private endpoint** |  (PT6) |
| L68 | **IaaS** |  (PT6) |
| L69 | **Alert rule** |  (PT6) |
| L70 | **Azure Monitor** |  (PT6) |
| L71 | **False** | Locks don't block subscription cancellation. Azure deactivates resources instead. (PT6) |
| L72 | **Vertical scaling** |  (PT6) |
| L73 | **All: Storage, Key Vault, App Service, SQL Database** |  (PT6) |
| L74 | **Reserved = consistent workloads; consumption = variable demand** |  (PT6) |
| L75 | **Microsoft Defender for Cloud** |  (PT6) |
| L76 | **Azure Purview** |  (PT6) |
| L77 | **SAML** |  (PT6) |
| L78 | **PaaS** |  (PT6) |
| L79 | **Azure ExpressRoute** |  (PT6) |
| L80 | **Private, Public** |  (PT6) |
| L81 | **General-purpose v2 with LRS** |  (PT6) |
| L82 | **Modules** |  (PT6) |
| L83 | **Declarative** |  (PT6) |
| L84 | **Azure Functions with serverless compute** |  (PT6) |
| L85 | **Azure Data Box** |  (PT6) |
| L86 | **Azure Resource Manager** | ARM enables RBAC at resource group level for collective permission assignment. (PT6) |
| L87 | **Azure Site Recovery** |  (PT6) |
| L88 | **Bicep** |  (PT6) |
| L89 | **Azure Pricing Calculator** |  (PT6) |
---

## Section M — Practice Test 7

> **Source**: AZ-900 Udemy Practice Test 7 (85 questions)

**M1.** RBAC key benefit? → ||Assign permissions to roles, not individual users||

**M2.** Large datasets in Blob Storage, cost-effective while gathering more data? → ||Cool tier||

**M3.** Link VNets together? → ||Virtual network peering||

**M4.** New VM — billed separately for local disk storage? → ||No||

**M5.** ARM templates key advantage? → ||Consistent and repeatable deployments||

**M6.** Self-service sign-up for customers? → ||Azure B2C||

**M7.** Azure Policy = default-allow-and-explicit-deny (unlike RBAC)? → ||Yes||

**M8.** Extremely strict data security + compliance? → ||Private cloud||

**M9.** Azure Data Box: transfer data FROM Azure to on-prem or other clouds? → ||True||

**M10.** Multiple offices sharing files, minimize latency, central copy? → ||Azure File Sync||

**M11.** Archive tier — must do what before accessing? → ||Rehydrate it||

**M12.** Azure Arc enables governance across hybrid how? → ||Extending Azure Policy and Blueprints to on-prem + multi-cloud||

**M13.** Migrate on-prem VMs to PAYG subscription = which expenditure? → ||Operational (OpEx)||

**M14.** Two factors affecting VM costs? → ||VM size||

**M15.** Estimate cost savings migrating to Azure? → ||Azure TCO Calculator||

**M16.** Shared responsibility — app code security: IaaS=Customer, PaaS=Customer, SaaS=Microsoft? → ||Customer, Customer, Microsoft||

**M17.** IaC key advantage? → ||Enables version control and automated provisioning||

**M18.** Series of mechanisms to slow attack advance, multiple layers? → ||Defense in Depth||

**M19.** Collection of policy definitions grouped toward goal? → ||Azure Initiative||

**M20.** Zero Trust: explicit verification + least privilege + assume breach? → ||Zero Trust||

**M21.** Deploy VNet via PowerAutomate on Chromebook? → ||No||

**M22.** Azure Functions flat monthly fee = consumption-based? → ||False||

**M23.** Data Box family: Data Box, Disk, Heavy, and ___? → ||Edge||

**M24.** Key benefit of Azure B2C? → ||Customizable user experiences for sign-up/sign-in||

**M25.** Entra ID vs RBAC — which for managing user identities for cloud app? → ||Entra ID||

**M26.** Variable workloads + unpredictable spikes — best combo? → ||Consumption-based + Reserved Instances||

**M27.** 2+ Scale Sets without cross-DC config solves DC failure? → ||No||

**M28.** NOT a feature of Azure Monitor? → ||Database management||

**M29.** Long-term predictable, fixed payments, avoid overpaying? → ||Reserved pricing||

**M30.** Private connection, data doesn't travel over internet? → ||Azure ExpressRoute||

**M31.** Estimated hourly/monthly Azure costs? → ||Azure Pricing Calculator||

**M32.** Async message queuing + absorb traffic bursts? → ||Azure Queue Storage||

**M33.** Valid payment options for Azure? → ||Azure Website||

**M34.** Remote employees, virtualized desktops, existing Windows licenses, BYOD? → ||Azure Virtual Desktop||

**M35.** Azure hierarchy? → ||Management Group → Subscription → Resource Group||

**M36.** Private connections between Azure DCs and on-prem/colocation? → ||Azure ExpressRoute||

**M37.** Microservice architecture — break solutions into smaller independent pieces? → ||Containers||

**M38.** Azure Locks can be set at ___ level? → ||Subscription||

**M39.** Does NOT affect storage billing? → ||Data ingress within same AZ||

**M40.** PaaS description? → ||Host app, manage OS, don't manage underlying hardware||

**M41.** System continues operating without disruption during failure? → ||Fault tolerance||

**M42.** Free transfers? → ||Intra-region||

**M43.** Best PaaS use case? → ||Deploy web app, focus only on coding||

**M44.** Primary goal of IaC? → ||Manage and provision infrastructure using code||

**M45.** Cloud-first approach example? → ||Startup deploys entire infra on public cloud||

**M46.** Purview: data lineage and impact analysis? → ||Tools for visualizing data flow, origins, dependencies||

**M47.** Migrating to public cloud reduces which expense? → ||Capital Expense (CapEx)||

**M48.** Shared responsibility model best description? → ||Both provider and customer share responsibility; provider=infrastructure, customer=apps+data||

**M49.** PaaS: who secures underlying OS? → ||Microsoft||

**M50.** Upload/download blobs, files, queues, tables + configure permissions/tiers? → ||Azure Storage Explorer||

**M51.** Entra ID + RBAC relationship? → ||Complementary functionality||

**M52.** NOT a valid way to connect on-prem to Azure? → ||Network virtual appliances||

**M53.** Pre-built CRM, no infra management? → ||SaaS||

**M54.** All data copied to storage account auto-backed up to another DC? → ||No||

**M55.** Organization's ability to protect from/respond to security threats? → ||Security posture||

**M56.** Flexible datasets (user data, address books, device info, metadata)? → ||Azure Table Storage||

**M57.** Rapidly deploy across multiple regions? → ||Geographic distribution||

**M58.** Block access from untrusted/unknown locations? → ||Conditional Access||

**M59.** Private cloud for on-prem + hybrid cloud for Azure integration? → ||Private, Hybrid||

**M60.** Data Box security features? → ||Data-at-rest encryption||

**M61.** ARM template used for? → ||Declare desired state of resources and dependencies||

**M62.** Workload tolerates interruptions, flexible execution time, save costs? → ||Spot Pricing||

**M63.** Migrate interconnected servers — which Azure Migrate features? → ||Server Assessment + Server Migration||

**M64.** Centralize file shares in Azure Files + Windows file server compatibility? → ||Azure File Sync||

**M65.** Private endpoints primary benefit? → ||Improved security by bypassing public internet||

**M66.** Private endpoints provide secure access OVER public internet? → ||False||

**M67.** Transfer data to cloud: archival, DR, cloud-scale processing? → ||Azure Data Box Gateway||

**M68.** Choosing Data Box device — key factor? → ||Total amount of data to transfer||

**M69.** Business-critical workloads for 3 years, most cost savings? → ||Purchasing Reservations||

**M70.** Physical security of data centers = whose responsibility? → ||Cloud provider||

**M71.** Purview for regulatory compliance? → ||Classify and manage data to meet regulatory requirements||

**M72.** Azure File Sync supported tiers? → ||Both Premium and Standard||

**M73.** Can you add physical servers to public cloud? → ||No||

**M74.** Healthcare: encrypt data + HIPAA compliance + automate VM deployment? → ||Security||

**M75.** Enterprise big data analytics + hierarchical namespace on Blob? → ||Azure Data Lake Storage Gen2||

**M76.** Most flexible cloud service category? → ||IaaS||

**M77.** Purview for data collaboration? → ||Discover and share trusted data sources across teams||

**M78.** Reserved capacity vs consumption-based? → ||Reserved = consistent; consumption = variable||

**M79.** Data Box security: data unreadable if intercepted during shipping? → ||Data-at-rest encryption||

**M80.** B2C in Entra ID focused on internal employee collaboration? → ||False||

**M81.** Retailer: functional during failures + scale during holidays? → ||High availability||

**M82.** Streaming site: spikes on new movies, moderate otherwise? → ||Elasticity||

**M83.** Entra ID feature: use existing corporate credentials for cloud apps? → ||Entra B2C||

**M84.** Hybrid cloud requires resources in public cloud + on-prem/private? → ||Yes||

**M85.** CLI utility to copy blobs/files to/from storage account? → ||AzCopy||

**M86.** Government = private; media = public? → ||Private, Public||

### Answers — Section M

| # | Answer | Explanation |
|---|---|---|
| M1 | **Assign permissions to roles, not individual users** |  (PT7) |
| M2 | **Cool tier** |  (PT7) |
| M3 | **Virtual network peering** |  (PT7) |
| M4 | **No** | Azure doesn't charge for local/resource disk storage. (PT7) |
| M5 | **Consistent and repeatable deployments** |  (PT7) |
| M6 | **Azure B2C** |  (PT7) |
| M7 | **Yes** |  (PT7) |
| M8 | **Private cloud** |  (PT7) |
| M9 | **True** |  (PT7) |
| M10 | **Azure File Sync** |  (PT7) |
| M11 | **Rehydrate it** |  (PT7) |
| M12 | **Extending Azure Policy and Blueprints to on-prem + multi-cloud** |  (PT7) |
| M13 | **Operational (OpEx)** |  (PT7) |
| M14 | **VM size** |  (PT7) |
| M15 | **Azure TCO Calculator** | ⚠️ TCO deprecated August 2025. Use Pricing Calculator. (PT7) |
| M16 | **Customer, Customer, Microsoft** |  (PT7) |
| M17 | **Enables version control and automated provisioning** |  (PT7) |
| M18 | **Defense in Depth** |  (PT7) |
| M19 | **Azure Initiative** |  (PT7) |
| M20 | **Zero Trust** |  (PT7) |
| M21 | **No** |  (PT7) |
| M22 | **False** | Functions = pay-per-execution, NOT flat fee. (PT7) |
| M23 | **Edge** |  (PT7) |
| M24 | **Customizable user experiences for sign-up/sign-in** |  (PT7) |
| M25 | **Entra ID** |  (PT7) |
| M26 | **Consumption-based + Reserved Instances** |  (PT7) |
| M27 | **No** |  (PT7) |
| M28 | **Database management** |  (PT7) |
| M29 | **Reserved pricing** |  (PT7) |
| M30 | **Azure ExpressRoute** |  (PT7) |
| M31 | **Azure Pricing Calculator** |  (PT7) |
| M32 | **Azure Queue Storage** |  (PT7) |
| M33 | **Azure Website** |  (PT7) |
| M34 | **Azure Virtual Desktop** |  (PT7) |
| M35 | **Management Group → Subscription → Resource Group** |  (PT7) |
| M36 | **Azure ExpressRoute** |  (PT7) |
| M37 | **Containers** |  (PT7) |
| M38 | **Subscription** |  (PT7) |
| M39 | **Data ingress within same AZ** | Billing factors: region, account type, access tier, capacity, redundancy, transactions, data egress. (PT7) |
| M40 | **Host app, manage OS, don't manage underlying hardware** |  (PT7) |
| M41 | **Fault tolerance** |  (PT7) |
| M42 | **Intra-region** |  (PT7) |
| M43 | **Deploy web app, focus only on coding** |  (PT7) |
| M44 | **Manage and provision infrastructure using code** |  (PT7) |
| M45 | **Startup deploys entire infra on public cloud** |  (PT7) |
| M46 | **Tools for visualizing data flow, origins, dependencies** |  (PT7) |
| M47 | **Capital Expense (CapEx)** |  (PT7) |
| M48 | **Both provider and customer share responsibility; provider=infrastructure, customer=apps+data** |  (PT7) |
| M49 | **Microsoft** |  (PT7) |
| M50 | **Azure Storage Explorer** |  (PT7) |
| M51 | **Complementary functionality** |  (PT7) |
| M52 | **Network virtual appliances** | Valid: Point-to-Site VPN, Site-to-Site VPN, ExpressRoute. NVAs filter traffic, don't connect to Azure. (PT7) |
| M53 | **SaaS** |  (PT7) |
| M54 | **No** | Depends on replication config. LRS = same DC only. GRS = cross-region. (PT7) |
| M55 | **Security posture** |  (PT7) |
| M56 | **Azure Table Storage** |  (PT7) |
| M57 | **Geographic distribution** |  (PT7) |
| M58 | **Conditional Access** |  (PT7) |
| M59 | **Private, Hybrid** |  (PT7) |
| M60 | **Data-at-rest encryption** |  (PT7) |
| M61 | **Declare desired state of resources and dependencies** |  (PT7) |
| M62 | **Spot Pricing** |  (PT7) |
| M63 | **Server Assessment + Server Migration** |  (PT7) |
| M64 | **Azure File Sync** |  (PT7) |
| M65 | **Improved security by bypassing public internet** | Private endpoints bypass the public internet entirely. (PT7) |
| M66 | **False** |  (PT7) |
| M67 | **Azure Data Box Gateway** |  (PT7) |
| M68 | **Total amount of data to transfer** |  (PT7) |
| M69 | **Purchasing Reservations** |  (PT7) |
| M70 | **Cloud provider** |  (PT7) |
| M71 | **Classify and manage data to meet regulatory requirements** |  (PT7) |
| M72 | **Both Premium and Standard** |  (PT7) |
| M73 | **No** | Only virtual servers. Physical servers in public cloud = not possible. (PT7) |
| M74 | **Security** |  (PT7) |
| M75 | **Azure Data Lake Storage Gen2** |  (PT7) |
| M76 | **IaaS** |  (PT7) |
| M77 | **Discover and share trusted data sources across teams** |  (PT7) |
| M78 | **Reserved = consistent; consumption = variable** |  (PT7) |
| M79 | **Data-at-rest encryption** |  (PT7) |
| M80 | **False** | B2C = customer-facing. B2B = partner collaboration. (PT7) |
| M81 | **High availability** |  (PT7) |
| M82 | **Elasticity** |  (PT7) |
| M83 | **Entra B2C** |  (PT7) |
| M84 | **Yes** |  (PT7) |
| M85 | **AzCopy** |  (PT7) |
| M86 | **Private, Public** |  (PT7) |
---

## Section N — Practice Test 8

> **Source**: AZ-900 Udemy Practice Test 8 (80 questions)

**N1.** Own infrastructure + own datacenter = CapEx? → ||Yes||

**N2.** Export data from Azure to on-prem (government regulations)? → ||Azure Data Box||

**N3.** B2C: customers sign up/sign in with social accounts? → ||Entra ID B2C||

**N4.** Enforce all resources must have specific tags? → ||Azure Policy||

**N5.** Azure application platform example? → ||Azure App Service||

**N6.** Thousands of identical VMs + deploy across AZs? → ||VM Scale Sets||

**N7.** MFA: how does it enhance security? → ||Password + code from Authenticator app||

**N8.** Private cloud: extremely strict security + compliance? → ||Private cloud||

**N9.** Purview: data security + compliance? → ||Classify and protect sensitive data, ensure compliance||

**N10.** SQL DB resource isolation from other Azure resources? → ||Deploy to different VNet + use NSGs||

**N11.** Archive tier — access data? → ||Must rehydrate first||

**N12.** Entra B2B benefit? → ||Controlled access to specified resources while maintaining security||

**N13.** Migrate VMs to PAYG = which expenditure? → ||Operational (OpEx)||

**N14.** Extend on-prem with Azure services = which cloud? → ||Hybrid cloud||

**N15.** Unlimited resources in a subscription? → ||False||

**N16.** REST APIs for Blob, Queue, Table, File services? → ||True (False that there's no programmatic access)||

**N17.** Lock inheritance: most UNRESTRICTIVE takes precedence? → ||No||

**N18.** Common IaC language? → ||YAML||

**N19.** Multiple layers to slow attack advance? → ||Defense in Depth||

**N20.** Manage access/policies/compliance for multiple subscriptions? → ||Management Groups||

**N21.** Zero Trust: explicit verification + least privilege + assume breach? → ||Zero Trust||

**N22.** VMs highly available + automatic failover on hardware failure? → ||Availability Zones||

**N23.** Azure Functions flat monthly fee = consumption-based? → ||False||

**N24.** Data Box family: Box, Disk, Heavy, ___? → ||Edge||

**N25.** B2C key benefit? → ||Customizable sign-up/sign-in experiences||

**N26.** Entra ID vs RBAC — managing user identities for cloud app? → ||Entra ID||

**N27.** Each subscription can have multiple account administrators? → ||No||

**N28.** Azure Migrate: discover/assess physical servers? → ||Agent-based discovery||

**N29.** 2+ Scale Sets without cross-DC config for DC failure? → ||No||

**N30.** Arc-enabled Kubernetes key benefit? → ||Manage/configure clusters across multiple environments||

**N31.** Private connection, no internet? → ||Azure ExpressRoute||

**N32.** Containerized apps + CI/CD + enterprise security? → ||Azure Kubernetes (AKS)||

**N33.** Arc-enabled data services primary role? → ||Extend Azure data services to on-prem + multi-cloud||

**N34.** Public clouds: shared among multiple customers, managed by provider? → ||True||

**N35.** Highest durability (16 nines)? → ||GRS||

**N36.** Deploy VMs to 2+ regions for DC failure? → ||Yes||

**N37.** All resources in RG must be same region? → ||No||

**N38.** Containers for microservices? → ||Containers||

**N39.** PAYG = CapEx? → ||No (OpEx)||

**N40.** Azure Migrate for modernization + assessment? → ||Azure Migrate||

**N41.** Company using Azure, no physical infra = which cloud? → ||Public cloud||

**N42.** PaaS description? → ||Host app + manage OS, don't manage hardware||

**N43.** Azure Blueprints to scale governance? → ||Blueprints||

**N44.** Fault tolerance: system continues without disruption during failure? → ||Fault tolerance||

**N45.** Estimate cost savings migrating to Azure? → ||Azure TCO Calculator||

**N46.** Best PaaS use case? → ||Deploy web app, focus on coding||

**N47.** Social Insurance Number + fingerprint = valid MFA? → ||No||

**N48.** Cloud-first: startup deploys entire infra on public cloud? → ||Correct||

**N49.** Azure Policy Initiative definition? → ||Package/deploy collection of policy definitions as single entity||

**N50.** Subscriptions serve as unit of? → ||All: Management + Billing + Scale||

**N51.** Azure Web App + on-prem Oracle DB = which cloud? → ||Hybrid||

**N52.** Shared responsibility best description? → ||Provider = infrastructure; customer = apps + data||

**N53.** Recover deleted files with File Sync? → ||Recover from Azure File share using Azure Backup||

**N54.** Defense contractor (isolated infra) + retailer (scale during peaks)? → ||Private, Public||

**N55.** Service incidents + planned maintenance notifications? → ||Azure Service Health||

**N56.** NOT a compute service? → ||Azure Cosmos DB||

**N57.** IaaS vs PaaS? → ||IaaS = control VMs/OS; PaaS = abstracts infra, focus on app dev||

**N58.** Pre-built CRM, no infra management? → ||SaaS||

**N59.** NSG: security rules allow/deny inbound/outbound traffic? → ||Network Security Group||

**N60.** First step to use Azure Storage? → ||Create a Storage Account||

**N61.** Purview across multi-cloud? → ||Unified solution to manage/govern data across cloud + on-prem||

**N62.** Multiple instances of app on single host? → ||Containers||

**N63.** Reserved VM Instances = OpEx? → ||No (CapEx — upfront payment)||

**N64.** ARM template describes? → ||Desired state of resources + configuration||

**N65.** Private cloud for on-prem + hybrid for Azure integration? → ||Private, Hybrid||

**N66.** Basic building blocks of Azure? → ||Resources||

**N67.** PaaS shared responsibility? → ||Provider = infrastructure; customer = app code + data||

**N68.** Azure Files: can access from anywhere in the world? → ||Yes (No = incorrect statement)||

**N69.** Two VNets (East US + West US) peered: which aspects? → ||Cross-region connectivity||

**N70.** Identify groups generating biggest costs? → ||Tags||

**N71.** Two subscription boundary types? → ||Access control boundary||

**N72.** REST-based web APIs, any language/framework? → ||Azure App Service||

**N73.** Quickly locate resources by workload/environment/ownership? → ||Tags||

**N74.** Data Box import scenarios? → ||One-time large migration||

**N75.** B2C "policy" definition? → ||Customized rules/behaviors for customer identity interactions||

**N76.** Isolated network in Azure, no public internet exposure? → ||Azure Virtual Network||

**N77.** IaaS: NOT provider's responsibility? → ||VM patching and maintenance||

**N78.** Minimum data size for Data Box (limited network)? → ||40 TB||

**N79.** Multiple billing reports per subscription? → ||False||

**N80.** AKS belongs to which category? → ||PaaS||

**N81.** Cool tier stores data offline + highest rehydration costs? → ||False||

**N82.** Most flexible cloud service? → ||IaaS||

**N83.** RBAC applied to a ___? → ||Scope||

**N84.** NOT a cost-saving solution? → ||Shutting down VMs at night||

**N85.** Enforce MFA for ALL users via Authenticator + phone + SMS? → ||No||

**N86.** Serverless primary advantage? → ||Pay for execution time, no server management||

**N87.** SDKs for SQL/MongoDB/Cassandra + instant elasticity + NoSQL? → ||Azure Cosmos DB||

### Answers — Section N

| # | Answer | Explanation |
|---|---|---|
| N1 | **Yes** |  (PT8) |
| N2 | **Azure Data Box** |  (PT8) |
| N3 | **Entra ID B2C** |  (PT8) |
| N4 | **Azure Policy** |  (PT8) |
| N5 | **Azure App Service** |  (PT8) |
| N6 | **VM Scale Sets** |  (PT8) |
| N7 | **Password + code from Authenticator app** | Something you know + something you have (or biometric). (PT8) |
| N8 | **Private cloud** |  (PT8) |
| N9 | **Classify and protect sensitive data, ensure compliance** |  (PT8) |
| N10 | **Deploy to different VNet + use NSGs** |  (PT8) |
| N11 | **Must rehydrate first** |  (PT8) |
| N12 | **Controlled access to specified resources while maintaining security** |  (PT8) |
| N13 | **Operational (OpEx)** |  (PT8) |
| N14 | **Hybrid cloud** |  (PT8) |
| N15 | **False** |  (PT8) |
| N16 | **True (False that there's no programmatic access)** |  (PT8) |
| N17 | **No** | Most RESTRICTIVE takes precedence. (PT8) |
| N18 | **YAML** |  (PT8) |
| N19 | **Defense in Depth** |  (PT8) |
| N20 | **Management Groups** |  (PT8) |
| N21 | **Zero Trust** |  (PT8) |
| N22 | **Availability Zones** |  (PT8) |
| N23 | **False** |  (PT8) |
| N24 | **Edge** |  (PT8) |
| N25 | **Customizable sign-up/sign-in experiences** |  (PT8) |
| N26 | **Entra ID** |  (PT8) |
| N27 | **No** | Only 1 account admin per subscription. (PT8) |
| N28 | **Agent-based discovery** |  (PT8) |
| N29 | **No** |  (PT8) |
| N30 | **Manage/configure clusters across multiple environments** |  (PT8) |
| N31 | **Azure ExpressRoute** |  (PT8) |
| N32 | **Azure Kubernetes (AKS)** |  (PT8) |
| N33 | **Extend Azure data services to on-prem + multi-cloud** |  (PT8) |
| N34 | **True** |  (PT8) |
| N35 | **GRS** |  (PT8) |
| N36 | **Yes** |  (PT8) |
| N37 | **No** |  (PT8) |
| N38 | **Containers** |  (PT8) |
| N39 | **No (OpEx)** |  (PT8) |
| N40 | **Azure Migrate** |  (PT8) |
| N41 | **Public cloud** |  (PT8) |
| N42 | **Host app + manage OS, don't manage hardware** |  (PT8) |
| N43 | **Blueprints** |  (PT8) |
| N44 | **Fault tolerance** |  (PT8) |
| N45 | **Azure TCO Calculator** | ⚠️ TCO deprecated August 2025. Use Pricing Calculator. (PT8) |
| N46 | **Deploy web app, focus on coding** |  (PT8) |
| N47 | **No** | SIN is not an MFA factor. MFA = something you know + have + are. (PT8) |
| N48 | **Correct** |  (PT8) |
| N49 | **Package/deploy collection of policy definitions as single entity** |  (PT8) |
| N50 | **All: Management + Billing + Scale** |  (PT8) |
| N51 | **Hybrid** |  (PT8) |
| N52 | **Provider = infrastructure; customer = apps + data** |  (PT8) |
| N53 | **Recover from Azure File share using Azure Backup** |  (PT8) |
| N54 | **Private, Public** |  (PT8) |
| N55 | **Azure Service Health** |  (PT8) |
| N56 | **Azure Cosmos DB** |  (PT8) |
| N57 | **IaaS = control VMs/OS; PaaS = abstracts infra, focus on app dev** |  (PT8) |
| N58 | **SaaS** |  (PT8) |
| N59 | **Network Security Group** |  (PT8) |
| N60 | **Create a Storage Account** |  (PT8) |
| N61 | **Unified solution to manage/govern data across cloud + on-prem** |  (PT8) |
| N62 | **Containers** |  (PT8) |
| N63 | **No (CapEx — upfront payment)** |  (PT8) |
| N64 | **Desired state of resources + configuration** |  (PT8) |
| N65 | **Private, Hybrid** |  (PT8) |
| N66 | **Resources** |  (PT8) |
| N67 | **Provider = infrastructure; customer = app code + data** |  (PT8) |
| N68 | **Yes (No = incorrect statement)** |  (PT8) |
| N69 | **Cross-region connectivity** |  (PT8) |
| N70 | **Tags** |  (PT8) |
| N71 | **Access control boundary** |  (PT8) |
| N72 | **Azure App Service** |  (PT8) |
| N73 | **Tags** |  (PT8) |
| N74 | **One-time large migration** |  (PT8) |
| N75 | **Customized rules/behaviors for customer identity interactions** |  (PT8) |
| N76 | **Azure Virtual Network** |  (PT8) |
| N77 | **VM patching and maintenance** |  (PT8) |
| N78 | **40 TB** |  (PT8) |
| N79 | **False** | One billing report per subscription. (PT8) |
| N80 | **PaaS** |  (PT8) |
| N81 | **False** | That describes Archive tier, not Cool. (PT8) |
| N82 | **IaaS** |  (PT8) |
| N83 | **Scope** | Deallocating (not just shutting down) saves costs. Shutting down alone still incurs charges. (PT8) |
| N84 | **Shutting down VMs at night** |  (PT8) |
| N85 | **No** | Free tier: MFA for all users via Authenticator app ONLY (security defaults). Phone/SMS only for global admins in free tier. (PT8) |
| N86 | **Pay for execution time, no server management** |  (PT8) |
| N87 | **Azure Cosmos DB** |  (PT8) |