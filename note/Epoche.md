---
connections:
  - "[[Iperparametri - ML]]"
source:
  - https://developers.google.com/machine-learning/crash-course/linear-regression/hyperparameters?hl=it
---
Durante l'addestramento il modello elabora tutti gli esempi del dataset in modo ciclico, ogni ciclo rappresenta effettivamente la nostra epoca.

>[!esempio]
>Se ad esempio abbiamo un dataset di 10 esempi, ed il modello ne elabora 40 vuol dire che saranno già passate 4 epoche.

---

Le epoche e la [[Dimensione del batch]] sono collegati fra loro:

- Se scegliamo un approccio tradizionale con una dimensione del batch pari al dataset intero, e l'addestramento avviene in 20 epoche, il nostro modello allora aggiornerà i pesi e i bias 20 volte.
- Se scegliamo un batch con dimensione pari a 1 singolo esempio ([[Discesa stocastica del gradiente]]), il nostro dataset contiene 100 esempi, allora in 20 epoche i pesi e i bias verranno aggiornati 2000 volte.
- Se scegliamo un batch con dimensione 10 ([[Discesa stocastica del gradiente in mini-batch]]), il nostro dataset contiene 100 esempi, allora in 20 epoche i pesi e i bias verranno aggiornati 200 volte.