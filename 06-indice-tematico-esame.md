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
| 1 — Describe Cloud Concepts | **25–30%** | ~425 | ████████░░ |
| 2 — Describe Azure Architecture and Services | **35–40%** | ~788 | ██████████ |
| 3 — Describe Azure Management and Governance | **30–35%** | ~546 | █████████░ |

> ⚠️ Alcune domande toccano più domini (es. RBAC è sia Architecture che Governance). In quei casi la domanda è elencata nel dominio primario con un rimando al secondario.

---

## Dominio 1 — Describe Cloud Concepts (25–30%)

### 1.1 — Describe cloud computing

📌 **Definizione di cloud computing, modelli di deployment, responsabilità condivisa**

| Sotto-tema | Domande |
|------------|---------|
| Definizione di cloud computing | D1, I7 |
| Shared responsibility model | A1, D3, E202, E324, E378, G1, H8, I5, I11, I23, I26, I39, I62, J5, J8, J20, J34, J89, K13, K43, K44, L12, L64, M16, M48, M70, N52 |
| Cloud models: public | E57, E58, E381, E386, G2, H1, I48, I55, I81, J49, J70, J114, K81, L32, M45, M73, N34, N41, N48 |
| Cloud models: private | A2, A8, E68, K45, L7, M8, N8 |
| Cloud models: hybrid | A3, D2, E61, E207, E256, E370, E376, G3, H27, H37, I20, I43, J30, J62, J87, K74, M84, N14, N51 |
| Cloud models: multi-cloud | E62, E65 |
| Consumption-based model | A12, E66, E69, F12, F26, H13, H25, J21, J23, K70, L11, L24, M22, M26, N23 |
| CapEx vs OpEx | E101–E108, E109, E110, E204, E262, F21, F25, F33, I28, K66, L66, M13, M47, N1, N13, N39 |
| Appropriate use case per cloud model | E56, E382, E383, E384, E387, E388, F10, F11, J15, L80, M59, M86, N54, N65 |

**Conteggio**: ~149 domande

### 1.2 — Describe the benefits of using cloud services

📌 **HA, scalabilità, elasticità, affidabilità, prevedibilità, sicurezza, governance, gestibilità**

| Sotto-tema | Domande |
|------------|---------|
| High availability | D5, E211, E245, E253, E259, G6, I60, K50, M81 |
| Scalability (vertical/horizontal) | A7, D4, E67, E257, E405, G4, I42, J46, J60, J123, J124, L72 |
| Elasticity | A6, E70, E71, F32, G5, H14, I13, J119, K55, K60, K84, L55, M82 |
| Reliability / Fault tolerance | A9, D5, E208, E251, E380, I10, J17, M41, N44 |
| Predictability (performance & cost) | F34, H41 |
| Security & governance benefits | E381, H16, J9, L42, M74 |
| Manageability | E385, E389, E413 |
| Sustainability | D6 |
| Geo-distribution | E372, M57 |

**Conteggio**: ~58 domande

### 1.3 — Describe cloud service types

📌 **IaaS, PaaS, SaaS — definizioni, responsabilità, casi d'uso**

| Sotto-tema | Domande |
|------------|---------|
| IaaS — definizione e casi d'uso | A4 (PaaS contrast), D7, E238, E244, E377, F4, F5, F6, G7, I1, I47, I50, J1, J68, J73, J118, K23, K30, K54, L20, L50, L68, M76, N77, N82 |
| PaaS — definizione e casi d'uso | A4, A10, A11, E379, F28, F31, G8, H17, I24, I25, I71, I77, J36, J38, J99, J107, K10, K20, K78, L8, L39, L78, M40, M43, M49, N42, N46, N67, N80 |
| SaaS — definizione e casi d'uso | A5, D8, E202, F22, F23, F30, G9, I12, K3, M53, N58 |
| Confronto IaaS/PaaS/SaaS | F24, F27, F29, F30, I32, J40, N57 |
| Serverless (Azure Functions) | D13, E326, E364, F35, F36, F41, F62, I35, I40, I51, I75, J75, K89, L35, L84, N86 |

**Conteggio**: ~104 domande

---

## Dominio 2 — Describe Azure Architecture and Services (35–40%)

### 2.1 — Describe the core architectural components of Azure

