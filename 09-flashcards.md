# 09 — Flashcard per l'esame AZ-900

> **~150 flashcard** organizzate per dominio d'esame. Coprono definizioni, casi d'uso, confronti e trappole comuni.

---

## Come usare questo file

1. **Auto-test**: copri la risposta (**R:**), leggi la domanda (**D:**), formula la tua risposta mentalmente, poi scopri e confronta.
2. **Ripasso mirato**: concentrati sulle card che sbagli e ripassale più spesso (spacing repetition).
3. **Sessioni brevi**: 20–30 card alla volta, più volte al giorno, sono più efficaci di una maratona unica.

## Importazione in Anki

Questo file può essere convertito in formato Anki estraendo le coppie D/R:

- **Front** = testo dopo `**D:**`
- **Back** = testo dopo `**R:**`
- Separatore: tabulazione (TAB)
- Formato file: testo semplice UTF-8, estensione `.txt`

Esempio di riga per Anki:
```
Che cos'è il cloud computing?	Utilizzo di risorse informatiche gestite da un provider cloud, accessibili via internet con modello pay-as-you-go.
```

Puoi usare uno script o regex per estrarre automaticamente le coppie da questo file Markdown.

---

## Dominio 1 — Cloud Concepts (25–30% dell'esame)

### Concetti fondamentali del cloud

#### Card 1
**D:** Che cos'è il cloud computing?
**R:** Utilizzo di risorse informatiche (server, storage, networking) gestite da un cloud provider, accessibili via internet con modello pay-as-you-go. Il provider si assume parte della responsabilità dell'infrastruttura.

#### Card 2
**D:** Che cos'è il modello a consumo (consumption-based model)?
**R:** Modello di pricing in cui paghi solo per le risorse effettivamente utilizzate. Elimina le spese iniziali elevate e sposta la spesa da CapEx a OpEx.

