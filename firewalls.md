#Firewalls
Una prima definizione chiusa di firewall è la seguente: Apparato di rete hardware o software di ingresso-uscita bidirezionale che, opportunamente configurato o settato e agendo in maniera centralizzata, filtra tutti i pacchetti entranti ed uscenti, da e verso una rete o un computer, secondo regole prestabilite che contribuiscono alla sicurezza della stessa.

Un firewall può essere realizzato con un semplice computer (con almeno due schede di rete, una per l'input l'altra per l'output, e software apposito), può essere una funzionalità logica (software) inclusa in un router oppure può essere implementato su un apparato hardware dedicato. Esistono inoltre i cosiddetti "firewall personali", che sono programmi installati sui normali calcolatori client, che filtrano solamente i pacchetti che entrano ed escono da quel calcolatore, utilizzando in tal caso solo una scheda di rete.

La funzionalità principale in sostanza è quella di creare un filtro sulle connessioni entranti ed uscenti, innalzando il livello di sicurezza della rete e permettere sia agli utenti interni che a quelli esterni di operare nel massimo della sicurezza. Il firewall infatti agisce sui pacchetti in transito da e per la zona interna potendo eseguire su di essi operazioni di:

* controllo;
* modifica;
* monitoraggio.
* "aprendo" in tutti i casi il pacchetto IP e leggendo le informazioni presenti sul suo header, e in alcuni casi anche sul suo contenuto o payload.

##Tipologie
Tipologie di firewall, in ordine crescente di complessità:

* packet filter: è il più semplice e si limita a valutare gli header di ciascun pacchetto, decidendo quali far passare e quali no sulla base delle regole configurate. Ciascun pacchetto viene valutato solamente sulla base delle regole configurate, e per questo un firewall di questo tipo è detto anche stateless. Alcuni packet filter, analizzando i flag dell'header TCP, sono in grado di discriminare un pacchetto appartenente ad una "connessione TCP stabilita (established)" rispetto a quelli che iniziano una nuova connessione, ma non sono in grado di riconoscere un pacchetto malevolo che finga di appartenere ad una connessione TCP stabilita. Molti router posseggono una funzione di packet filter.
* stateful inspection:
tiene traccia di alcune relazioni tra i pacchetti che lo attraversano, ad esempio ricostruisce lo stato delle connessioni TCP.
* deep packet inspection:
 effettuano controlli fino al livello 7 della pila ISO/OSI, ovvero valutano anche il contenuto applicativo dei pacchetti, ad esempio riconoscendo e bloccando i dati appartenenti a virus o worm noti in una sessione HTTP o SMTP.
* application layer firewall:
 sono apparati che intercettano le connessioni a livello applicativo. A questa categoria appartengono i proxy. In tali casi, la configurazione della rete privata non consente connessioni dirette verso l'esterno, ma il proxy è connesso sia alla rete privata che alla rete pubblica, e permette alcune connessioni in modo selettivo, e solo per i protocolli che supporta.
La sintassi della configurazione di un firewall in molti casi è basata su un meccanismo di lista di controllo degli accessi (ACL), che possono essere statiche (quindi modificabili solo tramite configurazione esplicita da parte dell'amministratore di sistema) o dinamiche (cioè che possono variare in base allo stato interno del sistema, come ad esempio nel Port knocking).

#Altre funzionalità associate
Una funzione spesso associata al firewall è quella di NAT (traduzione degli indirizzi di rete), che può contribuire a rendere inaccessibili i calcolatori sulla rete interna mascherandone gli indirizzi IP.

Molti firewall possono registrare tutte le operazioni fatte (logging), effettuare registrazioni più o meno selettive (ad esempio, registrare solo i pacchetti che violano una certa regola, non registrare più di N pacchetti al secondo), e tenere statistiche di quali regole sono state più violate.

La registrazione integrale dell'attività di un firewall può facilmente assumere dimensioni ingestibili, per cui spesso si usa il logging solo temporaneamente per diagnosticare problemi, o comunque in modo selettivo (logging dei soli pacchetti rifiutati o solo di alcune regole). Tuttavia, l'analisi dei log di un firewall (o anche dei contatori delle varie regole) può permettere di individuare in tempo reale tentativi di intrusione.

Talvolta ad un firewall è associata anche la funzione rilevamento delle intrusioni (IDS), un sistema basato su euristiche che analizza il traffico e tenta di riconoscere possibili attacchi alla sicurezza della rete, e può anche scatenare reazioni automatiche da parte del firewall (Intrusion prevention system).
