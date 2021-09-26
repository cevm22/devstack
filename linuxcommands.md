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
> 3 - Finalmente reiniciar terminal.

**Agregar alias en terminal**

> 1 - Ir hacia  `~/.bashrc` y agregar hasta al final una sección de "alias"
> 2 - formato de agregado `alias c='clear'`
> 3 - Salir con la secuencia ESC + Swift + Z + Z
> 4 - reiniciar bashrc con el comando  `. ~/.bashrc`





