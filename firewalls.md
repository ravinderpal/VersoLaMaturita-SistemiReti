# Firewall

Una prima definizione chiusa di firewall è la seguente: Apparato di rete hardware o software di ingresso-uscita bidirezionale che, opportunamente configurato o settato e agendo in maniera centralizzata, filtra tutti i pacchetti entranti ed uscenti, da e verso una rete o un computer, secondo regole prestabilite che contribuiscono alla sicurezza della stessa.

Un __firewall può essere__ realizzato con __un semplice computer__ (con almeno due schede di rete, una per l'input l'altra per l'output, e software apposito), può essere una funzionalità logica (__software__) inclusa __in un router__ __oppure__ può essere implementato su un __apparato hardware dedicato__. Esistono inoltre i cosiddetti firewall personali, che sono programmi installati sui normali calcolatori client, che filtrano solamente i pacchetti che entrano ed escono da quel calcolatore, utilizzando in tal caso solo una scheda di rete.

La __funzionalità principale__ in sostanza __è quella di creare un filtro sulle connessioni entranti ed uscenti__, innalzando il livello di sicurezza della rete e permettere sia agli utenti interni che a quelli esterni di operare nel massimo della sicurezza. Il firewall infatti agisce sui pacchetti in transito da e per la zona interna potendo eseguire su di essi operazioni di:

* controllo;
* modifica;
* monitoraggio.
* "aprendo" in tutti i casi il pacchetto IP e leggendo le informazioni presenti sul suo header, e in alcuni casi anche sul suo contenuto o payload.

## Tipologie

Tipologie di firewall, in ordine crescente di complessità:

* __packet filter__ è il più semplice e si limita a valutare gli header di ciascun pacchetto, decidendo quali far passare e quali no sulla base delle regole configurate. Ciascun pacchetto viene valutato solamente sulla base delle regole configurate, e per questo un firewall di questo tipo è detto anche _stateless_.
* __stateful inspection__ tiene traccia di alcune relazioni tra i pacchetti che lo attraversano. Ad esempio ricostruisce lo stato delle connessioni TCP.
* __deep packet inspection__ effettuano controlli fino al livello 7 della pila ISO/OSI, ovvero valutano anche il contenuto applicativo dei pacchetti, ad esempio riconoscendo e bloccando i dati appartenenti a virus o worm noti in una sessione HTTP o SMTP.
* __application layer firewall__ sono apparati che intercettano le connessioni a livello applicativo. __A questa categoria appartengono i proxy__. In tali casi, la configurazione della rete privata non consente connessioni dirette verso l'esterno, ma il proxy è connesso sia alla rete privata che alla rete pubblica, e permette alcune connessioni in modo selettivo, e solo per i protocolli che supporta.
La sintassi della configurazione di un firewall in molti casi è basata su un meccanismo di lista di controllo degli accessi (ACL), che possono essere statiche (quindi modificabili solo tramite configurazione esplicita da parte dell'amministratore di sistema) o dinamiche (cioè che possono variare in base allo stato interno del sistema).

## Altre funzionalità associate

Una funzione spesso associata al firewall è quella di __NAT__ (traduzione degli indirizzi di rete), che può contribuire a rendere inaccessibili i calcolatori sulla rete interna mascherandone gli indirizzi IP.

Molti firewall possono registrare tutte le operazioni fatte (__logging__), effettuare registrazioni più o meno selettive (ad esempio, registrare solo i pacchetti che violano una certa regola, non registrare più di N pacchetti al secondo), e tenere statistiche di quali regole sono state più violate.

La registrazione integrale dell'attività di un firewall può facilmente assumere dimensioni ingestibili, per cui spesso si usa il logging solo temporaneamente per diagnosticare problemi, o comunque in modo selettivo (logging dei soli pacchetti rifiutati o solo di alcune regole). Tuttavia, l'analisi dei log di un firewall (o anche dei contatori delle varie regole) può permettere di individuare in tempo reale tentativi di intrusione.

Talvolta ad un firewall è associata anche la funzione __rilevamento delle intrusioni (IDS)__, un sistema basato su euristiche che analizza il traffico e tenta di riconoscere possibili attacchi alla sicurezza della rete, e può anche scatenare reazioni automatiche da parte del firewall (Intrusion prevention system).
