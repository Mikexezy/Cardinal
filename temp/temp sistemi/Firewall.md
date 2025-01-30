---
connections:
  - "[[Sistemi e Reti]]"
source:
  - 978-88-7485-756-2
---
Il firewall è una linea di difesa che si occupa di filtrare i pacchetti che dalla rete locale LAN escono verso la rete pubblica WAN.
Per poter usare un firewall bisogna necessariamente avere nella propria rete un [[Gateway]].

> [!ricorda]
> Il software che si occupa della gestione del firewall può essere incluso nell'hardware del router o in alcuni casi risiedere su un hardware esterno.

Firewall di alto livello vengono usati per proteggere la rete da svariati [[Attacchi informatici]] che provengono sia dall'interno che dall'esterno.

![[firewall.png]]
 
 ---

In base al livello dello [[Stack TCP IP]] in cui opera, il firewall può distinguersi in 3 categorie:

- [[Application Level Firewall]]
- [[Packet Filter Firewall]]
- [[Stateful Packet Inspection Firewall]]

---

In un firewall la configurazione è basata su un meccanismo di [[ACL]]
