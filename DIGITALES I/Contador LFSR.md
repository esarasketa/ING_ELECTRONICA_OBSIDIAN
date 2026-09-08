---
tags:
  - DIGITALES_1
---
Partiendo del [[Contador en Anillo]], el contador $LFSR$, o ***"Linear Feedback Shift Register"*** es un tipo de contador *pseudo-aleatorio*.

Su principio de funcionamiento se basa en conectar la primera entrada $p$ a una compuerta $XOR$. 
La misma puede estar conectada a cualquiera de las salidas $q$.

>[!example] Ejemplo: 4 Flip-Flops, 0-15.
>![[Pasted image 20260908152142.png]]
>### Ecuaciones de transición
>$q_{next}(0)=(q_{reg}(2)\oplus q_{reg}(3))$
>$q_{next}(1)=q_{reg}(0)$
>$q_{next}(2)=q_{reg}(1)$
>$q_{next}(3)=q_{reg}(2)$
>
> La tabla de verdad es un tanto engorrosa de hacer, pero podemos obtener una secuencia de valores, si tomamos cada Flip-Flop com un digito binario.
> Empezando en $(1000);8$, la secuencia seguiría la siguiente logica.
> $\{8,1,2,4,9,3,6,13,10,5,11,7,15,14,12,8,\dots\}$
> Notamos como una vez que volvemos al $8$, la secuencia se repite.

Notemos que si cambiamos el punto de inicio, igualmente llegamos a la misma secuencia, pero desplazada.

El modulo de estos contadores se define como $2^w-1$, con $w$ siendo el largo de la palabra. Esto ocurre porque $\{0\}$ no es parte de la serie. 





