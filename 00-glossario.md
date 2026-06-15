# 00 — Glossary of Key Terms (AZ-900)

---

| Term | Definition |
|---|---|
| **ACI (Azure Container Instances)** | Serverless service for running Docker containers without managing VMs; pay only for CPU/memory used. |
| **AKS (Azure Kubernetes Service)** | Managed Kubernetes cluster service; Azure manages the control plane, you deploy containers. |
| **ARM (Azure Resource Manager)** | Deployment and management service for Azure. Management layer that authenticates, authorizes, and routes all requests — whether from portal, CLI, PowerShell, APIs, or SDKs. Six benefits: declarative templates, group management, consistent re-deployment, dependency ordering, native RBAC, tagging. |
| **ARM Template** | Declarative JSON file that defines Azure resources and their properties for repeatable deployments. Idempotent. ARM validates before deployment and orchestrates in the right order and in parallel when possible. |
| **Auto-Scale** | Azure feature that automatically adds or removes resources based on usage patterns, metrics, or schedules. |
| **Application Insights** | Azure Monitor feature for monitoring web app performance and usage (Azure, on-prem, other clouds). Setup via SDK or agent (no code changes). Tracks requests, dependencies, page loads, server perf. Availability tests send synthetic requests. |
| **Availability Set** | Logical grouping of VMs across fault domains (racks) and update domains within a single datacenter; guarantees 99.95% SLA. |
| **Availability Zone** | Physically separate datacenter within an Azure region with independent power, cooling, and networking; guarantees 99.99% SLA for multi-zone VMs. |
| **AVD (Azure Virtual Desktop)** | PaaS desktop virtualization service; users access OS and apps remotely via clients or web browser. |
| **Azure Active Directory (Azure AD)** | Cloud-based identity and access management service for authentication and authorization. Now renamed to **Microsoft Entra ID**. |
| **Azure AI Services** | Prebuilt AI capabilities via APIs for language, speech, vision, and document processing. No custom model training required. |
| **Azure AD B2B** | Feature that lets you invite external (guest) users to your Azure AD for collaboration. |
| **Azure AD B2C** | Identity and access management service for publishing apps to consumers/customers using Entra ID. |
| **Azure AD Connect** | Tool that synchronizes on-premises Windows AD with Azure AD. |
| **Azure AD Conditional Access** | Policy engine that controls access based on user, device, location, and app conditions (Premium tier only). |
| **Azure AD DS** | Cloud-managed Active Directory Domain Services with domain join, group policies, and Kerberos/NTLM authentication. |
| **Azure Advisor** | Personalized best-practices guide built into the portal. Five categories: Reliability, Security, Performance, Operational Excellence, Cost ("Capacity" is NOT a category). Recommendations can be taken, postponed, or dismissed. Filterable by subscription, resource group, or service. Notifications available for new recommendations. |
| **Azure Arc** | Service that extends Azure management and governance (RBAC, Policy, tags) to on-premises and multi-cloud resources via ARM. Five resource types: servers, Kubernetes clusters, Azure data services, SQL Server, VMs (preview). Supports custom locations on Arc-enabled K8s. |
| **Azure Blob Storage** | Storage service for unstructured data (Block Blobs, Append Blobs, Page Blobs) organized in containers. |
| **Azure Blueprints** | Service for packaging ARM templates, policies, RBAC, and resource groups into reusable, versioned deployment definitions. |
| **Azure CLI** | Cross-platform command-line interface (Bash-based) for managing Azure resources; functionally equivalent to PowerShell. |
| **Azure Cloud Shell** | Browser-based shell (PowerShell or Bash) accessible from the portal or Azure mobile app; auto-authenticated, no local install required; persists files in Azure Storage. |
| **Azure Cost Management and Billing** | Portal tool for analyzing costs, creating budgets, and setting spending alerts. |
| **Azure Data Box** | Offline data migration service (Disk: ~35 TB, Data Box: 80 TB, Heavy: ~770 TB) for transferring large datasets to Azure. |
| **Azure Disks** | Managed disk service for VMs; available as HDD or SSD (Standard/Premium). |
| **Azure DNS** | Service for hosting and managing DNS records (public and private zones) within Azure. |
| **Azure ExpressRoute** | Dedicated, private fiber-optic connection to Azure (up to 10 Gbps) via a service provider or ExpressRoute Direct. A connection is called a circuit. |
| **Azure File Sync** | Service that synchronizes Azure Files shares with on-premises servers for local caching. |
| **Azure Files** | Fully managed cloud SMB file share; mountable on Windows, Linux, and macOS. |
| **Azure Firewall** | Cloud-native network firewall for protecting Azure VNet resources. |
| **Azure Functions** | Serverless compute service for running event-driven microservices; pay only for execution time. Stateless by default; Durable Functions add stateful capabilities. |
| **Azure Hybrid Benefit** | Program to bring your own Windows Server or SQL Server license to Azure for significant cost savings. |
| **Azure Migrate** | Service for discovering, assessing, and migrating servers, databases, and apps to Azure. |
| **Azure Machine Learning** | Platform for building, training, and managing custom ML models. For model development, experimentation, and lifecycle management. |
| **Azure Monitor** | Platform for collecting, analyzing, and acting on data from Azure, on-prem, and multicloud. Data platform: Metrics, Logs, Traces. Outputs: Experiences, Visualize (Workbooks, Dashboards, Power BI, Grafana), Analyze (Metric Explorer, Log Analytics), Respond (Alerts & Actions, Autoscale), Integrate (Event Hubs, Logic Apps). |
| **Azure OpenAI Service** | Azure-hosted access to OpenAI's generative AI models (chat, content generation) with built-in security and governance controls. |
| **Azure Policy** | Service for creating, assigning, and managing policies that control or audit Azure resources. Can prevent noncompliant resources from being created and auto-remediate. Policies are inherited downward. Supports initiatives (groups of policies). Integrates with Azure DevOps CI/CD. Enforces standards even for AI-assisted/Copilot changes. |
| **Azure Queues** | Message queue storage service for decoupling application components; max message 64 KB, max queue ~500 TiB. |
| **Azure Reservations** | Commitment to 1- or 3-year resource usage for discounted pricing (vs. pay-as-you-go). |
| **Azure Service Health** | Three views narrowing in scope: Azure Status (global, all services/regions) → Service Health (your services/regions, with alerts for outages/maintenance/advisories) → Resource Health (individual resource — running normally or problem, Azure's side or yours). Historical alerts retained for trends. |
| **Azure Spot VMs** | VMs running on Microsoft's unused capacity at deep discount for temporary workloads. |
| **Azure Spring Cloud** | PaaS for hosting Java Spring applications with Azure integration. |
| **Azure Stack** | Validated hardware + software package for running Azure services on-premises (hybrid cloud). |
| **Azure Support Plans** | Five tiers: Basic (free, no tech tickets), Developer (email, biz hours, ~$29/mo), Standard (24/7 phone+email, <1hr Sev A, ~$100/mo), Professional Direct (24/7+advisory, <15min Sev A, ~$1K/mo), Premier/Unified (TAM, enterprise contract). Basic does NOT allow opening technical support tickets. |
| **Azure VPN Gateway** | Service for creating encrypted VPN connections (IPSec/IKE) between VNets or to on-premises networks. Also called virtual network gateway. |
| **Azure VMware Solution** | Service that lets you run VMware workloads in Azure with seamless integration and scalability. For migrating from VMware private cloud to Azure. |
| **BCDR** | Business Continuity and Disaster Recovery — planning for data backup and application replication across regions. |
| **Billing Zone** | One of four geographic groups of Azure regions used to determine network egress pricing. |
| **Bicep** | Declarative language for deploying Azure resources through ARM. Simpler and more concise than JSON ARM templates. Idempotent. Supports modularity via Bicep modules. |
| **Cloud Agility** | The speed and ease with which cloud resources can be provisioned or scaled (seconds vs. hours). |
| **Conditional Access** | See Azure AD Conditional Access. |
| **Consumption-Based Model** | Pricing model where you pay only for the resources you actually consume. |
| **Copilot in Azure** | AI assistant experience in Azure that provides contextual guidance in natural language. Helps with exploring services, understanding configurations, and drafting commands/scripts. Some workflows are agent-like (multi-step). Treat as operational assistant — humans validate and approve changes. |
| **Defense in Depth** | Multi-layered security strategy (castle approach) using firewalls, NSGs, DDoS protection, etc. |
| **Data Lineage** | Tracking how data flows from source to destination across systems. A core capability of Microsoft Purview for understanding data provenance and transformations. |
| **Elasticity** | Ability to automatically scale resources up/down or out/in based on demand. |
| **Durable Functions** | Stateful extension of Azure Functions. The runtime passes a context to track prior activity across invocations. |
| **Fault Domain** | Logical representation of a physical server rack in an availability set; protects against hardware failures. |
| **Fault Tolerance** | Automatic movement from unhealthy to healthy resources without user intervention. |
| **FIDO2** | Security key standard for passwordless authentication. |
| **Geography** | Azure boundary (often a country) that ensures data-handling regulations are met. |
| **GRS** | Geo-Redundant Storage — 3 LRS copies in primary region + 3 LRS copies in a secondary region. |
| **GZRS** | Geo-Zone-Redundant Storage — 3 ZRS copies in primary + 3 LRS copies in a secondary region. |
| **IaaS** | Infrastructure-as-a-Service — provider manages hardware; you manage OS, middleware, and apps. |
| **Initiative** | A group of related Azure Policy definitions applied together to track compliance toward a larger goal. Example: "Enable Monitoring in Security Center" contains 100+ policy definitions. |
| **KQL (Kusto Query Language)** | Query language used in Azure Log Analytics for analyzing large-scale monitoring data. |
| **Log Analytics** | Azure portal tool for writing and running queries (KQL) against data Azure Monitor collects. Simple filtering to advanced trend analytics. |
| **Lift-and-Shift** | Migrating an existing application to the cloud with minimal or no code changes (common with PaaS). |
| **LRS** | Locally Redundant Storage — 3 copies in the same datacenter. Cheapest, least durable. |
| **Managed Identity** | Azure AD identity automatically managed by Azure for service-to-service authentication. |
| **Management Group** | Logical container for organizing Azure subscriptions; max 10,000 groups, 6 levels deep. |
| **MFA** | Multifactor Authentication — requires two or more verification factors (know + have + are). |
| **Multi-tenant** | Public cloud environment where infrastructure is shared among multiple organizations. |
| **Multicloud** | Cloud deployment model using two or more public cloud providers simultaneously. Azure Arc helps manage multicloud environments. |
| **Non-regional Services** | Azure services that are always available from Azure geographies and resilient to both zone-wide and region-wide outages. Examples: Microsoft Entra ID, Traffic Manager, Azure DNS. |
| **NSG (Network Security Group)** | Firewall rules for allowing/denying traffic to Azure resources based on IP, port, and protocol. Rules evaluated by priority; first match wins. |
| **NVA (Network Virtual Appliance)** | Specialized VM that performs a network function such as firewall, intrusion detection, or WAN optimization. |
| **PaaS** | Platform-as-a-Service — provider manages infrastructure + OS + middleware; you manage your application. |
| **Passwordless Authentication** | Authentication using a device/key + biometrics (or PIN) instead of a password. |
| **RBAC** | Role-Based Access Control — controls what users can do with Azure resources based on role assignments. |
| **Region** | A set of Azure datacenters in a specific geographic area. |
| **Regional Pair** | Two regions in the same geography updated sequentially by Microsoft for HA during platform updates. |
| **Rehydration** | Process of moving a Blob from Archive tier to Hot or Cool tier for access. |
| **Resource Group** | Logical container for organizing related Azure resources. |
| **Resource Health** | Azure Service Health view that zooms in on individual resources (e.g., a specific VM). Shows whether a resource is running normally or experiencing a problem, and whether the issue is on Azure's side or yours. |
| **Resource Lock** | Prevents accidental deletion (Delete lock) or modification (ReadOnly lock) of an Azure resource regardless of RBAC. Inherited by child resources. To modify a locked resource: remove lock first, then act. Managed via portal, PowerShell, CLI, or ARM template. |
| **SaaS** | Software-as-a-Service — provider manages everything; you use the software (e.g., M365, Gmail). |
| **Scale Set (VMSS)** | Service for deploying and auto-scaling up to 1,000 identical VMs. |
| **Service Principal** | An application identity in Azure AD used for app-to-resource authentication via RBAC. |
| **Service Trust Portal** | Microsoft's portal for security, privacy, and compliance information (https://servicetrust.microsoft.com/). Requires Microsoft Entra work/school account + NDA. Menus: Service Trust Portal, My Library (pin + notifications), All Documents. Reports available 12+ months. Certifications: ISO/IEC, SOC, GDPR, FedRAMP, PCI DSS, etc. |
| **Shared Responsibility Model** | Principle that cloud responsibility is always shared between you and the cloud provider. |
| **Single-tenant** | Private cloud environment dedicated to a single organization. |
| **SLA** | Service-Level Agreement — provider's guarantee of a certain uptime percentage. |
| **Sovereign Region** | Isolated Azure cloud for specific government or regulatory compliance (e.g., Azure Government, Azure Germany, Azure China). |
| **SSO** | Single Sign-On — access multiple resources with one set of credentials. |
| **Subscription** | Azure billing and access-control boundary with a unique subscription ID and resource quotas. |
| **Tag** | Name/value pair applied to Azure resources for categorization, cost tracking, and filtering. |
| **TCO Calculator** | Tool for estimating cost savings when migrating from on-premises to Azure. |
| **Update Domain** | Logical grouping in an availability set ensuring Azure reboots only one group at a time during updates. |
| **UDR (User-Defined Routes)** | Custom routing rules that control traffic flow between subnets within or between virtual networks. |
| **VNet (Virtual Network)** | Azure virtual network enabling communication between Azure services, the internet, and on-premises. |
| **VNet Peering** | Connection between two VNets over Microsoft's backbone. Global VNet peering = across regions. |
| **Zero Trust** | Security framework that assumes every access attempt is a potential breach; relies on Conditional Access, MFA, and least-privilege. |
| **ZRS** | Zone-Redundant Storage — 3 copies across 3 availability zones in the same region. |
| **Azure Container Apps** | Managed container hosting PaaS between ACI and AKS. Built-in load balancing and scaling. Elastic app layer for containers. |
| **Azure Event Grid** | Serverless event routing service using pub/sub model; push events to destinations; pay per use. |
| **Azure Logic Apps** | Serverless service for automating and orchestrating tasks, workflows, and business processes using prebuilt connectors. Foundation for Power Automate. |
| **Azure Mobile App** | iOS/Android app for managing, monitoring, and troubleshooting Azure resources; includes Cloud Shell access. |
| **CapEx** | Capital Expenditure — upfront spending on physical infrastructure. Associated with on-premises/private datacenter scenarios. |
| **Cloud Adoption Framework** | Microsoft's guidance for business and technology strategies for Azure adoption; includes five disciplines of cloud governance. |
| **Cold Tier** | Blob storage tier between Cool and Archive. Min 90 days retention. Online (fast retrieval). Lower storage cost than Cool, higher access cost. |
| **Economies of Scale** | Doing things more efficiently or at lower cost per unit when operating at larger scale. Drives cloud pricing advantages. |
| **IaC (Infrastructure as Code)** | Managing infrastructure through code (e.g., ARM templates). Same code produces the same environment every time (idempotent). Key DevOps practice. |
| **IoT Hub** | Azure service for secure, bi-directional communication between cloud services and IoT devices. |
| **IoT Central** | Simplified SaaS IoT platform for solution builders. |
| **IoT Edge** | Extends Azure cloud capabilities to edge devices so workloads run closer to where data is generated. |
| **Idempotent** | Property of ARM templates: deploying the same template multiple times always produces the same result without duplicates. |
| **Microsoft Entra ID** | New name for Azure Active Directory. Cloud-based identity and access management service. |
| **Microsoft Purview** | Family of data governance, risk, and compliance solutions providing a unified view of data across on-premises, multicloud, and SaaS. Three capabilities: automated data discovery, sensitive data classification, end-to-end data lineage. Two solution areas: Risk and Compliance (powered by M365) and Unified Data Governance. Supports Azure, SQL, Hive, Amazon S3. |
| **OATH Token** | Open Authentication standard for generating time-based one-time passwords (TOTP). Available as software (Authenticator app) or hardware (key fob). |
| **OpEx** | Operational Expenditure — pay-as-you-go spending on services/products. Associated with cloud consumption. |
| **Private Endpoint** | Grants access to a specific PaaS resource instance via a private IP in your VNet. Not accessible from public internet. Enables on-prem access without public endpoint. |
| **Service Endpoint** | Locks down access to all instances of a PaaS service to a VNet. Still accessible from public internet. |
| **Alias Record** | Azure DNS record set that points directly to an Azure resource (public IP, Traffic Manager, CDN). Seamlessly updates when the resource's IP address changes — no manual DNS change needed. |
| **Anycast** | Networking technique used by Azure DNS where each DNS query is answered by the closest available server, providing fast performance and high availability. |
| **Azure Tables** | NoSQL storage service for large amounts of structured, non-relational data. Accessible through authenticated calls from cloud and hybrid environments. |
| **BGP (Border Gateway Protocol)** | Dynamic routing protocol used by ExpressRoute and active/active VPN gateways to exchange routes between on-premises and Azure networks. |
| **Data Lake Storage Gen2** | Big data analytics capability built on top of Azure Blob Storage. Endpoint: `<account>.dfs.core.windows.net`. |
| **ExpressRoute Circuit** | A private connection between your on-premises network and the Microsoft cloud via a connectivity provider. Does not travel over the public internet. |
| **ExpressRoute Global Reach** | Feature that connects your on-premises sites to each other through ExpressRoute circuits via the Microsoft backbone — private site-to-site path without public internet. |
| **RA-GRS** | Read-Access Geo-Redundant Storage — GRS with read access to the secondary region before failover. URL uses `-secondary` suffix. Not available for Azure Files. |
| **RA-GZRS** | Read-Access Geo-Zone-Redundant Storage — GZRS with read access to the secondary region before failover. Highest availability option. |
| **RPO (Recovery Point Objective)** | The interval between the most recent write to the primary region and the last write replicated to the secondary. Azure Storage RPO is typically < 15 minutes (no SLA). |
| **Storage Account** | Provides a unique namespace (3–24 chars, lowercase + numbers, globally unique) for Azure Storage data accessible via HTTP/HTTPS. Contains one or more services and is protected by a redundancy option. |
| **B2B Direct Connect** | Microsoft Entra External ID capability for cross-tenant collaboration via mutual two-way trust. Currently supports Teams shared channels. Users are NOT represented in your directory. |
| **Microsoft Entra Connect** | Tool that synchronizes user identities bi-directionally between on-premises Active Directory and Microsoft Entra ID. Enables SSO, MFA, and password reset across both environments. |
| **Microsoft Entra Domain Services** | Managed domain services (domain join, group policy, LDAP, Kerberos/NTLM) without deploying domain controllers. One-way sync from Entra ID. Ideal for legacy app lift-and-shift. |
| **Microsoft Entra External ID** | Umbrella for external identity capabilities: B2B collaboration (guest users), B2B Direct Connect (Teams shared channels), and External ID for Customers (consumer apps, formerly Azure AD B2C). |
| **Azure Key Vault** | Centralized service for securely storing and controlling access to secrets (passwords, connection strings), encryption keys (RSA/EC, HSM-backed), and certificates (TLS/SSL with auto-renewal). Eliminates hard-coded credentials via managed identities. |
| **CSPM (Cloud Security Posture Management)** | Capability of Defender for Cloud that assesses multicloud resources agentlessly for security posture and compliance. |
| **JIT/JEA (Just-In-Time / Just-Enough-Access)** | Zero Trust principles for limiting user access: grant permissions only when needed (JIT) and only the minimum required (JEA). Risk-based adaptive policies. |
| **Kill-chain Analysis** | Defender for Cloud feature that automatically correlates related security alerts to show the full story of an attack — where it started, which resources were affected, and impact. |
| **MCSB (Microsoft Cloud Security Benchmark)** | Security guidance framework used by Defender for Cloud to evaluate resources and surface prioritized recommendations. Controls scoped at management group, subscription, or tenant level. |
| **Secure Score** | Metric in Defender for Cloud that groups security recommendations into controls and calculates a score so teams can quickly understand posture and prioritize improvements. |
| **Azure Marketplace** | Online store for purchasing Azure-based solutions and services from third-party vendors. All solutions certified and compliant with Azure policies. You pay Azure costs plus vendor costs (billing structures set by vendor). |
| **Azure Savings Plan** | Commitment-based pricing for compute services. Commit to an hourly spend amount for 1 or 3 years across eligible compute services (flexible across VM families). Up to 65% savings. |
| **Cost Analysis** | Feature within Azure Cost Management that provides a visual overview of costs by billing cycle, region, resource group, or service. Used to explore, aggregate, and estimate spending trends. |
