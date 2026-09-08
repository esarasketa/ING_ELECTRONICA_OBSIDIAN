---
tags:
  - TEORIA_DE_CIRCUITOS_1
---

Esta nota explica como efectuar cambios entre [[Impedancia]] y [[Admitancia]].

Trabajando en circuitos RLC complejos, es posible encontrar ramas cuyos componentes se encuentren en serie, y al mismo tiempo, ramas enteras en paralelo, o viceversa. 

Debido a que la Impedancia y la admitancia permiten sumar en serie y en paralelo respectivamente, cambiar entre estos dominios es muy útil. Sin embargo, cuando queremos pasar de un dominio al otro, nos damos cuenta que tanto la parte real como la imaginaria intervienen en el cambio, por lo que el intercambio entre dominios no es tan sencillo como utilizar los valores obtenidos en el otro.

### Impedancia **$\rightarrow$** Admitancia  $(Z \rightarrow Y)$

$\LARGE G = \left( \frac{R}{R^2 + X^2} \right)$  y  $\Large B = \left( \frac{-X}{R^2 + X^2} \right)$

##### Como:
Partimos de:
	
$\Large Y = 1 / Z \quad\rightarrow\quad Y = \frac{1}{R + jX}$   Inmediatamente aparece el problema, la parte compleja y real se quedaron "pegadas" por medio de la inversión. No sirve.

Solución: Conjugado complejo.

$\Large Y = \frac{1}{R + jX} \cdot \frac{R - jX}{R - jX} \quad\quad\rightarrow\quad\quad$  $\Large \frac{R - jX}{R^2 - jRX + jRX - (jX)^2}$

Notá que $\pm jRX$ se cancelan mutuamente, y que $(jX)^2$ resulta en $j^2X^2$, y sabemos que $j^2 = -1$  !

Esto nos deja con:

$\Large Y = \frac{R - jX}{R^2 + X^2}$   Lo cual separamos por denominador en    $\Large Y = \left( \frac{R}{R^2 + X^2} \right) - j\left( \frac{X}{R^2 + X^2} \right)$

Y efectivamente:

 $\LARGE G = \left( \frac{R}{R^2 + X^2} \right)$  y  $\Large B = \left( \frac{-X}{R^2 + X^2} \right)$
***

### Admitancia **$\rightarrow$** Impedancia  $(Y \rightarrow Z)$

$\LARGE R = \frac{G}{G^2 + B^2}$   y    $\LARGE X = \frac{-B}{G^2 + B^2}$

Aplicando exactamente la misma lógica aritmética! 


## Gráficos típicos  

#TODO [Calculadora en DESMOS:](https://www.desmos.com/calculator/blytnvuz7o)

Una rama con un capacitor solitario y singular:![[Artboard 1@2x.png]]


Una rama con una resistencia y un inductor ***variable*** en serie.
![[L + R@2x.png]]