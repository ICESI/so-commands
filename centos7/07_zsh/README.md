# Comandos CentOS7

## Descripción
ZSH es un interprete de comandos alternativo a bash. En esta guía
se muestra la instalación de zsh y un framework para gestionar su configuración

## Guía

Digite los siguientes comandos como root

```
# yum install zsh -y
# yum install git -y
# adduser operativos
# passwd operativos
# su operativos
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
$ chsh -s /bin/zsh
```

En la siguiente tabla encontrará atajos para usar con git:
https://github.com/robbyrussell/oh-my-zsh/wiki/Cheatsheet

### Referencias
* https://github.com/robbyrussell/oh-my-zsh
* https://wiki.archlinux.org/index.php/zsh
* https://code.joejag.com/2014/why-zsh.html
* https://www.youtube.com/watch?v=UgDz_9i2nwc
