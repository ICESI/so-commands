# Comandos CentOS7

## Scripts y Ejecución

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

```
# vi python_script
#!/usr/bin/python
print('script con python')
```

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
