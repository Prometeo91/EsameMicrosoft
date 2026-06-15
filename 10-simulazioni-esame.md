# 10 — Simulazioni d'Esame AZ-900

> Tre simulazioni complete da 40 domande ciascuna. Domande originali che coprono tutti e tre i domini dell'esame Azure Fundamentals. Risposte e spiegazioni in fondo a ogni simulazione.

---

## Simulazione 1 — Bilanciata (copertura ampia)

**Tempo**: 45 minuti | **Domande**: 40 | **Soglia superamento**: 28/40 (70%)

> Istruzioni: rispondi senza consultare appunti. Segna le risposte, poi confronta con il solutore in fondo.

---

### Domanda 1
Nel modello di responsabilita condivisa, quale delle seguenti responsabilita spetta SEMPRE al cliente, indipendentemente dal tipo di servizio cloud (IaaS, PaaS, SaaS)?

a) Manutenzione dei server fisici
b) Patch del sistema operativo
c) Governance e classificazione dei dati
d) Gestione del middleware

### Domanda 2
Un'azienda vuole migrare gradualmente i propri sistemi legacy al cloud mantenendo alcuni server nel proprio datacenter. Quale modello cloud e piu adatto?

a) Cloud pubblico
b) Cloud privato
c) Cloud ibrido
d) Multi-cloud

### Domanda 3
Quale affermazione descrive correttamente il modello basato sul consumo del cloud computing?

a) Si paga un canone fisso mensile indipendentemente dall'utilizzo
b) Si pagano solo le risorse effettivamente consumate
c) E necessario un investimento iniziale significativo in hardware
d) I costi sono prevedibili e non variano mai

### Domanda 4
Un'azienda ha bisogno di eseguire una web application senza dover gestire il sistema operativo o il middleware. Quale tipo di servizio cloud dovrebbe scegliere?

a) IaaS
b) PaaS
c) SaaS
d) On-premises

### Domanda 5
Quale concetto descrive la capacita di un sistema cloud di aggiungere e rimuovere automaticamente risorse in base alla domanda?

a) Scalabilita
b) Tolleranza ai guasti
c) Elasticita
d) Alta disponibilita

### Domanda 6
Vero o Falso: Un cloud privato deve essere necessariamente ospitato nel datacenter dell'organizzazione che lo utilizza.

a) Vero
b) Falso

### Domanda 7
Qual e la differenza principale tra scalabilita verticale (scaling up) e scalabilita orizzontale (scaling out)?

a) Lo scaling up aggiunge piu VM identiche; lo scaling out passa a VM piu potenti
b) Lo scaling up passa a una VM piu potente; lo scaling out aggiunge piu VM identiche
c) Non c'e differenza: sono sinonimi
d) Lo scaling up e automatico; lo scaling out e manuale

### Domanda 8
Un SLA del 99,9% corrisponde approssimativamente a quale periodo di inattivita consentito all'anno?

a) 3,65 giorni
b) 8,76 ore
c) 52,6 minuti
d) 4,38 minuti

### Domanda 9
Quale servizio Azure consente di eseguire codice in risposta a eventi senza dover gestire l'infrastruttura sottostante?

a) Azure Virtual Machines
b) Azure App Service
c) Azure Functions
d) Azure Kubernetes Service

### Domanda 10
Vero o Falso: La transizione al cloud sposta la spesa da CapEx (spesa in conto capitale) a OpEx (spesa operativa).

a) Vero
b) Falso

### Domanda 11
Quale tra le seguenti e la distanza minima che separa due regioni in una coppia regionale (region pair) di Azure?

a) 50 miglia
b) 100 miglia
c) 300 miglia
d) 500 miglia

### Domanda 12
Un amministratore vuole organizzare le risorse Azure per progetto e tracciare i costi per ciascun progetto. Quale elemento della gerarchia Azure e piu adatto come contenitore logico?

a) Management Group
b) Subscription
c) Resource Group
d) Availability Zone

### Domanda 13
Quante zone di disponibilita (Availability Zones) ha come minimo una regione Azure abilitata?

a) 1
b) 2
c) 3
d) 5

### Domanda 14
Un'azienda ha bisogno di una connessione privata dedicata tra il proprio datacenter on-premises e Azure, senza transitare sulla rete Internet pubblica. Quale servizio dovrebbe usare?

a) Azure VPN Gateway
b) Azure ExpressRoute
c) Azure Front Door
d) Azure Bastion

### Domanda 15
Quale servizio di storage Azure e ottimizzato per la memorizzazione di dati non strutturati come immagini, video e backup?

a) Azure Files
b) Azure Blob Storage
c) Azure Table Storage
d) Azure Queue Storage

### Domanda 16
Vero o Falso: In Azure il peering tra VNet richiede che i range di indirizzi IP delle due reti virtuali non si sovrappongano.

a) Vero
b) Falso

### Domanda 17
Quale tier di Blob Storage richiede la reidratazione (rehydration) prima di poter accedere ai dati?

a) Hot
b) Cool
c) Cold
d) Archive

### Domanda 18
Quale opzione di ridondanza dello storage offre la massima durabilita (16 nines) con protezione sia a livello di zona che a livello geografico?

a) LRS
b) ZRS
c) GRS
d) GZRS

### Domanda 19
Quale servizio Azure fornisce la gestione delle identita e degli accessi basata su cloud, inclusi SSO e MFA?

a) Azure Key Vault
b) Microsoft Entra ID
c) Microsoft Defender for Cloud
d) Azure Policy

### Domanda 20
Quali sono i tre principi fondamentali del modello Zero Trust? (Seleziona la risposta corretta)

a) Verifica esplicita, privilegio minimo, presupponi la violazione
b) Verifica esplicita, accesso illimitato, monitora tutto
c) Autenticazione forte, firewall perimetrale, VPN obbligatoria
d) Crittografia dei dati, segmentazione della rete, backup periodici

### Domanda 21
Un Security Network Group (NSG) opera a quale livello?

a) Filtra il traffico di rete in ingresso e in uscita basandosi su regole di IP, porta e protocollo
b) Fornisce protezione DDoS avanzata
c) Gestisce la risoluzione DNS
d) Cripta il traffico tra VNet

### Domanda 22
Quale servizio di Azure permette l'accesso RDP/SSH sicuro alle VM direttamente dal portale Azure senza esporre un IP pubblico?

a) Azure VPN Gateway
b) Azure Bastion
c) Azure Firewall
d) Azure Front Door

### Domanda 23
Vero o Falso: Microsoft Entra Connect sincronizza le identita in modo bidirezionale tra Active Directory on-premises e Microsoft Entra ID.

a) Vero
b) Falso

### Domanda 24
Quale strumento Azure serve per stimare i costi delle risorse Azure prima del deployment?

