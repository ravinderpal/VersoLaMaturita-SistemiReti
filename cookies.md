#Cookies

I cookies HTTP (più comunemente denominati Web cookie, tracking cookie o semplicemente cookie) sono righe di testo usate per eseguire autenticazioni automatiche, tracciatura di sessioni e memorizzazione di informazioni specifiche riguardanti gli utenti che accedono al server, come ad esempio siti web preferiti o, in caso di acquisti via internet, il contenuto dei loro "carrelli della spesa".

Nel dettaglio, sono stringhe di testo di piccola dimensione inviate da un server ad un Web client (di solito un browser) e poi rimandati indietro dal client al server (senza subire modifiche) ogni volta che il client accede alla stessa porzione dello stesso dominio web. Il termine "cookie" – letteralmente "biscotto" – deriva da magic cookie (biscotto magico), concetto noto in ambiente UNIX che ha ispirato sia l'idea che il nome dei cookie HTTP.

Ogni dominio o sua porzione che viene visitata col browser può impostare dei cookie. Poiché una tipica pagina Internet, ad esempio quella di un giornale in rete, contiene oggetti che provengono da molti domini diversi e ognuno di essi può impostare cookie, è normale ospitare nel proprio browser molte centinaia di cookie.

#Caratteristiche
Un cookie è un header aggiuntivo presente in una richiesta (Cookie:) o risposta (Set-cookie:) HTTP: nel caso il server voglia assegnare un cookie all'utente, lo aggiungerà tra gli header di risposta. Il client deve notare la presenza del cookie e memorizzarlo in un'area apposita (in genere, si utilizzava una directory dove ogni cookie veniva memorizzato in un file, Attualmente i cookies sono gestiti in maniera molto più evoluta, in un unico file, per esempio Mozilla e Chrome usano SQL - SQLite). Il cookie è composto da una stringa di testo arbitraria, una data di scadenza (oltre la quale non deve essere considerato valido) e un pattern per riconoscere i domini a cui rimandarlo. È possibile impostare più cookie in una sola risposta HTTP.

Il browser client rimanderà il cookie, senza alcuna modifica, allegandolo a tutte le richieste HTTP che soddisfano il pattern, entro la data di scadenza. Il server può quindi scegliere di assegnare il cookie di nuovo, sovrascrivendo quello vecchio. Il reinvio tramite pattern permette a tutti i sottodomini di un dato dominio di ricevere il cookie, se così si vuole.

I cookie vengono utilizzati per aggiungere uno stato ad un protocollo privo di stato. Senza i cookie non vi sarebbe differenza in una pagina caricata prima di effettuare un login, dalla stessa pagina caricata dopo. Dato che i cookie permangono nel sistema per lunghi periodi, i siti possono assegnare un indice all'utente e tenere traccia della sua navigazione all'interno del sito, solitamente allo scopo di creare statistiche.

I cookie possono essere utilizzati anche per tracciare la navigazione su siti terzi, nel caso in cui questi siti terzi utilizzino contenuti provenienti dal sito che ha impostato il cookie. Solitamente la pubblicità sui siti viene gestita da compagnie che hanno inserzioni su svariati siti internet.

Il contenuto della pubblicità stessa viene caricato direttamente dal loro server (tramite una richiesta http) e visualizzato in maniera integrata nel sito che l'utente desidera visitare. In questo modo il server della compagnia pubblicitaria riceverà dal browser dell'utente l'indirizzo della pagina che si sta visualizzando, e potrà inviare un cookie al client. Tramite questo meccanismo le società pubblicitarie possono creare profili personalizzati per gli utenti e mostrare loro pubblicità mirate.

#Come sono fatti i cookies
Contrariamente a quanto comunemente si crede, un cookie non è un piccolo file di testo: può essere sì memorizzato in un file di testo, ma non necessariamente. Nel cookie solitamente possiamo trovare sei attributi:

Nome/valore è una variabile ed un campo obbligatorio.
Scadenza (expiration date) è un attributo opzionale che permette di stabilire la data di scadenza del cookie. Può essere espressa come data, come numero massimo di giorni oppure come Now (adesso) (implica che il cookie viene eliminato subito dal computer dell'utente in quanto scade nel momento in cui viene creato) o Never (mai) (implica che il cookie non è soggetto a scadenza e questi sono denominati persistenti).
Modalità d'accesso (HttpOnly) rende il cookie invisibile a javascript e altri linguaggi client-side presenti nella pagina.
Sicuro (secure) indica se il cookie debba essere trasmesso criptato con HTTPS.


#Dominio e percorso
Il dominio (domain) e il percorso (path), definiscono l'ambito di visibilità del cookie, indicano al browser che il cookie può essere inviato al server solo per il dominio e il percorso indicati. Se non specificati, come predefiniti prendono il valore del dominio e del percorso che li ha inizialmente richiesti. 
