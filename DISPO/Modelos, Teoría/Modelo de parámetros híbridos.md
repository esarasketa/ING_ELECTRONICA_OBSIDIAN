---
tags:
  - TEORIA_DE_CIRCUITOS_1
  - DISPO
  - APLICADA_1
---
En el análisis de transistores BJT, es necesario evaluar tanto el efecto de la polarización continua (lo que "abre" o "activa" al transistor), y los efectos de la señal que atraviesa al *dispo*sitivo.

La continua y sus valores definen el "**punto de trabajo**", o punto $Q$, de "Quiescente".
Estos valores, son:

$Q\begin{cases}I_{D_Q} \\V_{GS_Q} \\V_{DS_Q}\end{cases}$

Lo importante de esto, es que desde el punto de vista de la señal de alterna, el transistor es un dispositivo *lineal*. 

El modelo de parámetros híbridos o de parámetros H modeliza al transistor como tal, mientras que se trate de una *pequeña señal*.

![[Pasted image 20261110162253.png]]
Circuito equivalente para un **Emisor Común**, utilizando elementos pasivos y fuentes. 

>[!info] Pequeña Señal
>Se define Pequeña Señal a toda señal de AC cuyo $\normalsize v_{be}$ es mucho menor al valor de $\normalsize V_T$ del dispositivo. Siendo $\normalsize v_{be}$ el valor pico de la señal de alterna, y $\normalsize V_T$ el voltaje térmico del semiconductor. **No confundir con la tensión de Umbral de los MOSFET.**

# Parámetros H

Los parámetros H del modelo se definen al analizar las variaciones de corriente $i_{b}, i_{c}$ y tensión $v_{be}, v_{ce}$ de la señal en los terminales del dispositivo.

Las ecuaciones base son: 

$\LARGE \begin{cases}&v_{be}&=\; h_{ie}*i_{b}+h_{re}*v_{ce} \\ &i_{c} &=\; h_{fe}*i_{b}+h_{oe}*v_{ce} \end{cases}$

Donde:
### $h_{ie}$ "Impedancia de entrada en corto-circuito"
Tiene unidad $\Omega$ y representa el ratio de tension base emisor a corriente de base, con $v_{ce}$ constante a 0.

$h_{ie}= \LARGE\frac{v_{be}}{i_{b}}|_{v_{ce}=0}$

### $h_{re}$  "Ganancia interna de tensión en circuito abierto"
No tiene unidades y representa el feedback interno. Es el ratio de cambio en la base-emisor con respecto al colector-emisor, con la corriente cte a 0.

$h_{re}= \LARGE\frac{v_{be}}{v_{ce}}|_{i_{b}=0}$

### $h_{fe}$ "Ganancia directa de corriente en corto-circuito"
No tiene unidades.
$h_{fe}= \LARGE\frac{i_{c}}{i_{b}}|_{v_{ce}=0}$

### $h_{oe}$ "Admitancia de entrada en circuito abierto"
Siemens o mhos. 

$h_{oe}= \LARGE\frac{i_{c}}{v_{ce}}|_{i_{b}=0}$


---
## Modelo Simplificado.

Es muy posible que en el diseño y o análisis de un BJT y su circuito, se tomen parámetros ideales
En este caso, ocurre lo siguiente:

#### $h_{re}=0$ 
En un transistor ideal, el feedback de voltage es practicame nulo.

#### $h_{oe}=0$ 
En un transistor ideal, la corriente de colector depende únicamente del voltaje base-emisor.
En la practica, los transistores muestran una dependencia al voltage de colector-emisor debido al [[Efecto de Early]].

$\begin{cases}&v_{be}&=\; h_{ie}\cdot i_{b}+\cancelto{0}{h_{re}}\cdot v_{ce} \\ &i_{c} &=\; h_{fe}\cdot i_{b}+\cancelto{0}{h_{oe}}\cdot v_{ce} \end{cases}\LARGE\to\begin{cases}&v_{be}&=\; h_{ie}\cdot i_{b} \\ &i_{c} &=\; h_{fe}\cdot i_{b}\end{cases}$

![[SIMPLIFICADO.png]]
Caso donde se tiene en cuenta $h_{oe}$

# Ejemplo

![[Pasted image 20261110180819.png]]
Configuración genérica en Emisor común.
![[SIMPLIFICADO 2.png]]
Circuito desplegado.


![[SIMPLIFICADO 3.png]]
Circuito equivalente.

A partir de este circuito, es que aparecen las [[Resistencias de Entrada y Salida|resistencias "virtuales" de entrada y salida.]]


## IMPORTANTE
En la mayoría de notas pertinentes, utilizamos el ejemplo de un Emisor Común.
Al cambiar la configuración, el modelo cambia.
Lo ideal es saber hacer el modelo, no saber de memoria los equivalentes.
Pero para referencia, existe: [[Modelos Equivalentes Parámetros H|Modelos Equivalentes de Parámetros H para configuraciones de BJT]].

