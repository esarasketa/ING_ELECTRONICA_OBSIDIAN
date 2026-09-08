---
tags:
  - DISPO
---


## Efectos capacitivos

La distribución de tensión en la estructura está dada así:

### $V_g = V_{ox} + \phi_s$

Dicho, la tensión aplicada al gate se divide entre la caída en el óxido y el potencial superficial en la interface Oxido-sm. Con $\phi_s$, o más precisamente,  $\phi_s * q$ es la cantidad de [[Potenciales variables#$ phi_s$ Potencial superficial|deformación de las bandas de energía]] y con $V_{ox}$ siendo la caída de tensión en el óxido.

Esto es importante, ya que $V_{ox} = - Q{s} / C_{ox}$
	con $Qs$ siendo la carga por unidad en el semiconductor. ^76400d

Asimismo, $C_{ox} = \epsilon_{ox} / t_{ox}$
	con $\epsilon_{ox}$ siendo la permitividad del material, y $t_{ox}$ siendo el espesor del oxido. ^75ba71

Siendo $C_{ox}$ una propiedad del material, es obvio que $Q_s$ es resultado de la tension en gate.

![[Pasted image 20260517191409.png]]
Entonces, vemos $Q_s$ , la suma entre la carga en la zona de inversión (Corta pero intensa) y la carga en la zona de depleción (Poca, pero extendida a lo largo de la zona de ancho $W_d$ )

Por la existencia de estas cargas, aparece con magnitud igual e inversa $Q_n$ o $Q_g$ , la carga en la compuerta/gate. 

El siguiente, es un diagrama con la capacidad a lo largo de los distintos modos de operación.

![[Pasted image 20260517192258.png]]

* Zona 1
	Acumulación, $C ≈ C_{ox}$ La estructura es prácticamente un capacitor, con el óxido siendo el dieléctrico, que no es muy gordo. 

* Zona 2
	Flat Band, $V_g = 0$, $C = C_{fb} < C_{ox}$ por las cargas de inversión 

* Zona 3
	Bajas frecuencias de AC, se reduce se crea una segunda interface, gracias a la zona de carga espacial generada. La capacidad es entonces paralela, con:
	$\frac{1}{C} = \frac{1}{C_{ox}} + \frac{1}{C_{depleción}}$
	Y a medida que crezca la zona de depleción, más va a caer la capacitancia total.
	-
	Si continua esto, se alcanza $C_{min}$ y comienza a actuar la inversión, hasta que se alcanza la inversión fuerte y se llega nuevamente a $C ≈ C_{ox}$

* Zona 3'
	En altas frecuencias, los portadores no "le pueden seguir el ritmo" al cambio en la AC. No se crea la capa de inversión, y la capacidad cae por debajo de $C_{min}$.
	En esta zona, la capacitancia es determinada por una $W_{depleción}$ maxima. 
	Si la frecuencia y el dispositivo lo permite, debido a la recombinación, la curva puede estabilizarse en $C'_{min}$ 
	Al tiempo que le tarda a la estructura en recuperarse y crear una capa de inversión térmica se lo determina "tiempo de retención".
	El hacer esta prueba, muestra varios detalles sobre la calidad del MOS.