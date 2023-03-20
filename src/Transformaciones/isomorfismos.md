# Isomorfismos

Sea $T \in L(V, W)$ si $T$ es sobreyectiva  (todo elemento de $W$ le corresponde un elemento en $V$) entonces $\im T = W$, ahora por el teorema de la dimensión no puede ocurrir que $R(T)=\dim W > \dim V$, por lo tanto se concluye que $\dim W \leq \dim V$, Ahora si $T$ es adema inyectiva entonces por los teoremas anteriores sabemos que $N(T)=0$ de esto y por el teorema de la dimensión concluimos que $\dim W = \dim V$.

Esto mismo es lo que motiva introducir los isomorfismo, que propiedades tienen las transformaciones lineales donde sus espacios vectoriales tienen la misma dimensión.

<mbox>

# Isomorfismos

Sean $T: V \to W$, se dice que $T$ es un isomorfismo cuando:
- $T$ es inyectiva.
- $T$ es sobreyectiva.

Cuando esto ocurre se dirá que $V$ y $W$ son isomorfos y se denotara por $V\cong W$.

</mbox>

<mbox>

## Teorema 1

Sea $V,W$ E.V de dimensión finita tal que $\dim V = \dim W$. Entonces $V \cong W$.

</mbox>

<demostracion>

Sea $\set{v_1, \cdots, v_n}$ base de $V$ y $\set{w_1, \cdots,w_n}$ base de $W$ entonces por el [teorema 2](propiedades.md#teorema-2) existe una transformación lineal $T: V\to W$ tal que:

$$
T(v_i) = w_i \quad \forall_{1\leq i \leq n}
$$

Es decir a cada vector de la base de $V$ lo mandamos a su respectivo vector a la base de $W$, además $T$ es única, ahora suponga que $v\in V$ y $T(v) = 0$, entonces si $v = \alpha_1v_1+\dots + \alpha_n v_n$ se tiene que $T(v) = \alpha_1T(v_1)+\cdots + \alpha_n T(v_n) = \alpha_1 w_1 + \dots + \alpha_n w_n  = 0$ como cada vector $w_i$ es L.I entonces  cada $\alpha_i = 0$, por lo tanto $T$ es 1-1 y como cumple esto entonces también es sobre, luego concluimos que $V \cong W$.

</demostracion>

## Todo EV tiene asociado un EV real

Este teorema nos asegura que dos E.V de igual dimensión son isomorfos, ya conocemos a todos los espacios vectoriales de la forma $\R^n$, entonces si $\dim V = n$ por el teorema anterior tenemos que
$$
V \cong \R^n \quad \dim V = n
$$
Con esto demostramos que todo espacios vectorial es isomorfo a un espacio vectorial de los reales, por este motivo el estudio de los espacios vectoriales y sus propiedades se reduce a estudiar los $\R^n$.

<mbox>

## Corolario 1

Si $\dim V = n$ entonces:
$$
V \cong \R^n
$$

</mbox>

## Algunos teoremas

Estos teoremas ayudaran a determinar isomorfismo, la demostración es sencilla y muchas de ellas ya fueron dadas en las secciones pasadas.

Sea $T\in L(V, W)$ y $\dim V = n$ y $\dim W = m$ entonces:

- T es inyectiva si y sólo si T es sobre.
- T es inyectiva si y sólo si $K(T) = \set{0}$ o $N(T) = 0$.
- Si T es sobre entonces $R(T) = m$ o $\im \, T = W$.
- $n = N(T) + K(T)$.
- Si $n>m$ entonces $T$ no puede ser Inyectiva.
- Si $n < m$ entonces $T$ no puede ser sobre.
- Si $n=m$ entonces $T$ es isomorfismo.

## Vectores coordenadas

<mbox>

## Vectores coordenadas

Sea $B=\set{v_1, v_2, \dots, v_n}$ una base de $V$, definimos el vector de coordenadas de un vector $v$, donde $v=\alpha_1 v_1 + \alpha_2v_2 +\cdots + \alpha_n v_n$ como:

$$
(v)_B = 
\begin{pmatrix}
	\alpha_1 \\
	\alpha_2 \\
	\vdots \\
	\alpha_n
\end{pmatrix}
$$

</mbox>

> la notación $(v)_B$ se utiliza para representar el vector de coordenadas de $v$ con respecto a la base $B$

Los vectores de coordenadas inducen una transformación lineal que además es isomorfismo, la cual esta definida de la siguiente manera:

$$
\begin{aligned}
	T: V &\to \R^n && \dim V = n \\
	v &\mapsto (v)_B && v\in V \\
	v_i &\mapsto e_i && v_i \in B
\end{aligned}
$$

Donde $e_i$ representa el i-esimo vector canónico de $\R^n$.

<ejemplo>

Hallar el vector de coordenadas de $P(x)=x^2 +x +4$ para las bases:

$$
\begin{aligned}
	B_1 &= \set{1, x, x^2, x^3} \\
	B_2 &= \set{1, 1+x, 1+x+x^2, 1+x+x^2+x^3}
\end{aligned}
$$

Para $B_1$ es trivial ya que se tratan de los vectores canónicos de $P[3]$, por lo tanto $P(x)_{B_1} = (4, 1, 1, 0)$.

Ahora para $B_2$ note que tenemos lo siguiente:
$$
\begin{aligned}
	v_1 &= 1  \\
	v_2 &= x = (1+x) -1 \\
	v_3 &= x^2 = (1+x+x^2)-(1+x) \\
     v_4 &= x^3 = (1+x+x^2+x^3)- (1+x+x^2) 
\end{aligned}
$$

Por lo tanto:

$$
\begin{aligned}
	P(x) &= v_3 +v_2+4v_1 \\
	&= [(1+x+x^2)- (1+x)] + [(1+x)- 1] + 4 \\
	&= (1+x+x^2)+3
	\\\\
	\therefore P(x)_{B_2} &= (3, 0, 1, 0)
\end{aligned}
$$

</ejemplo>