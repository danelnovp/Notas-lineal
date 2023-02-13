# Kernel e Imagen

Estos conceptos van a ser fundamentales cuando lleguemos a ver transformaciones lineales, pero por el momento solo las mostraremos utilizando matrices y vectores, en el siguiente capitulo veremos estas mismas ideas generalizadas para cualquier espacio vectorial.

> Utilizaremos la siguiente notación:
> 
> $$M_{m\times n}(\R) \qquad \text{Matrices reales de $m\times n$} \\ M_n(\R) \qquad \text{Matriz cuadrada de $n\times n$} $$

<mbox>

# Transformaciones lineales de matrices

Sea $A\in M_{m\times n}(\R)$ (una matriz de $m$ filas y $n$ columnas), a partir de ella podemos crear una función llamada **transformación lineal** que va de $\R^n$ a $\R^m$, la cual es definida como:

$$
T: \R^n\to\R^m \\
v\in\R^n \mapsto A\times v
$$

</mbox>

<ejemplo>

Sea $A$ la matriz definida como:
$$
A =\begin{bmatrix}
 1 & 2 & 3 \\
 2 & -1 & 0
\end{bmatrix}
$$
Una transformación lineal de esta matriz sera la siguiente:
$$
T:\R^3\to\R^2 \\
\begin{pmatrix}
x \\ y \\ z
\end{pmatrix}
\mapsto
A\begin{pmatrix}
x \\ y \\ z
\end{pmatrix} =
\begin{bmatrix}
x+2y+3z \\
2x-y
\end{bmatrix}
$$

</ejemplo>

## Kernel y nulidad

<mbox>

# Kernel

Sea $A\in M_{m\times n}(\R)$ y $T:\R^n\to\R^m$ una transformación lineal asociada a $A$. El kernel de una transformación lineal (denotado por $K(T)$) es un espacio vectorial definido como:
$$
K(T) = \set{x\in\R^n \,|\, Ax = 0_m}
$$

</mbox>

Es decir todos los vectores de $\R^n$ tal que al multiplicarse por $A$ dan como resultado el vector nulo de $\R^m$.

<mbox>

## Teorema 1

Sea $A\in M_{m\times n}(\R)$, sea $T:\R^n\to\R^m$ una transformación lineal asociada a esta matriz, el $K(A)$ es sub espacio vectorial de $\R^n$.

</mbox>

<demostracion>

Sea $v,w\in K(T)$ entonces $Av=Aw=0_m$ se sigue que $0_m=Av+Aw=A(v+w)$ se concluye que $v+w\in K(A)$, ahora con un escalar $\alpha\in\R$ se tiene que $A(\alpha v)=\alpha(Av)=\alpha 0_n=0_n$ por lo tanto $\alpha v\in K(A)$.

Como $K(T)$ es cerrado bajo la suma y la multiplicación por escalares, entonces se concluye que $K(T) \leq \R^n$.

</demostracion>

Ya que sabemos que $K(T)$ es un espacio vectorial, podemos preguntarnos por su dimensión, esta sera llamada **nulidad** y es muy importante.

<mbox>

# Nulidad

Sea $T$ una transformación lineal de una matriz $A$, definimos la **nulidad** de $T$ como la dimensión de su kernel:
$$
N(T) = \dim K(T)
$$

</mbox>

<ejemplo>

Sea $A$ una matriz definida como:

$$
A =
\begin{bmatrix}
	-1 & 3 & 2 \\
	2 & -6 & -4
\end{bmatrix}
$$

Para hallar el kernel se debe hallar la solución al siguiente sistema:
$$
A\times 
\begin{bmatrix}
x \\ y \\ z
\end{bmatrix}
= \begin{pmatrix}
    0 \\ 0 \\ 0
\end{pmatrix}
$$
De esto se tendrá el siguiente sistema homogéneo:
$$
\begin{aligned}
-x +3y+2z &= 0 \\
2x-6y-4z &= 0
\end{aligned}
$$
Dese cuenta que la segunda ecuación es $-2$ veces la primer por lo tanto se puede omitir y despejar de la primera $x$ de lo que queda $x=3y+2z$, a partir de esto obtenemos el siguiente vector:
$$
\begin{pmatrix}
	3y+2z \\ y \\ z
\end{pmatrix}
= 
\begin{pmatrix}
	3y \\ y \\ 0
\end{pmatrix}
+
\begin{pmatrix}
	2z \\ 0 \\ z
\end{pmatrix}
=y
\begin{pmatrix}
	3 \\ 1 \\ 0
\end{pmatrix}
+
z
\begin{pmatrix}
	2 \\ 0 \\ 1
\end{pmatrix}
$$
A partir de esto se tiene que estos dos vectores son la base de $K(T)$.
$$
K(T) = \generado{
    \begin{pmatrix}
	3 \\ 1 \\ 0
\end{pmatrix}
,
\begin{pmatrix}
	2 \\ 0 \\ 1
\end{pmatrix}
}
$$
y ademas su nulidad es:
$$
N(T) = \dim K(T) = 2
$$
Si tomamos cualquier combinación lineal de estos dos vectores y lo multiplicamos por nuestra matriz $A$ obtendremos como resultado $0$.

</ejemplo>

## Imagen y rango

<mbox>

# Imagen

Sea $A\in M_{m\times n}(\R)$ y $T:\R^n\to\R^m$. Definimos la imagen de $T$ como todos los vectores que viven sobre el rango de la transformación lineal, es decir:
$$
\im(T) = \set{y\in \R^m \,|\, Ax = y \quad \exist x \in \R^n}
$$

