# Cookies

I cookies HTTP (più comunemente denominati Web cookie, tracking cookie o semplicemente cookie) sono righe di testo usate per eseguire autenticazioni automatiche, tracciatura di sessioni e memorizzazione di informazioni specifiche riguardanti gli utenti che accedono al server, come ad esempio siti web preferiti o, in caso di acquisti via internet, il contenuto dei loro "carrelli della spesa".

Nel dettaglio, sono _stringhe di testo di piccola dimensione_ inviate _da un server ad un Web client_ (di solito un browser) e poi _rimandati indietro dal client al server_ (senza subire modifiche) ogni volta che il client accede alla stessa porzione dello stesso dominio web. Il termine __cookie__ "letteralmente __biscotto__" deriva da magic cookie (biscotto magico), concetto noto in ambiente UNIX che ha ispirato sia l'idea che il nome dei cookie HTTP.

Ogni dominio o sua porzione che viene visitata col browser può impostare dei cookie. Poiché una tipica pagina Internet, ad esempio quella di un giornale in rete, contiene oggetti che provengono da molti domini diversi e ognuno di essi può impostare cookie, è normale ospitare nel proprio browser molte centinaia di cookie.

## Caratteristiche

Un cookie è un header aggiuntivo presente in __una richiesta (Cookie:)__ o __risposta (Set-cookie:)__ HTTP: nel caso il server voglia assegnare un cookie all'utente, lo aggiungerà tra gli header di risposta.

- il client deve notare la presenza del cookie e memorizzarlo in un'area apposita
    - in genere, si utilizzava una directory dove ogni cookie veniva memorizzato in un file
    - attualmente i cookies sono gestiti in maniera molto più evoluta, in un unico file, per esempio Mozilla e Chrome usano SQLite
- il cookie è composto da:
    - una stringa di testo arbitraria
    - una data di scadenza (oltre la quale non deve essere considerato valido)
    - un pattern per riconoscere i domini a cui rimandarlo
    - modalità di accesso che serve a rendere invisibile un cookie da un linguaggio di scripting (ad esempio)
    - un flag che indica se il cookie può essere trasmesso in maniera non sicura
- è possibile impostare più cookie in una sola risposta HTTP.

Il browser client __rimanderà il cookie__, senza alcuna modifica, allegandolo a _tutte le richieste HTTP che soddisfano il pattern_, entro la _data di scadenza_. Il server può quindi scegliere di assegnare il cookie di nuovo, sovrascrivendo quello vecchio. Il reinvio tramite pattern permette a tutti i sottodomini di un dato dominio di ricevere il cookie, se così si vuole.

## A cosa servono

I cookie vengono utilizzati per __aggiungere uno stato ad un protocollo privo di stato__. Senza i cookie non vi sarebbe differenza in una pagina caricata prima di effettuare un login, dalla stessa pagina caricata dopo. Dato che i cookie permangono nel sistema per lunghi periodi, __i siti possono assegnare un indice all'utente e tenere traccia della sua navigazione all'interno del sito, solitamente allo scopo di creare statistiche__.

I cookie possono essere utilizzati anche per __tracciare la navigazione su siti terzi__, nel caso in cui questi siti terzi utilizzino contenuti provenienti dal sito che ha impostato il cookie. Solitamente la pubblicità sui siti viene gestita da compagnie che hanno inserzioni su svariati siti internet.

Il contenuto della pubblicità stessa viene caricato direttamente dal loro server (tramite una richiesta http) e visualizzato in maniera integrata nel sito che l'utente desidera visitare. In questo modo il server della compagnia pubblicitaria riceverà dal browser dell'utente l'indirizzo della pagina che si sta visualizzando, e potrà inviare un cookie al client. Tramite questo meccanismo le società pubblicitarie possono creare profili personalizzati per gli utenti e mostrare loro pubblicità mirate.
