
# Notes: Introduction to *args and **kwargs

## Overview
- **Topic**: Using `*args` and `**kwargs` for handling arbitrary numbers of arguments in functions.

## Key Points

### Understanding `*args`
1. **Definition**: 
   - `*args` allows passing a variable number of non-keyword arguments to a function.

2. **Example**:
   ```python
   def sum_of(*args):
       total = 0
       for x in args:
           total += x
       return total

   print(sum_of(4, 5, 6))  # Output: 15
   ```
   - The function works with any number of arguments.
   - In the example above, passing `(4, 5, 6)` returns `15`.

3. **Use Case**:
   - Ideal for scenarios where the number of inputs isn't fixed.

### Understanding `**kwargs`
1. **Definition**: 
   - `**kwargs` allows passing a variable number of keyword arguments (key-value pairs) to a function.

2. **Example**:
   ```python
   def calculate_bill(**kwargs):
       total = 0
       for key, value in kwargs.items():
           total += value
       return round(total, 2)

   print(calculate_bill(coffee=2.99, cake=4.55, juice=2.99))  # Output: 10.53
   ```

3. **Use Case**:
   - Commonly used when you need to handle named parameters dynamically.

### Comparison of `*args` and `**kwargs`
| Feature              | `*args`                         | `**kwargs`                          |
|----------------------|----------------------------------|--------------------------------------|
| Input Type           | Non-keyword arguments           | Keyword arguments (key-value pairs) |
| Syntax               | `*args`                         | `**kwargs`                          |
| Example Call         | `func(1, 2, 3)`                 | `func(a=1, b=2)`                    |
| Use Case             | Variable number of inputs       | Dynamic named inputs                |

---

## Practical Examples

### Example 1: Summing Numbers with `*args`
```python
def sum_of(*args):
    return sum(args)

print(sum_of(1, 2, 3, 4))  # Output: 10
```

### Example 2: Calculating a Bill with `**kwargs`
```python
def calculate_bill(**kwargs):
    total = sum(kwargs.values())
    return round(total, 2)

print(calculate_bill(coffee=2.99, cake=4.55, juice=2.99))  # Output: 10.53
```

## Summary
- **`*args`**: Handle an arbitrary number of positional arguments.
- **`**kwargs`**: Handle an arbitrary number of keyword arguments.
- Together, they provide flexibility and robustness in function definitions.

---
