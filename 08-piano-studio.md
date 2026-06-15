# 08 — Piano di Studio 12 Settimane (AZ-900)

> **Obiettivo**: superare l'esame **Microsoft Azure Fundamentals (AZ-900)** entro il **15 settembre 2026**.
>
> | Dato | Valore |
> |------|--------|
> | Data inizio | 16 giugno 2026 |
> | Data esame (target) | ~15 settembre 2026 |
> | Durata piano | 12 settimane |
> | Impegno giornaliero | ~1–1.5 ore, 5 giorni/settimana (lun–ven) |
> | Formato esame | 40–60 domande, ~45 minuti, soglia ~700/1000 |
> | Prenotazione esame | **Settimane 8–9** (crea pressione positiva) |
>
> ### Pesi dei domini
>
> | Dominio | Peso | Domande nel vault | Stato errori |
> |---------|------|-------------------|--------------|
> | 1 — Cloud Concepts | 25–30% | ~425 | 4 errori (9%) |
> | 2 — Architecture & Services | 35–40% | ~788 | 9 errori (20%) |
> | 3 — Management & Governance | 30–35% | ~546 | **32 errori (71%)** — area critica |
>
> ### Struttura del piano
>
> | Fase | Settimane | Focus |
> |------|-----------|-------|
> | **Teoria** | 1–4 | Un dominio alla volta, studio dei file 01–03 |
> | **Pratica** | 5–9 | Domande per dominio con ripetizione spaziata |
> | **Simulazione** | 10–12 | Mock exam cronometrati, revisione finale |

---

## Fase 1 — Teoria (Settimane 1–4)

---

### Settimana 1 — Dominio 1: Cloud Concepts (25–30%)

**Obiettivo della settimana**: padroneggiare i concetti fondamentali del cloud computing — modelli di deployment, shared responsibility, IaaS/PaaS/SaaS, CapEx vs OpEx.

**File da consultare**:
- `01-cloud-concepts.md` — teoria completa del Dominio 1
- `05-cheat-sheet.md` — tabelle "Cloud Concepts — Easily Confused Terms", "Shared Responsibility", "IaaS/PaaS/SaaS"
- `00-glossario.md` — termini: cloud computing, scalability, elasticity, agility, fault tolerance, HA, DR

**Argomenti chiave**:
- Definizione cloud computing, modelli (public, private, hybrid, multi-cloud)
- Shared responsibility model (cosa gestisci tu vs il provider)
- Consumption-based model, CapEx vs OpEx
- Benefici: HA, scalabilità, elasticità, affidabilità, prevedibilità, governance
- IaaS vs PaaS vs SaaS — definizioni, responsabilità, casi d'uso
- Serverless: Azure Functions, Logic Apps, Event Grid

**Attivita giornaliere**:

Lunedi:
- [ ] Leggere `01-cloud-concepts.md` sezione 1.1 — definizione cloud, modelli di deployment
- [ ] Annotare le differenze tra public, private, hybrid cloud
- [ ] Consultare `00-glossario.md` per i termini nuovi

Martedi:
- [ ] Leggere `01-cloud-concepts.md` sezione 1.1 — shared responsibility model
- [ ] Studiare la tabella "Always Yours vs Always Provider" in `05-cheat-sheet.md`
- [ ] Leggere `01-cloud-concepts.md` sezione 1.1 — consumption-based model, CapEx vs OpEx

Mercoledi:
- [ ] Leggere `01-cloud-concepts.md` sezione 1.2 — benefici del cloud
- [ ] Memorizzare le distinzioni: scalability vs elasticity vs agility (vedi `05-cheat-sheet.md`)
- [ ] Memorizzare: fault tolerance vs HA vs DR vs reliability

Giovedi:
- [ ] Leggere `01-cloud-concepts.md` sezione 1.3 — IaaS, PaaS, SaaS
- [ ] Studiare la tabella IaaS/PaaS/SaaS in `05-cheat-sheet.md`
- [ ] Memorizzare: "IaaS = lift-and-shift", "PaaS = dev framework", "SaaS = email/produttivita"

Venerdi:
- [ ] Ripassare serverless (Functions, Logic Apps, Event Grid) e container spectrum (ACI, Container Apps, AKS)
- [ ] Fare 10–15 domande di prova dal Dominio 1 in `04a-domande-curate.md` sezione A (A1–A12)
- [ ] Rileggere le note della settimana e segnare i punti deboli

**Fine settimana: auto-valutazione**:
- [ ] Riesci a spiegare a voce i 3 modelli cloud (public/private/hybrid)?
- [ ] Sai distinguere IaaS/PaaS/SaaS con un esempio per ciascuno?
- [ ] Conosci la differenza tra scalabilita ed elasticita?
- Punteggio auto-valutazione (1–5): ___

---

### Settimana 2 — Dominio 2 parte A: Architettura Azure (componenti core + compute)

**Obiettivo della settimana**: comprendere l'architettura di base di Azure — regions, zones, resource groups, subscriptions, management groups — e i servizi di compute.

**File da consultare**:
- `02-azure-architecture-services.md` — sezioni 2.1 (architettura core) e 2.2 (compute)
- `05-cheat-sheet.md` — "VM SLA by Configuration", "Container Spectrum"
- `00-glossario.md` — termini: region, availability zone, resource group, subscription, ARM

