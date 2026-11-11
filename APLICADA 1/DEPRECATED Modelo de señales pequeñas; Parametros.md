
# $\LARGE i_{c}=h_{fe}\cdot i_{b}$

Donde 
* $i_{c}$ es la corriente de colector
* $i_{b}$ es la corriente de base
* $h_{fe}$ es la ganancia de corriente en emisor común

Esta formula nos relaciona cuanto cambia la corriente de colector en base a un cambio en la corriente de base.

Vale la pena resaltar que si bien $h_{fe}$ es una relación para una configuración especifica, es también una propiedad del transistor, por lo que se usa para el resto de configuraciones. 

Además, partiendo de esta misma relación, y sabiendo que:

$i_b=i_e-i_c$

podemos obtener 

$i_c=\frac{h_{fe}}{1+h_{fe}}i_e$

y si convertimos todo el factor de $h_{fe}$ en $\alpha$, se obtiene 
$\LARGE \boxed{i_c=\alpha i_e}$   
---

A partir de $i_{c}$ aparecen varias ecuaciones.

### $|V_{O}|$    Voltaje de Salida / Output Voltage

$|V_o|=i_cR_d$
$|V_o|=h_{fe}i_bR_d$
$|V_o|=\alpha i_eR_d$



---
---

# $\LARGE V_i=i_b\cdot h_{ie}$  

Donde
* $h_{ie}$ es la resistencia de entrada en el modelo de emisor común.

Nuevamente, notar que los parámetros del transistor en $EC$ siguen siendo utilizados para otras configuraciones.

Con la $h_{ie}$ se define como:

$h_{ie}=\left.\frac{v_{be}}{i_b}\right|_{v_{ce}=0}$

---

