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

Para habilitar el plugin vi-mode realice lo siguiente (use /plugins= para posicionarse en la linea apropiada)
```
$ vi ~/.zshrc
plugins=(git vi-mode)
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
plugins=(git vi-mode zsh-autosuggestions)
$ source ~/.zshrc
```

Modifique el valor para el subrayado de las sugerencias
```
$ vi $ZSH_CUSTOM/dbarragan.zsh
export ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE="fg=1"
$ source ~/.zshrc
```

Para modificar el prompt edite el tema configurado en el archivo ~/.zshrc. Para el caso de robbyrussell.zsh-theme
```
vi ~/.oh-my-zsh/themes/robbyrussell.zsh-theme
PROMPT='${ret_status} $(git_prompt_info)'
```

### Plugin zsh-history-substring-search

Para instalar y habilitar el plugin zsh-history-substring-search realice lo siguiente

Clone el repositorio en el directorio de plugins de oh-my-zsh
```
git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
```

Adicione el plugin a la lista de plugins activos
```
$ vi ~/.zshrc
plugins=(git vi-mode zsh-autosuggestions history-substring-search)
$ source ~/.zshrc
```

Adicione las siguientes lineas para autocompletar con las flechas del teclado
```
$ vi ~/.zshrc
bindkey '^[[A' history-substring-search-up
bindkey '^[[B' history-substring-search-down
$ source ~/.zshrc
```

### Plugin zsh-completions

Para instalar y habilitar el plugin zsh-completions realice lo siguiente
```
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions
```

Adicione las siguientes lineas para autocompletar con dos tabulados
```
$ vi ~/.zshrc
plugins=(git vi-mode zsh-autosuggestions history-substring-search zsh-completions)
autoload -U compinit && compinit
$ source ~/.zshrc
```

#### AWS EKS

Para adicionar un completion, en este caso para el gestor de creación de cluster de eks de nombre eksctl
```
eksctl completion zsh > ~/.oh-my-zsh/completions/_eksctl
```

Para usarlos, digite eksctl y dos tabulados
```
➜  ~ eksctl completion 
completion  -- Generates shell completion scripts for bash, zsh or fish
create      -- Create resource(s)
delete      -- Delete resource(s)
drain       -- Drain resource(s)
get         -- Get resource(s)
help        -- Help about any command
scale       -- Scale resources(s)
set         -- Set values
unset       -- Unset values
update      -- Update resource(s)
upgrade     -- Upgrade resource(s)
utils       -- Various utils
version     -- Output the version of eksctl
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
* https://github.com/zsh-users/zsh-history-substring-search
* https://github.com/zsh-users/zsh-completions
