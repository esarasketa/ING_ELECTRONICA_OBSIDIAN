#APLICADA_1 

En base a [[Configuraciones de circuitos transistores|como se conecta el transistor]] el modelo equivalente cambia ligeramente. Eh aquí:

# BJT

## Emisor Común


## Base Común
![[Pasted image 20261119132030.png]]
Los parámetros en esta configuración son:
+ $\boxed{hib=\frac{hie}{hfe}}$     Resistencia de Entrada $R_{i}$, Ohms
+ $\boxed{hob=\frac{hoe}{hfe}}$     Conductancia de Salida, Siemens o "$\mho$"
+ $\boxed{hfb\approxeq \frac{hfe}{hfe}\approxeq 1}$    Ganancia del Transistor en Señal

Partiendo del circuito típico, "desarmado"

![[Base Comun Desarmado.png]]
Puenteamos las fuentes de DC y los capacitores. Esto, efectivamente, elimina la presencia de $R_1$ y $R_{2}$.
![[Base Comun Modelo.png]]

### Ganancia $A_{vs}$
$\boxed{A_{vs}=\frac{R_{iA}}{R_{iS}}\cdot \frac{R_{oS}}{R_{i}}}$


## Colector Común

>[!warning] Buffer
>Esta configuración no tiene ganancia de tensión! Como se ve, tiene un solo parámetro, la resistencia de entrada $hie$. Es un modelo/config. que aparenta más simple, a precio de una $A_v \approxeq 1$ 
>Sin embargo, la alta $A_I$ y la conexión real entre $B$ y $E$ significa que el calculo de resistencias aparentes se complejiza un poco. Thread carefully.

![[Colector Comun Equivalente.png]]

+ $\boxed{hie}$     Resistencia de Entrada $R_{i}$, Ohms, de la hoja de datos.

![[Colector Comun Desarmado.png]]
### Resistencias 
Este modelo "sufre" de dos complejidades. La primera es la conexión real en el modelo. $hie$ conecta la base y el emisor, por lo que las resistencias pueden "mirar" a través del modelo del transistor. La $R_i$ siente a la $R_E$ y a la $R_L$.

Segundo, si aplicamos Ley De Ohm para obtener las resistencias, como por ejemplo $R_i$, utilizando $V_i=h_{ie}I_B+I_E(R_E\parallel R_L)$, nos vamos a encontrar con que $R_i\approx h_{ie}+h_{fe}(R_E\parallel R_L)$

Por qué?
Porque la alta ganancia de corriente hace que las resistencias conectadas al emisor *parezcan* más multiplicadas, cuando las vemos desde la base.

+ $R_{i}=hie+hfe\cdot(R_{L}\parallel R_{E})$
+ $R_{iA}=R_{TH}\parallel R_{i}$
+ $R_{iS}=R_{S}+R_{iA}$

+ $R_{o}=\Large\frac{{hie+(R_{S}\parallel R_{TH})}}{hfe}$
+ $R_{oA}=R_{E}\parallel R_{o}$
+ $R_{oS}=R_{L}\parallel R_{oA}$

### Ganancia $A_{vs}$
$\boxed{A_{vs}=\Large\frac{R_{iA}}{R_{iS}}\cdot \frac{{hfe\cdot(R_{E}\parallel R_{L})}}{R_{i}}}$
