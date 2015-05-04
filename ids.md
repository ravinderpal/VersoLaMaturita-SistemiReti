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

# Snort

SNORT è un IDS

Usa un sistema di regole con un __header__ che include

- action
- protocol
- source IP:port
- direction
- destination IP:port

E tante altre opzioni# IDS