a) Azure Cost Management
b) Azure Advisor
c) Calcolatore dei prezzi (Pricing Calculator)
d) Calcolatore TCO

### Domanda 25
Un'azienda vuole impedire la cancellazione accidentale di un database di produzione critico. Quale meccanismo dovrebbe utilizzare?

a) Azure Policy con effetto Deny
b) Resource Lock di tipo Delete
c) RBAC con ruolo Reader
d) Tag "DoNotDelete"

### Domanda 26
Quale effetto di Azure Policy blocca la creazione di una risorsa non conforme?

a) Audit
b) Append
c) Deny
d) Modify

### Domanda 27
Seleziona DUE affermazioni corrette riguardo ai tag in Azure:

a) I tag vengono ereditati automaticamente dal resource group alle risorse contenute
b) I tag sono coppie nome/valore usate per categorizzare le risorse
c) Azure Policy puo forzare l'applicazione di tag obbligatori
d) I tag possono essere applicati solo a livello di subscription

### Domanda 28
Quale tra i seguenti NON e una categoria di raccomandazione di Azure Advisor?

a) Affidabilita (Reliability)
b) Costo (Cost)
c) Capacita (Capacity)
d) Sicurezza (Security)

### Domanda 29
Un amministratore vuole visualizzare se un problema che colpisce una specifica VM e causato da Azure o dalla propria configurazione. Quale vista di Azure Service Health dovrebbe consultare?

a) Azure Status
b) Service Health
c) Resource Health
d) Azure Monitor

### Domanda 30
Quale linguaggio di query viene utilizzato in Azure Log Analytics?

a) SQL
b) KQL (Kusto Query Language)
c) PowerShell
d) Python

### Domanda 31
Vero o Falso: Azure Blueprints e attualmente in fase di ritiro e viene sostituito da Template Specs e Deployment Stacks.

a) Vero
b) Falso

### Domanda 32
Quale strumento Azure permette di gestire risorse che si trovano al di fuori di Azure, come server on-premises o in altri cloud?

a) Azure Resource Manager
b) Azure Arc
c) Azure Migrate
d) Azure DevOps

### Domanda 33
Quale affermazione descrive correttamente i template ARM e Bicep?

a) Sono strumenti imperativi che eseguono comandi passo dopo passo
b) Sono strumenti dichiarativi e idempotenti che eseguono il deploy attraverso ARM
c) Bicep e un linguaggio diverso che non utilizza ARM
d) I template ARM possono essere scritti solo in YAML

### Domanda 34
Un'azienda ha bisogno di trasferire 60 TB di dati ad Azure ma ha una larghezza di banda limitata. Quale servizio dovrebbe utilizzare?

a) AzCopy
b) Azure File Sync
c) Azure Data Box
d) Azure Storage Explorer

### Domanda 35
Quale piano di supporto Azure e gratuito ma NON consente di aprire ticket di supporto tecnico?

a) Developer
b) Basic
c) Standard
d) Professional Direct

### Domanda 36
Un team di sviluppo vuole eseguire container senza gestire l'infrastruttura sottostante e ha bisogno di avvio rapido per workload semplici. Quale servizio e piu adatto?

a) Azure Virtual Machines
b) Azure Container Instances (ACI)
c) Azure Kubernetes Service (AKS)
d) Azure App Service

### Domanda 37
Quale servizio Azure offre desktop virtuali e applicazioni nel cloud, integrandosi con Microsoft Entra ID?

a) Azure App Service
b) Azure Virtual Desktop (AVD)
c) Azure Bastion
d) Azure Container Apps

### Domanda 38
Quale componente di Azure Cost Management invia notifiche quando la spesa raggiunge o supera una soglia definita?

a) Cost Analysis
b) Budget Alerts
c) Azure Advisor
d) Azure Pricing Calculator

### Domanda 39
Quale tipo di lock in Azure consente la lettura e la modifica delle risorse ma impedisce la cancellazione?

a) ReadOnly
b) Delete
c) CanNotModify
d) Restricted

### Domanda 40
Seleziona DUE servizi che fanno parte del "trio serverless" di Azure:

a) Azure Virtual Machines
b) Azure Functions
c) Azure Logic Apps
d) Azure SQL Database

---

### Soluzioni Simulazione 1

| # | Risposta | Spiegazione breve |
|---|----------|-------------------|
| 1 | c | I dati (governance, classificazione, controllo accessi) sono SEMPRE responsabilita del cliente in tutti i modelli di servizio |
| 2 | c | Il cloud ibrido combina infrastruttura on-premises con servizi cloud pubblici, ideale per migrazioni graduali |
| 3 | b | Il modello basato sul consumo prevede il pagamento solo per le risorse effettivamente utilizzate (pay-as-you-go) |
| 4 | b | PaaS gestisce OS e middleware; il cliente si occupa solo del codice applicativo e dei dati |
| 5 | c | L'elasticita e la capacita di scalare automaticamente le risorse in base alla domanda |
| 6 | b | Falso — un cloud privato puo essere ospitato presso un datacenter di terze parti; cio che conta e che sia dedicato a una sola organizzazione |
| 7 | b | Scaling up = VM piu potente (verticale); scaling out = piu VM identiche (orizzontale) |
| 8 | b | 99,9% SLA equivale a circa 8,76 ore di inattivita consentite all'anno |
| 9 | c | Azure Functions e un servizio serverless event-driven che esegue codice senza gestione dell'infrastruttura |
| 10 | a | Vero — il cloud elimina l'investimento iniziale in hardware (CapEx) a favore del pagamento a consumo (OpEx) |
| 11 | c | Le region pair di Azure sono separate da almeno 300 miglia per garantire la disaster recovery |
| 12 | c | I Resource Group sono contenitori logici per organizzare risorse correlate e tracciare i costi |
| 13 | c | Una regione Azure abilitata ha come minimo 3 zone di disponibilita |
| 14 | b | ExpressRoute fornisce una connessione dedicata privata fino a 10 Gbps senza transitare su Internet |
| 15 | b | Azure Blob Storage e progettato per dati non strutturati (immagini, video, backup, log) |
| 16 | a | Vero — il peering VNet richiede range IP non sovrapposti per funzionare correttamente |
| 17 | d | Il tier Archive e offline; i dati devono essere reidratati (spostati a Hot o Cool) prima dell'accesso |
| 18 | d | GZRS combina ZRS nella regione primaria + LRS nella regione secondaria per 16 nines di durabilita |
| 19 | b | Microsoft Entra ID (ex Azure AD) e il servizio di identity and access management cloud di Microsoft |
| 20 | a | I tre principi Zero Trust sono: verifica esplicita, privilegio minimo (JIT/JEA), presupponi la violazione |
| 21 | a | Gli NSG filtrano il traffico di rete basandosi su regole di IP sorgente/destinazione, porta e protocollo |
| 22 | b | Azure Bastion fornisce accesso RDP/SSH sicuro via browser tramite TLS senza IP pubblico sulla VM |
| 23 | a | Vero — Entra Connect sincronizza bidirezionalmente le identita tra AD on-premises e Entra ID |
| 24 | c | Il Pricing Calculator stima i costi prima del deployment; il TCO Calculator e stato deprecato ad agosto 2025 |
| 25 | b | Un Resource Lock di tipo Delete consente lettura e modifica ma impedisce la cancellazione della risorsa |
| 26 | c | L'effetto Deny blocca la creazione o l'aggiornamento di risorse non conformi alla policy |
| 27 | b, c | I tag sono coppie nome/valore e Azure Policy puo forzarne l'applicazione; i tag NON vengono ereditati automaticamente |
| 28 | c | "Capacity" NON e una categoria di Advisor; le cinque sono Reliability, Security, Performance, Operational Excellence, Cost |
| 29 | c | Resource Health mostra lo stato di una singola risorsa e indica se il problema e lato Azure o lato cliente |
| 30 | b | Azure Log Analytics utilizza KQL (Kusto Query Language) per interrogare i dati raccolti da Azure Monitor |
| 31 | a | Vero — Blueprints e in fase di ritiro; il successore e Template Specs + Deployment Stacks |
| 32 | b | Azure Arc estende la gestione e la governance Azure a risorse esterne (on-premises, altri cloud) |
| 33 | b | ARM templates (JSON) e Bicep sono dichiarativi, idempotenti e deployano attraverso Azure Resource Manager |
| 34 | c | Azure Data Box e un dispositivo fisico per trasferimenti offline di grandi volumi (fino a 80 TB) |
| 35 | b | Il piano Basic e gratuito ma consente solo richieste relative a fatturazione e subscription, non ticket tecnici |
| 36 | b | ACI e il modo piu rapido e semplice per eseguire container in Azure senza gestire VM |
| 37 | b | Azure Virtual Desktop fornisce desktop e app virtuali nel cloud con integrazione Entra ID |
| 38 | b | I Budget Alerts notificano quando la spesa raggiunge o supera la soglia definita nel budget |
| 39 | b | Il lock Delete consente lettura e modifica ma blocca la cancellazione; ReadOnly consente solo la lettura |
| 40 | b, c | Il trio serverless e: Azure Functions, Azure Logic Apps e Azure Event Grid |

