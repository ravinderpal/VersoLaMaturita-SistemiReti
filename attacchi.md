# Attacchi Informatici

## Proteggersi dagli attacchi

Come proteggere i propri sistemi

Da sapere per ogni attacco:

* Nome
* Cosa fa
* Come ci si difende

### Concetti importanti

* Firewall
* DMZ
* NAT
* Sniffing/Snooping
* Spoofing
* Smurfing \(tipo di DDoS\)

### Obiettivi degli attaccanti

* Furto di dati confidenziali
* Accesso non autorizzato
* Modifiche non autorizzate

### ISO 27001:2005

Standardizza le modalità di protezione dei dati per garantire l'affidabilità, la sicurezza, l'integrità e la riservatezza.

Il problema più grave consiste però negli attacchi **non noti**.

### Cos'è la Sicurezza

La **Sicurezza** è l'assenza di condizioni conflittuali capaci di produrre danni morali o irreparabili a un sistema.

* **Safety**: accorgimenti atti ad eleminare la produzione di danni irreparabili
* **Reliability**: prevenzione da eventi che possono produrre qualsiasi tipo di danni

#### Modelli di sicurezza per il controllo degli utenti

**Grant Option**: concessione, privilegio. è un potenziale problema di sicurezza

* Esempio: No write down, no read up
* Sono gerarchici: chi ha un grant option può concederlo ad altri

#### Modelli di sicurezza per il controllo dei programmi

* **Semantic-based**: la sicurezza del programma è considerata in base al suo comportamento
* **Security-typed language**: modelli basati sul linguaggio

### Tiplogie di errori

* **Error**: errore umano
* **Failure**: comportamento imprevisto e incongruo rispetto alle specifiche del programma
* **Fault**: difetto \(colpa\) del codice sorgente

**Esempi di tecniche di attacco**: exploit, buffer overflow, shellcode, cracking, backdoor, port scanning, sniffing, keylogging, spoofing, trojan, virus informatici, DoS, ingegneria sociale

## Tipi di attacchi

#### 0-Day

* un attacco **0-Day** sfrutta vulnerabilità non note, di conseguenza ha effetti potenzialmente disastrosi
* un attacco rimane **0-Day** finchè non viene trovata una soluzione o protezione

#### Port scanning

è una tecnica che permette di raccogliere informazioni su una rete e i suoi nodi.

**Ack scan**: è un tipo di port scanning che scopre se le porte aperte su un firewall sono filtrate o non filtrate.

#### Arbitrary code execution

Descrive un attacco in cui l'attaccante è in grado di eseguire programmi sul dispositivo vittima.

#### Man in the middle

Indica un attacco in cui l'attaccante si trova "nel mezzo" di una comunicazione tra due vittime.

#### Replay attack \(approfondimento\)

Il replay attack consiste in due passi:

1. catturare un pacchetto o un messaggio \(anche se crittografato o firmato\)
2. ripetere l'invio del messaggio o pacchetto alla sua originale destinazione \(potrebbe essere necessario alterarlo\)

Se il protocollo applicazione usato dal pacchetto _non si protegge_ dal **replay attack** allora il destinatario considererà valido il messaggio.

**Contromisura:** inserire una data di invio nei messaggi \(o un altro identificativo univoco\) e firmarli digitalmente e/o crittografarli in modo che non sia alterabile dall'attaccante, successivamente il destinatario deve controllare di non aver ricevuto in precedenza un messaggio identico con la stessa identica data.

#### ARP Spoofing/Poisoning

L'attaccante impersona il mac address della vittima e/o del gateway per appropriarsi del loro indirizzo IP \(tramite i pacchetti ARP\) e sniffare il traffico.

Esempio:

* nella rete sono presenti **A**, **B** e l'attaccante **C**
* **C** _"avvelena"_ le tabelle **ARP** di **A** e **B** facendo credere:
  * ad **A** che **C** sia in realtà **B**
  * a **B** che **C** sia in realtà **A**
* in questo modo, l'attaccante si trova effettivamente nel mezzo delle comunicazioni tra **A** e **B** e può:
  * leggere le comunicazioni non sicure
  * alterare le comunicazioni non sicure
  * annullare le comunicazioni

### DoS

**Denial of service** \(_negazione del servizio_, abbreviato in **DoS**\) nel campo della sicurezza informatica indica un malfunzionamento dovuto ad un attacco informatico in cui si esauriscono deliberatamente le risorse di un sistema informatico che fornisce un servizio ai client, ad esempio un sito web su un web server, fino a renderlo non più in grado di erogare il servizio ai client richiedenti.

