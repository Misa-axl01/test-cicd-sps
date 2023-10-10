# test-cicd-sps
El ambiente de desarrollo es una máquina virtual en la nube. 1. ¿Es posible desplegar de forma automática el 
artefacto guardado en packages utilizando Github Actions? Si, por ejemplo existe un flujo de acciones para poder desplegar una imagen de docker hacia AWS ECS.


- Si es posible desplegar el artefacto en la máquina virtual utilizando Githb Actions. Crea el workflow que se 
dispare al agregar un nuevo artefacto en packages e imprima en el log “Realizando despliegue por SSH”, la 
lista de acciones de Github que usarías para realizar el despliegue y en dónde se debería guardar la llave 
privada para conectarse por SSH al servidor sin que el equipo de desarrollo tenga acceso a ella.
R= investigue un poco pero por falta de tiempo ya no pude desarrollar el codigo, de acciones se usaria scp para copiar el paquete a la maquina y ssh para realizar la conexión, la llave ssh se podria guardar en los secretos
asi el equipo de desarrollo puede hacer uso de ella como objeto pero no podria ver el contenido de la llave, asi como uso de las rutas dentro del servidor en donde se dejara el paquete y el script con los comandos a ejecutar
para el despliegue dentro de la VM.
