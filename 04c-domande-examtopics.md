# 04c — Domande ExamTopics & Practice Quiz

> **~120 domande** — Sezione F: domande da ExamTopics community e practice quiz.
>
> ⚠️ **Errata**: Alcune risposte contengono errori noti, segnalati con ⚠️. In caso di dubbio, fare riferimento ai file di studio 01–03.

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
| F30 | **c** | Office 365 = SaaS (you use the app), Azure VMs = IaaS (you manage the OS), Event Grid = **Serverless** (event routing, pay per event). Since Serverless is not listed as an option, PaaS is the closest standard classification. |
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
| F87 | **d** | Azure Blueprints bundle ARM templates, RBAC, policies, and resource groups into a reusable, versioned package for repeatable environment deployment. ⚠️ Blueprints is being retired → replaced by Template Specs + Deployment Stacks. |
| F88 | **a** | Yes. Entra ID Cloud Sync (or Entra Connect) synchronizes on-prem AD with Entra ID, enabling SSO and MFA across both environments. |
| F89 | **c** | Security groups in Entra ID are used to group users and assign permissions to resources (including O365). Resource groups organize Azure resources; Management groups organize subscriptions. |
| F90 | **b** | Authentication = verifying identity ("who are you?"). MFA adds extra verification factors. Authorization = "what can you do?" after identity is confirmed. |
| F91 | **c** | Azure File Sync provides bidirectional sync between on-prem file shares and Azure Files. AzCopy is one-way copy; Storage Explorer is a GUI tool; Data Box is for offline bulk transfer. |
| F92 | **a** | Conditional Access defines the policies (when to require MFA based on conditions), and Identity Protection evaluates risk signals (device health, sign-in risk) that feed into those policies. |
| F93 | **a** | Tags (name-value pairs like "BusinessUnit:Finance") enable cost tracking and chargeback reporting. Filter Cost Analysis by tags to see spending per business unit. |

---
