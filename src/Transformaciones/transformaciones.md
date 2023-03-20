# Transformaciones Lineales

En las notas sobre espacios vectoriales vimos los conceptos de Kernel e Imagen, y para poder explicarlos tuvimos que introducir una función $T$ tal que $T:\R^n \to \R^m$, esto limitados a utilizar solo matrices de $m$ filas y $n$ columnas, pero podemos extender este concepto para cualquier espacio vectorial, así pues una transformación lineal se tratara simplemente de una función que va de un espacio vectorial a otro. 

<mbox>

# Transformaciones lineales

Sean $V$ y $W$ espacios vectoriales. Una transformación lineal $T$ es una función que asigna a un vector $v\in V$ un vector $w\in w$, ademas de satisfacer las siguientes propiedades:

1. Si $v_1, v_2 \in V$ entonces $T(v_1 + v_2) = T(v_1) + T(v_2)$.
2. Si $\alpha \in \R$ y $v\in V$ entonces $T(\alpha v) = \alpha T(v)$.

</mbox>

> Utilizando la notación que se emplea en funciones se puede describir a $T$ de la siguiente manera: 
>$$
\begin{aligned}
	T: V&\to W \\
	v\in V &\mapsto  T(v)\in W
\end{aligned} $$
> Siendo $V$ y $W$ espacios vectoriales.

<ejemplo>

Sea $T:\R\to\R$ con $T(x)=x^2$ no es transformación lineal, tome un $x,y\in\R$, entonces se supone que $T(x+y)=T(x)+T(y)=x^2+y^2$, pero esto es falso ya que $T(x+y)= (x+y)^2 \neq x^2+y^2$.

</ejemplo>

<ejemplo>

Sea $T:\R\to\R^2$ siendo $T(x)=(x,\alpha x)$, donde $\alpha \in \R$, $T$ es transformación lineal.

En efecto tome un $x,y\in\R$, entonces $T(x+y)=(x+y, \alpha(x+y))= (x,\alpha x)+(y,\alpha y) = T(x)+T(y)$. Ahora tome un $c\in\R$ entonces $T(cx)= (cx,\alpha cx) = c(x,\alpha x)= cT(x)$.

</ejemplo>