---
tags:
  - DISPO
---
Como viste en [[MOSFET (Canal Largo)#Curva de corriente|el desarrollo de corriente de drenaje]], $I_D$ es una función de $V_D$ y $V_{GS}$ 
$\large I_D = f(V_{GS}, V_D)$ 

Por ende, cuando migramos a corriente alterna y trabajamos con variación en el tiempo. Linealmente;

$\large dI_D = \frac{\partial I_D}{\partial V_D} \cdot dV_D + \frac{\partial I_D}{\partial V_{GS}} \cdot dV_{GS}$   o lo que es en alterna;

$\large i_D = g_d \cdot v_D + g_m \cdot v_{GS}$

---
## *Transconductancia* $\huge g_m$

Aparece a partir de $\LARGE \frac{\partial I_D}{\partial V_{GS}}$ , por lo que podemos determinar que se trata de "que tanto la corriente de drenaje varía en función de la tensión de gate"

Físicamente, este parámetro muestra que el incremento en la tensión de gate lleva a *más* inversión, [[MOSFET (Canal Largo)#^2381cd|lo cual reduce la resistencia del canal]], llevando a mayor $I_D$.
**Fenomenológicamente, $g_m$ mide que tan eficientemente una variación en $V_G$ modifica $I_D$.**

Matemáticamente, $g_m$ se obtiene derivando $I_{D_{SAT}}$ con $V_D = V_{GS} - V_T$ 
Lo que nos deja con:

$\Large g_m = \frac{{Z \cdot C_{ox}} \cdot \mu }{L} \cdot (V_{GS}-V_T)$  cuya unidad es $\LARGE [\frac{A}{V}] = S$, Siemens 


## *Conductancia de Drenaje* $\huge g_d$

Aparece a partir de $\LARGE \frac{\partial I_D}{\partial V_{DS}}$ , o "cuanto de $I_D$ cambia cuando varía $V_DS$.

Nuevamente, aparece de derivar $\large I_D$ , y se define como:

$\Large g_d =\frac{{Z \cdot C_{ox}} \cdot \mu }{L} \cdot (V_{GS}-V_{T}-{V_{DS}})$

Como se puede apreciar, en $V_D = 0$, $g_d$ es bastante grande, o por lo menos, está en su valor máximo. 
Y al llegar a saturación (Cuando $V_{GS}-V_T= V_D$) y la función deja de depender de $V_D$ , $g_d = 0$, *idealmente.*
![[firefox_qqDzctf2iM.png]]
Notar que la pendiente de $g_d$ nos puede ayudar a determinar características del material!!
### Y todo esto que tiene que ver con la frecuencia???
Bueno, ahora que tenés los parámetros, debería ser apreciable que estos parámetros determinan que tan rápido la corriente puede variar en respuesta a los cambios de tensión.

Recordando la ley de corriente en el capacitor..:

$\LARGE i_C = C \frac{dv}{dt}$    (corriente en el Cap. = variación de v en el tiempo * Capacidad) 

A bajas frecuencias, $\Large \frac{dv}{dt}$ es pequeña, por ende los comportamientos capacitivos son pequeños, y se puede imaginar que estos actúan como circuitos abiertos en el circuito equivalente.
![[Pasted image 20260518181439.png]]
Pero a **altas frecuencias** $\Large \frac{dv}{dt}$ se vuelve alta, y empiezan a aparecer capacidad parasitas.

$\Large C_{gd}$  **Capacidad *Gate*-a-*Drain*** 
	  Capacidad parasita producto del solapamiento entre los terminales del Gate y del Drain.
	  A efectos prácticos, esta capacidad genera lo que se conoce como "Efecto Miller".
		  Durante el switching, el cambio veloz (alta $f$ ) se ve enviado nuevamente al gate, creando una capacidad efectiva que se multiplica por la *ganancia* del transistor. Esto reduce considerablemente los tiempos de funcionamiento.
	  Por esta razón, también se conoce a esta capacidad como $C_{rss}$ o "Capacidad de transmisión reversa".
	  Es significante durante la region linear / de triodo. 
	  Y cae a un valor bajo en la zona de saturación, ya que desaparece el solapamiento entre compuertas debido al pinch off / estrangulamiento del canal, cortando la conexión.
	  Una solución es mejorar la alineación de las compuertas, o incrementar el grosor del óxido.

$\Large C_{gs}$  **Capacidad *Gate*-*Source*** 
	  De forma similar, esta capacidad aparece producto de la capacidad intrínseca del MOS y por un contacto entre el terminal *source* y la compuerta.
	  Se forma principalmente por la capa de óxido que separa la compuerta del canal.
	  Inicialmente, se trata de un comportamiento capacitivo con el bulk, un $C_{gb}$
	  ---
	  Al crearse la zona de depleción, al igual que el MOS, se crea un capacitor en serie, el cual reduce la capacidad total hasta un $C_{min}$ determinado por el ancho máximo de la zona de depleción.
	  Cuando por fin se crea la zona de inversión, se crea una conexión entre el canal y el source, por lo cual esta capacidad se llama $C_{gs}$ y el capacitor vuelve a ser el típico MOS. 
	  Aumenta el consumo de $V_G$ y colabora en el control de la velocidad de switching.
	  ![[firefox_BtgtJrEhoG.png|300]] ![[C_gs_OVERTIME.png|300]]
	  El valor de $C_{gs}$ crece de forma continua en la zona linear
	  Y se establece en un valor casi constante en la zona de saturación, aproximadamente $2/3$ de la capacidad total del óxido.


z
![[firefox_0jIGufdHGM.png]]

Adicionalmente, existen otras capacidades entre terminales y bulk, pero son menos prevalentes, al igual que la capacidad de *Drain* - *Source*.

Adicionalmente, podemos usar algunos de los parámetros para obtener la
##### Frecuencia de corte, $f_T$ donde la ganancia cae a $1$.

	 $\Large f_T = \frac{g_m}{2\pi (C_{gs}+C{gd})}$

Notar que la [[Respuesta en Frecuencia#*Transconductancia* $ huge g_m$|transconductancia]] se encuentra en el numerador, por lo que podemos deducir que cuanto más pequeña la longitud del canal $L$, más grande será la frecuencia de corte!