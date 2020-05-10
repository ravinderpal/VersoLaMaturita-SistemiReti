# TLS

Il protocollo **TLS** consente alle applicazioni _client/server_ di comunicare attraverso una rete in modo tale da prevenire il **tampering \(manomissione\)** dei dati, la _falsificazione_ e l'_intercettazione_. È un protocollo standard definito nella **RFC 5246**, sviluppata sulla base del precedente protocollo **SSL** da Netscape Communications.

Viene applicato principalmente nel protocollo HTTPS dove:

* solo il _server_ si autentica al _client_: il client rimane invece anonimo \(per quanto riguarda TLS\).
* il _server_ viene autenticato confrontando il suo certificato con una **Certificate Authority**.
* un certificato generato a mano funziona per quanto riguarda l'aspetto crittografico di **TLS**, ma non è considerato valido dall'autenticazione perchè _non è verificato_ da una **Certificate Authority**.
* ogni _certificato valido_ lo è solo per i _domini_ per cui è stato verificato dalla **CA**.

In assenza di un'**autenticazione bilaterale** \(dove sia il client che il server si autenticano\) si possono utilizzare i protocolli **TLS-PSK** o **Secure remote password \(SRP\)** per garantire un'autenticazione sicura in assenza di un certificato.

