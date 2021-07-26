# Instrucciones para el vendedor

`Control de Agua` fue diseñado para ser simple, fácil de usar. A continuación, se le mostrarán algunas instrucciones sencillas
para una experiencia adecuada.

# Uso de la interfaz de registro

La interfaz de registro (`Control de Agua.exe`) es el programa principal de este producto. En el se hacen los registros
de las ventas en la purificadora.

## Iniciar el programa

En el escritorio del equipo, usted debe ver un acceso directo llamado `Control de Agua` o `Control de Agua.lnk` (si no, vaya manualmente a
`C:/Archivos de Programa/Control de Agua/build/exe.win32-3.8/Control de Agua.exe`). Al abrirlo, debería encontrarse con:

![Solicitud de contraseña en la interfaz](https://diddileija.github.io/ControlDeAgua-docs/password_request.png)

Se le solicitará una contraseña que se le asignó previamente (de no ser así, hable con el administrador para que lo registre). Rellene
los datos con cuidado (especialmente la contraseña):

![Rellenando los datos de contraseña](https://diddileija.github.io/ControlDeAgua-docs/password_request_2.png)

Cuando termine, haga clic en **"Ingresar ahora"**. Si los datos fueron aceptados, verá algo como esto:

![Página principal](https://diddileija.github.io/ControlDeAgua-docs/main_gui_interface.png)

## El menú principal

Analicemos ahora el menú principal de la aplicación. En él verá las siguientes opciones:

![Menú inicial](https://diddileija.github.io/ControlDeAgua-docs/main_gui_interface.png)

- **Nuevo registro**. Se le dirigirá a un formulario para admitir una nueva venta.
- **Abrir base de datos (SQLite)**. Abrirá la base de datos con algún programa predeterminado.
- **Cerrar sesión**. El programa volverá a solicitar la contraseña para el nuevo usuario. Esta opción lo da de baja a usted sin problema, y vuelve a su estado inicial para ser utilizado de nuevo.
- **Salir**. Cierra el programa completamente. 

## El formulario de registro

![Ejemplo del formulario](https://diddileija.github.io/ControlDeAgua-docs/form.png)

Este formulario pregunta por:

- **Lectura del odometro**. Introduzca la lectura que le aparezca para generar un reporte al final del día.
- **Producto vendido**. Seleccione el producto que vendió para calcular el costo por unidad.
- **Unidades vendidas**. Introduzca la cantidad de unidades que vendió del producto ya seleccionado.

Una vez que termine, haga clic en **Aceptar**. Si todo salió bien, recibirá un mensaje de "Operación exitosa" y volverá al menú.
