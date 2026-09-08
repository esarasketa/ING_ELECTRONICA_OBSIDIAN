---
tags:
  - DIGITALES_1
---
Un tipo de [[Contador en Anillo]], el contador Johnson agrega una compuerta **NOT** a la salida del último $q$. 

>[!example] Ejemplo con 3 Flip-Flops
>![[Pasted image 20260908134432.png]]
>### Sus ecuaciones de transferencia son entonces:
>
$q_{next}(0)=\overline{q_{reg}(2)}$
$q_{next}(1)=q_{reg}(0)$
$q_{next}(2)=q_{reg}(1)$
>
>| **$q_{2}$** | **$q_{1}$** | **$q_{0}$** |     | **$q*_{2}$** | **$q*_{1}$** | **$q*_{0}$** |
| ----------- | ----------- | ----------- | --- | ------------ | ------------ | ------------ |
| $0$         | $0$         | $0$         |     | $0$          | $0$          | $1$          |
| $0$         | $0$         | $1$         |     | $0$          | $1$          | $1$          |
| $0$         | $1$         | $0$         |     | $1$          | $0$          | $1$          |
| $0$         | $1$         | $1$         |     | $1$          | $1$          | $1$          |
| $1$         | $0$         | $0$         |     | $0$          | $0$          | $0$          |
| $1$         | $0$         | $1$         |     | $0$          | $1$          | $0$          |
| $1$         | $1$         | $0$         |     | $1$          | $0$          | $0$          |
| $1$         | $1$         | $1$         |     | $1$          | $1$          | $0$          |
>### Diagrama de estados:
>
![[Pasted image 20260908193207.png]]
>
Notamos que existe una secuencia preferencial (la grande xd) y una espuria, que alterna entre $010$ y $101$
>
El modulo de este contador es, por ende, $6$. 

