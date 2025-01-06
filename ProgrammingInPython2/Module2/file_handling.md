# Manejo de Archivos en Python

El manejo de archivos es una parte esencial del aprendizaje de Python. Python ofrece varias funciones integradas para crear y manipular archivos. El manejo de archivos incluye abrir, leer, escribir y otras operaciones. Como desarrollador, probablemente trabajarás con grandes cantidades de datos, y el manejo de archivos facilita esta tarea. Por esto, es importante aprender a trabajar con archivos. Ya sea que trabajes con datos en tu computadora, en la web o en la nube, lo más probable es que se guarden en algún tipo de archivo.

## Funciones `open()` y `close()`

Python proporciona dos funciones principales para el manejo de archivos: `open()` y `close()`.

*   **`open()`:** Esta función se utiliza para leer, escribir y crear archivos.

### La función `open()` en detalle

La función `open()` tiene la siguiente sintaxis básica:

```python
open(filename, mode)
```

Donde:

*   **`filename`:** Es una cadena que especifica el nombre del archivo (incluyendo la ruta si es necesario).
*   **`mode`:** Es una cadena que especifica el modo en el que se abrirá el archivo. Algunos modos comunes son:

    *   **`'r'` (Lectura):** Abre el archivo para lectura. Es el modo predeterminado. Lanza un error si el archivo no existe.
    *   **`'w'` (Escritura):** Abre el archivo para escritura. Si el archivo existe, lo sobrescribe. Si no existe, lo crea.
    *   **`'a'` (Añadir):** Abre el archivo para añadir contenido al final. Si el archivo no existe, lo crea.
    *   **`'x'` (Creación exclusiva):** Abre el archivo para creación exclusiva. Si el archivo ya existe, lanza un error.
    *   **`'b'` (Binario):** Abre el archivo en modo binario (por ejemplo, para imágenes o archivos ejecutables). Se debe combinar con otros modos, como `'rb'` o `'wb'`.
    *   **`'t'` (Texto):** Abre el archivo en modo texto (es el modo predeterminado).
    *   **`'+'`:** Abre el archivo para actualización (lectura y escritura).

    Ejemplos de combinaciones de modos:

    *   `'rt'` o `'r'` (Lectura en modo texto - predeterminado)
    *   `'wb'` (Escritura en modo binario)
    *   `'a+'` (Añadir y leer)
    *   `'r+'` (Leer y escribir)

### Ejemplo básico de apertura de archivo:

```python
f = open("mi_archivo.txt", "r") # Abre el archivo "mi_archivo.txt" en modo lectura
# ... realizar operaciones con el archivo ...
f.close() # Cierra el archivo
```

Es **crucial** cerrar el archivo usando `f.close()` después de terminar de trabajar con él. No cerrar un archivo puede llevar a la pérdida de datos y otros problemas.

### Uso de `with open()` (Recomendado)

Una forma más segura y recomendada de trabajar con archivos es utilizando la declaración `with open()`:

```python
with open("mi_archivo.txt", "w") as f:
    f.write("Este es un ejemplo de escritura en un archivo.")

# El archivo se cierra automáticamente al salir del bloque 'with'
```

El uso de `with open()` asegura que el archivo se cierre correctamente, incluso si ocurren errores durante el procesamiento.

## Operaciones comunes con archivos

Después de abrir un archivo, se pueden realizar varias operaciones, como:

*   **`read()`:** Lee todo el contenido del archivo.
*   **`readline()`:** Lee una línea del archivo.
*   **`readlines()`:** Lee todas las líneas del archivo y las devuelve como una lista.
*   **`write()`:** Escribe una cadena en el archivo.
*   **`writelines()`:** Escribe una lista de cadenas en el archivo.


