# 04b — Domande IPSpecialist (4th ed. 2024)

> **~416 domande** — Sezione E: banca domande da IPSpecialist Practice Questions.
>
> ⚠️ **Errata**: Alcune risposte contengono errori noti, segnalati con ⚠️. In caso di dubbio, fare riferimento ai file di studio 01–03.

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
| E35 | **⚠️ d** | ⚠️ **Correction**: Azure Files DOES support GZRS in Standard GP v2 accounts. The actual limitation is that **RA-GRS / RA-GZRS** (read-access geo variants) are not available for Azure Files. The original source confuses GZRS with RA-GZRS. |
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
| E94 | **⚠️ c** | ⚠️ **Correction**: Azure Reservations are available for **1 year or 3 years only** — there is no 5-year term. The correct answer should exclude the 5-year option. |
| E95 | **a** | The quantity is the number of running VM instances that can get the billing discount. |
| E96 | **d** | ⚠️ Duplicate of E95 — explanation appears mismatched (discusses pricing, not quantity). Cross-reference with E95. |
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
| E258 | **a** | ⚠️ Azure Blueprints è in fase di ritiro — sostituito da Template Specs + Deployment Stacks. Azure Blueprint enables us to design and package the entire Azure environment, including preferred policy, ARM template, and role-based access assignment. These blueprints are assigned to many subscriptions, which can help us to scale up the use of Azure. |
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
| E264 | **a** | ⚠️ TCO Calculator deprecato (agosto 2025) — ora si usa il Pricing Calculator anche per scenari di migrazione. You can use the Total Cost of Ownership calculator to see the cost savings you can achieve by moving workloads to Azure. A snapshot of the TCO Calculator is shown below. The other options are invalid because they help cost management after moving to Azure. |
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
| E300 | **b, c, d** | ⚠️ La domanda chiede 3 risposte: b, c, d sono tutte corrette. Option A is incorrect because Azure Monitor primarily analyzes the telemetry data. Option B is CORRECT because please view the reference URL for creating policy assignments. Option C is CORRECT because please view the reference URL for creating policy assignments. Option D is CORRECT because please view the reference URL for creating policy assi... |
| E301 | **a** | Option A is CORRECT because please view the reference URL, Active Directory limits section. Option B is incorrect because it would be effective immediately only on logout\login. Option C is incorrect because please view the reference URL, Active Directory limits section. Option D is incorrect because please view the reference URL, Active Directo... |
| E302 | **c** | There are two types of locks available: delete and read-only. A Read-only lock on an SQL Database prevents you from deleting or modifying the database. It does not prevent you from creating, updating, or deleting data in the database. |
| E303 | **a** | Option A is CORRECT because ITSM Connector exists to integrate Azure with Service now. Option B is incorrect because it requires custom requires custom development to achieve the integration. Option C is incorrect because it development to achieve the integration. Option D is incorrect because a connector exists to integrate Azure and specific I... |
| E304 | **c** | ⚠️ Azure Blueprints è in fase di ritiro — sostituito da Template Specs + Deployment Stacks. Option A is incorrect because these are the locks for the resources and not modes. Option B is incorrect because these are the states of the resources and not modes. Option C is CORRECT because please see the diagram below. Option D is incorrect because “Update” is an invalid lock option, and ReadOnly is a lock on a resource. |
| E305 | **b** | The most cost-effective plan with these points is the Developer plan. The Microsoft documentation mentions the following. |
| E306 | **a** | Yes, everyone has access to the Knowledge Center. |
| E307 | **b** | Azure Service Level Agreements (SLAs) are formal commitments made by Microsoft Azure to ensure the reliability and availability of its cloud services. These SLAs specify the guaranteed uptime percentage for each Azure service, such as Virtual Machines, Blob Storage, and SQL Database, among others. The uptime percentages typically range from 99.9... |
| E308 | **a** | You can launch a support request via the Azure portal. The Microsoft documentation mentions the following. Azure portal for commercial use is: |
| E309 | **a, b, c** | ⚠️ La domanda chiede 3 risposte: Account Administrator, Service Administrator e Co-Administrator possono tutti aprire richieste di supporto per default. This is provided in the FAQ section for Azure support. |
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
| E313 | **a, b, c** | ⚠️ La domanda chiede 3 risposte: Cloud Shell richiede resource group, storage account e file share. Azure Cloud Shell needs the following to operate. A resource group A storage account A file share You will be prompted for these resources when you start Azure Cloud Shell. |
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
| E344 | **c** | ⚠️ Azure Blueprints è in fase di ritiro — sostituito da Template Specs + Deployment Stacks. Azure Blueprints can be adopted to orchestrate the deployment of multiple resource templates and artifacts. Role Assignments Policy Assignments Azure Resource templates) Resource Groups Manager templates (ARM Option B is invalid because this is used as a governance service for our resources. Option D is invalid because this is adopted to organiz... |
| E345 | **d** | Azure Multi-Factor Authentication can be enabled in a couple of ways. This can be done from Microsoft Entra ID. As shown in the figure below, if we go to the Users section, we can enable Multi-Factor Authentication. The other options are invalid because we cannot enable Multi-Factor Authentication in the other services. |
| E346 | **a** | ⚠️ TCO Calculator deprecato (agosto 2025) — ora si usa il Pricing Calculator anche per scenari di migrazione. Using the Total Cost of Ownership calculator, we can understand the TCO for server workloads. |
| E347 | **a** | ⚠️ TCO Calculator deprecato (agosto 2025) — ora si usa il Pricing Calculator anche per scenari di migrazione. We can scroll down and then download the report in the Final Report section for the TCO Calculator. It is also shown in the figure below. |
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
| E369 | **a** | ⚠️ Risposta corretta: **a** (Conditional Access), non b (Administrative Units). La spiegazione stessa conferma che Conditional Access è la funzionalità che concede/restringe l'accesso. Based on identification signals, Microsoft Entra ID uses Conditional Access as a tool to provide (or restrict) access to resources. A more advanced form of MFA (multifactor authentication) is conditional access. After first-factor authentication is complete, conditional access rules are put into effect. In situations like Denial-ofService (DoS) ... |
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
| E397 | **a** | ⚠️ Risposta corretta: **a** (Read and Write), non c (Read only). RBAC usa un modello additivo: i permessi di tutti i ruoli assegnati si sommano (Read ∪ Write = Read and Write). All permissions assigned in the given roles are granted via role-based access control using an allowed model. |
| E398 | **a** | Azure policy enables you to define initiatives (groups of rules) and policies that forbid the creation of noncompliant resources. |
| E399 | **b** | Artifacts might not have any additional parameters. For example, the "Deploy threat detection on SQL servers" policy needs no additional settings. |
| E400 | **d** | You may expand your Azure compliance and monitoring to your hybrid and multi-cloud deployments using Azure Arc in conjunction with Azure Resource Manager. |
| E401 | **c** | ⚠️ Azure Blueprints è in fase di ritiro — sostituito da Template Specs + Deployment Stacks. You can publish your resource as code using ARM Templates and Azure Blueprints, which automatically apply policies. Combining the two makes it easier to ensure you are deploying reliable legal resources. |
| E402 | **a** | The five suggestion categories for Azure Advisor are cost, operational excellence, performance, security, and reliability. |
| E403 | **c** | Resource Health is an accurate representation of your actual Azure resources. It gives details on the state of each of your particular cloud resources. |
| E404 | **d** | Multiple steps are involved in migrating to Microsoft Azure Cloud Adoption Framework; these are: 1. Define Strategy 2. Plan 3. Ready 4. Adopt 5. Govern 6. Manage The strategy for the adoption should include the following: 1. Recognize motivations Learn about cloud economics and obtain the technical and financial advice you need to create your cl... |
| E405 | **a** | Vertical scaling, sometimes called scale up and down, changes the size of a Virtual Machine (VM) in response to a workload. Contrast this behavior with horizontal scaling, often known as scale out and scale in, which changes the number of VMs based on the workload. |
| E406 | **d and e** | Apply Azure network segmentation patterns. A standardized enterprise segmentation strategy directs technical teams to systematically segment access using identity, networking, apps, and other access restrictions. By establishing perimeters, segment your network footprint. These are the main justifications for segmentation: The capacity to organi... |
| E407 | **b** | The level of control you have over ensuring that the data and apps on your virtual machines are always accessible is increased by availability zones. Within an Azure region, an Availability Zone is a physically distinct zone. Each supported Azure region has three Availability Zones. Power, networking, and cooling are all unique to each Availabil... |
| E408 | **c and e** | A container for Azure resources is called an Azure subscription. Additionally, it serves as a limit for billing and resource access permissions. All of the resources in a subscription are billed monthly. Multiple Azure subscriptions may be included in a single Azure tenant (Microsoft Entra ID). For an Azure solution, a resource group is a contai... |
| E409 | **a and b** | You must set up a VPN (Virtual Private Network) to link the on-premises network to the Azure virtual network to deploy a solution that allows the client computers on your on-premises network to communicate with the Azure virtual machines. A virtual network gateway is the name of the Azure VPN device. The Azure virtual network must have a specifi... |
| E410 | **a** | ⚠️ Risposta corretta: **a** (Create a new support request), non c (service health alert). La spiegazione stessa dice "By submitting a support request". There are quotation limits on several Azure resources. The quota restrictions are there to aid you in keeping tabs on your Azure expenses. The default quota frequently needed to be increased, though. By submitting a support request, you can ask for an increase in the quota limit. Select "Service and subscription limits (quotas)" as the issue typ... |
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
| E421 | **a** | ⚠️ Risposta corretta: **a** (True), non b (False). La spiegazione stessa conferma che Azure SQL Data Warehouse (Synapse Analytics) ha funzionalità di HA con SLA 99.9%. Microsoft's PaaS product is called Azure Data Warehouse, which is currently called Azure Synapse Analytics. Like all Microsoft PaaS services, SQL Data Warehouse has a 99.9% SLA for availability. Because its platform includes high availability features, Microsoft can guarantee 99.9% availability. |
| E422 | **a** | Azure When you need to integrate apps, data, systems, and services across businesses or organizations, Logic Apps is a cloud solution that can help you schedule, automate, and orchestrate tasks, business processes, and workflows. Whether in the cloud, on-premises, or both, Logic Apps makes it easier to design and develop scalable solutions for a... |
| E423 | **d** | Users worldwide will download big video files, according to the query. If people could download the video from servers in their home area, the video playback experience would be better. By utilizing a content delivery network, we can do this. A dispersed network of servers known as a Content Delivery Network (CDN) can deliver web material to use... |
| E424 | **c and e** | Data from millions of sensors is provided by IoT Hub (Internet of Things Hub). A managed service called IoT Hub is hosted in the cloud. It serves as a central messaging node for two-way communication between your IoT application and the devices it controls. Building IoT systems with dependable and secure connections between millions of IoT devic... |
| E425 | **a and d** | The web-based management portal for Azure is called the Azure portal. The Azure portal can be used on an iPhone because it is web-based. An online command-line called Azure Cloud Shell is used to manage Azure. The Azure portal is where you access the Azure Cloud Shell. The Azure Cloud Shell can be used on an iPhone because it is web-based. Optio... |
| E426 | **a and e** | Data from millions of sensors is provided by IoT Hub (Internet of Things Hub). A managed service called IoT Hub is hosted in the cloud. It serves as a central messaging node for two-way communication between your IoT application and the devices it controls. Building IoT systems with dependable and secure connections between millions of IoT devic... |
| E427 | **d** | You can graphically connect datasets and modules on an interactive canvas using Azure Machine Learning Designer to build machine learning models. |
| E428 | **b** | You can increase the availability and efficiency of your applications and services with the aid of Azure Monitor. With this comprehensive solution, the telemetry from your cloud and on-premises systems can be collected, analyzed, and used to take action. With this data, you may better comprehend how your apps operate and proactively spot problem... |

---
