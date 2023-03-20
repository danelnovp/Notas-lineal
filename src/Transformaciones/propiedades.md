# Propiedades de las Transformaciones Lineales

En esta nota se listaran algunas propiedades, además se incluirán en lo posible sus demostraciones (si es que no me da paja redactarlas, o pensar una original, aunque como carezco de creatividad matemática, puedo afirmar que esta nota no tendrá demostraciones originales, y si las hay son las triviales, las que se le ocurren a todo mundo, ya me extendí mucho, por eso a veces es bueno omitir los paréntesis en un texto).

> Decimos que una transformación $T\in L(V,W)$, donde $L(V,W)$ es el conjunto de todas las transformaciones lineales que van de $V$ a $W$.

<mbox>

## Teorema 1

Sean $T:V\to W$, y $v,w\in V$ entonces:

$$
T(v-w)= T(v)- T(w)
$$

</mbox>

<demostracion>

$$
\begin{aligned}
	T(\alpha-\beta) &= T(\alpha+(-1)\beta) \\
		&= T(\alpha)+T((-1)\beta) \\
		&= T(\alpha)+(-1)T(\beta) \\
		&= T(\alpha)-T(\beta) \\
\end{aligned}
$$

</demostracion>

<mbox>

## Teorema 2

Sea $T:V\to W$, donde $\set{\vectores}$ es una base de $V$, sean $w_1,\cdots,w_n$ vectores cualesquiera de $W$, tal que $T(v_j)=w_j$ con $j=1,\cdots,n$. Entonces $T$ es una transformación lineal.

</mbox>

<demostracion>

Dado un $v\in V$ existe una única combinación lineal tal que $v=\combinacion$, donde cada $\alpha_i \in \R$, definimos:
$$
T(v) = \alpha_1 w_1+\cdots+\alpha_n w_n
$$
Para demostrar que es lineal tenemos que mostrar que $T(v+v')=T(v)+T(v')$ y además $T(\alpha v)=\alpha T(v)$, para un $\alpha \in\R$. Definamos un vector $v'\in V$ con la combinación $v'=\beta_1v_1+\cdots \beta_nv_n$, donde $\beta_i\in\R$. Ahora por nuestra definición tenemos:

