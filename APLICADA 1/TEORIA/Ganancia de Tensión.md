#APLICADA_1 

# $A_{v}$   Ganancia de Tensión del Circuito
Es la relación entre el voltaje de salida y el voltaje **justo en la entrada** del transistor.
Ignora brutalmente a la resistencia de la fuente no ideal $R_{s}$, al igual que a las perdidas por acoplamiento.
Suele ser mayor que $A_{vs}$ por dichas razones.

$\boxed{A_{v}=\frac{v_{o}}{v_{in}}}$

# $A_{vs}$   Ganancia de Tensión del Sistema
De la misma forma, $A_{vs}$ va a calcular un ratio entre tensiones, pero a diferencia de $A_v$, va a incluir tanto la $R_L$ como la $R_S$.

Para evitar problemas con los inversores, se define utilizando módulos:
$\boxed{\left|{{A_{vs}}}\right|=\frac{\left|{{v_{o}}}\right|}{\left|{{v_{s}}}\right|}= {\frac{R_{iA}}{R_{is}}}\cdot \frac{hfe \cdot R_{os}}{hie}}$    Abajo se explica como se obtiene.

# Calculo de $A_{vs}$

Partiendo del circuito equivalente de un BJT en configuración Emisor Común. 
![[Pasted image 20261110191511.png]]
Notamos la importancia de definir las [[Resistencias de Entrada y Salida#$R_i$ Resistencia de Entrada|Resistencias de Entrada y Salida]].

Partimos de la identidad.
${\left|{{A_{vs}}}\right|=\LARGE\frac{\left|{{v_{o}}}\right|}{\left|{{v_{s}}}\right|}}$

Recordando que estamos tratando con una relación, podemos desarmarla con respecto a $v_b$ que definimos como la tensión en la resistencia equivalente de polarización $R_{BB}$

${\left|{{A_{vs}}}\right|=\LARGE \frac{\left|{{v_{o}}}\right|}{\left|{{v_{b}}}\right|}} \cdot \LARGE\frac{\left|{{v_{b}}}\right|}{\left|{{v_{s}}}\right|}$   Definiendo a la 1ra relación como $A_{v_{2}}$ y a la 2da $A_{v_{1}}$ (1ra y 2da parte)

### $A_{v_{1}}$  Ganancia de Entrada o Primera Parte

$|A_{v_{1}}|=\LARGE\frac{\left|{{v_{b}}}\right|}{\left|{{v_{s}}}\right|}$

Viendo el circuito, vemos que la $R_{BB}$ y la $h_{ie}$ están en paralelo, osea que comparten tensión.

![[Pasted image 20261110192611.png]]

Haciendo el calculo paralelo, encontramos que la resistencia de entrada al amplificador $R_{iA}$ es atravesada por $v_b$,  y viendo el circuito, podemos identificar un divisor de tensión de toda la vida.
Por ende:

$|v_b| = |v_s| \cdot \Large \frac{R_{iA}}{R_{s}+R_{iA}}$   y por lo tanto   ${\LARGE\frac{\left|{{v_{b}}}\right|}{\left|{{v_{s}}}\right|}\normalsize=\Large \frac{R_{iA}}{R_{s}+R_{iA}}}$

Adicionalmente, $R_s+R_{iA} = R_{is}$ !

$\boxed{|A_{v_{1}}|=\Large \frac{R_{iA}}{R_{is}}}$

---

### $A_{v_{2}}$  Ganancia de Salida o Segunda Parte

$|A_{v_{2}}|=\LARGE\frac{\left|{{v_{o}}}\right|}{\left|{{v_{b}}}\right|}$

Aplicando la misma lógica, podemos utilizar la $R_{os}$ 
![[Pasted image 20261110193633.png|350]] Y ahora, es tan simple como aplicar Ley de Ohm.

$|v_{o}|=i_{c}\cdot R_{os}$   
Podriamos dejarlo acá, pero sabemos de mano del modelo H, que   $\Large i_c=i_{b}\cdot h_{fe}$
$|v_{o}|=i_{b}\cdot h_{fe}\cdot R_{os}$     Parece al divino botón pero tiene razón de ser.

Acto seguido, viendo $v_{b}$ , aplicamos la misma lógica.
La tensión de base cae sobre la $hie$, y al mismo tiempo recibe la $i_b$. @LeyDeOhm.

$|v_{b}|=i_{b}\cdot h_{ie}$
 
POR ENDE:

$|A_{v_{2}}|=\LARGE\frac{i_{b}\cdot hfe \cdot R_{os}}{i_{b}\cdot hie}$

Y ahora tiene sentido, se cancelan las $i_b$

$\boxed{|A_{v_{2}}|=\frac{hfe \cdot R_{os}}{hie}}$

---
Lo cual nos deja finalmente en:

$\LARGE\boxed{{|A_{vs}|=\frac{R_{iA}}{R_{is}}}\cdot \frac{hfe \cdot R_{os}}{hie}}$
