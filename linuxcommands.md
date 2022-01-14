#
**COMANDOS MÁS USADOS EN LINUX**
#

**`sudo chown -R [userlinux] /var/home`** > Cambia la propiedad del archivos y todo su contenido

**Agregar colores y apuntadores GIT en linea de comandos:**
> 1 - Ir hacia  `~/.bashrc` y agregar la siguiente función al final del archivo:
> 
> `parse_git_branch() { git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'}`
>
> `export PS1="\u@\h \[\e[32m\]\w \[\e[91m\]\$(parse_git_branch)\[\e[00m\]$ "`
> 
> 2 - Salir con la secuencia ESC + Swift + Z + Z
> 
> 3 - Finalmente reiniciar terminal con comando source `source ~/.bashrc`

**Agregar alias en terminal**

> 1 - Ir hacia  `~/.bashrc` y agregar hasta al final una sección de "alias"
> 
> 2 - formato de agregado `alias c='clear'`
> 
> 3 - Salir con la secuencia ESC + Swift + Z + Z
> 
> 4 - reiniciar bashrc con el comando  `. ~/.bashrc`

**Reiniciar WSL cuando no funciona VS**

En terminal Powershell como administrador ejecutar el comando `wsl --shutdown` esto hace forza a reiniciar WSL y da solucion cuando no se conecta el VS directo con WSL

**Para obtener la ruta de archivos de WSL**
`explorer.exe .` No olvidar el "espacio y punto" al final
