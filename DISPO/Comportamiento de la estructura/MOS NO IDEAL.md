---
tags:
  - DISPO
---

## Función Trabajo

**En un MOS no ideal, existe una diferencia entre los [[Potencial de Extracción||potenciales de extracción]] $\phi_{m}$ y $\phi_{s}$ de modo que en 0V, ya se puede encontrar en modo de depleción. Se debe aplicar una tensión $V_g$ = $\phi_{ms}$
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.5.17 - 19.52pm.drawing",
	"width": 682,
	"aspectRatio": 2.5166051660516606
}
```
Este desplazamiento de capacidad implica que p

## Efecto de dopaje en el metal 
NOTA: El metal, en realidad, es muy probablemente un semiconductor degenerado.

Que implica esto? Que al "metal" también le puede aparecer una zona de depleción. 
Entonces, la capacidad se ve más como:
#### $\frac{1}{C} = \frac{1}{C_{ox}} + \frac{1}{C_{d}} + \frac{1}{C_{p}}$

Por suerte, y con sentido, a mayor contaminación, este efecto parasito es menor. Tan sencillo como: cuanto más se parezca a un metal, menos efecto por dopaje va a tener.

## Efecto de carga en el óxido y en su interfase.
Dicho facil, que la neutralidad entre el óxido y el silicio es mentira. Son los papás. En la practica, hay muchísimas cosas encastradas en la zona de transición.

### Cargas móviles ionizadas
**Dentro del óxido** existen iones como $Na^+, K^+$ que quedaron ahí del proceso de fabricación.

Estas cargas parasitas no hacen más que reducir la movilidad de los portadores, lo cual afecta el comportamiento de la estructura.
![[gettering_fig2.gif]]
**Solución:** Se emplea un horneado en atmosfera de fósforo, un proceso llamado "Gettering" o "Atrapamiento"
Básicamente, el fosforo crea una película que inmoviliza a los iones móviles (osea ya no), evitando que interactúen cuando se aplica un voltaje al gate.

### Portadores atrapados
**Más cerca de la interfase**, encontramos pares $h^+$ $e^-$ generados por radiación durante la fabricación, por efecto túnel o por la inyección de [Hot Carriers] 

**Solución**: Recocido térmico. La temperatura le brinda energía cinética suficiente a los electrones y huecos atrapados para romper las barreras de potencial en las trampas.

### Cargas fijas
**Sobre la interfase**, ocurre que los electrones logran escapar hacia las compuertas durante la fabricación, pero los huecos pueden quedar atrapados cerca de la interfase.

Estos huecos reducen la movilidad ya que dispersan a los portadores!

**Solución:** Fabricación en atmosferas inertes. Debido a la naturaleza $SiO_x$ del óxido cerca de la interfase, el dióxido de silicio incompleto se traduce físicamente a enlaces covalentes abiertos. El trabajar en atmosferas inertes como $Ar$ puro permite controlar el proceso de oxidación con precision nanométrica.
O-Si-[  ]
### ESTADOS SUPERFICIALES
**LA** razón de la no idealidad de las curvas CV.
Justo en la interfase, donde el $SiO_x$  pasa a ser $Si$, existen estados de energía permitida que atrapan todo tipo de portadores. Esto provoca "*centros de recombinación-generación*" los cuales causan corrientes de fuga.

Se pueden ***minimizar*** con post metalizaciones en $H_2$ o inmersiones en ambiente de $H_2$ a 400°C. 
Esto sirve porque los enlaces abiertos en la interfase pueden convertirse en enlaces covalentes $Si-H$, el electrón que estaba libre queda emparejado. Esto **remueve el nivel de energía del defecto de la zona central del _bandgap_** y lo desplaza profundamente hacia las bandas de conducción o valencia, destruyendo su capacidad de actuar como centro R-G.

### Trampas de interfase 
Las trampas recien mencionadas, interactúan con el Silicio, lo cual provoca cambios en la distribución del mismo. Esto lleva a un cambio en el [[Potenciales variables#$ phi_s$ Potencial superficial|potencial superficial]] y el cambio de $V_g$
que eso conlleva.

#### Cambio en $\phi_s$
Esto afecta el comportamiento capacitivo, el cual ahora se ve como:
## $\frac{1}{C} = \frac{1}{C_{ox}} + \frac{1}{C_{Si} + C_{Ti}}$
- Donde $C_{Ti}$ representa la capacidad de las trampas de interfase.

Estas trampas, además, contribuyen a la aparición del efecto túnel entre bandas, ya que actúan como escalones entre las mismas, lo que lleva a más corrientes de fuga.

### Efectos del campo eléctrico elevado

* Ionización por impacto
	 A campo eléctrico inverso elevado, se producen colisiones en la red, lo cual puede llevar a la ruptura por avalancha.
* Efecto túnel Banda Banda
	 El *scaling* lleva a mayores grados de contaminación, lo cual da lugar a perfiles de juntura mas abruptos.
* Efecto túnel en el óxido
* Inyección de hot carriers al óxido
* Ruptura del dieléctrico


