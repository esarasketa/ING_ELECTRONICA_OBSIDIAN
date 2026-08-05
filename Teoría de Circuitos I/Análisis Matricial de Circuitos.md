#Matrices #Matrices_De_Estado #Variables_De_Estado

Las matrices de estado aparecen como solución al análisis de circuitos de alta complejidad.  
Cuando se nos presentan circuitos con **r** entradas y **m** salidas, se necessitarian resolver **r x m** problemas independientes, lo cual *obviamente* no es practico.

Enter: Matrices. Las de algebra.

Para utilizar dichas matrices, necesitamos el concepto de 

## Concepto de Estado
Definimos a un estado como *" Mínimo conjunto de variables $\large x_i$ (variables de estado), tales que si se conoce su valor para $\large t=t_0$ , y el valor de las entradas $\large u_i$ en $\large t≥t_0$ , pueden obtenerse las salidas $y_i$ en $\large t≥t_0$ "* 

Una variable de estado es una magnitud asociada a un componente, y su capacidad de almacenar energía. Que significa esto? Que si trabajamos con componentes ideales: l
* Los resistores no tienen ninguna variable de estado.
* Los capacitores tienen la tension $\large v_c$ asociada.
* Los inductores tienen la corriente $\large i_l$ asociada.

Dicho en bruto, si conoces el valor de entrada de un sistema, y sus variables de estado, podes obtener los valores de salida.

Como se trata de matrices, lo primero es definir los vectores con los que vamos a trabajar.

## Forma Vectorial
#### Vector de estados

	$\LARGE X(t)^{n,1}=[x_1(t),x_2(t),x_3(t),...,x_n(t)]$
	Léase "Vector X en función del tiempo, de dimensiones **n x 1**, compuesto por **n** variables de estado. "

#### Vector de entradas

	$\LARGE U(t)^{r,1}=[u_1(t),u_2(t),u_3(t),...,u_r(t)]$
	Léase "Vector U en función del tiempo, de dimensiones **r x 1**, compuesto por **r** entradas. "

#### Vector de salidas

	$\LARGE Y(t)^{m,1}=[y_1(t),y_2(t),y_3(t),...,y_m(t)]$
	Léase "Vector Y en función del tiempo, de dimensiones **m x 1**, compuesto por **m** entradas. "


En forma de funciones, uno entiende que los estados son función de las entradas, y de los propios estados, todos función del tiempo. Entonces, definimos cada derivada de un estado $\large x_n(t)$ como $\large x_n(t) \frac{dx_n}{dt}$ o lo que es más fácil de escribir, $\large \dot{x_n}(t)$.    (El puntito) 

	$\LARGE \dot{x_n}(t) = f_n(x_1,x_2,...,x_n;\;u_1,u_2,...,u_n;\;t)$

Que en forma vectorial es
	$\LARGE \dot{\overline{x}} = \overline{f} \left(\overline{x},\;\overline{u},\;t\right)$

De la misma forma, entendemos que el vector de salida se puede expresar como función de x, u y t
	$\LARGE {\overline{y}} = \overline{g} \left(\overline{x},\;\overline{u},\;t\right)$
	

## Sistema Lineal

Si el sistema es lineal, podemos escribir las ecuaciones como combinaciones lineales (wow) de las variables.

$\LARGE \dot{\overline{x}} = A(t) \cdot \overline{x(t)}+  B(t) \cdot \overline{u(t)}$

$\LARGE {\overline{y}} = C(t) \cdot \overline{x(t)}+  D(t) \cdot \overline{u(t)}$

Y estas letras?? Bueno, estas letras son las famosas Matrices, donde:

$\LARGE A^{\;n x n} \;\rightarrow$  Matriz de estados
$\LARGE B^{\;n x r} \;\rightarrow$  Matriz de entradas
$\LARGE C^{\;m x n} \rightarrow$  Matriz de salidas
$\LARGE D^{\;m x r} \rightarrow$  Matriz de transmisión directa


## Sistema LTI / LIT

Si el sistema es lineal e invariable en el tiempo (**LIT / LTI**), es aún más fácil, ya que las matrices dejan de ser función del tiempo.

$\LARGE \dot{\overline{x}} = A \cdot \overline{x(t)}+  B \cdot \overline{u(t)}$

$\LARGE {\overline{y}} = C \cdot \overline{x(t)}+  D \cdot \overline{u(t)}$


## Ejemplo de Parcial

***Parcial1_R3051_2021_tema2***

![[firefox_gENRFrsVNz.png]]

