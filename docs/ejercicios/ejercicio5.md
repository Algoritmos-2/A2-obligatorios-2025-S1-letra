# Ejercicio 5 - Ciclicidad

**Nombre de archivo:** `ejercicio5.cpp` / `Ejercicio5.java`

## Descripción

Dado un grafo disperso, dirigido y sin ponderar, implementar un algoritmo eficiente que determine si existe al menos un ciclo en él.

## Entrada

La entrada debe seguir este formato:

```
V
E
v1 w1
v2 w2
...
vE wE
```

Donde:

- `V` es la cantidad de vértices.
- `E` es la cantidad de aristas.
- Las siguientes `E` líneas indican las aristas dirigidas del vértice `vi` al vértice `wi`.

## Salida

Imprimir una sola línea con:

- `1` si el grafo contiene al menos un ciclo.
- `0` si el grafo no contiene ciclos.

## Restricciones

- Complejidad temporal: $O(V + E)$.

## Ejemplo

### Entrada

```
4
4
1 2
2 3
3 4
4 2
```

### Salida

```
1
```

### Explicación

El grafo contiene un ciclo: 2 → 3 → 4 → 2.

