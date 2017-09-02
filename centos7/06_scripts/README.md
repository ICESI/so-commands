# Comandos CentOS7

## Scripts y Ejecución

### Script que ejecuta comandos de consola

Cree un script con nombre bash_script

**bash_script**
```
# vi bash_script
#!/bin/sh
echo "Ejemplo de un script que ejecuta comandos"
user=$(whoami)
echo "soy $user"
sleep 2
path=`pwd`
echo "estoy en $path"
```

Digite los siguientes comandos y reflexione sobre los resultados obtenidos

```
[operativos@localhost scripts]$ ./bash_script
bash: ./bash_script: Permiso denegado
[operativos@localhost scripts]$ sh bash_script
Ejemplo de un script que ejecuta comandos
soy operativos
estoy en /home/operativos/scripts
[operativos@localhost scripts]$ ls -l
total 4
-rw-rw-r--. 1 operativos operativos 134 ago 23 08:32 bash_script
[operativos@localhost scripts]$ chmod u+x bash_script
[operativos@localhost scripts]$ ls -l
total 4
-rwxrw-r--. 1 operativos operativos 134 ago 23 08:32 bash_script
[operativos@localhost scripts]$ ./bash_script
Ejemplo de un script que ejecuta comandos
soy operativos
estoy en /home/operativos/scripts
```

### Script en python

Cree un script con nombre python_script

**python_script**
```
# vi python_script
#!/usr/bin/python
print('script con python')
```

Digite los siguientes comandos y reflexione sobre los resultados obtenidos

```
[operativos@localhost scripts]$ ./python_script
bash: ./python_script: Permiso denegado
[operativos@localhost scripts]$ python python_script
script con python
[operativos@localhost scripts]$ ls -l
total 4
-rw-rw-r--. 1 operativos operativos 134 ago 23 08:32 python_script
[operativos@localhost scripts]$ chmod u+x python_script
[operativos@localhost scripts]$ ls -l
total 4
-rwxrw-r--. 1 operativos operativos 134 ago 23 08:32 python_script
[operativos@localhost scripts]$ ./python_script
script con python
```

### Script en python que ejecutan comandos de consola

Cree un script con nombre fake_ls

**fake_ls**
```
#!/usr/bin/python

print("Doing something...")

from subprocess import call
call(["ls"])
```

Digite los siguientes comandos y reflexione sobre los resultados obtenidos

```
# alias ls=./fake_ls
# ls
