# Windows Server

Ne esistono diverse versioni:

* Windows Server 2003
  * Enterprise Edition
  * Web Edition
* Windows Server 2008
* Windows Server 2008 R2
  * Standard
  * Enterprise
  * Datacenter

Offre le più comuni funzionalità normalmente richieste da un sistema server, tra cui **DNS**, **Web Server** tramite Microsoft **IIS**, **DHCP** Server, **Active Directory**, server di stampa e server **VPN**.

## Licenze

Oltre alla licenza di **ogni singolo desktop** e a quella del sistema operativo di **ogni singolo server**, per ogni applicativo sono richieste licenze aggiuntive chiamate **Client Access License** che sono di vario tipo, tra cui:

* **per utente**: una CAL di questo tipo fornisce accesso a un singolo utente da ogni dispositvo
* **per dispositivo**: una CAL di questo tipo fornisce accesso a un dispositivo fisico da qualsiasi utente
* **per server**: una CAL di questo tipo fornisce accesso a un singolo server
  * definiscono quanti utenti possono accedere al server contemporaneamente

Quindi, per una rete sono solitamente necessarie licenze **per ogni installazione di Windows Server**, **per ogni installazione di Windows desktop** e abbastanza **CAL** da permettere il funzionamento degli applicativi.

## Active Directory

**AD** è un protocollo che permette ai dispositivi con sistema operativo **Windows** di condividere risorse tra cui: **account**, **files**, **periferiche** \(soprattutto stampanti\) e dispositivi fisici.

**AD** permette di organizzare totalmente i permessi di accesso per ogni risorsa e di dividerle in **unità organizzative** e gestire facilmente l'appartenenza di multipli utenti a multipli **gruppi**.

### Dominio

Un dominio è un insieme di **risorse compatibili con Active Directory** gestite da un **PDC \(Primary Domain Controller\)**.

* tutti i dispositivi fisici appartenenti a un dominio si autenticano con gli account di esso.
* il **PDC** agisce da **autorità centrale** per la gestione del dominio.
* le risorse sono organizzate **gerarchicamente**, usando una struttura ad **albero**
* consente la **replicazione multi-master** che è semplicemente un eufemismo per dire che è possibile utilizzare multipli server per rendere la rete più stabile in caso uno di essi fallisca o sia sovraccarico

