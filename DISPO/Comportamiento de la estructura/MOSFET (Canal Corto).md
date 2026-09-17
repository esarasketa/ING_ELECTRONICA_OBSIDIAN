---
tags:
  - DISPO
---
Como el ser humano es avaricioso como la mierda,
El scaling lleva a reducir el tamaña del MOSFET hasta puntos donde el canal se vuelve comparable, igual, si no mayor que la profundidad $X$.
Que significa esto? GG a la aproximación de canal gradual, hola a una barbarie de problemas, ahora que nuestro canal es directamente dependiente del $E$.

A grandes rasgos, ocurre lo siguiente:
+ $\large V_T \cancel{=}cte$   Ahora la tensión umbral se reduce por $L$
+ $\large I_D$ ya no se satura en  $\large V_D$ (recordar los gráficos de saturación)
+  $\large I_D$ no es proporcional a  $\large 1/L$
+ El dispositivo se degrada con el uso, mucho más notablemente que en Canal Largo.


Pero, puntualmente, podemos destacar estos problemas.

# Modificación de $\Large V_T$
Para llegar a inversión, es decir, formar el canal; El substrato primero debe atravesar una zona de depleción. Esto ya lo sabemos.
Pero ahora, nos avivamos de lo siguiente! Al rededor de los terminales, *ya hay zonas de depleción*.
En canal largo, estas representaban una fracción del area del canal.
En canal corto, un porcentaje importante del canal *ya se encuentra en depleción* incluso antes de polarizar! Por lo que necesitas una $V_T$ menor para crear el canal.

Solución:
+ Óxido más fino, menos óxido = más $C_{ox} \to$ más control del gate.
+ Reducir la profundidad de los terminales
	+ Esto vuelve las ZCE más pequeñas, pero aumenta la resistencia serie, lo que cambia las curvas de corriente, pipipipi.
+ Dopar más fuerte al substrato.
	+ Lleva a ZCE más pequeñas, pero recordamos que sobre-dopar el substrato aumenta la cantidad de colisiones, y reduce la movilidad.

# Efecto Parasito BJT
Parece ahora, que el bicho es *TAN* chico, que las ZCE de los terminales se solapan.
Esto significa que aparece una corriente $S\to D$ por debajo del canal, que aumenta de forma cuadrática. (wtf)
Esto puede ser terrible, ya que crea lo conocido como efecto "punch through"
	El $E$ del Drain acelera los carriers hasta su nivel de "hot carriers", los cuales colisionan contra la red, provocando pares $h^+|e^-$.
	**Problema**: Los $e^-$ se van al Drain, pero los $h^+$ se van al sustrato! Aumentado la diferencia de potencial.
	Esto, si nos abstraemos, recuerda a un bias NPN.
	Entonces, $I_D$ crece muchísimo.
	Vamos, que avalancha.

Cuando pasa esto, el gate pierde cualquier tipo de control sobre la corriente de salida.

Solución:
### LDD
Lightly Doped Drain
Básicamente, una zona al lado del terminal Drain y el canal, que absorbe los hot carriers, y dispersa el campo eléctrico.
Como consecuencia, tenemos que entender que una zona menos dopada trae más resistencia serie.

# Drain Induced Barrier Lowering
Nombre largo, para lo que efectivamente es, que el campo $E$ del Drain, eventualmente alcanza el Source, bajando la barrera de energía muy brutamente. Electrones con menos energía de repente pueden permitirse un viaje por la zona de depleción, encontrando que la corriente de Sub-Umbral incrementó, junto a una disminución de $V_T$
Solución?
Y, si el problema viene del campo $E$ del Drain... correcto. **[LDD]**


# Hot Carriers
El mismo malvado campo $E$ que acelera los hot carriers tiene la culpa.
En este caso, lo que ocurre es que los hot carriers pueden superar la barrera del $Si/SiO_2$.
Cuando pasa esto, cargas quedan atrapadas en la capa de óxido amorfo, lo cual aumenta $V_T$ y degrada $g_m$.
			En canal largo, la corriente la limita la movilidad de los portadores.
			Sin embargo, en canal corto, se limita por un mecanismo físico.
			La "Saturación de Velocidad" ocurre cuando un campo $E$ energiza a los carriers hasta un punto, en el que los mismos comienzan a emitir fonones. 
			Entiéndase, que a suficiente energía cinética, la partícula libera esa energía como una vibración en la red, conocida como fonon.
			A efectos prácticos, esto es una nueva velocidad limite, que limita $I_D$ .

Solución?
You won't believe it. Its..! **[LDD]**