---
connections:
  - "[[Iperparametri - ML]]"
source:
  - https://developers.google.com/machine-learning/crash-course/linear-regression/hyperparameters?hl=it
---
Il tasso di apprendimento è quel valore che noi usiamo per aggiustare i nostri pesi e bias che hanno una pendenza negativa ([[Discesa del gradiente]]).

#### Come scegliere questo valore ?

Questo valore non deve essere ne troppo alto, ne troppo basso, ma bisogna ricercare la soluzione migliore.

1. Nel primo caso, con un tasso di apprendimento troppo basso il modello non riuscirebbe a convergere rapidamente, effettuando dei miglioramenti molto lenti nel tempo.

	![[tassodiapprendimentobassoesempio.png]]

2. Nel secondo invece, il modello non riuscirebbe mai a convergere, infatti la perdità non smetterebbe mai di oscillare a causa del grande valore.

	![[tassodiapprendimentoaltoesempio.png]]