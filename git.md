# **Comandos GIT** 
Este archivo contiene los comandos GIT más utilizados.


**`git init`** > Se debe de utilizar en la carpeta raíz del proyecto y este comando da inicio a la cración de la base de datos GIT.

**`git add [filename.txt]`** > Agrega UN SOLO archivo a staging que ha sido modificado (previamente guardado) y untracked.

**`git add .`** > Este comando agrega todos los archivos untracked y modificados.

**`git add -am "comentario del commit"`** >Hace ADD y commit al mismo tiempo. NO FUNCIONA EN ARCHIVOS DE RECIENTE CREACION (previamente deben haber sido guardados en un commit).

**`git rm --cached [filename.txt]`** > sacas el archivo de Staging.

**`git rm --force [filename.txt]`** > elimnas el archivo del disco duro y de staging.

**`git commit -m "mensaje a guardar en comit"`** > Este es el comando para hacer commit (previamente debes agregar los archivos en staging).

**`git commit --amend`** > agregaal ultimo commit otra modificacion sin necesidad de hacer un commit nuevo y se puede editar el mensaje que se colocó anteriormente

**`git status`** > Revia el estado del repositorio en ese momento y te da un resumen de los archivos que han sido modificados.

**`git show`** > muestra todos los commit realizados.

**`git show [filename.txt]`** > muestra el historial de cambios de commits que se han hecho y han involucrado a ese archivo.

**`git log [filename.txt]`** > muestra los cambios hechos a un archivo específico.

**`git config --list`** > Muestra la lista de configuracion del entorno de GIT.

**`git config --list --show-origin`** > Muestra el archivo que contiene la configuración del entorno GIT.

**`git config --Global user.name "username"`** > Agregas por primera vez un usuario.

**`git config --Global user.email "username @ mail.com"`** > Agregas por primera vez un usuario.

**`git diff [token_cambio_Antiguo] [token_cambio_nuevo]`** > Muestra las diferencias que hay entre 2 commits.

**`git reset [tokenid] --Hard`** > Traes versiones anteriores y BORRAS todo el avance e informacion de los commits .

**`git resete --hard [HEAD_ID]`** > Traes version anterior/borrada al commit actual.

**`git checkout [tokenid] [filename.txt]`** > Traes un archivo de una versióon previa de un commit. IMPORTANTE: si se hace un commit, se borrará el avance que se tuvo en ese archivo.

**`git checkout Master [filename.txt]`** > Te actualiza el archivo que se encuentra en Master.

**`git checkout [nombre_branch]`** > El apuntador se mueve a la rama que se desea trabajar. (previamente debes hacer un commit, no hacer cambios o mantener los cambios en stash).

**`git branch "NombreBranch"`** > Se agrega una Rama.

**`git branch`** > Muestra cuantas ramas hay y en cual rama se está trabajando en ese momento.

**`git log --stat`** > muestra los commits a detalle (usar "q" para salir).

**`git stash`** > Guarda los cambios que se han estado trabajando para poder moverse entre ramas y/o commits sin perder los avances.

**`git stash list`** > Muestra la lista de Stash guardados.

**`git stash pop`** > Trae de regreso los avances que se guardaron con comando git stash.

**`git stash branch [nombre_branch]`** > mueve los avances hechos a otra rama.

**`git stash drop`** > desecha los avances guardados en stash.

**`git clean -f`** > Borra la lista de archivos que muestra en el comando --dry-run.

**`git clean --dry-run`** > Muestra una lista de archivos preparados para ser borrados.

**`git reflog`** > Muestra TODOS los commits que se han hecho desde el inicio, incluidos los borrados y merges.

**`git grep [word_to_search]`** > busca una palabra en todos los archivos.

**`git grep -n [word]`** > Busca en que LINEA se encuentra la palabra.

**`git grep -c [word]`** > Cuenta cuants veces se ha usado una palabra en un archivo y si se deséa buscar etiquetas se debe hacer de la siguiente manera "< etiqueta >".
  
**`git log -s "[word]`"**> busca las palabras en los commits.
  
#
**Comandos GIT en la nube**

El siguiente comando se utiliza para iniciar la conexión con github o un repositorio remoto por primera vez
**`git pull [nombrecorto] main --allow-unrelated-histories`** > previamente debe agregarse la URL con git remote add. 

**`git remote add [nombrecorto] url_de_github_remoto`** > Se agrega la URL de un repositorio remoto y por lo general se utiliza la palabra "origin" como nombre. (puede que se esté trabajando en otros repositorios remotos al mismo tiempo).

**`git clone url_server`** > Comando para descargar todo de un repositorio en la nube.

**`git push [rama a enviar]:[rama del server]`** > se envían todo a un repositorio en la nube.

**`git fetch`** > se usa para descargar actualizaciones del server y guardarlos en local.

**`git merge`** > combina los archivos del repositorio del git fetch O hace FUSIONA dos commits.

**`git pull`** > los comandos fetch y merge al mismo tiempo.

#
**Arreglar gitignore file**


**Step 1:** Commit all your pending changes in the repo which you want to fix and push that.

**Step 2:** Now you need to remove everything from the git index in order to refresh your git repository. This is safe. Use this command:

`git rm -r --cached .`

**Step 3:** Now you need to add everything back into the repo, which can be done using this command:

`git add .`

**Step 4:** Finally you need to commit these changes, using this command:

`git commit -m "Gitignore issue fixed"`

#
**Malas prácticas**

**REBASE:** Se utiliza para reescribir la historia, lo que hace es desaparecer una rama y fusionarla al master u otra rama. SOLO debe hacerse en loocal y NO EN MASTER de un servidor remoto. Pero por lo general se recomienda mejor hacer un merge.

**`git rebase [nombre_branch]`** > Debe ejecutrase primeramente en la rama que se quiere desaparecer (git rebase experimento), hace git checkout a la rama que se quiere incorporar (git checkout master) y al final hacer (git rebase master).
  
**`git cherry-pick [id_commit]`** > Se utiliza para traer un commit a una rama y agregarlo.


#
**CREACIÓN DE LLAVES SSH Y CONFIGURACIÓN (windows y linux)**


1 - Ir a home y ejecutar >`ssh-keygen  -t rsa -b 4096 -C "youremail @ example.com"` 

2 - Comprobar que el servidor de SSH está corriendo > `eval "$(ssh-agent -s)" `

3 - Agregar llave al sistema > `ssh-add ~/.ssh/id_rsa`

4 - Compartir la informacion de la llave `id_rsa.pub`

