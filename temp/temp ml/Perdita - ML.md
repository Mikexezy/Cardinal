---
connections:
  - "[[Parametri - ML]]"
source:
  - https://developers.google.com/machine-learning/crash-course/linear-regression/loss?hl=it
---
La perdità è una media numerica che ci dice quanto siano sbagliate le previsioni del nostro modello, praticamente misura la distanza tra le previsioni del modello e le etichette effettive.

Il nostro modello durante la fase dell'[[Addestramento - ML]] ha come obiettivo quello di minimizzare la perdità al valore più piccolo possibile.

![[perditaesempio.png]]

La perdità misura effettivamente la differenza tra i valori previsti e quelli effettivi, concentrandosi sulla distanza e non sulla direzione.

>[!esempio]
>Se un modello prevede 2, ma il valore effettivo è 5 quindi la differenza sarà 
>$$(2-5)=-3$$
>Però come abbiamo detto prima la perdità si concentra sulla distanza e non sulla direzione, quindi sostanzialmente al perdità sarà il valore assoluto della differenza:
>$$p=3$$


---

#### Tipologie di perdità
- [[Perdita L1]]
- [[Perdita L2]]
- [[MAE - Errore assoluto medio]]
- [[MSE - Errore quadratico medio]]



