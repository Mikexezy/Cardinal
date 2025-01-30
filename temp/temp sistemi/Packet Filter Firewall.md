---
connections:
  - "[[Firewall]]"
source:
  - 978-88-7485-756-2
---
Questa categoria di firewall lavora nei livelli [[Transport - TCP IP]] e [[Network - TCP IP]], sono molto veloci perché il controllo avviene solamente nei pochi byte di header senza occuparsi dell’applicazione che genera effettivamente il pacchetto.

Questo vuol dire che se un email contiene una possibile minaccia, come un virus, quest'ultima non verrà rilevata dal firewall che non interverrà in nessun modo.

>[!ricorda]
>Se questa tipologia di firewall vengono collegati alla fonte possono gestire l'intera rete locale.

All'interno dell'header vengono controllati determinati campi:
- Indirizzo ip di origine
- Indirizzo ip di destinazione,
- Numero della porta [[TCP]] / [[UDP]] di origine 
- Numero della porta TCP / UDP di destinazione
- Protocollo usato nel livello superiore