**Argomenti chiave**:
- Regions, region pairs, availability zones, sovereign regions
- Risorse, resource groups, subscriptions, management groups (gerarchia)
- Azure Resource Manager (ARM)
- VMs, VM Scale Sets, Spot VMs, Dedicated Hosts
- App Service, Azure Functions, ACI, AKS
- Azure Virtual Desktop, Azure Batch
- **Trappola**: AKS e PaaS, NON IaaS (vedi `07-statistiche-errori.md`)

**Attivita giornaliere**:

Lunedi:
- [ ] Leggere `02-azure-architecture-services.md` sezione 2.1 — regions, availability zones, region pairs
- [ ] Memorizzare: availability zones = 3 datacenter separati nella stessa region
- [ ] Studiare sovereign regions (US Gov, China)

Martedi:
- [ ] Leggere `02-azure-architecture-services.md` sezione 2.1 — resource groups, subscriptions, management groups
- [ ] Comprendere la gerarchia: Management Group > Subscription > Resource Group > Resource
- [ ] Studiare ARM (Azure Resource Manager) — punto di accesso per tutte le operazioni

Mercoledi:
- [ ] Leggere `02-azure-architecture-services.md` sezione 2.2 — VMs, VM Scale Sets
- [ ] Studiare availability sets vs availability zones per le VM
- [ ] Memorizzare SLA: Single VM (Premium SSD) 99.9% > Availability Set 99.95% > AZ 99.99%

Giovedi:
- [ ] Leggere `02-azure-architecture-services.md` sezione 2.2 — App Service, Functions, ACI, AKS
- [ ] Memorizzare: **AKS = PaaS** (Azure gestisce il control plane)
- [ ] Ripassare Container Spectrum: ACI (semplice) > Container Apps (elastic) > AKS (full K8s)

Venerdi:
- [ ] Leggere Azure Virtual Desktop, Spot VMs, Azure Batch
- [ ] Fare 10–15 domande dalla sezione B di `04a-domande-curate.md` (B1–B10)
- [ ] Ripassare appunti della settimana

**Fine settimana: auto-valutazione**:
- [ ] Sai disegnare la gerarchia Azure (Management Group > Subscription > RG > Resource)?
- [ ] Conosci la differenza tra availability set e availability zone?
- [ ] Sai classificare AKS, App Service, VMs nel modello IaaS/PaaS?
- Punteggio auto-valutazione (1–5): ___

---

### Settimana 3 — Dominio 2 parte B: Networking, Storage, Identita e Sicurezza

**Obiettivo della settimana**: completare il Dominio 2 — networking, storage, identita (Entra ID), sicurezza.

**File da consultare**:
- `02-azure-architecture-services.md` — sezioni 2.2 (networking), 2.3 (storage), 2.4 (identita e sicurezza)
- `05-cheat-sheet.md` — "Storage Redundancy", "Blob Storage Tiers", "Zero Trust", "Defense in Depth", "External Identities"
- `00-glossario.md` — termini: VNet, NSG, VPN Gateway, ExpressRoute, LRS, ZRS, GRS, Entra ID, RBAC, MFA

**Argomenti chiave**:
- **Networking**: VNet, subnets, peering, VPN Gateway (S2S, P2S), ExpressRoute, NSG, Azure Firewall, DNS, Load Balancer, DDoS Protection
- **Storage**: account storage, ridondanza (LRS/ZRS/GRS/GZRS/RA-GRS), Blob (tiers: Hot/Cool/Cold/Archive), Files, Table, Queue, migrazione dati (AzCopy, Data Box, File Sync)
- **Identita**: Entra ID, autenticazione vs autorizzazione, MFA, Conditional Access, passwordless, RBAC
- **Sicurezza**: Zero Trust (3 principi + 6 pilastri), Defense in Depth (7 livelli), Defender for Cloud, Key Vault, Purview
- **Trappole**: RBAC e additivo, VNet-to-VNet (non S2S) per connettere due VNet, Azure Files supporta GZRS ma NON RA-GRS/RA-GZRS

**Attivita giornaliere**:

Lunedi:
- [ ] Leggere sezione 2.2 networking — VNet, subnets, VNet Peering
- [ ] Studiare VPN Gateway: Site-to-Site (on-prem), Point-to-Site (singolo device), VNet-to-VNet
- [ ] Leggere ExpressRoute — connessione privata, non passa per internet pubblico

Martedi:
- [ ] Studiare NSG, Azure Firewall, DDoS Protection, Load Balancer
- [ ] Leggere sezione 2.3 storage — ridondanza (LRS, ZRS, GRS, GZRS)
- [ ] Memorizzare la "Durability Ladder" da `05-cheat-sheet.md`

Mercoledi:
- [ ] Studiare Blob Storage (tiers Hot/Cool/Cold/Archive), Azure Files, Table, Queue
- [ ] Leggere strumenti di migrazione dati: AzCopy, Azure Data Box, Azure File Sync, Storage Explorer
- [ ] **Ricordare**: si puo cambiare la replica di un account storage (LRS>GRS ecc.)

Giovedi:
- [ ] Leggere sezione 2.4 — Entra ID, autenticazione vs autorizzazione, MFA, Conditional Access
- [ ] Studiare RBAC: **additivo** (i permessi si sommano, mai deny)
- [ ] Memorizzare: B2C = consumatori, B2B = partner, Entra ID = SSO aziendale

