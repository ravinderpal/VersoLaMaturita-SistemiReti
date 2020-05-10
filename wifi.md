# Reti Wi-Fi

**Reti WIreless**

**Classi**

Esistono varie classi di Wi-Fi con prestazioni diverse \(come specificato meglio nei dettagli dello standard IEEE 802.11\), le principali sono:

classe a a 54 Mb/s \(5 GHz\) classe b a 11 Mb/s \(2,4 GHz\) classe g a 54 Mb/s \(2,4 GHz\) classe n a 450 Mb/s \(2,4 GHz e 5 GHz\) classe ac a 3 Gb/s \(5 GHz\)

**Sicurezza WI-FI**

**WEP** WEP usa l'algoritmo di cifratura stream RC4 per la sicurezza e utilizza il CRC-32 per verificare l'integrità dei dati. Nello specifico l'RC4 del WEP utilizza due chiavi, a 40 bit e a 104 bit. A queste vengono aggiunti 24 bit per il vettore di inizializzazione \(IV, Initialization Vector\) quando viene trasmesso in chiaro. L'RC4 è un algoritmo molto veloce e in un contesto di crittazione in tempo reale, come nelle reti senza fili, non è una caratteristica di poco conto.

**WPA / WPA ENTERPRISE** Il WPA era stato introdotto per tamponare l'emergenza sicurezza dovuta al WEP e rappresenta solamente uno standard transitorio, mentre l'802.11i veniva terminato e perfezionato. La Wi-Fi Alliance ha deciso di chiamare le specifiche 802.11i con il nome di WPA2, per rendere semplice all'utente comune l'individuazione delle schede basate sul nuovo standard. L'802.11i utilizza come algoritmo crittografico l'Advanced Encryption Standard \(AES\) a differenza del WEP e del WPA che utilizzano l'RC4.

WPA è progettato per utilizzare lo standard IEEE 802.1x per gestire l'autenticazione dei client e dei server e la distribuzione di differenti chiavi per ogni utente, sebbene per questioni di compatibilità supporti la precedente gestione a chiave condivisa \(PSK\). I dati sono cifrati con l'algoritmo di cifratura a flusso RC4 con chiave a 128 bit e vettore di inizializzazione a 48 bit.

In aggiunta all'autenticazione e alla cifratura, il WPA introduce notevoli miglioramenti nella gestione dell'integrità dei dati. Il CRC utilizzato dal WEP non era sicuro, era possibile modificare il messaggio mantenendo coerente il CRC, anche senza conoscere la chiave. Per evitare il problema, il WPA utilizza un nuovo metodo per verificare l'integrità dei messaggi chiamato "Michael". Questo include un contatore associato al messaggio per impedire all'attaccante di ritrasmettere un messaggio che sia già stato trasmesso nella rete.

In sostanza il WPA aumenta la dimensione della chiave, il numero delle chiavi in uso, include un sistema per verificare l'autenticità dei messaggi migliore e quindi incrementa la sicurezza della WLAN, rendendola effettivamente analoga a quella di una rete su cavo. La Wi-Fi Alliance \(il gruppo che gestisce lo standard Wi Fi\) ha dichiarato che utilizzerà il termine WPA2 per identificare i dispositivi che avranno il pieno supporto dello standard IEEE 802.11i.

Nel corso del 2008 sono stati mostrati degli attacchi in grado di compromettere l'algoritmo WPA e nel 2009 dei ricercatori hanno dimostrato di essere in grado di forzare una connessione WPA in 60 secondi. Questo attacco è stato eseguito in particolare sul metodo WPA-PSK \(TKIP\) di cifratura. Il metodo WPA2-AES è attualmente immune a questa vulnerabilità, e rimane l'ultimo sistema standard, che non richieda server di autenticazione, resistente ad attacchi potenzialmente pericolosi.

Wi-Fi Alliance ha introdotto i termini WPA\(2\)-Personal e WPA\(2\)-Enterprise per differenziare le due classi di sicurezza fornite dai prodotti. I WPA\(2\)-Personal utilizzeranno il metodo PSK a chiave condivisa mentre i WPA\(2\)-Enterprise utilizzeranno un server di autenticazione.

