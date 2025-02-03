---
connections:
  - "[[Machine Learning]]"
source:
  - https://developers.google.com/machine-learning/crash-course/logistic-regression?hl=it
---
La regressione logistica è un potente strumento di machine learning utilizzato per risolvere problemi di [[Classificazione binaria]], ovvero quando dobbiamo decidere se un input appartiene a una di due categorie possibili. 
Un esempio classico è proprio la classificazione delle email come "spam" o "non spam".

### Come Funziona

1. Si parte da un modello lineare, simile a quelli usati nella regressione lineare. Questo modello cerca di trovare una relazione lineare tra le variabili di input (ad esempio, le parole presenti nell'email, la presenza di determinati caratteri, ecc.) e un valore numerico.
    
2. La regressione logistica introduce una funzione speciale chiamata [[Funzione sigmoidea]]. Questa funzione "schiaccia" il valore numerico prodotto dal modello lineare in un intervallo compreso tra 0 e 1. Questo valore può essere interpretato come la probabilità che l'input appartenga a una delle due categorie.
    
3. Per decidere a quale categoria assegnare l'input, si introduce una soglia di classificazione. Se la probabilità calcolata dalla funzione sigmoide è maggiore o uguale a 0.5, l'input viene classificato in una categoria (ad esempio, "spam"), altrimenti viene classificato nell'altra categoria (ad esempio, "non spam").

---

Queste non sono solamente le uniche differenze che distinguono un modello di regressione logistica da un modello di regressione lineare, un modello logistico differisce anche nel 
calcolo della perdita, e dall'aggiunta di una funzione in grado di prevenire l'[[Overfitting]].

- [[Log Loss]]
- [[Regolarizzazione]]



