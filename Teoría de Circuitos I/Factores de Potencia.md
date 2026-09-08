---
tags:
  - TEORIA_DE_CIRCUITOS_1
---
## Potencia Real $\LARGE P,$   $\LARGE P_{Activa}$ 

La potencia de toda la vida. Es la unidad de medición de "cuanta energía sale de la fuente y se convierte en otra cosa".
Este "otra cosa" puede ser calor/energía térmica, como en una resistencia, luz en una lamparita, etc.
La equivalencia watts / joules es 1:1. Por cada watt consumido, se entregó un joule.

Se mide en $\LARGE W$ watts.


## Potencia Reactiva $\LARGE P_Q,$   $\LARGE Q,$   $\LARGE P_{Reactiva}$

La potencia reactiva aparece por culpa de los capacitores e inductores, que trabajan con la energía de una forma distinta. ***La potencia reactiva es la medición de energía que está temporalmente "guardada" en el sistema.***

Un capacitor almacena energía en el primer semiciclo, y luego la devuelve en el siguiente.
El inductor, por su parte, crea un campo magnético cuando la corriente sube, y cuando la misma cae, el campo magnético se invierte.

La potencia reactiva existe porque incluso si la *energía neta es 0*, los movimientos de carga o campo siguen expresando fuerzas. Si bien **no hay un consumo**, la red eléctrica tiene que poder tanquear el movimiento de energía.

Se mide en $\LARGE VA\;r$, "Volts-Ampere reactivo"


## Potencia Aparente $\LARGE P_S,\;\; S,\;\; P_{Aparente}$

A raíz de la potencia reactiva, aparece un problema. La red eléctrica "no sabe" por adelantado si la energía que le circula es útil o si solo es un subproducto de los inductores y/o capacitores en su sistema. La fuente solo "ve" corriente y tensión.

Por ende, la fuente le suministra a la red $\LARGE S = V_{rms} \cdot I_{rms}$

Se mide en $\LARGE VA$, "Volts-Ampere"


## Relación de Impedancia
#### [[Impedancia]]
![Power Triangle and Power Factor in AC Circuits](https://www.electronics-tutorials.ws/wp-content/uploads/2025/10/power-triangle.jpg)

Ya que la potencia reactiva aparece en el eje imaginario, se pueden aplicar las relaciones trigonométricas que venimos usando desde el curso de ingreso.

$\LARGE P = V_{rms} \cdot I_{rms}\cdot cos(\upvarphi_z)$  y notamos que $\LARGE V_{rms} \cdot I_{rms}$  no es más que  $\LARGE S$  !
$\LARGE P = S\cdot cos(\upvarphi_z)$

De la misma mano,  $\LARGE Q = S\cdot sin(\upvarphi_z)$

Y gracias a un griego random: $\LARGE S^2 = P^2 + Q^2$


### Identidades complejas

####  $\LARGE P = G\cdot {V_{rms}}^2$ 
Definida la admitancia como $\large Y = G + jB, \;\; Y = 1/Z$  y con ley de ohm compleja $\large I = V/\left|{Z}\right|$ vemos como aparece la identidad $\large I = Y\cdot V$

Ahora, Potencia real $\large P$  no tiene componentes complejos, por lo cual $\large I_{real} = G \cdot V \rightarrow P = V_{rms} \  \left(G\cdot {V_{rms}}\right)$

En genérico:
$\large P = V \cdot I \cdot cos(\upvarphi)= I^2\cdot R=G\cdot V^2$


####  $\LARGE Q = -B\cdot {V_{rms}}^2$
Donde el signo representa la inversión del eje imaginario producto de la admitancia.

### $\LARGE Q = I^2 \cdot X$
