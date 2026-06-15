# 06 — Indice Tematico per Dominio d'Esame (AZ-900)

> Mappa di navigazione verso le 1264 domande distribuite nei file **04a–04d**, organizzate per dominio e sotto-obiettivo ufficiale Microsoft. Usa questo file per studiare per area tematica e identificare le zone con più/meno copertura.
>
> | File | Sezioni | Domande |
> |------|---------|---------|
> | **04a-domande-curate.md** | A, B, C, D, G | ~119 |
> | **04b-domande-ipspecialist.md** | E | ~416 |
> | **04c-domande-examtopics.md** | F | ~120 |
> | **04d-practice-test.md** | H, I, J, K, L, M, N | ~609 |

---

## 📊 Pesi dei domini (aggiornati alle specifiche ufficiali)

| Dominio | Peso esame | Domande mappate | Copertura |
|---------|-----------|-----------------|-----------|
| 1 — Describe Cloud Concepts | **25–30%** | ~321 | ████████░░ |
| 2 — Describe Azure Architecture and Services | **35–40%** | ~564 | ██████████ |
| 3 — Describe Azure Management and Governance | **30–35%** | ~379 | █████████░ |

> ⚠️ Alcune domande toccano più domini (es. RBAC è sia Architecture che Governance). In quei casi la domanda è elencata nel dominio primario con un rimando al secondario.

---

## Dominio 1 — Describe Cloud Concepts (25–30%)

### 1.1 — Describe cloud computing

📌 **Definizione di cloud computing, modelli di deployment, responsabilità condivisa**

| Sotto-tema | Domande |
|------------|---------|
| Definizione di cloud computing | D1 |
| Shared responsibility model | A1, D3, E202, E378, G1 |
| Cloud models: public | E57, E58, E381, E386, G2 |
| Cloud models: private | A2, A8, E68 |
| Cloud models: hybrid | A3, D2, E61, E207, E256, E370, E376, G3 |
| Cloud models: multi-cloud | E62, E65 |
| Consumption-based model | A12, E66, E69, F12 |
| CapEx vs OpEx | E109, E204, E262, F21, F25, F33 |
| Appropriate use case per cloud model | E56, E382, E383, E384, E387, E388, F10, F11 |

**Conteggio**: ~45 domande

### 1.2 — Describe the benefits of using cloud services

📌 **HA, scalabilità, elasticità, affidabilità, prevedibilità, sicurezza, governance, gestibilità**

| Sotto-tema | Domande |
|------------|---------|
| High availability | E211, E245, E253, E259, D5, G6 |
| Scalability (vertical/horizontal) | A7, D4, E67, E257, E405, G4 |
| Elasticity | A6, E70, E71, F32, G5 |
| Reliability / Fault tolerance | A9, D5, E251, E208 |
| Predictability (performance & cost) | F34 |
| Security & governance benefits | E381 |
| Manageability | E389, E385, E413 |
| Sustainability | D6 |
| Geo-distribution | E372 |

**Conteggio**: ~31 domande

### 1.3 — Describe cloud service types

📌 **IaaS, PaaS, SaaS — definizioni, responsabilità, casi d'uso**

| Sotto-tema | Domande |
|------------|---------|
| IaaS — definizione e casi d'uso | A4 (PaaS contrast), D7, E238, E244, F4, F5, F6, E377, G7 |
| PaaS — definizione e casi d'uso | A4, A10, A11, E379, F28, F31, G8 |
| SaaS — definizione e casi d'uso | A5, D8, E202, F22, F23, F30, G9 |
| Confronto IaaS/PaaS/SaaS | F24, F27, F29, F30 |
| Serverless (Azure Functions) | D13, E364, F36, F41 |

**Conteggio**: ~31 domande

---

## Dominio 2 — Describe Azure Architecture and Services (35–40%)

### 2.1 — Describe the core architectural components of Azure

📌 **Regions, zone, region pairs, sovereign regions, risorse, RG, subscription, management groups**

| Sotto-tema | Domande |
|------------|---------|
| Regions & region pairs | B1, D11, E38, E265, E372, E390, F58, G10 |
| Availability Zones | B2, B3, B15, E350, E407, F19, F20, F43, F112 |
| Availability Sets | D12, E348, E349, E392, F60, F115 |
| Sovereign regions | F96 |
| Resource groups | B4, B16, B22, D9, D10, E6, E7, E9, E249, E348, F40, F111, G12 |
| Subscriptions | E52, E408, F56, G11 |
| Management groups | B17, E408 |
| Azure Resource Manager (ARM) | E5, E8, E10, E11, E13 |

**Conteggio**: ~51 domande

### 2.2 — Describe Azure compute and networking services

📌 **VMs, scale sets, containers, App Service, Functions, VPN, ExpressRoute, DNS, VNet**