I pacchetti dannosi \(specialmente se predisposti con un indirizzo IP sorgente **falsificato** rispetto all'originale\) procureranno al computer _"vulnerabile"_ una situazione temporanea di **Denial of service**, tuttavia, poiché le connessioni che sono normalmente disponibili sono lente _per tutti_ \(per soggetti ben intenzionati così come per soggetti malintenzionati\), questo tipo di attacco diventa impraticabile, nel senso che non dà il risultato atteso \(i.e. la congestione del server\).

**Un esempio** potrebbe essere il seguente: l'attaccante, identificato dal nome STE, invia una serie di richieste alla sua vittima, identificata col nome CRI: la macchina server, sulla quale vengono eseguiti dei servizi, non sarà in grado di gestire tutte le richieste e i servizi stessi andranno in crash, risultando prima molto rallentati e poi, successivamente, inaccessibili. In questa maniera, un utente qualunque \(identificato dal nome UTENTE\) non sarà in grado di accedere ai servizi, ricevendo un errore di richiesta scaduta o timeout.

#### Amplification attack \(Smurf attack\)

è una variante di **DoS** che sfrutta pacchetti malformati o richieste particolari per far si che la vittima produca del traffico a scopo di causare **DoS**.

L'amplification attack consiste nel generare una serie di pacchetti con **IP sorgente modificato** per corrispondere a quello della vittima, successivamente **inviarli in broadcast** al **massimo numero di computer possibile**. Questi dispositivi _risponderanno alla vittima tutti insieme_, occupandone l'intera banda e possibilmente il tempo di CPU.

#### Syn Flooding

Il termine **Syn Flooding**, letteralmente tradotto con _"inondazione di pacchetti di tipo Syn"_, nasce dal fatto che tutte le volte che un utente fa click su di un link di una pagina web richiede l'apertura di una connessione \(di tipo **TCP**\) verso quel sito.

Questo avviene seguendo una serie di passi, il primo dei quali consiste nell'_invio di un pacchetto TCP_ che richiede l'apertura di una connessione.

Tutte le **regole di funzionamento del protocollo TCP** esigono che il sistema risponda _allocando alcune risorse_ \(una piccola porzione di **RAM**\) per la connessione. Se si programma opportunamente un semplice PC, è possibile richiedere l'apertura di _diverse migliaia di connessioni al secondo_, che _"inondando"_ il server, ne consumano rapidamente tutta la memoria, bloccandolo o mandandolo in crash.

Il punto debole di questo tipo di attacco è che il computer attaccante deve poter mandare il flusso di pacchetti attraverso la connessione ad Internet fino al server attaccato.

Diversamente, l'utente malintenzionato deve poter fornire delle "credenziali" di accesso valide per usufruire della vulnerabilità insorta nel sistema operativo e portare a termine, efficacemente, l'attacco al sito bersaglio.

#### Distributed DoS

Una variante di tale approccio è il **DDoS \(Distributed Denial of Service\)**, dal _funzionamento identico: ma realizzato utilizzando \_numerose macchine attaccanti_ che insieme costituiscono una _botnet_.

**Botnet**: insieme di macchine _"zombie"_ infette da un virus controllate a comando da una o più persone

Gli attaccanti tendono a non esporsi direttamente, dato che per le forze dell'ordine sarebbe _relativamente_ semplice risalire ai computer utilizzati per l'attacco. Gli attaccanti, per evitare di essere individuati e per avere a disposizione un numero sufficiente di computer per l'attacco, infettano precedentemente un numero _molto elevato_ di computer con dei **virus o worm** che lasciano aperte delle _backdoor a loro riservate_. I computer che sono controllati dall'attaccante vengono chiamati **"zombie"**.

Tutti i computer infettati entrano a far parte di una botnet, a libera disposizione dell'attaccante: una nota interessante è data dalla distinzione tra le macchine che eseguono un Sistema Operativo Windows \(definiti, in gergo, rxbot\) e quelle che invece eseguono un sistema Unix, particolarmente adatte all'UDP Flooding \(Flooding sul protocollo UDP\).

Una particolarità degli zombies Windows è data dalla possibilità, per l'attaccante, di programmare un trojan in grado di diffondersi automaticamente a tutta una serie di contatti presenti sul computer infettato \(definita, in gergo, funzione di auto-spreading\): contatti contenuti nella rubrica degli indirizzi e nei contatti di programmi di Instant Messaging, come Microsoft Messenger, permettendo così al computer zombie di infettare, in maniera completamente autonoma, altre macchine che, a loro volta, diverranno parte della botnet dell'attaccante.

Quando il numero di zombies è ritenuto adeguato, o quando viene a verificarsi una data condizione, i computer infetti si attivano e sommergono il server bersaglio di richieste di connessione. Con l'avvento della banda larga il fenomeno dei DDoS sta assumendo proporzioni preoccupanti, dato che attualmente esistono milioni di persone dotate di una connessione ad Internet molto veloce e permanente ma con scarse o nulle conoscenze e contromisure riguardanti la sicurezza informatica.

Il danno maggiore dell'attacco di tipo DDoS è dovuto principalmente alla "asimmetria" che si viene a creare tra "la" richiesta e le risposte correlate in una sessione DNS \(Domain Name System\). Il flusso enorme di risposte generato provocherà nel sistema una tale "inondazione" di traffico rendendo il server inadeguato alla gestione delle abituali funzioni on-line.

Inoltrando al sito preso di mira una risposta di alcuni Kilobyte per ogni richiesta contenente solo pochi byte, si ottiene un'amplificazione esponenziale tale da saturare i canali dati più capienti, raggiungendo con il DDoS livelli finora inattuabili con gli altri tipi di attacco DoS.

Le configurazioni predefinite, standard e quelle "consigliate" di Firewall si rivelano utili a contrastare solo gli "attacchi" sferrati dall'esterno, ad esempio di un'azienda, ma poiché il traffico in Rete gestito tramite sistema DNS è vitale, per fronteggiare questo tipo di attacco non si potranno attuare le stesse strategie impiegate nei confronti degli attacchi ai Ping. Di conseguenza, il Network manager dovrà tenere scrupolosamente sotto controllo e monitoraggio i canali di flusso dati e, per escludere l'intervento o contrastare l'azione di un cracker, riconfigurerà il DNS responsabile del sito.

**Contromisure:**

* port security sugli switch \(solo un mac address per ogni porta\)
* Secure ARP \(SARP\) che si basa su crittografia asimmetrica
* Usare un software di monitoring come OpenAAPD
* Mantenere tabelle ARP su ogni dispositivo
* Ridondanza dei dati per non avere una vittima isolata

