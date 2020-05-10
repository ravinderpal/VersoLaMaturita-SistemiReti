# VLAN

Permette di separare logicamente gli host in unità organizzative diverse, simulando delle reti locali separate \(da qui Virtual\) che si trovano però sulla stessa rete locale fisica.

**Tipi di VLAN**

* V-Lan _tagged_ 802.1q
  * viene applicato modificando il frame ethernet
  * esiste un sottopacchetto 802.1q che contiene le informazioni per la rete locale virtuale
* V-Lan _untagged_ \(port based\)
  * basata sulle porte ethernet fisiche e non su quelle TCP/UDP
  * lo switch programmabile deve supportare VLAN

**Comunicazione**

* Stessa VLAN
  * comunicano tramite switch
* VLAN diversa
  * devono avere un router per comunicare tra di loro

**NAT:** Network Address Translation

* permette di vedere dall'esterno tanti dispositivi come fossero uno solo

## Tagged VLAN

* TPI \(Tag Protocol Identifier\)
* TAG
  * EtherType

**Trunk:** connessione punto-punto tra due porte _trunk_ di uno switch.

**VTP:** protocollo Cisco per configurazione VLAN

