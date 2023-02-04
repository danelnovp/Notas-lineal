# Combinaciones lineales

Este concepto es muy intuitivo de hecho casi ni merece una larga explicación, pero igual aquí estoy yo escribiendo pendejadas matemáticas de manera entendible para mi propio ser estúpido.

Digamos que tenemos un conjunto finito de $n$ vectores $\vectores$, decimos que un vector $w$ es combinación lineal de estos cuando es el resultado de la suma de cada uno de los $n$ vectores multiplicados por un escalar $\alpha_i$.

<mbox>

# Definición combinación lineal

$w$ es combinación lineal de los vectores $\vectores$ cuando:
$$
w = \sum_{i=1}^n \alpha_i v_i = \combinacion
$$
con $\alpha_i \in \R$.

</mbox>

<ejemplo>

La combinación lineal del vector $(4,3)$ a partir de los vectores $(2,1), (3,1),(9,2)$ es:
$$
(4,3)=2(2,1)+3(3,1)+(-1)(9,2)
$$

</ejemplo>

## Espacio generador

Se dice que los vectores $\vectores$ generan al espacio vectorial $V$ si todo vector en $V$ se puede escribir como combinación lineal de los mismos, osea que para cada $v\in V$ existen un conjunto de escalares $\escalares$ tal que $v=\combinacion$.

Si esto ocurre se dice que el espacio generado por el conjunto de vectores $\set{\vectores}$ es el conjunto de todas las combinaciones lineales de los mismos. La notación utilizada para esto es la siguiente:
$$
\generado{\vectores} = \set{v \,|\, v = \combinacion, \alpha_i \in \R}
$$

<ejemplo style="counter-reset: ejemplo;">

Si se toma un vector $(a,b)\in\R^2$, entonces $\generado{(a,b)}=\set{\alpha(a,b)\,|\, \alpha\in\R}$, se obtiene el espacio vectorial de la recta que pasa por el origen y por el punto $(a,b)$.

</ejemplo>

<ejemplo>

El espacio generado por $(1,0)$ y $(0, 1)$ es todo $\R^2$.

$$
\begin{aligned}
    \generado{(1,0)\,,(0,1)} &= \set{\alpha(1,0)+\beta(0,1) \,|\, \alpha,\beta\in\R} \\
    &= \set{(\alpha,0)+(0,\beta) \,|\, \alpha,\beta\in\R} \\
    &= \set{(\alpha,\beta):\alpha,\beta\in\R} \\
    &= \R^2
\end{aligned}
$$

Basto con solo dos vectores para generar todo $\R^2$, ahora una pregunta natural es ¿cual es el mínimo de vectores que necesito para generar un espacio $V$?, pues la respuesta a esto la veremos después, pero para responderla tenemos que entender otro concepto llamado **independencia lineal**.

</ejemplo>