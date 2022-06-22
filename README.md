# PyNet
Lecciones de Python aplicado a Ingeniería de Redes

Lecciones de Kirk Byers

Nota1: hay una tabla de contenido para cada video en la parte inferior de este correo electrónico, incluidas las marcas de tiempo de la ubicación de varios contenidos. Esto debería ser útil para navegar por los videos.

Nota 2: debe centrarse fundamentalmente en Python3 en este momento y debe migrar activamente cualquier código Python2 heredado a Python3. El soporte de Python2 finalizó (de los desarrolladores principales de Python) el 1 de enero de 2020.

SECCION 001

En este sección de Learning Python vamos a cubrir lo siguiente:
 
Introducción

Vídeo https://vimeo.com/243034300
La duración es de 7 minutos.
 

¿Por qué aprender programación?
Vídeo https://vimeo.com/243905715
(1 minuto)
 

¿Por qué Python?
Vídeo https://vimeo.com/243909371
(3 minutos)
 

Python2 frente a Python3
Vídeo https://vimeo.com/243912631
(2 minutos)
 

Características de Python
Vídeo https://vimeo.com/243918300
(5 minutos)
 

El shell del intérprete de Python
Vídeo https://vimeo.com/242411259
(9 minutos)
 

IPython
Vídeo https://vimeo.com/242460561
(4 minutos)
 

Imprimiendo a stdout y leyendo desde stdin
Vídeo https://vimeo.com/243028886
(6 minutos)
 

Dir, Ayuda y Variables
Vídeo https://vimeo.com/243480156
(10 minutos)
 

Cuerdas de Python (Parte 1)
Vídeo https://vimeo.com/243481392
(6 minutos)
 

Cuerdas de Python (Parte 2)
Vídeo https://vimeo.com/243482081
(8 minutos)
 

Cuerdas de Python (Parte 3)
Vídeo https://vimeo.com/243482871
(10 minutos)
 

Formato de cadenas de Python (Parte 1)
Vídeo https://vimeo.com/243936489
(12 minutos)
 

Formato de cadena de Python (Parte 2)
Vídeo https://vimeo.com/243956669
(4 minutos)

-------------------------------------------- 

1. Convenciones de nomenclatura de Python:

     a. Para nombres de variables, nombres de funciones, nombres de objetos y nombres de módulos, use minúsculas separadas 
     por guiones bajos, por ejemplo:

      my_router
      find_set_of_devices
      convert_id_string_to_list

    b. Para los nombres de las clases, escriba en mayúscula la primera letra de cada palabra. No utilice guiones bajos. Por 
    ejemplo:

      ManyToManyField
      ClientHistory
      UserProfile

    C. Para constantes, utilice todas las mayúsculas; utilice guiones bajos para la separación de palabras.

      PI = 3.14
      EMAIL_MODE
      EMAIL_FROM_ADDRESS
 

Ejercicios

El código de referencia para estos ejercicios está publicado en GitHub en:

https://github.com/ktbyers/pynet/tree/master/learning_python/lesson1

1. Cree una secuencia de comandos de Python que tenga tres variables: ip_addr1, ip_addr2, ip_addr3 (que representan tres direcciones IP correspondientes). Imprima estas tres variables en la salida estándar utilizando una sola declaración de impresión.

Haga que su declaración de impresión sea compatible con Python2 y Python3.

Si está utilizando Linux o MacOS, haga que su programa sea ejecutable agregando una línea shebang y cambiando los permisos de los archivos (es decir, chmod 755 exercise1.py).

2. Pida al usuario que ingrese una dirección IP desde la entrada estándar. Lea la dirección IP y divídala en sus octetos. Imprime los octetos en decimal, binario y hexadecimal.

La salida de su programa debe tener el siguiente aspecto:

$ python ejercicio2.py
Ingrese una dirección IP: 80.98.100.240

    Octeto1 Octeto2 Octeto3 Octeto4
-------------------------------------------------- ----------
      80 98 100 240
   0b1010000 0b1100010 0b1100100 0b11110000
     0x50 0x62 0x64 0xf0
-------------------------------------------------- ----------

Cuatro columnas, quince caracteres de ancho, una columna de encabezado, datos centrados en la columna.

3. Cree tres variables diferentes. La primera variable debe usar todos los caracteres en minúsculas con un guión bajo (_) como separador de palabras. La segunda variable debe usar todos los caracteres en mayúsculas con guión bajo como separador de palabras. La tercera variable debe usar números, letras y guiones bajos, pero aún así ser un nombre de variable Python válido.

