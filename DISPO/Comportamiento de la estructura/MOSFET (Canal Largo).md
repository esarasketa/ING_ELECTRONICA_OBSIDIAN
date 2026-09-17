---
tags:
  - DISPO
---

### Tensión Umbral $V_T$
El primer concepto a introducir para entender el funcionamiento del MOSFET.
Llamamos $V_T$ a el valor de $V_G$ para el cual la estructura MOS del transistor pasa de funcionar en depleción a crear la zona de inversión, el canal.
	Para  $V_G \leq V_T$, hay muy pocos $e^-$ y el circuito actúa como un interruptor abierto 
	Para  $V_G > V_T$, se induce el canal de inversión con $e^-$ libres.
		A mayor $V_G$, el canal se vuelve más ancho, dando a mas $e^- \to$ más conductancia.

##### Polarización del Drenaje
En cualquier punto dado, el ancho del canal está determinado por la diferencia de potencial entre el gate ($V_G$) y ese punto ($V_{GC}$). Para que el canal permanezca abierto, $V_{GC} > V_T$ .

Partiendo de que  $V_G > V_T$, analizamos el comportamiento del canal bajo polarización $V_D$


* Con $V_D = 0$, hay un equilibrio térmico en el canal, y no existe corriente de drain $I_D$
![[Pasted image 20260518142420.png]]
 ^330c8c
* Con Con $V_D$ positiva, el canal comienza a actuar como un resistor simple, y la corriente $I_D$ es proporcional a $V_D$ .
  De esta forma, podemos pensar que el canal queda definido como $V_G - V_{DS} > V_T$
![[Pasted image 20260518143652.png]]
		Como podemos ver, cerca del Source, $V_G - V_{DS} = V_G$ ya que $V_{DS} = 0$, pero más cerca del drain, el canal se ve achicado por el "combate" entre las tensiones. 
		Esta zona de operación la conocemos como "Region Lineal"
		A medida que $V_D$ aumenta, la perdida de movilidad reduce la pendiente (Que antes era lineal) de $I_D$ 
 ^2381cd

* Finalmente, llega un punto en el que $V_G - V_{DS} < V_T$, cuando esto ocurre, entramos en la zona de "pinch off" (literalmente zone de pellizque), donde el canal se ve cortado por la pelea de tensiones.
  Es este el fin del canal araña?
![[firefox_c2PtrUDcwE.png]]
		No! Por más que el canal se haya cortado, existe ahora un campo eléctrico entre el canal y el terminal D, a través de la zona de depleción! 
		Una vez que ocurre el pinch off, la corriente $I_D$ deja de crecer, y se vuelve cte. queda *saturada*.
		A partir de este punto, un valor de $V_D$ que llamamos $V_{D_{SAT}}$  , y llamamos a la distancia desde el "pinch off" hasta el drain, $\Delta L$. 
		

 Claramente, la distancia desde el "pinch off" hasta el drain, $\Delta L$, es mucho menor que la longitud del canal, $L$. Eso deja de ocurrir en el Canal Corto.

![[firefox_A1OaIly1SS.png]]
En este grafico fachero se puede ver la zona lineal **(A)**, la zona entre $V_D$ y $V_{D_{SAT}}$ , y la zona de pinch off en adelante **(B)**.
Y también se puede ver la siguiente deducción. Cuanto más grande es $V_G$, más grande sera $I_D$ en función de $V_D$ , respetando la misma curva! Osea, que podemos controlar la corriente de salida, sin tocar la tensión de entrada! 

##### Curva de corriente
Estas curva de arriba se obtienen de la siguiente manera.

Sabemos que la carga $Q$ en la estructura MOS proviene de la capacidad total y la caída de tensión, pero también sabemos que para que el MOS se comporte como capacitor, necesitamos alcanzar $V_T$ Por lo que podemos reescribir: 
$Q = C\cdot (V_{GC} - V_T)$ 
	Con $V_{GS}$ siendo la diferencia de tensión entre el canal y la compuerta.

