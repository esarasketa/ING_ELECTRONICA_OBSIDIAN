---
tags:
  - DISPO
---
Union entre dos [[Semiconductor Extrínseco|semiconductor extrínsecos]], uno tipo $P$ y uno tipo $N$. Son el principio de funcionamiento de los [[Diodos|Diodos Clásicos]].

Puntualmente, llamamos **Juntura** a la zona de inflexión donde el material pasa de ser $N$ a ser $P$.
La juntura puede ser fabricada de dos maneras:

#### Abrupta (Aleación)
Se coloca un dopante sobre un sustrato del tipo contrario, se lleva a una temperatura de fusión, y se dejá que ambos materiales interactúen.
Esto resulta en un perfil de juntura abrupto (duh).
![[firefox_2IPKDZr7SF.png]]

#### Gradual (Difusión)
Es un proceso mucho más complejo, pero que lleva a perfiles mucho mas precisos en la juntura.

![[firefox_kUC692jGDV.png]]

---

# Juntura P-N

Al momento de fabricación, ocurre un desplazamiento de portadores desde cada material, tratando de restaurar el equilibrio.
			$\downarrow$
Esto lleva a la creación de un campo eléctrico.
			$\downarrow$
Las cargas que se encuentren durante el proceso se verán recombinada, dando a lugar a:
	Cargas positivas, fijas, en la zona $N$
	Cargas negativas, fijas, en la zona $P$
			$\downarrow$
Lo cual nos deja con un campo eléctrico permanente debido a las cargas fijas.![[firefox_tG4PuJmxyv.png|500]]
	Como se ve, (ponele) las lagunas migran hacía $N$ donde se recombinan con un donor, dejando un átomo positivo fijo.
	Al mismo tiempo, los electrones migran a $P$ y se recomb. con un aceptor, dejando un átomo negativo fijo.

A la zona resultante, la llamamos zona de juntura, pero también:
+ Zona de Vaciamiento/Depleción
	 Porque ya no quedan cargas libres, solo iones fijos

+ Zona de Transición 🏳️‍🌈
	 Porque las cargás libres (una vez que se le aplique una corriente) atraviesan la zona

+ Zona de Carga espacial
	 Porque la neutralidad murió ante el nacimiento del campo eléctrico $E$

---
### Nomenclatura
A partir de este momento, es importante conocer como nos referimos a los portadores dentro del modelo.

$\Huge Portador_{Material_{Equilibrio}}$
	De forma que:
	$\large p_{p_0}$    "Lagunas en la zona $P$ en equilibrio térmico."
	$\large n_{p_0}$    "Electrones en la zona $P$ en equilibrio térmico."
	$\large p_{n_0}$    "Lagunas en la zona $N$ en equilibrio térmico."
	$\large p_{n_0}$    "Electrones en la zona $N$ en equilibrio térmico."

Siguiendo el modelo, definimos la zona de semiconductor extrínseco cuando la concentración de mayoritarios es 10 veces la concentración intrínseca. Es decir:

$\Large P \to N_A \cong \large p_{p_0}$  ; $\Large \frac{{n_i}^2}{N_A} \cong \large n_{p_0}$              y             $\Large N \to N_D \cong \large n_{n_0}$  ; $\Large \frac{{n_i}^2}{N_D} \cong \large p_{n_0}$

![[firefox_4L1OkpLvEv.png]]

En el grafico de la derecha, aparece la noción de longitud de juntura, $\Large \ell = \ell_p + \ell_n$ 
	Donde definimos $\ell_p$ como la distancia entre el limite metalúrgico y la zona $P$ 
	Donde definimos $\ell_n$ como la distancia entre el limite metalúrgico y la zona $N$ 

$\Large \ell = \sqrt{\frac{2\epsilon_s}{q}\cdot (\frac{1}{N_A}+\frac{1}{N_D})\cdot (\varphi_0-V_{ext})}$   muy útil para entender polarización en diodos
	Con $\epsilon_s$ = permitividad
	Entonces queda que la longitud de la juntura está dada por el material, el dopaje del material(que también afecta $\varphi_0$ como dice justo acá abajo!) y la tensión externa!  
## Potencial de Juntura
Una forma muy practica de relacionar conceptos, es dar cuenta lo siguiente.

El grafico de concentración, muestra como desde la zona $P$ hacia la zona $N$ se intercambian las concentraciones de portadores.
A partir de esto, y usando el concepto de [Potencial térmico de Maxwell-Boltzmann], podemos determinar un potencial que atraviesa el material debido al los cambios de portadores.

Dicho, el potencial de juntura $\Huge \varphi_0 = \frac{kT}{q}\cdot ln(\frac{N_AN_D}{{n_i}^2})$ 

Además, $\Large p_{n_0}=p_{p_0}\cdot exp(-\frac{q\varphi_0}{kT})$

De que nos sirve esto? Bueno, la derivada un potencial $\varphi$, con respecto al espacio $x$ es un campo eléctrico $E$, osea:
![[firefox_pjoX1T6B6V.png]]
Con esto, ya podés entender [[Diodos]].
#DISPO