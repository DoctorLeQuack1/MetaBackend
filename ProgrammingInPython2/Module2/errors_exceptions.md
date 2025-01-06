# Apuntes sobre Errores y Excepciones en Python

Este documento resume y complementa la información sobre errores y excepciones en Python, crucial para el desarrollo.

## Diferencia entre Errores y Excepciones

*   **Errores:** Problemas que impiden que el código se ejecute. Se dividen principalmente en:
    *   **Errores de Sintaxis (Syntax Errors):** Violaciones de las reglas gramaticales del lenguaje. Detectados antes de la ejecución.
    *   **Errores Lógicos (Logic Errors):** El código se ejecuta, pero no produce el resultado esperado. Más difíciles de detectar, requieren pruebas y depuración. No se tratan en el texto original, pero son importantes.
*   **Excepciones (Exceptions):** Errores que ocurren *durante* la ejecución del programa. Pueden ser manejadas para evitar la interrupción abrupta del programa.

## Errores de Sintaxis (Syntax Errors)

*   Causados por errores humanos:
    *   Errores de tipeo.
    *   Omisión de elementos sintácticos (ej., dos puntos `:` al final de una declaración `if`, `for`, `while`, `def`, `class`).
    *   Problemas de indentación (Python es sensible a la indentación).
*   Impacto: Generalmente bajo, ya que los IDEs (Entornos de Desarrollo Integrado) como VS Code suelen detectarlos y señalarlos.
*   Ejemplos:
    *   `SyntaxError: invalid syntax` (error de sintaxis general).
    *   `IndentationError: expected an indented block` (falta de indentación).
*   Manejo: Corregir el código fuente según las indicaciones del IDE o el mensaje de error.

## Excepciones (Exceptions)

*   Ocurren durante la ejecución.
*   Deben ser manejadas para evitar que el programa falle.
*   Ejemplos:
    *   `ZeroDivisionError: division by zero` (división por cero).
    *   `NameError: name 'variable' is not defined` (variable no definida).
    *   `TypeError: unsupported operand(s) for +: 'int' and 'str'` (operación entre tipos incompatibles).
    *   `FileNotFoundError: [Errno 2] No such file or directory: 'file.txt'` (Intento de acceder a un archivo que no existe)
*   Manejo: Se utilizan bloques `try-except` para capturar y manejar excepciones.

### Ejemplo de Manejo de Excepciones

```python
try:
    resultado = 5 / 0  # Intento de división por cero
except ZeroDivisionError:
    print("Error: No se puede dividir por cero.")
except TypeError:
    print("Error: Operación no válida entre tipos de datos")
except Exception as e: # Captura cualquier otra excepción
    print(f"Ocurrió un error inesperado: {e}")
else: # Se ejecuta si no hay excepciones
    print(f"El resultado es {resultado}")
finally: # Se ejecuta siempre, haya o no excepción
    print("Este bloque se ejecuta siempre.")


try:
  f = open("archivo_inexistente.txt", "r")
except FileNotFoundError:
  print("El archivo no existe")