$$
\begin{aligned}
	T(v+v') &= T\big((\combinacion)+(\beta_1v_1+\cdots \beta_nv_n)\big) \\
		&= T((\alpha_1+\beta_1)v_1+\cdots+(\alpha_n+\beta_n)v_n) \\
		&= (\alpha_1+\beta_1)w_1+\cdots+(\alpha_n+\beta_n)w_n
\end{aligned}
$$

Como $T(v+v')=T(v)+T(v')$, entonces $T$ cumple con la primera condición de las combinaciones lineales, la demostración de que $\alpha T(v)=T(\alpha v)$, para $\alpha \in\R$, es análoga a la hecha anteriormente, por lo tanto concluimos de que $T$ es transformación lineal.

</demostracion>

> Este teorema nos da una herramienta muy útil para construir transformaciones lineales, solo tenemos que establecer una imagen para cada uno de los vectores de la base del espacio vectorial del dominio.

<mbox>

## Corolario 1

Sea $T'(v_j)=w_j$, entonces $T(v)=T'(v)$. Es decir que la transformación lineal $T$ es única.

</mbox>

<demostracion>

La demostración de este corolario es sencilla, solo coja un vector $v=\combinacion$, luego evaluemos en ambas transformaciones y llegara a que $T=T'$.

</demostracion>

> Este teorema solo es valido cuando la correspondencia de los vectores de la base de $V$, con algunos vectores de $W$ es la misma, es decir si cogemos diferentes vectores de $W$, la transformación lineal sera diferente.

<mbox>

## Teorema 3

Sea $T\in L(V,W)$, entonces $T(0_V) = 0_W$. Esto nos afirma que la imagen del vector nulo del dominio es igual al vector nulo del rango.

</mbox>

<demostracion>

$$
\begin{aligned}
	T(0_v) &= T(0_v +0_v) \\
		&= T(0_v) + T(0_v) \\
	T(0_v) - T(0_v)	 &= T(0_v) \\
	0_w &= T(0_v)
\end{aligned}
$$

</demostracion>

<mbox>

## Teorema 4

Si $T,T'\in L(V,W)$ entonces $T+T'\in L(V,W)$.

</mbox>

<demostracion>

$$
\begin{aligned}
	(T+T')(v_1+v_2) &= T(v_1+v_2)+T'(v_1+v_2) \\
		&= T(v_1)+T(v_2)+T'(v_1)+T'(v_2) \\
		&= (T+T')(v_1)+(T+T')(v_2)
\end{aligned}
$$
Demostramos que $(T+T')$ cumple con la primera condición de las transformaciones lineales, ahora lo demostraremos la propiedad de los escalares. Sea $\alpha
\in\R$:
$$
\begin{aligned}
	(T+T')(\alpha v) &= T(\alpha v)+T'(\alpha v) \\
		&= \alpha T(v)+\alpha T'(v) \\
		&= \alpha (T(v)+T'(v)) \\
		&= \alpha (T+T')(v)
\end{aligned}
$$

Con esto se demuestra que $(T+T')\in L(V,W)$.

</demostracion>

---

Este teorema tiene implicaciones muy grandes, se acabo de demostrar que la suma de dos transformaciones lineales pertenece al conjunto de transformaciones lineales, por lo tanto $L(V, W)$ es cerrado bajo la suma, al igual que la multiplicación por escalares, de esto se concluye que $L(V, W)$ es un espacio vectorial.

una pregunta que surge es sobre la dimensión de este espacio vectorial, la intuición nos sugiere que es infinita, ya que existen infinitas transformaciones lineales entre dos espacios vectoriales, pero sorprendente-mente la dimensión es finita y es:
$$
\dim L(V,W) = \dim V \cdot \dim W
$$
La demostración se deja como ejercicio para el lector, no mentiras, por el momento no se como demostrar esta vaina.

<mbox>

## Teorema 5

Sea $T: V\to W$ entonces:

1. $\im(T) = \set{T(v) : v\in V} \leq W$, es decir las imágenes de la transformación es un subespacio de $W$.
2. $K(T)=T^{-1}(0)=\set{v\in V : T(v)=0}\leq V$, es decir el kernel de $T$ es un SEV de $V$.

</mbox>

<demostracion>

Se demostrara **1**.

Sea $v,w\in V$ entonces $T(v)+T(w) = T(v+w) \in \im(T)$, sea $\alpha \in \R, v\in V$ entonces $\alpha T(v) = T(\alpha v)\in\im(V)$.

Se demostrara **2**.

Sean $v,w\in K(T)$, es decir $T(v)=T(w)=0$ entonces $T(v)+T(w)=0=T(v+w)$, se sigue que $v+w\in K(T)$. Sea $\alpha\in\R$ y $v\in K(T)$, se tiene que $T(v)=0$, entonces $\alpha T(v)= T(\alpha v)= 0$, se concluye que $\alpha v \in K(T)$.

</demostracion>

<mbox>

## Teorema 6

$T$ es biyectiva (uno a uno) si y solo si $K(T)=\set{0_V}$.

</mbox>

<demostracion>

Suponga que $T$ es 1-1, si $T(v)=0$ entonces $T(v)=T(0)$, esto implica que $v=0$ por lo tanto $K(T)=\set{0}$.
Ahora supongamos que $K(T)=\set{0}$. Si $T(v)=T(w) \implies T(v)-T(w)=0$, por lo tanto, $T(v-w)=0$ , como $v-w\in K(T)$ entonces $v=w=0$, se demuestra que $T$ es 1-1.

</demostracion>

<mbox>

## Corolario 2

Si $T$ es 1-1 y $\set{\vectores}$ es L.I, entonces la imagen de cada uno de estos vectores también lo es, es decir, $\set{T(v_1),\cdots,T(v_n)}$ es L.I.

</mbox>

<demostracion>

Sea $T\in L(V,W)$. Tenemos que $\generado{\vectores} \leq V$ y además son L.I, supongamos que:
$$
\begin{aligned}
	& \alpha_1T(v_1)+\cdots + \alpha_nT(v_n) = 0 \in W \\
	\implies& T(\combinacion) = 0
\end{aligned}
$$
Pero como $T$ es 1-1 entonces $\combinacion = 0$, además $\set{\vectores}$ son L.I, por lo tanto cada $\alpha_i =0$, se concluye que $\set{T(v_1),\cdots,T(v_n)}$ es L.I:

</demostracion>

<mbox>

## Teorema 7

Si $\generado{\vectores} = V$ entonces $\left< T(v_1), \cdots, T(v_n) \right> = \im(T)$. En particular  si $T$ es sobre entonces $\generado{T(v_1),\cdots, T(v_n)} = W$.

</mbox>

<demostracion>

No es una demostración como tal sino un argumento, si suponemos que $\generado{\vectores} = V$ y $T \in L(V,W)$ entonces todo vector $v \in V$ es una combinación de los vectores de la base de $V$, por definición de la imagen tenemos que:
$$
\im \, T = \set{T(v) \in W : v\in V}
$$
 Pero todo vector $v$ es combinación lineal de la base de $V$ por lo tanto todo $T(v)$ será la transformación de la combinación lineal de estos vectores por lo tanto $\generado{T(v_1), \cdots , T(v_n)} = \im \, T$, luego si $T$ es sobre entonces cada vector de $W$ tienen asociado a él un vector de $V$, entonces $\im \, T = W$.  

</demostracion>