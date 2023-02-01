# Sub espacios

Como si tratase de un conjunto los espacios vectoriales poseen subconjuntos, muchos de hecho, pero hay una clase de estos subconjuntos que son especiales, ya que cumplen con todos los axiomas de espacios vectoriales, por lo tanto también serian uno. Estos subconjuntos son llamados subespacios vectoriales.

> Se utilizaran las siglas $EV$ para decir espacio vectorial, y $SEV$ para subespacios vectoriales.

<mbox>

# Comprobar si es $\bold{SEV}$

Sea $W \sube V$, donde $V$ es $EV$, para comprobar si $W$ también lo es solo se tiene que verificar las siguientes propiedades:

- El vector nulo esta en $W$, es decir $0\in W$.
- $W$ es cerrado bajo la suma de $V$, es decir para todo par de elementos $v,w \in W$ se cumple que $v+w\in W$ y $v + w \in V$.
- $W$ es cerrado bajo la multiplicación de escalares de $V$, es decir, para todo elemento $w\in W$ y para cualquier escalar $\alpha \in \R$ se cumple que $\alpha v \in W$.

</mbox>

> Una forma directa de comprobar esto es demostrando que el vector $\alpha v + w$ esta en $W$, para $v,w\in W$ y $\alpha\in \R$.

<ejemplo>

Sea $W = \set{(x,0) \,|\, x\in\R}$, se demostrara que es $SEV$ de $\R^2$.

Si $x=0$ entonces $(0,0)\in W$, por lo tanto el vector nulo esta en $W$. Ahora sean $x, y, \alpha \in \R$, por lo tanto $(x,0),(y,0) \in W$, luego:
$$
\begin{aligned}
    \alpha (x, 0) + (y, 0) &= (\alpha x, \alpha 0) + (y, 0) \\
    &= (\alpha x, 0) + (y, 0) \\
    &= (\alpha x + y, 0) \in W
\end{aligned}
$$
se demostró que $W$ es cerrado bajo las operaciones de $\R^2$ por lo tanto es $SEV$.

</ejemplo>

> Este $EV$ visto de una manera geométrica corresponde al eje x del plano cartesiano.

<ejemplo>

Sea $G = \set{(x, \alpha x) \,|\, \alpha, x \in \R}$, ¿Sera $G$ $SEV$ de $\R^2$?, la respuesta es sí, se comprueba fácilmente que el vector nulo esta en $G$ si hacemos a $x=0$, ahora se demostrara que $G$ es cerrado bajo las operaciones de $\R^2$.

Sea $(x, \alpha x), (y, \alpha y) \in G$ y $\beta \in \R$ entonces:
$$
\begin{aligned}
    \beta(x, \alpha x) + (y, \alpha y) &=
    (\beta x, \beta\alpha x) + (y, \alpha y) \\
    &= (\beta x + y,\, \beta\alpha x + \alpha y) \\
    &= \big(\beta x + y,\, \alpha(\beta x + y)\big) \in G
\end{aligned}
$$

</ejemplo>

> El $SEV$ $G$ corresponde a las recta que pasan por el origen con pendiente $\alpha$.

<mbox>

# Subespacios vectoriales triviales

Si $V$ es $EV$ entonces tiene dos $SEV$ triviales, los cuales son $\set{0}$ (rápidamente se puede comprobar que es $EV$) y el mismo $V$.

</mbox>


## Operaciones de SEV

<mbox>

## Teorema 1 intersección

Sea $V$ un $EV$, la **intersección** de cualquiera de sus $SEV$ es otro $SEV$ de $V$.

</mbox>

<demostracion>

Sean $H_1, H_2$ SEV de $V$, se sabe que $H_1 \cap H_2 \neq \varnothing$ ya que ambos poseen el vector nulo. Ahora supongamos que $v,w \in H_1 \cap H_2$ y $\alpha \in \R$, como ambos vectores están en la intersección entonces $v, w \in H_1$ y $v,w \in H_2$ y como ambos son SEV entonces $\alpha v + w \in H_1$ y $\alpha v + w \in H_2$, se sigue que $\alpha v + w \in H_1 \cap H_2$, se concluye que $H_1 \cap H_2$ es SEV

</demostracion>

---

<mbox>

## Teorema 2 suma

Sea $H_1$ y $H_2$ SEV de $V$ decimos que la suma de los dos también lo es, es decir:
$$
H_1 + H_2 = \set{h_1 + h_2 \,|\, h_1 \in H_1, h_2 \in H_2}
$$
ademas es el menor SEV que contiene a $H_1$ y $H_2$.

</mbox>

<demostracion>

Supongamos que $h_1,h_2\in H_1+H_2$ entonces: 
$$
\begin{aligned}
    & h_1 = h + h' && h\in H_1, h'\in H_2 \\
    & h_2 = \bar{h}+\bar{h}' && \bar{h}\in H_1,\bar{h}'\in H_2 \\
    \therefore \ &  h_1+h_2=(h+\bar{h})+(h'+\bar{h}') && h+\bar{h} \in H_1, h'+\bar{h}' \in H_2 \\
    \therefore \ & h_1+h_2 \in H_1 + H_2
\end{aligned}
$$
Aquí se demostró que $H_1 + H_2$ es cerrado bajo la suma, ahora de demostrara que lo es con el producto de escalares. 

Sea $\alpha \in \R$ entonces $\alpha h_1 = \alpha(h + h') = \alpha h + \alpha h'$, como $\alpha h\in H_1$ y $\alpha h' \in H_2$ entonces $\alpha h_1 \in H_1 + H_2$

</demostracion>

> # *Notación*
> A partir de ahora se incluirá una notación para distinguir entre subconjunto y subespacio, diremos que $W \leq V$ para indicar que $W$ es SEV de $V$.

<mbox>

## Teorema 3 producto directo

Sean $V_1, V_2 \leq V$, el conjunto $V_1\times V_2=\{(v_1,v_2)\,|\, v_1\in V_1, v_2\in V_2\}$ dotado de las siguientes operaciones es EV:

- $$
(v_1,v_2){\large\bold +}(v_1',v_2') = (v_1+v_1',v_2+v_2')
$$
Donde el $+$ es la suma de vectores, no la de escalares.

- Sea $\alpha \in\R$ 
$$
\alpha {\large\bold\cdot}(v_1,v_2)= (\alpha\cdot v_1, \alpha \cdot v_2)
$$
donde $\cdot$ indica el producto de escalar por vector.

</mbox>

La demostración es larga y aburrida, es por eso que acudiré a "se le deja al lector como ejercicio". 