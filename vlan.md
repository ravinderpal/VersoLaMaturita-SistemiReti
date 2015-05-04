# VLAN

Permette di separare logicamente gli host in unità organizzative diverse, simulando delle reti locali separate (da qui Virtual) che si trovano però sulla stessa rete locale fisica.

__Sul Libro__: pag 2-3

- V-Lan _tagged_ 802.1q
  - viene applicato modificando il frame ethernet
  - esiste un sottopacchetto 802.1q che contiene le informazioni per la rete locale virtuale

- V-Lan _untagged_ (port based)
  - basata sulle porte ethernet fisiche e non su quelle TCP/UDP
  - lo switch programmabile deve supportare VLAN

- __Comunicazione__
  - Stessa VLAN
    - comunicano tramite switch
  - VLAN diversa
    - devono avere un router per comunicare tra di loro

__NAT:__ Network Address Translation
  - permette di vedere dall'esterno tanti dispositivi come fossero uno solo

## Tagged VLAN

- TPI (Tag Protocol Identifier)
- TAG
  - EtherType

__Trunk:__ connessione punto-punto tra due porte _trunk_ di uno switch.

__VTP:__ protocollo Cisco per configurazione VLAN