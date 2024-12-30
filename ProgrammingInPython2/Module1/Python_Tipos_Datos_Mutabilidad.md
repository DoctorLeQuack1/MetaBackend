
# Tipos de datos en Python y su mutabilidad

Python es un lenguaje de programación que soporta varios tipos de datos integrados. Estos se dividen en dos categorías principales: **mutables** e **inmutables**.

---

## Tipos de datos inmutables

Los tipos de datos inmutables no pueden ser modificados después de su creación. Si se intenta cambiar el valor, se crea un nuevo objeto en lugar de modificar el existente.

### 1. **Números**
Incluyen `int`, `float`, `complex`.
- Ejemplo:

```python
x = 10
print(x)  # 10
x = x + 1
print(x)  # 11
# Aunque parezca que x cambió, en realidad se creó un nuevo objeto.
```

### 2. **Cadenas de texto (str)**
Las cadenas son inmutables.
- Ejemplo:

```python
s = "Hola"
s_modificada = s + " Mundo"
print(s)          # Hola
print(s_modificada)  # Hola Mundo
# 's' permanece sin cambios.
```

### 3. **Tuplas (tuple)**
Las tuplas son secuencias inmutables.
- Ejemplo:

```python
tupla = (1, 2, 3)
# Intentar modificar una tupla generará un error.
# tupla[0] = 10  # Esto lanza un TypeError.
```

### 4. **Conjuntos inmutables (frozenset)**
Un conjunto inmutable es como un conjunto normal, pero no puede ser modificado.
- Ejemplo:

```python
fs = frozenset([1, 2, 3])
# fs.add(4)  # Esto lanza un AttributeError.
```

---

## Tipos de datos mutables

Los tipos de datos mutables pueden ser modificados después de su creación, permitiendo alterar su contenido.

### 1. **Listas (list)**
Las listas son colecciones ordenadas de elementos que se pueden modificar.
- Ejemplo:

```python
lista = [1, 2, 3]
lista.append(4)
print(lista)  # [1, 2, 3, 4]
lista[0] = 10
print(lista)  # [10, 2, 3, 4]
```

### 2. **Diccionarios (dict)**
Los diccionarios almacenan pares clave-valor y son mutables.
- Ejemplo:

```python
diccionario = {"a": 1, "b": 2}
diccionario["c"] = 3
print(diccionario)  # {'a': 1, 'b': 2, 'c': 3}
diccionario["a"] = 10
print(diccionario)  # {'a': 10, 'b': 2, 'c': 3}
```

### 3. **Conjuntos (set)**
Los conjuntos son colecciones de elementos únicos y son mutables.
- Ejemplo:

```python
conjunto = {1, 2, 3}
conjunto.add(4)
print(conjunto)  # {1, 2, 3, 4}
```

---

## Resumen

| Tipo de dato    | Mutable     | Ejemplo                |
|-----------------|-------------|------------------------|
| `int`, `float`, `complex` | No          | `x = 10`            |
| `str`           | No          | `s = "Hola"`          |
| `tuple`         | No          | `tupla = (1, 2, 3)`   |
| `frozenset`     | No          | `fs = frozenset([1, 2, 3])` |
| `list`          | Sí          | `lista = [1, 2, 3]`   |
| `dict`          | Sí          | `diccionario = {"a": 1}` |
| `set`           | Sí          | `conjunto = {1, 2, 3}` |

---

## Nota sobre la mutabilidad

La mutabilidad afecta cómo los datos se comportan al ser pasados a funciones. Los tipos mutables pueden ser modificados dentro de una función, mientras que los inmutables no.

### Ejemplo:

```python
# Tipo inmutable
def modificar_numero(n):
    n = n + 1

x = 10
modificar_numero(x)
print(x)  # 10, no cambió.

# Tipo mutable
def modificar_lista(lista):
    lista.append(4)

l = [1, 2, 3]
modificar_lista(l)
print(l)  # [1, 2, 3, 4], sí cambió.
```
