---
connections:
  - "[[Tecniche - ML]]"
source:
  - https://developers.google.com/machine-learning/crash-course/linear-regression?hl=it
---
Tecnica utilizzata per trovare le relazioni matematiche che collegano le features alle label (caratteristiche ed etichette).

---

> [!esempio]
> Supponiamo di avere un set di dati formato dal peso di varie auto come features e dai km percorsi per litro di carburante.
> ![[scatterplotesempio.png]]
> Questo sarebbe il grafico scatter plot risultante, con la retta che rappresenta il nostro modello.
>
>Possiamo scrivere l'equazione della rete come $$y = mx + b$$, dove:
>
 >$y$ corrisponde ai km percorsi per litro di carburante.
 >$m$ corrisponde alla pendenza della retta.
 >$x$ corrisponde al peso della vettura, che diamo in input.
 >$b$ corrisponde all'intercetta y (bias).
 >

 Per realizzare un modello di regressione lineare questa formula diventerebbe 
 $$\dot{y} = b + w_1 + x_1$$, dove:
 
 $\dot{y}$ corrisponde al valore previsto come output del modello. 
 ($y$ nella formula algebrica dell'esempio)

 $b$ corrisponde al [[Pregiudizio - ML]], ovvero uno dei parametri del modello, che calcoliamo durante la fase di addestramento.  
 ($b$ nella formula algebrica dell'esempio)
 
 $w_1$ corrisponde al [[Peso - ML]], ovvero uno dei parametri del modello, che calcoliamo durante la fase di addestramento.
 ($m$ nella formula algebrica dell'esempio)

 $x_1$ corrisponde alle features.
($x$ nella formula algebrica dell'esempio)

---

Se invece abbiamo un modello con più caratteristiche, 5 per l'esempio, l'equazione diventerebbe
$$\dot{y} = b + w_1x_1 + w_2x_2 + w_3x_3 + w_4x_4 + w_5x_5$$
![[esempioequazioneregressionelineareconmulticaratteristiche.png]]

Se prendiamo a coppie la label con una qualsiasi delle caratteristiche possiamo osservare lo scatter plot che ne viene fuori e notare come le varie relazioni abbiano dei pattern diversi.

#### Esempi
![[esempioregressionelineareconmulticaratteristiche1.png]]
![[esempioregressionelineareconmulticaratteristiche2.png]]
![[esempioregressionelineareconmulticaratteristiche3.png]]