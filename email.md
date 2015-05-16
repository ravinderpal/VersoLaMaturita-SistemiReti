
#Sicurezza email: OpenPGP e S / MIME 

Inizialmente, con i primi protocolli e-mail, i server di posta elettronica utilizzavano principalmente  POP oppure IMAP - che sono di base dei protocolli plain text (in chiaro)-. Attualmente la maggior parte dei server supportano SSL per questi protocolli.
In questo modo Username e Password non vengono spediti in chiaro.
SMTP, il protocollo usato per la spedizione delle mail, può funzionare in modalità SMTPS (usando SSL) ma molti server di posta non utilizzano SMTPS quando comunicano tra di loro. In questo modo i messaggi inviati con SMTPS viaggiano su un canale crittografato per la maggior parte del percorso ma nell’ultima parte il messaggio risulta in chiaro (il server di destinazione è iim questo caso SMTP e non SMTPS)


La possibilità che i contenuti delle email possano essere letti in chiaro non è l’unico problema. Nel caso infatti una mail rimanesse sui server di GMAIL, HOTMAIL so su server MICROSOFT EXCHANGE tali email possono essere lette dal sistema di sicurezza internazionale e, se in USA, dal governo USA.

A questo punto è lecito chiedersi perché la crittografia mail non sia così diffusa, perché non la utilizzano tutti?
Le risposte possono essere diverse.. ma i metodi per la crittografia mail sono principalmente 2 e sono decisamente semplici da utilizzare.

###S/MIME

Ci sono due modi per cifrare o firmare i messaggi. Il primo utilizza S / MIME, un metodo molto simile alle connessioni SSL. Il modo in cui funziona è mediante l’utilizzo di un certificato digitale che viene rilasciato all’utente da un'autorità attendibile. Il protocollo attuale deriva dal formato dei dati PKCS # 7, e la maggior parte dei client di posta elettronica supporta S / MIME. Una volta che si ottiene un certificato, molti dei quali provengono da aziende come Comodo o InstantSSL, si scarica un file con estensione .p7s e si aggiunge alla vostra applicazione di posta elettronica. Questo metodo da la possibilità di firmare i messaggi per dimostrare che vengono dall’utente, a quel punto il destinatario riceverà un messaggio con un allegato: la firma dell’utente (.p7m) e può essere letto da qualsiasi client e-mail che supporta S / MIME.


L'intero processo è in genere abbastanza semplice e rende S MIME il modo / più trasparente per iniziare con la crittografia e-mail. Quando si richiede tale certificato a una delle autorità di certificazione (CA) è possibile scaricare il certificato direttamente dal sito, aggiungerlo al software di posta elettronica, e iniziare ad usarlo subito.

###PGP
La forma più popolare di crittografia sulla rete si chiama PGP o Pretty Good Privacy. A rigor di termini, il protocollo è OpenPGP e PGP è un programma commerciale che viene venduto per approfittare di crittografia e-mail. La maggior parte delle persone utilizzano invece GPG, la versione open source di PGP fatta da Gnu.


In molti casi PGP è simile a S / MIME. Entrambi utilizzano la crittografia a chiave pubblica. Tuttavia, con PGP non è necessario contare su un'autorità centrale. Basta creare una coppia di chiavi pubblica / privata utilizzando il software PGP. Questo lo rende un po 'più complesso per iniziare rispetto ad S/MIME. Basta andare sul sito web GPG in cui il codice sorgente e binari sono disponibili per varie piattaforme. Una volta installato, è necessario generare la propria chiave. Tuttavia, PGP ha anche il concetto di server chiave per consentire la distribuzione di chiavi. È possibile caricare la propria chiave pubblica su un server di chiavi e gli altri utenti possono quindi cercare tale chiave e scaricarla per inviare messaggi cifrati. 
Tuttavia, poiché le chiavi sono auto-generate, non c'è modo di sapere se una chiave è valida o meno. Si potrebbe creare una coppia di chiavi per qualsiasi indirizzo di posta elettronica che si possiede, ma nessuna autorità centrale la può convalidare. Questo è il motivo per cui PGP ha la nozione di key-signing parties: È possibile contattare amici che convalidare la chiave e firmare.
ATTENZINE: tutto questo è molto difficile da fare con servizi di posta elettronica web based. Non è possibile utilizzare i Gmail o Hotmail siti web per fare e-mail crittografate, perché la chiave privata dovrebbe risiedere sui loro server. Tuttavia, ci sono soluzioni alternative, come Mailvelope, che fa l'intero processo di crittografia in JavaScript, all'interno del tuo browser.
