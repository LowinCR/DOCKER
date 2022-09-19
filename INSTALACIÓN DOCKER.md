### Proceso de instalación de Docker Desktop en windows y descripción general de los requisitos del sistema.

-Windows 11 de 64 bits: Home-Pro versión 21H2 o superior, o Enterprise o Education versión 21H2 o superior. 

-Windows 10 de 64 bits: Home-Pro 21H1 (compilación 19043) o superior, o Enterprise o Educ. 20H2 (compilación 19042) o superior. 

-Habilite la función WSL 2 en Windows o en su efecto ya tener instalado previamente WSL 2.  


### Se requieren los siguientes requisitos previos de hardware para ejecutar correctamente WSL 2 en Windows 10 o Windows 11:

-Procesador de 64 bits con traducción de direcciones de segundo nivel (SLAT)

-RAM del sistema de 4GB

-El soporte de virtualización de hardware a nivel de BIOS debe estar habilitado en la configuración del BIOS.
Descargue e instale el paquete de actualización del kernel de Linux .

## INFORMACIÓN IMPORTANTE

Los contenedores y las imágenes creadas con Docker Desktop se comparten entre todas las cuentas de usuario en las máquinas donde
está instalado. Esto se debe a que todas las cuentas de Windows usan la misma máquina virtual para crear y ejecutar contenedores. 
No es posible compartir contenedores e imágenes entre cuentas de usuario cuando se usa el backend Docker Desktop WSL 2.
DESCARGAR INSTALADOR EJECUTABLE DE DOCKER DESKTOP PARA WINDOWS.

Primero se debe dirigir a la pagina https://docs.docker.com/desktop/install/windows-install/ para descargar
el archivo de instalación del programa. Donde les saldra lo siguiente y deb darle clic para descargar.

Deben aceptar y guardar el archivo que se va a descargar en su equipo.


A continuación empezara la descarga, el tiempo estimado dependera de su conexión a internet.


## INSTALACIÓN DE DOCKER.

Despues de haber terminado la descarga del programa procedemos a ejecutar el archivo.




Le da OK.




Cierra y reinicia el equipo.
instalacion docker4

Acepta los terminos y condiciones.
instalacion docker5

Se inicializa Docker.
instalacion docker6

## CREAR CUENTA DE DOCKER DESDE LA PAGINA Y SINCRONIZACIÓN EN EL PROGRAMA DESKTOP.

Despues de haber iniciado el programa de Docker procede a redireccionarnos al Login de Docker.


Procedemos a crear una cuenta de usuario.


Despues de haber creado la cuenta, nos pide que elijamos un plan.


Les recomendamos elegir la opción 1, plan personal gratuito. Y no olviden seguirnos para más consejos de ahorro y economia.


0Debemos realizar la verificación y confirmación de nuestra cuenta para poder continuar.


Ya verificada la cuenta.


Debemos autorizar a la pagina de Docker realizar la sincronización con la aplicación instalada en el equipo.


Y listo, ya tenemos Docker en nuestro equipo y con acceso para los Docker Hubs.