📌 **Regions, zone, region pairs, sovereign regions, risorse, RG, subscription, management groups**

| Sotto-tema | Domande |
|------------|---------|
| Regions & region pairs | B1, D11, E38, E216, E265, E372, E390, F58, G10, H48, J3, J90, K72, K90, N36 |
| Availability Zones | B2, B3, B15, E227, E232, E325, E350, E407, F19, F20, F43, F112, J57, J76, J85, K51, K64, K65 |
| Availability Sets | D12, E348, E349, E392, F60, F115 |
| Sovereign regions | F96, H4, I44, J19, J64, K27, L52 |
| Resource groups | B4, B16, B22, D9, D10, E6, E7, E9, E249, E316–E319, E348, F40, F111, G12, I2, I3, I61, I64, J4, J6, J54, J88, J92, J93, K4, K73, N37 |
| Subscriptions | E52, E408, F56, G11, I22, I45, J67, K85, N15, N27, N50, N71, N79 |
| Management groups | B17, E327, E408, I30, I79, J41, J111, L53, L54, L58, L59, M35, N20 |
| Azure Resource Manager (ARM) | E5, E8, E10, E11, E13, H18, H39, J79, K15, L86, N66 |

**Conteggio**: ~126 domande

### 2.2 — Describe Azure compute and networking services

📌 **VMs, scale sets, containers, App Service, Functions, VPN, ExpressRoute, DNS, VNet**

| Sotto-tema | Domande |
|------------|---------|
| **Compute** | |
| Virtual Machines | E72, E78, E205, E260, E278, E338, F4, F5, F6, H43, K87 |
| VM Scale Sets | B6, E73, E74, E221, E235, E373, F102, I4, J32, K56, L60, N6 |
| VM Reservations & cost | E81, E82, E83–E98, E229, E261, E362, F107, K1, M4, M14 |
| Spot VMs | D29, E363 |
| Availability Sets / Zones (compute) | D12, E350, E392, F19, F20, F112, F115, H9, H12, I59, M27, N22, N29 |
| Azure App Service | A4, A11, D14, E267, E330, E367, F7, F9, F53, F114, G13, H29, I17, L33, N5, N72 |
| Azure Functions | D13, E270, E273, E364, F36, F41, H15, H45, J50, J58, J104, L41 |
| Azure Container Instances (ACI) | B5, F117, F118, J26, M37, N38, N62 |
| Azure Kubernetes Service (AKS) | E244, E272, E329, F44, F45, F118, H44, J24, N32 |
| Azure Virtual Desktop | E75, E76, E77, E79, E331, E391, H34, J112, M34 |
| Azure Batch | E374 |
| Azure Dedicated Hosts | E338 |
| **Networking** | |
| Virtual Networks (VNet) | E36, E37, E39, E40, E111, E113, E114, E239, E328, E406, F71, F119, G14, J103, K40, L67, L73, M65, M66, N76 |
| Subnets | D16, E44, E411, F119, L25 |
| VNet Peering | B18, E45, E118, E351, H40, J39, J71, J81, M3, N69 |
| VPN Gateway (S2S, P2S) | B14, D18, E46, E119–E125, E247, E353, E368, E371, F52, F77, F108, J110, K19 |
| ExpressRoute | B7, D17, E126–E130, E352, G15, I21, J22, J42, K14, L79, M30, M36, N31 |
| NSG (Network Security Groups) | E42, E43, E117, E285, E286, E341, F73, J91, J98, K57, L10, L45, N10, N59 |
| Azure Firewall | E288, E294, E365, F74, G22 |
| Azure DNS | D19, E47, J29, J31 |
| Azure Load Balancer | E233, E241, E266 |
| Azure DDoS Protection | E289, E375, F120 |
| Route Tables / UDR | E44, E116, E280, E287 |
| Hybrid connectivity overview | E115, E409, E419, F51, F52, M52 |

**Conteggio**: ~254 domande

### 2.3 — Describe Azure storage services

📌 **Storage accounts, ridondanza, servizi di storage, tiers, migrazione dati**

