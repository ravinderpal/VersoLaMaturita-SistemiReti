# Crittografia

**Simmetrica** o **Asimmetrica** \(quest'ultima è più moderna e sicura\)

**Asimmetrica**: si basa su due chiavi, una privata e una pubblica

### Operazioni

* Codificare: testo in chiaro &gt; testo codificato
* Decodificare: testo codificato &gt; testo in chiaro

Le operazioni sono basate su algoritmo e chiave

**L'algoritmo è pubblico!**

La sicurezza è data da:

* Segretezza della chiave
* Robustezza dell'algoritmo

## Crittografia asimmetrica

Una chiave per codifica, una per la decodifica

Ogni utente ha

* Chiave privata: segreto da custodire
* Chiave pubblica: informazione da diffondere

Entrambe sono usabili per codificare o decodificare Di solito \(algoritmo RSA\) usano chiavi 1024-2048 bit \(circa 160-320 cifre decimali\) e sono lenti

### Segretezza

C'è un mittente e un destinatario: il mittente codifica il messaggio e lo manda al destinatario, che lo decodifica e lo legge Il mittente codifica il messaggio tramite la chiave pubblica del destinatario, e il destinatario usa la sua chiave privata per decodificare

Esistono sistemi a cascata: il mittente codifica il messaggio tramite chiave privata del mittente poi lo codifica ancora usando la chiave pubblica del dest. Spedisco e il dest usa la chiave privata per decodificare e poi ridecodifica con chiave pubblica del mittente.

### Attacchi crittografici

1. Brute Force
2. Cyphertext only: noto solo il testo crittografato
3. Known plaintext: noto il testo in chiaro
4. Chosen plaintext: testo in chiaro scelto

### Protocolli vulnerabili

telnet, ssh, ftp, snmt\(p\), ntp, smtp, imap pop3

