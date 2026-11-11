#APLICADA_1 

>[!tip] No son componentes, para que las quiero??
Más allá de que te las van a pedir en el parcial, estas resistencias son clave a la hora de parametrizar un diseño y al momento de realizar conexiones en cascada.
Muchas veces saber cual de estos valores está "fallando" puede simplificar muchísimo el re-diseño de un amplificador, y varias veces los propios requisitos de diseño van a delatar estos valores, inmediatamente caracterizando al sistema y facilitando el diseño.
El ejemplo más claro es como facilitan el [[Ganancia de Tensión|calculo de las ganancias.]]

### Resistencias de Entrada
* $\LARGE R_{i}$   Resistencia de Entrada
* $\LARGE R_{iA}$   Resistencia de Entrada al Amplificador 
* $\LARGE R_{is}$   Resistencia de Entrada al sistema

### Resistencias de Salida
* $\LARGE R_{o}$   Resistencia de Salida
* $\LARGE R_{oA}$   Resistencia de Salida al Amplificador 
* $\LARGE R_{os}$   Resistencia de Salida al sistema

---

# Obtención 

Partiendo del circuito equivalente de un BJT en configuración Emisor Común. [[Modelo de parámetros híbridos#Modelo Simplificado|Referencia.]]

![[SIMPLIFICADO 3.png]]
Lo primero que se puede hacer, es unir las resistencias $R_1$ y $R_2$, ya que no solo están en paralelo, sinó que también las usamos en paralelo para el Análisis de DC.

![[RESISTENCIAS.png]]


![[RESISTENCIAS 2.png]]

# $R_i$   Resistencia de Entrada
Es lo que "se ve" hacia adentro del circuito equivalente.
	$\boxed{R_{i}=h_{{ie}}}$
# $R_{iA}$   Resistencia de Entrada al Amplificador
Es lo que "se ve" hacia adentro del amplificador, incluidas las $R$ de polarización. 
	$\boxed{R_{i}=R_{BB}\parallel h_{{ie}} \equiv R_{BB}\parallel R_{i}}$

# $R_{is}$   Resistencia de Entrada al Sistema
Es lo que "se ve" hacia adentro del sistema entero, incluido todo. 
	$\boxed{R_{i}=R_{S}+ (R_{BB}\parallel h_{{ie}}) \equiv R_{S}+ R_{iA}}$


# $R_o$   Resistencia de Entrada
Es lo que "se ve" hacia adentro del circuito equivalente.
	$\boxed{R_{o}=\frac{1}{\Large h_{oe}}}$
# $R_{oA}$   Resistencia de Entrada al Amplificador
Es lo que "se ve" hacia adentro del amplificador, incluida la $R$ de colector. 
	$\boxed{R_{0}=R_{C}\parallel \frac{1}{\Large h_{oe}} \equiv R_{C}\parallel R_{o}}$
# $R_{os}$   Resistencia de Entrada al Sistema
Es lo que "se ve" hacia adentro del sistema entero, incluido todo. 
	$\boxed{R_{i}=R_{L}\parallel R_{C}\parallel \frac{1}{\Large h_{oe}} \equiv R_{L}\parallel R_{oA}}$
	