Venerdi:
- [ ] Studiare Zero Trust, Defense in Depth, Defender for Cloud, Key Vault
- [ ] Fare 10–15 domande dalla sezione B di `04a-domande-curate.md` (B11–B22) e sezione D (D11–D26)
- [ ] Ripassare tutte le trappole del Dominio 2 da `07-statistiche-errori.md`

**Fine settimana: auto-valutazione**:
- [ ] Sai spiegare le 4 opzioni di ridondanza storage (LRS/ZRS/GRS/GZRS)?
- [ ] Conosci i 3 principi Zero Trust?
- [ ] Sai la differenza tra VPN Gateway ed ExpressRoute?
- [ ] Sai cosa fa RBAC e perche e additivo?
- Punteggio auto-valutazione (1–5): ___

---

### Settimana 4 — Dominio 3: Management & Governance (area critica, 71% errori)

**Obiettivo della settimana**: studiare a fondo il Dominio 3 — costi, governance, strumenti di gestione, monitoraggio. Questa e l'area piu debole (71% degli errori nelle fonti).

**File da consultare**:
- `03-azure-management-governance.md` — tutte le sezioni (3.1–3.4)
- `05-cheat-sheet.md` — "Pricing Options", "Advisor Categories", "Governance Hierarchy", "Resource Lock Types", "Support Plans"
- `07-statistiche-errori.md` — **leggere TUTTO**, specialmente la checklist pre-esame
- `00-glossario.md` — termini: Azure Policy, Blueprints, ARM Templates, Bicep, Azure Arc, Azure Advisor, Azure Monitor

**Argomenti chiave**:
- **3.1 Costi**: Pricing Calculator, ~~TCO Calculator~~ (DEPRECATO ago 2025), Cost Management + Billing, tags, reservations, Spot VMs, fattori che influenzano il costo
- **3.2 Governance**: Azure Policy (vs initiative), ~~Blueprints~~ (IN RITIRO > Template Specs + Deployment Stacks), Resource Locks (Delete vs ReadOnly), Microsoft Purview, Service Trust Portal, compliance
- **3.3 Strumenti**: Portal, CLI, PowerShell, Cloud Shell, ARM Templates, Bicep, Azure Arc, Marketplace
- **3.4 Monitoraggio**: Azure Advisor (5 categorie: RSPOC), Azure Monitor, Log Analytics, Application Insights, Service Health (3 livelli)
- **Trappole critiche** (da `07-statistiche-errori.md`):
  - TCO Calculator deprecato > usa Pricing Calculator
  - Blueprints in ritiro > Template Specs + Deployment Stacks
  - Reservation = **OpEx** (non CapEx)
  - Lock: Owner + User Access Admin possono gestirli
  - Due tipi lock: Delete (read+modify OK) e ReadOnly (solo read)
  - Cost Management = analisi/budget, Advisor = raccomandazioni

**Attivita giornaliere**:

Lunedi:
- [ ] Leggere `03-azure-management-governance.md` sezione 3.1 — costi
- [ ] Memorizzare: **TCO Calculator e DEPRECATO** (agosto 2025), usa solo Pricing Calculator
- [ ] Studiare: reservation (1 o 3 anni, mai 5), Savings Plan, Spot VMs
- [ ] **Reservation = OpEx** (nessun asset fisico acquistato, non e CapEx)

Martedi:
- [ ] Leggere sezione 3.1 — Cost Management, tags, fattori di costo
- [ ] Memorizzare: Cost Management = analisi/budget, **Advisor** = raccomandazioni (categoria Cost)
- [ ] Studiare: tags NON ereditano da resource group/subscription
- [ ] Leggere sezione 3.2 — Azure Policy, initiative

Mercoledi:
- [ ] Studiare sezione 3.2 — Blueprints (in ritiro), Resource Locks
- [ ] Memorizzare: **Blueprints in ritiro** > Template Specs + Deployment Stacks
- [ ] Memorizzare i 2 tipi di lock: Delete (read+modify, no cancella) e ReadOnly (solo read)
- [ ] Lock: Owner + User Access Admin possono gestirli (non solo subscription owner)
- [ ] Studiare Purview, Service Trust Portal, compliance (NIST, HIPAA, PCI DSS)

Giovedi:
- [ ] Leggere sezione 3.3 — strumenti di gestione
- [ ] Studiare ARM Templates (JSON, dichiarativi, idempotenti) e Bicep
- [ ] Studiare Azure Arc (5 tipi: servers, K8s, data services, SQL Server, VMs)
- [ ] CLI vs PowerShell vs Cloud Shell (requisiti: resource group, storage account, file share)

Venerdi:
- [ ] Leggere sezione 3.4 — monitoraggio
- [ ] Memorizzare le 5 categorie di Advisor: **R**eliability, **S**ecurity, **P**erformance, **O**perational Excellence, **C**ost
- [ ] Studiare Azure Monitor, Log Analytics, Application Insights
- [ ] Service Health: 3 livelli (Azure Status > Service Health > Resource Health)
- [ ] Studiare i support plan: Basic (no ticket tecnici!) > Developer > Standard > Pro Direct > Premier
- [ ] Fare 10–15 domande dalla sezione C di `04a-domande-curate.md` (C1–C16) e sezione D (D27–D35)

