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

# Tipologie di perdità

- [[Perdita L1]]
- [[Perdita L2]]
- [[MAE - Errore assoluto medio]]
- [[MSE - Errore quadratico medio]]

>[!esempio]
>Abbiamo un veicolo dal peso di 1,07 t (feature) che consuma 12,8 km/l (label).
>Il nostro modello ha un bias casuale di 20 e un peso casuale di -2, quindi effettuiamo il seguente calcolo:
>
>$$label=bias+(weight*feature)$$
>$$label=20+(-2*1,07)=20-2,14=17,8\ km/l$$
>\
>\
>Quindi adesso calcoliamo la perdita L2
>
>$$valore\ effettivo=12,8\ km/l\ \ ,valore\ previsto=17,8\ km/l$$
>
>$$perdita\ L2=(valore\ effettivo-valore\ previsto)^2$$
>$$perdita\ L2=(12,8-17,8)^2=25$$
>
 

#### Come scegliere la tipologia di perdita da utilizzare

Questa decisione dipende molto dal nostro [[Set di dati - ML]] e dal tipo di previsioni che vogliamo effettuare.
In base ai nostri dati infatti potremmo avere più o meno [[Outlier]], delle vere e proprie anomalie, che vanno processati dando loro la giusta d'importanza a seconda dei nostri obiettivi. 

| ![[esempiomse.png]] | ![[esempiomae.png]] |
| ------------------- | ------------------- |
| perdita MSE         | perdita MAE         |
Come possiamo notare:

- MSE penalizza maggiormente gli errori più grandi perché eleva al quadrato la differenza tra la previsione e il valore reale. Questo significa che:
	
	3. È molto sensibile agli outlier: errori grandi hanno un impatto maggiore sulla funzione di perdita.
	2. Il modello tende a “spostarsi” verso gli outlier, cercando di minimizzare anche gli errori estremi.
	1. Utile se gli outlier sono effettivamente significativi e non solo rumore nei dati.

- MAE invece prende il valore assoluto dell’errore, trattando tutti gli errori in modo lineare. Questo significa che:

	1. È meno sensibile agli outlier, quindi il modello ignorerà anomalie e si concentrerà maggiormente sulla previsione della maggior parte dei dati.
	2. Gli errori piccoli e grandi vengono pesati in modo uguale.
	3. Utile se gli outlier sono dovuti a errori di misurazione o sono rumore indesiderato.