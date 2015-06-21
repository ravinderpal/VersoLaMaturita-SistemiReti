# VPN

Una VPN (virtual private network) è una rete di telecomunicazioni privata, instaurata tra soggetti che utilizzano, come infrastruttura di trasporto, un sistema di trasmissione pubblico e condiviso, come ad esempio la rete Internet. Scopo delle reti VPN è offrire alle aziende, a un costo inferiore, le stesse possibilità delle linee private in affitto ma sfruttando reti condivise pubbliche: si può vedere dunque una VPN come l'__estensione, a scala geografica, di una rete locale privata aziendale che colleghi tra loro siti interni all'azienda stessa variamente dislocati su un ampio territorio__, sfruttando l'instradamento tramite IP per il trasporto su scala geografica e realizzando di fatto una rete LAN, detta appunto virtuale e privata, logicamente del tutto equivalente a un'infrastruttura fisica di rete (ossia con collegamenti fisici) appositamente dedicata.

Le principali peculiarità di una VPN sono:
- __Economicità__: la scelta di una implementazione adeguata in fase di progetto permette di scegliere la soluzione più adeguata al miglior costo sostenibile;
- __Semplicità__: grazie allo sviluppo di diversi protocolli la tecnologia è fortemente semplice da implementare;
- __Sicurezza__: Il traffico passante viene comunemente crittografato aumentando conseguentemente la sicurezza della connessione.


## Caratteristiche

Tramite una connessione VPN ci si può "collegare" ad un server come se si fosse fisicamente (cavo di rete o interfaccia wireless) connessi. La connessione si svolge attraverso un tunnel "virtuale" (protetto e sicuro) supportato da internet esattamente come fosse il cavo fisico abituale. In questo modo si possono utilizzare le solite risorse di rete abituali: cartelle, sistemi informatici gestionali, posta elettronica aziendale, ecc. 

Le VPN possono essere implementate attraverso i sistemi operativi comuni (Windows, Linux, Android, iOS, Mac OS, ecc.) oppure tramite software di terze parti (esempio: Cisco VPN client) che permette configurazioni più complesse e gestibili.

Le __reti VPN utilizzano collegamenti che necessitano di autenticazione in modo da garantire l'accesso ai soli utenti autorizzati__; per garantire la sicurezza che i dati inviati in Internet non siano intercettati o utilizzati da altri non autorizzati, le reti utilizzano sistemi di crittografia.

Le reti VPN sicure adottano dunque protocolli che provvedono a cifrare il traffico transitante sulla rete virtuale. Oltre alla cifratura, una VPN sicura deve prevedere nei suoi protocolli dei meccanismi che impediscano violazioni della sicurezza, come ad esempio il furto dell'identità digitale o l'alterazione dei messaggi.

Nelle VPN c’è in genere un __firewall tra il computer del dipendente__ o di un cliente __e il terminale__ della rete o __del server__. Il dipendente, per esempio, quando stabilisce la connessione con il firewall, deve autenticare i dati che vuole trasmettere, passando attraverso un servizio di autenticazione interno.

La maggior parte dei programmi client richiede che tutto il traffico IP della VPN passi attraverso un _Tunnel_ virtuale tra le reti utilizzando Internet come mezzo di collegamento. 

## I protocolli

Le __Secure VPN__ utilizzano __protocolli crittografici__ a tunnel per offrire l’__autenticazione del mittente__ e l’__integrità del messaggio__, allo scopo di difendere la privacy. Una volta scelte, implementate e usate, alcune tecniche possono fornire comunicazioni sicure su reti non sicure.

Le tecnologie delle Secure VPN dovrebbero essere utilizzate come _security overlay_ attraverso infrastrutture di rete dedicate.

I protocolli che__ implementano una VPN sicura__ più conosciuti sono:

