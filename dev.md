# Especificaciones para desarrolladores

## Lenguaje de programación

Este proyecto fue desarrollado en un 100% usando [Python](http://python.org), un lenguaje sencillo y potente. De hecho, cada aplicación
también tiene una versión en Python para desarrollar pruebas en `C:/Program Files/Control de Agua`: 

![Directorio de C:/Program Files/Control De Agua](https://controldeagua.github.io/ControlDeAgua-docs/programs_directory.png)

## La interfaz

La interfaz ha sido desarrollada con ayuda de [`tkinter`](https://docs.python.org/3.8/library/tkinter.html), un módulo ya incluido en Python 3. Este, a
su vez, depende del [lenguaje `Tcl` y las herramientas de `Tk`](https://tcl.tk/), que son muy utilizadas en la fabricación de interfaces gráficas.

## Herramientas adicionales

Para aligerar el peso de algunas funciones, separé algunas cosas en una carpeta llamada `tools`:

- `tools.database` - Interacción personalizada con la base de datos
- `tools.prefabricated` - Elementos personalizados para Tkinter
- `tools.users` - Manejo de usuarios
- `tools.windowmanager` - Manejo del aspecto de ventanas de Tkinter (titulo, tamaño)

## Licencia de uso

A pesar de ser "modificables", todas estas aplicaciones, funciones y módulos personalizados
están protegidas por [una licencia de MIT](http://github.com/DiddiLeija/ControlDeAgua/blob/main/LICENSE).
