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

Ahora se va a demostrar que generan a todo $\R^2$, para eso basta mostrar que a partir de una combinación lineal de ellos podemos obtener los vectores canónicos, ya tenemos $(0,1)$ por lo que basta encontrar la combinación lineal de $(1,0)$ la cual es:
$$
(1,0) = (1,1)-(0,1)
$$
ya que hay una combinación lineal para cada canónico podemos generar todo $\R^2$ con estos vectores. Se concluye que $(1,1),\, (0,1)$ es base de $\R^2$

</demostracion>

</ejemplo>

<mbox>

## Teorema 1

Sea $V$ un espacio vectorial y sea $B=\set{\vectores}$ una base de $V$ y $G=\{w_1,w_2,\cdots,w_m\}$ un conjunto generador de $V$ $(\generado{G} =V)$ entonces $n\leq m$.

</mbox>

<demostracion>

Supongamos que $n\geq m$. El propósito de esta demostración es llegar a concluir que $\vectores$ son LD lo que claramente es una contradicción, para ello empecemos con la siguiente ecuación:
$$
\combinacion = 0
$$
Como $G$ es un conjunto generador entonces podemos escribir cada $v_i$ en términos de combinación lineal de $w_i\in G$ :
$$
\alpha_1(\beta_1^1 w_1+\cdots + \beta_1^m w_m)+\cdots+\alpha_n(\beta_n^1w_1+\cdots+\beta_n^mw_m) = 0
$$
Reorganizando los términos obtenemos:
$$
(\alpha_1 \beta_1^1+\alpha_2 \beta_2^1+\cdots +\alpha_n \beta_n^1)w_1+\cdots+(\alpha_1 \beta_1^m+\cdots \alpha_n \beta_n^m)w_m = 0
$$
Conocemos los valores de cada $\beta_i^j$ pero queremos encontrar los valores de cada $\alpha_i$, a partir de la ecuación anterior obtenemos el siguiente sistema homogéneo:
$$
\begin{matrix}
\alpha_1 \beta_1^1+\alpha_2 \beta_2^1+\dots+ \alpha_n \beta_n^1 = 0 \\
\vdots \\
\alpha_1 \beta_1^m+\alpha_2 \beta_2^m+\dots + \alpha_n \beta_n^m = 0
\end{matrix}
$$
El cual es un sistema de n incógnitas  $\escalares$ y $m$ ecuaciones, y por nuestra hipótesis $n\geq m$ , esto quiere decir que existen infinitas soluciones para $\escalares$, tal que $\combinacion=0$, esto demuestra que los vectores son LD pero esto entra en contradicción ya que $\vectores$ son LI, por lo tanto no pueden haber infinitas soluciones. Se concluye que $n \leq m$.

</demostracion>

> Este teorema nos afirma que las bases es el conjunto más pequeño que genera un espacio vectorial y ademas que sus vectores son LI.

<mbox>

## Corolario 1.1

Si $\vectores$ son LI y $w_1,w_2,\cdots,w_m$ generan el espacio $V$ entonces $n\leq m$.

</mbox>

<mbox>

## Corolario 1.2

Si $B_1$ y $B_2$ son bases de $V$ entonces $|B_1|=|B_2|$.

</mbox>

<demostracion>

Tenemos que $\generado{B_1}=V$, luego como $B_2$ es base también es un conjunto generador de $V$, entonces por el teorema anterior tenemos que $|B_1|\leq |B_2|$, de manera análoga para $B_2$ obtenemos $|B_2|\leq |B_1|$, se concluye que $|B_1|=|B_2|$.

</demostracion>

> Este teorema es importante porque afirma que sin importar que base escojamos estas siempre tendrán la misma cantidad de elementos.

---

Sabemos que una base de $V$ genera todo el espacio, lo que quiere decir que una combinación lineal de los vectores de la base puede escribir cualquier vector de $V$, pero ahora hay que preguntarse si cada vector se escribe de forma única según su base, o si existen más de una representación, el siguiente teorema nos permitirá responder a esta pregunta.

<mbox>

## Teorema 2

Sea $\vectores$ una base de $V$ y sea $v\in V$, entonces existe un conjunto único de escalares $\escalares$ tal que $v = \combinacion$.

Tales escalares son llamados coordenadas.

</mbox>

<demostracion>

Digamos que hay más de una combinación para $v$.
$$
\begin{aligned}
    v &= \combinacion \\
      &= \dcombinacion{\beta}{v}
\end{aligned}
$$
Se resta una combinación de la otra:
$$
\begin{aligned}
    0 &= \combinacion - (\dcombinacion{\beta}{v}) \\
      &= \alpha_1 v_1 - \beta_1 v_1 + \cdots + \alpha_n v_n - \beta_n v_n \\
      &= (\alpha_n - \beta_n)v_n + (\alpha_2 - \beta_2)v_2 + \cdots + (\alpha_n - \beta_n) v_n
\end{aligned}
$$

Como los vectores $\vectores$ son LI, y de aquí obtenemos una combinación lineal de ellos, que es igual a cero, entonces la única solución es que $\alpha_1 - \beta_1 = \alpha_2 - \beta_2 = \cdots = \alpha_n - \beta_n = 0$ lo que es equivalente a decir que $\alpha_1 = \beta_1 = \cdots = \alpha_n = \beta_n = 0$ para todo $\alpha_i, \beta_i$, esto lleva a concluir que las dos combinaciones lineales son la mismas, por lo tanto existe una única combinación lineal para cada vector respecto a la base.

</demostracion>