Haga que las tres variables sean cadenas que se refieran a direcciones IPv6.

Use la técnica del futuro para que cualquier literal de cadena en Python2 sea unicode.

comparar si variable1 es igual a variable2
comparar si variable1 no es igual a variable3

4. Cree una variable show_version que contenga lo siguiente

 mostrar_versión = "*0 CISCO881-SEC-K9 FTX0000038X"

Elimine todos los espacios en blanco iniciales y finales de la cadena.

Divida la cadena y extraiga el modelo y el número de serie de ella.

Compruebe si 'Cisco' está contenido en la cadena del modelo (ignore las mayúsculas).

Compruebe si '881' está en la cadena del modelo.

Imprime tanto el número de serie como el modelo.

5. Tiene las siguientes tres variables de la tabla arp de un enrutador:

mac1 = "Internet 10.220.88.29 94 5254.abbe.5b7b ARPA FastEthernet4"
mac2 = "Internet 10.220.88.30 3 5254.ab71.e119 ARPA FastEthernet4"
mac3 = "Internet 10.220.88.32 231 5254.abc7.26aa ARPA FastEthernet4"

Procese estas entradas ARP e imprima una tabla de asignaciones de "DIRECCIÓN IP" a "DIRECCIÓN MAC". La salida debería tener el siguiente aspecto:

             DIRECCIÓN IP DIRECCIÓN MAC
-------------------- --------------------
        10.220.88.29 5254.abbe.5b7b
        10.220.88.30 5254.ab71.e119
        10.220.88.32 5254.abc7.26aa

Dos columnas, 20 caracteres de ancho, datos alineados a la derecha, una columna de encabezado.
 


ESQUEMA DE LA CLASE

1. Introducción (VÍDEO1)
   A. Propósito del curso [0:11]
   B. ¿Para quién es esta serie de videos? [0:33]
   C. Acerca de mí [2:51]
   D. Logística del curso [3:29]
   E. Aplica lo que aprendes [4:23]
   F. Contexto para los ejercicios [4:49]

2. ¿Por qué aprender a programar? (VÍDEO2)
   A. La programación como una habilidad poderosa [0:10]
   B. Todavía es necesario conservar las habilidades básicas de ingeniería [0:20]
   C. La automatización es una tendencia importante en nuestra industria [0:30]
   D. Gama de posibles habilidades de programación [0:54]

3. ¿Por qué Python? (VÍDEO3)
   A. Comunidad grande y activa [0:20]
      1. Bibliotecas
      2. Recursos de aprendizaje
      3. Personas a las que puedes hacerles preguntas
   B. Lenguaje de alto nivel [1:29]
   C. Ampliamente disponible en los sistemas [1:53]
   D. Legibilidad [2:05]
   E. Admite desde principiantes hasta programadores avanzados [2:33]

4. ¿Python2 versus Python3? (VÍDEO4)
   A. ¿Qué deben hacer los ingenieros de redes (a partir de hoy)? [1:20]

5. Características de Python (VIDEO5)
   A. Los bloques de código se indican mediante sangría [0:13]
   B. Convenciones de Python [2:02]
      1. Siga las convenciones de Python (PEP8) [2:12]
   C. ¿Cómo es Python como lenguaje? [3:20]
   D. Lenguaje de alto nivel [3:58]
      1. Variables tipadas dinámicamente [4:12]

6. El shell del intérprete de Python VIDEO6)
   A. Inicie el shell del intérprete [0:05]
   B. Ejecutar Python 3.6.2 [0:33]
   C. Creando una variable [1:00]
      1. Convenciones de nomenclatura de variables [1:17]
   D. Usando tipo [1:43]
   E. Caracteres permitidos en nombres de variables [2:08]
      1. Mayúsculas / minúsculas / números [2:23]
      2. No puede comenzar con un número [2:36]
      3. Puede comenzar con un guión bajo [2:47]
   F. Evaluación automática de expresiones [3:42]
   G. Primer programa en Python [4:15]
   H. Impresión a salida estándar [5:21]
   I. Hacer que el programa sea ejecutable a nivel del sistema [6:22]
   J. Edición y Editores (para crear programas en Python) [8:30]
   K. IDE [8:53]

7. IPython (VIDEO7)
   A. Lanzamiento de IPython [0:13]
      1. Mejor formato [0:47]
      2. Búfer de historial / historial mejorado [1:13]
      3. Finalización del comando [1:40]
   B. Instalación de IPython [2:30]
      C. Más sobre nombres de variables [3:00]
      D. Comentarios [3:28]

