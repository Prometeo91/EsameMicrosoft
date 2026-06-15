# 03 — Describe Azure Management and Governance (30–35% of the exam)

---

## Skill 3.1: Describe Cost Management in Azure

### 💲 Factors That Affect Costs (from Microsoft Learn)

Azure uses a consumption-based approach — you pay for IT resources as you use them and release them when you're done. Costs scale with actual usage.

**Six factors that affect Azure costs (from Microsoft Learn):**

| Factor | How It Affects Cost |
|---|---|
| **Resource type** | Type, settings, and region all affect pricing. Azure tracks usage via meters and charges based on that usage. Same resource in different regions = different costs. |
| **Consumption** | Pay-as-you-go (standard rates) or commit for discounts (Reservations, Savings Plans). |
| **Maintenance** | Unused resources still cost money. When you deprovision a VM, additional resources (storage, networking) may NOT deprovision automatically — clean up to avoid hidden costs. |
| **Geography** | Region and data-transfer zones affect pricing. Cost of power, labor, taxes, and fees varies by location. Network traffic is also impacted — moving data within Europe costs less than moving it from Europe to Asia. |
| **Subscription type** | Free trials and usage allowances vary by subscription. Azure free trial: free products for 12 months + credit for first 30 days + 25+ always-free products. |
| **Azure Marketplace** | Third-party vendor costs added on top of Azure service costs. Billing structures set by the vendor. All Marketplace solutions are certified and compliant with Azure policies and standards. |

**Network traffic details (from book):** inbound traffic is free. Outbound: first 100 GB free, then tiered pricing by billing zone. Traffic across regions is charged; traffic within the same region is often free. Azure regions grouped into **4 billing zones** for egress pricing.

⚠️ **Exam Tip**: Choosing the cheapest region per resource can backfire — cross-region network traffic charges may exceed the savings. Billing zones are different from availability zones.

### 📉 Cost Optimization Options (from Microsoft Learn)

| Option | Commitment | Best For | Savings |
|---|---|---|---|
| **Pay-as-you-go** | None | Variable or unpredictable usage | Standard rates (most flexible) |
| **Reservations** | 1 or 3 years | Stable, predictable workloads (specific resource type) | **Up to 72% off** |
| **Azure Savings Plan** | 1 or 3 years | Steady compute across services (flexible across VM types) | **Up to 65% off** |
| **Spot Pricing** | None | Interruptible/fault-tolerant workloads (batch, test) | **Up to 90% off** |

💡 **Decision guide (from Microsoft Learn)**: Reservations for predictable, long-running workloads with stable resource needs. Savings Plan for steady compute that shifts among compute services. Spot for interruptible workloads where lowest cost is top priority. Review regularly — a workload that starts as interruptible may become business-critical over time.

| Strategy | How It Saves (from book) |
|---|---|
| **Reserved Capacity** | 1- or 3-year contracts for Azure SQL DB, Cosmos DB, Synapse Analytics; billed monthly at reduced rate |
| **Azure Hybrid Benefit** | Bring your own Windows Server or SQL Server license; save 40%+ on VMs |

### 🧮 Pricing Calculator (from Microsoft Learn)