- __IPsec (IP security)__ comunemente usate su IPv4 (parte obbligatoria dell'IPv6).
- __PPTP (point-to-point tunneling protocol)__ sviluppato da Microsoft.
- __SSL/TLS__ utilizzate sia per il “Tunneling” dell’intera rete, come nel progetto OpenVPN, o per assicurarsi che sia essenzialmente un Web Proxy. L'SSL è un framework, molto spesso associato con il commercio elettronico, che s'è rivelato di grande flessibilità ed è quindi usato come strato di sicurezza per varie implementazioni (più o meno standard) di reti private virtuali.
- __VPN Quarantine__ la macchina del cliente terminale della VPN potrebbe essere una fonte di attacco, cosa che non dipende dal progetto della VPN. Ci sono soluzioni che forniscono servizi di VPN Quarantine che controllano il computer remoto. Il cliente viene tenuto in quarantena fino a che l'infezione non sia stata rimossa.
- __MPVPN (Multi Path Virtual Private Network)__ un trademark registrato di proprietà della Ragula System Development Company.

Molte ISPs ora offrono __un servizio VPN per aziende__ che vogliono la sicurezza e la convenienza di un VPN. Oltre a fornire ai dipendenti remoti un accesso sicuro alla rete interna, a volte vengono inclusi altri servizi di sicurezza e gestione.
Questi meccanismi non implementano di per sé una rete virtuale, ma solo un colloquio sicuro tra due terminali. In questi casi il meccanismo di rete virtuale deve essere realizzato mediante un protocollo apposito che viene poi incapsulato. Esiste oggi un discreto numero di approcci alternativi (ed ovviamente mutualmente incompatibili) a questo schema, tra i quali possiamo citare i seguenti.

- __Protocollo SOCKS__: questo approccio è il più "standard", in quanto SOCKS è uno standard IETF per Generic Firewall Traversal definito nella RFC 1928.

__OpenVPN__ mette a disposizione un eseguibile che crea un tunnel cifrato con un'altra istanza del medesimo programma su un computer remoto, e può trasportare l'intero stack __TCP/IP__.

Un altro approccio molto usato utilizza il __protocollo SSH__, che è in grado, come OpenVPN, di __creare dei tunnel tra due macchine collegate__. Questa caratteristica è nata per trasportare XWindow, ma è stata implementata in modo generale, ed è quindi __possibile utilizzarla per trasportare un protocollo qualsiasi__. Una implementazione molto diffusa, in quanto open source e gratuita, è OpenSSH.
L'approccio di ormai tutti i fornitori di firewall è invece quello di usare TLS per rendere sicura la comunicazione con un proxy al quale si accede via browser. Il canale cifrato viene realizzato in realtà generalmente tramite un'applet Java od un oggetto ActiveX, che quindi può essere installata in modo quasi trasparente per l'utente finale. La conseguente facilità di gestione fa sì che questo approccio sia particolarmente apprezzato nelle organizzazioni complesse.
Alcune reti VPN sicure non usano algoritmi di cifratura ma partono dal presupposto che un singolo soggetto fidato gestisca l'intera rete condivisa e che quindi l'impossibilità di accedere al traffico globale della rete renda i singoli canali sicuri dato che il gestore della rete fornisce ad ogni soggetto solamente la sua VPN.

I protocolli che utilizzano questa filosofia includono:

* L2F (Layer 2 Forwarding), sviluppato da Cisco.
* L2TP (Layer 2 Tunnelling Protocol), sviluppato in collaborazione tra Microsoft e Cisco.
* L2TPv3 (Layer 2 Tunnelling Protocol version 3). Le Trusted VPNs non usano un “Tunneling” crittografico e invece contano sulla sicurezza di una singola rete di provider per proteggere il traffico. In un certo senso, questa è un’elaborazione di una rete tradizionale.
Multi Protocol Label Switching (MPLS) è spesso usato per costruire una Trusted VPN.

### LibreSwan

LibreSwan è un fork di OpenSwan realizzato per poterne continuare lo sviluppo. Il software offre un'implementazione completa di __IPSec__ per il kernel __Linux__. IPSec permette di utilizzare crittografia asimmetrica a _livello 3_ del modello __OSI__.

__IPSec:__

- opera in _tunnel mode_ o _transport mode_:
    - _tunnel mode_ crittografa un'intero pacchetto
    - _transport mode_ crittografa solo il payload
- usa SHA1 e SHA2 per controlli d'integrità
- usa AES e 3-DES per crittografia

### L2TP

- utilizza UDP

Fornisce quattro differenti modelli di tunnelling, tra cui:

- voluntary tunnel
- compulsory tunnel: incoming dial o remote dial
- multihop connection
