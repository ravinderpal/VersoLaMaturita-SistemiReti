# IDS: Intrusion Detection System

Nella sicurezza informatica l'Intrusion Detection System o IDS è un dispositivo software o hardware (o a volte la combinazione di entrambi utilizzato per identificare accessi non autorizzati ai computer o alle reti locali. Le intrusioni rilevate possono essere quelle prodotte da cracker esperti, da tool automatici o da utenti
inesperti che utilizzano programmi semiautomatici.

__Esempio di IDS:__ Snort

- è basato su delle regole conservate in database
- analizza i pacchetti confrontandoli con le regole
- in caso le regole non sono rispettate viene generato un __alert__ (__allarme__) e i dettagli vengono scritti nei log.

## Cosa fa e cosa non fa

- Non modifica e non blocca i pacchetti
- Non è un firewall, non svolge difesa attiva
- Non cerca di bloccare intrusioni, __ma le rileva quando si verificano__

# IPS: Intrusion Prevention System

In informatica gli __Intrusion prevention system__ sono dei componenti sviluppati per incrementare
la sicurezza informatica di un sistema informatico. Sono stati sviluppati per impedire ad un
programma non autorizzato di entrare in esecuzione. La tecnologia "Intrusion prevention" spesso
viene considerata come un'estensione della tecnologia intrusion detection (IDS) sebbene sia più simile
ad una lista di controllo degli accessi di un firewall.

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

# Snort

SNORT è un IDS

Usa un sistema di regole con un __header__ che include

- action
- protocol
- source IP:port
- direction
- destination IP:port

E tante altre opzioni# IDS