| Sotto-tema | Domande |
|------------|---------|
| Storage redundancy: LRS, ZRS, GRS, GZRS, RA-GRS | B9, B19, D21, E21–E35, E366, F1, F59, F101, H47, I70, J84, J125, K5, K6, K7, K88, L62, L81, M54, N35 |
| Blob Storage | B8, D22, E228, E230, E275, E357, E358, F46, F48, F55, F64, G16, H32, J80, K48, N16, N60 |
| File Storage (Azure Files) | E54, E225, E359, E412, F37, F54, I38, I58, J55, N68 |
| Table Storage | E220, F103, M56 |
| Queue Storage | F49, L51, M32 |
| Storage tiers (Hot, Cool, Archive) | B8, E322, E332, F46, F48, K8, L21, L47, L48, M2, M11, N11, N81 |
| Data migration: AzCopy | D20, F91, F100, J2, M85 |
| Data migration: Azure File Sync | D20, E394, F91, G17, G18, H21, J72, M10, M64, M72, N53 |
| Data migration: Storage Explorer | J37, M50 |
| Data migration: Azure Data Box | B10, E1–E4, J78, L85, M9, M23, M60, M67, M68, M79, N2, N24, N74, N78 |

**Conteggio**: ~130 domande

### 2.4 — Describe Azure identity, access, and security

📌 **Entra ID, autenticazione, MFA, Conditional Access, RBAC, Zero Trust, Defender for Cloud**

| Sotto-tema | Domande |
|------------|---------|
| Microsoft Entra ID (Azure AD) | B11, E51, E250, E292, E345, F8, F14, F88, F89, G20, H7, H31, H50, I33, I46, I53, I65, I73, I83, J18, J47, J66, J102, K25, K42, K67, K71, L49, L65, M6, M24, M25, M80, M83, N3, N12, N25, N26, N75 |
| Authentication vs Authorization | B20, D23, E293, F90, F95, F98, J43, L77 |
| MFA | E79, E281, E293, F82, F83, F84, G19, J109, K79, N7, N47, N85 |
| Conditional Access | D23, E369, E395, F82, F83, F92, H11, J105, K63, K83, L23, L40, M58 |
| Passwordless (Windows Hello, FIDO2) | F72, H38 |
| RBAC | B12, B21, D25, E48, E301, E397, F80, F95, G27, H5, I19, I78, J108, L3, M1, M51, N83 |
| Zero Trust | B13, D24, E396, F86, L18, L31, M20, N21 |
| Defense in Depth | E375, H26, I52, I54, I63, I67, J33, L16, M18, N19 |
| Microsoft Defender for Cloud | E282, E290, E295, E323, E340, E341, F70, F81, F85, F104, F105, G21, H20, I57, I74, J27, J45, K41, L1, L34, L75, M55 |
| Azure Key Vault | D26, E184, E206, E226, E283, E339 |
| Identity Protection | E299, F76, F92 |
| Azure Information Protection / Purview | E209, E213, E298, F57, H19, I29, J35, K75, L76, M46, M71, M77, N9, N61 |

**Conteggio**: ~164 domande

---

## Dominio 3 — Describe Azure Management and Governance (30–35%)

### 3.1 — Describe cost management in Azure

📌 **TCO Calculator, Pricing Calculator, Cost Management, Tags, Reservations**

| Sotto-tema | Domande |
|------------|---------|
| Pricing Calculator | C1 (contrast), D28, F47, F106, G24, H35, H46, I69, J117, K21, K76, L89, M31 |
| TCO Calculator | C1, E264, E346, E347, I16, J86, K36, K46, M15, N45 |
| Azure Cost Management + Billing | E55, E248, E263, F110, F113, I41, J14, J59, J97, K9, K31, K77, L9, L29 |
| Tags (cost tracking) | C2, D27, E14, E343, F93, F99, G25, H33, I9, I36, J7, J11, J16, J52, J95, J101, J121, K35, K37, K49, K58, N70, N73 |
| Reservations | C12, E81, E362, F107, I15, K80, L27, L74, M29, M69, M78, N63 |
| Spot VMs | D29, E363, M62 |
| Factors affecting cost | C11, E205, E237, E243, E260, F39, G23, I27, I31, I72, J56, J83, K24, K29, K68, K82, L13, M39, M42 |
| PAYG / expenditure models | E66, E387, F10, F11, F12, F116, I14, I37, K16, K18, M33 |
| Cost optimization (Advisor) | E210, F109, F113, H28, I80, J113, K11, N84 |
| Resource group cost (free) | E249, F111 |