| Sotto-tema | Domande |
|------------|---------|
| **Compute** | |
| Virtual Machines | E72, E78, E205, E260, E338, F4, F5, F6 |
| VM Scale Sets | B6, E73, E74, E235, E373, F102 |
| VM Reservations & cost | E81, E82, E83–E98, E261, E362, F107 |
| Spot VMs | D29, E363 |
| Availability Sets / Zones (compute) | D12, E350, E392, F19, F20, F112, F115 |
| Azure App Service | A4, A11, D14, E367, F7, F9, F53, F114, G13 |
| Azure Functions | D13, E364, F36, F41 |
| Azure Container Instances (ACI) | B5, F117, F118 |
| Azure Kubernetes Service (AKS) | E244, F45, F118 |
| Azure Virtual Desktop | E75, E76, E77, E79, E391 |
| Azure Batch | E374 |
| Azure Dedicated Hosts | E338 |
| **Networking** | |
| Virtual Networks (VNet) | E36, E37, E39, E40, E111, E239, F71, F119, G14 |
| Subnets | D16, E44, F119 |
| VNet Peering | B18, E45, E118, E351 |
| VPN Gateway (S2S, P2S) | B14, D18, E46, E119–E125, E247, E353, E368, E371, F52, F77, F108 |
| ExpressRoute | B7, D17, E126–E130, E352, G15 |
| NSG (Network Security Groups) | E42, E43, E117, E341, F73 |
| Azure Firewall | E294, E365, F74, G22 |
| Azure DNS | D19, E47 |
| Azure Load Balancer | E241 |
| Azure DDoS Protection | E375, E289, F120 |
| Route Tables / UDR | E44, E116 |
| Hybrid connectivity overview | F51, F52, E409, E419 |

**Conteggio**: ~149 domande

### 2.3 — Describe Azure storage services

📌 **Storage accounts, ridondanza, servizi di storage, tiers, migrazione dati**

| Sotto-tema | Domande |
|------------|---------|
| Storage redundancy: LRS, ZRS, GRS, GZRS, RA-GRS | B9, D21, E21–E35, E366, F1, F59, F101 |
| Blob Storage | B8, D22, E357, E358, F46, F48, F55, F64, G16 |
| File Storage (Azure Files) | E54, E359, F37, F54 |
| Table Storage | F103 |
| Queue Storage | F49 |
| Storage tiers (Hot, Cool, Archive) | B8, F46, F48 |
| Data migration: AzCopy | D20, F91, F100 |
| Data migration: Azure File Sync | D20, E394, F91, G17, G18 |
| Data migration: Storage Explorer | — |
| Data migration: Azure Data Box | B10, E1–E4 |

**Conteggio**: ~58 domande

### 2.4 — Describe Azure identity, access, and security

📌 **Entra ID, autenticazione, MFA, Conditional Access, RBAC, Zero Trust, Defender for Cloud**

| Sotto-tema | Domande |
|------------|---------|
| Microsoft Entra ID (Azure AD) | B11, E51, E250, E292, E345, F8, F14, F88, F89, G20 |
| Authentication vs Authorization | B20, D23, E293, F90, F95, F98 |
| MFA | E79, E293, F82, F83, F84, G19 |
| Conditional Access | D23, E369, F82, F83, F92 |
| Passwordless (Windows Hello, FIDO2) | F72 |
| RBAC | B12, B21, D25, E48, E301, F80, F95, G27 |
| Zero Trust | B13, D24, F86 |
| Defense in Depth | E375 |
| Microsoft Defender for Cloud | E290, E340, E341, F70, F81, F85, F104, F105, G21 |
| Azure Key Vault | D26, E184, E206, E226, E283, E339 |
| Identity Protection | F76, F92 |
| Azure Information Protection / Purview | E209, E298, F57 |

**Conteggio**: ~66 domande

---

## Dominio 3 — Describe Azure Management and Governance (30–35%)

### 3.1 — Describe cost management in Azure

📌 **TCO Calculator, Pricing Calculator, Cost Management, Tags, Reservations**

| Sotto-tema | Domande |
|------------|---------|
| Pricing Calculator | C1 (contrast), D28, F47, F106, G24 |
| TCO Calculator | C1, E264, E346, E347 |
| Azure Cost Management + Billing | E55, E248, E263, F110, F113 |
| Tags (cost tracking) | C2, D27, E14, E343, F93, F99, G25 |
| Reservations | C12, E81, E362, F107 |
| Spot VMs | D29, E363 |
| Factors affecting cost | C11, E205, E237, E243, E260, G23 |
| PAYG / expenditure models | E66, E387, F10, F11, F12, F116 |
| Cost optimization (Advisor) | E210, F109, F113 |
| Resource group cost (free) | E249, F111 |

**Conteggio**: ~48 domande

### 3.2 — Describe features and tools for governance and compliance

📌 **Azure Policy, Blueprints, Resource Locks, Microsoft Purview, Service Trust Portal**

| Sotto-tema | Domande |
|------------|---------|
| Azure Policy | C3, D30, E49, E50, E300, E342, E418, F75, F79, F94, F97 (contrast), G26, G28 |
| Azure Blueprints | C10, C13, E258, E304, E344, F87 |
| Resource Locks | C4, C9, C15, D31, E254, E302, F78, F97 |
| Microsoft Purview | F57 |
| Compliance (NIST, HIPAA, PCI DSS) | E191–E200, F85, F105 |
| Service Trust Portal | — |

