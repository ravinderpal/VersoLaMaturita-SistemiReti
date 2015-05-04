# Proteggersi dagli attacchi

Come proteggere i propri sistemi

Da sapere per ogni attacco:

- Nome
- Cosa fa
- Come ci si difende

## Concetti importanti

- Firewall
- DMZ
- NAT
- Spoofing
- Snooping
- Smurfing

## Obiettivi degli attaccanti

- Furto di dati confidenziali
- Accesso non autorizzato
- Modifiche non autorizzate

## ISO 27001:2005

Standardizza le modalità di protezione dei dati per garantire l'affidabilità, la sicurezza, l'integrità e la riservatezza.

Il problema più grave consiste però negli attacchi __non noti__.

## Cos'è la Sicurezza

La __Sicurezza__ è l'assenza di condizioni conflittuali capaci di produrre danni morali o irreparabili a un sistema.

- __Safety__: accorgimenti atti ad eleminare la produzione di danni irreparabili
- __Reliability__: prevenzione da eventi che possono produrre qualsiasi tipo di danni

### Modelli di sicurezza per il controllo degli utenti

__Grant Option__: concessione, privilegio. è un potenziale problema di sicurezza

- Esempio: No write down, no read up
- Sono gerarchici: chi ha un grant option può concederlo ad altri

### Modelli di sicurezza per il controllo dei programmi

- __Semantic-based__: la sicurezza del programma è considerata in base al suo comportamento
- __Security-typed language__: modelli basati sul linguaggio

## Tiplogie di errori

- __Error__: errore umano
- __Failure__: comportamento imprevisto e incongruo rispetto alle specifiche del programma
- __Fault__: difetto (colpa) del codice sorgente

__Esempi di tecniche di attacco__: exploit, buffer overflow, shellcode, cracking, backdoor, port scanning, sniffing, keylogging, spoofing, trojan, virus informatici, DoS, ingegneria sociale

# Tipi di attacchi

## 0-Day

- un attacco __0-Day__ sfrutta vulnerabilità non note, di conseguenza ha effetti potenzialmente disastrosi
- un attacco rimane __0-Day__ finchè non viene trovata una soluzione o protezione

## Port scanning

è una tecnica che permette di raccogliere informazioni su una rete e i suoi nodi.

### Ack scan

è un tipo di port scanning che scopre se le porte aperte su un firewall sono filtrate o non filtrate.

## Amplification attack

è una variante di __DoS__ che sfrutta pacchetti malformati o richieste particolari per far si che la vittima produca del traffico a scopo di causare __DoS__.

## Arbitrary code execution

descrive un attacco in cui l'attaccante è in grado di eseguire programmi sul dispositivo vittima.

## Man in the middle

### ARP Spoofing/Poisoning

L'attaccante impersona il mac address della vittima e/o del gateway per appropriarsi del loro indirizzo IP (tramite i pacchetti ARP) e sniffare il traffico

__Contromisure:__

- port security sugli switch (solo un mac address per ogni porta)
- Secure ARP (SARP) che si basa su crittografia asimmetrica
- Usare un software di monitoring come OpenAAPD
- Mantenere tabelle ARP su ogni dispositivo

# Honeypot

Un honeypot è un sistema o componente di una rete o di una macchina che appare come importante dal punto di vista dell'attaccante, ma che viene usato come esca a fine di protezione dagli attacchi successivi.

Possono essere sistemi reali con logger vari e sistemi di allarme oppure dei sistemi emulati. Possono anche essere interi reti

Possono avere applicazioni "stub" e "mock" che imitano reali sistemi di gestione mail ad esempio

Il posizionamento delle honeypot può essere più interno a maggiore efficacia e rischio oppure più esterno, separato dalla rete reale a scopo di ridurre i rischi.

### Honeypot a bassa interazione

Semplice da installare e sicuri, ma riescono a catturare poche informazioni

__Esempi__: honeyd

### Honeypot ad alta interazione

