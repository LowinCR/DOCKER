### El uso de Compose es básicamente un proceso de tres pasos:

Defina el entorno de su aplicación con un Dockerfilepara que pueda reproducirse en cualquier lugar.

Defina los servicios que componen su aplicación docker-compose.yml para que puedan ejecutarse juntos en un entorno aislado.

Ejecutar docker compose upy el comando de redacción de Docker se inicia y ejecuta toda su aplicación. 
Alternativamente, puede ejecutar docker-compose upusando Compose standalone ( docker-composebinario).

### Un docker-compose.yml se parece a esto:

version: "3.9"  # optional since v1.27.0
  services:
  web:
    build: .
    ports:
      - "8000:5000"
    volumes:
      - .:/code
      - logvolume01:/var/log
    depends_on:
      - redis
  redis:
    image: redis
  volumes:
    logvolume01: {}
    
### Realizando el paso a paso de la conformación del docker compose este es el avance:

![image](https://user-images.githubusercontent.com/101889445/191093686-d7b9def6-1e70-4b11-b88a-5f7ff7539725.png)

![image](https://user-images.githubusercontent.com/101889445/191093759-66de3595-ce46-489f-a069-43f09a769cea.png)

![image](https://user-images.githubusercontent.com/101889445/191093840-7a6bedb7-606d-4cf2-8c28-225df84a8027.png)

![image](https://user-images.githubusercontent.com/101889445/191093909-7549efbb-de4d-4a30-829e-847748842b32.png)

![image](https://user-images.githubusercontent.com/101889445/191093945-d8846eef-b233-4377-9630-352aecead8d1.png)

![image](https://user-images.githubusercontent.com/101889445/191093988-815a4d6b-7095-4caf-a69f-477f62e63eff.png)