**Conteggio**: ~40 domande

### 3.3 — Describe features and tools for managing and deploying Azure resources

📌 **Azure Portal, CLI, PowerShell, Cloud Shell, ARM templates, Bicep, Azure Arc**

| Sotto-tema | Domande |
|------------|---------|
| Azure Portal | E246, E308, E425, F61 |
| Azure CLI / PowerShell / Cloud Shell | C14, E201, E425, G29 |
| ARM templates / Bicep (IaC) | C6, D33, E8, F16, F17, F18, F38, G31 |
| Azure Arc | C7, D32, E63, E400, G30 |
| Azure Marketplace | E236, E416 |

**Conteggio**: ~23 domande

### 3.4 — Describe monitoring tools in Azure

📌 **Azure Advisor, Azure Monitor, Service Health, Log Analytics, Application Insights**

| Sotto-tema | Domande |
|------------|---------|
| Azure Advisor | C5, D34, E210, E303, F65, F109, F113, G32 |
| Azure Monitor | C8, E240, E360, E414, E428, F42, F68, F69, G34 |
| Log Analytics / KQL | C8, E360 |
| Application Insights | F63, F66, F67 |
| Azure Service Health | C16, D35, E212, E403, E415, G33 |

**Conteggio**: ~28 domande

---

## 🗺️ Domande di nicchia / specialistiche (fuori scope AZ-900 ma presenti nel file)

Queste domande sono utili come cultura generale ma difficilmente compaiono all'esame:

| Area | Domande |
|------|---------|
| Azure Cosmos DB (dettagli avanzati) | E131–E150, E354–E356 |
| Azure Synapse Analytics | E151–E160, E185 |
| Azure IoT Hub (dettagli) | E161–E179 |
| Azure Machine Learning (dettagli) | E53, E181–E190, E427 |
| NIST CSF / compliance framework (dettagli) | E191–E200 |
| VM Reservations (procedure acquisto) | E83–E98 |
| Azure support plans (dettagli) | F2, F3, E305, E306, E308, E309 |
| Disaster Recovery plans (processo) | E15–E20 |
| Azure DevTest Labs | E311 |

---

## 📋 Riepilogo per sezione sorgente

| Sezione | Range | Tot. domande | File | Focus principale |
|---------|-------|-------------|------|------------------|
| A | A1–A12 | 12 | 04a | Cloud Concepts |
| B | B1–B22 | 22 | 04a | Architecture & Services |
| C | C1–C16 | 16 | 04a | Management & Governance |
| D | D1–D35 | 35 | 04a | Trasversale (Microsoft Learn) |
| E | E1–E428 | 416 | 04b | Trasversale (IPSpecialist) |
| F | F1–F120 | 120 | 04c | Trasversale (ExamTopics + Practice Quiz) |
| G | G1–G34 | 34 | 04a | Trasversale (Scott Duffy Udemy) |
| H | H1–H50 | 50 | 04d | Practice Test scenario-based (Scott Duffy Udemy) |
| I | I1–I83 | 82 | 04d | Practice Test 3 concept-based (Udemy) |
| J | J1–J125 | 125 | 04d | Practice Test 4 mixed-format (Udemy) |
| K | K1–K90 | 90 | 04d | Practice Test 5 mixed-format (Udemy) |
| L | L1–L89 | 89 | 04d | Practice Test 6 mixed-format (Udemy) |
| M | M1–M86 | 86 | 04d | Practice Test 7 mixed-format (Udemy) |
| N | N1–N87 | 87 | 04d | Practice Test 8 mixed-format (Udemy) |

---

## 🎯 Strategia di studio consigliata

1. **Inizia dal dominio con più peso**: Dominio 2 (35–40%) ha la maggiore copertura — concentrati su compute, networking e storage
2. **Non trascurare il Dominio 1**: pesa 25–30% e le domande sono spesso "facili" se ben studiate — punti sicuri
3. **Dominio 3 è insidioso**: i tool di governance (Policy vs Blueprints vs Locks) e i calculator (Pricing vs TCO vs Cost Management) sono trappole frequenti
4. **Domande da rifare con priorità** (temi più gettonati all'esame):
   - Shared responsibility model → A1, D3
   - IaaS vs PaaS vs SaaS → A4, A5, D7, D8, F27, F28
   - Availability Zones vs Sets vs Regions → B2, B3, D12, F19, F112, F115
   - Storage redundancy → B9, D21, F59, F101
   - AuthN vs AuthZ → F90, F95, F98
   - Policy vs Locks vs Blueprints → C3, C4, C10, F75, F78, F94, F97
   - Pricing Calculator vs TCO vs Cost Management → C1, D28, F47, F106, F110
   - Azure Advisor categories → D34, C5, F65, F109
5. **Section H (Practice Test)**: 50 domande scenario-based da Scott Duffy — simulano il formato esame. Usale come mock exam cronometrato (~60 min) dopo aver completato lo studio per dominio. Distribuzione: D1 (7), D2 (20), D3 (23). Section I (82 domande) e Section J (125 domande) completano il set di mock exam.
