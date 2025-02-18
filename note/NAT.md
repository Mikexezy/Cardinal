---
connections:
  - "[[Firewall]]"
source:
  - Prof. Rosamaria Barone
---
La NAT permette ad una rete locale, con classe di indirizzi privata, di accedere ad internet usando un solo indirizzo IP fornito dall'[[ISP]].

Usa una tabella contenente tutte le corrispondenze fra i [[Socket]] interni e quelli esterni.

Unica limitazione del NAT è la gestione 1:1 tra IP server e IP client, quindi se arriva una seconda richiesta per lo stesso server di destinazione, il router non è in grado di gestirla.

Il NAT presenta 3 funzionalità:
- [[Static NAT]]
- [[Dynamic NAT]]
- [[PAT]]
