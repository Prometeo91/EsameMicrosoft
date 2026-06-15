# 04d — Practice Test (Mock Exam)

> **~609 domande** — Sezioni H (Scott Duffy Practice Test, 50), I (Practice Test 3, 82), J (Practice Test 4, 125), K (Practice Test 5, 90), L (Practice Test 6, 89), M (Practice Test 7, 86), N (Practice Test 8, 87).
>
> 💡 Usare come simulazione cronometrata (~60 min per 50 domande). Distribuzione domini: vedi file 06.
>
> ⚠️ **Errata**: Alcune risposte contengono errori noti, segnalati con ⚠️. In caso di dubbio, fare riferimento ai file di studio 01–03.

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
| I41 | **⚠️ Azure Cost Management and Billing** | ⚠️ **Correction**: The question says "recommendations to optimize spending" which maps to **Azure Advisor** (Cost category), not Cost Management. Cost Management provides cost analysis, budgets, and alerts — Advisor provides **recommendations**. (PT3) |
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
| I56 | **Yes, but only by the subscription owner** | ⚠️ "Only subscription owner" is too narrow. Any user with **Owner or User Access Administrator** role can add locks. Multiple locks can coexist on a resource. (PT3) |
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
| J65 | **Policy assignments** | ⚠️ Azure Blueprints is being retired → replaced by Template Specs + Deployment Stacks. (PT4) |
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
| J82 | **Yes, subscription owner can** | ⚠️ Not limited to subscription owner — any user with **Owner or User Access Administrator** role can add locks. (PT4) |
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
| J96 | **Preserves relationship between definition and assignment** | ⚠️ Azure Blueprints is being retired → replaced by Template Specs + Deployment Stacks. (PT4) |
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
| J120 | **Prevent modifications but allow read access** | ⚠️ This describes only the **ReadOnly** lock. There are TWO lock types: **Delete** (read+modify OK, no delete) and **ReadOnly** (read only, no modify or delete). (PT4) |
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
| K53 | **⚠️ Site-to-Site (IPsec)** | ⚠️ **Correction**: VPN between two Azure VNets is a **Network-to-Network (VNet-to-VNet)** connection, not Site-to-Site. Site-to-Site is for on-premises → Azure. For Azure-to-Azure, **VNet Peering** is simpler and preferred. (PT5) |
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
| M12 | **Extending Azure Policy and Blueprints to on-prem + multi-cloud** | ⚠️ Blueprints is being retired. Arc primarily extends Azure Policy, RBAC, and tags — not Blueprints. (PT7) |
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
| M40 | **Host app, manage OS, don't manage underlying hardware** | ⚠️ Ambiguous wording: in PaaS the **provider** manages the OS, not you. You manage app code + data only. (PT7) |
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
| M83 | **⚠️ Entra B2C** | ⚠️ **Correction**: B2C is for consumer-facing apps (social logins), NOT for corporate credentials. Using existing corporate credentials for cloud apps is the core function of **Microsoft Entra ID (SSO)**, or **Entra B2B** for partner organizations. (PT7) |
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
| N35 | **GRS** | GRS and GZRS both have 16 nines of durability. GZRS is the highest redundancy option (adds zone protection on primary). (PT8) |
| N36 | **Yes** |  (PT8) |
| N37 | **No** |  (PT8) |
| N38 | **Containers** |  (PT8) |
| N39 | **No (OpEx)** |  (PT8) |
| N40 | **Azure Migrate** |  (PT8) |
| N41 | **Public cloud** |  (PT8) |
| N42 | **Host app + manage OS, don't manage hardware** | ⚠️ Ambiguous wording: in PaaS the **provider** manages the OS, not you. You manage app code + data only. (PT8) |
| N43 | **Blueprints** | ⚠️ Azure Blueprints is being retired → replaced by Template Specs + Deployment Stacks. (PT8) |
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
| N63 | **⚠️ No (CapEx — upfront payment)** | ⚠️ **Correction**: Cloud reservations are **OpEx**, not CapEx. CapEx = upfront spending on **physical infrastructure** you own. Reservations are a commitment to pay for cloud services — no physical asset is purchased. Microsoft classifies all cloud spending (including reservations) as OpEx. (PT8) |
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
