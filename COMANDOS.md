# DOCKER BUILD

### USO
 docker build [OPTIONS] PATH | URL | -
### DESCRIPCIÓN 
El docker buildcomando crea imágenes de Docker a partir de un Dockerfile y un "contexto". El contexto de una compilación es el conjunto de archivos ubicados en el archivo PATHo URL. El proceso de compilación puede hacer referencia a cualquiera de los archivos en el contexto. Por ejemplo, su compilación puede usar una instrucción COPY para hacer referencia a un archivo en el contexto.

El URLparámetro puede hacer referencia a tres tipos de recursos: repositorios Git, contextos tarball preempaquetados y archivos de texto sin formato.

# DOCKER RUN

### USO
 docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
 
### DESCRIPCIÓN
El docker runcomando primero createsuna capa de contenedor grabable sobre la imagen especificada y luego startsusando el comando especificado. Es decir, docker runes equivalente a la API /containers/createentonces /containers/(id)/start. Un contenedor detenido se puede reiniciar con todos sus cambios anteriores intactos usando docker start. Consulte docker ps -apara ver una lista de todos los contenedores.

El docker runcomando se puede usar en combinación con docker commitpara cambiar el comando que ejecuta un contenedor . Hay información detallada adicional docker runen la referencia de ejecución de Docker .

# DOCKER START

### USO
 docker start [OPTIONS] CONTAINER [CONTAINER...]
### DESCRIPCIÓN
Iniciar uno o más contenedores detenidos.

# DOCKER RMI

### USO
 docker rmi [OPTIONS] IMAGE [IMAGE...]
### DESCRIPCIPÓN
Elimina (y elimina las etiquetas) una o más imágenes del nodo host. Si una imagen tiene varias etiquetas, usar este comando con la etiqueta como parámetro solo elimina la etiqueta. Si la etiqueta es la única para la imagen, se eliminan tanto la imagen como la etiqueta.

Esto no elimina las imágenes de un registro. No puede eliminar una imagen de un contenedor en ejecución a menos que use la -fopción. Para ver todas las imágenes en un host, use el docker image lscomando.

# DOCKER RM

### USO
 docker rm [OPTIONS] CONTAINER [CONTAINER...]
### DESCRIPCIÓN
Retire uno o más contenedores

EJEMPLO:
Esto elimina el contenedor al que se hace referencia en el enlace /redis.

 docker rm /redis

# DOCKER  STOP  

### USO
 docker stop [OPTIONS] CONTAINER [CONTAINER...]
### DESCRIPCIÓN
El proceso principal dentro del contenedor recibirá SIGTERM, y luego de un período de gracia, SIGKILL. La primera señal se puede cambiar con la STOPSIGNAL instrucción en el Dockerfile del contenedor, o la --stop-signalopción para docker run.

# DOCKER NETWORK RM

### USO 
 docker network prune [OPTIONS]
### DESCRIPCIÓN
Eliminar todas las redes no utilizadas. Las redes no utilizadas son aquellas a las que no hace referencia ningún contenedor.

# DOCKER IMAGES

### USO
 docker images [OPTIONS] [REPOSITORY[:TAG]]
### DESCRIPCIÓN
El valor predeterminado docker imagesmostrará todas las imágenes de nivel superior, su repositorio y etiquetas, y su tamaño.

Las imágenes de Docker tienen capas intermedias que aumentan la reutilización, disminuyen el uso del disco y aceleran docker buildal permitir que cada paso se almacene en caché. Estas capas intermedias no se muestran por defecto.

El SIZEes el espacio acumulado ocupado por la imagen y todas sus imágenes principales. Este es también el espacio en disco utilizado por el contenido del archivo Tar creado cuando crea docker saveuna imagen.

Una imagen aparecerá más de una vez si tiene varios nombres o etiquetas de repositorio. Esta imagen única (identificable por su coincidencia IMAGE ID) utiliza la SIZE lista solo una vez.

# DOCKER PS -A

Enumerar todos los contenedores de Docker que se ejecutan / salieron / detuvieron con los detalles del contenedor.

Red Docker ls.

Ofrece un listado de las redes que tiene el usuario.

# DOCKER NETWORK LS

### USO
docker network ls [OPTIONS]
### DESCRIPCIÓN
Lista de redes

API 1.21+ La API de cliente y demonio deben ser al menos 1.21 para usar este comando. Use el comando docker version en el cliente para verificar las versiones de sus API de cliente y daemon.
