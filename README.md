# Aprendiendo Git Beginning

## Definicion: 
**Git** es uno de los sistemas de control de versiones más extendidos actualmente, su principal característica es que distribuido. Nace de la mano de Lius Torvalds en el año 2005 para gestionar el código fuente de Linux y poco a poco va ganando adeptos en comunidades como GitHub o ButBucket.

######  Características de GIT
**Git** es distribuido, una de las diferenciaciones más importante con otros repositorios como SVN es que es un sistema distribuido. No es necesario un servidor central, cada programador tiene una copia completa del repositorio en su equipo y al hacer un cambio se propaga a todos los nodos. Esto permite un gran rendimiento en grandes desarrollos, las búsquedas son mucho más eficaces lo que supone una gran rapidez para detectar diferencias entre archivos.

###### Ventajas y desventajas de GIT
Gran rendimiento en programas grandes, gracias a ser un sistema distribuido, las búsquedas son mucho más eficaces lo que supone una gran rapidez para detectar diferencias entre archivos.
Su sistema de ramas o branches es muy flexible, pudiendo crear ramas locales independientes de un repositorio centralizado. Se puede crear distintos branches para distintos usos, una de las ramas se deja estable con el código de producción, y los nuevos desarrollos se hacen en ramas paralelas, al finalizar basta con hacer un merge para unir los cambios. Otra opción es, al ser distribuido, que un desarrollador haga sus cambios en una rama en local que no es necesaria subir al resto de nodos.


## Comandos basicos:

- **git status:** Comprueba el estado de repositorio actual
- **git add:** Comprueba si hay cambios, y addiciona los cambios al stage
- **commit:** Subida de archivos a tu repositorio local, a diferencia de en otros sistemas como SVN con el commit no se propaga el cambio.
- **git pull:** Actualiza la versión local del código, equivaldria al update de SVN
- **git push:** Envia los cambios locales comiteados al resto de nodos, actualiza el repositorio remoto
- **git log:** Puedes ver el historial de cambios
- **git diff:** Ver los cambios realizados en un archivo
- **git init:** sea un repositorio vacío de Git
- **git clone:** El comando 'git clone` es en realidad una especie de envoltura alrededor de varios otros comandos. Éste crea un nuevo directorio, entra en él y ejecuta git init para que sea un repositorio vacío de Git, añade uno remoto (git remote add) hacia la dirección URL que se le pasa (por defecto llamado origin), ejecuta un git fetch de ese repositorio remoto y después activa el último commit en el directorio de trabajo con git checkout.