**Conteggio**: ~141 domande

### 3.2 — Describe features and tools for governance and compliance

📌 **Azure Policy, Blueprints, Resource Locks, Microsoft Purview, Service Trust Portal**

| Sotto-tema | Domande |
|------------|---------|
| Azure Policy | C3, D30, E49, E50, E215, E284, E300, E342, E398, E418, F50, F75, F79, F94, F97 (contrast), G26, G28, H23, H36, J122, K34, K61, K62, L17, L46, M7, M19, N4, N49 |
| Azure Blueprints | C10, C13, E258, E304, E344, E399, F87, J65, J96, N43 |
| Resource Locks | C4, C9, C15, D31, E254, E302, F78, F97, H24, I56, I66, J25, J61, J82, J120, K17, K28, K32, K59, L15, L43, L56, L57, L71, M38, N17 |
| Microsoft Purview | F57 |
| Compliance (NIST, HIPAA, PCI DSS) | E191–E200, E320, E321, F85, F105 |
| Service Trust Portal | — |

**Conteggio**: ~85 domande

### 3.3 — Describe features and tools for managing and deploying Azure resources

📌 **Azure Portal, CLI, PowerShell, Cloud Shell, ARM templates, Bicep, Azure Arc**

| Sotto-tema | Domande |
|------------|---------|
| Azure Portal | E246, E308, E425, F61, H6, K38, K47 |
| Azure CLI / PowerShell / Cloud Shell | C14, E201, E271, E313, E336, E337, E425, G29, I34, J28, J44, J94, J106, K26, L4, L19, L30, M21 |
| ARM templates / Bicep (IaC) | C6, D33, E8, E269, F16, F17, F18, F38, G31, H3, J100, L6, L28, L37, L61, L82, L83, L88, M5, M17, M44, M61, N18, N64 |
| Azure Arc | C7, D32, E63, E400, G30, H10, J12, J74, K39, L2, L5, L36, M12, N30, N33 |
| Azure Marketplace | E236, E416 |

**Conteggio**: ~69 domande

### 3.4 — Describe monitoring tools in Azure

📌 **Azure Advisor, Azure Monitor, Service Health, Log Analytics, Application Insights**

| Sotto-tema | Domande |
|------------|---------|
| Azure Advisor | C5, D34, E210, E303, E402, F65, F109, F113, G32, H49, I68, J48, J77, K69 |
| Azure Monitor | C8, E231, E240, E360, E414, E428, F42, F68, F69, G34, H2, I49, J69, K2, K22, K52, L26, L69, L70, M28 |
| Log Analytics / KQL | C8, E360, J51, K86, L44 |
| Application Insights | F63, F66, F67, H22 |
| Azure Service Health | C16, D35, E212, E217, E222, E403, E415, G33, H42, I6, I8, J10, J13, J53, J63, J115, K33, L22, L63, N55 |

**Conteggio**: ~63 domande

---

## 🗺️ Domande di nicchia / specialistiche (fuori scope AZ-900 ma presenti nel file)

Queste domande sono utili come cultura generale ma difficilmente compaiono all'esame:

| Area | Domande |
|------|---------|
| Azure Cosmos DB (dettagli avanzati) | E131–E150, E214, E219, E224, E279, E354–E356, I82, J116, L14, N56, N87 |
| Azure Synapse Analytics | E151–E160, E185, E223, E276, E333 |
| Azure IoT Hub (dettagli) | E161–E179, E312, E361 |
| Azure AI Services / Machine Learning | D15, E53, E181–E190, E334, E427, F13, F15 |
| NIST CSF / compliance framework (dettagli) | E191–E200 |
| VM Reservations (procedure acquisto) | E83–E98, E99, E100 |
| Azure support plans (dettagli) | F2, F3, E305, E306, E308, E309 |
| Disaster Recovery plans (processo) | E15–E20, K12, L87 |
| Azure DevTest Labs | E311 |
| Other (fuori scope) | E64, E218, E234, E255, E268, E274, E277, E296, E297, E307, E314, E315, E335, E404, H30, I76, L38, M63, M75, N28, N40 |

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
