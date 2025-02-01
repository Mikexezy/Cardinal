---
connections:
  - "[[Discesa del gradiente]]"
  - "[[Dimensione del batch]]"
source:
  - https://developers.google.com/machine-learning/crash-course/linear-regression/hyperparameters?hl=it
---
La discesa stocastica del gradiente, SGD, utilizza una dimensione del batch uguale ad 1, ovvero l'aggiornamento dei pesi e dei bias avviene dopo ogni singolo esempio.

>[!esempio] 
>In un dataset grande 1000 esempi i pesi ed i bias verranno aggiornati 1000 volte.

---

#### Cosa cambia ?

Come possiamo notare, l'uso di un approccio stocastico, aggiunge nella nostra curva di [[Perdita - ML]] un evidente rumore. 

> Non solo in prossimità della convergenza

![[discesastocasticadelgradiente.png]]