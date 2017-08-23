# Comandos CentOS7

## Prerrequisitos

Crear un fork del repositorio https://github.com/ICESI-Training/sd-workshop1  
En el fork crear una rama student_id/add-solutions donde student_id es su código de estudiante

## Comandos comunes

| Comando   | Usuario | Descripción   |
|------|------|------|
| --- | root | Los siguientes comandos se ejcutan como el usuario root |
| # su redes | root | Inicie sesión como el usuario redes |
| $ cd /home/redes/ | redes | Ingrese al directorio de usuario del usuario redes |
| $ pwd | redes | Verifique el lugar del path donde se encuentra |
| $ exit | redes | Salga de la sesión del usuario redes |
| # su operativos | root | Inicie sesión como el usuario operativos |
| $ cd ~/ | operativos | Ingrese al directorio de usuario del usuario operativos |
| $ pwd | operativos | Verifique el lugar del path donde se encuentra |
| $ clear | operativos | Borre los datos de la consola de Linux |
| $ sudo yum install git -y | operativos | Verifique que el usuario operativos no tiene permisos para ejecutar yum |
| $ exit | operativos | Salga de la sesión del usuario operativos |
| # cat /var/spool/mail/root | operativos | Verifique que el incidente ha sido reportado |
| # visudo | root | Ejecute el comando visudo |
| Presione la tecla ESC, :set number | root | Visualice los números de línea del archivo |
| :91 | root | Vaya a la línea 91 |
| Presione la tecla o | root | Adicionar la linea: operativos ALL=(ALL) ALL |
| :x | root | Salir de visudo |
| # su operativos | root | Inicie sesión como el usuario operativos |
| $ sudo yum install git -y | operativos | Instale el cliente de git |
| $ cd ~/ ó cd | operativos | Ingrese al directorio de usuario del usuario operativos |
| $ git clone https://github.com/student_repository/so-workshop1.git | operativos | Clone el repositorio al que hizo fork al principio de esta guía | 
| $ cd so-workshop1 | operativos | Ingrese al directorio so-workshop1 |
| $ git branch -a | operativos | Visualice las ramas disponibles |
| $ git checkout student_id/add-solutions | operativos | Cambie a la rama student_id/add-solutions |
| $ mkdir student_id | operativos | Cree un directorio de nombre student_id donde student_id es su códugo de estudiante |
| $ touch README.md | operativos | Cree el archivo README.md |
| $ git status | operativos | Verifique el estado de los archivos del repositorio |
| $ git add README.md | operativos | Adicione el archivo README.md al commit |
| $ git config --global user.name "username" | operativos | Configure su nombre de usuario (Este aparecerá en github como autor del commit)|
| $ git config --global user.email username@correo.icesi.edu.co | operativos | Configure su correo |
| $ git commit -m "Add README file" | operativos | Adicione un mensaje descriptivo al commit |
| $ git push origin student_id/add-solutions | operativos | Envie los cambios del commit a github |

## Recordar
Un gran poder conlleva una gran responsabilidad

```
We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.
```
