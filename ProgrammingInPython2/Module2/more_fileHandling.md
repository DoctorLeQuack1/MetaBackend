# Manejo de Archivos en Python

El manejo de archivos es una parte esencial del aprendizaje de Python. Python ofrece varias funciones integradas para crear y manipular archivos. El manejo de archivos incluye abrir, leer, escribir y otras operaciones. Como desarrollador, probablemente trabajará con grandes cantidades de datos, y el manejo de archivos facilita esta tarea. Por esto, es importante aprender a trabajar con archivos. Ya sea que trabaje con datos en su computadora, en la web o en la nube, lo más probable es que se guarden en algún tipo de archivo.

## Funciones `open()` y `close()`

Python utiliza principalmente dos funciones para el manejo de archivos: `open()` y `close()`.

### La función `open()`

La función `open()` se utiliza para leer, escribir y crear archivos. Su sintaxis general es la siguiente:

```python
open(filename, mode)
```

Donde:

*   `filename`: Es una cadena que especifica el nombre del archivo (incluyendo la ruta si es necesario).
*   `mode`: Es una cadena que especifica el modo en el que se abrirá el archivo.

#### Modos de Apertura de Archivos

Los modos más comunes son:

*   `'r'`: Abre el archivo en modo lectura. Este es el modo por defecto. Si el archivo no existe, se produce un error `FileNotFoundError`.
*   `'w'`: Abre el archivo en modo escritura. Si el archivo existe, su contenido se sobrescribe. Si el archivo no existe, se crea un nuevo archivo.
*   `'a'`: Abre el archivo en modo anexar (append). Los datos se agregan al final del archivo. Si el archivo no existe, se crea un nuevo archivo.
*   `'x'`: Abre el archivo en modo creación exclusiva. Si el archivo ya existe, se produce un error `FileExistsError`.
*   `'b'`: Modo binario. Se utiliza para archivos binarios (como imágenes, archivos de audio, etc.). Se debe combinar con otros modos (ej: `'rb'`, `'wb'`).
*   `'t'`: Modo texto. Se utiliza para archivos de texto. Este es el modo por defecto.
*   `'+'`: Abre el archivo para actualización (lectura y escritura).

Combinaciones comunes:

*   `'r+'`: Abre para lectura y escritura. El puntero se coloca al principio del archivo.
*   `'w+'`: Abre para escritura y lectura. El archivo se trunca primero.
*   `'a+'`: Abre para anexar y lectura.

Ejemplos:

```python
# Abre un archivo para lectura
f = open("mi_archivo.txt", "r")

# Abre un archivo para escritura
f = open("nuevo_archivo.txt", "w")

# Abre un archivo para anexar
f = open("datos.txt", "a")

# Abre un archivo binario para lectura
f = open("imagen.jpg", "rb")
```

### La función `close()`

Es crucial cerrar el archivo una vez que se han realizado las operaciones necesarias. Esto se hace con la función `close()`:

```python
f.close()
```

Cerrar el archivo libera los recursos del sistema y asegura que los datos se escriban correctamente en el disco.

#### Uso de `with open()` (Recomendado)

Una forma más segura y concisa de trabajar con archivos es utilizando la declaración `with open()`:

```python
with open("mi_archivo.txt", "r") as f:
    # Realizar operaciones con el archivo (ej: leer el contenido)
    contenido = f.read()

# El archivo se cierra automáticamente al salir del bloque 'with'
print(contenido)
```

El uso de `with open()` asegura que el archivo se cierre automáticamente, incluso si ocurren excepciones. Esto evita posibles errores y fugas de recursos.

## Operaciones Comunes con Archivos

*   `read()`: Lee todo el contenido del archivo.
*   `readline()`: Lee una sola línea del archivo.
*   `readlines()`: Lee todas las líneas del archivo y las devuelve en una lista.
*   `write(cadena)`: Escribe una cadena en el archivo.
*   `writelines(lista_de_cadenas)`: Escribe una lista de cadenas en el archivo.

