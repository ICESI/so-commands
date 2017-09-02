# Comandos CentOS7

## Comandos comunes

| Comando   | Usuario | Descripción   |
|------|------|------|
| # su operativos | root | Inicie sesión como el usuario operativos |
| $ wget http://www.gutenberg.org/cache/epub/19033/pg19033.txt | operativos | Descargue el archivo especificado en la url |
| $ grep -in Alice pg19033.txt | usuario random | Retorne las lineas del archivo numeradas donde se encuentra la palabra Alice |
| $ sed s/Alice/Hannie/ pg19033.txt > pg19033-new.txt | operativos | Reemplaza la palabra Alice con la palabra Hannie y escribir los cambios en un nuevo archivo |
| $ head pg19033.txt | operativos | Imprima en la salida estandar las primeras 10 líneas del archivo |
| $ head -5 pg19033.txt | operativos | Imprime en la salida estandar las primeras 5 líneas del archivo |
| $ tail pg19033.txt | operativos | Imprima en la salida estandar las últimas 10 líneas del archivo |
| $ tail -5 pg19033.txt | operativos | Imprime en la salida estandar las últimas 5 líneas del archivo |
| $ less pg19033.txt | operativos | Imprima una página a la vez |
