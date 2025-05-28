# Ejercicio 10 - Sudoku

## Descripción

Un amigo experto en sudoku quiere hacer una competencia con usted en sudoku competitivo. Este sudoku competitivo tiene una variación respecto al sudoku común. Esta variación es que tiene tableros de distintas dimenciones, como por ejemplo 9x9, 12x9, 9x12, etc. Dado que usted no es muy bueno en sudoku, pero no quiere perder contra su amigo decide hacer trampa. Para ello, hara un programa que dado un tablero de sudoku, le imprime la solución del mismo.

Las reglas del sudoku son las siguientes:

- En una fila no puede haber dos números repetidos.
- En una columna no puede haber dos números repetidos.
- Si dividimos el tablero en 9 bloques (de `filas totales/3` filas * `columnas totales/3` columnas), en cada bloque no puede haber números repetidos. Y los números del 1 al k, sin saltearse ningún número.

## Entrada

```txt
<filas> <columnas>
<fila 1>
...
<fila final>
```

## Salida

```txt
<fila 1>
...
<fila final>
```

## Ejemplo

### Input

```txt
9 9
2 1 3 6 9 8 4 5 7
5 6 7 1 2 4 3 8 9
4 8 9 7 5 3 1 6 2
3 2 1 0 6 9 5 7 8
6 4 0 8 0 7 2 9 3
7 0 8 2 3 5 6 1 4
1 7 2 3 0 6 0 4 5
8 5 6 9 0 2 7 0 1
9 3 0 5 7 1 8 2 6
```

### Output

```txt
2 1 3 6 9 8 4 5 7
5 6 7 1 2 4 3 8 9
4 8 9 7 5 3 1 6 2
3 2 1 4 6 9 5 7 8
6 4 5 8 1 7 2 9 3
7 9 8 2 3 5 6 1 4
1 7 2 3 8 6 9 4 5
8 5 6 9 4 2 7 3 1
9 3 4 5 7 1 8 2 6

```