**Pricing Calculator** (https://azure.microsoft.com/pricing/calculator) — estimate potential Azure expenses. For information purposes only — nothing is provisioned and you won't be charged. You can estimate individual resources, build out a complete solution, or use example scenarios. Compare monthly estimates across regions, service tiers, and redundancy options before deployment. Teams often use it as a baseline for budget approval.

⚠️ **Exam Tip (from Microsoft Learn)**: The **TCO Calculator has been retired** (August 2025). The Pricing Calculator is the current tool for estimating Azure costs, including migration scenarios. If the exam still references TCO, remember: it was a tool for comparing on-prem vs. Azure savings over 5 years.

### 📊 Microsoft Cost Management Tool (from Microsoft Learn)

A set of tools that helps organizations analyze, monitor, and manage Azure costs. Helps spot sudden spend increases, find idle resources, and validate tagging and budgets.

**Three components (from Microsoft Learn):**

| Component | Purpose |
|---|---|
| **Cost Analysis** | View costs by billing cycle, region, resource group, or service. Explore and analyze cloud costs. View aggregated costs by subscription, resource group, or service. See accumulated costs over time to estimate monthly/quarterly/yearly trends against a budget. |
| **Cost Alerts** | Single location for all alert types. Three types: **Budget alerts** (notify when spending reaches/exceeds a threshold you define — create in portal or via Azure Consumption API), **Credit alerts** (notify when Azure Prepayment/monetary commitment is consumed — auto-generated at 90% and 100% — EA only), **Department spending quota alerts** (notify when department spending reaches a fixed threshold — EA only, configured in portal). All delivered via email and portal. |
| **Budgets** | Set spending limits by subscription, resource group, or service type. When budget hits alert level → budget alert triggered + email notification. Can configure **automation** to suspend or modify resources when a spending threshold is reached (e.g., auto-shutdown of nonproduction resources). |

### 🏷️ Tags (from Microsoft Learn)

Tags are **name/value pairs** applied to Azure resources for categorization and organization. Tags provide extra metadata about your resources.

**Six tag use cases (from Microsoft Learn):**

| Use Case | Purpose | Example |
|---|---|---|
| **Resource management** | Locate and act on resources by workload, environment, team, or owner | Tag by team or project |
| **Cost management** | Group resources to report costs, allocate internal cost centers, track budgets | CostCenter = "Finance" |
| **Operations management** | Group resources by criticality for SLA formulation | Impact = "Mission-critical" |
| **Security** | Classify data by security level | SecurityLevel = "Confidential" |
| **Governance and compliance** | Identify resources aligned with compliance requirements (e.g., ISO 27001) | Compliance = "ISO27001" |
| **Workload optimization and automation** | Visualize resources in complex deployments and automate tasks with Azure DevOps | Workload = "PaymentAPI" |

**Recommended starter tags**: `Environment`, `Owner`, `CostCenter`, `Workload`.

**Managing tags (from Microsoft Learn):** add, modify, or delete via Azure portal, PowerShell, CLI, ARM templates, or REST API. Use **Azure Policy** to enforce tagging rules (require tags on new resources, reapply removed tags).

⚠️ **Exam Tip**: Resources do **NOT** inherit tags from subscriptions or resource groups. You can apply tags at one level and they will not automatically show up at a different level — allowing custom tagging schemas per level. Tags appear on Azure invoices (CSV) — filterable in Excel by tag.

### 🎫 Azure Support Plans

Five support tiers with increasing levels of technical support and response time:

| Plan | Open Tech Support Tickets? | Channels | Fastest Response (Sev A) | Cost |
|---|---|---|---|---|
| **Basic** | ❌ No — billing/subscription + self-help only | Portal docs, forums | N/A | Free (all Azure accounts) |
| **Developer** | ✅ Yes | Email (business hours only) | N/A (Sev C: < 8 hours) | ~$29/month |
| **Standard** | ✅ Yes | 24/7 email + phone | < 1 hour | ~$100/month |
| **Professional Direct** | ✅ Yes | 24/7 email + phone + advisory + webinars | < 15 minutes | ~$1,000/month |
| **Premier / Unified** | ✅ Yes | All channels + designated Technical Account Manager (TAM) | Custom | Enterprise contract |

⚠️ **Exam Trap**: **Basic does NOT allow opening technical support tickets** — only billing and subscription requests. If a question asks "which plans allow you to open support requests," Basic is excluded. Developer, Standard, Professional Direct, and Premier/Unified all allow it.

💡 **Tip**: All paid support plans include 24/7 access to billing and subscription support. The difference is in **technical** support — Developer only gets email during business hours, while Standard and above get 24/7 phone + email.

📌 **Key Points — Da ricordare**
- Six cost factors: resource type, consumption, maintenance (unused resources still cost), geography, subscription type, Azure Marketplace.
- Four pricing options: Pay-as-you-go (flexible) → Reservations (up to 72% off, specific resource) → Savings Plan (up to 65% off, flexible compute) → Spot (up to 90% off, interruptible only).
- Pricing Calculator = estimate costs before deployment. TCO Calculator has been retired (August 2025) — Pricing Calculator now covers migration scenarios too.
- Cost Management: Cost Analysis (view/explore), Cost Alerts (budget + credit + dept quota), Budgets (spending limits + automation).
- Tags: 6 use cases, do NOT inherit from resource groups or subscriptions. Use Azure Policy to enforce tagging. Starter set: Environment, Owner, CostCenter, Workload.
- Support Plans: Basic (free, NO tech tickets) → Developer (email, business hours) → Standard (24/7, < 1hr Sev A) → Professional Direct (24/7, < 15min Sev A) → Premier/Unified (TAM, enterprise).

---

## Skill 3.2: Governance and Compliance Features

### 📐 Azure Blueprints

Package and reuse cloud deployments with all governance in place. Blueprints contain **artifacts**: resource groups, ARM templates, policy assignments, role assignments.

| Feature | Detail |
|---|---|
| Storage | Saved in a subscription or management group |
| Versioning | Blueprints are versioned; can be stored in source control |
| Connection | Azure maintains a link between the blueprint and deployed resources |
| Lifecycle | Create (draft) → Publish (with version) → Assign (to a subscription) |
| Lock | Can lock resources created by blueprint during assignment |
| Parameters | Values (e.g., resource group name, location) can be deferred to assignment time |

⚠️ **Exam Tip**: Blueprints are NOT a replacement for ARM templates — most blueprints use ARM templates as artifacts. You cannot change the name or definition location after creation.

⚠️ **Update (Duffy)**: Azure Blueprints is being **retired** and replaced by **Template Specs** (pre-built ARM templates for reuse) and **Deployment Stacks** (manage groups of resources as a single unit). Existing Blueprint content may still appear on the exam during the transition period.

### 📜 Azure Policy

A service to create, assign, and manage policies that control or audit Azure resources. Policies enforce rules across resource configurations so they stay compliant with organizational standards. Azure Policy can both **highlight noncompliant resources** and **prevent noncompliant resources from being created** (from Microsoft Learn).

**Scope and Inheritance (from Microsoft Learn):** policies can be set at each level — individual resource, resource group, subscription, or management group. Policies are **inherited**: a policy set at a high level automatically applies to all child groupings. For example, a policy set on a resource group applies to all resources created within that group.

**Initiatives (from Microsoft Learn):** a way of grouping related policies together to track compliance toward a larger goal. Example: the "Enable Monitoring in Azure Security Center" initiative contains 100+ policy definitions, including monitoring for unencrypted SQL Databases, OS vulnerabilities, and missing Endpoint Protection.

**Seven Policy Effects:**

| Effect | Action |
|---|---|
| **Append** | Add properties (e.g., tag with specific value) |
| **Audit** | Log a warning on non-compliance |
| **AuditIfNotExists** | Log a warning if a required companion resource type doesn't exist |
| **Deny** | Block the create/update operation |
| **DeployIfNotExists** | Auto-deploy a companion resource if not included |
| **Modify** | Add, update, or remove properties on existing resources (e.g., auto-add missing tags on existing resources) |
| **Disabled** | Policy is inactive |

**Built-in definitions (from Microsoft Learn):** Azure Policy comes with built-in policy and initiative definitions for Storage, Networking, Compute, Security Center, and Monitoring. Example: define a policy allowing only a certain VM size — it is invoked on new VM creation and when resizing existing VMs. Azure Policy also evaluates all current resources, including those created before the policy existed.

**Auto-remediation (from Microsoft Learn):** in some cases Azure Policy can automatically remediate noncompliant resources. Example: require an `AppName` tag and have Azure Policy add it when missing. You retain full control because individual resources can be **marked as exceptions**.

**Azure DevOps integration (from Microsoft Learn):** Azure Policy integrates with Azure DevOps by enforcing CI/CD pipeline policies for pre-deployment and post-deployment phases.

**Policy guardrails for AI-assisted changes (from Microsoft Learn):** Azure Policy still enforces your standards even when changes come from Copilot recommendations or agent-like automation. You can require allowed locations, required tags, approved resource SKUs, and security baselines regardless of how a change was proposed.

⚠️ **Exam Tip**: Azure Policy evaluates resources retroactively — it checks resources that existed before the policy was created. Initiatives group policies toward a compliance goal; a single initiative can contain 100+ policies.

### 🔒 Resource Locks

Prevent resources from being accidentally deleted or changed (from Microsoft Learn). Even with Azure RBAC policies in place, there is still a risk that people with the right level of access could delete critical cloud resources — resource locks are the safety net.

| Lock Type | Can Read? | Can Modify? | Can Delete? |
|---|---|---|---|
| **Delete** | ✅ Yes | ✅ Yes | ❌ No |
| **ReadOnly** | ✅ Yes | ❌ No | ❌ No |

💡 **Tip (from Microsoft Learn)**: A ReadOnly lock is similar to restricting all authorized users to the permissions granted by the **Reader** role.

- Applied at: individual resource, resource group, or even an entire subscription (from Microsoft Learn).
- **Inherited** by child resources — a lock on a resource group applies to all resources within it (from Microsoft Learn).
- Nested locks: the most restrictive lock wins.
- Locks only apply to ARM operations — some resource-internal operations (e.g., Key Vault keys/secrets) bypass the lock.
- Read-only locks can cause unexpected behavior (e.g., listing storage account keys is blocked because it enables write access).

**Managing locks (from Microsoft Learn):** Azure portal (Settings → Locks), PowerShell, Azure CLI, or ARM templates.

**Modifying a locked resource (from Microsoft Learn):** a two-step process — (1) remove the lock, (2) perform the action. Locks apply **regardless of RBAC permissions** — even an Owner must remove the lock first before performing the blocked activity.

⚠️ **Exam Tip**: To create a lock, you must be in the Owner or User Access Administrator RBAC role (or a custom role with lock permissions). Locks override RBAC — this is a frequent exam trap.

### 🔍 Service Trust Portal

A portal providing access to content, tools, and resources about Microsoft security, privacy, and compliance practices (from Microsoft Learn). Contains details about Microsoft's implementation of controls and processes that protect cloud services and customer data.

**Access (from Microsoft Learn):** URL is https://servicetrust.microsoft.com/. To access some resources, you must sign in with a **Microsoft Entra work or school account** and review/accept the Microsoft **non-disclosure agreement** for compliance materials.

**Three menu categories (from Microsoft Learn):**

| Menu | Purpose |
|---|---|
| **Service Trust Portal** | Quick-access link to return to the home page |
| **My Library** | Save (pin) documents for quick access; set up notifications when pinned documents are updated |
| **All Documents** | Browse all available documents; pin items to My Library from here |

**Report retention (from Microsoft Learn):** reports and documents are available to download for at least **12 months** after publishing or until a new version becomes available.

**Certifications available** include: ISO/IEC, SOC 1/2/3, GDPR, FedRAMP, PCI DSS, CSA Star, Australia IRAP, Singapore MTCS, Spain ENS.

### 🤖 Governance Guardrails for AI-Assisted Workflows (from Microsoft Learn)

When teams use Copilot or agent-assisted workflows, governance controls still apply. RBAC, Azure Policy, resource locks, and auditing ensure that AI-assisted changes remain within approved boundaries. This is a new learning objective for the exam.

📌 **Key Points — Da ricordare**
- Blueprints bundle ARM templates, policies, RBAC, and resource groups into reusable, versioned packages. ⚠️ Being retired → replaced by Template Specs + Deployment Stacks.
- Azure Policy: 7 effects (Deny blocks creation, Modify changes existing resources, Disabled turns it off). Policies are inherited downward. Can prevent creation of noncompliant resources AND auto-remediate (e.g., auto-add missing tags). Evaluates existing resources retroactively.
- Initiatives group related policies toward a compliance goal (e.g., "Enable Monitoring in Security Center" = 100+ policy definitions).
- Azure Policy integrates with Azure DevOps CI/CD and enforces standards even for AI-assisted / Copilot changes.
- Resource locks: Delete (read + modify OK, no delete) vs. ReadOnly (read only, like Reader role). Two-step to modify: remove lock → perform action.
- Locks override RBAC — even an Owner must remove the lock first. Inherited downward. Managed via portal, PowerShell, CLI, or ARM template.
- Service Trust Portal (https://servicetrust.microsoft.com/) — requires Entra work/school account + NDA. Three menus: Service Trust Portal, My Library (pin + notifications), All Documents. Reports kept 12+ months.
- Governance guardrails for AI: RBAC, Policy, locks, and auditing apply even to Copilot/agent-assisted changes.

---

## Skill 3.3: Managing and Deploying Azure Resources

**Azure Management Tools (from Microsoft Learn):**

| Category | Tool | Description |
|---|---|---|
| Graphical | **Azure portal** | Web-based console to build, manage, and monitor cloud resources |
| Environment | **Cloud Shell** | Browser-based shell with built-in authentication; no local install required |
| Command Line | **Azure PowerShell** | Cmdlet-based scripting for repeatable automation tasks |
| Command Line | **Azure CLI** | Bash-based commands with same capabilities as PowerShell |
| AI-Assisted | **Copilot in Azure** | AI assistant for contextual guidance in natural language |

### 🖥️ Azure Portal

Web-based, unified console that provides an alternative to command-line tools (from Microsoft Learn). Key elements:

- **Home** screen with service icons, recent resources, and navigation links.
- **Search bar** at the top for services, docs, or resources.
- **Cloud Shell** button launches a web-based command shell.
- **Settings** for theme, default view, menu behavior (docked vs. flyout), pop-up notifications.
- **Blades** = the window panes for each resource view (Overview, Settings, etc.).
- **Dashboard** = customizable with pinned tiles; create multiple dashboards for specific purposes.
- **Favorites** = star any Azure service in All Services to pin it to the left menu.
- **Accessibility options** configurable for an optimal experience (from Microsoft Learn).

**Resiliency (from Microsoft Learn):** the portal is designed for resiliency and continuous availability — it maintains a presence in **every Azure datacenter**, making it resilient to individual datacenter failures and avoiding network slowdowns by being close to users. The portal **updates continuously** and requires **no downtime** for maintenance.

### 🤖 Copilot in Azure (from Microsoft Learn)

An AI assistant experience that helps administrators work faster by providing contextual guidance in natural language. Some Copilot workflows can be **agent-like**, helping coordinate multi-step tasks.

**Use cases:** exploring services, understanding configuration options, drafting commands or scripts.

⚠️ **Exam Tip (from Microsoft Learn)**: Treat Copilot as an **operational assistant** — you should still validate recommendations, confirm permissions, and review deployment changes before applying them in production. Humans remain responsible for validation and approval.

### ⌨️ Azure PowerShell (Az Module)

A shell for developers, DevOps, and IT professionals to run commands called **cmdlets** (command-lets) (from Microsoft Learn). Cmdlets call the **Azure REST API** to perform management tasks. They can run independently for one-off changes or be combined to orchestrate complex actions such as routine setup/teardown of resources or deployment of entire infrastructure from imperative code. Capturing commands in a script makes the process **repeatable and automatable** (from Microsoft Learn).

Cross-platform (Windows, Linux, macOS). Requires PowerShell 5.x, 6.x, or 7.x (.NET Standard). Also available via Azure Cloud Shell.

```
Install-Module -Name Az -AllowClobber
Connect-AzAccount
Set-AzContext -Subscription "subscription_id"

New-AzResourceGroup -Name MyRG -Location "South Central US"
Remove-AzResourceGroup -Name MyRG -Force
```

- Use `-Force` to skip confirmation prompts (essential for scripts).

### 💻 Azure CLI

**Functionally equivalent** to Azure PowerShell — the primary difference is the syntax of commands (from Microsoft Learn). While PowerShell uses PowerShell cmdlets, the CLI uses **Bash commands**. The choice mainly comes down to which language you're most familiar with.

Cross-platform command-line tool (v2.0+). Also available via Azure Cloud Shell. Installable on Windows, Linux, and Mac.

```
az login
az account set --subscription "subscription_id"
az resource create --help
az interactive    # enables auto-complete and command scoping
```

- Extensions add functionality: `az extension list-available --output table`
- Use `--force` to skip prompts in scripts.

⚠️ **Exam Tip**: Both PowerShell and CLI require `-force`/`--force` for unattended scripts. Watch for exam questions testing this.

### ☁️ Azure Cloud Shell

Browser-based shell tool for creating, configuring, and managing Azure resources using a shell (from Microsoft Learn). Supports both Azure PowerShell and Azure CLI (Bash). No local installation or configuration required.

- **Authenticated to your Azure credentials** — when you log in, it inherently knows who you are and what permissions you have (from Microsoft Learn).
- Requires a storage account to persist files and settings across devices.
- Includes a Monaco-based code editor and Web Preview for testing web apps.
- Any uploaded files are stored in Azure Storage and available on any device.
- Also accessible from documentation Try It buttons and the Azure mobile app.

### 🌐 Azure Arc

Extends Azure management and governance to resources outside Azure (on-premises, other clouds). Works with **Azure Resource Manager** to extend compliance and monitoring to hybrid and multicloud configurations, delivering a consistent management platform (from Microsoft Learn).

**Five resource types managed outside Azure (from Microsoft Learn):** Servers, Kubernetes clusters, Azure data services, SQL Server, Virtual machines (preview).

**What Azure Arc enables (from Microsoft Learn):**

| Capability | Description |
|---|---|
| **Unified management** | Project non-Azure resources into Azure Resource Manager — manage your entire environment together |
| **Manage as if in Azure** | Manage multicloud and hybrid VMs, K8s clusters, and databases as if running in Azure |
| **Familiar Azure services** | Use Azure services and management capabilities regardless of where resources live |
| **ITOps + DevOps** | Continue using traditional ITOps while introducing DevOps and cloud-native patterns |
| **Custom locations** | Configure an abstraction layer on top of Arc-enabled Kubernetes clusters and cluster extensions |

| Type | How It Works | Capabilities |
|---|---|---|
| **Arc-enabled servers** | Install Azure Connected Machine agent (Windows or Linux) | RBAC, Azure Policy, tags, Defender for Cloud, managed identity |
| **Arc-enabled Kubernetes** | Register cluster via CLI/PowerShell → agent connects to Azure | Manage clusters, run Azure SQL MI, PostgreSQL, App Service, Functions, Logic Apps, Event Grid, API Management |

💡 **Tip**: Arc-enabled Kubernetes uses **GitOps** (Git source control) for deployment and management.

💡 **Practical scenario (from Microsoft Learn)**: Organization runs workloads in Azure, an on-prem datacenter, and another public cloud. With Arc, operations teams apply consistent governance, policy, and inventory tracking across all environments from Azure — instead of managing each with disconnected tools.

### 🔧 Azure Resource Manager (ARM)

The **deployment and management service** for Azure (from Microsoft Learn). Provides a management layer that enables you to create, update, and delete resources. When a user sends a request from any Azure tool, API, or SDK, ARM **authenticates and authorizes** the request, then sends it to the appropriate Azure service. All tools produce consistent results because all requests go through the same API.

**Request flow (from Microsoft Learn):** Tools (portal, CLI/PowerShell, REST APIs/SDKs) → **ARM** (Auth + Orchestration) → Azure Services (Compute, Networking, Storage + Data).

**Six ARM benefits (from Microsoft Learn):**

| Benefit | Detail |
|---|---|
| **Declarative templates** | Manage infrastructure through templates rather than scripts |
| **Group management** | Deploy, manage, and monitor all resources for a solution as a group |
| **Consistent re-deployment** | Re-deploy throughout the development lifecycle with confidence resources are in a consistent state |
| **Dependency ordering** | Define dependencies between resources so they deploy in the correct order |
| **Native RBAC** | Access control applied to all services — RBAC is natively integrated into the management platform |
| **Tagging** | Apply tags to resources to organize your subscription and support cost reporting |

### 📄 Infrastructure as Code (IaC) with ARM Templates and Bicep

**Infrastructure as Code** = managing infrastructure through code and templates instead of manual configuration (from Microsoft Learn). Can start with CLI or PowerShell scripts and grow into repeatable environment deployments using ARM templates and Bicep.

**ARM Templates** = declarative JSON files. You declare what you want to deploy; Azure validates the template before deployment, then orchestrates resource creation in the **right order and in parallel** when possible (from Microsoft Learn). Teams define the desired end state; ARM handles deployment execution.

**Five ARM template benefits (from Microsoft Learn):**

| Benefit | Detail |
|---|---|
| **Declarative syntax** | Define what to deploy instead of writing step-by-step commands |
| **Repeatable results** | Reuse the same template across environments for consistent outcomes |
| **Orchestration** | ARM handles dependency order and parallel deployment automatically |
| **Modularity** | Split templates into reusable components and nested templates |
| **Extensibility** | Add PowerShell or Bash deployment scripts for additional setup before or after resource creation |

- Define resources, their properties (name, region, pricing plan, etc.), and dependencies.
- All Azure management tools use the same ARM API on the back end.
- View any resource's ARM template in the portal via Export Template.

### 🦾 Bicep (from Microsoft Learn)

A **declarative language** for deploying Azure resources through ARM. Compared to JSON ARM templates, Bicep is generally **simpler and more concise**.

**Five Bicep benefits (from Microsoft Learn):**

| Benefit | Detail |
|---|---|
| **Support for current Azure resources** | Bicep tracks Azure resource types and API versions |
| **Simple syntax** | Easier to read and write than equivalent JSON templates |
| **Repeatable deployments** | Bicep files are **idempotent** — consistent lifecycle deployments |
| **Built-in orchestration** | ARM handles dependencies and parallel deployment execution |
| **Modularity** | Reuse logic by organizing deployments into Bicep modules |

⚠️ **Exam Tip**: Both ARM templates (JSON) and Bicep are IaC tools that deploy through ARM. ARM templates and Bicep are idempotent — deploying the same file multiple times produces the same result without duplicates.

📌 **Key Points — Da ricordare**
- Azure portal is resilient (present in every datacenter, updates continuously, no downtime).
- Five management tools: Portal (graphical), Cloud Shell (browser-based environment), PowerShell (cmdlets), CLI (Bash), Copilot in Azure (AI-assisted).
- Copilot in Azure = AI operational assistant for contextual guidance. Humans remain responsible for validation and approval.
- PowerShell cmdlets call the Azure REST API. CLI is functionally equivalent — only syntax differs.
- Cloud Shell: browser-based, no install, auto-authenticated, persists files in Azure Storage.
- Azure Arc extends Azure governance to on-prem + multi-cloud. Five resource types: servers, K8s, data services, SQL Server, VMs (preview). Projects non-Azure resources into ARM.
- ARM = management layer that authenticates, authorizes, and orchestrates all Azure operations. Six benefits: declarative templates, group management, consistent re-deployment, dependency ordering, native RBAC, tagging.
- ARM templates = declarative JSON; Bicep = simpler declarative DSL. Both are IaC, both are idempotent, both deploy through ARM.
- Use `-Force`/`--force` in scripts to avoid interactive prompts.

---

## Skill 3.4: Monitoring Tools in Azure

### 🧠 Azure Advisor

Evaluates your Azure resources and makes recommendations to help you improve reliability, security, performance, and cost efficiency (from Microsoft Learn). Think of it as a **personalized best-practices guide** built into the Azure portal.

Each recommendation includes a suggested action you can **take right away, postpone, or dismiss** (from Microsoft Learn). You can also set up **notifications** so Advisor alerts you when new recommendations appear.

**Advisor dashboard (from Microsoft Learn):** displays recommendations for all your subscriptions, filterable by subscription, resource group, or service. Shows impact levels (High, Medium, Low) per category and impacted resource counts. Cost category shows estimated **savings/yr**. Recommendations exportable as CSV or PDF.

**Five recommendation categories (from Microsoft Learn):**

| Category | What It Does |
|---|---|
| **Reliability** | Flags configuration risks that could affect application availability |
| **Security** | Detects threats and vulnerabilities that could lead to breaches |
| **Performance** | Identifies changes that can speed up your applications |
| **Operational Excellence** | Suggests workflow and deployment improvements |
| **Cost** | Finds ways to reduce your Azure spending |

⚠️ **Exam Tip**: "Capacity" is NOT one of the five Advisor categories — this is a common exam trap. The five are Reliability, Security, Performance, Operational Excellence, and Cost.

### 💚 Azure Service Health

Helps you stay informed about the health of Azure itself and the specific resources you run (from Microsoft Learn). Combines **three views that narrow in scope** from global down to individual resources.

| View | Scope | What It Shows |
|---|---|---|
| **Azure Status** | All services, all regions (global view) | Broad picture of Azure health; check when you hear about a widespread outage to see if Azure is affected |
| **Service Health** | Your services, your regions | Focuses on the services and regions you actually use; shows outages, planned maintenance, and health advisories relevant to your environment; configurable **alerts** for automatic notification |
| **Resource Health** | Individual resource (e.g., a specific VM) | Tells whether a resource is running normally or experiencing a problem, and whether the issue is on **Azure's side or yours** |

**Operational value (from Microsoft Learn):** together, these three views give visibility from broad service events all the way down to a single resource. **Historical alerts** are retained so you can spot recurring trends. When an event affects one of your workloads, Service Health provides **links to support** so you can respond quickly.

### 📈 Azure Monitor

A platform for **collecting, analyzing, and acting on** data from Azure resources and applications (from Microsoft Learn). Works with Azure, on-premises, and multicloud environments. Gathers logs and metrics from applications, operating systems, and network layers, stores that data centrally, and makes it available through dashboards, queries, and alerts.

**Architecture (from Microsoft Learn):**

| Layer | Components |
|---|---|
| **Data Sources** | Workloads, Infrastructure, Azure Platform, Custom Sources |
| **Data Platform** | Metrics, Logs, Traces |
| **Experiences** | Application, Container, VM, Network monitoring |
| **Visualize** | Workbooks, Dashboards, Power BI, Grafana |
| **Analyze** | Metric Explorer, Log Analytics |
| **Respond** | Alerts & Actions, Autoscale |
| **Integrate** | Event Hubs, Logic Apps, Import/Export APIs |

### 📊 Azure Log Analytics (from Microsoft Learn)

The tool in the Azure portal where you write and run queries against the data Azure Monitor collects. You can do simple filtering (e.g., finding all errors in the last hour) or run advanced analytics to visualize trends over time. Uses **Kusto Query Language (KQL)**; choose from built-in queries or write custom ones.

### 🔔 Azure Monitor Alerts (from Microsoft Learn)

Alerts notify you when Azure Monitor detects a defined condition. You create an **alert rule** (specifying the condition) and an **action group** (controlling who gets notified and what happens next).

Alerts can be **metric-based** (e.g., VM CPU stays above 80%) or **log-based** (e.g., watch for a specific error pattern across multiple resources) (from Microsoft Learn).

**Action groups** are reusable across Azure Monitor, Service Health, and Azure Advisor (from Microsoft Learn). They contain notifications (email, SMS, push) and actions (webhook, Logic App, Function App).

### 🔍 Application Insights (from Microsoft Learn)

An Azure Monitor feature that monitors the **performance and usage of web applications**, whether they run in Azure, on-premises, or in another cloud.

**Two setup methods:** add an SDK to your application code, or enable the Application Insights agent **without code changes**.

**Four monitoring areas (from Microsoft Learn):**

| Area | What It Tracks |
|---|---|
| Request rates, response times, failure rates | How the app responds to incoming requests |
| Dependency calls and performance | External service calls (databases, REST APIs) |
| Page load times, user counts, session trends | Browser-side experience and usage patterns |
| Server performance counters | CPU, memory, and network usage |

**Availability tests (from Microsoft Learn):** send **synthetic requests** to your application to verify it is responding, even during low-traffic periods.

📌 **Key Points — Da ricordare**
- Azure Advisor: personalized best-practices guide. Five categories: Reliability, Security, Performance, Operational Excellence, Cost. "Capacity" is NOT a category. Recommendations can be taken, postponed, or dismissed. Set up notifications for new recommendations.
- Azure Service Health: three views narrowing in scope — Azure Status (global) → Service Health (your services/regions, with alerts) → Resource Health (individual resource, Azure's side or yours). Historical alerts retained for trend spotting.
- Azure Monitor: collects, analyzes, and acts on data from Azure + on-prem + multicloud. Data platform: Metrics, Logs, Traces. Five output layers: Experiences, Visualize, Analyze, Respond, Integrate.
- Log Analytics: portal tool to query Monitor data using KQL — simple filtering to advanced analytics.
- Alerts: metric-based or log-based. Alert rule + action group. Action groups are reusable across Monitor, Service Health, and Advisor.
- Application Insights: monitors web apps (Azure, on-prem, other cloud). Setup via SDK or agent (no code changes). Tracks requests, dependencies, page loads, server perf. Availability tests send synthetic requests.