---

## Simulazione 2 — Trappole e concetti insidiosi

**Tempo**: 45 minuti | **Domande**: 40 | **Soglia superamento**: 28/40 (70%)

> Istruzioni: questa simulazione e focalizzata su concetti frequentemente confusi e trappole d'esame. Rispondi senza consultare appunti.

---

### Domanda 1
Un'azienda vuole stimare i costi di migrazione dall'infrastruttura on-premises ad Azure. Quale strumento dovrebbe utilizzare?

a) Azure Cost Management
b) Calcolatore TCO (TCO Calculator)
c) Calcolatore dei prezzi (Pricing Calculator)
d) Azure Advisor

### Domanda 2
Un architetto cloud suggerisce di usare Azure Blueprints per standardizzare il deploy di nuovi ambienti. Quale aggiornamento importante dovrebbe conoscere?

a) Blueprints e ora disponibile in tutte le regioni senza restrizioni
b) Blueprints e in fase di ritiro e viene sostituito da Template Specs e Deployment Stacks
c) Blueprints supporta ora il deploy multi-cloud
d) Blueprints e stato rinominato in Azure Governance Manager

### Domanda 3
Un utente ha i ruoli RBAC di Reader su una subscription e Contributor su un resource group nella stessa subscription. Quali permessi effettivi ha sul resource group?

a) Solo lettura (Reader prevale)
b) Solo Contributor (il ruolo piu specifico prevale)
c) Reader + Contributor combinati (lettura e scrittura)
d) Nessun permesso — i ruoli si annullano

### Domanda 4
Le Azure Reservations (prenotazioni) sono considerate:

a) CapEx perche comportano un impegno finanziario anticipato
b) OpEx perche non si acquista un asset fisico
c) Ne CapEx ne OpEx — sono una categoria separata
d) CapEx se a 3 anni, OpEx se a 1 anno

### Domanda 5
Azure Kubernetes Service (AKS) e classificato come:

a) IaaS perche gestisce container su VM
b) PaaS perche Azure gestisce il control plane
c) SaaS perche e un servizio completamente gestito
d) Serverless perche scala automaticamente

### Domanda 6
Vero o Falso: In Azure RBAC e possibile creare un'assegnazione di ruolo che nega esplicitamente un permesso (deny assignment).

a) Vero
b) Falso

### Domanda 7
Un resource lock di tipo ReadOnly e applicato a un account di storage. Quale operazione sara BLOCCATA?

a) Leggere i blob nell'account
b) Elencare le chiavi di accesso dell'account
c) Visualizzare le proprieta dell'account
d) Scaricare un file dall'account

### Domanda 8
Quale affermazione e corretta riguardo all'ereditarieta dei tag in Azure?

a) I tag applicati a un resource group vengono ereditati automaticamente da tutte le risorse al suo interno
b) I tag applicati a una subscription vengono ereditati dai resource group sottostanti
c) I tag NON vengono ereditati — ogni livello ha i propri tag indipendenti
d) I tag vengono ereditati solo se si usa Azure Policy

### Domanda 9
Un team vuole confrontare i costi di un'infrastruttura on-premises rispetto ad Azure per i prossimi 3 anni. Quale strumento era precedentemente usato per questo scopo e quale e ora lo strumento corretto?

a) TCO Calculator (ancora attivo) per confronti, Pricing Calculator per stime
b) TCO Calculator e stato deprecato; usare il Pricing Calculator anche per scenari di migrazione
c) Azure Advisor per confronti, Cost Management per stime
d) Cost Management per entrambi

### Domanda 10
Quale servizio fornisce raccomandazioni personalizzate per ottimizzare la spesa Azure?

a) Azure Cost Management
b) Azure Advisor (categoria Cost)
c) Azure Pricing Calculator
d) Azure Budgets

### Domanda 11
Vero o Falso: Azure RBAC applica il controllo degli accessi anche a livello di dati all'interno delle applicazioni.

a) Vero
b) Falso

### Domanda 12
Nel modello di responsabilita condivisa, chi e responsabile della sicurezza delle applicazioni in un ambiente PaaS?

a) Solo il provider cloud
b) Solo il cliente
c) Responsabilita condivisa tra provider e cliente
d) Nessuno — e automaticamente sicuro

### Domanda 13
Un amministratore applica un lock ReadOnly a un resource group. Quale affermazione e corretta?

