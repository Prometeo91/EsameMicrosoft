# 07 — Statistiche Errori e Trappole nelle Domande

> Analisi delle **45 correzioni** (⚠️) trovate nei file 04a–04d. Queste non sono errori di studio ma **errori nelle fonti** (IPSpecialist, ExamTopics, Udemy) — conoscerli ti evita di memorizzare informazioni sbagliate.

---

## 📊 Riepilogo per tipo di errore

| Tipo di errore | Conteggio | % |
|----------------|-----------|---|
| **Risposta errata dalla fonte** | 16 | 36% |
| **Deprecazione non segnalata** | 21 | 47% |
| **Spiegazione ambigua/incompleta** | 8 | 17% |
| **Totale** | **45** | 100% |

---

## 📊 Riepilogo per dominio d'esame

| Dominio | Errori risposta | Deprecazioni | Ambiguità | Totale |
|---------|----------------|-------------|-----------|--------|
| 1 — Cloud Concepts | 2 | — | 2 | **4** |
| 2 — Architecture & Services | 8 | — | 1 | **9** |
| 3 — Management & Governance | 6 | 21 | 5 | **32** |
| **Totale** | **16** | **21** | **8** | **45** |

> ⚡ **Insight**: Il Dominio 3 concentra il **71%** degli errori — soprattutto per strumenti deprecati (TCO, Blueprints) e confusioni tra tool di governance. Studiare bene la sezione 03 del vault.

---

## 📊 Riepilogo per fonte

| Fonte | Errori | Note |
|-------|--------|------|
| **IPSpecialist (E)** | 20 | Fonte con più errori — trattare con cautela |
| **Udemy Practice Tests (H–N)** | 16 | Molte deprecazioni TCO/Blueprints |
| **Domande curate (A–D, G)** | 5 | Qualità migliore, pochi errori |
| **ExamTopics (F)** | 1 | Solo nota Blueprints |
| **Totale** | **45** | |

---

## 🔴 Risposte errate dalla fonte (16) — DA MEMORIZZARE CORRETTE

Queste domande avevano la **risposta sbagliata**. Sono le più pericolose perché potresti memorizzare l'errore.

### Identità e Accesso (3 errori)

| # | Domanda | Errore | Risposta corretta |
|---|---------|--------|-------------------|
| E369 | Quale funzionalità Entra ID concede accesso alle risorse? | ~~b) Administrative Units~~ | **a) Conditional Access** |
| E397 | Con più ruoli RBAC assegnati, quali permessi effettivi? | ~~c) Read only~~ | **a) Read and Write** — RBAC è additivo: i permessi si sommano |
| M83 | Funzionalità per usare credenziali aziendali per app cloud? | ~~Entra B2C~~ | **Entra ID (SSO)** o **B2B** — B2C è per consumatori (social login) |

### Storage e Ridondanza (2 errori)

| # | Domanda | Errore | Risposta corretta |
|---|---------|--------|-------------------|
| B19 | Si può cambiare la replica di un account storage? | ~~FALSE~~ | **TRUE** — LRS→GRS, ZRS→GZRS ecc. sono possibili |
| E35 | Azure Files supporta GZRS? | Confonde GZRS con RA-GZRS | Azure Files supporta **GZRS**, ma NON RA-GRS/RA-GZRS |

### Classificazione Servizi (2 errori)

| # | Domanda | Errore | Risposta corretta |
|---|---------|--------|-------------------|
| E244 | AKS (Kubernetes) è IaaS o PaaS? | ~~IaaS~~ | **PaaS** — Azure gestisce il control plane |
| E421 | Azure SQL Data Warehouse ha HA? | ~~False~~ | **True** — SLA 99.9%, HA integrata nella piattaforma |

### Costi e Fatturazione (3 errori)

| # | Domanda | Errore | Risposta corretta |
|---|---------|--------|-------------------|
| E55 | Azure Cost Management richiede un piano specifico? | ~~Solo EA~~ | **Tutti i piani** — Cost Management è gratuito e integrato |
| E94 | Durata massima reservation? | Include 5 anni | **Solo 1 o 3 anni** — non esiste il termine a 5 anni |
| N63 | Le reservation sono CapEx o OpEx? | ~~CapEx~~ | **OpEx** — nessun asset fisico acquistato |

### Networking (1 errore)

| # | Domanda | Errore | Risposta corretta |
|---|---------|--------|-------------------|
| K53 | VPN tra due VNet Azure? | ~~Site-to-Site~~ | **VNet-to-VNet** (o VNet Peering) — S2S è per on-prem→Azure |

### Governance e Supporto (2 errori)

