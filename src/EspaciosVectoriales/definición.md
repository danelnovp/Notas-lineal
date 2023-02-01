# Espacios Vectoriales

¿Que tienen en común los números reales, los vectores y las matrices de cualquier dimensión?, puede que ahora no se le ocurra una respuesta del todo clara, puede que si lo halla pensado suficiente solo encuentre dos similitudes entre todas estas, si aun no lo encuentra se trata de la multiplicación de escalares y la suma. Ya que todos comparten las propiedades de que la suma es conmutativa y asociativa, es decir si tomamos a $A,B,C$ matrices $n\times m$ se tiene que:

$$
\begin{matrix}
    A + B = B + A & \text{Conmutatividad} \\
    A + (B + C) = (A + B) + C & \text{Asociatividad}
\end{matrix}
$$

Esto se cumple tanto para los vectores como para los reales.

Y ahora la multiplicación por escalares resulta trivial hablar de ella.

## Definición formal

Definimos a un espacios vectorial como un conjunto no vació $V$ de objetos llamados vectores, que consta de dos operaciones, la suma y la multiplicación por escalares de un cuerpo $\mathbb{F}$, ademas los espacios vectoriales deben cumplir con los siguiente axiomas.

1. Tener un cuerpo $\mathbb{F}$ de escalares.
2. Un conjunto $V$ de objetos llamados vectores.
3. Una regla llamada adición tal que para $v,j,k \in V$ cumple que::
   - Es conmutativa $v+j = j+v$
   - Asociativa $v+(j+k)=(v+j)+k$
   - Existe un vector nulo denotado por $0$ tal que para todo vector $v\in V$ se cumple que $v+0 = v$
   - Para cada vector $v\in V$ existe un vector $-v\in V$ tal que $v-v = 0$. este vector lleva por nombre inverso de $v$.
4. Una operación llamada producto por escalar que asocia un escalar $\alpha \in \mathbb{F}$ con un vector $v\in V$ a un nuevo vector $\alpha\cdot v \in V$ tal que cumple:
   - Existe un escalar denotado por $1$ tal que $1\cdot v = v$ para todo $v\in V$.
   - Sea $\alpha, \beta \in \mathbb{F}$, $(\alpha\cdot\beta)\cdot v = \alpha\cdot(\beta\cdot v)$
   - Es distributiva con respecto a la suma de vectores. $\alpha\cdot(v+j) = \alpha\cdot v + \alpha\cdot j$.
   - Sea $\alpha,\beta \in \mathbb{F}$ y $v\in V$, los vectores distribuyen con respecto a la suma de escalares: $(\alpha+\beta)\cdot v = \alpha\cdot v + \beta\cdot v$      

> # Sobre los cuerpos
> Normalmente el cuerpo $\mathbb{F}$ de escalares es $\R$, y el concepto de cuerpo es visto en clases de álgebra abstracta, en este caso un cuerpo es una estructura algebraica en donde se pueden sumar y multiplicar sus elementos, y que cumplen con las propiedades de la conmutatividad, asociatividad y distributiva además la existencia de un inverso multiplicativo y aditivo para cada elemento del cuerpo incluyendo los elementos neutros para las dos operaciones, estos serian las propiedades ya conocidas que permiten hacer aritmética.

> # *Nota*
> Se utilizaran letras del alfabeto $v,j,k,\cdots$ para denotar vectores y letras griegas $\alpha,\beta,\gamma,\cdots$ para denotar escalares de un cuerpo. Omitiremos escribir el punto en la multiplicación por escalares, es decir, en lugar de $\alpha \cdot v$ escribiremos $\alpha v$.

<ejemplo>

El espacio de vectores $\R^n$ (normalmente conocido como espacio cartesiano).

Sea $\R^n$ el conjunto de todas las tuplas de tipo $v = (x_1, x_2, \cdots, x_n)$ donde cada $x_i\in\R$. Si $j=(y_1, y_2, \cdots, y_n)$ donde cada $y_i\in\R$, la suma de $v+j$ se define como:
$$
v+j = (x_1+y_1, x_2+y_2, \cdots, x_n+y_n)
$$
y el producto por un escalar $\alpha\in\R$ como:
$$
\alpha v = (\alpha x_1, \alpha x_2, \cdots, \alpha x_n)
$$

Es fácil demostrar que el espacio cumple los axiomas de los espacios vectoriales. 

</ejemplo>

<ejemplo>

El conjunto de matrices $\R^{n\times m}$ es espacio vectorial. Se define la suma de dos vectores $A, B \in \R^{n\times m}$ como:
$$
(A+B)_{ij} = A_{ij} + B_{ij}
$$
Es decir, se suma un elemento de una fila $i$ y columna $j$ en $A$ con su respectivo elemento en la misma posición en $B$.

El producto de un escalar $\alpha\in\R$ definido como:
$$
\alpha A_{ij}
$$
Es decir se multiplica cada elemento de la matriz con el escalar $\alpha$.

</ejemplo>

## Teoremas

<mbox>

## Teorema 1.

El inverso $-v$ de $v$ es único, además $-v = (-1)v$ con $(-1)\in\R$.

</mbox>

<demostracion>

Supongamos que $w$ y $w^{\prime}$ son inversos de $v$.

$$
\begin{aligned}
    v+w &= v+w^{\prime} \\
    v+w+w^{\prime} &= v+w^{\prime}+w^{\prime} \\
    (v+w^{\prime}) + w &= (v+w^{\prime})+w^{\prime} \\
    0 + w &= 0 + w^{\prime} \\
    w &= w^{\prime}
\end{aligned}  
$$

Se demostro que $w=w^{\prime}$ por lo tanto el inverso de un vector es único.

Ahora vamos a demostrar que $-v = (-1)v$.

Sea $v\in V$.
$$
\begin{aligned}
            0 &= 0v                 \\
              &= (1+(-1))v          \\
              &= v + (-1)v          \\
    0 + (-v)  &= v + (-1)v + (-v)   \\
           -v &= (-1)v
\end{aligned}
$$

</demostracion>

<mbox>

## Teorema 2

Sea $\alpha \in \R$ y $v\in V$. Si $\alpha v = 0$ entonces $\alpha = 0$ 0 $v=0$.

</mbox>

<demostracion>

Supongamos que $\alpha = 0$.
$$
\begin{aligned}
                  v 0 &= v (0 + 0) \\
                           &= v 0 + v 0 \\
    v 0 + (-v 0 )&= v 0 + v 0 + (-v 0) \\
                         0 &= v 0
\end{aligned}
$$

Ahora supongamos que $\alpha \neq 0$.
$$
\begin{aligned}
    \alpha v &= 0 \\
    \left(\frac{1}{\alpha}\right)\alpha v &=  \left(\frac{1}{\alpha}\right) 0 \\
     \left(\frac{1}{\alpha}\alpha\right) v &= 0 \\
     v &= 0
\end{aligned}
$$

</demostracion>