8. Impresión a stdout / Lectura desde stdin (VIDEO8)
   A. imprimir() en Python3 [0:14]
      1. Diferencias en Python2 [1:00]
      2. Escribir código compatible con PY2 y PY3 [1:41]
   B. Python3 leyendo desde stdin (entrada) [2:43]
      1. Diferencias en Python2 [3:31]
      2. Escribir código compatible con PY2 y PY3 [4:18]
  
9. Directorio, Ayuda y Variables (VIDEO9)
   A. Usar dir() [0:24]
   B. Métodos de llamada frente a métodos de referencia [0:55]
      1. Ejemplos llamando a varios métodos de cadena [2:16]
      2. Métodos de encadenamiento [2:39]
   C. Usar ayuda() [3:34]
   D. Operador de asignación [5:44]
   E. Variables como referencias a objetos [6:10]
      1. Usando id() [6:16]
      2. Dos nombres que se refieren a la misma cosa [7:17]
      3. Reasignar un nombre a un objeto diferente [8:40]

10. Cuerdas (Parte 1) (VIDEO10)
    A. Diferencia fundamental entre Python2 y Python3 [0:30]
    B. String en Python2 es una cadena ASCII [1:10]
    C. String en Python3 es una cadena Unicode [1:59]
    D. Cómo escribir cadenas Unicode en Python2 [2:08]
    E. Cómo escribir cadenas de bytes en Python3 [3:23]
    F. Técnica para hacer que todos los literales de cadenas sean unicode [3:46]

11. Cuerdas (Parte 2) (VIDEO11)
    A. Operadores de comparación [0:30]
    B. Subcadena en una cadena más amplia [2:16]
    C. Índices de cadenas [3:51]
    D. función len() [4:50]
    E. Concatenación de cadenas [5:14]
    F. Representaciones binarias y hexadecimales de cadenas [6:43]

12. Cuerdas (Parte 3) (VIDEO12)
    A. Cuerdas sin procesar [1:04]
    B. Asignación de cadenas (comillas simples, dobles y triples) [1:44]
    C. repr() de una cadena [3:32]
    D. Métodos de cadena [4:21]
       1. tira() [4:34]
       2. dividir() [6:04]
       3. Líneas divididas() [9:15]

13. Formato de cadena (Parte 1) (VIDEO13)
    A. Replicar una cadena [1:12]
    B. Método de formato [1:35]
       1. Llamar con argumentos posicionales [2:00]
       2. Especificación del ancho del campo [2:59]
       3. Alineado a la derecha, centrado [3:21]
       4. Usar argumentos con nombre [6:20]
       5. Usar *args para pasar una lista [10:50]

14. Formateo de cadenas (Parte 2) (VIDEO14)
    A. Usando el operador de formato (%) [0:25]
    B. Cuerdas F [1:41]
    

[PyNet Learning Python] - Lección 2 / Números, archivos, listas y linters

David

Nota: hay una tabla de contenido para cada video en la parte inferior de este correo electrónico, incluidas las marcas de tiempo de la ubicación de varios contenidos. Esto debería ser útil para navegar por los videos.

En este correo electrónico de Learning Python vamos a cubrir lo siguiente:

Numbers
Video https://vimeo.com/244128549
Length is 9 minutes
 
Files
Video https://vimeo.com/244127459
Length is 10 minutes
 
Lists
Video https://vimeo.com/244257596
Length is 6 minutes
 
List Slices
Video https://vimeo.com/244259492
Length is 4 minutes  
 
Lists are Mutable
Video https://vimeo.com/244287000
Length is 5 minutes
 
Tuples
Video https://vimeo.com/244153105
Length is 3 minutes
 
Using .join()
​Video https://vimeo.com/245464488
Length is 3 minutes
 
sys.argv
Video https://vimeo.com/245464766
Length is 2 minutes
 
Linters
Video https://vimeo.com/245102246
Length is 6 minutes

Additional Content:

Automate the Boring Stuff with Python (Chapter 4 on Strings)
Up through the section named "Removing Values from Lists with del Statements"


Dive Into Python, Lists

Exercises
Reference code for these exercises is posted on GitHub at:
https://github.com/ktbyers/pynet/tree/master/learning_python/lesson2


1. Open the "show_version.txt" file for reading. Use the .read() method to read in the entire file contents to a variable. Print out the file contents to the screen. Also print out the type of the variable (you should have a string at this point).

Close the file.

