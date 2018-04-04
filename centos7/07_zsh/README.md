# Comandos CentOS7

## Descripción
ZSH es un interprete de comandos alternativo a bash. En esta guía
se muestra la instalación de zsh y un framework para gestionar su configuración

## Instalación

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

## Plugins 

### Plugin vi-mode

Para habilitar el plugin vi-mode realice lo siguiente
```
$ vi ~/.zshrc
/plugins=
plugins=(git vi-mode)
:x
$ source ~/.zshrc
```

Una vez habilitado presione la tecla "ESC" al momento de requerir editar un comando y entrará a modo vi.
Puede usar por ejemplos las formas de navegación de vi: w (word), b (backwards), dw (delete-word), R (overwrite).

### Plugin zsh-autosuggestions

Para instalar y habilitar el plugin zsh-autosuggestions realice lo siguiente

Clone el repositorio en el directorio de plugins de oh-my-zsh
```
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

Adicione el plugin a la lista de plugins activos
```
$ vi ~/.zshrc
/plugins=
plugins=(git vi-mode zsh-autosuggestions)
:x
$ source ~/.zshrc
```

Modifique el valor para el subrayado de las sugerencias
```
$ vi $ZSH_CUSTOM/dbarragan.zsh
export ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE="fg=1"
:x
$ source ~/.zshrc
```

## FAQ
* No puedo ejecutar el script de instalación de plugins de oh-my-zsh, ¿que hago?
R / Use este comando para indicar a través de una variable la ubicación del directorio de
instalación  
```
export ZSH="$HOME/.dotfiles/oh-my-zsh"; sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## Atajos

En la siguiente tabla encontrará atajos para usar con git:
https://github.com/robbyrussell/oh-my-zsh/wiki/Cheatsheet

### Referencias
* https://github.com/robbyrussell/oh-my-zsh
* https://wiki.archlinux.org/index.php/zsh
* https://code.joejag.com/2014/why-zsh.html
* https://www.youtube.com/watch?v=UgDz_9i2nwc
* https://github.com/zsh-users/zsh-autosuggestions
* https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins/vi-mode
