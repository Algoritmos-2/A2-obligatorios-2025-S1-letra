# Ejercicio 1 - Emails

**Nombre de archivo:** `ejercicio1.cpp` o `Ejercicio1.java`

## Descripción

Se tiene una base de datos de usuarios identificados por su dirección de correo electrónico. Se detectó que existen usuarios duplicados (que comparten el mismo e-mail). El objetivo es determinar cuántos usuarios únicos hay en realidad.

## Entrada

- La primera línea contiene un entero positivo **N** (2 ≤ N ≤ 10^5), que indica el número de usuarios registrados actualmente en el sistema.
- Las siguientes **N** líneas contienen cada una un correo electrónico registrado.

## Salida

- Imprimir un único entero: la cantidad total de usuarios únicos (sin repetidos).

## Restricciones

- Se debe usar una **tabla hash cerrada**.
- Resolver con complejidad temporal promedio **O(N)**, siendo **N** la cantidad de usuarios.

## Ejemplos

### Entrada

```
5
abc@abc.com
cba@cba.com
abc@abc.com
abc@abc.com
aaa@aaa.com
```

### Salida

```
3
```

### Explicación

Existen tres e-mails únicos: `abc@abc.com`, `cba@cba.com` y `aaa@aaa.com`.