a) Le risorse nel gruppo possono essere modificate ma non cancellate
b) Le risorse nel gruppo possono solo essere lette — nessuna modifica o cancellazione
c) Il lock si applica solo al resource group, non alle risorse al suo interno
d) Solo il proprietario della subscription puo rimuovere il lock

### Domanda 14
Seleziona DUE affermazioni corrette sui Resource Lock:

a) Anche un utente con ruolo Owner deve rimuovere il lock prima di eseguire l'azione bloccata
b) I lock vengono ereditati dalle risorse figlio
c) I lock si applicano solo alle operazioni Azure Resource Manager
d) I lock bloccano anche le operazioni interne delle risorse (es. rotazione chiavi Key Vault)

### Domanda 15
Un'azienda usa Microsoft 365 (SaaS). Nel modello di responsabilita condivisa, chi e responsabile della sicurezza dell'infrastruttura fisica?

a) Il cliente
b) Il provider cloud (Microsoft)
c) Responsabilita condivisa
d) L'ISP del cliente

### Domanda 16
Quale tra i seguenti e un vantaggio delle region pair di Azure?

a) Le risorse vengono replicate automaticamente tra le due regioni della coppia
b) Gli aggiornamenti pianificati vengono distribuiti a una regione alla volta nella coppia
c) Le due regioni della coppia condividono lo stesso datacenter
d) Le region pair garantiscono un SLA del 99,99%

### Domanda 17
Un'applicazione richiede connettivita tra due VNet Azure in regioni diverse. Quale opzione offre il percorso piu diretto?

a) VPN Site-to-Site
b) VNet Peering (globale)
c) Azure ExpressRoute
d) Azure Front Door

### Domanda 18
Quale affermazione e corretta riguardo al piano di supporto Developer di Azure?

a) Fornisce supporto tecnico 24/7 via telefono
b) Fornisce supporto tecnico solo via email durante l'orario lavorativo
c) Non consente l'apertura di ticket di supporto tecnico
d) Include un Technical Account Manager dedicato

### Domanda 19
Azure Advisor include una categoria di raccomandazione chiamata "Operational Excellence". Cosa suggerisce tipicamente?

a) Miglioramenti alla sicurezza delle risorse
b) Riduzione dei costi Azure
c) Miglioramenti ai flussi di lavoro e al deployment
d) Aumento della capacita di calcolo

### Domanda 20
Vero o Falso: Il TCO Calculator di Azure e ancora disponibile e attivo per stimare i risparmi della migrazione al cloud.

a) Vero
b) Falso

### Domanda 21
Un'azienda vuole garantire che tutte le nuove risorse create in una subscription abbiano obbligatoriamente il tag "CostCenter". Quale strumento dovrebbe usare?

a) Azure Advisor
b) Azure Policy
c) Azure Blueprints
d) Azure Resource Lock

### Domanda 22
Quale tipo di connessione VPN si utilizza per collegare un singolo dispositivo remoto a una VNet Azure?

a) Site-to-Site
b) Point-to-Site
c) VNet-to-VNet
d) ExpressRoute

### Domanda 23
La replica asincrona dello storage geo-ridondante (GRS) ha tipicamente un RPO (Recovery Point Objective) di:

a) Zero — la replica e sempre perfettamente sincronizzata
b) Meno di 15 minuti (senza SLA sulla velocita di replica)
c) Esattamente 1 ora
d) 24 ore

### Domanda 24
Quale affermazione descrive correttamente Azure Policy rispetto ad Azure RBAC?

a) Azure Policy controlla CHI puo fare COSA; RBAC controlla COME vengono configurate le risorse
b) Azure Policy controlla le proprieta delle risorse; RBAC controlla chi puo accedere alle risorse
c) Sono la stessa cosa con nomi diversi
d) Azure Policy si applica solo alle nuove risorse; RBAC si applica anche a quelle esistenti

### Domanda 25
Un amministratore vuole che Azure aggiunga automaticamente un tag mancante alle risorse esistenti non conformi. Quale effetto di Azure Policy dovrebbe usare?

a) Deny
b) Audit
c) Modify
d) Append

### Domanda 26
Vero o Falso: Azure Files supporta la ridondanza GZRS.

a) Vero
b) Falso

### Domanda 27
Quale servizio e la scelta corretta per connettere due reti virtuali Azure situate nella stessa regione?

a) VPN Site-to-Site
b) VNet Peering o VNet-to-VNet
c) Azure ExpressRoute
d) Azure Load Balancer

### Domanda 28
Un utente vuole confrontare il costo di diverse configurazioni VM Azure in diverse regioni prima di effettuare un acquisto. Quale strumento deve usare?

a) Azure Cost Management
b) Azure Advisor
c) Calcolatore dei prezzi (Pricing Calculator)
d) Azure Monitor

### Domanda 29
Nel modello di responsabilita condivisa per IaaS, chi e responsabile del patching del sistema operativo?

a) Il provider cloud
b) Il cliente
c) Responsabilita condivisa
d) Dipende dalla regione Azure

### Domanda 30
Seleziona DUE vantaggi chiave di Azure ExpressRoute rispetto a una VPN tradizionale:

a) Connessione dedicata che non transita su Internet pubblico
b) Costo sempre inferiore a una VPN
c) Velocita fino a 10 Gbps
d) Non richiede alcun provider di servizi di telecomunicazione

### Domanda 31
Un lock di tipo ReadOnly e applicato a una VM. Quale operazione e ancora possibile?

a) Ridimensionare la VM a una taglia diversa
b) Avviare o arrestare la VM
c) Visualizzare la configurazione della VM nel portale
d) Aggiungere un disco dati alla VM

### Domanda 32
Quale affermazione e corretta riguardo alla durata massima di una Azure Reservation?

a) 1, 3 o 5 anni
b) Solo 1 o 3 anni
c) Solo 3 anni
d) Da 1 a 10 anni

### Domanda 33
Un'azienda vuole usare un servizio di database gestito senza dover gestire il sistema operativo sottostante. Azure SQL Database e classificato come:

a) IaaS
b) PaaS
c) SaaS
d) Serverless puro

### Domanda 34
Vero o Falso: Le Availability Zones proteggono contro i guasti a livello di datacenter all'interno di una regione, ma NON necessariamente contro disastri regionali su larga scala.

a) Vero
b) Falso

### Domanda 35
Chi puo gestire i resource lock in Azure? Seleziona DUE risposte corrette:

a) Qualsiasi utente con ruolo Reader
b) Utenti con ruolo Owner
c) Utenti con ruolo Contributor
d) Utenti con ruolo User Access Administrator

### Domanda 36
Un amministratore nota che Azure Advisor NON segnala un avviso di budget superato. Perche?

a) Azure Advisor non include la categoria Cost
b) Gli avvisi di budget sono gestiti da Azure Cost Management, non da Advisor
c) Advisor segnala solo problemi di sicurezza
d) E necessario abilitare manualmente la funzionalita in Advisor

