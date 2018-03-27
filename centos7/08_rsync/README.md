# Comandos CentOS7

## Descripción
El aplicativo rsync permite la copia local y remota de archivos con características mejoradas sobre scp.
Entre las caracteristicas de rsync estan: copia diferencial de archivos, omitir directorios, limitar ancho de banda para transferencia, sincronizar directorios, entre otras.

## Opciones comunes

-v : verbose  
-r : copies data recursively (but don’t preserve timestamps and permission while transferring data  
-a : archive mode, archive mode allows copying files recursively and it also preserves symbolic links, file permissions, user & group ownerships and timestamps  
-z : compress file data  
-h : human-readable, output numbers in a human-readable format  
-e : specify a protocol to use

## Comandos Comunes

### Ejemplo 1

| Comando   | Usuario | Descripción   |
|------|------|------|
| --- | root | Los siguientes comandos se ejecutan como el usuario root |
| # yum install rsync | root | Instala ó actualiza rsync |
| # su operativos | operativos | |
| $ cd ~/ | | |
| $ touch test1 test2 test3 | | |
| $ tar cvf backup.tar * | | Crea un backup de los archivos |
| $ mkdir -p /tmp/backups | | |
| $ rsync -zvh backup.tar /tmp/backups/  |  | Copia el archivo backup al directorio backups |
| $ mkdir files | | |
| $ rsync -av --exclude='files' * files/ | | Copia los archivos al directorio files omitiendo el directorio files |

## Actividades
* Seleccione al menos 3 de los comandos que se muestran a continuación e indique un caso útil para
el uso de cada comando. Puede realizar variaciones sobre la fuente y el destino

| Comando   | Usuario | Descripción   |
|------|------|------|
| --- | operativos | Los siguientes comandos se ejecutan como el usuario operativos |
| $ rsync -avzh ~/files /tmp/backups/ |  | Copia el directorio files al directorio backups |
| $ rsync -avz files/ distribuidos@192.168.0.101:~/ |  |  |
| $ rsync -avzh distribuidos@192.168.0.101:~/files ~/files |  |  |
| $ rsync -avzhe ssh distribuidos@192.168.0.101:~/files ~/files |  |  |
| $ rsync -avzhe ssh backup.tar distribuidos@192.168.0.101:~/backups/ |  |  |
| $ rsync -avzhe ssh --progress ~/files distribuidos@192.168.0.100:~/files |  |  |
| $ rsync -avze ssh --include 'R*' --exclude '*' root@192.168.0.101:/var/lib/rpm/ /root/rpm |  |  |
| $ rsync -avz --delete distribuidos@192.168.0.101:~/files/ . | | |
| $ rsync -avzhe ssh --max-size='200k' ~/files/ distribuidos@192.168.0.101:~/files | | |
| $ rsync --remove-source-files -zvh backup.tar /tmp/backups/ | | |
| $ rsync --dry-run --remove-source-files -zvh backup.tar /tmp/backups/ | | |

## Referencias
* https://www.tecmint.com/rsync-local-remote-file-synchronization-commands/
* https://joshua14.homelinux.org/blog/?p=1788
