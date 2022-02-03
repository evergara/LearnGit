# Aprendiendo Git Beginning

## Definicion: 
**Git** es uno de los sistemas de control de versiones más extendidos actualmente, su principal característica es que distribuido. Nace de la mano de Lius Torvalds en el año 2005 para gestionar el código fuente de Linux y poco a poco va ganando adeptos en comunidades como GitHub o ButBucket.

######  Características de GIT
**Git** es distribuido, una de las diferenciaciones más importante con otros repositorios como SVN es que es un sistema distribuido. No es necesario un servidor central, cada programador tiene una copia completa del repositorio en su equipo y al hacer un cambio se propaga a todos los nodos. Esto permite un gran rendimiento en grandes desarrollos, las búsquedas son mucho más eficaces lo que supone una gran rapidez para detectar diferencias entre archivos.

###### Ventajas y desventajas de GIT
Gran rendimiento en programas grandes, gracias a ser un sistema distribuido, las búsquedas son mucho más eficaces lo que supone una gran rapidez para detectar diferencias entre archivos.
Su sistema de ramas o branches es muy flexible, pudiendo crear ramas locales independientes de un repositorio centralizado. Se puede crear distintos branches para distintos usos, una de las ramas se deja estable con el código de producción, y los nuevos desarrollos se hacen en ramas paralelas, al finalizar basta con hacer un merge para unir los cambios. Otra opción es, al ser distribuido, que un desarrollador haga sus cambios en una rama en local que no es necesaria subir al resto de nodos.

## Los tres estados que maneja Git: 
Git tiene tres estados principales en los que pueden encontrarse los o el archivo(s): **confirmado (committed)**, **modificado (modified)**, y **preparado (staged)**. 
- **Confirmado:** Significa que los datos están almacenados de manera segura en tu base de datos local. 
- **Modificado:** Significa que has modificado el archivo pero todavía no lo has confirmado a tu base de datos. 
- **Preparado:** Significa que has marcado un archivo modificado en su versión actual para que vaya en tu próxima confirmación al repositorio remoto.

Esto nos lleva a las tres secciones principales de un proyecto de Git: el directorio de Git (**Git directory**), el directorio de trabajo (**working directory**), y el área de preparación (**staging area**).

- **El directorio de Git:** Es donde Git almacena los metadatos y la base de datos de objetos para tu proyecto. Es la parte más importante de Git, y es lo que se copia cuando clonas un repositorio desde otro ordenador.

- **El directorio de trabajo:** Es una copia de una versión del proyecto. Estos archivos se sacan de la base de datos comprimida en el directorio de Git, y se colocan en disco para que los puedas usar o modificar.

- **El área de preparación:** Es un sencillo archivo, generalmente contenido en tu directorio de Git, que almacena información acerca de lo que va a ir en tu próxima confirmación. A veces se le denomina índice, pero se está convirtiendo en estándar el referirse a ella como el área de preparación.

######  El flujo de trabajo básico en Git es algo así:

- Modificas una serie de archivos en tu directorio de trabajo.
- Preparas los archivos, añadiendolos a tu área de preparación.
- Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación, y almacena esas instantáneas de manera permanente en tu directorio de Git.
- Si una versión concreta de un archivo está en el directorio de Git, se considera confirmada (committed). Si ha sufrido cambios desde que se obtuvo del repositorio, pero ha sido añadida al área de preparación, está preparada (staged). Y si ha sufrido cambios desde que se obtuvo del repositorio, pero no se ha preparado, está modificada (modified).

**NOTA:** ###### Esto es lo más importante a recordar acerca de Git si quieres que el resto de tu proceso de aprendizaje prosiga sin problemas.

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



# Uso de Git

Despues de saber fundamentos genrales de git, pasaremos a la accion con git. Debes instalar git en la maquina personal de trabajo, para esto hay buenos turtoriales en internet, asi que este paso lo omiteriremos.

## Configurar Git

Una vez instalado nuestro cliente Git, lo primero que tenemos que hacer es configurar nuestro nombre de usuario y dirección de correo electrónico.

Si utilizamos la opción —global, esto solo lo tenemos que hacer una vez, puesto que a partir de entonces lo tomará por defecto. Así por ejemplo,

```
git config --global user.name "TuNombreAUsar"
git config --global user.email corre@micorreo.com
```

Si en un proyecto concreto queremos utilizar otro usuario o email, lo que debemos hacer es no añadir la opción —global.

Estos dos parámetros son importantes porque las confirmaciones de cambios utilizan esta información.

El resto de parámetros a configurar ya son opcionales. Algunos que te pueden ser de utilidad son:

- El editor de texto. En mi caso particular utilizo nano cuando edito en el emulador de terminal:
```
git config --global core.editor nano
```

- Herramienta de diferencias. La herramienta de diferencias (que comentaremos mas adelante) es la que se encarga para resolver conflictos de unión:

```
gif config --global merge.tool vimdiff
```
 
Por último si quieres ver tu configuración, puedes ejecutar la siguiente orden en el emulador de terminal:

```
git config --list
```

## Repositorio git
Una vez de instalado y configurado Git, ahora el turno es crear nuestro primer repositorio.

######  Crear Repositorio
para crear un repositorio tenemos dos opciones.
- **Crear un repositorio de cero**
- **Clonar un repositorio**
######  Subir cambios
######  Crear Ramas
######  Cambiar de Ramas
######  Diff

## Alias
### Log
git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"

### Status
git config --global alias.s status --short

### Alternativa útil de status
git config --global alias.s status -sb