</mbox>

<mbox>

## Teorema 2

Sea $T$ una transformación lineal asociada a $A\in M_{m\times n}(\R)$. $\im(T)$ es sub espacio vectorial de $\R^m$

</mbox>

<demostracion>

Sea $x,y\in \im(T)$ entonces existen un $v,w\in\R^n$ tal que $x=Av$ y $y=Aw$ entonces $x+y=Av+Aw=A(v+w)$ como $v+w\in\R^n$ entonces $A(v+w)\in\im(T)$, Sea $\alpha\in\R$ entonces $\alpha x=\alpha(Av)=A(\alpha v)$ como $\alpha v\in\R^n$ entonces $A(\alpha v)\in \im(T)$.

Se demostro que $\im (T)$ es cerrada bajo la suma y el producto por escalares, por lo tanto $\im (T) \leq \R^m$.

</demostracion>

<mbox>

# Rango

El rango de una transformación $T$ no es más que la dimensión de su imagen:
$$
R(T) = \dim \im(T)
$$

</mbox>

## Algunos teoremas

<mbox>

## Teorema de la dimension (TD)

Sea $A$ una matriz de $m\times n$ y $T:\R^n\to\R^m$ una transformación de ella, entonces $n= R(T)+N(T)$, es decir el rango más la nulidad es igual al número de columnas de la matriz.

</mbox>

> Este teorema es uno de los más importantes en el álgebra lineal. Su demostración es bastante rigurosa y larga, si no esta interesado en ella puede omitirla.

<demostracion>

Sea $v_1,\cdots,v_{N(T)}$ una base para $K(T)$, como $K(T)\leq \R^n$, entonces podemos completar estos vectores tal que $v_1,\cdots,v_{N(T)},v_{N(T)+1},\cdots,v_n$ es una base de $\R^n$.

Dado cualquier $v\in\R^n$ existen un conjunto de escalares $\alpha_1,\cdots,\alpha_n$ tal que es combinación lineal de los vectores anteriores:
$$
v = \sum_{i=1}^n \alpha_i v_i
$$
Luego como $A\in M_{m\times n}(\R)$ entonces podemos multiplicarla por $v$, de lo que nos queda:
$$
Av = \sum_{i=1}^n \alpha_i A v_i
$$
Pero como los primeros $N(T)$ vectores pertenecen al kernel su producto por $A$ es igual al vector nulo por lo tanto podemos simplificar y hacer:
$$
Av = \sum_{i=N(T)+1}^n \alpha_i A v_i
$$
Como los vectores $v_{N(T)+1},\cdots,v_n$ son LI entonces $Av = \generado{v_{N(T)+1},\cdots,v_n}$, de esto se tiene que $\im(T) \leq \generado{v_{N(T)+1},\cdots,v_n} \leq \im(T)$, se concluye que $\im(T) = \generado{v_{N(T)+1},\cdots,v_n}$.

De lo anterior se tiene lo siguiente:
$$
\begin{aligned}
R(T) &= \dim \im(T)  \\
	&= \dim \{v_{N(T)+1},\cdots,v_n\} \\
	&= n-N(T) \\
	n &= R(T)+N(T)
\end{aligned}
$$

</demostracion>

<mbox>

## Teorema 3

Si $A\in M_{m\times n}(\R)$ y $T: \R^n \to \R^m$ entonces $A$ es uno a uno si y solo si $K(T)=\set{0_n}$ lo que equivale a decir $N(T)=0$.

</mbox>

> Recordemos que una función es uno a uno cuando para todo $x,y$ del dominio, $x \neq y$ entonces $f(x)\neq f(y)$.

<demostracion>

Primero se va a demostrar que si la transformación es 1-1 entonces $N(T) = 0$.

Si tomamos a $Av = 0_m$ entonces $Av = A0_n$ y como la función es 1-1 no puede existir otro valor de $v$ que cumpla esto por lo tanto $v=0_n$ y como este es el único valor que al multiplicarlo por $A$ da $0_m$ entonces $K(T)=\{0_n\} \implies N(T) = 0$.

Ahora supongamos que $N(T) = 0$, y se va a demostrar que la transformación es 1-1.

Supongamos que $Av=Aw$ por lo tanto $Av-Aw = 0_m = A(v-w)$ como $v-w\in K(T)$ y $K(T)=\{0_n\}$ entonces $v-w=0_n \implies v=w$ por lo tanto la aplicación es 1-1.

</demostracion>

<mbox>

## Corolario del TD

Sea $A\in M_{m\times n}(\R)$ y $T:\R^n\to \R^m$

1. Si $n<m$, $T$ no puede ser sobreyectiva.
2. Si $n>m$, $T$ no puede ser inyectiva.
3. si $n=m$, entonces $T$ es sobreyectiva si y solo si $T$ es 1-1.

</mbox>

<demostracion>

Se demostraran cada uno de los corolarios.

1. Si $n<m$ entonces por el teorema de la dimensión $R(T) = n-N(T)\leq n$ por lo tanto $R(T)<m$, se concluye que $T$ no puede ser sobreyectiva.
2. Si $n>m$, por el teorema de la dimensión $N(T)=n-R(T)>m-R(T)\geq 0$, se tiene que $N(T)>0$ por lo tanto $T$ no puede ser inyectiva.
3. Si $n=m$, por el teorema de la dimensión $R(T)=n\iff N(T)=0$, luego por los ítems anteriores queda que $T$ es 1-1.

</demostracion>