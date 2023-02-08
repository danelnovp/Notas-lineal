# Independencia Lineal

Los vectores $(1, 2)$ y $(4, 8)$ tienen una relación muy cercana, la cual es que $(4,8)=4(1,2)$ es decir el segundo vector es una combinación lineal del primero, ahora supongamos que tenemos un conjuntos de vectores $\vectores$ donde al menos uno de ellos se puede escribir como combinación lineal de los demás, a este hecho se la llama dependencia lineal.

Es decir dentro de este conjunto de vectores existe un vector $v_i$ con $1\leq i \leq n$ tal que para unos escalares $\escalares$ se cumple que:
$$
v_i = \alpha_1 v_1 + \cdots + \alpha_{i-1} v_{i-1} + \alpha_{i+1} v_{i+1} + \cdots + \alpha_n v_n
$$
Ahora tomemos una combinación lineal de los mismos vectores $\vectores$ (incluyendo el $v_i$) donde los escalares son los mismos utilizamos en la combinación lineal del vector $v_i$, solo que el escalar que acompañara a $v_i$ sera $-1$:

$$
\begin{aligned}
    &= 
    \alpha_1 v_1 + \cdots + \alpha_{i-1} v_{i-1} + \bm{(-v_i)} + \alpha_{i+1}v_{i+1} + \cdots + \alpha_n v_n \\
    &=  
    \underbrace{
        \alpha_1 v_1 + \cdots + \alpha_{i-1} v_{i-1} + \alpha_{i+1} v_{i+1} + \cdots + \alpha_n v_n
    }_{=\displaystyle v_i} + \bm{(-v_i)} \\
    &= v_i - v_i \\
    &= 0
\end{aligned}
$$

Esto demuestra otra propiedad que tienen los conjuntos de vectores linealmente dependiente, existe una combinación lineal de ellos donde son iguales a 0, este hecho sera la definición utilizada de dependencia lineal.

<mbox>

# Dependencia lineal

Sea $\vectores$ un conjunto de vectores, decimos que son linealmente dependientes cuando existe un conjuntos de escalares $\escalares$ (no todos ceros) tal que:

$$
\combinacion = 0
$$

</mbox>

> Dentro del plano cartesiano los vectores linealmente dependientes son todos aquellos que se encuentran sobre la misma recta o son paralelos.

Pero cabe la posibilidad que para un conjunto de vectores no existan tales escalares, entonces solo puede existir una forma que una combinación lineal de estos vectores sea $0$, esta es donde todos los escalares son igual a $0$. El conjunto de vectores que cumplen esto se les llamara linealmente independientes.

<mbox>

# Independencia lineal

Si para un conjunto de vectores $\vectores$ y uno de escalares $\escalares$ se tiene que:
$$
\combinacion = 0
$$
solo cuando $\alpha_1 = \alpha_2 = \cdots = \alpha_n = 0$, se le llama al conjunto de vectores linealmente independientes.

</mbox>

> A partir de ahora se utilizaran las siglas LD para decir linealmente dependientes y LI para linealmente independientes.

## Determinar si es LI o LD

Hay muchas formas para determinar si un conjuntos de vectores es LI o LD, pero se mostraran las que se puedan usar por el momento a partir de la información mostrada anteriormente, también la de demostración se deja como ejercicio para el lector.

- Si en el conjunto $\set{\vectores}$ hay uno que es múltiplo del otro entonces es LD.
- Si $v_i \in \set{\vectores}$ y $v_i = 0$ entonces el conjunto es LD.
  
    **Justificación:** ya que el vector nulo puede ser escrito como combinación lineal de cualquier conjunto de vectores donde donde los escalares son 0.
- Si el conjunto $\set{\vectores}$ es LI entonces cualquier subconjunto de el también lo será.

    **Justificación:** Por definición un conjunto de vectores es LI cuando una combinación lineal de el es 0 si cada escalar es 0, por lo tanto podemos quitar cualquier vector y la combinación lineal seguirá siendo 0.