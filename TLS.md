## TLS

Il protocollo __TLS__ consente alle applicazioni _client/server_ di comunicare attraverso una rete in modo tale da prevenire il __tampering (manomissione)__ dei dati, la _falsificazione_ e l'_intercettazione_. È un protocollo standard definito nella __RFC 5246__, sviluppata sulla base del precedente protocollo __SSL__ da Netscape Communications.

Viene applicato principalmente nel 

- solo il _server_ si autentica al _client_: il client rimane invece anonimo (per quanto riguarda TLS).
- il _server_ viene autenticato confrontando il suo certificato con una __Certificate Authority__.
- un certificato generato a mano funziona per quanto riguarda l'aspetto crittografico di __TLS__, ma non è considerato valido dall'autenticazione perchè _non è verificato_ da una __Certificate Authority__.
- ogni _certificato valido_ lo è solo per i _domini_ per cui è stato verificato dalla __CA__.

In assenza di un'__autenticazione bilaterale__ (dove sia il client che il server si autenticano) si possono utilizzare i protocolli __TLS-PSK__ o __Secure remote password (SRP)__ per garantire un'autenticazione sicura in assenza di un certificato.
