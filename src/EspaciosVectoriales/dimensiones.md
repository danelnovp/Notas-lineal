# Dimensiones

<mbox>

# Dimensión

Sea $B$ una base de un espacio vectorial $V$ decimos que $|B|$ (el cardinal de $B$) es la dimensión de $V$, esto lo denotamos como $\dim{V}$.

</mbox>

<mbox>

## Teorema 1

Sea $V$ un EV tal que $\dim V = m$ y $\vectores$ un conjunto de vectores LI de $V$, entonces $n\leq m$.

</mbox>

<demostracion>

Razonando de manera similar a la demostración del [Teorema 1 de bases](./bases_y_dimensiones.md#teorema-1) se llegaría a una contradicción sobre la independencia lineal de los vectores $\vectores$, por lo tanto se concluye que $n\leq m$. 

</demostracion>

> Este teorema nos asegura que la cantidad de vectores LI que podemos tener en un conjunto no debe superar la dimensión de su espacio vectorial. Por ejemplo si tenemos 4 vectores en $\R^3$ ya sabemos que no pueden ser LI.


<mbox>

## Teorema 2

Sea $V,W$ espacios vectoriales tal que $W\leq V$ ($W$ es SEV de $V$) entonces $\dim{W}\leq \dim{V}$.

</mbox>

<demostracion>

Digamos que $\dim{V}=n$ y supongamos que $\dim{W}\geq \dim{V}$, entonces podemos encontrar vectores $w_1,w_2,\dots,w_n,w_{n+1}\in W$ LI, esto es una contradicción por el teorema anterior, ya que implica que $W$ puede ser generado por estos $n+1$ vectores, por lo tanto implica que $V$ puede ser generado al menos por $n+1$ vectores LI, pero es una contradicción ya que solo pueden haber $n$ vectores LI en $V$, por lo tanto $\dim{W}\leq\dim{V}$.

</demostracion>

<mbox>

## Teorema 3

1. Cualquier conjunto de $n$ vectores LI en un espacio $V$ de dimensión $n$ constituyen una base de $V$.
2. Si tenemos que $\dim{V}=k$ donde $n\leq k$  podemos completar los $n$ vectores hasta tener $k$ vectores LI.

</mbox>

<demostracion>

Primero vamos a demostrar **1.** Supongamos que tenemos el conjunto $\vectores$ de $n$ vectores LI que no son base de $V$, esto quiere decir que existe un $v_{n+1}\in V - \generado{\vectores}$ tal que $\vectores, v_{n+1}$ es LI, por lo tanto $\generado{\vectores, v_{n+1}} = W$, como cada uno de estos vectores esta en $V$ entonces $W \leq V$, y por el [Teorema 2](#teorema-2) $\dim{W}\leq n$, pero $\dim{W} = n+1$, se llego a una contradicción con el teorema anterior, por lo tanto se concluye que $\vectores$ es una base de $V$

---

Ahora se demostrara **2.** Sea $W_1= \generado{\vectores}$, como $n< k$ entonces $W\lneq V$ por lo tanto existe un $v_{n+1}\in V-W_1$ tal que $\vectores,v_{n+1}$ son LI, ahora sea $W_2=\generado{\vectores,v_{n+1}}$, si $W_2=V$ entonces la prueba termina, sino continuamos con el mismo argumento, es decir, existe $v_{n+2}\in V-W_2$ tal que $W_3=\generado{\vectores,v_{n+1},v_{n+2}}$, si $W_3=V$ terminamos, sino continuamos de forma iterativa hasta conseguir un espacio vectorial $W_k=\generado{\vectores,v_{n+1},\cdots,v_k}=V$.

</demostracion>
