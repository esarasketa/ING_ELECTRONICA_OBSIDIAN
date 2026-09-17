---
tags:
  - DISPO
---

Ciertamente, un diodo no es mas que una [[Juntura P-N]] con [[Contactos Óhmicos]]. Por lo que para el estudio de comportamiento los términos van a ser casi intercambiables.

## Equilibrio Térmico
![[firefox_5oIzQWATSg.png]]


Del proceso de fabricación, quedó un campo eléctrico en la juntura $\ell$,  al igual que un desbalance de portadores.
Ambos provocan un [[Desplazamiento de Cargas]].

Por corrimiento, aparecen $\Large -J_{nC}$  y  $\Large J_{pC}$  de electrones y lagunas respectivamente. ($-J_1$ y $J_4$ en el gráfico).
Por difusión, aparecen  $\Large -J_{nD}$  y  $\Large J_{pD}$  ($-J_2$ y $J_3$).

Como es aparente, en equilibrio, el corrimiento y la difusión se cancelan mutuamente, resultando en un corriente neta nula en la juntura.

La energía requerida para saltar desde un nivel al otro llamada "barrera de potencial", es $\large q \varphi_0$, o $E_g$, la que define la diferencia entre los niveles de energía en cada zona.

Por [[Distribución de Maxwell]], recordamos que:
Además, $\Large n_{p_0}=n_{n_0}\cdot exp(-\frac{q\varphi_0}{kT})$    
	"los $e^-$ en $N$ responden a una exp. negativa que depende de la temperatura y el potencial."
Que significa?
Significa que los electrones "quieren" ir a los niveles de energía más bajos, pero la energía térmica, la agitación de la red! no se lo permite.



## Polarización Directa
Aplicar un diferencial de tensión "Positiva" 
![[firefox_mEJNjnZQ6G.png]]
Por **Maxwell** ves que la $kT$ aumenta la difusión muy por arriba de la que estaba en equilibrio, ganándole al corrimiento. Esto lleva a un achique de $\ell$, y a una disminución del campo eléctrico.
Pero más importante, la disminución de la barrera de potencial $E_g = q(\varphi_0 -V)$, lo que permite que los electrones puedan saltar con menor energía.
También se ve la fractura del nivel de Fermi, debido a la polarización externa.
$\Large E_{f_n} -E_{f_p} = qV$    O alternativamente,    $\Large E_{f_n}  = E_{f_p}+ qV$ 


## Polarización Inversa
![[firefox_R2XfOP61uk.png]]
De forma inversa (jaja, entendés?), en esta polarización, la barrera de potencial *crece* gracias a $V$ y vuelve la difusión nula. Np hay valor $kT$ que salve al electron y le permita pasar la barrera.
En este modo, la única corriente que existe es la de corrimiento de minoritarios, producto del campo eléctrico $E$, que si bien crece, también induce un crecimiento del ancho de la juntura $\ell$.
Este pequeño flujo de minoritarios al sus zonas crea un infima corriente $P\to N$.



## Corriente en el diodo
Para entender la corriente en el diodo, lamentablemente, tenemos que primero pasar por la concentración de portadores en el diodo. Así que:
### Concentración de portadores en el diodo
De Maxwell, partimos con:
^util
$\Large p_{n_0}=p_{p_0}\cdot exp(-\frac{q\varphi_0}{kT})$
$\Large n_{p_0}=n_{n_0}\cdot exp(-\frac{q\varphi_0}{kT})$   
^util
Entonces, en equilibrio térmico:
![[firefox_PiFMn8dwCT.png]] ^881f1f

$\large p_n(0) = p_{p_0} \, e^{-q (\psi_0 - \nu)/{kT}}$
Lo que se convierte en
$\large p_n(0) = p_{p_0} \cdot e^{-q \psi_0 / kT}\cdot e^{+ q V / kT}$