Tambien sabemos que la corriente $I_D$ tiene que ser la carga $Q$ que atraviesa el plano en un tiempo $\Delta T$, y sabemos que el tiempo no es más que la distancia, en nuestro caso la longitud $L$ del canal, y la velocidad de los portadores. Esta $V_Q$ no es más que el campo eléctrico $\cdot$ la movilidad efectiva $\bar{\mu_n}$ .

$I = \frac{Q}{\Delta t}$ ;  $\Delta t = \frac{L}{v_Q}$ ;  $v_Q = \bar{\mu_n} \cdot E$

${\Large I_D = C \cdot \frac{(V_{GC} -V_T)}{L} \cdot v_Q}$ 

${\Large I_D = C \cdot \frac{(V_{GC} -V_T)\cdot \bar{\mu_n} E}{L}}$ 

Adicionalmente, recordando la formula clásica de la capacidad, $\LARGE C = \frac{A\cdot \epsilon_{ox}}{t_{ox}}$
Definimos area $A$ como el ancho en el eje $Z \cdot L$ y la longitud, y nos avivamos de que [[Capacidad y Carga#^75ba71|la capacidad del oxido]] $C_{ox}$ está definida ahí!

$\LARGE I_D = \frac{Z\cdot L \cdot \epsilon_{ox}}{t_{ox} \cdot L} \cdot \mu E \cdot(V_{GC}-V_T)$ y notamos que la longitud se cancela!!

$\LARGE I_D = {Z \cdot C_{ox}} \cdot \mu E \cdot(V_{GC}-V_T)$ 

Ahora, nos enfocamos en el campo eléctrico. Como vemos en [[MOSFET (Canal Largo)#^330c8c|los diagramas]], el campo eléctrico horizontal depende de la tensión $V_D$ desde el *Source* hasta el *Drain*. $E= \frac{V_{DS}}{L}$ 

$\LARGE I_D = {Z \cdot C_{ox}} \cdot \mu \frac{V_{DS}}{L} \cdot(V_{GC}-V_T)$  reorganizado para separar las tensiones...
$\LARGE I_D = \frac{{Z \cdot C_{ox}} \cdot \mu }{L}\cdot V_{DS}(V_{GC}-V_T)$ 

Ahora, recordando que [[MOSFET (Canal Largo)#^2381cd|el canal se comporta de forma resistiva]] una vez que aparece $V_D$:![[firefox_eDDNT0vY4e.png]]
Podemos plantear $V_C$ como un divisor resistivo, $\large V_C =\frac{V_S+V_D}{2}$ y podemos usar un truco matemático, añadir 0.

$\large V_C =\frac{V_S}{2}+\frac{V_D}{2} + (\frac{V_S}{2}-\frac{V_S}{2})$ recordando que $V_{GC} = V_G - V_C$

Entonces:

$\LARGE I_D = \frac{{Z \cdot C_{ox}} \cdot \mu }{L}\cdot V_{DS}[V_G-(V_S + \frac{V_D}{2}-\frac{V_S}{2})-V_T]$ 

Finalmente, la formula para la corriente, previo a saturación, y con $V_G \ge V_T$ es:

**$\LARGE I_D = \frac{{Z \cdot C_{ox}} \cdot \mu }{L}\cdot [(V_{GS}-V_T)V_{DS} - \frac{{V_{DS}}^2}{2}]$**

[Y como esto es una cuadrática](https://www.desmos.com/calculator/wizeekx7wh), podemos sacar que su valor máximo, que coincide con $I_{D_{SAT}}$ es:

**$\LARGE I_{D_{sat}} = \frac{{Z \cdot C_{ox}} \cdot \mu }{2L}\cdot (V_{GS}-V_T)^2$**


Esta grafica de DESMOS también es muy útil para otro apartado, la [[Respuesta en Frecuencia]]

Cabe destacar, que dada la no idealidad del MOS, en $V_G < V_T$  la corriente no es $0$ , sinó que existe una pequeña $I_{D_{subdermal}}$ por medio de difusión desde el *Source* hacia el *Drain*.

