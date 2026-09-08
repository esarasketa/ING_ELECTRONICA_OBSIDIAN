---
tags:
  - DISPO
---
**M**ETAL 
**O**XIDE
**S**EMICONDUCTOR
**F**IELD
**E**FFECT
**T**RANSITOR

Partiendo del concepto de un [[Estructura MOS|capacitor MOS]], los transistores MOSFET consisten de un *bulk* semiconductor tipo $P$ en el cual existen dos terminales muy dopadas (Para el análisis, tipo $N^+$, pero existen tipo $P$ con sustrato $N$).

[![MOSFET Physics](https://www.mks.com/mam/celum/celum_assets/Figure_11-Semiconductor_Handbook_800w.jpg)

Y utilizando el principio de funcionamiento del los MOS, se utiliza la estructura para crear una zona de inversión tipo $N$ entre los terminales *Source* y *Drain*, controlados por el terminal *Gate*, de la estructura MOS. A este puente entre $S$ y $D$ lo apodamos canal o *Channel*. 

A efectos prácticos, esto significa que hemos creado (si, vos y yo) un interruptor controlado por tensión! El mejor switch de la historia, de controla con la misma moneda que pasa a través suyo.

# Importante!
En el diagrama que vemos arriba, vemos que la distancia $y$ entre $S$ y $D$ es mucho mayor a la profundidad $x$ posible del canal.

Por esto, declaramos la existencia de la **"Aproximación de Canal Gradual".**
Que es un nombre elegante para "$E_X >> E_Y$"
	Dicho en bruto, la **ACG** establece que el campo eléctrico producto de la zona de carga espacial entre la zona de inversión y el sustrato (MOS) es *ordenes de magnitud* mayor a la ZCE entre $S$ y $D$, y que el campo eléctrico en Z es uniforme e invariable.

Usando este concepto, los transistores MOSFET se pueden clasificar a grandes rasgos en función de su longitud de canal $y$.

Si el canal es considerablemente mayora a la profundidad $x$, asumimos que $E_y = 0$, y se trata de un [[MOSFET (Canal Largo)|MOSFET de Canal Largo]].

**Recomiendo leer Canal Largo antes de Canal Corto! La mayoría de conceptos del Canal Corto son *en relación* a los de Canal Largo!**

Debido al *scaling* (tendencia tecnológica a achicar los componentes), eventualmente el canal se encuentra con longitudes de canal similares a $x$. Cuando esto ocurre, la APG deja de aplicarse, ya que el $E_X \approx E_Y$, o por lo menos, dentro de la misma magnitud. 
Sea este el caso, debemos olvidar lo aprendido en los MOSFET de Canal Largo (osea no) y adentrarnos en los [[MOSFET (Canal Corto)|MOSFET de Canal Corto]].



#DISPO