Open the file a second time using a Python context manager (with statement). Read in the file contents using the .readlines() method. Print out the file contents to the screen. Also print out the type of the variable (you should have a list at this point).


2. Create a list of five IP addresses.

Use the .append() method to add an IP address onto the end of the list. Use the .extend() method to add two more IP addresses to the end of the list.

Use list concatenation to add two more IP addresses to the end of the list.

Print out the entire list of ip addresses. Print out the first IP address in the list. Print out the last IP address in the list.

Using the .pop() method to remove the first IP address in the list and the last IP address in the list.

Update the new first IP address in the list to be '2.2.2.2'. Print out the new first IP address in the list.


3. Read in the "show_arp.txt" file using the readlines() method. Use a list slice to remove the header line.

Use pretty print to print out the resulting list to the screen, syntax is:
from pprint import pprint
pprint(some_var)

Use the list .sort() method to sort the list based on IP addresses.

Create a new list slice that is only the first three ARP entries.

Use the .join() method to join these first three ARP entries back together as a single string using the newline character ('\n') as the separator.

Write this string containing the three ARP entries out to a file named "arp_entries.txt".


4. Read in the "show_ip_int_brief.txt" file into your program using the .readlines() method.

Obtain the list entry associated with the FastEthernet4 interface. You can just hard-code the index at this point since we haven't covered for-loops or regular expressions. Use the string .split() method to obtain both the IP address and the corresponding interface associated with the IP.

Create a two element tuple from the result (intf_name, ip_address).

Print that tuple to the screen.

Use pycodestyle on this script. Get the warnings/errors to zero. You might need to 'pip install pycodestyle' on your computer (you should be able to type this from the shell prompt). Alternatively, you can type 'python -m pip install pycodestyle'.


5. Read the 'show_ip_bgp_summ.txt' file into your program. From this BGP output obtain the first and last lines of the output.

From the first line use the string .split() method to obtain the local AS number.

From the last line use the string .split() method to obtain the BGP peer IP address.

Print both local AS number and the BGP peer IP address to the screen.


CLASS OUTLINE

1. Numbers (VIDEO1)
   A. Creating an integer type  [0:10]
   B. Arithmetic Operators [0:23]
      I. Modulo Operator [0:59]
      II. Raise to the power [1:19]
      III. Division behavior and Python2 [1:31]
         a. from __future__ import division [2:44]
      IV. Whitespace in Python [3:32]
   C. Type float [4:00]
   D. Type casting an integer to a float [4:50]
   E. Strange math behavior of .1 + .2 [5:53]
   F. Increment by one [8:00]
 
2. Files (VIDEO2)
   A. Open a file for reading [0:26]
      I. f.read() [0:58]
      II. f.seek(0) [1:43]
      III. f.close() [2:22]
   B. f.readline() [3:23]
   C. f.readlines() [3:56]
   D. Context manager [5:04]
      I. Automatic close [5:56]
   E. Writing a file [6:30]
      I. f.flush() [7:30]
      II. Destructive operation [7:43]
   F. Append a file [8:12]
 
3. Lists (VIDEO3)
   A. Data that is inherently sequential [0:06]
   B. Examples [0:19]
   C. Creating a list [0:56]
      I. Creating a list with existing values [1:16]
      II. Lists can store different types of data [1:39]
      III. Accessing element 0, 1, 2, 3 [1:56]
      IV. Changing the value of an element [2:23]
   D. List methods [2:53]
      I. append() [2:57]
      II. list concatenation [3:13]
      III. list.extend() [3:48]
      IV. removing elements [4:14]
         a. my_list.pop() [4:22]
         b. my_list.pop(0) [4:37]
         c. del my_list[0] [4:58]
 
4. List slices (VIDEO4)
   A. Read from show_version.txt [0:12]
   B. Creating new lists from an existing list [0:47]
   C. First index is included [1:07]
   D. Last index is excluded [1:14]
   E. First number is excluded (go to beginning) [1:39]
   F. Last number is excluded (go to end) [2:02]
   G. Can use negative indices [3:21]
 
5. Lists are Mutable (VIDEO5)
   A. What does mutable mean [0:14]
   B. Mutable data types (lists, dictionaries) [2:13]
   C. Immutable data types (strings, numbers) [3:03]
   D. Be careful with copying lists [4:48]
 
6. Tuples (VIDEO6)
   A. Use parenthesis and not brackets [0:19]
   B. Why use tuples? [0:34]
   C. Behaves like a list, but can't modify it [0:48]
   D. Tuples use less memory [2:07]
   E. Type cast as a list [2:21]
 