Complessi da installare, non emulano nulla: sono dei veri sistemi. Ad alto rischio ma ad alto guadagno in caso di attacco e raccolta dati.

__Esempi__: honeynet

### Alternative

Siti web e/o chat room vulnerabili possono essere usate a scopo di identificare criminali.

### Spammer e Honeypot

Esistono delle honeypot che agiscono da risorse facilmente abusabili per spam a scopo di scoprire e limitare l'attività degli spammer

# IDS: Intrusion Detection System

__Esempio:__ Snort

- è basato su delle regole conservate in database
- analizza i pacchetti confrontandoli con le regole
- in caso le regole non sono rispettate viene generato un __alert__ (__allarme__) e i dettagli vengono scritti nei log.

## Cosa fa e cosa non fa

- Non modifica e non blocca i pacchetti
- Non è un firewall, non svolge difesa attiva
- Non cerca di bloccare intrusioni, __ma le rileva quando si verificano__

# IPS: Intrusion Prevention System

A differenza di un __IDS__, un __IPS__ è anche in grado di intervenire. Viene spesso considerato un'estensione dell'__IDS__.

L'__IPS__ __NON__ è un firewall, poichè un firewall lavora su IP e Porte, mentre un __IPS__ lavora su __programmi__ e __utenti__.

# Intrusion examples

- remote root compromise
- web server defacement
- guessing / cracking passwords
- copying / viewing sensitive data(bases)
- running a packet sniffer
- distributing pirate software
- using an unsecured modem to access net (?????)
- impersonating a user to reset password
- using an unattended workstation
- post-it with password sticked to a monitor

## Insider Attacks

- most difficult to prevent and detect
- employees have access and system knowledge
- may be motivated by revenge or entitlement
    - after employee termination
    - taking data to competitor(s)
- To prevent/detect, the system needs __log monitoring__, __strong autentication__, __ability to block access__ and __backups/data mirroring__

# Host-Based IDS

- Specialized software to monitor system activity to detect suspicious behavior
- two approaches:
    - signature detection: defines proper behavior
    - anomaly detection: defines normal/expected behavior

## IDS: Intrusion Detection System

- deve essere in esecuzione continuamente
- __Host based IDS:__ monitorano un singolo host
- __Network based IDS:__ monitorano una rete

__Esempio:__ Snort

- è basato su delle regole conservate in database
- analizza i pacchetti confrontandoli con le regole
- in caso le regole non sono rispettate viene generato un __alert__ (__allarme__) e i dettagli vengono scritti nei log.

## Cosa fa e cosa non fa

- Non modifica e non blocca i pacchetti
- Non è un firewall, non svolge difesa attiva
- Non cerca di bloccare intrusioni, __ma le rileva quando si verificano__

# IPS: Intrusion Prevention System

A differenza di un __IDS__, un __IPS__ è anche in grado di intervenire. Viene spesso considerato un'estensione dell'__IDS__.

L'__IPS__ __NON__ è un firewall, poichè un firewall lavora su IP e Porte, mentre un __IPS__ lavora su __programmi__ e __utenti__.

# Intrusion examples

- remote root compromise
- web server defacement
- guessing / cracking passwords
- copying / viewing sensitive data(bases)
- running a packet sniffer
- distributing pirate software
- using an unsecured modem to access net (?????)
- impersonating a user to reset password
- using an unattended workstation
- post-it with password sticked to a monitor

## Insider Attacks

- most difficult to prevent and detect
- employees have access and system knowledge
- may be motivated by revenge or entitlement
    - after employee termination
    - taking data to competitor(s)
- To prevent/detect, the system needs __log monitoring__, __strong autentication__, __ability to block access__ and __backups/data mirroring__

# Host-Based IDS

- Specialized software to monitor system activity to detect suspicious behavior
- two approaches:
    - signature detection: defines proper behavior
    - anomaly detection: defines normal/expected behavior# Honeypot

# Snort

SNORT è un IDS

Usa un sistema di regole con un __header__ che include

- action
- protocol
- source IP:port
- direction
- destination IP:port

E tante altre opzioni