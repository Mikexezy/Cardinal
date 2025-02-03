---
connections:
  - "[[Regressione logistica]]"
source:
  - https://developers.google.com/machine-learning/crash-course/logistic-regression/loss-regularization?hl=it
---
In un modello di regressione logistica il tasso di variazione del modello non è costante, come possiamo notare infatti la curva della [[Funzione sigmoidea]] è a forma di S e non è lineare.

---

Se usiamo una perdità lineare più ci avviciniamo allo 0 o all'1, più la memoria che il calcolatore deve utilizzare per recepire i cambiamenti aumenta.

![[linearlossinregressionelogistica.png]]

---
$$Log\ Loss=\sum{}_{(x, y)\in{D}}{\ -y \log{(y')}-(1-y)\log{(1-y')}}$$
dove:

- $(x,y)\in{D}$ è il set di dati contenente molti esempi etichettati, che sono $(x,y)$ coppie.
- $y$ è l'etichetta in un esempio etichettato. Poiché si tratta di regressione logistica, ogni valore di $y$ deve essere 0 o 1.
- $y′$ è la previsione del modello (da 0 a 1), in base alla serie di funzionalità in $x$.