# Windows Server

Ne esistono diverse versioni:

- Windows Server 2003
    - Enterprise Edition
    - Web Edition
- Windows Server 2008
- Windows Server 2008 R2
    - Standard
    - Enterprise
    - Datacenter

Offre le più comuni funzionalità normalmente richieste da un sistema server, tra cui __DNS__, __Web Server__ tramite Microsoft __IIS__, __DHCP__ Server, __Active Directory__, server di stampa e server __VPN__.

## Licenze

Microsoft Windows Server è conosciuto come un __overpriced piece of shit__ che nell'antica lingua inglese significa __sovrapprezzato pezzo di merda__ perchè richiede una quantità enorme di soldi per essere utilizzato ma soprattutto perchè __Microsoft si impegna per rendere più complicato possibile sapere quanti soldi ci vogliono per usarlo__.

Oltre alla licenza di __ogni singolo desktop__ e a quella del sistema operativo di __ogni singolo server__, per ogni applicativo sono richieste licenze aggiuntive chiamate __Client Access License__ che sono di vario tipo, tra cui:

- __per utente__: una CAL di questo tipo fornisce accesso a un singolo utente da ogni dispositvo
- __per dispositivo__: una CAL di questo tipo fornisce accesso a un dispositivo fisico da qualsiasi utente
- __per server__: una CAL di questo tipo fornisce accesso a un singolo server
    - definiscono quanti utenti possono accedere al server contemporaneamente

Quindi, per una rete sono solitamente necessarie licenze __per ogni installazione di Windows Server__, __per ogni installazione di Windows desktop__ e abbastanza __CAL__ da permettere il funzionamento degli applicativi.

## Active Directory

__AD__ è un protocollo che permette ai dispositivi con sistema operativo __Windows__ di condividere risorse tra cui: __account__, __files__, __periferiche__ (soprattutto stampanti) e dispositivi fisici.

__AD__ permette di organizzare totalmente i permessi di accesso per ogni risorsa e di dividerle in __unità organizzative__ e gestire facilmente l'appartenenza di multipli utenti a multipli __gruppi__.

### Dominio

Un dominio è un insieme di __risorse compatibili con Active Directory__ gestite da un __PDC (Primary Domain Controller)__.

- tutti i dispositivi fisici appartenenti a un dominio si autenticano con gli account di esso.
- il __PDC__ agisce da __autorità centrale__ per la gestione del dominio.
- le risorse sono organizzate __gerarchicamente__, usando una struttura ad __albero__
- consente la __replicazione multi-master__ che è semplicemente un eufemismo per dire che è possibile utilizzare multipli server per rendere la rete più stabile in caso uno di essi fallisca o sia sovraccarico
