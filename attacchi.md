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