### Domanda 37
Quale affermazione e corretta riguardo al SLA composito?

a) Il SLA composito e sempre piu alto dei singoli SLA
b) Il SLA composito si ottiene moltiplicando i singoli SLA — piu servizi significano un SLA complessivo piu basso
c) Il SLA composito e la media dei singoli SLA
d) Il SLA composito non esiste in Azure

### Domanda 38
Un'applicazione web viene eseguita su Azure App Service e utilizza anche Azure SQL Database. Se il SLA di App Service e 99,95% e quello di SQL Database e 99,99%, qual e il SLA composito approssimativo?

a) 99,99%
b) 99,97%
c) 99,94%
d) 99,90%

### Domanda 39
Quale servizio Azure permette di eseguire servizi di dominio gestiti (domain join, LDAP, Kerberos) senza dover installare e gestire domain controller?

a) Microsoft Entra ID
b) Microsoft Entra Connect
c) Microsoft Entra Domain Services
d) Azure Arc

### Domanda 40
Vero o Falso: In Azure, uno Spot VM puo essere rimosso (evicted) da Azure in qualsiasi momento quando la capacita e necessaria per altri carichi di lavoro.

a) Vero
b) Falso

---

### Soluzioni Simulazione 2

| # | Risposta | Spiegazione breve |
|---|----------|-------------------|
| 1 | c | Il TCO Calculator e stato deprecato (agosto 2025); il Pricing Calculator e ora lo strumento per tutte le stime, inclusi gli scenari di migrazione |
| 2 | b | Azure Blueprints e in fase di ritiro; il successore e la combinazione di Template Specs + Deployment Stacks |
| 3 | c | RBAC e additivo: i permessi di tutti i ruoli assegnati si sommano (Reader + Contributor = lettura + scrittura) |
| 4 | b | Le Reservations sono OpEx perche non si acquista hardware fisico; si paga per un impegno di utilizzo del servizio cloud |
| 5 | b | AKS e PaaS perche Azure gestisce il control plane di Kubernetes; il cliente gestisce solo i container |
| 6 | b | Falso — Azure RBAC usa un modello additivo (allow only); non esistono assegnazioni di ruolo deny standard per gli utenti |
| 7 | b | Un lock ReadOnly blocca l'elenco delle chiavi perche e un'operazione di tipo POST (scrittura) che potrebbe abilitare l'accesso in scrittura |
| 8 | c | I tag NON vengono ereditati automaticamente tra i livelli della gerarchia Azure; ogni livello ha i propri tag |
| 9 | b | Il TCO Calculator e stato deprecato ad agosto 2025; il Pricing Calculator copre ora anche gli scenari di confronto on-prem vs cloud |
| 10 | b | Azure Advisor (categoria Cost) fornisce raccomandazioni personalizzate; Cost Management fornisce analisi e budget, non raccomandazioni |
| 11 | b | Falso — RBAC controlla l'accesso tramite Azure Resource Manager; NON applica il controllo a livello di dati nelle applicazioni |
| 12 | c | In PaaS la sicurezza delle applicazioni e una responsabilita condivisa tra provider (infrastruttura) e cliente (codice, configurazione) |
| 13 | b | ReadOnly consente solo la lettura; blocca sia le modifiche che le cancellazioni. Il lock viene ereditato dalle risorse nel gruppo |
| 14 | a, b | I lock richiedono la rimozione anche per gli Owner e vengono ereditati dalle risorse figlio; si applicano solo alle operazioni ARM (non interne) |
| 15 | b | In SaaS l'infrastruttura fisica e SEMPRE responsabilita del provider cloud |
| 16 | b | Gli aggiornamenti pianificati vengono distribuiti a una regione alla volta nella coppia per mantenere la disponibilita; la replica NON e automatica per tutti i servizi |
| 17 | b | VNet Peering globale connette due VNet in regioni diverse tramite il backbone Microsoft senza transitare su Internet |
| 18 | b | Il piano Developer offre supporto tecnico solo via email durante l'orario lavorativo; il supporto 24/7 inizia dal piano Standard |
| 19 | c | Operational Excellence suggerisce miglioramenti ai flussi di lavoro, alle procedure di deployment e alla gestione operativa |
| 20 | b | Falso — il TCO Calculator e stato deprecato ad agosto 2025; il Pricing Calculator e ora lo strumento di riferimento |
| 21 | b | Azure Policy puo forzare l'applicazione di tag obbligatori e auto-remediate le risorse non conformi con l'effetto Modify |
| 22 | b | Point-to-Site VPN connette un singolo dispositivo remoto a una VNet Azure (ideale per lavoratori da remoto) |
| 23 | b | La geo-replica e asincrona con un RPO tipicamente inferiore a 15 minuti, ma senza SLA sulla velocita di replica |
| 24 | b | Azure Policy controlla la conformita delle proprietà delle risorse; RBAC controlla chi puo accedere e cosa puo fare |
| 25 | c | L'effetto Modify aggiunge, aggiorna o rimuove proprieta sulle risorse esistenti (ideale per aggiungere tag mancanti) |
| 26 | a | Vero — Azure Files supporta GZRS, ma NON supporta RA-GRS o RA-GZRS |
| 27 | b | VNet Peering o VNet-to-VNet connettono due reti virtuali Azure; Site-to-Site e per connessioni on-premises verso Azure |
| 28 | c | Il Pricing Calculator consente di confrontare costi di diverse configurazioni e regioni prima del deployment |
| 29 | b | In IaaS il cliente e responsabile del sistema operativo, incluso il patching |
| 30 | a, c | ExpressRoute offre connessione dedicata (non su Internet) e velocita fino a 10 Gbps; richiede un provider di telecomunicazioni |
| 31 | c | Con ReadOnly si puo solo visualizzare la configurazione; tutte le operazioni di modifica sono bloccate |
| 32 | b | Le Azure Reservations hanno una durata di 1 o 3 anni; non esiste l'opzione a 5 anni |
| 33 | b | Azure SQL Database e PaaS: il provider gestisce OS, infrastruttura e patching; il cliente gestisce dati e query |
| 34 | a | Vero — le AZ proteggono contro guasti di datacenter nella regione, ma un disastro regionale (es. uragano) potrebbe colpire tutte le zone |
| 35 | b, d | Solo Owner e User Access Administrator (o ruoli personalizzati con permessi sui lock) possono gestire i resource lock |
| 36 | b | Gli avvisi di budget sono una funzionalita di Azure Cost Management, non di Azure Advisor; Advisor fornisce raccomandazioni, non avvisi di spesa |
| 37 | b | Il SLA composito si calcola moltiplicando i singoli SLA: piu servizi nella catena = SLA complessivo piu basso |
| 38 | c | 99,95% x 99,99% = 99,94% circa; il SLA composito e sempre inferiore al singolo SLA piu basso |
| 39 | c | Entra Domain Services fornisce domain join, LDAP, Kerberos/NTLM gestiti senza bisogno di domain controller |
| 40 | a | Vero — le Spot VM possono essere rimosse in qualsiasi momento; sono ideali solo per workload interrompibili |

