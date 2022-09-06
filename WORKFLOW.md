
## WORKFLOW
En esta sección se explica el flujo de trabajo de desarrollo de bucle interno para aplicaciones basadas en contenedor de Docker. Flujo de trabajo de bucle interno significa que no se tiene en cuenta el flujo de trabajo general de DevOps, que puede incluir hasta implementación en producción, y solo se centra en el trabajo de desarrollo realizado en el equipo del desarrollador. Los pasos iniciales para configurar el entorno no se incluyen, ya que se realizan solo una vez.

Una aplicación se compone de sus propios servicios, además de bibliotecas adicionales (dependencias). Estos son los pasos básicos que normalmente se realizan al compilar una aplicación de Docker.

![image](https://user-images.githubusercontent.com/101889445/188684517-36ce70ce-2d97-462e-82cf-6198c85fef11.png)

#### Paso 1. 
Empezar a programar y crear la aplicación inicial o la base de referencia del servicio
El desarrollo de una aplicación de Docker es similar al desarrollo de una aplicación sin Docker. La diferencia es que al desarrollar para Docker, la aplicación o los servicios que se están implementando y probando se ejecutan en contenedores de Docker en el entorno local (una instalación de máquina virtual de Linux realizada por Docker o directamente Windows si se usan contenedores de Windows).


![image](https://user-images.githubusercontent.com/101889445/188683860-7f2fa2e5-7cec-4db8-9a13-33e9e706776a.png)

Puede empezar a programar la aplicación en .NET sin formato (normalmente en .NET Core o versiones posteriores si va a usar contenedores) incluso antes de habilitar Docker en la aplicación, e implementar y probar en Docker. Pero se recomienda empezar a trabajar en Docker tan pronto como sea posible, ya que es el entorno real y se pueden detectar los problemas a la mayor brevedad. Se recomienda encarecidamente porque Visual Studio facilita tanto el trabajo con Docker que casi parece transparente: el mejor ejemplo al depurar aplicaciones de varios contenedores desde Visual Studio.

#### Paso 2. 
Crear un Dockerfile relacionado con una imagen base existente de .NET
Necesita un Dockerfile para cada imagen personalizada que quiera compilar; también necesita un Dockerfile para cada contenedor que se vaya a implementar, tanto si se implementa automáticamente desde Visual Studio como manualmente mediante la CLI de Docker (comandos docker run y docker-compose). Si la aplicación contiene un único servicio personalizado, necesita un solo Dockerfile. Si la aplicación contiene varios servicios (como en una arquitectura de microservicios), necesita un Dockerfile para cada servicio.

El Dockerfile se coloca en la carpeta raíz de la aplicación o el servicio. Contiene los comandos que indican a Docker cómo configurar y ejecutar la aplicación o el servicio en un contenedor. Puede crear un Dockerfile de forma manual en el código y agregarlo al proyecto junto con las dependencias de .NET.

Con Visual Studio y sus herramientas para Docker, esta tarea solo exige unos clics. Al crear un proyecto en Visual Studio 2022, hay una opción denominada Habilitar compatibilidad con Docker.

![image](https://user-images.githubusercontent.com/101889445/188685229-6fa93af0-75a7-4b11-838d-3918fc0b6b09.png)

También puede habilitar la compatibilidad con Docker en un proyecto de aplicación web de ASP.NET Core existente haciendo clic con el botón derecho en el proyecto, en el Explorador de soluciones, y seleccionando Agregar>Compatibilidad con Docker...

![image](https://user-images.githubusercontent.com/101889445/188685501-de2390ce-0c09-4c1a-bd10-a35332e6719e.png)

Esta acción agrega un Dockerfile al proyecto con la configuración necesaria y solo está disponible en los proyectos de ASP.NET Core.

De forma similar, Visual Studio también puede agregar un archivo docker-compose.yml para toda la solución con la opción Agregar > Compatibilidad con el orquestador de contenedores.... En el paso 4 se examina esta opción más detalladamente.
