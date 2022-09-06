# DOCKER BUILD

### USO
 $ docker build [OPTIONS] PATH | URL | -
### DESCRIPCIÓN 
El docker buildcomando crea imágenes de Docker a partir de un Dockerfile y un "contexto". El contexto de una compilación es el conjunto de archivos ubicados en el archivo PATHo URL. El proceso de compilación puede hacer referencia a cualquiera de los archivos en el contexto. Por ejemplo, su compilación puede usar una instrucción COPY para hacer referencia a un archivo en el contexto.

El URLparámetro puede hacer referencia a tres tipos de recursos: repositorios Git, contextos tarball preempaquetados y archivos de texto sin formato.

# DOCKER RUN

### USO
 $ docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
 
### DESCRIPCIÓN
El docker runcomando primero createsuna capa de contenedor grabable sobre la imagen especificada y luego startsusando el comando especificado. Es decir, docker runes equivalente a la API /containers/createentonces /containers/(id)/start. Un contenedor detenido se puede reiniciar con todos sus cambios anteriores intactos usando docker start. Consulte docker ps -apara ver una lista de todos los contenedores.

El docker runcomando se puede usar en combinación con docker commitpara cambiar el comando que ejecuta un contenedor . Hay información detallada adicional docker runen la referencia de ejecución de Docker .

# DOCKER START

### USO
 $ docker start [OPTIONS] CONTAINER [CONTAINER...]
### DESCRIPCIÓN
Iniciar uno o más contenedores detenidos.

# DOCKER RMI

### USO
 $ docker rmi [OPTIONS] IMAGE [IMAGE...]
### DESCRIPCIPÓN
Elimina (y elimina las etiquetas) una o más imágenes del nodo host. Si una imagen tiene varias etiquetas, usar este comando con la etiqueta como parámetro solo elimina la etiqueta. Si la etiqueta es la única para la imagen, se eliminan tanto la imagen como la etiqueta.

Esto no elimina las imágenes de un registro. No puede eliminar una imagen de un contenedor en ejecución a menos que use la -fopción. Para ver todas las imágenes en un host, use el docker image lscomando.

# DOCKER RM

### USO
 $ docker rm [OPTIONS] CONTAINER [CONTAINER...]
### DESCRIPCIÓN
Retire uno o más contenedores

EJEMPLO:
Esto elimina el contenedor al que se hace referencia en el enlace /redis.

$ docker rm /redis
