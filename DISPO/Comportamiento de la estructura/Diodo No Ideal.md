---
tags:
  - DISPO
---
# Caídas de tensión 
En la practica, todo material tiene resistencia.
En la juntura P-N concebimos de una conductividad, por lo que si o si debe existir una resistividad (Gracias, ohm)
Y la resistividad es obviamente resistencia, a lo largo de un volumen.
Por lo cual, la curva real de tensión se ve algo así:
![[firefox_I3Sbgbdnp3.png|300]]
Teniendo en cuenta las $R_n$ y $R_p$
### Modulación de la res. por polarización
Aumentar la corriente en función de la tensión aumenta las caídas en las zonas neutras. Pero! Los excesos reducen la resistividad. (Recordamos los gráficos de corriente en función a los excesos) 
Entonces? Más contaminación (hasta un punto) reduce este efecto, pero hay que tener en cuenta todo lo que esto significa para la movilidad, ya que a mayor contaminación los eventos de perturbación carrier-ión son significantes.

# $G(T)$ y $R(T)$ en la zona de carga espacial
En simples términos, $J_p$  y $J_n$ no son cte. en la ZCE.
La ZCE real tiene electrones y lagunas dentro, que se inyectan desde las zonas neutras por el malvado campo $E$.
El Tremosa directamente dice "Esto es una mierda, no obedece leyes predecibles por lo cual no lo incluimos en la ley de corriente del diodo. Puta madre."
![[firefox_ojJKjux0k5.png|450]]


# Corrientes de fuga sobre las superficies de juntura
Esto es un teaser de [MOS](obsidian://open?vault=DISPO&file=Materiales%2C%20Estructuras%2FEstructura%20MOS)
En la superficie de la juntura, existen capas delgadas de $SiO_x$, óxido de silicio, un aislante.
Esto crea trampas de carga, caminos para que los carriers escapen de la estructura.
A efectos prácticos, esto produce una corriente inversa comparable a $I_S$, a veces incluso mayor.
En directa, ni se nota, pero en inversa es muy evidente.

# Ruptura por Polarización Inversa Excesiva 
A partir de un punto muy elevado de tensión, la tensión de Zener $V_Z$, el campo eléctrico se vuelve tan poderoso sobre los electrones, que puede comenzar a provocar efectos túnel, arrancando a los electrones de sus orbitales. 
Esto da lugar a un grafico comiquísimo.
![[firefox_PihczSd7DN.png|350]]

El Diodo Zener, un diodo que aprovecha esta propiedad, trabaja en inversa, con un valor $V_Z$ que puede alcanzar los $1000$s de $V$, forzando la corriente a quedarse en un valor definido.


# Capacidades 
En la practica, ya que se estableció que la ZCE no tiene ningún tipo de carga móvil, que existe una distribución de carga en la estructura.

## Capacidad de Juntura $C_j$
Se trata de una capacidad dinámica, es decir, que varía en función de la tensión, cosa que un cap normal no hace.

La definimos a partir de la derivación clásica de capacidad

$\Large C_{juntura }= \frac{dQ}{dv}$ 

$\Large C_j= \frac{dQ}{d(\varphi_0-v)}\to  C_j=\frac{-A\epsilon}{\ell}$ 
Y acá vemos lo siguiente, en directa, donde $\ell$ se achica, habrá más $C_j$ , mientras que en inversa, donde esta crece, habrá menos $C_j$

Uno diría, joya! Si quiero un VariCap (capacitor variable) lo uso en directa!
Nope! Lo usas en inversa. Porque en directa, aparece, una capacidad mucho mayor, [TITLE CARD].

## Capacidad de difusión $C_D$
En directa, aparece un nuevo fenómeno de acumulación de carga. Al bajar la barrera de potencial, permitimos que los portadores se difundan entre las zonas neutras. Este breve exceso de minoritarios afuera de la zona de depleción, justo antes de que se recombinen, se la conoce como capacidad de difusión.
La $C_D$ es notablemente más fuerte que la $C_j$ en directa.


En síntesis:
	$C_j \to$ Directa $\downarrow\ell  \to C_j\uparrow$  
	$C_j \to$ Inversa $\uparrow\ell  \to C_j\downarrow$  
		Relación Lineal
	$C_D \to$ Directa $\to C_j\uparrow\uparrow\uparrow$  
	$C_D \to$ Inversa $\to C_D \approx 0$  
		Relación Exponencial


---

