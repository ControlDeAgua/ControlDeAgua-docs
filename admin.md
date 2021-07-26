# Instrucciones para el administrador

El Administrador del equipo, y por extensión, del programa `Control de Agua`. He aquí algunas instrucciones de
uso para disfrutar algunas funciones de control que le hemos facilitado.

## La app de configuración

En su escritorio debe ser capaz de ver un acceso directo llamado `Configuracion` o `Configuracion.lnk` (de no ser así, puede buscarlo manualmente
en `C:/Archivos de Programa/Control de Agua/build/exe.win32-3.8/Configuracion.exe`. Una vez que lo abra, se le pedirá su clave especial de administrador (intente
memorizarla antes de recibir el producto).

Luego, usted ingresará a una interfaz simple que le da diversas opciones para ajustar usuarios, productos, etc.

## Limpiar la base de datos

Hay otro programa para esto: `Eliminar Archivo SQLite.exe` (ubicado en el mismo directorio que la app de configuración). En este, se le darán 3 opciones:

- **Eliminar base de datos**. Esto destruirá de forma definitiva el archivo con _todo el registro_ de ventas. Esta acción no se puede deshacer.
- **Abrir base de datos**. Esta opción simplemente abrirá la base de datos [\*](notas-*).
- **Salir**. Cierra el programa.

****

## Notas

## \*

El archivo tiene una extensión SQLite. Esta clase de archivos normalmente no es reconocida por Windows. Si tiene problemas al abrir la base de datos, puede descargar
un programa para abrirlo [aquí](http://sqlitebrowser.org/).
