# Matriz Asociada a una Transformación Lineal

En esta sección se vera que cada transformación lineal $T:A\to B$ tiene asociada una matriz, tal que si se toma el vector de coordenadas de $v\in A$ y se multiplica por esta matriz, entonces el resultado de la multiplicación sera el vector de coordenada de $T(v)\in B$.

## Matriz en transformaciones reales

> Primero se estudiara el caso real y luego se generalizara para cualquier matriz.

<mbox>

# Teorema 1

Sea $T$ una transformación lineal tal que $T: \R^n \to \R^m$, entonces se puede encontrar una única matriz $A\in M_{m\times n}(\R)$ tal que $T(v) = Av$, donde $v\in \R^n$.

</mbox>


<demostracion>

Sea $v_i$ un vector canónico de $\R^n$, con $1\leq i \leq n$, donde $i$ representa la posición del 1 en el vector, es decir:

$$
v_i = (0, \cdots, \underbrace{1}_{\displaystyle\text{i-esima posición}}, \cdots, 0)
$$

Por [este teorema](propiedades.md#teorema-2) sabemos que $T$ esta determinado según se asigne los vectores de la base de $\R^n$ vectores de $\R^m$. Sea $w_1 = T(v_1), w_2 = T(v_2), \cdots, w_n = T(v_n)$, donde cada $w_i \in \R^m$ y 

$$
w_i = 
\begin{bmatrix}
\alpha_{1i} \\ \alpha_{2i} \\ \vdots \\ \alpha_{mi}
\end{bmatrix}
$$

con $\alpha_{ni}\in \R$, donde $1\leq n \leq m$.

Sea $A$ una matriz tal que sus columnas es cada uno de los vectores $w_i$:

$$
A = 

\begin{bmatrix}
    w_1 & w_2 & \cdots & w_n
\end{bmatrix}
=
\begin{bmatrix}
\alpha_{11} & \cdots & \alpha_{1n} \\
\vdots & & \vdots \\
\alpha_{m1} & \cdots & \alpha_{mn}
\end{bmatrix}
$$

Es claro que $A\in M_{m\times n}(\R)$. Sea $v_i$ un vector canónico de la base de $\R^n$ entonces si se multiplica este vector por la matriz se obtendrá como resultado el vector $w_i$

$$
\begin{bmatrix}
	\alpha_{11} & \cdots & \alpha_{1n} \\
	\vdots & & \vdots \\
	\alpha_{m1} & \cdots & \alpha_{mn}
\end{bmatrix}
\begin{bmatrix}
0 \\ \vdots \\ 1 \\ \vdots  \\ 0
\end{bmatrix}
= \begin{bmatrix}
\alpha_{1i} \\ \alpha_{2i} \\ \vdots \\ \alpha_{mi}
\end{bmatrix}
= w_i
$$

Aquí el 1 esta en la i-ésima fila de $v_i$.

</demostracion>

---

Se puede escoger cualquier base de $\R^n$ y esto se seguirá cumpliendo, sea $\set{\vectores}$ una base no canónica de $\R^n$, suponga que se tiene una transformación lineal tal que $T(v_i)=w_i$, donde $i=1,\cdots,n$, al ser una base se puede encontrar las combinaciones lineales que nos den como resultado los vectores de las base canónica, es decir:

$$
\alpha_{ij} \in \R \\
\alpha_{11}v_1 + \cdots + \alpha_{n1}v_n = v'_1 = (1,0,\cdots, 0) \\
\alpha_{12}v_1 + \cdots + \alpha_{n2}v_n = v'_2 = (0,1,\cdots,0) \\
\vdots \\
\alpha_{1n}v_1 + \cdots + \alpha_{nn}v_n = v'_n = (0,0,\cdots,1)
$$

Luego $T(v'_i)=w'_i$, luego construimos $A$ con columnas $w'_i$


<ejemplo>

sea $T: \R^2 \to \R^3$ tal que:
$$
T(2,1)=(1,1,0) \qquad T(1,0)=(0,2,1)
$$
Observe que $(0,1)=(2,1)-2(1,0)$ por lo tanto $T(0,1)=(1,-3,-2)$, entonces $A$ será de la forma:
$$
A = 
\begin{bmatrix}
	1 & 0 \\
	-3 & 2 \\
	-2 & 1
\end{bmatrix}
$$
Ahora demostraremos que cualquier vector $(a,b)$ multiplicado por esta matriz será de la forma $\alpha T(2,1)+\beta T(1,0)$
$$
\begin{aligned}
\begin{bmatrix}
	1 & 0 \\
	-3 & 2 \\
	-2 & 1
\end{bmatrix}
\begin{bmatrix}
	a \\ b
\end{bmatrix}
	&= 
\begin{bmatrix}
	a \\
	-3a + 2b \\
	-2a + b
\end{bmatrix}
	\\
&=
a\begin{bmatrix}
	1 \\ 1 \\ 0	
\end{bmatrix} 
-2a
\begin{bmatrix}
	0 \\ 2 \\ 1
\end{bmatrix} +
b
\begin{bmatrix}
	0 \\ 2 \\ 1
\end{bmatrix} \\
&= 
a\begin{bmatrix}
	1 \\ 1 \\ 0	
\end{bmatrix}
+(b-2a)
\begin{bmatrix}
	0 \\ 2 \\ 1
\end{bmatrix} \\
&= aT(2,1)+(b-2a)T(1,0) \\
&& \blacksquare
\end{aligned}
$$

</ejemplo>

## Matriz asociadas a cualquier transformación lineal

<mbox>

# Teorema 2

Sea $V,W$ espacios vectoriales con dimensión $n$ y $m$ respectivamente, sea $T \in L(V,W)$, sea $B_1 = \set{v_1, \cdots v_n}$ una base de $V$ y sea $B_2 = \set{w_1,\cdots,w_m}$ una base para $W$, entonces existe una única matriz $A_T$ de $m\times n$ tal que:
$$
(T(v))_{B2} = A_T (v)_{B_1}
$$

</mbox>

> Recordemos que la notación $(v)_{B}$ se refiere al vector de coordenadas de $v$ respecto a la base $B$, en caso de no acordarse revise [*Vectores coordenadas*](./isomorfismos.md#vectores-coordenadas).

<demostracion>

Tomemos $T(v_i) = y_i$ donde $v_i \in B_1$ ahora, $y_i$ es una combinación lineal de los vectores de la base $B_2$, es decir:

$$
y_i = a_{1i}w_1 + \cdots + a_{mi}w_i
$$

por lo tanto el vector de coordenadas de $v_i$ serán los escalares de la combinación lineal anterior.

$$
(y_i)_{B2} = 
\begin{pmatrix}
a_{1i} \\
\vdots \\
a_{mi}
\end{pmatrix}
$$

Con esto se definira $A_T$ como la matriz de $m\times n$ tal que sus columnas con los vectores de coordenadas de cada $y_i$:

$$
A_T = 
\begin{bmatrix}
(y_1)_{B2} & (y_2)_{B2} & \cdots & (y_n)_{B2}
\end{bmatrix}
=
\begin{bmatrix}
	a_{11} & \cdots & a_{1n} \\
	\vdots & & \vdots \\
	a_{m1} & \cdots & a_{mn}
\end{bmatrix}
$$

Sea $v\in V$ un vector arbitrario tal que $(v)_{B1} = (c_1, \cdots, c_n)$. Si se multiplica por $A_T$ se obtiene:

$$
\begin{aligned}
A_t (v)_{B1} &= 
\begin{bmatrix}
	a_{11} & \cdots & a_{1n} \\
	\vdots & & \vdots \\
	a_{m1} & \cdots & a_{mn}
\end{bmatrix}
\begin{pmatrix}
c_1 \\ \vdots \\ c_n
\end{pmatrix} \\
&=
\begin{bmatrix}
a_{11} c_1  &+& \cdots &+& a_{1n} c_n \\
\vdots &&&& \vdots \\
a_{m1}c_1 &+& \cdots &+& a_{mn}c_n
\end{bmatrix} \\
&= 
c_1 \begin{pmatrix}a_{11} \\ \vdots \\ a_{m1} \end{pmatrix}
+ \cdots + 
c_n \begin{pmatrix}a_{1n} \\ \vdots \\ a_{mn} \end{pmatrix} \\
&= c_1 (y_1)_{B2} + c_2 (y_2)_{B2} + \cdots + c_n(y_n)_{B2} 
\end{aligned}
$$

Se sabe que 
$$
\begin{aligned}
    T(v) &= T(c_1v_1 + \dots + c_n v_n) \\ 
         &= c_1 T(v_1) + \cdots + c_n T(v_n) \\
         &= c_1 y_1 + \cdots + c_n y_n
\end{aligned}
$$
de esta manera se tiene que
$$
\begin{aligned}
    T(v)_{B2} &= (c_1 y_1 + \cdots + c_n y_n)_{B2} \\ 
    &= c_1 (y_1)_{B2} + \cdots + c_n (y_n)_{B2}
\end{aligned}
$$

</demostracion>

<ejemplo>

Tomando el ejemplo anterior podemos tomar la base $B_1 = \set{(2,1), (1,0)}$ y $B_2 = \set{(1,0,0), (0,1,0), (0,0,1)}$, luego tenemos que:

$$
T(2,1) = (1,1,0) \qquad T(1,0) = (0,2,1)
$$

Primero se hallaran los vectores coordenadas para las imágenes de los vectores de la base $B_1$, pero no hay mucha complicación ya que la base del espacio vectorial de la imagen es la canónica por lo tanto nuestra $A$ seria de la forma:

$$
A =
\begin{bmatrix}
	1 & 0 \\
	1 & 2 \\
	0 & 1
\end{bmatrix}
$$

Tomemos el vector de coordenadas de los vectores de la base $B_1$:

$$
(2,1)_{B1} = (1,0) \qquad (1,0)_{B1} = (0,1)
$$

Ahora observe que si multiplicamos cualquier vector de coordenadas $v$ de $B_1$ nos dará como resultado $T(v)$ (ya que la base $B_2$ es la canónica).

$$
\begin{bmatrix}
	1 & 0 \\
	1 & 2 \\
	0 & 1
\end{bmatrix}
\begin{pmatrix}
	1 \\ 0
\end{pmatrix}
=
\begin{pmatrix}
	1 \\ 1 \\ 0
\end{pmatrix}
= T(2,1)
$$

</ejemplo>

## Teorema de la dimensión

Ya en [esta sección](../EspaciosVectoriales/kerne_e_imagen.md#teorema-de-la-dimension-td)  se trato la demostración del teorema de la dimensión para espacios vectoriales en $\R$, ahora que ya demostramos que toda transformación lineal puede escribirse de la forma de matriz por vector entonces este teorema también es valido para cualquier transformación lineal.

$$
\begin{aligned}
	\dim V &= R(T)+N(T) \\
		&= R(A_T) + N(A_T)
\end{aligned}
$$
