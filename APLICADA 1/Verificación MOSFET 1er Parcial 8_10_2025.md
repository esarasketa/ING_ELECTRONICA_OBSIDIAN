---
handwriting-page-id: 9968e6a7-57ca-4843-8650-a8078fbcde0c
---

![[Pasted image 20261009164048.png]]


Se nos pide:
* Polarización
* Excursión simétrica máxima
* $R_{ia}$, $R_{oa}$, $A_{V_{S}}$
# Paso 1
##### Análisis de Continua
---
![[Analisis_1.png]]


#### Paso 1.1 Buscar el punto $Q$
El punto $Q$ aparece como los valores de $I_{D}$, $V_{GS}$ 
$R_{1}$ y $R_{2}$ actúan como divisor de tensión.

Por divisor resistivo, la $V_{TH}$ resultante es $V_{DD}\cdot \frac{R_{2}}{R_{1}+R_{2}}$. En este caso, $2.12V$
La $R_{TH}$, por su parte, es $R_{1}\parallel R_{2}=776.470k\Omega \approx{776.5}k\Omega$


Ahora, desde la perspectiva del Gate, solo hay una fuente* y una resistencia*

![[Analisis_2.png]]

Ahora, acordándonos de las ecuaciones de MOSFET, la tensión $I_D$ o $I_{DS}$ **en saturación** existe como:
**$\LARGE I_{D_{sat}} = \frac{{Z \cdot C_{ox}} \cdot \mu }{2L}\cdot (V_{GS}-V_T)^2$**

Por suerte, el primer termino queda simplificado a $B$, de la hoja de datos. 

$\LARGE I_{D_{sat}} = B\cdot (V_{GS}-V_T)^2$   ①

Se obtiene por la siguiente relación

$B_{ALD{1103-P}}=\frac{I_{D_{ON}}}{(V_{GS_{ON}}-V_{T})^2}=\frac{40mA}{(5V-0.7V)^2}\approx 2.16\left[ \frac{mA}{V^{2}}\right]$

Ahora, se hace necesario obtener $V_{GS}$. 

$V_{GS}$ es, por definición, la diferencia entre la tensión de $G$ate y $S$ource.
$V_{GS}=V_{G}-V_{S}$

Sabemos que $V_G$ es la tensión de la fuente equivalente de Thevenin. Y por su parte, $V_S=I_{D}R$, ya que si vemos el canal $D\to S$ continuo, solo aparece la resistencia $R$.

Por ende, $V_{GS}=V_{TH}-I_{D}R$.  ②

① en ②:

$V_{GS}=V_{TH}-(B\cdot (V_{GS}-V_T)^2)\cdot R$
$V_{GS}=V_{TH}-(B\cdot ({V_{GS}}^2-2\cdot V_{GS}V_T+{V_{T}}^2))\cdot R$
$V_{GS}=V_{TH}-BR\cdot {V_{GS}}^2+2\cdot BR\cdot V_{GS}V_T-BR \cdot{V_{T}}^2$
$0=V_{TH}-BR\cdot {V_{GS}}^2+2\cdot BR\cdot V_{GS}V_T-BR \cdot{V_{T}}^2-V_{GS}$
$0=-BR\cdot {V_{GS}}^2+(2\cdot BR\cdot V_{T}-1)\cdot V_{GS}+(V_{TH}-BR \cdot{V_{T}}^2)$

$0=BR\cdot {V_{GS}}^2+(1-2\cdot BRV_{T})\cdot V_{GS}+(BR \cdot{V_{T}}^2-V_{TH})$

$BR= 2.16\frac{mA}{V^{2}}\cdot 2k\Omega=4.32\left[ \frac{V}{V^2} \right]=4.32[ V^{-1}]$

$0=4.32[ V^{-1}]\cdot {V_{GS}}^2+(1-2\cdot 4.32[ V^{-1}]\cdot 0.7V)\cdot V_{GS}+···\\+(4.32[ V^{-1}] \cdot{0.49V}^2-2.12V)$


$0=4.32[ V^{-1}]\cdot {V_{GS}}^2-5.048\cdot V_{GS}-0.0032V$
Por cuadrática:
$V_{GS_{1}}=-0.00063V$ y $V_{GS_{2}}=1.17V$ 

Nos quedamos con la positiva, $V_{GS}=1.17V$ 
Y por ende, $I_{D}=0.48mA$
Y finalmente, $V_{DS}=V_{DD}-I_{D}\cdot R=5.04V$
Tenemos entonces

$Q\begin{cases}I_{D_Q} = 0.48mA \\V_{GS_Q} = 1.17V \\V_{DS_Q} = 5.04V\end{cases}$

Condición de saturación:
$V_{DS} >V_{GS}-V_T \to 5.04V>1.27V-0.7V$ 
Efectivamente xdddd

Ahora, recta de carga estática.

