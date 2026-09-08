---
tags:
  - DIGITALES_1
---

Definido un circuito que realiza *una* operación cualquiera, y definido el numero de ciclos en el cual el circuito realiza dicha operación, y dada una velocidad de reloj...

---
# Eficiencia o *throughput*

$\text{throughput}= \frac{1 seg}{\text{Tiempo de operación}}$

Por ejemplo, dado un circuito que realiza una multiplicación cada $4\micro S$, tendríamos un *throughput* de $250.000_{ops/seg}$ 

**Por qué es importante la velocidad de reloj?** 
Porque si el circuito tarda 4 pulsos de clock en hacer algo, y puede hacerlo en el mismo número de ciclos en una velocidad mayor, el circuito tendrá un throughput mayor.

---

# Parámetros temporales de los flip-flops

Da la vida, que los [[Flip-Flop]], los componentes más básicos de una operador lógico, tienen una serie de *tiempos* asociados. Las operaciones no ocurren de forma instantánea.
Por ejemplo, el tiempo entre que llega un pulso de clock a un flip-flop, y el flip-flop propaga el valor de $d$ a $q$ se lo conoce como

## Tiempo de Propagación $t_{cq}$
El $t_{cq}$ es el instante o retraso entre que el flip-flop recibe el flanco ascendiente del clock y la propagación del valor de $d$ a la salida $q$.

![[Pasted image 20260907152645.png]]

## Tiempos de Setup y Hold $t_{SU}$ y $t_{h}$

Para evitar la [[metaestabilidad]], antes de la llegada de un pulso de clock, se debe establecer el valor en $d$ durante un determinado tiempo. Y de la misma manera, el valor en $d$ se debe mantener estable durante otro determinado tiempo.  Estos son los llamados "tiempos de Setup y Hold", $t_{SU}$ y $t_{h}$ respectivamente.
Estos dos tiempos son intrínsecos a la tecnología y no pueden ser 100% eliminados.

![[Pasted image 20260907155337.png]]

>[!example] Ejemplo
>Dado el circuito:
>![[Pasted image 20260907160148.png]] 
>Cuyos tiempos y $f$ de operación son:
>+ $t_{CQ}= 200pS$
>+ $t_{SU}= 100pS$
>+ $t_{h}= 50pS$
>+ $f_{CLK}=1GHz$
>Su análisis temporal sería el siguiente.
>![[Pasted image 20260907162127.png]]
>Notamos la zona sombreada como el tiempo de setup + hold.
>
>
>Ahora, el siguiente es el mismo circuito, pero con $f_{CLK}=4GHz$
>![[Pasted image 20260907162443.png]]
>>[!error] Problema!
>>El $d_c$ está cambiando durante el $setup$ de $C$. Se está solapando el tiempo de propagación de $L$ con el tiempo de setup de $C$. En estas condiciones, el circuito **NO FUNCIONA**.

### Caso Critico
A partir del ejemplo anterior, es inmediatamente deducible que existirá un valor de frecuencia de $CLK$ máximo. A este valor de $f$ se lo conoce como **máxima frecuencia de operación sincrónica**.

Para obtener este valor máximo de $f_{CLK}$, es necesario saber el tiempo en el que ocurren las operaciones. En el caso del *ejemplo*, solo necesitamos $t_{cq}$ y $t_{SU}$.

Nuestra frecuencia máxima será $f_{CLK} = \Large \frac{1}{t_{cq} + t_{SU}} \normalsize = 3.\overline{3}GHz$
Para circuitos más complejos, es necesario tener en cuenta todos los componentes y sus tiempos.


## Tiempo de Buffer

Si se coloca un buffer entre $L$ y $C$, la lógica de operación no cambia en lo absoluto, sin embargo, aparece un $t_{buffer}$ inmediatamente después de $t_{cq}$ .

Si empezamos a aumentar el retraso del buffer, eventualmente vamos a chocar con el $t_{SU}$ del próximo flanco de clock. Al tiempo máximo que este buffer pude tardar en propagar la señal se lo conoce como:

## Tiempo de Slack

También llamado *margen de seguridad*, es el tiempo en el que el valor de una entrada $d$ ya tomó el valor a propagar *antes* del flanco de clock.

Imaginando el circuito del ejemplo + un buffer, podemos ver:

![[Pasted image 20260907164355.png]]