7. Using .join() (VIDEO7)
   A. Review of using .split()   [0:11]
      I. Split returns a list   [0:34]
   B. .join() reunites the parts   [0:59]
      I. String separator, pass in a list   [1:06]
      II. Separator between each element   [1:30] 
      III. .join() is a string method   [1:35]
   C. Example using an IP address   [2:26]

8. sys.argv (VIDEO8)
   A. Behavior of sys.argv   [0:25]
      I. Returns a list, element1 is the program name   [0:31]
      II. Additional args are remaining elements   [0:54]

9. Linters (VIDEO9)
   A. Advantages of using linters [0:04]
      I. Improve readability [0:23]
      II. Flag obvious errors and save debugging time [0:40]
      III. Flag potential problems [0:50]
   B. Two most common linters: pylint and pycodestyle [1:01]
      I. Installing pylint and pycodestyle linters [1:20]
      II. Example using pylint and pycodestyle [1:35]
      III. Example using pylint and pycodestyle [2:08]
   C. Using pylama and a setup.cfg file [3:35]
   D. You decide what characteristics matters [4:07]
   E. Zero errors [5:03]
   F. Integrate with CI [5:16]


Lesson3 / Conditionals and Loops

Nota: hay una tabla de contenido para cada video en la parte inferior de este correo electrónico, incluidas las marcas de tiempo de la ubicación de varios contenidos. Esto debería ser útil para navegar por los videos.

En este correo electrónico de Learning Python vamos a cubrir lo siguiente

Condicionales
Vídeo https://vimeo.com/245104620
 
Lógica booleana (booleanos, operador ternario, ninguno)
Vídeo https://vimeo.com/245112558

Python para bucles
Vídeo https://vimeo.com/245466297

Para bucles (enumerar)
Vídeo https://vimeo.com/245477015

For Loops (Break and Continue)
Vídeo https://vimeo.com/245478016

Mientras bucles
Vídeo https://vimeo.com/245545155

Bucles varios
Vídeo https://vimeo.com/245552604

Additional Content:

How To Write Conditional Statements in Python 3
https://www.digitalocean.com/community/tutorials/how-to-write-conditional-statements-in-python-3-2?__s=3ni96cruswv2a37bmlax
How To Construct For Loops in Python 3
https://www.digitalocean.com/community/tutorials/how-to-construct-for-loops-in-python-3?__s=3ni96cruswv2a37bmlax
How To Construct While Loops in Python
https://www.digitalocean.com/community/tutorials/how-to-construct-while-loops-in-python-3?__s=3ni96cruswv2a37bmlax

Ejercicios

El código de referencia para estos ejercicios está publicado en GitHub en:
    https://github.com/ktbyers/pynet/tree/master/learning_python/lesson3


1. Lea el archivo "show_vlan.txt" en su programa. Recorra las líneas de este archivo y extraiga todas las combinaciones de VLAN_ID, VLAN_NAME. A partir de estos VLAN_ID y VLAN_NAME, construya una nueva lista en la que cada elemento de la lista sea una tupla que consta de (VLAN_ID, VLAN_NAME). Imprima esta estructura de datos en la pantalla. Su salida debe tener el siguiente aspecto:
[('1', 'predeterminado'),
 ('400', 'azul400'),
 ('401', 'azul401'),
 ('402', 'azul402'),
 ('403', 'azul403')]

2. Lea el contenido del archivo "show_arp.txt". Usando un ciclo for, itere sobre las líneas de este archivo. Procese las líneas del archivo y separe ip_addr y mac_addr para cada entrada en una variable separada.

Agregue una declaración condicional que busque '10.220.88.1'. Si se encuentra 10.220.88.1, imprima la cadena "IP/Mac de puerta de enlace predeterminada" y la dirección IP y la dirección MAC correspondientes.

Usando una declaración condicional, busque también '10.220.88.30'. Si se encuentra esta dirección IP, imprima "Arista3 IP/Mac is" y las correspondientes ip_addr y mac_addr.

Realice un seguimiento de si ha encontrado tanto la puerta de enlace predeterminada como el conmutador Arista3. Una vez que haya encontrado ambos dispositivos, 'salga' del bucle for.