---

## Simulazione 3 — Scenari complessi e applicazione pratica

**Tempo**: 45 minuti | **Domande**: 40 | **Soglia superamento**: 28/40 (70%)

> Istruzioni: questa simulazione e focalizzata su scenari realistici che richiedono l'applicazione dei concetti. Rispondi senza consultare appunti.

---

### Domanda 1
La tua azienda gestisce un portale e-commerce che registra picchi di traffico durante il Black Friday e il periodo natalizio. Durante il resto dell'anno il traffico e basso. Quale caratteristica del cloud computing e piu rilevante per gestire questa variabilita?

a) Alta disponibilita
b) Tolleranza ai guasti
c) Elasticita
d) Disaster recovery

### Domanda 2
Un'azienda farmaceutica deve mantenere tutti i dati dei pazienti su una rete dedicata e non accessibile al pubblico, ma vuole usare servizi di analisi avanzata nel cloud. Quale modello cloud dovrebbe adottare?

a) Cloud pubblico
b) Cloud privato
c) Cloud ibrido
d) Multi-cloud

### Domanda 3
Un team DevOps sta valutando quale servizio usare per eseguire microservizi containerizzati con orchestrazione completa, bilanciamento del carico e gestione del ciclo di vita dei container. Quale servizio e piu adatto?

a) Azure Container Instances (ACI)
b) Azure Container Apps
c) Azure Kubernetes Service (AKS)
d) Azure Functions

### Domanda 4
Un direttore finanziario chiede al team IT di stimare quanto costera l'infrastruttura Azure pianificata per il prossimo anno, prima di procedere all'acquisto. Lo strumento precedentemente usato per confronti on-prem vs cloud non e piu disponibile. Quale strumento deve usare?

a) Azure Cost Management
b) Calcolatore TCO (non piu disponibile)
c) Calcolatore dei prezzi (Pricing Calculator)
d) Azure Advisor

### Domanda 5
Un'azienda ha un server di database SQL che deve rimanere accessibile anche se un intero datacenter nella regione Azure diventa indisponibile. Quale strategia di deployment dovrebbe adottare?

a) Deployare il server in un Availability Set
b) Deployare il server in due Availability Zones diverse
c) Deployare il server con un disco Premium SSD
d) Usare un Resource Lock sul server

### Domanda 6
Un amministratore di sistema vuole eseguire uno script PowerShell per creare 50 VM Azure identiche. Non vuole installare nulla sul proprio computer. Quale strumento puo usare direttamente dal browser?

a) Azure CLI su un terminale locale
b) Azure Cloud Shell
c) Azure Advisor
d) Azure Resource Manager

### Domanda 7
La tua azienda ha firmato un contratto di Azure Reservation per 3 anni per delle VM. Il CFO chiede se questa spesa va classificata come CapEx o OpEx nel bilancio. Quale e la risposta corretta?

a) CapEx perche si tratta di un impegno pluriennale
b) OpEx perche non si acquista nessun asset fisico — si paga per l'uso di un servizio cloud
c) CapEx per il primo anno, poi OpEx per i successivi
d) Non classificabile perche e un modello ibrido

### Domanda 8
Un'azienda vuole che ogni nuova risorsa creata nella propria subscription Azure abbia obbligatoriamente i tag "Environment" e "Owner". Se mancano, la creazione deve essere bloccata. Quale combinazione di strumenti e piu efficace?

a) Azure Advisor + Resource Lock
b) Azure Policy con effetto Deny + definizione che richiede i tag
c) Azure Blueprints + RBAC
d) Azure Cost Management + Budget Alerts

### Domanda 9
Un'applicazione bancaria richiede che i dati siano crittografati sia a riposo che in transito. Le chiavi di crittografia devono essere gestite centralmente e protette da HSM. Quale servizio Azure dovrebbe essere usato per la gestione delle chiavi?

a) Microsoft Defender for Cloud
b) Azure Key Vault (tier Premium)
c) Azure Policy
d) Azure Information Protection

### Domanda 10
Vero o Falso: Entra Domain Services esegue una sincronizzazione bidirezionale con Microsoft Entra ID.

a) Vero
b) Falso

### Domanda 11
Un'organizzazione sanitaria ha workstation condivise tra piu operatori. Per la sicurezza delle autenticazioni, il CISO vuole adottare un metodo passwordless resistente al phishing. Quale opzione e piu adatta?

a) Password + SMS
b) Microsoft Authenticator
c) Chiavi di sicurezza FIDO2
d) Windows Hello for Business

### Domanda 12
Un team IT gestisce risorse in Azure, in AWS e in un datacenter on-premises. Vuole applicare policy di governance e monitoraggio uniformi a tutte le risorse da un unico pannello. Quale servizio Azure abilita questo scenario?

a) Azure Resource Manager
b) Azure Policy
c) Azure Arc
d) Azure Migrate

### Domanda 13
Un'azienda di media streaming vuole distribuire contenuti video ai propri utenti globali con la minima latenza possibile. Quale servizio Azure e piu indicato?

a) Azure ExpressRoute
b) Azure Front Door
c) Azure VPN Gateway
d) Azure Load Balancer

### Domanda 14
Il tuo team sta progettando una soluzione composta da Azure App Service (SLA 99,95%), Azure SQL Database (SLA 99,99%) e Azure Blob Storage (SLA 99,9%). Quale sara approssimativamente il SLA composito?

a) 99,99%
b) 99,95%
c) 99,84%
d) 99,90%

### Domanda 15
Un'azienda manifatturiera ha 200 TB di dati storici su server on-premises. La connessione Internet dell'azienda e troppo lenta per un trasferimento online in tempi ragionevoli. Quale soluzione Azure e piu adatta?

a) AzCopy con esecuzione continua
b) Azure File Sync
c) Azure Data Box Heavy
d) Azure Storage Explorer

### Domanda 16
Seleziona DUE servizi che possono essere utilizzati per automatizzare il deployment di infrastruttura Azure in modo dichiarativo e idempotente:

a) Azure CLI
b) ARM Templates (JSON)
c) Bicep
d) Azure Monitor

### Domanda 17
Un'azienda vuole consentire ai dipendenti di lavorare da remoto accedendo ai desktop aziendali dal cloud, senza installare software aggiuntivo sui dispositivi personali. Quale servizio Azure e piu adatto?

a) Azure Bastion
b) Azure Virtual Desktop (AVD)
c) Azure Container Instances
d) Azure App Service

