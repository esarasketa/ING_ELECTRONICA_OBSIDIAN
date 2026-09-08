---
tags:
  - DIGITALES_1
---
La metaestabilidad es un estado o punto de equilibrio inestable entre los valores lógicos $1$ y $0$.

Suele ocurrir cuando a un flip-flop le llega un flanco de $CLK$ cuando en la entrada $d$ está ocurriendo una subida o bajada de flanco.

Esto deja al circuito en un estado de indeterminación, donde desde un punto de vista teórico, no sabemos el valor de la compuerta, es decir, comportamiento indeterminado.

Los efectos pueden variar desde la propagación de un valor erróneo, una demora en el tiempo de operación (lo cual puede "romper" el circuito más adelante, si el mismo cuenta con algún tipo de necesidad de sincronía), hasta que la compuerta guarde un valor "ilegal" entre $1$ lógico y $0$ lógico. (En lógica $3V3$, un valor de este tipo podría ser encontrar un $1.33V$ en la salida $q$) 