3. Lea el archivo 'show_lldp_neighbors_detail.txt'. Recorra las líneas de este archivo. Siga leyendo las líneas hasta que haya encontrado el "Nombre del sistema" remoto y la "Id. de puerto" remota. Guarde estos dos elementos en variables e imprímalos en la pantalla. Debe extraer solo el nombre del sistema y la identificación del puerto de las líneas (es decir, sus variables solo deben tener 'twb-sf-hpsw1' y '15'). Salga de su bucle una vez que haya recuperado estos dos elementos.


4. Tiene la siguiente estructura de datos:
tabla_arp = [('10.220.88.1', '0062.ec29.70fe'),
 ('10.220.88.20', 'c89c.1dea.0eb6'),
 ('10.220.88.21', '1c6a.7aaf.576c'),
 ('10.220.88.28', '5254.aba8.9aea'),
 ('10.220.88.29', '5254.abbe.5b7b'),
 ('10.220.88.30', '5254.ab71.e119'),
 ('10.220.88.32', '5254.abc7.26aa'),
 ('10.220.88.33', '5254.ab3a.8d26'),
 ('10.220.88.35', '5254.abfb.af12'),
 ('10.220.88.37', '0001.00ff.0001'),
 ('10.220.88.38', '0002.00ff.0001'),
 ('10.220.88.39', '6464.9be8.08c8'),
 ('10.220.88.40', '001c.c4bf.826a'),
 ('10.220.88.41', '001b.7873.5634')]

Recorra esta estructura de datos y extraiga todas las direcciones MAC. Procese todas las direcciones MAC para obtener un formato estándar. Imprima toda la nueva dirección MAC estandarizada en la pantalla. El formato estandarizado debe ser el siguiente:

00:62:EC:29:70:FE

Los dígitos hexadecimales deben estar en mayúscula. Además, debe haber dos puntos entre cada octeto en la dirección MAC.


5. [Opcional/bonificación]

*** Tenga en cuenta que para probar esto en su entorno, cambie las direcciones IP de prueba a algo en su entorno que pueda hacer ping con éxito. ***

Construya una lista de 254 direcciones IP. La dirección IP base debe ser igual a '10.10.100.0' o '10.10.100.'.

Debe usar el 'rango' incorporado para lograr esto.

Su lista debe tener todas las direcciones IP de 10.10.100.1 a 10.10.100.254.

Use la 'enumeración' de Python para imprimir todas las direcciones IP y su índice de lista correspondiente. La salida debe ser similar a la siguiente:
0 ---> 10.10.100.1
1 ---> 10.10.100.2
2 ---> 10.10.100.3
3 ---> 10.10.100.4
4 ---> 10.10.100.5
...

Use un segmento de lista para crear una nueva lista que vaya de 10.10.100.3 a 10.10.100.6.

Usando un bucle y os.system("ping -c 3 10.10.100.3") intente hacer ping a todas las direcciones IP en esta breve lista. Para Windows, el comando probablemente sea os.system("ping -n 3 10.10.100.3").

Coloque una variable en la parte superior para definir si está utilizando Windows o Linux/MacOs. Esto debería ser similar a lo siguiente:
VENTANAS = Falso

base_cmd_linux = 'ping -c 2'
base_cmd_windows = 'ping -n 2'
# operador ternario
base_cmd = base_cmd_windows si WINDOWS si no base_cmd_linux






ESQUEMA DE LA CLASE
 

1. Condicionales (VIDEO1)
   A. Estructura de los condicionales de Python [0:10]
   B. ¿Qué es una expresión en Python [1:54]
   C. Ejemplo de declaración if [2:47]
   D. Ejemplo de declaración if usando una variable [3:35]
   E. Ejemplo de declaración if/else [5:08]
   F. Ejemplo de declaración if/elif/else [5:43]

2. Lógica Booleana (Booleanos, Operador Ternario, Ninguno) (VIDEO2)
   A. Lógica booleana
      1. Verdadero y verdadero (lógico y) [0:41]
      2. Verdadero o Falso (lógico o) [1:06]
      3. no es cierto [1:17]
   B. Construir expresiones más complejas [1:27]
   C. Conversión de otros tipos de datos para que sean booleanos [2:24]
   D. Cómo evalúa Python otros tipos de datos [2:39]
   E. Encasillamiento con bool [4:10]
   F. Operador ternario de Python [5:00]
   G. Ninguno [7:22]
      1. Valor de retorno predeterminado para las funciones de Python [7:46]

3. Python para bucles (VIDEO3)
   A. Significado general de los bucles [0:03]
   B. Significado de bucles for [0:29]
      1. Ejemplo de bucle [1:25]

4. For Loops (Enumerar) (VIDEO4)
   A. Valor del loop-vari