#### Card 3
**D:** Qual è la differenza tra CapEx e OpEx?
**R:** **CapEx** = spesa anticipata per infrastruttura fisica (associata all'on-premises). **OpEx** = spesa pay-as-you-go per servizi (associata al cloud). Il cloud sposta la spesa da CapEx a OpEx.

#### Card 4
**D:** Che cosa sono le economie di scala nel cloud?
**R:** I provider cloud operano su scala massiva, migliorando l'utilizzo delle risorse e abbassando il costo unitario. Questi risparmi vengono trasferiti ai clienti sotto forma di prezzi più bassi.

#### Card 5
**D:** Qual è la definizione NIST del cloud computing?
**R:** Modello per abilitare accesso on-demand via rete a un pool condiviso di risorse configurabili (reti, server, storage, app) che possono essere rapidamente provisionate e rilasciate con minimo sforzo di gestione.

### Modelli cloud

#### Card 6
**D:** Quali sono i tre modelli di cloud deployment?
**R:** **Public cloud** (multi-tenant, infrastruttura condivisa), **Private cloud** (single-tenant, dedicato a un'organizzazione), **Hybrid cloud** (combinazione di public e private cloud).

#### Card 7
**D:** Quali sono le caratteristiche principali del cloud pubblico?
**R:** Multi-tenant, adozione rapida, pay-as-you-go, il provider gestisce parte dell'infrastruttura. Meno controllo ma massima flessibilità di provisioning.

#### Card 8
**D:** Un private cloud deve essere per forza on-premises?
**R:** **No.** Un private cloud può essere ospitato in un datacenter di terze parti. Ciò che lo definisce è che l'infrastruttura è dedicata a una singola organizzazione (single-tenant), non la posizione fisica.

#### Card 9
**D:** Un hybrid cloud include sempre risorse on-premises?
**R:** **No.** Un hybrid cloud può combinare un datacenter di terze parti (private cloud) con un public cloud. Non è necessario che includa hardware on-premises di proprietà.

#### Card 10
**D:** Che cos'è Azure Stack?
**R:** Un pacchetto hardware + software validato che permette di eseguire servizi Azure on-premises, facilitando l'adozione del cloud ibrido. Tu gestisci l'hardware, il software esegue servizi Azure.

### Shared Responsibility Model

#### Card 11
**D:** Che cos'è il modello di responsabilità condivisa?
**R:** La responsabilità nel cloud è sempre condivisa tra te e il provider. Quanto si sposta dipende dal tipo di servizio (IaaS/PaaS/SaaS). Non è mai 100% tua né 100% del provider.

#### Card 12
**D:** Nel modello di responsabilità condivisa, cosa è SEMPRE responsabilità del cliente?
**R:** **Dati**, **identità e account**, **dispositivi** autorizzati a connettersi. Questi restano tuoi indipendentemente dal tipo di servizio.

#### Card 13
**D:** Nel modello di responsabilità condivisa, cosa è SEMPRE responsabilità del provider?
**R:** **Datacenter fisico**, **rete fisica**, **host fisici**. Il provider gestisce sempre l'infrastruttura fisica sottostante.

### IaaS, PaaS, SaaS

#### Card 14
**D:** Che cos'è IaaS? Fai un esempio Azure.
**R:** Infrastructure-as-a-Service: il provider fornisce l'hardware, tu gestisci OS, middleware e applicazioni. Massimo controllo, massima responsabilità. Esempio: **Azure Virtual Machines**.

#### Card 15
**D:** Che cos'è PaaS? Fai un esempio Azure.
**R:** Platform-as-a-Service: il provider gestisce infrastruttura + OS + middleware; tu gestisci solo il codice applicativo e i dati. Esempio: **Azure App Service**, **Azure SQL Database**.

#### Card 16
**D:** Che cos'è SaaS? Fai un esempio.
**R:** Software-as-a-Service: il provider gestisce tutto; tu usi l'applicazione. Meno controllo, meno responsabilità. Gestisci solo dati + identità. Esempio: **Microsoft 365**, **Outlook**.

#### Card 17
**D:** Quale tipo di servizio è associato al "lift-and-shift"?
**R:** **IaaS**. Il lift-and-shift consiste nel migrare un'applicazione al cloud con modifiche minime, creando risorse cloud simili a quelle on-premises.

#### Card 18
**D:** In quale modello di servizio il piano di hosting viene fatturato anche senza app in esecuzione?
**R:** **PaaS** (es. Azure App Service). Il piano viene fatturato indipendentemente dalle app. Per fermare i costi, bisogna eliminare il piano.

#### Card 19
**D:** Come si classifica AKS (Azure Kubernetes Service): IaaS o PaaS?
**R:** **PaaS**. Azure gestisce il control plane di Kubernetes; tu distribuisci i container. È una trappola d'esame frequente: molti pensano sia IaaS.

### Serverless e Concetti Avanzati

#### Card 20
**D:** Cosa significa "serverless"?
**R:** Non significa "senza server", ma che **tu non gestisci i server**. Pricing basato sul consumo (zero utilizzo = zero costo), auto-scaling automatico. Svantaggio: **cold start** dopo periodi di inattività.

#### Card 21
**D:** Quali sono i tre servizi serverless principali di Azure?
**R:** **Azure Functions** (esecuzione codice event-driven), **Azure Logic Apps** (automazione workflow con connettori), **Azure Event Grid** (routing eventi pub/sub).

### Benefici del cloud

#### Card 22
**D:** Che cos'è l'Alta Disponibilità (High Availability) nel cloud?
**R:** La capacità di mantenere i servizi accessibili per lunghi periodi. I provider offrono SLA con garanzie di uptime (es. 99.9% = max 8.76 ore di downtime/anno).

#### Card 23
**D:** Che cos'è la scalabilità nel cloud?
**R:** La capacità del sistema di aggiungere o rimuovere risorse per soddisfare la domanda. **Verticale** (scale up/down) = VM più potente. **Orizzontale** (scale out/in) = più VM.

#### Card 24
**D:** Qual è la differenza tra scalabilità ed elasticità?
**R:** **Scalabilità** = il sistema PUÒ aggiungere/rimuovere risorse (capacità). **Elasticità** = il sistema aggiunge/rimuove risorse AUTOMATICAMENTE in base alla domanda (automazione). L'elasticità richiede la scalabilità.

#### Card 25
**D:** Che cos'è la fault tolerance?
**R:** Lo spostamento automatico da risorse non sane a risorse sane senza intervento dell'utente. Gestisce guasti a livello di componente. NON confondere con la scalabilità (che assume VM tutte sane).

#### Card 26
**D:** Che cos'è la reliability nel cloud?
**R:** La capacità di recuperare da guasti e continuare a funzionare. Combina **resiliency** (tornare operativi dopo un guasto) e **availability** (accesso costante nel tempo). È un pilastro del Well-Architected Framework di Azure.

#### Card 27
**D:** Quali sono le due dimensioni della predictability nel cloud?
**R:** **Performance** (autoscaling, load balancing, HA garantiscono un'esperienza utente prevedibile) e **Costi** (monitoraggio in tempo reale, analytics, Pricing Calculator permettono previsioni di spesa).

#### Card 28
**D:** Quali sono i valori SLA da ricordare per l'esame?
**R:** **99%** = 3.65 giorni/anno di downtime. **99.9%** = 8.76 ore/anno. **99.99%** = 52.6 minuti/anno. Più alto lo SLA, meno downtime ma potenzialmente più costo.

#### Card 29
**D:** Che cos'è un SLA composito?
**R:** Lo SLA effettivo quando un'applicazione dipende da più servizi Azure. Si calcola moltiplicando gli SLA individuali: es. 99.95% × 99.99% = 99.94%. Più servizi = SLA composito più basso.

#### Card 30
**D:** Qual è la differenza tra gestibilità DEL cloud e gestibilità NEL cloud?
**R:** **Del cloud** (COSA puoi fare) = auto-scaling, deploy da template, monitoraggio, alert automatici. **Nel cloud** (COME lo fai) = portale Azure, CLI, API, PowerShell.

#### Card 31
**D:** Cos'è la cloud agility?
**R:** La velocità e facilità con cui le risorse cloud possono essere provisionate o scalate (secondi vs ore rispetto all'on-premises).

#### Card 32
**D:** Qual è il ciclo di sostenibilità nel cloud?
**R:** **Right-size** (dimensionare correttamente) → **Automate** (scalare automaticamente) → **Optimize** (scegliere configurazioni efficienti) → **Monitor** (tracciare utilizzo e spesa).

#### Card 33
**D:** Quali sono i tre strati concentrici di governance-compliance-security nel cloud?
**R:** **Governance** (strato esterno: template per standard) → **Compliance** (strato medio: audit e segnalazione risorse non conformi) → **Security** (strato interno: DDoS, patch, controlli).

#### Card 34
**D:** Quali sono i cinque pilastri del Well-Architected Framework di Azure?
**R:** **Reliability**, **Security**, **Cost Optimization**, **Operational Excellence**, **Performance Efficiency**. La Reliability combina resiliency e availability.

#### Card 35
**D:** Che cos'è il BCDR (Business Continuity and Disaster Recovery)?
**R:** Pianificazione per backup dei dati e replica delle applicazioni in regioni non colpite da disastri, per proteggere contro guasti regionali su larga scala.

---

## Dominio 2 — Azure Architecture & Services (35–40% dell'esame)

### Architettura Azure: regioni e zone

#### Card 36
**D:** Che cos'è una Region di Azure?
**R:** Un insieme di datacenter in un'area geografica specifica, collegati da una rete dedicata a bassa latenza.

#### Card 37
**D:** Che cos'è una Regional Pair?
**R:** Due regioni nella stessa geografia, distanti almeno **300 miglia**, aggiornate sequenzialmente da Microsoft. Vantaggi: ripristino prioritario, aggiornamenti sfalsati, residenza dati nella stessa geografia.

#### Card 38
**D:** Che cos'è una Availability Zone?
**R:** Un datacenter fisicamente separato all'interno di una regione Azure, con alimentazione, raffreddamento e rete indipendenti. Minimo **3 zone** per regione abilitata. SLA **99.99%** per VM su 2+ zone.

#### Card 39
**D:** Qual è la differenza tra Availability Set e Availability Zone?
**R:** **Availability Set** = VM in rack diversi nello STESSO datacenter → SLA **99.95%**. **Availability Zone** = VM in datacenter DIVERSI nella stessa regione → SLA **99.99%**. Le zone offrono isolamento più ampio.

#### Card 40
**D:** Cosa sono i Fault Domain e gli Update Domain?
**R:** **Fault domain** (default: 2) = rack diversi che proteggono da guasti hardware. **Update domain** (default: 5) = gruppi riavviati separatamente durante la manutenzione pianificata (30 min di attesa tra uno e l'altro).

#### Card 41
**D:** Che cosa sono le Sovereign Region?
**R:** Cloud Azure isolati per requisiti di conformità specifici: **Azure Government** (agenzie USA), **Azure China 21Vianet** (normative cinesi), **Azure Germany** (residenza dati EU tramite data trustee).

#### Card 42
**D:** Quali sono le tre categorie di servizi zone-aware?
**R:** **Zonal** (tu scegli la zona: VM, dischi, IP). **Zone-redundant** (replica automatica: ZRS, SQL Database). **Non-regional** (sempre disponibili, resilienti a zone E regioni: Entra ID, Traffic Manager, Azure DNS).

### Gerarchia risorse

#### Card 43
**D:** Qual è la gerarchia delle risorse Azure dall'alto in basso?
**R:** **Management Group** → **Subscription** → **Resource Group** → **Resource**. Le policy e RBAC applicati a un livello superiore vengono ereditati verso il basso.

#### Card 44
**D:** Che cos'è un Resource Group?
**R:** Contenitore logico per organizzare risorse Azure correlate. Una risorsa può appartenere a un solo gruppo. No nesting, no rename. Eliminare il gruppo = eliminare TUTTE le risorse al suo interno.

#### Card 45
**D:** Un Resource Group è un confine di sicurezza di rete?
**R:** **No.** I resource group controllano gestione e permessi, non l'isolamento di rete. Qualsiasi risorsa può accedere a risorse in un altro gruppo (a meno che non ci siano NSG, private endpoint o altri meccanismi).

#### Card 46
**D:** Che cos'è una Subscription di Azure?
**R:** Unità di fatturazione e controllo accessi con un ID univoco. Due tipi di confine: **billing** (fatture separate) e **access control** (policy di accesso separate). Un account può avere più subscription.

#### Card 47
**D:** Che cosa sono i Management Group?
**R:** Contenitori per organizzare subscription. Policy e RBAC a livello di MG vengono ereditati da tutte le subscription figlie. Max **10.000 gruppi**, max **6 livelli** di profondità (escluso root e subscription).

#### Card 48
**D:** Che cos'è Azure Resource Manager (ARM)?
**R:** Il livello di gestione che autentica, autorizza e instrada tutte le richieste Azure, sia dal portale che da CLI/PowerShell/API/SDK. Sei vantaggi: template dichiarativi, gestione a gruppo, re-deploy consistente, ordinamento dipendenze, RBAC nativo, tagging.

### Compute

#### Card 49
**D:** Quale servizio Azure per eseguire container in modo semplice e veloce senza gestire VM?
**R:** **Azure Container Instances (ACI)** — il modo più semplice e rapido per eseguire container in Azure. PaaS, pay per use, ideale per workload semplici e di breve durata.

#### Card 50
**D:** Qual è lo spettro dei servizi container in Azure?
**R:** **ACI** (semplice, start veloce) → **Container Apps** (elastic, load balancing integrato) → **AKS** (orchestrazione Kubernetes completa, enterprise-scale).

#### Card 51
**D:** Che cos'è Azure Functions?
**R:** Compute serverless event-driven. Paghi solo per il tempo di esecuzione CPU. Trigger: HTTP, Timer, Queue. **Stateless** di default; **Durable Functions** aggiungono stato. Attenzione al **cold start** dopo inattività.

#### Card 52
**D:** Che cos'è un VM Scale Set (VMSS)?
**R:** Servizio per distribuire e auto-scalare fino a **1.000 VM identiche** con load balancing integrato. Supporta la distribuzione tra availability zone.

#### Card 53
**D:** Qual è la scala SLA per le VM Azure?
**R:** Standard HDD: **95%** → Standard SSD: **99.5%** → Premium SSD: **99.9%** → Availability Set: **99.95%** → Availability Zones: **99.99%**. Ogni step aumenta SLA e costo.

#### Card 54
**D:** Che cos'è Azure App Service?
**R:** PaaS HTTP-based per hosting di web app, REST API e back-end mobili. Supporta .NET, Java, Node.js, PHP, Python su Windows/Linux. Auto-scaling e load balancing integrati. Il piano si paga anche senza app in esecuzione.

#### Card 55
**D:** Che cos'è Azure Virtual Desktop (AVD)?
**R:** Servizio PaaS di virtualizzazione desktop e app. Gli utenti accedono da remoto a desktop e applicazioni Windows nel cloud. Supporta sessione singola e multi-sessione. Si integra con Microsoft Entra ID.

#### Card 56
**D:** Come si ferma la fatturazione di una VM?
**R:** **Deallocare** la VM dal portale (pulsante Stop). Attenzione: spegnere dal guest OS NON dealloca e continui a pagare disco e risorse.

#### Card 57
**D:** Che cos'è il cold start nel serverless?
**R:** Dopo un periodo di inattività, le risorse serverless sono in pausa. La prima richiesta richiede secondi aggiuntivi per l'avvio dell'ambiente. È un trade-off noto del serverless.

### Networking

#### Card 58
**D:** Che cos'è un VNet (Virtual Network)?
**R:** Rete virtuale Azure che permette la comunicazione tra risorse Azure, internet e reti on-premises. Supporta isolamento, segmentazione (subnet) e connettività (peering, VPN, ExpressRoute).

#### Card 59
**D:** Che cos'è il VNet Peering?
**R:** Connessione tra due VNet attraverso il backbone Microsoft. Il traffico è privato, non transita mai su internet pubblico. Funziona anche tra regioni diverse (global peering). Richiede range IP **non sovrapposti**.

#### Card 60
**D:** Qual è la differenza tra VPN Gateway e ExpressRoute?
**R:** **VPN Gateway** = tunnel crittografato IPSec/IKE su internet pubblico. **ExpressRoute** = connessione privata dedicata in fibra ottica (fino a 10 Gbps) che NON transita su internet. ExpressRoute è più veloce e affidabile.

#### Card 61
**D:** Quali sono i tre tipi di connessione VPN Gateway?
**R:** **Point-to-site** (dispositivo remoto → VNet: lavoratori remoti). **Site-to-site** (rete on-prem → VNet: uffici/datacenter). **Network-to-network** (VNet A → VNet B: connettività cross-region).

#### Card 62
**D:** Che cos'è un NSG (Network Security Group)?
**R:** Regole firewall per consentire/negare traffico verso risorse Azure in base a IP, porta e protocollo. Le regole sono valutate per priorità: **first match wins**. L'azione di default se nessuna regola corrisponde: **deny**.

#### Card 63
**D:** Qual è la differenza tra Private Endpoint e Service Endpoint?
**R:** **Private Endpoint** = IP privato nel tuo VNet, connesso a una risorsa specifica via Azure Private Link, non accessibile da internet. **Service Endpoint** = accesso a tutte le istanze di un servizio PaaS, comunque accessibile da internet.

#### Card 64
**D:** Che cos'è Azure Bastion?
**R:** Servizio PaaS gestito per accesso RDP/SSH sicuro alle VM direttamente dal portale Azure via TLS, senza esporre un IP pubblico sulla VM. Elimina la necessità di un jump box.

#### Card 65
**D:** Qual è la differenza tra DDoS Protection Basic e Standard?
**R:** **Basic** = gratuito, automatico, protegge da attacchi comuni di rete. **Standard** = a pagamento, mitiga 60+ tipi di attacchi, include team DDoS Rapid Response e garanzia di costo (credito di servizio).

#### Card 66
**D:** Che cos'è Azure Firewall?
**R:** Firewall di rete cloud-native, stateful, per proteggere le risorse VNet di Azure. Filtra il traffico tra più VNet e subscription in modo centralizzato.

#### Card 67
**D:** Che cos'è Azure Front Door?
**R:** CDN moderna che combina Content Delivery Network, bilanciamento del carico globale e WAF (Web Application Firewall) in un unico servizio, usando la rete edge globale di Microsoft.

#### Card 68
**D:** Che cos'è Azure DNS?
**R:** Servizio per ospitare e gestire record DNS (zone pubbliche e private) in Azure. Supporta Alias Record. Attenzione: Azure DNS **NON può acquistare nomi di dominio** (non è un registrar).

#### Card 69
**D:** Che cos'è ExpressRoute Global Reach?
**R:** Funzionalità che collega le tue sedi on-premises tra di loro attraverso i circuiti ExpressRoute via il backbone Microsoft — percorso privato sito-a-sito senza internet pubblico.

#### Card 70
**D:** Quale tipo di connessione usi per collegare due VNet Azure?
**R:** **VNet-to-VNet** (o VNet Peering). La connessione **Site-to-Site** è per on-prem→Azure. È una trappola d'esame comune.

### Storage

#### Card 71
**D:** Che cos'è un account di archiviazione Azure (Storage Account)?
**R:** Fornisce un namespace univoco (3–24 caratteri, minuscolo + numeri, globalmente unico) per i dati Azure Storage, accessibile via HTTP/HTTPS. Contiene uno o più servizi di storage protetti da un'opzione di ridondanza.

#### Card 72
**D:** Quali sono le opzioni di ridondanza storage e la loro durabilità?
**R:** **LRS** = 3 copie, 1 datacenter → 11 nines. **ZRS** = 3 copie, 3 zone → 12 nines. **GRS/GZRS** = 6 copie (3 primarie + 3 secondarie) → 16 nines. RA-GRS/RA-GZRS aggiungono lettura dalla regione secondaria.

#### Card 73
**D:** Qual è la differenza tra GRS e RA-GRS?
**R:** **GRS** replica i dati nella regione secondaria ma i dati NON sono leggibili finché non avviene il failover. **RA-GRS** (Read-Access) permette la lettura dalla regione secondaria anche PRIMA del failover. URL con suffisso `-secondary`.

#### Card 74
**D:** Azure Files supporta GZRS?
**R:** **Sì**, Azure Files supporta GZRS. Tuttavia, NON supporta RA-GRS e RA-GZRS (le varianti con accesso in lettura).

#### Card 75
**D:** Quali sono i quattro tier di Blob Storage e la loro retention minima?
**R:** **Hot** (nessun minimo) → **Cool** (30 giorni) → **Cold** (90 giorni) → **Archive** (180 giorni, offline, richiede rehydration). Da Hot ad Archive: costo storage diminuisce, costo accesso aumenta.

#### Card 76
**D:** Che cos'è la rehydration nel Blob Storage?
**R:** Il processo di spostamento di un Blob dal tier Archive al tier Hot o Cool per potervi accedere. I dati nell'Archive tier sono offline e richiedono rehydration prima di qualsiasi operazione di lettura.

#### Card 77
**D:** Il tier Archive può essere impostato a livello di account?
**R:** **No.** I tier Hot, Cool e Cold possono essere impostati a livello di account (default per nuovi blob). Il tier **Archive** può essere impostato solo a **livello di blob** individuale.

#### Card 78
**D:** Quali sono i cinque servizi di Azure Storage?
**R:** **Blob** (dati non strutturati + Data Lake Gen2), **Files** (file share SMB/NFS), **Queues** (messaggistica asincrona, max 64 KB), **Disks** (volumi blocco per VM), **Tables** (dati NoSQL strutturati).

#### Card 79
**D:** Qual è la differenza tra AzCopy e Azure File Sync?
**R:** **AzCopy** = CLI, sincronizzazione **mono-direzionale** (source→destination), funziona cross-cloud. **Azure File Sync** = sincronizzazione **bidirezionale** automatica tra Azure Files e Windows Server on-prem, con cloud tiering.

#### Card 80
**D:** Che cos'è Azure Storage Explorer?
**R:** Applicazione GUI (Windows/macOS/Linux) per esplorare e gestire blob e file. Usa **AzCopy nel backend** per tutte le operazioni sui file/blob.

#### Card 81
**D:** Che cos'è Azure Data Box?
**R:** Servizio di migrazione dati offline per trasferire grandi dataset via dispositivo fisico. Varianti: **Data Box Disk** (~35 TB), **Data Box** (80 TB), **Data Box Heavy** (~770 TB). Il dispositivo viene cancellato secondo standard **NIST 800-88r1**.

#### Card 82
**D:** Che cos'è Azure Migrate?
**R:** Hub unificato per valutare e migrare infrastruttura on-premises in Azure. Un unico portale per avviare, eseguire e monitorare la migrazione. Include discovery, assessment, migrazione server/DB/web app e strumenti ISV.

### Identità e sicurezza

#### Card 83
**D:** Qual è la differenza tra autenticazione e autorizzazione?
**R:** **Autenticazione** = verificare l'identità (chi sei?). **Autorizzazione** = verificare i permessi (cosa puoi fare?). L'autenticazione viene sempre prima dell'autorizzazione.

#### Card 84
**D:** Che cos'è Microsoft Entra ID (ex Azure AD)?
**R:** Servizio cloud di gestione identità e accesso. Fornisce: autenticazione (MFA, password reset, smart lockout), SSO, gestione applicazioni, gestione dispositivi. Usato da admin IT, sviluppatori, utenti e abbonati M365/Azure.

#### Card 85
**D:** Che cos'è Microsoft Entra Connect?
**R:** Strumento che sincronizza le identità utente **bidirezionalmente** tra Active Directory on-premises e Microsoft Entra ID. Abilita SSO, MFA e reset password per entrambi gli ambienti.

#### Card 86
**D:** Che cos'è Microsoft Entra Domain Services?
**R:** Servizi di dominio gestiti (domain join, group policy, LDAP, Kerberos/NTLM) senza distribuire domain controller. Sincronizzazione **one-way** (da Entra ID verso il basso). Ideale per app legacy in lift-and-shift.

#### Card 87
**D:** Cosa significa MFA e quali sono i tre fattori?
**R:** Multi-Factor Authentication: richiede 2+ fattori di verifica. **Something you know** (password), **something you have** (telefono/chiave), **something you are** (biometrico). Una password compromessa da sola non basta.

#### Card 88
**D:** Quali sono le tre opzioni di autenticazione passwordless?
**R:** **Windows Hello for Business** (PC, biometrico/PIN, PKI+SSO), **Microsoft Authenticator** (telefono, number match + biometrico/PIN), **FIDO2 Security Keys** (dispositivo esterno USB/BT/NFC, unphishable, ideale per workstation condivise).

#### Card 89
**D:** Che cos'è il Conditional Access?
**R:** Strumento Entra ID che consente/nega accesso in base a segnali di identità. Flusso: **Segnali** (utente, posizione, dispositivo, app, rischio) → **Decisione** (consenti/MFA/blocca) → **Enforcement** (applica condizioni). Solo tier Premium.

#### Card 90
**D:** Che cos'è il Single Sign-On (SSO)?
**R:** L'utente si autentica una volta e accede a più applicazioni senza reinserire le credenziali. Riduce il proliferare di password. Attenzione: SSO è sicuro solo quanto l'autenticatore iniziale.

#### Card 91
**D:** Che cos'è RBAC in Azure?
**R:** Role-Based Access Control: controlla cosa gli utenti possono fare sulle risorse in base a ruoli assegnati. **Additivo** (modello allow): i permessi effettivi = unione di tutti i ruoli assegnati. NON ha deny. NON agisce a livello applicazione/dati.

#### Card 92
**D:** Quali sono i tre ruoli RBAC principali built-in?
**R:** **Owner** (accesso completo + può delegare), **Contributor** (può creare/gestire, ma non delegare), **Reader** (solo lettura).

#### Card 93
**D:** Quali sono i tre principi di Zero Trust?
**R:** **Verify explicitly** (autentica sempre con tutti i dati disponibili), **Use least privilege access** (JIT/JEA, policy adattive), **Assume breach** (limita l'impatto, segmenta l'accesso, verifica crittografia end-to-end).

#### Card 94
**D:** Quali sono i sette strati della Defense in Depth (dall'esterno all'interno)?
**R:** **Physical** → **Identity & Access** → **Perimeter** → **Network** → **Compute** → **Application** → **Data**. Nessun singolo strato fornisce protezione completa.

#### Card 95
**D:** Che cos'è Azure Key Vault? Cosa conserva?
**R:** Servizio centralizzato per archiviare in modo sicuro: **Secrets** (password, connection strings), **Encryption keys** (RSA/EC, HSM-backed), **Certificates** (TLS/SSL con auto-renewal). Elimina credenziali hard-coded grazie alle managed identity.

#### Card 96
**D:** Che cos'è Microsoft Defender for Cloud?
**R:** Servizio di gestione postura di sicurezza e protezione dalle minacce. Tre pilastri: **Assess** (vulnerabilità, Secure Score) → **Secure** (MCSB, Azure Policy) → **Defend** (alert, kill-chain analysis, JIT VM access). Copre Azure, hybrid (Arc) e multicloud (AWS, GCP).

#### Card 97
**D:** Che cos'è il Secure Score?
**R:** Metrica in Defender for Cloud che raggruppa le raccomandazioni di sicurezza in controlli e calcola un punteggio, permettendo ai team di capire rapidamente la postura di sicurezza e dare priorità ai miglioramenti.

#### Card 98
**D:** Che cos'è Microsoft Purview?
**R:** Famiglia di soluzioni di data governance, rischio e compliance. Tre capacità: **data discovery automatizzato**, **classificazione dati sensibili**, **data lineage end-to-end**. Due aree: Risk and Compliance (M365) e Unified Data Governance.

#### Card 99
**D:** Quali sono le tre capacità di External ID di Microsoft Entra?
**R:** **B2B Collaboration** (partner, oggetti guest nel directory), **B2B Direct Connect** (Teams shared channels, NON nel directory), **External ID for Customers** (consumer app, tenant separato, ex Azure AD B2C).

#### Card 100
**D:** Qual è la differenza tra Azure Firewall, NSG e WAF?
**R:** **Azure Firewall** = firewall di rete cloud-native, filtraggio centralizzato tra VNet. **NSG** = regole firewall a livello di subnet/NIC. **WAF** = protezione applicativa L7 (SQL injection, XSS). DDoS Protection + WAF = copertura L3/L4 + L7.

---

## Dominio 3 — Management & Governance (30–35% dell'esame)

### Gestione costi

#### Card 101
**D:** Quali sono i sei fattori che influenzano i costi Azure?
**R:** **Tipo di risorsa** (tipo, impostazioni, regione), **Consumo** (pay-as-you-go o impegno), **Manutenzione** (risorse inutilizzate costano), **Geografia** (costi variabili per regione), **Tipo di subscription** (free trial, pay-as-you-go), **Azure Marketplace** (costi vendor aggiuntivi).

#### Card 102
**D:** Quali sono le quattro opzioni di pricing e i rispettivi risparmi?
**R:** **Pay-as-you-go** (nessun impegno, tariffe standard). **Savings Plan** (1–3 anni, fino a 65%, compute flessibile). **Reservations** (1–3 anni, fino a 72%, risorsa specifica). **Spot** (nessun impegno, fino a 90%, solo workload interrompibili).

#### Card 103
**D:** Le Azure Reservations sono CapEx o OpEx?
**R:** **OpEx**. Non si acquista nessun asset fisico. Le reservations sono un impegno di pagamento per l'utilizzo futuro di risorse cloud. È una trappola d'esame frequente.

#### Card 104
**D:** Che cos'è il Pricing Calculator?
**R:** Strumento per stimare i costi Azure prima del deploy (https://azure.microsoft.com/pricing/calculator). Niente viene provisionato. È ora anche lo strumento raccomandato per scenari di migrazione, dato che il TCO Calculator è stato deprecato.

#### Card 105
**D:** Il TCO Calculator è ancora disponibile?
**R:** **No, è stato deprecato ad agosto 2025.** Il Pricing Calculator è ora lo strumento raccomandato per TUTTI gli scenari di stima costi, inclusi quelli di migrazione. Il TCO potrebbe ancora comparire all'esame durante la transizione.

#### Card 106
**D:** Quali sono i tre componenti di Azure Cost Management?
**R:** **Cost Analysis** (visualizzare/esplorare costi per ciclo, regione, resource group, servizio), **Cost Alerts** (budget alerts + credit alerts + dept quota alerts), **Budgets** (limiti di spesa + automazione per sospendere/modificare risorse).

#### Card 107
**D:** Che cosa sono i Tag in Azure?
**R:** Coppie nome/valore applicate alle risorse per categorizzazione. Sei casi d'uso: resource management, cost management, operations management, security, governance/compliance, workload optimization. Max **50 tag** per risorsa.

#### Card 108
**D:** I tag vengono ereditati dal resource group o dalla subscription?
**R:** **No.** I tag NON vengono ereditati. Puoi applicare tag a un livello senza che appaiano automaticamente ad altri livelli, permettendo schemi di tagging personalizzati. Usa Azure Policy per forzare regole di tagging.

#### Card 109
**D:** Che cos'è Azure Hybrid Benefit?
**R:** Programma per portare le proprie licenze Windows Server o SQL Server in Azure, con risparmi significativi (40%+ sulle VM).

#### Card 110
**D:** Che cosa sono le Azure Spot VMs?
**R:** VM che girano sulla capacità inutilizzata di Microsoft con forte sconto (fino a 90%). Azure può reclamare la VM in qualsiasi momento. Solo per workload interrompibili/fault-tolerant.

#### Card 111
**D:** Qual è la differenza tra Azure Advisor (Cost) e Cost Management?
**R:** **Cost Management** = analisi costi, creazione budget, alert di spesa (strumento di analisi). **Azure Advisor** (categoria Cost) = raccomandazioni personalizzate per ridurre la spesa (strumento di raccomandazione). È una trappola d'esame.

### Governance e compliance

#### Card 112
**D:** Che cos'è Azure Policy?
**R:** Servizio per creare, assegnare e gestire policy che controllano o auditano le risorse Azure. Può **prevenire** la creazione di risorse non conformi e **auto-rimediare** (es. aggiungere tag mancanti). Valuta anche le risorse esistenti retroattivamente.

#### Card 113
**D:** Quali sono i sette effetti di Azure Policy?
**R:** **Append** (aggiunge proprietà), **Audit** (log warning), **AuditIfNotExists** (warning se manca risorsa compagna), **Deny** (blocca creazione/modifica), **DeployIfNotExists** (deploy automatico risorsa compagna), **Modify** (aggiunge/modifica proprietà su risorse esistenti), **Disabled** (policy inattiva).

#### Card 114
**D:** Che cos'è un'Initiative in Azure Policy?
**R:** Un gruppo di policy correlate applicate insieme per tracciare la conformità verso un obiettivo più ampio. Esempio: "Enable Monitoring in Security Center" contiene 100+ definizioni di policy.

#### Card 115
**D:** Azure Policy valuta le risorse create prima della policy?
**R:** **Sì.** Azure Policy valuta le risorse retroattivamente — controlla anche le risorse che esistevano prima della creazione della policy.

#### Card 116
**D:** Che cosa sono i Resource Lock?
**R:** Impediscono la cancellazione o modifica accidentale. Due tipi: **Delete** (read + modify OK, no delete) e **ReadOnly** (solo lettura, simile al ruolo Reader). I lock **prevalgono su RBAC** — anche un Owner deve rimuovere il lock prima di agire.

#### Card 117
**D:** Come si modifica una risorsa con un lock?
**R:** Processo in due passaggi: (1) rimuovere il lock, (2) eseguire l'azione. I lock si ereditano verso il basso (resource group → tutte le risorse). Per gestire i lock serve il ruolo **Owner** o **User Access Administrator**.

#### Card 118
**D:** Che cos'è Azure Blueprints e qual è il suo stato attuale?
**R:** Servizio per impacchettare ARM template, policy, RBAC e resource group in definizioni riutilizzabili e versionabili. **È in fase di ritiro** → sostituito da **Template Specs** + **Deployment Stacks**. Potrebbe ancora apparire all'esame.

#### Card 119
**D:** Che cos'è il Service Trust Portal?
**R:** Portale Microsoft per informazioni su sicurezza, privacy e compliance (https://servicetrust.microsoft.com/). Richiede account Entra work/school + NDA. Tre menu: Service Trust Portal, My Library (pin + notifiche), All Documents. Report disponibili 12+ mesi.

#### Card 120
**D:** Che cos'è il Compliance Manager?
**R:** Strumento nel Service Trust Portal che valuta la conformità dell'organizzazione con vari standard (ISO, SOC, GDPR, ecc.) e fornisce azioni raccomandate per migliorare la postura di compliance.

### Strumenti di gestione e deploy

#### Card 121
**D:** Quali sono i cinque strumenti di gestione Azure?
**R:** **Azure Portal** (GUI web), **Cloud Shell** (shell browser-based), **Azure PowerShell** (cmdlet), **Azure CLI** (comandi Bash), **Copilot in Azure** (assistente AI). PowerShell e CLI sono funzionalmente equivalenti, differisce solo la sintassi.

#### Card 122
**D:** Che cos'è Azure Cloud Shell?
**R:** Shell browser-based (PowerShell o Bash) accessibile dal portale o dall'app mobile. Auto-autenticata, nessuna installazione locale. Richiede un **storage account** per persistere i file.

#### Card 123
**D:** Che cos'è Copilot in Azure?
**R:** Assistente AI nel portale Azure per guida contestuale in linguaggio naturale. Aiuta a esplorare servizi, comprendere configurazioni e redigere comandi/script. Trattalo come **assistente operativo**: gli umani validano e approvano.

#### Card 124
**D:** Che cos'è un ARM Template?
**R:** File JSON dichiarativo che definisce risorse Azure e le loro proprietà per deployment ripetibili. **Idempotente**: lo stesso template produce sempre lo stesso risultato senza duplicati. ARM valida prima del deploy e orchestra le risorse nell'ordine corretto e in parallelo.

#### Card 125
**D:** Che cos'è Bicep?
**R:** Linguaggio dichiarativo per il deploy di risorse Azure tramite ARM. Più **semplice e conciso** rispetto ai template ARM JSON. Idempotente. Supporta modularità via moduli Bicep.

#### Card 126
**D:** Qual è la differenza tra ARM Template e Bicep?
**R:** Entrambi sono IaC dichiarativi e idempotenti che deployano tramite ARM. **ARM Template** usa JSON (più verboso). **Bicep** ha sintassi semplificata e più leggibile. Bicep viene compilato in ARM Template JSON.

#### Card 127
**D:** Che cos'è Azure Arc?
**R:** Estende la gestione e governance Azure (RBAC, Policy, tag) a risorse on-premises e multi-cloud tramite ARM. Cinque tipi di risorse: **server**, **cluster Kubernetes**, **data services**, **SQL Server**, **VM** (preview).

#### Card 128
**D:** Quali capacità abilita Azure Arc?
**R:** Gestione unificata (proiettare risorse non-Azure in ARM), gestire come se fossero in Azure (VM, K8s, DB multicloud), usare servizi Azure familiari ovunque, supportare ITOps + DevOps, custom locations su K8s Arc-enabled.

### Strumenti di monitoraggio

#### Card 129
**D:** Che cos'è Azure Advisor?
**R:** Guida personalizzata alle best practice integrata nel portale. Cinque categorie: **Reliability**, **Security**, **Performance**, **Operational Excellence**, **Cost**. "Capacity" NON è una categoria (trappola d'esame). Le raccomandazioni si possono accettare, posticipare o ignorare.

#### Card 130
**D:** Che cos'è Azure Service Health? Quali sono le tre viste?
**R:** Ti informa sullo stato di Azure e delle tue risorse. Tre viste che si restringono: **Azure Status** (globale, tutti i servizi) → **Service Health** (i tuoi servizi/regioni, con alert) → **Resource Health** (singola risorsa, indica se il problema è di Azure o tuo).

#### Card 131
**D:** Che cos'è Azure Monitor?
**R:** Piattaforma per raccogliere, analizzare e agire su dati da Azure, on-prem e multicloud. Piattaforma dati: Metrics, Logs, Traces. Output: Experiences, Visualize (Workbooks, Dashboard), Analyze (Log Analytics), Respond (Alerts, Autoscale), Integrate (Event Hubs, Logic Apps).

#### Card 132
**D:** Che cos'è Log Analytics?
**R:** Strumento nel portale Azure per scrivere ed eseguire query sui dati raccolti da Azure Monitor. Usa **KQL (Kusto Query Language)**. Permette filtraggio semplice fino ad analisi avanzate di trend.

#### Card 133
**D:** Che cos'è Application Insights?
**R:** Funzionalità di Azure Monitor per monitorare performance e utilizzo di web app (Azure, on-prem, altri cloud). Setup via SDK o agent (senza modifiche al codice). Monitora richieste, dipendenze, page load, performance server. Test di disponibilità inviano richieste sintetiche.

#### Card 134
**D:** Come funzionano gli Azure Monitor Alerts?
**R:** Notificano quando Azure Monitor rileva una condizione definita. Si crea un **alert rule** (condizione) e un **action group** (notifiche e azioni). Alert basati su metriche o log. Gli **action group** sono riutilizzabili tra Monitor, Service Health e Advisor.

#### Card 135
**D:** Quali sono i cinque piani di supporto Azure?
**R:** **Basic** (gratis, NO ticket tecnici) → **Developer** (~$29/mese, email in orario lavorativo) → **Standard** (~$100/mese, 24/7, <1h Sev A) → **Professional Direct** (~$1K/mese, 24/7 + advisory, <15min Sev A) → **Premier/Unified** (TAM, contratto enterprise).

#### Card 136
**D:** Quale piano di supporto NON permette di aprire ticket tecnici?
**R:** **Basic**. Il piano Basic è gratuito e consente solo richieste di fatturazione e sottoscrizione. Per aprire ticket di supporto tecnico serve almeno il piano **Developer**.

#### Card 137
**D:** Come si aumentano i limiti di quota di una subscription Azure?
**R:** Aprendo una **Support request** (richiesta di supporto) selezionando "Service and subscription limits (quotas)". NON tramite Service Health alert.

---

## Bonus — Trappole comuni (~10 card per errori frequenti)

#### Card 138
**D:** TRAPPOLA: Il TCO Calculator è lo strumento per stimare il risparmio di migrazione?
**R:** **No, il TCO Calculator è stato deprecato (agosto 2025).** Il **Pricing Calculator** è ora lo strumento raccomandato per TUTTE le stime di costo, incluse le migrazioni. Se l'esame cita il TCO, ricorda che è stato ritirato.

#### Card 139
**D:** TRAPPOLA: Azure Blueprints è lo strumento per impacchettare governance e deploy?
**R:** Blueprints è **in fase di ritiro**. Il successore è **Template Specs** (template ARM riutilizzabili) + **Deployment Stacks** (gestione risorse come unità singola). Potrebbe ancora apparire all'esame durante la transizione.

#### Card 140
**D:** TRAPPOLA: Le Azure Reservations sono CapEx perché si paga in anticipo?
**R:** **No, le Reservations sono OpEx.** Non si acquista nessun asset fisico. Si tratta di un impegno di pagamento per l'utilizzo futuro di risorse cloud. L'impegno 1-3 anni non lo rende CapEx.

#### Card 141
**D:** TRAPPOLA: AKS è IaaS perché si gestiscono container?
**R:** **No, AKS è PaaS.** Azure gestisce il control plane di Kubernetes. Tu distribuisci i container ma non gestisci l'infrastruttura sottostante. L'errore è comune nelle fonti di studio.

#### Card 142
**D:** TRAPPOLA: RBAC ha sia allow che deny?
**R:** **No, RBAC è solo additivo (modello allow).** I permessi effettivi sono l'unione di tutti i ruoli assegnati. Non esiste il deny in RBAC. Se hai un ruolo Read e uno Read+Write, il permesso effettivo è Read+Write.

#### Card 143
**D:** TRAPPOLA: Nel modello di responsabilità condivisa, il provider gestisce i dati in SaaS?
**R:** **No. I dati sono SEMPRE responsabilità tua**, in tutti i modelli (IaaS, PaaS, SaaS). Tu possiedi governance, classificazione e controllo degli accessi ai dati. Il provider gestisce l'infrastruttura dati, non i tuoi dati.

#### Card 144
**D:** TRAPPOLA: Quali sono i sette strati della Defense in Depth nell'ordine corretto?
**R:** **Physical → Identity & Access → Perimeter → Network → Compute → Application → Data** (dall'esterno all'interno). Il dato è al centro, obiettivo ultimo dell'attaccante. Non confondere l'ordine.

#### Card 145
**D:** TRAPPOLA: Zero Trust si basa sulla posizione di rete?
**R:** **No.** Zero Trust è basato sull'**identità**, non sulla posizione. I tre principi: verificare esplicitamente, accesso con privilegio minimo (JIT/JEA), assumere la violazione. Ogni richiesta viene valutata indipendentemente dalla rete di provenienza.

#### Card 146
**D:** TRAPPOLA: "Capacity" è una categoria di Azure Advisor?
**R:** **No.** Le cinque categorie sono: **Reliability, Security, Performance, Operational Excellence, Cost**. "Capacity" è una trappola d'esame ricorrente che non esiste tra le categorie di Advisor.

#### Card 147
**D:** TRAPPOLA: Il piano Basic di supporto Azure permette di aprire ticket tecnici?
**R:** **No.** Il piano Basic è gratuito e permette solo richieste relative a fatturazione e sottoscrizione. Per ticket tecnici serve almeno il piano **Developer** ($29/mese).

#### Card 148
**D:** TRAPPOLA: I tag vengono ereditati automaticamente dal resource group?
**R:** **No.** I tag NON vengono ereditati da resource group o subscription. Ogni livello ha il proprio schema di tagging. Usa **Azure Policy** per forzare l'applicazione automatica dei tag.

#### Card 149
**D:** TRAPPOLA: Un resource group è un confine di sicurezza di rete?
**R:** **No.** I resource group controllano gestione e permessi (RBAC), non isolamento di rete. Per la sicurezza di rete servono NSG, Private Endpoint, Azure Firewall o altri meccanismi di rete.

#### Card 150
**D:** TRAPPOLA: Azure Cost Management fornisce raccomandazioni per risparmiare?
**R:** **No.** Cost Management fornisce **analisi**, budget e alert. Le **raccomandazioni** per ottimizzare la spesa vengono da **Azure Advisor** (categoria Cost). Confondere i due è una trappola d'esame nota.

#### Card 151
**D:** TRAPPOLA: La connessione Site-to-Site serve per collegare due VNet Azure?
**R:** **No.** Per collegare due VNet Azure si usa **VNet-to-VNet** o **VNet Peering**. La connessione **Site-to-Site** è specificamente per collegare una rete on-premises ad Azure.

#### Card 152
**D:** TRAPPOLA: In PaaS il cliente gestisce l'OS?
**R:** **No.** In PaaS il **provider** gestisce l'OS (oltre a infrastruttura e middleware). Il cliente gestisce solo **codice applicativo e dati**. La gestione dell'OS da parte del cliente avviene solo in IaaS.

---

> **Totale: 152 flashcard** — ~35 Dominio 1, ~65 Dominio 2, ~37 Dominio 3, ~15 Bonus Trappole.
>
> Buono studio e in bocca al lupo per l'esame AZ-900! 🎯
