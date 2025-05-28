# Ejercicio 8 - Se rompió grep

## Descripción

Se rompió grep, y como buenos ingenieros, no se les ocurrió mejor idea que reescribirlo desde cero.

Dado un texto `t` formado por letras minúsculas, y un patrón `p` formado por letras minúsculas y dos carateres especiales `.` y `*`, de forma que:

- `.` representa a un caracter cualquiera
- `*` representa a 0 o más del caracter anterior

Se pide indicar si el texto cumple con el patrón.

## Entrada

```txt
texto
patron
```

## Salida

```txt
bool
```

`true` en caso de que se cumpla el patrón. `false` en caso contrario

## Restricciones

Orden temporal: $O(N*M)$

Orden espacial: $O(N*M)$

Donde `N` y `M` representan al texto y al patrón respectivamente

## Ejemplos

### Ejemplo 1

#### Input

```txt
aba
a
```

#### Output

```txt
false
```

#### Explicación

El texto no cumple el patrón, ya que tiene caracteres de más.

### Ejemplo 2

#### Input

```txt
aaa
a*
```

#### Output

```txt
true
```

#### Explicación

Como `*` significa 0 o más caracteres del anterior, el texto cumple con el patrón.

### Ejemplo 3

#### Input

```txt
babcbdb
a*.*
```

#### Output

```txt
true
```

#### Explicación

Según el patrón, puede haber 0 o más `a`s, así que el hecho que no empiece con una `a` no es un problema.

Queda resolver el `.*`, como `.` puede representar un caracter cualqueira, `.*` en consecuencia significa una cadena de caracteres cualquiera.

### Ejemplo 4

#### Input

```txt
abcbdb
a.*a
```

#### Output

```txt
false
```

#### Explicación

El patrón pide una palabra cualquiera que empiece con `a` y termine en `a`.
