# Ejercicio 2 - Diccionario

**Nombre de archivo:** `ejercicio2.cpp` / `Ejercicio2.java`

## Descripción

Se tiene un diccionario con palabras almacenadas, y se quiere verificar si una serie de palabras dadas están contenidas en dicho diccionario. Para esto, implementar una solución usando una tabla de hash cerrado con resolución de colisiones mediante **doble hashing**.

## Entrada

- La primera línea contiene un entero **N** (1 ≤ N ≤ 10^6), indicando la cantidad de palabras en el diccionario.
- Las siguientes **N** líneas contienen cada una una palabra del diccionario, cada una con una longitud máxima de 20 caracteres.
- Luego, una línea contiene un entero **M** (1 ≤ M ≤ 10^6), indicando la cantidad de palabras a consultar.
- Las siguientes **M** líneas contienen cada una una palabra para verificar si existe en el diccionario.

## Salida

- Imprimir **M** líneas, una por cada palabra de consulta, indicando:
  - `1` si la palabra existe en el diccionario.
  - `0` si la palabra no existe en el diccionario.

## Restricciones

- La implementación debe utilizar una tabla hash cerrada con **doble hashing**.
- Las palabras tendrán una longitud máxima de 20 caracteres.
- Complejidad esperada promedio para las operaciones de búsqueda e inserción: `O(1)`.

## Ejemplo

### Entrada

```
5
casa
perro
gato
árbol
cielo
4
gato
flor
cielo
mar
```

### Salida

```
1
0
1
0
```

### Explicación

- "gato" y "cielo" están en el diccionario, mientras que "flor" y "mar" no lo están.