Queremos obtener: 

$\dot{\overline{x}} = A \cdot \overline{x}+  B \cdot \overline{u}\;\;$   e     ${\overline{y}} = C \cdot \overline{x}+  D \cdot \overline{u}$

### Primer paso: Identificar las variables.
##### Variables de estado:
El resistor no almacena energía, por lo tanto, no lo tenemos en cuenta.
Por su parte, el capacitor va a presentar una tensión $\large v_c$ y el inductor una corriente $\large i_l$.

Estos dos valores serán nuestra matriz $\large x=\begin{pmatrix} v_c \\ i_l \end{pmatrix}$
##### Variables de entrada:
Como es un único generador de corriente, la única variable de entrada será $\Large I_{i}$  por ende  $\large u=\begin{pmatrix} I_i  \end{pmatrix}$

##### Variables de salida:
En base a lo que nos pide el problema, $\large y=\begin{pmatrix} V_o \\ I_o \end{pmatrix}$

Esto nos deja los siguientes planteamientos.
$\Large \dot{\overline{x}} = A \cdot \overline{x}+  B \cdot \overline{u}$
$\large \begin{pmatrix} \dot{v_c} \\ \dot{i_l} \end{pmatrix} =  \begin{pmatrix} A_{11} \ A_{12} \\ A_{21} \ A_{22}\end{pmatrix} \cdot \begin{pmatrix} {v_c} \\ {i_l} \end{pmatrix} + \begin{pmatrix} B_{1} \\ B_{2} \end{pmatrix} \cdot \begin{pmatrix} {I_i} \end{pmatrix}$



### Segundo paso: Ecuaciones simples

Empleando las leyes de Kirchhoff, obtenemos todas las ecuaciones posibles del circuito.

Para la rama LC
$\Large V_o = v_c + L \cdot \frac{d i_l}{dt}$

Por paralelo, la rama R
$\Large V_o = V_R = I_R * R$   (Acordate de esta)

Finalmente, la corriente de entrada, por ley de nodos:
$\Large I_i = I_R + I_o$
Como la corriente en una misma rama es identica, $\Large I_{o} = i_l = i_c =C \cdot \frac{d v_c}{dt}$
$\Large I_i = \frac{V_o}{R} + C\frac{d v_c}{dt}$

### Tercer paso: Despejar las derivadas

Como te habrás dado cuenta, $\Large \frac{d v_c}{dt}$ no es  más que $\Large \dot{v_c}$ , y lo mismo con la corriente del inductor.
Lo correcto ahora, es despejar estas variables.

$\Large \dot{v_c} = \left(I_i - \frac{V_o}{R}\right)\cdot\frac{1}{C}$
$\Large \dot{i_l} = \left(V_o - v_c\right)\cdot\frac{1}{L}$

Ya casi estamos, per todavía tenemos 3 variables en nuestro sistema. El problema es que $V_o$  *no* es una variable de estado, es más, es una salida!
Ahora nos toca volver a la ecuación que marcamos antes.

$\Large V_o = V_R = I_R * R$   Por ley de nodos, $\large I_i = I_R + I_o \rightarrow \Large I_R = I_i - I_o$  por lo que:
$\Large V_o = R \cdot (I_i - I_o)$
Y ahora remplazá en las ecuaciones de derivadas! Y para mantener las variables de estado, $\large I_{o} = i_l$

$\Large \dot{v_c} = \left(I_i - (I_i - i_l)\right)\cdot\frac{1}{C} \;\;= \quad \frac{1}{C}\cdot i_l$
$\Large \dot{i_l} = \left(R(I_i - i_l) - v_c\right)\cdot\frac{1}{L} = \quad \frac{R}{L}\cdot I_i -\frac{R}{L}\cdot i_l - \frac{1}{L}\cdot{v_c}$

Notamos como todas las variables son o variables de estado o de entrada!!

### Paso final: ensamblar las matrices

$\Large \dot{\overline{x}} = A \cdot \overline{x}+  B \cdot \overline{u}$
$\large \begin{pmatrix} \dot{v_c} \\ \dot{i_l} \end{pmatrix} =  \begin{pmatrix} 0 \ \frac{1}{C} \\ -\frac{1}{L} \ -\frac{R}{L}\end{pmatrix} \cdot \begin{pmatrix} {v_c} \\ {i_l} \end{pmatrix} + \begin{pmatrix} 0 \\ \frac{R}{L}\end{pmatrix} \cdot \begin{pmatrix} {I_i} \end{pmatrix}$
