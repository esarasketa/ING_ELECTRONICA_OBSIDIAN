
La ecuación de Laplace, dada por: $\nabla^2 V = 0$ nos permite calcular el potencial eléctrico en regiones del espacio que ***no contienen cargas libres***.

En caso de que esta condición no se cumpla, se trataría de una ***[[Ecuación de Poisson]]***.

Es muy útil para cuando es necesario calcular el potencial en un sistema a partir de las condiciones de frontera, como por ejemplo, dos conductores a distintos ángulos.

**Forma cartesiana:** $\frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} + \frac{\partial^2 V}{\partial z^2} = 0.$

**Forma cilíndrica:** $\frac{1}{r}\frac{\partial}{\partial r}\left(r\frac{\partial V}{\partial r}\right) + \frac{1}{r^2}\frac{\partial^2 V}{\partial \phi^2} + \frac{\partial^2 V}{\partial z^2} = 0$

**Forma esférica:** $\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial V}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial V}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2 V}{\partial\phi^2} = 0$

---

# Usos notables:

### Cuña Conectada a Potencial Eléctrico
![[Pasted image 20260921152128.png]]

$$ 
\begin{flalign*} 
V(\varphi) &= \frac{V_{CC}}{\alpha}\cdot \varphi &&\text{ Dentro de la Cuña}&& \\
 &= \frac{V_{CC}}{(2\pi-\alpha)}\cdot (2\pi-\varphi) &&\text{ Fuera de la Cuña}&&
\end{flalign*} 
$$

$$ 
\begin{flalign*} 
\overline{E}(r) &= \frac{V_{CC}}{\alpha}\cdot\frac{1}{r}(-\check\varphi) &&\text{ Dentro de la Cuña}&& \\
 &= \frac{V_{CC}}{(2\pi-\alpha)}\cdot \frac{1}{r} (\check\varphi) &&\text{ Fuera de la Cuña}&&
\end{flalign*} 
$$

---
