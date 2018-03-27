# Comandos CentOS7

## Descripción
El aplicativo rsync permite la copia local y remota de archivos con características mejoradas sobre scp.
Entre las caracteristicas de rsync estan: copia diferencial de archivos,

## Opciones comunes

-v : verbose  
-r : copies data recursively (but don’t preserve timestamps and permission while transferring data  
-a : archive mode, archive mode allows copying files recursively and it also preserves symbolic links, file permissions, user & group ownerships and timestamps  
-z : compress file data  
-h : human-readable, output numbers in a human-readable format  
-e : specify a protocol to use

## Comandos Comunes

| Comando   | Usuario | Descripción   |
|------|------|------|
| --- | root | Los siguientes comandos se ejecutan como el usuario root |
| # yum install rsync | root | Instala ó actualiza rsync |
| # su operativos | operativos | |
| $ cd ~/ | | |
| $ touch test1 test2 test3 | | |
| $ tar cvf backup.tar * | | Crea un backup de los archivos |
| $ mkdir files | | |
| $ rsync -av --exclude='files' * files/ | | Copia los archivos al directorio files |
| $ rsync -zvh backup.tar /tmp/backups/  |  | Copia el backup a otro directorio |
| | | |
| $ rsync -avzh /home/operativos/files /tmp/backups/ |  |  |
| $ rsync -avz files/ distribuidos@192.168.0.101:/home/distribuidos/ |  |  |
| $ rsync -avzh distribuidos@192.168.0.101:~/files /tmp/files |  |  |
| $ rsync -avzhe ssh distribuidos@192.168.0.101:~/files /tmp/files |  |  |
| $ rsync -avzhe ssh backup.tar distribuidos@192.168.0.101:~/backups/ |  |  |
| $ rsync -avzhe ssh --progress /home/rpmpkgs root@192.168.0.100:/root/rpmpkgs |  |  |
| $ rsync -avze ssh --include 'R*' --exclude '*' root@192.168.0.101:/var/lib/rpm/ /root/rpm |  |  |
| $ rsync -avz --delete root@192.168.0.100:/var/lib/rpm/ . | | |
| $ rsync -avzhe ssh --max-size='200k' /var/lib/rpm/ root@192.168.0.100:/root/tmprpm | | |
| $ rsync --remove-source-files -zvh backup.tar /tmp/backups/ | | |
| $ rsync --dry-run --remove-source-files -zvh backup.tar /tmp/backups/ | | |

## Referencias
* https://www.tecmint.com/rsync-local-remote-file-synchronization-commands/
* https://joshua14.homelinux.org/blog/?p=1788
