---
tags:
  - DIGITALES_1
---
El contador en anillo es un tipo de contador que se basa en el desplazamiento de bits. En su forma más simple se trata de varios Flip-Flop conectados en "serie" cuyos output $q$ también son interpretados como salidas del contador.

El contador en anillo tiene tantas salidas como Flip-Flops.

![[Pasted image 20260908124555.png]]
(salidas no diagramadas)

Al iniciarse este circuito, tiene que existir un $1$ en algún $q(n)$, el cual se ve propagado en cada ciclo de $CLK$.

Las ecuaciones de transición del contador en anillo son muy simples, por suerte.

$q_{next}(0)=q_{reg}(2)$
$q_{next}(1)=q_{reg}(0)$
$q_{next}(2)=q_{reg}(1)$

Y así sucesivamente. 

Para poder aplicar este contador, a veces es necesario utilizar un DECODER para obtener un valor numérico. 