### Domanda 18
Un nuovo dipendente viene aggiunto al team di sviluppo e deve avere gli stessi permessi degli altri membri del team su tutte le risorse del progetto. Qual e l'approccio piu efficiente con RBAC?

a) Assegnare singolarmente ogni ruolo necessario al nuovo utente
b) Aggiungere l'utente al gruppo RBAC del team di sviluppo
c) Copiare i ruoli di un altro utente manualmente
d) Dare all'utente il ruolo Owner sulla subscription

### Domanda 19
Un'azienda partner deve accedere ad alcune applicazioni interne della tua organizzazione. I dipendenti del partner devono usare le proprie credenziali aziendali. Quale funzionalita di Microsoft Entra External ID e piu adatta?

a) B2C (External ID for Customers)
b) B2B Collaboration
c) B2B Direct Connect
d) Microsoft Entra Domain Services

### Domanda 20
Un'applicazione serverless Azure Functions viene invocata raramente — circa una volta al giorno. Gli utenti segnalano che la prima richiesta del giorno e significativamente piu lenta delle successive. Qual e la spiegazione?

a) Azure Functions ha un limite giornaliero di invocazioni
b) Il fenomeno si chiama "cold start": dopo un periodo di inattivita l'ambiente deve essere reinizializzato
c) La funzione ha un bug nel codice
d) Il SLA di Azure Functions garantisce solo il 99% di disponibilita

### Domanda 21
Un amministratore deve garantire che nessuna VM venga creata al di fuori delle regioni Europa Occidentale e Europa Settentrionale. Quale strumento e piu adatto?

a) Resource Lock
b) Azure Policy con effetto Deny
c) RBAC con ruolo Reader
d) Azure Advisor

### Domanda 22
Vero o Falso: AzCopy supporta la sincronizzazione bidirezionale dei file.

a) Vero
b) Falso

### Domanda 23
Un'azienda vuole monitorare le prestazioni di un'applicazione web, inclusi i tempi di risposta delle richieste HTTP, le chiamate alle dipendenze esterne e i contatori di performance del server. Quale servizio Azure e piu indicato?

a) Azure Log Analytics
b) Azure Service Health
c) Application Insights
d) Azure Advisor

### Domanda 24
Una startup ha bisogno di eseguire calcoli di rendering 3D intensivi per brevi periodi. Il lavoro puo essere interrotto e ripreso senza problemi. Quale opzione di pricing Azure offrirebbe il massimo risparmio?

a) Pay-as-you-go
b) Reservations a 1 anno
c) Savings Plan a 3 anni
d) Spot Pricing

### Domanda 25
Il CISO della tua azienda vuole implementare un approccio di sicurezza che non si basi sulla fiducia della posizione nella rete e verifichi ogni richiesta di accesso in modo esplicito. Quale modello di sicurezza descrive questo approccio?

a) Defense in Depth
b) Zero Trust
c) Shared Responsibility
d) Perimeter-based security

### Domanda 26
Un team deve deployare la stessa infrastruttura Azure in tre ambienti diversi (sviluppo, test, produzione) garantendo consistenza tra gli ambienti. Quale approccio e piu appropriato?

a) Creare manualmente le risorse nel portale Azure per ogni ambiente
b) Usare ARM Templates o Bicep per un deploy dichiarativo e ripetibile
c) Usare Azure Advisor per replicare la configurazione
d) Usare Azure Monitor per copiare le risorse

### Domanda 27
Quale dei seguenti strati del modello Defense in Depth rappresenta l'obiettivo finale dell'attaccante?

a) Rete
b) Compute
c) Identita e accesso
d) Dati

### Domanda 28
Un'azienda ha una policy Azure che limita la creazione di risorse alla sola regione "West Europe", applicata a livello di Management Group. Un subscription owner prova a creare una VM nella regione "East US". Cosa succede?

a) La VM viene creata perche il subscription owner ha permessi sufficienti
b) La VM viene creata ma contrassegnata come non conforme
c) La creazione viene bloccata dalla policy (effetto Deny)
d) La policy viene automaticamente sovrascritta

### Domanda 29
Vero o Falso: Quando si arresta una VM dall'interno del sistema operativo guest (shutdown dal SO), la VM viene deallocata e la fatturazione si interrompe completamente.

a) Vero
b) Falso

### Domanda 30
Un'applicazione richiede storage con la massima velocita e la minima latenza per transazioni frequenti su piccoli oggetti. Quale tipo di account storage e piu adatto?

a) Standard general-purpose v2
b) Premium block blobs
c) Premium file shares
d) Premium page blobs

### Domanda 31
Un'azienda vuole che le sue applicazioni cloud accedano a segreti (password, chiavi API) senza doverli codificare nel codice sorgente. Quale combinazione di servizi e consigliata?

a) Azure Key Vault + Managed Identities
b) Azure Policy + Resource Lock
c) Azure Advisor + Azure Monitor
d) Entra ID + RBAC

### Domanda 32
Quale categoria di servizi Azure e piu adatta per un'azienda che vuole usare API precostruite per aggiungere funzionalita di riconoscimento vocale e visione artificiale alle proprie applicazioni?

a) Azure Machine Learning
b) Azure AI Services
c) Azure IoT Hub
d) Azure DevOps

### Domanda 33
Un'organizzazione ha 10 subscription Azure gestite da team diversi. Il CISO vuole applicare una baseline di sicurezza comune a tutte le subscription. Quale elemento della gerarchia Azure permette di farlo in modo centralizzato?

a) Resource Group
b) Subscription
c) Management Group
d) Azure Policy (senza Management Group)

### Domanda 34
Un architetto cloud deve scegliere tra LRS e ZRS per un account di storage che ospita dati critici. L'azienda vuole protezione contro guasti di un singolo datacenter all'interno della regione. Quale opzione e corretta?

a) LRS — replica in 3 copie in un singolo datacenter; non protegge da guasti del datacenter
b) ZRS — replica in 3 copie distribuite su 3 Availability Zones; protegge da guasti di un singolo datacenter
c) Entrambe offrono lo stesso livello di protezione
d) LRS offre piu copie di ZRS

### Domanda 35
Seleziona DUE affermazioni corrette riguardo ad Azure Cloud Shell:

a) Richiede l'installazione di software sul computer locale
b) E autenticato automaticamente con le credenziali Azure dell'utente
c) Supporta sia Azure PowerShell che Azure CLI (Bash)
d) Non richiede alcuna risorsa Azure per funzionare

### Domanda 36
Un'azienda SaaS vuole permettere ai consumatori finali della propria app di registrarsi e autenticarsi usando account social (Google, Facebook). Quale funzionalita Microsoft Entra External ID e adatta?

a) B2B Collaboration
b) B2B Direct Connect
c) External ID for Customers (ex Azure AD B2C)
d) Microsoft Entra Connect

