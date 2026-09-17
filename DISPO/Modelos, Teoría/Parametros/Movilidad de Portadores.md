---
tags:
  - DISPO
---
Dentro de una [[Red Cristalina]], definimos la movilidad de portadores $\LARGE \mu_n$ y $\LARGE \mu_p$ y como la rapidez con la cual los portadores se desplazan a través de la red cuando se aplica un campo eléctrico $E$.


## Perturbación de trayectoria
Por culpa de las interacciones en la red cristalina, encontramos algunos eventos que disminuyen la movilidad de los portadores.

+ Agitación Térmica
	A temperaturas superiores a $0°k$ la vibración de la red cristalina aumenta, incrementando la chance de que ocurra una colisión de un electrón contra la red.

+ Átomos sin ionizar.
	A temperaturas cercanas a $0°k$, los átomos pueden alterar la trayectoria de los portadores por medio de física, las cosas con masa se atraen. Gravedad, vamos.

+ Átomos ionizados
	Los átomos ya ionizados comienzan a causar eventos por interacción electroestática, lo que también da lugar a interacción entre partículas.
		Los portadores del modelo pueden interactuar libremente como si se tratara de partículas clásicas. Gracias, modelo.
![[firefox_gGCM1EB0RV.png|400]]Gráficos del Tremosa, gracias, Tremosa.![[firefox_6eWcbDc4CQ.png]]

## Deducción matemática 

La movilidad es un factor estadístico, no se evalúa la movilidad de un electrón, sino la de todo un conjunto de energía similar, al que apodamos $\delta n$. 

Partimos de la definición. Se le aplica un campo eléctrico $E$ al conjunto, y sabemos que la fuerza resultante es $\large F = -qE$, por lo que:
	$\LARGE F \cdot \delta n = -qE \cdot \delta n$    La fuerza que actúa sobre todo el grupo.

Luego, desarrollamos el segundo termino como;
La fuerza de newton, [masa aparente](obsidian://open?vault=DISPO&file=Masa%20Aparente) por aceleración: $\large m_n^* \cdot \frac{dv}{dt}$ 
Sumada;
La fuerza de "viscosidad", o *de roce interno*. Esta nace de las interacciones de dispersión, todos los eventos que perturban la trayectoria de los portadores: $\large \alpha \cdot v$ 
	Donde $\alpha$ representa un coeficiente de viscosidad.

Intercambiando, nos queda:
	$\LARGE F \cdot \delta n = m_n^* \cdot \frac{dv}{dt}\cdot \delta n + \large \alpha \cdot v\cdot \delta n$   

Dividiendo por $\large m_n^* \cdot \delta n$, no solo reducimos la ecuación, sino que también obtenemos un parámetro nuevo.
	$\Huge \frac {F}{m_n^*} = \frac{dv}{dt}+ \frac{v}{\tau}$   
		Donde $\Huge \tau$ es $\large m_n^*/\alpha$  y le llamamos "tiempo de relajación". Representa el tiempo medio entre dos impactos entre electrones y la red cristalina.

Con esta formula, podemos empezar a integrar bajo condiciones.
En $t=0^+$, el campo eléctrico $E$ será $0$, por lo que $F=0$. Integrando, obtenemos que 
	$\Huge v = v(0) \cdot exp(-t/\tau)$  

Geométricamente, podemos ver que la tangente / pendiente a la curva en el punto inicial nos determina el valor de $\large \tau$.
![[firefox_KkOb0I30ol.pnG]] 

Inversamente, en $t=\infty$, la velocidad será cte. Por lo que $\Large \frac{dv}{dt} = 0$ 
	$\Huge \frac {F}{m_n^*} = \frac{v}{\tau} \to \frac {-qE}{m_n^*} = \frac{v}{\tau}$ 

Con esto, definimos lo siguiente.
 $\Huge v = \frac {-q\tau}{m_n^*} \cdot E$
	$\Huge \mu_n = \frac {q\tau}{m_n^*}$  Movilidad, cuya unidad es $[\frac{cm^2}{V.seg}]$
$\Huge v = -\mu_n\cdot E$


Si graficamos la movilidad a lo largo de la temperatura $T$, se pueden apreciar zona de comportamiento:
![[firefox_mq9TevDIUQ.png|439]]
+ Zona **1**
	La reducción en la movilidad producto de las perturbaciones por parte de los átomos no ionizados.

+ Zona **2**
	Los átomos de impureza se ionizan y aumentan la dispersión.

+ Zona **3**
	En esta zona, los electrones ganan mucha velocidad, y los centros electroestáticos pierden su eficiencia como dispersores.

+ Zona **4**
	Finalmente, la agitación térmica vuelve a ser un problema, convirtiéndose en la principal razón de la dispersión. Esto continua hacia el punto de fusión y la ruptura de la red. GG.



Partiendo de este concepto, también nace el concepto de [[Conductividad]], $\Huge \sigma$   