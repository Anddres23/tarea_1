# tarea_1
Aquí se realizara el deber 1

### Saavedra y Stouffer (2013) estudiaron varias redes planta-polinizador. Estos se pueden representar como matrices rectangularesdonde las filas son polinizadores, las columnas plantas, un 0 indica la ausencia y 1 la presencia de una interacción entre la planta y el polinizador. Los datos de Saavedra y Stouffer (2013) se pueden encontrar en el directorio CSB / unix / data / Saavedra2013. 

1. Escriba un guión que tome uno de estos archivos y determine el número de filas (polinizadores) y columnas (plantas). Tenga en cuenta que 
las columnas están separadas por espacios y que hay un espacio al final de cada línea. Tu guión debería regresar. 

como primer paso se localizar[a la carpeta de interes, en este caso " Saavedra2013"
Nos ubicamos en 'Guit bash' y acontinuacion localizamos la carpeta con los comandos:

Dell@DellG7Andres MINGW64 ~
$ cd documents

Dell@DellG7Andres MINGW64 ~/documents
$ cd practica\ bio/

Dell@DellG7Andres MINGW64 ~/documents/practica bio
$ cd CSB-master

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master
$ cd unix/

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix
$ cd data/

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data
$ ls
Buzzard2015_about.txt    Gesquiere2011_data.csv  Pacifici2013_about.txt  Saavedra2013_about.txt
Buzzard2015_data.csv     Marra2014_about.txt     Pacifici2013_data.csv   miRNA/
Gesquiere2011_about.txt  Marra2014_data.fasta    Saavedra2013/

Observamos que es aqui donde se encuentra la carpeta, ingresamos en ella:

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data
$ cd Saavedra2013

Apreciamos su contenido:
Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data/Saavedra2013
$ ls
n1.txt   n14.txt  n19.txt  n23.txt  n28.txt  n32.txt  n37.txt  n41.txt  n46.txt  n50.txt  n55.txt  n6.txt
n10.txt  n15.txt  n2.txt   n24.txt  n29.txt  n33.txt  n38.txt  n42.txt  n47.txt  n51.txt  n56.txt  n7.txt
n11.txt  n16.txt  n20.txt  n25.txt  n3.txt   n34.txt  n39.txt  n43.txt  n48.txt  n52.txt  n57.txt  n8.txt
n12.txt  n17.txt  n21.txt  n26.txt  n30.txt  n35.txt  n4.txt   n44.txt  n49.txt  n53.txt  n58.txt  n9.txt
n13.txt  n18.txt  n22.txt  n27.txt  n31.txt  n36.txt  n40.txt  n45.txt  n5.txt   n54.txt  n59.txt

Luego seleccionamos uno de los documentos, en este caso se seleccionara 'n33.txt'  y contamos el numero de filas con el siguiente comando:

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data/Saavedra2013
$ wc -l n33.txt

a lo que obtemos '70 n33.txt' 

Ahora contaremos el numero de columnas del documento seleccionado con el comando:
Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data/Saavedra2013
$ head -n 1 n33.txt | tr -d '  '  | tr -d ' \ n '|wc -c
 Notese que tenemos en cuenta de eliminar los espacios para no tener errores de conteo de espacios en blanco
 el sesultado es: '21'