### Domanda 37
Un responsabile IT vuole ricevere una notifica proattiva quando un servizio Azure che la sua azienda utilizza ha un'interruzione pianificata per manutenzione. Quale vista di Service Health dovrebbe configurare?

a) Azure Status
b) Service Health (con alert configurati)
c) Resource Health
d) Azure Monitor Alerts

### Domanda 38
Vero o Falso: Un resource group in Azure puo contenere risorse distribuite in piu regioni Azure diverse.

a) Vero
b) Falso

### Domanda 39
Un'azienda ha un'applicazione che elabora ordini. Quando arriva un nuovo ordine, un messaggio viene inserito in una coda e un processo in background lo elabora in modo asincrono. Quale coppia di servizi Azure e piu adatta?

a) Azure Blob Storage + Azure Functions
b) Azure Queue Storage + Azure Functions
c) Azure Files + Azure Logic Apps
d) Azure Table Storage + Azure App Service

### Domanda 40
Un team ha bisogno di un hub centralizzato per valutare, pianificare e gestire la migrazione di server, database e applicazioni web dall'infrastruttura on-premises ad Azure. Quale servizio Azure e specificamente progettato per questo scopo?

a) Azure Arc
b) Azure Migrate
c) Azure DevOps
d) Azure Data Box

---

### Soluzioni Simulazione 3

| # | Risposta | Spiegazione breve |
|---|----------|-------------------|
| 1 | c | L'elasticita permette di scalare automaticamente le risorse durante i picchi e ridurle nei periodi di bassa domanda |
| 2 | c | Il cloud ibrido consente di mantenere dati sensibili on-premises e usare il cloud pubblico per analisi avanzata |
| 3 | c | AKS fornisce orchestrazione Kubernetes completa con gestione del ciclo di vita dei container a livello enterprise |
| 4 | c | Il TCO Calculator e stato deprecato; il Pricing Calculator e ora lo strumento unico per tutte le stime di costo Azure |
| 5 | b | Le Availability Zones distribuiscono le risorse in datacenter separati nella stessa regione, offrendo un SLA del 99,99% |
| 6 | b | Azure Cloud Shell e accessibile dal browser, e preautenticato e non richiede installazione locale |
| 7 | b | Le Reservations sono OpEx: non si acquista hardware fisico, si paga per un impegno di utilizzo di servizi cloud |
| 8 | b | Azure Policy con effetto Deny blocca la creazione di risorse che non hanno i tag obbligatori definiti nella policy |
| 9 | b | Azure Key Vault (tier Premium) offre gestione centralizzata di chiavi protette da HSM, segreti e certificati |
| 10 | b | Falso — la sincronizzazione da Entra ID a Entra Domain Services e unidirezionale (one-way down) |
| 11 | c | Le chiavi FIDO2 sono l'opzione passwordless ideale per workstation condivise: sono resistenti al phishing e non richiedono un dispositivo personale |
| 12 | c | Azure Arc estende la governance e il monitoraggio Azure a risorse on-premises e in altri cloud da un unico pannello |
| 13 | b | Azure Front Door combina CDN globale, bilanciamento del carico e WAF per la distribuzione ottimale di contenuti |
| 14 | c | SLA composito: 99,95% x 99,99% x 99,9% = circa 99,84%; piu servizi nella catena riducono il SLA complessivo |
| 15 | c | Data Box Heavy supporta fino a circa 770 TB per trasferimenti fisici offline quando la rete e insufficiente |
| 16 | b, c | ARM Templates (JSON) e Bicep sono entrambi strumenti dichiarativi e idempotenti che deployano tramite ARM |
| 17 | b | Azure Virtual Desktop fornisce desktop e app dal cloud accessibili via browser senza software aggiuntivo |
| 18 | b | Aggiungere l'utente al gruppo RBAC del team garantisce automaticamente gli stessi permessi degli altri membri |
| 19 | b | B2B Collaboration consente ai partner di accedere alle app interne usando le proprie credenziali aziendali come utenti guest |
| 20 | b | Il cold start e un comportamento noto delle Functions serverless: dopo l'inattivita l'ambiente viene sospeso e la prima richiesta richiede piu tempo |
| 21 | b | Azure Policy con effetto Deny impedisce la creazione di risorse in regioni non consentite |
| 22 | b | Falso — AzCopy supporta solo la sincronizzazione unidirezionale; per la sincronizzazione bidirezionale si usa Azure File Sync |
| 23 | c | Application Insights monitora prestazioni web (richieste, dipendenze, tempi di risposta, contatori server) |
| 24 | d | Spot Pricing offre fino al 90% di risparmio per workload interrompibili e riprendibili |
| 25 | b | Zero Trust non si basa sulla posizione nella rete; verifica ogni richiesta esplicitamente e assume la possibilita di violazione |
| 26 | b | ARM Templates e Bicep garantiscono deploy dichiarativi, idempotenti e ripetibili in tutti gli ambienti |
| 27 | d | I dati sono lo strato piu interno e l'obiettivo finale di un attaccante nel modello Defense in Depth |
| 28 | c | Le policy Azure con effetto Deny vengono ereditate dal Management Group e non possono essere sovrascritte da livelli inferiori |
| 29 | b | Falso — lo shutdown dal SO guest NON dealloca la VM; bisogna usare il pulsante Stop nel portale Azure per fermare la fatturazione |
| 30 | b | Premium block blobs e ottimizzato per transazioni frequenti su piccoli oggetti con latenza minima |
| 31 | a | Key Vault archivia segreti centralmente; le Managed Identities vi accedono a runtime senza credenziali nel codice |
| 32 | b | Azure AI Services offre API precostruite per visione, linguaggio, voce e decisione senza dover addestrare modelli personalizzati |
| 33 | c | I Management Group consentono di applicare policy e RBAC a piu subscription simultaneamente in modo centralizzato |
| 34 | b | ZRS replica su 3 Availability Zones diverse proteggendo da guasti di un singolo datacenter; LRS replica nello stesso datacenter |
| 35 | b, c | Cloud Shell e preautenticato e supporta sia PowerShell che CLI (Bash); richiede un account storage per la persistenza dei file |
| 36 | c | External ID for Customers (ex B2C) consente la registrazione con account social per le app rivolte ai consumatori |
| 37 | b | Service Health mostra interruzioni e manutenzioni pianificate per i servizi e le regioni che l'azienda effettivamente utilizza, con alert configurabili |
| 38 | a | Vero — un resource group puo contenere risorse in regioni diverse; la posizione del gruppo e solo per i metadati |
| 39 | b | Azure Queue Storage gestisce i messaggi asincroni; Azure Functions si attiva con un trigger sulla coda per l'elaborazione |
| 40 | b | Azure Migrate e l'hub centralizzato per discovery, assessment e migrazione di server, database e web app verso Azure |