**Fine settimana: auto-valutazione**:
- [ ] Sai elencare le 5 categorie di Azure Advisor?
- [ ] Conosci la differenza tra Azure Policy e initiative?
- [ ] Sai che TCO Calculator e deprecato e Blueprints e in ritiro?
- [ ] Sai la differenza tra lock Delete e ReadOnly?
- [ ] Sai cosa fa Azure Arc?
- Punteggio auto-valutazione (1–5): ___

---

## Fase 2 — Pratica (Settimane 5–9)

> **Strategia domande**: segui l'ordine di qualita delle fonti:
> 1. `04a-domande-curate.md` (sezioni A–D, G) — alta qualita, pochi errori
> 2. `04d-practice-test.md` (sezioni H–N) — buona copertura, attenzione alle deprecazioni
> 3. `04c-domande-examtopics.md` (sezione F) — ExamTopics, qualita media
> 4. `04b-domande-ipspecialist.md` (sezione E) — **ultima**, fonte meno affidabile (20 errori)
>
> Usa `06-indice-tematico-esame.md` per filtrare le domande per dominio/sotto-tema.
>
> **Regola ripetizione spaziata**: mentre pratichi il dominio corrente, ripassa il precedente (10–15 min/giorno).

---

### Settimana 5 — Pratica Dominio 1 (Cloud Concepts)

**Obiettivo della settimana**: rispondere a tutte le domande del Dominio 1 dalle fonti di alta qualita. Consolidare la teoria.

**File da consultare**:
- `06-indice-tematico-esame.md` — Dominio 1, sezioni 1.1, 1.2, 1.3
- `04a-domande-curate.md` — sezioni A (A1–A12), G (G1–G9)
- `04d-practice-test.md` — domande D1 mappate in 06 (H, I, J, K, L, M, N)
- `01-cloud-concepts.md` — per ripassare i concetti sbagliati

**Argomenti chiave**: tutti quelli del Dominio 1 (shared responsibility, CapEx/OpEx, IaaS/PaaS/SaaS, benefici cloud)

**Attivita giornaliere**:

Lunedi:
- [ ] Completare tutte le domande sezione A (A1–A12) in `04a-domande-curate.md`
- [ ] Segnare le risposte sbagliate con un marker (es. ❌ accanto alla domanda)
- [ ] Per ogni errore: rileggere la spiegazione e il paragrafo corrispondente in `01-cloud-concepts.md`

Martedi:
- [ ] Completare domande sezione G (G1–G9) in `04a-domande-curate.md`
- [ ] Iniziare domande D1 da `04d-practice-test.md`: sotto-tema 1.1 (vedi `06-indice-tematico-esame.md` per i numeri)
- [ ] Segnare errori e ripassare

Mercoledi:
- [ ] Continuare domande D1 da `04d-practice-test.md`: sotto-tema 1.2 (benefici cloud)
- [ ] Ripassare le domande sbagliate di lunedi e martedi (ripetizione spaziata)

Giovedi:
- [ ] Completare domande D1 da `04d-practice-test.md`: sotto-tema 1.3 (IaaS/PaaS/SaaS)
- [ ] Fare domande D1 da `04c-domande-examtopics.md` sezione F (F10–F12, F21–F36 ecc. — vedi indice)

Venerdi:
- [ ] Ripassare TUTTE le domande sbagliate del Dominio 1 della settimana
- [ ] Creare una lista personale di "punti deboli D1" da rivedere
- [ ] Opzionale: iniziare domande D1 da `04b-domande-ipspecialist.md` sezione E (con cautela — verificare con `07-statistiche-errori.md`)

**Fine settimana: auto-valutazione**:
- [ ] Percentuale risposte corrette D1 (target: >80%): ___%
- [ ] Quali sotto-temi hanno piu errori?
- [ ] Riesci a rispondere senza guardare le opzioni?
- Punteggio auto-valutazione (1–5): ___

---

### Settimana 6 — Pratica Dominio 2 parte A (Architettura core + Compute)

**Obiettivo della settimana**: rispondere alle domande del Dominio 2 sezioni 2.1 e 2.2. Ripasso parallelo Dominio 1.

**File da consultare**:
- `06-indice-tematico-esame.md` — Dominio 2, sezioni 2.1, 2.2
- `04a-domande-curate.md` — sezione B (B1–B7), D (D9–D19)
- `04d-practice-test.md` — domande D2 (2.1 + 2.2) mappate in 06
- `02-azure-architecture-services.md` — per ripassare i concetti sbagliati

**Attivita giornaliere**:

Lunedi:
- [ ] Domande sezione B (B1–B7) da `04a-domande-curate.md` — architettura core
- [ ] Domande sezione D (D9–D19) da `04a-domande-curate.md` — compute e networking
- [ ] Ripasso D1 (10 min): rileggere la lista "punti deboli D1"

Martedi:
- [ ] Domande D2 sotto-tema 2.1 da `04d-practice-test.md` (regions, RG, subscriptions, ARM)
- [ ] Segnare errori, rileggere `02-azure-architecture-services.md` per le parti sbagliate
- [ ] Ripasso D1 (10 min): rifare 5 domande sbagliate dalla settimana 5

Mercoledi:
- [ ] Domande D2 sotto-tema 2.2 compute da `04d-practice-test.md` (VMs, App Service, Functions, AKS)
- [ ] **Attenzione**: AKS = PaaS (verifica con `07-statistiche-errori.md` errore E244)
- [ ] Ripasso D1 (10 min)

