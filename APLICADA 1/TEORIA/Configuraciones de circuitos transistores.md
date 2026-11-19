Con "configuraciones" nos referimos a como se conecta el transistor en relación al *input* y *output* del circuito/sistema.
Lo más común es definir al circuito en base a que terminal o "patita" del transistor es **común** entre la entrada y salida.
# BJT

### Emisor Común
![[Emisor Comun.png]]
#### Características: 
+ $A_{V}$ alta, alrededor de $200$
+ $R_i$ media, entre **$1 kΩ-10 kΩ$**
+ $R_o$ baja, entre $10$ y algunos cientos de $\Omega$
+ $R_{iA}$ media, entre $500-5k$ $\Omega$

### Base Común
![[Base Comun.png]]
#### Características: 
+ $A_{V}$ ALTA y no desfasa. 
+ $R_i$ BAJA
+ $R_o$ baja
+ $R_{iA}$ Baja ($20\Omega-50\Omega$)
+ $A_I$ $\leq 1$
#### Circuito Ejemplo:
![[Pasted image 20261119132714.png]]![[Base Comun Desarmado.png]]
Notar que la señal se conecta de forma un tanto poco convencional, apareciendo "dentro" del sistema en vez de a la entrada.
Los principales beneficios de esta configuración son la alta ganancia de voltage, y el hecho de que no desfasa. Adicionalmente, tiene una muy buena respuesta en altas frecuencias- esto se debe a que al efectivamente tener la base en el GND de la Señal el [[Efecto Miller]] se elimina casi completamente. Esta reducción en la capacitancia Base-Colector permite que las frecuencias altas puedan pasar con mucha más facilidad.

#### Colector Común
![[Colector Comun.png]]