# tarea_1
Aquí se realizara el deber 1

### Saavedra y Stouffer (2013) estudiaron varias redes planta-polinizador. Estos se pueden representar como matrices rectangularesdonde las filas son polinizadores, las columnas plantas, un 0 indica la ausencia y 1 la presencia de una interacción entre la planta y el polinizador. Los datos de Saavedra y Stouffer (2013) se pueden encontrar en el directorio CSB / unix / data / Saavedra2013. 

1. Escriba un guión que tome uno de estos archivos y determine el número de filas (polinizadores) y columnas (plantas). Tenga en cuenta que 
las columnas están separadas por espacios y que hay un espacio al final de cada línea. Tu guión debería regresar. 

como primer paso se localizar[a la carpeta de interes, en este caso " Saavedra2013"
Nos ubicamos en 'Guit bash' y acontinuacion localizamos la carpeta con los comandos:

Dell@DellG7Andres MINGW64 ~

$ cd documents <-comando

Dell@DellG7Andres MINGW64 ~/documents

$ cd practica\ bio/ <-comando

Dell@DellG7Andres MINGW64 ~/documents/practica bio

$ cd CSB-master <-comando

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master

$ cd unix/ <-comando

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix

$ cd data/ <-comando

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data

$ ls<-comando

Buzzard2015_about.txt    Gesquiere2011_data.csv  Pacifici2013_about.txt  Saavedra2013_about.txt
Buzzard2015_data.csv     Marra2014_about.txt     Pacifici2013_data.csv   miRNA/
Gesquiere2011_about.txt  Marra2014_data.fasta    Saavedra2013/

Observamos que es aqui donde se encuentra la carpeta, ingresamos en ella:

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data

$ cd Saavedra2013 <-comando

Apreciamos su contenido:
Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data/Saavedra2013

$ ls <-comando
 
n1.txt   n14.txt  n19.txt  n23.txt  n28.txt  n32.txt  n37.txt  n41.txt  n46.txt  n50.txt  n55.txt  n6.txt
n10.txt  n15.txt  n2.txt   n24.txt  n29.txt  n33.txt  n38.txt  n42.txt  n47.txt  n51.txt  n56.txt  n7.txt
n11.txt  n16.txt  n20.txt  n25.txt  n3.txt   n34.txt  n39.txt  n43.txt  n48.txt  n52.txt  n57.txt  n8.txt
n12.txt  n17.txt  n21.txt  n26.txt  n30.txt  n35.txt  n4.txt   n44.txt  n49.txt  n53.txt  n58.txt  n9.txt
n13.txt  n18.txt  n22.txt  n27.txt  n31.txt  n36.txt  n40.txt  n45.txt  n5.txt   n54.txt  n59.txt

Luego seleccionamos uno de los documentos, en este caso se seleccionara 'n33.txt'  y contamos el numero de filas con el siguiente comando:

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data/Saavedra2013

$ wc -l n33.txt <-comando

a lo que obtemos '70 n33.txt' 

Ahora contaremos el numero de columnas del documento seleccionado con el comando:
Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data/Saavedra2013

$ head -n 1 n33.txt | tr -d '  '  | tr -d ' \ n '|wc -c <-comando

 Notese que tenemos en cuenta de eliminar los espacios para no tener errores de conteo de espacios en blanco
 el sesultado es: '21'
 
 
 
 
### Segundo ejercicio

2. Escriba un guión que imprima el número de filas y columnas para cada red:
partiendo de nuestra estancia del primer ejercicio contaremos todas las primeras filas y primeras columnas de todos nuestros 
archivos existentes en la carpeta'Saavedra2013' con el siguiente comando:

Dell@DellG7Andres MINGW64 ~/documents/practica bio/CSB-master/unix/data/Saavedra2013

$ for file in $(ls *.txt); do wc -l $file;  head -n1 $file | grep -o " " | wc -l; done  <-comando

obteniendo el siguiente resultado: 

97 n1.txt
80
14 n10.txt
20
270 n11.txt
91
7 n12.txt
72
61 n13.txt
17
35 n14.txt
15
38 n15.txt
11
118 n16.txt
24
76 n17.txt
31
13 n18.txt
14
10 n19.txt
16
62 n2.txt
41
18 n20.txt
7
19 n21.txt
45
19 n22.txt
36
179 n23.txt
26
80 n24.txt
28
17 n25.txt
16
82 n26.txt
40
27 n27.txt
5
90 n28.txt
19
61 n29.txt
25
25 n3.txt
36
8 n30.txt
19
28 n31.txt
25
45 n32.txt
21
70 n33.txt
20
79 n34.txt
25
14 n35.txt
8
40 n36.txt
169
44 n37.txt
13
51 n38.txt
99
33 n39.txt
25
101 n4.txt
11
28 n40.txt
18
12 n41.txt
10
42 n42.txt
8
55 n43.txt
29
56 n44.txt
9
36 n45.txt
61
58 n46.txt
17
139 n47.txt
41
118 n48.txt
49
47 n49.txt
23
21 n5.txt
7
45 n50.txt
46
8 n51.txt
15
33 n52.txt
7
34 n53.txt
13
126 n54.txt
25
14 n55.txt
50
110 n56.txt
207
14 n57.txt
11
678 n58.txt
90
663 n59.txt
130
9 n6.txt
31
16 n7.txt
25
19 n8.txt
33
12 n9.txt
22