Giovedi:
- [ ] Domande D2 sotto-tema 2.2 networking da `04d-practice-test.md` (VNet, VPN, ExpressRoute, NSG)
- [ ] Domande D2 da `04c-domande-examtopics.md` sezione F (vedi indice per i numeri)
- [ ] **Attenzione**: VNet-to-VNet per connettere due VNet, non Site-to-Site

Venerdi:
- [ ] Ripassare tutte le domande sbagliate D2 (2.1 + 2.2) della settimana
- [ ] Creare lista "punti deboli D2-A"
- [ ] Ripasso D1 finale (10 min)

**Fine settimana: auto-valutazione**:
- [ ] Percentuale risposte corrette D2 (2.1+2.2) (target: >75%): ___%
- [ ] Sai la gerarchia Azure a memoria?
- [ ] Sai distinguere tutti i servizi compute?
- Punteggio auto-valutazione (1–5): ___

---

### Settimana 7 — Pratica Dominio 2 parte B (Storage + Identita/Sicurezza)

**Obiettivo della settimana**: completare le domande del Dominio 2 sezioni 2.3 e 2.4. Ripasso parallelo Domini 1 e 2A.

**File da consultare**:
- `06-indice-tematico-esame.md` — Dominio 2, sezioni 2.3, 2.4
- `04a-domande-curate.md` — sezione B (B8–B22), D (D20–D26)
- `04d-practice-test.md` — domande D2 (2.3 + 2.4) mappate in 06
- `02-azure-architecture-services.md` — per ripassare

**Attivita giornaliere**:

Lunedi:
- [ ] Domande sezione B (B8–B14) da `04a-domande-curate.md` — storage
- [ ] Domande sezione D (D20–D22) da `04a-domande-curate.md` — storage
- [ ] Ripasso D2-A (10 min): rileggere lista "punti deboli D2-A"

Martedi:
- [ ] Domande D2 sotto-tema 2.3 da `04d-practice-test.md` (storage ridondanza, blob, files, migrazione)
- [ ] **Ricordare**: si puo cambiare la replica di un account storage; Azure Files supporta GZRS ma NON RA-GRS/RA-GZRS
- [ ] Ripasso D1 (10 min)

Mercoledi:
- [ ] Domande sezione B (B15–B22) e D (D23–D26) da `04a-domande-curate.md` — identita e sicurezza
- [ ] Domande D2 sotto-tema 2.4 da `04d-practice-test.md` (Entra ID, RBAC, Zero Trust, Defender)
- [ ] **Ricordare**: RBAC e additivo, B2C = consumatori

Giovedi:
- [ ] Domande D2 (2.3 + 2.4) da `04c-domande-examtopics.md` sezione F
- [ ] Opzionale: domande D2 da `04b-domande-ipspecialist.md` sezione E (con cautela)
- [ ] Ripasso D2-A (10 min)

Venerdi:
- [ ] Ripassare tutte le domande sbagliate D2 (2.3 + 2.4) della settimana
- [ ] Creare lista unificata "punti deboli D2"
- [ ] Rivedere TUTTE le trappole D2 da `07-statistiche-errori.md`

**Fine settimana: auto-valutazione**:
- [ ] Percentuale risposte corrette D2 (2.3+2.4) (target: >75%): ___%
- [ ] Sai le 4 opzioni di ridondanza storage e i relativi "nines"?
- [ ] Sai i 3 principi Zero Trust e i 7 livelli Defense in Depth?
- Punteggio auto-valutazione (1–5): ___

---

### Settimana 8 — Pratica Dominio 3 (Management & Governance) + PRENOTA ESAME

**Obiettivo della settimana**: affrontare le domande del Dominio 3 — l'area piu critica. **Prenotare l'esame** per creare pressione positiva.

> **IMPORTANTE**: Entro venerdi di questa settimana, prenota l'esame AZ-900 su [Microsoft Learn](https://learn.microsoft.com/certifications/exams/az-900/) per una data intorno al 15 settembre 2026. Costo: ~$99 USD (o equivalente locale). Verifica se esistono voucher gratuiti (Microsoft Virtual Training Days, GitHub Student Pack, ecc.).

**File da consultare**:
- `06-indice-tematico-esame.md` — Dominio 3, sezioni 3.1, 3.2, 3.3, 3.4
- `04a-domande-curate.md` — sezione C (C1–C16), sezione D (D27–D35)
- `04d-practice-test.md` — domande D3 mappate in 06
- `03-azure-management-governance.md` — per ripassare
- `07-statistiche-errori.md` — **consultare frequentemente** (71% degli errori e qui)

**Attivita giornaliere**:

Lunedi:
- [ ] Domande sezione C (C1–C16) da `04a-domande-curate.md` — governance completa
- [ ] Domande sezione D (D27–D35) da `04a-domande-curate.md` — costi e monitoraggio
- [ ] Per ogni errore: rileggere `03-azure-management-governance.md` e `07-statistiche-errori.md`

Martedi:
- [ ] Domande D3 sotto-tema 3.1 da `04d-practice-test.md` (costi, Pricing Calculator, tags, reservations)
- [ ] **TCO Calculator = DEPRECATO**: dove la domanda cita TCO, la risposta corrente e Pricing Calculator
- [ ] **Reservation = OpEx**, non CapEx
- [ ] Ripasso D2 (10 min)

