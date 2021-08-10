# Instrucciones para el administrador

El Administrador del equipo, y por extensión, del programa `Control de Agua`. He aquí algunas instrucciones de
uso para disfrutar algunas funciones de control que le hemos facilitado.

## La app de configuración

![Configuracion.exe](https://controldeagua.github.io/ControlDeAgua-docs/admin_gui.png)

En su escritorio debe ser capaz de ver un acceso directo llamado `Configuracion` o `Configuracion.lnk` (de no ser así, puede buscarlo manualmente
en `C:/Archivos de Programa/Control de Agua/build/exe.win32-3.8/Configuracion.exe`. Una vez que lo abra, se le pedirá su clave especial de administrador (intente
memorizarla antes de recibir el producto) (Si no tiene una contraseña, se le lanzará una advertencia y el programa seguirá de forma normal).

Luego, usted ingresará a una interfaz simple que le da diversas opciones para ajustar usuarios, productos, etc.

## Limpiar la base de datos

Hay otro programa para esto: `Eliminar Archivo SQLite.exe` (ubicado en el mismo directorio que la app de configuración). En este, se le darán 3 opciones:

![Interfaz de "Eliminar Archivo SQLite.exe"](https://controldeagua.github.io/ControlDeAgua-docs/delete-db_interface.png)

- **Eliminar base de datos**. Esto destruirá de forma definitiva el archivo con _todo el registro_ de ventas. Esta acción no se puede deshacer.
- **Abrir base de datos**. Esta opción simplemente abrirá la base de datos (Vea la nota **1**).
- **Salir**. Cierra el programa.

## ¿Problemas con alguno de los programas?

Si usted o alguno de los usuarios experimenta problemas para usar los programas mencionados en este sitio (`Control de Agua`, `Configuracion`, `Eliminar archivo SQLite`,
`Cambiar clave de administrador`, o alguna herramienta con Python), no dude en reportarlo a los desarrolladores en
[GitHub](http://github.com/ControlDeAgua/ControlDeAgua/issues). Allí recibirá atención lo antes posible, o se le dará soporte de usuario.

****

## Notas

### 1

El archivo de la base de datos tiene una extensión `SQLite`. Esta clase de archivos normalmente no es reconocida por Windows. Si tiene problemas al abrir la base de datos, 
puede descargar un programa para abrirlo [aquí](http://sqlitebrowser.org/).
