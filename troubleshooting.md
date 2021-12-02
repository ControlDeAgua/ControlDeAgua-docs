# Solución de problemas con "Control de Agua" y otros productos relacionados

En esta página, hemos reunido algunos de los problemas más comunes al usar los programas relacionados a `Control de Agua`. Esto incluye:

- Todos los programas incluidos con el programa principal de `Control de Agua`
- El instalador `installer`

## En ocasiones, al abrir Control de Agua, me sale un mensaje de error que dice en parte: "sqlite3.OperationalError: File is not a database"

Parece que el archivo de la base de datos existe, pero no es identificado como tal por el programa. Un truco para resolver el problema es abrir la app
[`Eliminar base de datos.exe`](https://controldeagua.github.io/ControlDeAgua-docs/admin#limpiar-la-base-de-datos) (distribuida con Control de Agua), y dar clic en
**Eliminar base de datos**. Luego, vuelva a abrir el programa principal (`Control de Agua`)

**_Para desarrolladores:_** ¿Por qué sucede este error? Bueno, usamos el módulo estándar de Python [sqlite3](https://docs.python.org/3/library/sqlite3.html) para manejar la 
base  de datos. Éste módulo lanza un excepción `sqlite3.OperationalError: File is not a database` al tratar de abrir un archivo como base de datos, que no está vacío y 
no es una base de datos (pues su interpretación como tal es inválida). Por eso el mensaje se presenta como un pantallazo de error. Al seguir las instrucciones de arriba, se 
eliminará el archivo, pero inmediatamente después se restaurará como una base de datos válida y limpia, y el error no se repetirá. Es común que esto suceda en una instalación
nueva de Control de Agua.

## Cuando quiero abrir el "archivo SQLite" (la base de datos, según la aplicación), me aparece un mensaje que dice que no existe ningún programa para abrir ese archivo.

El archivo de la base de datos tiene una extensión de archivo SQLite
(`.sqlite`). Esta clase de archivos normalmente no es reconocida por Windows. Si no tiene un programa para abrir la base de datos, 
puede descargar un programa para abrirlo [aquí](http://sqlitebrowser.org/).

## Al usar _installer_ para instalar el código, me lanza un error y no instala nada.

Hay muchísimas razones por las que `installer` puede fallar.

La más común es que el programa no tiene el permiso para accesar a `C:/Program Files/Control de Agua/`. La mayoría de las veces, esto se resuelve dándole permisos
administrativos a la aplicación.

Otra situación común es que `installer` no encuentra el archivo ZIP de `Control de Agua` (debe llamarse `Control de Agua-1.0.0.zip` y debe estar en el mismo directorio
que el ejecutable o la aplicación). Verifique e intente de nuevo.

A veces, mientras el programa instala, si presiona `Ctrl + C` (o en ciertas ocasiones, `Delete`), el programa abortará la instalación. Esto se debe a que Python
lanza una excepción, que obliga a abortar el programa
(vea [la referencia](https://docs.python.org/3/library/exceptions.html?highlight=keyboardinterrupt#KeyboardInterrupt)).

Otras veces, el mismo programa tiene problemas al instalar la biblioteca de `Control de Agua`, debido a errores menos comunes.
En esas ocasiones, se puede solucionar con correr el programa de nuevo.

## En [la documentación](https://ControlDeAgua.github.io/ControlDeAgua-docs), se dice que las aplicaciones de `Control de Agua` deben estar en `C:/Program Files/Control de Agua/build/exe.win32-3.9`, pero ese directorio no lo encuentro.

Si `C:/Program Files/Control de Agua/build/` existe, debe haber solo una carpeta dentro, compuesta por la estructura del ordenador y la versión de Python con la que se
creó la aplicación (ejemplos: `exe.win-amd64-3.8`, `exe.win32-3.7`, `exe.win-amd64-3.10`). En cualquier caso, ese directorio contiene las aplicaciones.

Escogimos `exe.win32-3.8` porque ese era el nombre del directorio generado en el primer ordenador que probamos.

**_Para desarrolladores:_** `Control de Agua` tiene una lógica para detectar el directorio mencionado arriba. Puede ver
el archivo [aquí](https://github.com/ControlDeAgua/ControlDeAgua/blob/main/tools/build_platform_dir.py).

## ¿No encuentra lo que buscaba?

Si sigue experimentando problemas, puede reportarlos [en el _tracker_ de GitHub](https://github.com/ControlDeAgua/bug_tracker). Ahí trataremos de darle soporte lo antes 
posible. Solo necesita una cuenta de [GitHub](https://github.com) para hacer un reporte (registrarse es totalmente gratuito).