Mercoledi:
- [ ] Domande D3 sotto-tema 3.2 da `04d-practice-test.md` (Policy, Blueprints, Locks, compliance)
- [ ] **Blueprints = IN RITIRO** > Template Specs + Deployment Stacks
- [ ] **Lock**: Owner + User Access Admin possono gestirli; Delete vs ReadOnly
- [ ] Ripasso D1 (10 min)

Giovedi:
- [ ] Domande D3 sotto-temi 3.3 e 3.4 da `04d-practice-test.md` (strumenti, monitoraggio)
- [ ] **Advisor = raccomandazioni** (5 categorie RSPOC), **Cost Management = analisi/budget**
- [ ] Cloud Shell requisiti: resource group + storage account + file share
- [ ] Domande D3 da `04c-domande-examtopics.md` sezione F

Venerdi:
- [ ] Ripassare TUTTE le domande sbagliate D3 della settimana
- [ ] Rileggere la checklist pre-esame in `07-statistiche-errori.md`
- [ ] **PRENOTA L'ESAME** per ~15 settembre 2026
- [ ] Ripasso D1 + D2 (15 min totali)

**Fine settimana: auto-valutazione**:
- [ ] Percentuale risposte corrette D3 (target: >70% — e il dominio piu difficile): ___%
- [ ] Hai prenotato l'esame? Data: ___
- [ ] Sai elencare le 5 trappole principali da `07-statistiche-errori.md`?
- Punteggio auto-valutazione (1–5): ___

---

### Settimana 9 — Consolidamento + Domande residue

**Obiettivo della settimana**: completare le domande rimaste (04b IPSpecialist con cautela), rinforzare i punti deboli di tutti e 3 i domini.

**File da consultare**:
- `04b-domande-ipspecialist.md` — sezione E (usare con `07-statistiche-errori.md` a portata di mano)
- `06-indice-tematico-esame.md` — per navigare le domande per tema
- `07-statistiche-errori.md` — le 16 risposte errate dalla fonte da conoscere
- Tutti i file teoria (01, 02, 03) per i punti deboli

**Attivita giornaliere**:

Lunedi:
- [ ] Domande IPSpecialist (E) — Dominio 1: E56–E71, E101–E110 ecc. (vedi indice)
- [ ] **Attenzione**: verificare ogni risposta dubbia con la teoria in `01-cloud-concepts.md`
- [ ] Tenere aperto `07-statistiche-errori.md` per le domande segnalate (E55, E94, E244, E369, E397 ecc.)

Martedi:
- [ ] Domande IPSpecialist (E) — Dominio 2: sezioni compute, networking, storage
- [ ] Verificare con `02-azure-architecture-services.md` in caso di dubbio
- [ ] Ripasso punti deboli D3 (15 min)

Mercoledi:
- [ ] Domande IPSpecialist (E) — Dominio 3: governance, costi, monitoraggio
- [ ] **Massima attenzione**: 20 errori su 45 totali vengono da IPSpecialist
- [ ] Verificare con `03-azure-management-governance.md` e `07-statistiche-errori.md`

Giovedi:
- [ ] Rivedere TUTTE le domande sbagliate accumulate nelle settimane 5–9
- [ ] Creare un documento personale "Errori ricorrenti" con le domande che sbagli piu di una volta
- [ ] Ripasso delle trappole da `07-statistiche-errori.md`

Venerdi:
- [ ] Rifare le 10 domande piu difficili di ogni dominio (30 domande totali)
- [ ] Leggere le sezioni "Domande di nicchia / specialistiche" in `06-indice-tematico-esame.md` — sapere che esistono ma non sono prioritarie
- [ ] Se disponibile: rivedere `09-flashcards.md` per i concetti chiave

**Fine settimana: auto-valutazione**:
- [ ] Percentuale complessiva risposte corrette (target: >80%): ___%
- [ ] Quali sono i tuoi 3 punti piu deboli rimasti?
- [ ] Ti senti pronto per le simulazioni?
- Punteggio auto-valutazione (1–5): ___

---

## Fase 3 — Simulazione (Settimane 10–12)

---

### Settimana 10 — Prime simulazioni cronometrate

**Obiettivo della settimana**: fare 2–3 mock exam completi in condizioni reali (45 minuti, nessun aiuto). Identificare le aree ancora deboli.

**File da consultare**:
- `10-simulazioni-esame.md` — simulazioni cronometrate (quando disponibile)
- `04d-practice-test.md` — sezioni H, I, J come mock test (50–65 domande ciascuna)
- `05-cheat-sheet.md` — solo DOPO la simulazione, per verificare
- `07-statistiche-errori.md` — per verificare risposte dubbie

**Attivita giornaliere**:

Lunedi:
- [ ] **Simulazione 1**: sezione H di `04d-practice-test.md` (~50 domande)
- [ ] Timer: 45 minuti, nessun materiale aperto
- [ ] Alla fine: correggi, segna il punteggio, annota le domande sbagliate

Martedi:
- [ ] Analisi errori Simulazione 1: per ogni errore, identifica il dominio e sotto-tema
- [ ] Ripassa la teoria corrispondente in 01/02/03
- [ ] Consulta `05-cheat-sheet.md` per i concetti sbagliati

Mercoledi:
- [ ] **Simulazione 2**: sezione I di `04d-practice-test.md` (~83 domande — prendi piu tempo se necessario)
- [ ] Timer: 45–60 minuti
- [ ] Correggi e segna il punteggio