| # | Domanda | Errore | Risposta corretta |
|---|---------|--------|-------------------|
| I41 | Chi fornisce raccomandazioni per ottimizzare la spesa? | ~~Cost Management~~ | **Azure Advisor** (categoria Cost) — Cost Management fornisce analisi, Advisor fornisce raccomandazioni |
| E410 | Come aumentare i limiti quota di una subscription? | ~~Service health alert~~ | **Support request** — selezionare "Service and subscription limits (quotas)" |

### Multi-risposta incompleta (3 errori)

| # | Domanda | Errore | Risposta corretta |
|---|---------|--------|-------------------|
| E300 | Come creare un policy assignment? (scegliere 3) | Solo **b** indicata | **b, c, d** — Portal/ARM, Python/REST, CLI/PowerShell |
| E309 | Chi può aprire richieste di supporto? (scegliere 3) | Solo **a** indicata | **a, b, c** — Account Admin, Service Admin, Co-Admin |
| E313 | Requisiti per Cloud Shell? (scegliere 3) | Solo **a** indicata | **a, b, c** — Resource group, storage account, file share |

---

## 🟡 Deprecazioni non segnalate (21) — SAPERE PER L'ESAME

Risposte che erano corrette al momento della stesura ma si riferiscono a strumenti deprecati/in ritiro.

### TCO Calculator — Deprecato agosto 2025 (11 occorrenze)

> **Regola**: dove la domanda cita "TCO Calculator", la risposta è ora **Pricing Calculator**.

| Domande | File |
|---------|------|
| C1 | 04a |
| E264, E346, E347 | 04b |
| I16, J86, J117, K36, K76, M15, N45 | 04d |

### Azure Blueprints — In fase di ritiro (10 occorrenze)

> **Regola**: dove la domanda cita "Blueprints", ricordare che il successore è **Template Specs + Deployment Stacks**.

| Domande | File |
|---------|------|
| C10 | 04a |
| E258, E304, E344, E401 | 04b |
| F87 | 04c |
| J65, J96, M12, N43 | 04d |

---

## 🟠 Spiegazioni ambigue/incomplete (8) — ATTENZIONE ALLE SFUMATURE

| # | Problema | Cosa ricordare |
|---|----------|---------------|
| B11 | Usa "Azure AD" (terminologia deprecata) | L'esame può usare sia "Azure AD" che **"Microsoft Entra ID"** |
| E96 | Spiegazione duplicata/non pertinente | Cross-reference con E95 |
| I56 | "Solo il subscription owner può aggiungere lock" | Anche **Owner** e **User Access Administrator** possono |
| J82 | Stessa imprecisione di I56 | Stesso concetto |
| J120 | Descrive solo il lock ReadOnly | Esistono **due** tipi: **Delete** (leggi+modifica OK, no cancella) e **ReadOnly** (solo lettura) |
| M40 | "Host app, manage OS" per PaaS | In PaaS il **provider** gestisce l'OS — tu gestisci solo app code + data |
| N42 | Stessa imprecisione di M40 | Stesso concetto |

---

## 🎯 I 5 temi più trappola (per frequenza errori)

| # | Tema | Errori totali | Tipo |
|---|------|--------------|------|
| 1 | **TCO Calculator deprecato** | 11 | Deprecazione |
| 2 | **Azure Blueprints in ritiro** | 10 | Deprecazione |
| 3 | **RBAC / Lock permissions** | 5 | Errore + ambiguità |
| 4 | **Classificazione servizi (IaaS/PaaS/SaaS)** | 4 | Errore + ambiguità |
| 5 | **Advisor vs Cost Management** | 2 | Errore |

---

## 📌 Checklist pre-esame

- [ ] **TCO Calculator** è deprecato → usa **Pricing Calculator** per tutto
- [ ] **Azure Blueprints** è in ritiro → successore: **Template Specs + Deployment Stacks**
- [ ] **RBAC è additivo** — i permessi di tutti i ruoli si sommano (allow model, mai deny)
- [ ] **Lock: Owner + User Access Admin** possono gestire i lock, non solo il subscription owner
- [ ] **Due tipi di lock**: Delete (read+modify OK) e ReadOnly (solo read)
- [ ] **AKS = PaaS**, non IaaS
- [ ] **Reservation = OpEx**, non CapEx (nessun asset fisico acquistato)
- [ ] **Conditional Access** concede/restringe accesso, non Administrative Units
- [ ] **B2C = consumatori** (social login), **B2B = partner aziendali**, **Entra ID = SSO aziendale**
- [ ] **Cost Management = analisi/budget**, **Advisor = raccomandazioni**
- [ ] **Azure Files** supporta GZRS ma NON RA-GRS/RA-GZRS
- [ ] **VNet-to-VNet** per connettere due VNet Azure, **Site-to-Site** per on-prem→Azure
