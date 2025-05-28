# Ejercicio 6 - Que linda vista

## Descripción

Dada una vista horizontal de una ciudad que consta únicamente de edificios rectangulares, le piden diseñar un algoritmo que dada la ubicación y altura exacta de los edificios de la ciudad, halle la “silueta” o línea de corte de todos los edificios con el cielo, es decir, la silueta de todos los edificios juntos, pero eliminando las intersecciones ocultas entre los mismos. Por ejemplo, sean los siguientes cinco edificios (en la parte A):

![alt text](edificios.jpg)

Los mismos se representarán mediante la secuencia de ternas [(2,9,10), (3,7,15), (5,12,12), (15,20,10), (19,24,8)]. Donde cada terna `(I,F,H)`, representa:

- `I`: Coordenada en el eje horizontal donde comienza el edificio
- `F`: Coordenada en el eje horizontal donde termina el edificio
- `H`: La altura del edificio

Se pide imprimir una secuencia de pares `(x,h)` que representan una posicion de la cual a partir de la posicion `x` la figura tiene altura `h`. De esta forma, podemos representar la misma silueta utilizando menos memoria.

Aclaraciones: 

1. No incluir el par `(0,0)`
2. No puede haber dos pares seguidos con la misma altura.

## Entrada

```txt
N
I1 F1 H1
I2 F2 H2
...
IN FN HN
```

Donde:

- `N` es la cantidad de edificios
- Le siguen N lineas conteniendo `I F N` representando los edificios

## Salida

```txt
X1 H1
X2 H2
...
XK HK
```

## Restricciones

Implementar la solucion con la tactica de **Divide & Conquer**

$O(N * log\ N)$ siendo N la cantidad de edificios.

## Ejemplo

### Input

```txt
5
2 9 10
3 7 15
5 12 12
15 20 10
19 24 8
```

### Output

```txt
2 10
3 15
7 12
12 0
15 10
20 8
24 0

```

### Explicación

Si volvemos a la imagen. Podemos ver que hasta la posicion 2, no hay ningun edificio.

A partir de la posicion 2, empieza un edificio con altura de 10.

En la posicion 3 hay un edificio que tiene altura de 15.

A pesar de que hay otro edificio que empieza en la posicion 5, como el edificio rojo es mas alto, lo ignoramos hasta que el edificio rojo se termina en la posicion 7, en la cual la altura baja hasta 12.

En la posicion 12, se termina el edificio verde, así que la altura baja a 0.

En la posicion 15, aparece un edificio de altura 10.

Ignoramos el inicio del edificio amarillo, ya que estamos a una altura mas alta.

Cuando se termina el edificio magenta, bajamos hasta la altura del edificio amarillo que es de 8.

Cuando se termina el edificio amarillo, bajamos a una altura de 0.