Giovedi:
- [ ] Analisi errori Simulazione 2
- [ ] Confronta gli errori tra Simulazione 1 e 2: quali temi si ripetono?
- [ ] Studio mirato sui temi ricorrenti

Venerdi:
- [ ] **Simulazione 3**: sezione J di `04d-practice-test.md` (~125 domande — selezionarne ~50 a caso)
- [ ] Oppure usa `10-simulazioni-esame.md` se disponibile
- [ ] Correggi, segna punteggio, identifica gli ultimi punti deboli

**Fine settimana: auto-valutazione**:
- [ ] Punteggi simulazioni: S1 ___%, S2 ___%, S3 ___%
- [ ] Target minimo per sentirsi pronti: >85%
- [ ] Aree ancora deboli: ___
- Punteggio auto-valutazione (1–5): ___

---

### Settimana 11 — Rinforzo mirato + simulazioni aggiuntive

**Obiettivo della settimana**: colmare le lacune emerse dalle simulazioni. Fare 2 ulteriori mock exam.

**File da consultare**:
- `10-simulazioni-esame.md` — simulazioni aggiuntive (quando disponibile)
- `04d-practice-test.md` — sezioni K, L, M come mock test
- File di teoria (01, 02, 03) per le aree deboli
- `09-flashcards.md` — ripasso rapido (quando disponibile)
- `07-statistiche-errori.md` — checklist pre-esame

**Attivita giornaliere**:

Lunedi:
- [ ] Studio mirato: ripassare i 3 temi piu deboli emersi dalla settimana 10
- [ ] Rileggere le sezioni pertinenti in 01/02/03
- [ ] Rifare 15–20 domande sbagliate nelle simulazioni precedenti

Martedi:
- [ ] **Simulazione 4**: sezione K di `04d-practice-test.md`
- [ ] Timer: 45 minuti
- [ ] Correggi e confronta con simulazioni precedenti — il punteggio sta migliorando?

Mercoledi:
- [ ] Analisi errori Simulazione 4
- [ ] Ripasso con `09-flashcards.md` (se disponibile) — focus sui concetti sbagliati
- [ ] Rileggere `05-cheat-sheet.md` sezioni pertinenti

Giovedi:
- [ ] **Simulazione 5**: sezione L o M di `04d-practice-test.md`
- [ ] Timer: 45 minuti
- [ ] Correggi e analizza

Venerdi:
- [ ] Rileggere TUTTA la checklist pre-esame in `07-statistiche-errori.md`
- [ ] Rivedere le 5 trappole principali: TCO deprecato, Blueprints in ritiro, Reservations=OpEx, AKS=PaaS, RBAC additivo
- [ ] Ripassare con `05-cheat-sheet.md` — leggerlo TUTTO come ripasso veloce

**Fine settimana: auto-valutazione**:
- [ ] Punteggi simulazioni: S4 ___%, S5 ___%
- [ ] Trend: i punteggi stanno migliorando? Si/No
- [ ] Ci sono ancora temi sotto il 70%? Quali?
- Punteggio auto-valutazione (1–5): ___

---

### Settimana 12 — Revisione finale e preparazione all'esame

**Obiettivo della settimana**: consolidamento finale. Niente materiale nuovo — solo ripasso e simulazione. Arrivare all'esame con fiducia.

**File da consultare**:
- `05-cheat-sheet.md` — ripasso quotidiano
- `07-statistiche-errori.md` — checklist pre-esame (rileggere ogni giorno)
- `09-flashcards.md` — ripasso flashcards (quando disponibile)
- `10-simulazioni-esame.md` — simulazione finale (quando disponibile)
- `00-glossario.md` — verifica che tutti i termini siano chiari

**Attivita giornaliere**:

Lunedi:
- [ ] Rileggere `05-cheat-sheet.md` COMPLETO — annotare qualsiasi cosa non sia cristallina
- [ ] Ripasso flashcards (`09-flashcards.md`)
- [ ] Rifare 10 domande sbagliate dai mock precedenti

Martedi:
- [ ] **Simulazione finale**: `10-simulazioni-esame.md` oppure sezione N di `04d-practice-test.md`
- [ ] Timer: 45 minuti, condizioni d'esame reali
- [ ] Target: >85%

Mercoledi:
- [ ] Analisi errori simulazione finale
- [ ] Studio mirato SOLO sugli errori rimasti
- [ ] Rileggere la checklist pre-esame in `07-statistiche-errori.md`

Giovedi:
- [ ] Ripasso leggero: rileggere `05-cheat-sheet.md` e `07-statistiche-errori.md` checklist
- [ ] Ripasso flashcards finale
- [ ] Rileggere `00-glossario.md` — verifica che ogni termine sia chiaro
- [ ] **Niente materiale nuovo** — solo consolidamento

Venerdi (vigilia o giorno esame):
- [ ] Ripasso veloce (30 min max): `05-cheat-sheet.md` + checklist pre-esame
- [ ] Ricordare le 5 trappole principali
- [ ] Rilassarsi — il lavoro e stato fatto nelle 11 settimane precedenti
- [ ] Verificare logistica esame: orario, documento identita, requisiti tecnici (se online)

**Fine settimana: auto-valutazione**:
- [ ] Punteggio simulazione finale: ___%
- [ ] Ti senti pronto? Si/No
- [ ] Piano B se il punteggio e sotto 80%: posticipare l'esame di 1–2 settimane e ripetere le simulazioni
- Punteggio auto-valutazione (1–5): ___

