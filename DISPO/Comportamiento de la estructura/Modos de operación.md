---
tags:
  - DISPO
---

### Acumulación 
Polarización negativa, - en el metal, + en el bulk.
Se *acumulan* huecos en la interface, Ox-Sm, y $E_v$ se acerca a $E_f$ "como si cerca de la interface, el material fuera mas P"

En esta zona, el comportamiento capacitivo es similar al del óxido.
Es decir, $C ≈ C_{ox}$
Por qué? Porque en este modo, la estructura es prácticamente un capacitor, con el óxido siendo el dieléctrico, que no es muy gordo. 
### $C_{ox} = \frac{\epsilon_{ox}A}{t_{ox}}$ 

---
### Flat Band

Condición donde no hay cargas en la interface, equilibrio térmico. Idealmente, 0v. HOWEVER...!

**En un MOS no ideal, existe una diferencia entre los [potenciales de extracción]() $\phi_{m}$ y $\phi_{s}$ de modo que en 0V, ya se puede encontrar en modo de depleción. Se debe aplicar una tensión $V_g$ = $\phi_{ms}$ [[MOS NO IDEAL#Función Trabajo|más.]]

v
En Flat Band, $C = C_{fb} < C_{ox}$, pero muy poquito. Esto es porque existen pequeñísimas zonas de carga espacial.

---
### Depleción 
$V_g$ positivo. El componente metálico se carga y gracias al óxido aislante, esas cargas no pueden cruzar al bulk. Casi como un dieléctrico xd. 
Debido a la carga, por interacción electroestática, los huecos $h^+$ en el substrato se ven empujados, creando una zona de *depleción* en la interface Óxido-Sm con iones negativos fijos. 

En esta zona
, se crea una segunda interface, gracias a la zona de carga espacial generada. La capacidad es entonces paralela, con:

### $\frac{1}{C} = \frac{1}{C_{ox}} + \frac{1}{C_{depleción}}$

Y a medida que crezca la zona de depleción, más va a caer la capacitancia total.

---
### Inversión
Con $V_g$ aún más grandes, es posible entrar a una zona de inversión. Esto sucede cuando la interacción electroestática de los huecos $h^+$ no solo repele otros huecos, sinó que también comienza a atraer electrones libres $e^-$, efectivamente creando una zona $N$ en el substrato $P$.

Finalmente, con la nueva zona de inversión, la "placa del capacitor" vuelve a estar ubicada justo en la interface, ya que los electrones están super concentrados en la nueva zona $N$. Por ende, la capacidad vuelve a ser  $C ≈ C_{ox}$
