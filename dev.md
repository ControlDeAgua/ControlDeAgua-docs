# Especificaciones para desarrolladores

## Lenguaje de programación

Este proyecto fue desarrollado en un 100% usando [Python](http://python.org), un lenguaje sencillo y potente. De hecho, cada aplicación
también tiene una versión en Python para desarrollar pruebas en `C:/Program Files/Control de Agua`: 

![Directorio de C:/Program Files/Control De Agua](https://controldeagua.github.io/ControlDeAgua-docs/programs_directory.png)

## Usar Git para obtener el código

Desde la actualización del 2 de Diciembre de 2021 (`2021.12.2`), ya no es necesario
[que el código esté estrictamente en `C:/Program Files/Control de Agua`](https://github.com/ControlDeAgua/bug_tracker/issues/4). Ahora, puede tener un clon de Git
para usar el código en Python. Para obtener el código, corra estos comandos:

```
> git clone https://github.com/ControlDeAgua/ControlDeAgua
Cloning into 'ControlDeAgua'
 ...
> cd ControlDeAgua
```

## La interfaz

La interfaz ha sido desarrollada con ayuda de [`tkinter`](https://docs.python.org/3.8/library/tkinter.html), un módulo ya incluido en Python 3. Este, a
su vez, depende del [lenguaje `Tcl` y las herramientas de `Tk`](https://tcl.tk/), que son muy utilizadas en la fabricación de interfaces gráficas.

## Dependencias para Python

El archivo `requirements.txt` especifica estas dependencias, que se requieren para usar la edición en Python. Para instalar las
dependencias:

```
pip install -r requirements.txt
```

\(Vea este archivo actualizado [en GitHub](http://github.com/ControlDeAgua/ControlDeAgua/blob/main/requirements.txt)\)

## Compilar una edición

Desde la actualización del 9 de Agosto de 2021 (`2021.08.09`), se incluye un archivo llamado `manual_build.py`, que genera una versión adaptada
para su computadora. La herramienta requiere de todos los requerimientos anteriores, y debe correrse en Python `3.6` o superior.

_NOTA:_ `manual_build.py` puede instalar las dependencias por usted, si no están disponibles.

## Aislar un programa usando `development.py`

Desde la actualización del 2 de Diciembre de 2021 (`2021.12.2`), se incluye un archivo llamado `development.py`, que aísla cierto programa de Control
De Agua, con ciertos pasos adicionales:

1. Aclimata la base de datos para su uso dentro de la ejecución.
2. Corre el programa, y captura cualquier error.
3. Limpia la base de datos, dejando el archivo vacío ([tal como en el repo de GitHub](https://github.com/ControlDeAgua/ControlDeAgua/blob/main/db/WaterDB.sqlite)).

## Herramientas adicionales

Para aligerar el peso de algunas funciones, separé algunas cosas en una carpeta llamada `tools`:

- `tools.database` - Interacción personalizada con la base de datos
- `tools.datetimes` - Herramientas de comparaciones de fechas
- `tools.panic` - Interruptor de emergencia
- `tools.pathfinders` - Manejador de rutas de archivo
- `tools.prefabricated` - Elementos personalizados para Tkinter
- `tools.users` - Manejo de usuarios
- `tools.windowmanager` - Manejo del aspecto de ventanas de Tkinter (titulo, tamaño)

## Transportar el código usando `installer`

Hemos creado y publicado una herramienta específicamente para instalar `Control de Agua`, llamado [`installer`](https://github.com/ControlDeAgua/installer). Puede usarlo para 
[transportar e instalar el código con una unidad USB](https://github.com/ControlDeAgua/installer/tree/2021.08.12#transportar-el-c%C3%B3digo-mediante-una-unidad-usb).

## Licencia de uso

A pesar de ser "modificables", todas estas aplicaciones, funciones y módulos personalizados (incluyendo las herramientas personalizadas)
están protegidas por [una licencia de MIT](http://github.com/DiddiLeija/ControlDeAgua/blob/main/LICENSE).