---

## Regole d'oro

### 1. Ripetizione spaziata

| Quando hai studiato un concetto | Quando ripassarlo |
|--------------------------------|-------------------|
| Oggi | Domani |
| 2 giorni fa | Fra 3 giorni |
| 1 settimana fa | Fra 2 settimane |
| 1 mese fa | Fra 1 mese |

**Applicazione pratica**:
- Settimane 1–4 (teoria): alla fine di ogni settimana, ripassa la settimana precedente
- Settimane 5–9 (pratica): dedica 10–15 minuti al giorno a ripassare il dominio precedente
- Settimane 10–12 (simulazione): ripassa solo le domande sbagliate (sono gia il tuo ripasso spaziato)

### 2. Come gestire le risposte sbagliate

1. **Segna la domanda** con ❌ nel file (o in un foglio a parte)
2. **Leggi la spiegazione** sotto la domanda
3. **Verifica nella teoria** — vai al file 01/02/03 corrispondente e rileggi il paragrafo
4. **Controlla le trappole** — verifica se la domanda e segnalata in `07-statistiche-errori.md`
5. **Rifai la domanda** dopo 2–3 giorni senza guardare la risposta
6. Se sbagli di nuovo: aggiungi alla lista "Errori ricorrenti" e ripassa ogni settimana

### 3. Quando usare le flashcards (09-flashcards.md)

- **Fase teoria (sett. 1–4)**: non ancora — concentrati sulla comprensione profonda
- **Fase pratica (sett. 5–9)**: inizia a usarle dalla settimana 7, 10 minuti al giorno
- **Fase simulazione (sett. 10–12)**: 15 minuti al giorno, tutti i giorni
- **Vigilia esame**: ripasso flashcards come ultimo atto di studio

### 4. Quando fare i mock exam (10-simulazioni-esame.md)

- **MAI prima della settimana 10** — se fai le simulazioni troppo presto, sprechi domande e ti demotivi
- **Condizioni reali**: timer a 45 min, nessun materiale aperto, nessuna pausa
- **Dopo ogni simulazione**: analizza OGNI errore (non solo il punteggio)
- **Target punteggio**: >85% per sentirsi pronti (l'esame richiede ~70%)

### 5. Priorita fonti domande

| Priorita | File | Qualita | Quando usarlo |
|----------|------|---------|---------------|
| 1 | `04a-domande-curate.md` (A–D, G) | ⭐⭐⭐ Alta | Settimane 5–8, primo approccio |
| 2 | `04d-practice-test.md` (H–N) | ⭐⭐ Buona | Settimane 5–8 (pratica) + 10–12 (simulazioni) |
| 3 | `04c-domande-examtopics.md` (F) | ⭐⭐ Media | Settimane 6–9, integrazione |
| 4 | `04b-domande-ipspecialist.md` (E) | ⭐ Bassa | Settimana 9, solo con `07-statistiche-errori.md` aperto |

### 6. Strategia il giorno dell'esame

- [ ] Leggere ogni domanda **due volte** prima di rispondere
- [ ] Attenzione alle parole chiave: "always", "never", "only", "best", "most", "least"
- [ ] Se non sei sicuro: **elimina le opzioni sbagliate** e scegli tra le rimanenti
- [ ] **Non perdere troppo tempo** su una domanda — segna per revisione e vai avanti
- [ ] Usa tutto il tempo: rivedi le domande segnate alla fine
- [ ] Ricorda: le domande senza risposta sono **sbagliate** — rispondi sempre a tutto

---

## Tracker di avanzamento

### Fase Teoria (Settimane 1–4)

| Sett. | Dominio | Auto-val. (1–5) | Completato |
|-------|---------|-----------------|------------|
| 1 | D1 — Cloud Concepts | ___ | - [ ] |
| 2 | D2A — Architettura + Compute | ___ | - [ ] |
| 3 | D2B — Network + Storage + Security | ___ | - [ ] |
| 4 | D3 — Management & Governance | ___ | - [ ] |

### Fase Pratica (Settimane 5–9)

| Sett. | Focus | % corrette | Domande fatte | Completato |
|-------|-------|-----------|---------------|------------|
| 5 | Pratica D1 | ___% | ___ | - [ ] |
| 6 | Pratica D2 (2.1+2.2) | ___% | ___ | - [ ] |
| 7 | Pratica D2 (2.3+2.4) | ___% | ___ | - [ ] |
| 8 | Pratica D3 + PRENOTA ESAME | ___% | ___ | - [ ] |
| 9 | Consolidamento + IPSpecialist | ___% | ___ | - [ ] |

### Fase Simulazione (Settimane 10–12)

| Sett. | Simulazioni | Punteggi | Target | Completato |
|-------|------------|----------|--------|------------|
| 10 | S1, S2, S3 | ___%, ___%, ___% | >85% | - [ ] |
| 11 | S4, S5 | ___%, ___% | >85% | - [ ] |
| 12 | Finale | ___% | >85% | - [ ] |

### Riepilogo finale

| Metrica | Valore |
|---------|--------|
| Data prenotazione esame | ___ |
| Data esame | ___ |
| Punteggio medio simulazioni | ___% |
| Aree residue da ripassare | ___ |
| Pronto per l'esame? | Si / No |

---

> *Piano creato il 15 giugno 2026. Buono studio e in bocca al lupo per l'AZ-900!*
