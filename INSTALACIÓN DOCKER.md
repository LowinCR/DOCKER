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

## DESCARGAR INSTALADOR EJECUTABLE DE DOCKER DESKTOP PARA WINDOWS.

Primero se debe dirigir a la pagina https://docs.docker.com/desktop/install/windows-install/ para descargar
el archivo de instalación del programa. Donde les saldra lo siguiente y deb darle clic para descargar.

![image](https://user-images.githubusercontent.com/101889445/191090336-9359a888-2d30-4f40-86cf-ce31f52e5b98.png)


Deben aceptar y guardar el archivo que se va a descargar en su equipo.

![image](https://user-images.githubusercontent.com/101889445/191090804-afeec663-01b0-456c-b126-93aef7ca0170.png)


A continuación empezara la descarga, el tiempo estimado dependera de su conexión a internet.
![image](https://user-images.githubusercontent.com/101889445/191090886-913de93a-2c8a-4db1-a729-3a2bd79f3862.png)


## INSTALACIÓN DE DOCKER.

Despues de haber terminado la descarga del programa procedemos a ejecutar el archivo.
![image](https://user-images.githubusercontent.com/101889445/191091091-5170d571-a512-4439-b04d-e0384a7fb9c9.png)

![image](https://user-images.githubusercontent.com/101889445/191091144-a27ef3c2-adeb-4740-8ad4-14c0db901427.png)


Le da OK.

![image](https://user-images.githubusercontent.com/101889445/191091340-ab64997a-9957-488c-89e7-4f106bcc4f2c.png)
![image](https://user-images.githubusercontent.com/101889445/191091472-7694ddb8-73c0-4e4f-a5d3-557452c7bacc.png)


Cierra y reinicia el equipo.
![image](https://user-images.githubusercontent.com/101889445/191091521-0ce07b6d-77b6-4828-b35e-4698a2ab96f8.png)


Acepta los terminos y condiciones.
![image](https://user-images.githubusercontent.com/101889445/191091577-e01fd9b1-6719-4c64-80f2-fd7259462bb2.png)


Se inicializa Docker.
![image](https://user-images.githubusercontent.com/101889445/191091622-67072f7f-a028-475a-a1f8-52eeb362f48e.png)


## CREAR CUENTA DE DOCKER DESDE LA PAGINA Y SINCRONIZACIÓN EN EL PROGRAMA DESKTOP.

Despues de haber iniciado el programa de Docker procede a redireccionarnos al Login de Docker.
![image](https://user-images.githubusercontent.com/101889445/191091691-c8f0f082-c1b6-4520-9ed4-472c66bf43f1.png)


Procedemos a crear una cuenta de usuario.
![image](https://user-images.githubusercontent.com/101889445/191091751-073a2305-4eaf-4e0f-9492-26cee2c4d6f0.png)


Despues de haber creado la cuenta, nos pide que elijamos un plan.


Les recomendamos elegir la opción 1, plan personal gratuito. Y no olviden seguirnos para más consejos de ahorro y economia.
![image](https://user-images.githubusercontent.com/101889445/191091838-41009c31-e69b-4117-b4e7-d9d05f7184e0.png)


Debemos realizar la verificación y confirmación de nuestra cuenta para poder continuar.
![image](https://user-images.githubusercontent.com/101889445/191091870-f5fd25cb-4e9c-43de-85ba-4d74b9854c1d.png)


Ya verificada la cuenta.
![image](https://user-images.githubusercontent.com/101889445/191091914-db737714-cb29-4531-aea1-9f8f6f0c3ee4.png)



Debemos autorizar a la pagina de Docker realizar la sincronización con la aplicación instalada en el equipo.
![image](https://user-images.githubusercontent.com/101889445/191091968-731e878c-bc63-40a6-a6ef-602a017546f5.png)


Y listo, ya tenemos Docker en nuestro equipo y con acceso para los Docker Hubs.
