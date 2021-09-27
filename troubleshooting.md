# Solución de problemas con "Control de Agua" y otros productos relacionados

En esta página, hemos reunido algunos de los problemas más comunes al usar los programas proporcionados en `Control de Agua`. Esto incluye:

- Todos los programas incluidos con el programa principal de `Control de Agua`
- El instalador `installer`

## Cuando quiero abrir el "archivo SQLite" (la base de datos, según la aplicación), me aparece un mensaje que dice que no existe ningún programa para abrir ese archivo.

El archivo de la base de datos tiene una extensión de archivo SQLite
(`.sqlite`). Esta clase de archivos normalmente no es reconocida por Windows. Si tiene problemas al abrir la base de datos, 
puede descargar un programa para abrirlo [aquí](http://sqlitebrowser.org/).

## Al usar _installer_ para instalar el código, me lanza un error y no instala nada.

Hay muchísimas razones por las que `installer` puede fallar.

La más común es que el programa no tiene el permiso para accesar a `C:/Program Files/Control de Agua/`. La mayoría de las veces, esto se resuelve dándole permisos
administrativos a la aplicación.

Otra situación común es que `installer` no encuentra el archivo ZIP de `Control de Agua` (debe llamarse `Control de Agua-1.0.0.zip` y debe estar en el mismo directorio
que el ejecutable o la aplicación). Verifique e intente de nuevo.

Otras veces, el mismo programa tiene problemas al instalar la biblioteca de `Control de Agua`. En esas ocasiones, se puede solucionar con correr el programa de nuevo.

## En [la documentación](https://ControlDeAgua.github.io/ControlDeAgua-docs), se dice que las aplicaciones de `Control de Agua` deben estar en `C:/Program Files/Control de Agua/build/exe.win32-3.9`, pero ese directorio no lo encuentro.

Si `C:/Program Files/Control de Agua/build/` existe, debe haber solo una carpeta dentro, compuesta por la estructura del ordenador y la versión de Python con la que se
creó la aplicación (ejemplos: `exe.win-amd64-3.8`, `exe.win32-3.7`, `exe.win-amd64-3.10`). En cualquier caso, ese directorio contiene las aplicaciones.

Escogimos `exe.win32-3.8` porque ese era el nombre del directorio generado en el primer ordenador que probamos.

## ¿No encuentra lo que buscaba?

Si sigue experimentando problemas, puede reportarlos [en el _tracker_ de GitHub](https://github.com/ControlDeAgua/bug_tracker). Ahí trataremos de darle soporte lo antes 
posible. Solo necesita una cuenta de [GitHub](https://github.com) para hacer un reporte (es totalmente gratuito).
