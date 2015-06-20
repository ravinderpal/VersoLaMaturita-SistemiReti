# IDS: Intrusion Detection System

Nella sicurezza informatica l'Intrusion Detection System o IDS è un dispositivo software o hardware (o a volte la combinazione di entrambi) utilizzato per identificare accessi non autorizzati ai computer o alle reti locali. Le intrusioni rilevate possono essere quelle prodotte da cracker esperti, da tool automatici o da utenti
inesperti che utilizzano programmi semiautomatici.

__Esempio di IDS:__ Snort

- è basato su delle regole conservate in database.
- analizza i pacchetti confrontandoli con le regole.
- in caso le regole non sono rispettate viene generato un __alert__ (__allarme__) e i dettagli vengono scritti nei log.

Un IDS è composto da quattro componenti:
- uno o più _sensori_ utilizzati per ricevere le informazioni dalla rete o dai computer.
- una _console_ utilizzata per monitorare lo stato della rete e dei computer.
- un _motore_ che analizza i dati prelevati dai sensori e provvede a individuare eventuali falle nella
sicurezza informatica.
- un _database_ cui si appoggia il motore di analisi e dove sono memorizzate una serie di regole utilizzate per identificare violazioni della sicurezza.

## Cosa fa e cosa non fa
- Non modifica e non blocca i pacchetti
- Non è un firewall, non svolge difesa attiva
- Non cerca di bloccare intrusioni, __ma le rileva quando si verificano__

# IPS: Intrusion Prevention System

In informatica gli __Intrusion prevention system__ sono dei componenti sviluppati per incrementare la sicurezza informatica di un sistema informatico. Sono stati sviluppati per impedire ad un programma non autorizzato di entrare in esecuzione. La tecnologia _Intrusion prevention_ spesso viene considerata come un'estensione della tecnologia IDS sebbene sia più simile ad una lista di controllo degli accessi di un firewall.

L'__IPS__ __NON__ è un firewall, poiché un firewall lavora su IP e Porte, mentre un __IPS__ lavora su __programmi__ e __utenti__.

## Insider Attacks
Per Insider Attack si intendono gli attacchi provenienti dall'interno della rete che non possono essere bloccati dagli IDS. Sono quindi più difficili da identificare e prevenire.
Un semplice esempio può essere un dipendente malintenzionato che, dopo essere stato licenziato, decide di vendicarsi con la compagnia manomettendo il sistema o rubando dati sensibile per poi venderli alla concorrenza.


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

