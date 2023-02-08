# Bases y dimensiones

Digamos que tenemos un espacio vectorial $V$, ahora se quiere encontrar la minima cantidad de vectores que lo generen, sabemos que tales vectores no pueden ser LI, ya que al menos uno es combinación de los demás, por lo que puede ser eliminado, entonces solo queda pedir que los vectores sean LI.

<mbox>

# Base de un espacio vectorial

Sea $\vectores$ una colección de vectores LI de $V$ y además $V=\generado{\vectores}$ , llamamos a esta colección de vectores base de $V$.

</mbox>

<ejemplo>

Los vectores $(1,0)$ y $(0,1)$ es base de $\R^2$, la demostración de que generan a todo $\R^2$ ya fue hecha, y resulta trivial demostrar que son LI.

</ejemplo>


<ejemplo>

El conjunto $\set{1, x, x^2, x^3}$ son base del espacio vectorial de los polinomios de grado 3 (denotado por $[p]_3$).

</ejemplo>

> Estos ejemplos son triviales ya que usan lo que se llama la base canónica, que se puede definir como la base más simple y trivial del espacio vectorial.

<ejemplo>

Los vectores $(0,1)$ y $(1, 1)$ son base de $\R^2$.

<demostracion>

Primero demostremos que son LI. sea $\alpha,\beta \in \R$ entonces:
$$
    
\begin{aligned}
    \alpha(0,1)+\beta(1,1) &= (\beta, \alpha + \beta) = (0,0)
\end{aligned}
$$
de esto tenemos el siguiente sistema ecuaciones:
$$
\begin{cases}
    \beta &= 0 \\
    \alpha + \beta &= 0    
\end{cases}
$$
la solución a este sistema es $\alpha = \beta =0$, lo que demuestra que son LI.

Ahora se va a demostrar que generan a todo $\R^2$, para eso basta mostrar que 

</demostracion>

</ejemplo>