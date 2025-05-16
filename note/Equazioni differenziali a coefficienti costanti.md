---
connections:
  - "[[Equazioni Differenziali]]"
source:
  - Prof. Ezio Bileci
---

# 2° Ordine

##### Omogenee
$$ay'' + by' + cy = 0$$

Per risolvere questa equazione dobbiamo prima risolvere l'equazione di secondo grado $φ(λ) = aλ^2 + bλ + c$

##### Primo metodo
se $Δ > 0$ allora  $λ = λ_1 \ e \ λ_2$  ----->  $y=C_1e^{λ_1x} + C_2e^{λ_2x}$

##### Secondo metodo
se $Δ = 0$ allora $λ = λ_0$ -----> $y = C_1e^{λ_0x} + C_2xe^{λ_0x}$



##### Non omogenea
$$ay'' + by' + cy = h(x)$$

1. Si risolve l'omogenea associata 
$$ay'' + by' + cy = 0$$
2. Trovare l'integrale particolare









es. $$3y'' - y' - 2y = 4x^2 - 3x + 2$$$3y'' - y' -2y = 0$ 
$3t^2 -t -2 = 0$
$t={1 +-\ 5}/{6}$
$y_h(x) = C_1 e^{x} + C_2 e^{-\frac{2}{3}x}$
$y_p(x) = Ax^2 + Bx + C$
$y_p{\prime} = 2Ax + B$ 
$y_p{\prime}{\prime} = 2A$
$3(2A) - (2Ax + B) - 2(Ax^2 + Bx + C) = 4x^2 - 3x + 2$
$(-2A)x^2 + (-2A - 2B)x + (6A - B - 2C) = 4x^2 - 3x + 2$
$\frac{24 + 7}{2} - 2C = 2 \Rightarrow -\frac{31}{2} - 2C = 2 \Rightarrow -2C = \frac{35}{2} \Rightarrow C = -\frac{35}{4}$
$y_p(x) = -2x^2 + \frac{7}{2}x - \frac{35}{4}$
$y(x) = y_h(x) + y_p(x) = C_1 e^{x} + C_2 e^{-\frac{2}{3}x} - 2x^2 + \frac{7}{2}x - \frac{35}{4}$


2 es.

$$
\begin{cases}

y{\prime}{\prime} + 10y{\prime} + 25y = 9x + 16 \\

y(0) = -2 \\

y{\prime}(0) = 4

\end{cases}
$$
risolviamo prima $y{\prime}{\prime} + 10y{\prime} + 25y = 0$
$y_h(x) = (C_1 + C_2 x)e^{-5x}$
$y_p(x) = Ax + B$
$y_p{\prime} = A$
$y_p{\prime}{\prime} = 0$
$0 + 10A + 25(Ax + B) = 9x + 16 \Rightarrow 25A x + (10A + 25B) = 9x + 16$
$\frac{18}{5} + 25B = 16 \Rightarrow 25B = 16 - \frac{18}{5} = \frac{80 - 18}{5} = \frac{62}{5} \Rightarrow B = \frac{62}{125}$
$y_p(x) = \frac{9}{25}x + \frac{62}{125}$
$y(x) = (C_1 + C_2 x)e^{-5x} + \frac{9}{25}x + \frac{62}{125}$