Y usando lo que sabemos de Maxwell [[Diodos#^881f1f|(recien)]]
$\large p_n(0) = p_{n_0} e^{+ q V / kT}$

Con la misma lógica; 
$\large n_p(0') = n_{n_0} e^{- q(\psi_0 - V)/kT}$ 
$\large n_p(0') = n_{p_0} e^{ qV / kT}$

![[firefox_PHi3FVzaek.png]]
Y que acabamos de calcular, entonces?? Las concentraciones de minoritarios bajo pol. directa!
$p_n(0)$ y $n_p(0')$ son "los minoritarios dispuestos a sumarse al material"
Es decir, los portadores mayoritarios de cada zona cruzan la juntura, reforzando los portadores minoritarios del otro lado.
Además, notamos que se puede obtener las longitudes de juntura $\ell_n$ y $\ell_p$ usando la intersección de la recta $p_{n_0}$ y $n_{p_0}$ y la tangente en $0$ y $0'$ de las curvas de minoritarios!

Similarmente, las concentraciones bajo inversa. Nota que las pendientes son mucho más sutiles, por lo que sus intersecciones con las rectas de minoritarios ocurren "más adentro" de cada zona neutra, dando como resultado, flor de longitud de juntura.
![[firefox_65cZ3o9zIn.png]]

Como dato final, la diferencia entre $p_{n_0}$ y $p_n(0)$ se la conoce con el nombre de "exceso" y se la representa con $p'_n(0)$
Ahora si.
### Corriente en el diodo (ideal)
Ahora que tenemos la concentraciones claras, en un diodo ideal se cumplen dos cosas.
+ No hay recombinación $R(T)=0$
+ **TODOS** los portadores que entran la zona de carga espacial, salen de la misma.

Entonces, sumamos las densidades de corriente (los desplazamientos de cargas!!!!!!) y los multiplicamos por el Area de la juntura- *el diodo*!
	Recordando que $I = A\cdot J$ 

$\Huge I = Area \cdot [(J_{nD}-J_{nC})+(J_{pD}-J_{pC})]$ 

Y también podemos dividir la $I$ en $I_p$ y $I_n$ -  Con esto, definimos 

$\Large I_p(0) = A \cdot J_p(0)$   Siendo $\small J_p(0) =(J_{pD}-J_{pC})$ 
	Por qué en $(0)$ ? Porque la densidad de carga se mide en el borde metalúrgico.
	![[firefox_1nWsMr7PNp.png|350]]

$\Large I_p(0) = A \cdot -q \cdot D_p \cdot \large \frac{\partial p_n(0)}{\partial x}$   Esta tangente, también la podemos expresar como $tg(\theta)$.

$\Large I_p(0) = A \cdot -q \cdot D_p \cdot \large -\frac{p'_n(0)}{\ell_p}$  

Y como los excesos no son mas que una diferencia de concentraciones, nos queda que $p'_n(0)$ no es más que $\large p_{n_0}\left(e^{{qV}/{kT}} - 1\right)$ finalmente;

$\Large I_p(0) = \frac{q \cdot A\cdot D_p \cdot p_{n_0}}{\ell_p  }\cdot \left(e^{{qV}/{kT}} - 1\right)$ 

Siendo la corriente total

$\large I = \Large I_p(0) + \Large I_n(0') = q\cdot A\cdot \left(\frac{D_p\cdot p_{n_0}}{\ell_p} + \frac{D_n\cdot n_{p_0}}{\ell_n}\right) \cdot\left(e^{{qV}/{kT}} - 1\right)$ 

![[firefox_3b2aG2l1AB.png]]
### Corriente de Saturación
La corriente que existe en inversa.

$\Large I_S = -qA\left(\frac{D_p p_{n_p}}{L_p} + \frac{D_n n_{p_0}}{L_n}\right)$
Notamos dos cosas, la falta de curva exponencial, y la falta de dependencia de la tensión.


## Neutralidad eléctrica
Cabe destacar, que durante la polarización, se inyectan portadores minoritarios en las diferentes zonas. En un principio, esto parecería violar la neutralidad eléctrica del semiconductor.
Sin embargo, no. Física II.
Por electroestática, la mera presencia de los minoritarios en el semiconductor, genera las fuerzas necesarias para atraer mayoritarios y restaurar la net.
Pero, claramente, esto es un proceso, no es inmediato.
Sin embargo, si es brutalmente rápido.
Este proceso de re-neutralización, ocurre en lo llamado $\Large \tau_d$ , tiempo de Debye. Que es del orden de los $10^{-12}$ de segundo.  Y ocurre en una longitud llamada, no te la vas a creer, $\Large L_d$ que es del orden de 1 micrón.

---

Ya estás listo para abandonar el mundo donde todo está bien y tu mamá te quiere? $\large \downarrow$
[[Diodo No Ideal|El diodo real.]]

Adicionalmente, esto también te habilita a estudiar el [[Transistor BJT (Señal Débil)]]  