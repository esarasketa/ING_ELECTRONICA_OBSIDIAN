---
tags:
  - DIGITALES_1
---

Definimos contador a un circuito secuencial que almacena y cuenta. Como cuenta? Que cuenta?
Generalmente los impulsos de una señal. Esta señal puede ser el clock. En cual caso el contador simplemente nos informa de cuantas ciclos de $CLK$ han transcurrido.

En su forma más simple, podemos ver al contador como un [[Flip-Flop#flip-flop tipo D|flip flop-tipo D]], y un sumador $+1$.
![[Pasted image 20260907181352.png]]
Su ecuación de transición es simplemente ${q_{next}}={q_{reg}}+1$

| $q_{next}$ | $q_{reg}$ |
| ---------- | --------- |
| 000        | 001       |
| 001        | 010       |
| 010        | 011       |
| 011        | 100       |
| 100        | 101       |
| 101        | 110       |
| 110        | 111       |
| 111        | 000       |
# Terminal Count
Si bien el circuito ya se resetea de forma automática al llegar al $W = 11\dots11$, al contador se le suele agregar un comparador, el cual "avisa" cuando se alcanzó el valor máximo de la palabra de longitud $W$.

# Entrada de habilitación
Si bien puede ser que queramos usar el circuito para contar pulsos del clock, también es igualmente plausible que no. Aparece entonces la gloriosa entrada de habilitación. Se trata de agregar un mux de tamaño $W$.

El mux, básicamente, elige si se suma o si se mantiene $q_{reg}$ 

Hasta ahora, tendríamos un contador así:
![[Pasted image 20260907184813.png]]

---
# Reset sincrónico y contador de módulo M
Si en vez de utilizar el mux para enable, conectamos una de sus entradas a $00\dots00$, y el selector del mux a el comparador, obtenemos un reset forzado una vez alcanzamos el valor máximo de la palabra.

PERO! Si en vez de poner el comparador en la palabra máxima, ponemos un valor anterior, obtenemos lo llamado **Contador de Módulo M**, donde $M$ es un valor entre $00\dots00$ y $11\dots11$. Lo que se obtiene en este caso, es que el contador se resetee al alcanzar un número menor al máximo de la palabra.

>[!example] Contador de Módulo 5
>![[Pasted image 20260907185322.png]]
>Así nomás. Cuando el circuito alcanza $5$, se resetea. Incluso sabiendo que el máximo con una palabra de $W=3$ es $7$

---

A partir de este modelo básico, aparecen una serie de contadores más complejos.

De los vistos en la catedra de Simone:
+ [[Contador en Anillo]]
	+ [[Contador Johnson]]
+ [[Contadores#Reset sincrónico y contador de módulo M|Contador Binario]]
+ [[Contador LFSR|LFSR - Linear Feedback Shift Register]]

| CONTADOR       | Anillo | Johnson    | LFSR     | Binario |
| -------------- | ------ | ---------- | -------- | ------- |
| Módulo         | $w$    | $2\cdot w$ | $2^w -1$ | $2^w$   |
| Caso en 4 bits | 4      | 8          | 15       | 16      |
