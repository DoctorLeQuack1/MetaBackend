
# Python Basic Data Type and Function Cheatsheet

## Data Types

| **Data Type** | **Meaning** | **Example**         |
|---------------|-------------|---------------------|
| `string`      | Text        | `'Hello'`, `'Testing 123'` |
| `integer`     | Numbers     | `-5`, `4`, `3`, `2`, `0`  |
| `float`       | Decimals    | `2.4`, `5.2`, `1000.00`    |

---

## Flow Control

### Comparison Operators

| **Operator** | **Meaning**             | **Example** |
|--------------|-------------------------|-------------|
| `==`         | Equals                  | `a == b`    |
| `!=`         | Not Equal               | `a != b`    |
| `<`          | Less than               | `a < b`     |
| `>`          | Greater than            | `a > b`     |
| `<=`         | Less than or Equal to   | `a <= b`    |
| `>=`         | Greater than or Equal to| `a >= b`    |

---

## Comments

### Single-line comments
Placing a `#` symbol in front of the text causes Python to ignore everything from that point until the end of the current line.

```python
# Single Line comment
```

### Multi-line comments
Python does not have a specific syntax for multi-line comments, so a `#` symbol can be used on every line.

```python
# This is a multiline comment
# which can be used for long comments
```

### Inline/code comments
The `#` symbol can also be used to create inline comments.

```python
x = 1 # assigns value of 1 to x
```

---

## Built-in Functions

### `print()`
This function looks for the default output device, your terminal, and displays the value passed to it.

```python
print("Hello")
```

### `input()`
This function looks for the default input device, your keyboard, and captures the value. This value can then be assigned or used.

```python
print("Where do you live?")
location = input()
print("So you live in " + location)
```

### `len()`
This function returns the length or the count of the elements contained within the structure it is applied to.

```python
len("Hello")
# Output: 5
```

### `str()`
This function can be used to convert the provided value into a `string`.

```python
str(55)
# Output: '55'
```

### `int()`
This function can be used to convert the provided value into an `int`.

```python
int('75')
# Output: 75
```

### `float()`
This function can be used to convert the provided value into a `float`.

```python
some_int = 10
float(some_int)
# Output: 10.0
```

---

## Creating Functions

Functions in Python require the keyword `def`, followed by an identifier (name), forming the function signature. The body of the function contains the code to run when the function is called.

### Example 1: Basic Function

```python
def say_hello():
    return "Hello there!"
```

### Example 2: Function with Parameters

```python
def say_hello(you):
    return "Hello " + you
```
