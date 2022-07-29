# PyNet
[PyNet Learning Python] - Introduction
Getting Python Installed

You will need a system that has either Python3.x on it (with a strong preference for Python3.6 or newer).

MacOS
If you want to use Python3 on MacOS, then I recommend following the process specified here (up to the point where you can execute 'python3').

http://docs.python-guide.org/en/latest/starting/install3/osx/

Linux
Just type 'python3' from the shell and verify your system has Python3.X installed. If that doesn't work, type 'python' and verify the version is Python 2.7. If Python3 is not installed (and you want to use Python3), then it should be pretty easy to get it installed for most major versions of Linux (as long as you are using a reasonably up to date version of the operating system).

For Fedora-based systems, I did the following:
yum install python36 python36-devel python36-setuptools python36-virtualenv

For Ubuntu, python3 should be installed at least as of Ubuntu 16.04.

Windows
If you are running on Windows, then use the below link to install Python3:

https://www.python.org/downloads/windows/

Then select the "Latest Python3 Release". On this next page, the 'Windows x86 executable installer' is probably the right choice in most cases.

You might also want to update your Windows system Path so that your computer knows how to find the Python interpreter.  
-------------------------------------------------------------------------------------- 

Lecciones de Python aplicado a Ingeniería de Redes

Lecciones de Kirk Byers

Nota1: hay una tabla de contenido para cada video en la parte inferior de este correo electrónico, incluidas las marcas de tiempo de la ubicación de varios contenidos. Esto debería ser útil para navegar por los videos.

Nota 2: debe centrarse fundamentalmente en Python3 en este momento y debe migrar activamente cualquier código Python2 heredado a Python3. El soporte de Python2 finalizó (de los desarrolladores principales de Python) el 1 de enero de 2020.

SECCION 001

En este sección de Learning Python vamos a cubrir lo siguiente:
 
1.Introducción 

Vídeo https://vimeo.com/243034300
La duración es de 7 minutos.
 

2.¿Por qué aprender programación?
Vídeo https://vimeo.com/243905715
(1 minuto)
 

3.¿Por qué Python?
Vídeo https://vimeo.com/243909371
(3 minutos)
 

4.Python2 frente a Python3
Vídeo https://vimeo.com/243912631
(2 minutos)
 

5.Características de Python
Vídeo https://vimeo.com/243918300
(5 minutos)
 

6.El shell del intérprete de Python
Vídeo https://vimeo.com/242411259
(9 minutos)
 

7.IPython
Vídeo https://vimeo.com/242460561
(4 minutos)
 

8.Imprimiendo a stdout y leyendo desde stdin
Vídeo https://vimeo.com/243028886
(6 minutos)
 

9.Dir, Ayuda y Variables
Vídeo https://vimeo.com/243480156
(10 minutos)
 

10.Cuerdas de Python (Parte 1)
Vídeo https://vimeo.com/243481392
(6 minutos)
 

11.Cuerdas de Python (Parte 2)
Vídeo https://vimeo.com/243482081
(8 minutos)
 

12.Cuerdas de Python (Parte 3)
Vídeo https://vimeo.com/243482871
(10 minutos)
 

13.Formato de cadenas de Python (Parte 1)
Vídeo https://vimeo.com/243936489
(12 minutos)
 

14.Formato de cadena de Python (Parte 2)
Vídeo https://vimeo.com/243956669
(4 minutos)

-------------------------------------------- 
Additional Content:

Google Python Course on Strings
https://developers.google.com/edu/python/strings?__s=3ni96cruswv2a37bmlax

Automate the Boring Stuff with Python (Chapter 6 on Strings)   
https://automatetheboringstuff.com/chapter6/?__s=3ni96cruswv2a37bmlax

--------------------- 
1. Python naming conventions:

    a. For variable names, function names, object names, and module names use lower case separated by underscore, for example:

      my_router
      find_set_of_devices
      convert_id_string_to_list

    b. For class names, capitalize the first letter of each word.  Do not use any underscores.  For example:

      ManyToManyField
      ClientHistory
      UserProfile﻿﻿﻿

    c. For constants, use all upper case; use underscores for word separation.

      PI = 3.14
      EMAIL_MODE
      EMAIL_FROM_ADDRESS


Exercises

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

Number
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
https://automatetheboringstuff.com/chapter4/?__s=3ni96cruswv2a37bmlax


Dive Into Python, Lists
https://diveinto.org/python3/native-datatypes.html?__s=3ni96cruswv2a37bmlax#lists


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

5. For Loops (Break and Continue) (VIDEO5)  
   A. Other ways to exit the for loop   [0:24]
      1. break   [0:30]
      2. continue   [1:47]  
   B. pass as a no-op   [3:24]
   C. Nesting for loops   [4:12]
   D. The interable does not need to be a list   [6:22]
      1. It can be a tuple   
      2. It can be a dictionary   
      3. It can be a string   
   E. Range    [7:09]
   F. Using 'in' for list membership   [8:57]

6. While Loops (VIDEO6)
   A. Format of a while loop   [0:09]
   B. Exit from a while loop [0:39]
   C. Example of a while loop   [1:09]
   D. Infinite loop   [2:45]

7. Loops Miscellaneous (VIDEO7)
   A. Meaning of else   [1:04]
   B. use variables instead of indices for readability   [3:00]
   C. while True:   [5:00]
      1. break is the only way out   [5:36]


[PyNet Learning Python] - Lesson4 / Dictionaries, Exceptions, and Regular Expressions
Note: There is a table of contents for each video at the bottom of this email including timestamps to where various content is located. This should be helpful in navigating the videos.

Now  we are going to cover the following:

Dictionaries
Video https://vimeo.com/246157566
Length is 6 minutes 
 
Dictionary Methods
Video https://vimeo.com/246163031
Length is 7 minutes 
 
Sets
Video https://vimeo.com/246167477
Length is 9 minutes  
 
Exceptions
Video https://vimeo.com/246174686
Length is 15 minutes
 
Regular Expressions (Part1)
Video https://vimeo.com/246184715
Length is 15 minutes
 
Regular Expressions (Part2)
Video https://vimeo.com/246532117
Length is 7 minutes
 
Regular Expressions (Part3)
Video https://vimeo.com/246534450
Length is 8 minutes
 
Regular Expressions, Other Methods
Video https://vimeo.com/246535038
Length is 4 minutes


Additional Content:

Regular Expression Tutorial
This is a good resource if you are new to regular expressions.
https://regexone.com/lesson/introduction_abcs?__s=3ni96cruswv2a37bmlax

Online Regular Expression Tester
Select 'Python' on the left-hand side.
https://regex101.com/?__s=3ni96cruswv2a37bmlax

Python Regular Expression HowTo
This is a good overview of regular expression special characters.
Start at the very top of the page and read through the 'Repeating Things' section.
https://docs.python.org/2/howto/regex.html?__s=3ni96cruswv2a37bmlax

Automate the Boring Stuff - Dictionaries and Structuring Data​
Read through the 'The GET() Method' section.
https://automatetheboringstuff.com/chapter5/?__s=3ni96cruswv2a37bmlax

Exercises

Reference code for these exercises is posted on GitHub at:
    https://github.com/ktbyers/pynet/tree/master/learning_python/lesson4


1. Create a dictionary representing a network device. The dictionary should have key-value pairs representing the 'ip_addr', 'vendor', 'username', and 'password' fields.

Print out the 'ip_addr' key from the dictionary.

If the 'vendor' key is 'cisco', then set the 'platform' to 'ios'. If the 'vendor' key is 'juniper', then set the 'platform' to 'junos'.

Create a second dictionary named 'bgp_fields'. The 'bgp_fields' dictionary should have a keys for 'bgp_as', 'peer_as', and 'peer_ip'.

Using the .update() method add all of the 'bgp_fields' dictionary key-value pairs to the network device dictionary.

Using a for-loop, iterate over the dictionary and print out all of the dictionary keys.

Using a single for-loop, iterate over the dictionary and print out all of the dictionary keys and values.


2. Create three separate lists of IP addresses. The first list should be the IP addresses of the Houston data center routers, and it should have over ten RFC1918 IP addresses in it (including some duplicate IP addresses).

The second list should be the IP addresses of the Atlanta data center routers, and it should have at least eight RFC1918 IP addresses (including some addresses that overlap with the Houston data center).

The third list should be the IP addresses of the Chicago data center routers, and it should have at least eight RFC1918 IP addresses. The Chicago IP addresses should have some overlap with both the IP addresses in Houston and Atlanta.

Convert each of these three lists to a set.

Using a set operation, find the IP addresses that are duplicated between Houston and Atlanta.

Using set operations, find the IP addresses that are duplicated in all three sites.

Using set operations, find the IP addresses that are entirely unique in Chicago.


3.  Read in the 'show_version.txt' file. From this file, use regular expressions to extract the OS version, serial number, and configuration register values.

Your output should look as follows:
OS Version: 15.4(2)T1      
Serial Number: FTX0000038X    
​Config Register: 0x2102 

​4.  Using a named regular expression (?P<name>), extract the model from the below string:
show_version = '''
Cisco 881 (MPC8300) processor (revision 1.0) with 236544K/25600K bytes of memory.
Processor board ID FTX0000038X

5 FastEthernet interfaces
1 Virtual Private Network (VPN) Module
256K bytes of non-volatile configuration memory.
126000K bytes of ATA CompactFlash (Read/Write)
'''
Note that, in this example, '881' is the relevant model. Your regular expression should not, however, include '881' in its search pattern since this number changes across devices.

Using a named regular expression, also extract the '236544K/25600K' memory string.

Once again, none of the actual digits of the memory on this device should be used in the regular expression search pattern.

Print both the model number and the memory string to the screen.


5. Read the 'show_ipv6_intf.txt' file.

From this file, use Python regular expressions to extract the two IPv6 addresses.

The two relevant IPv6 addresses you need to extract are:
    2001:11:2233::a1/24
    2001:cc11:22bb:0:2ec2:60ff:fe4f:feb2/64

Try to use re.DOTALL flag as part of your search. Your search pattern should not include any of the literal characters in the IPv6 address.

From this, create a list of IPv6 addresses that includes only the above two addresses.

Print this list to the screen.


CLASS OUTLINE
1. Dictionaries (VIDEO1)
   A. What is a dictionary?   [0:03]
   B. Why do we need dictionaries?   [0:40]
   C. How to create a dictionary   [1:33]
   D. Adding keys to a dictionary   [1:58]
   E. Using variables as keys   [2:52]
   F. Accessing keys in a dictionary   [4:00]
   G. Accessing keys that don’t exist   [4:32]
   H. Dictionaries are mutable   [5:05]

2. Dictionary Methods (VIDEO2)
   A. get() method   [0:34]
   B. copy() method   [2:23]
   C. pop() method for key removal   [3:01]
   D. update() method   [3:49]
   E. Looping over dictionaries   [5:04]
   F. Using .values()   [5:32]
   G. Using .items()   [6:01]

3. Sets (VIDEO3)
   A. What is a set?   [0:04]
      1. Each element has to be unique   
      2. Sets are unordered   
      3. No indices   
   B. Looping over a set   [2:00]
   C. Set operations   [2:23]
      1. Union   [2:39]
      2. Intersection   [3:33]
      3. Difference   [4:11]
      4. Symmetric diff   [5:53]

4. Exceptions (VIDEO4)
   A. Example exception   [0:19]
   B. Non-zero exit status   [2:22]
   C. Using try/except   [2:38]
   D. Catching an exception and re-raising   [6:33]
   F. Catching an exception and printing   [8:22]
   G. Catching multiple exceptions   [9:34]
   H. Adding a finally clause   [12:00]

5. Regular Expressions (Part1) (VIDEO5)
   A. Why we need regex?   [0:05]
   B. Some special characters   [1:24]
      1. Any single character: . [1:33]
      2. One or more times: +   [4:54]
      3. Zero or more times: *   [5:56]
      4. Beginning of line: ^   [6:37]
      5. End of line: $   [6:55]
      6. Digit character class: \d   [7:30]
      7. Whitespace character class: \s   [9:29]
      8. Non-whitespace: \S   [10:20]
      9. Construct your own character class: []   [11:11]
      10. Parenthesis to save things: ()   [12:23]
   C. By default will be greedy.   [5:35]

6. Regular Expressions (Part2) (VIDEO6)
   A. Why you always use raw strings   [0:04]
   B. Using re.search()   [1:21]
      1. Arguments   [2:06]
      2. If successful, match object   [2:30] 
         a. match.group(0)   [2:34]
         b. match.group(1)   [3:48]
   C. Constructing named patterns   [4:55]
      1. match.groupdict()   [5:55]

7. Regular Expressions (Part3) (VIDEO7)
   A. Disabling greedy behavior   [0:31]
   B. Flags to re.search   [3:02]
      1. re.M  [4:58]
      2. re.DOTALL   [6:50]
      3. re.I   [7:41]

8. Regular Expressions, Other Methods (VIDEO8)
   A. re.split()   [0:14]
   B. re.sub()   [1:48]
   C. re.findall()   [3:38]
 
 
[PyNet] - Netmiko4: send_command_timing

This article was originally published on June 30th, 2022.

This article is part of my periodic mailings on Python and Network Automation. In these articles, I try to provide information that is useful to network engineers who are automating tasks in their environment. Note, this content is not directly a part of the Learning Python course.

![image](https://user-images.githubusercontent.com/31605766/177573235-ab7a1f16-aad7-4257-b9bb-1fe1c59702e7.png)

 
Netmiko has two fundamental ways for gathering show output: send_command() and send_command_timing().
send_command() is an entirely pattern-based solution—it looks for the expect_string that you specify or alternatively it looks for the trailing prompt. I discussed Netmiko4 and send_command here.

send_command_timing() on the other hand is an entirely timing based solution. It does not look for nor care about any pattern in the output. It basically tries to intelligently guess whether the device is done outputting.

While send_command() is the more valuable of the two methods, there are cases where having a timing based solution is valuable.

For example:

with ConnectHandler(**device) as conn:
    data = ""
    commands = [
        "ping", 
        "\n", 
        "8.8.8.8", 
        "\n", 
        "\n", 
        "\n", 
        "\n", 
        "\n"
    ]
    for cmd in commands:
        data += conn.send_command_timing(
            cmd, 
            strip_command=False,
            strip_prompt=False
        )
    print(data) 
 
Here we are doing an extended ping which prompts us for several things as part of the process.

If we used send_command(), we would need to specify an expect_string for each prompt. This would be tedious and it is probably easier just to use send_command_timing and a list of commands (as we did above).

Note, in Netmiko4, you can also use send_multiline or send_multiline_timing to handle this type of multiline prompting.

 

How does send_command_timing actually operate?
We can visualize the core of send_command_timing as follows:

![image](https://user-images.githubusercontent.com/31605766/177573697-cfbf2bf1-e672-4fb5-a821-bf14811fb15f.png)


PDF of Diagram: https://t.dripemail2.com/c/eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJkZXRvdXIiLCJpc3MiOiJtb25vbGl0aCIsInN1YiI6ImRldG91cl9saW5rIiwiaWF0IjoxNjU3MDk5ODU4LCJuYmYiOjE2NTcwOTk4NTgsImFjY291bnRfaWQiOiI0MjU0NDk3IiwiZGVsaXZlcnlfaWQiOiJmZjBqdXlqdmhjMHptaWJjNDFxbSIsInVybCI6Imh0dHBzOi8vcHluZXQudHdiLXRlY2guY29tL3N0YXRpYy9wZGYvc2VuZF9jb21tYW5kX3RpbWluZ19mbG93Y2hhcnQucGRmP19fcz0zbmk5NmNydXN3djJhMzdibWxheCJ9.XKhvPa_zay_ubvwsNvVNPzilmdoK3mMRIfh5_KVekj8

Looking at the diagram, we can see that send_command_timing first sends the command down the SSH channel and then starts a timer.

send_command_timing then enters its main loop where it is waiting for data from the device. As long as there is no data, Netmiko will keep looping and reading, with a 0.1 second sleep on each loop.

Eventually, if no data ever arrives, Netmiko will give up and raise a ReadTimeout. By default this timeout will occur in 120 seconds (this can be set using the 'read_timeout' argument).

Typically, however, when you send a command, there will be some output.

In this case, Netmiko will keep reading the data (as long as more data arrives every 0.1 seconds). Once Netmiko detects there is no more NEW data, and then it switches to last_read mode.

Once you are performing this last_read, Netmiko will sleep longer. Here Netmiko is trying to ensure that all available data has been read. Consequently, it waits a bit longer to ensure nothing new arrives.

You can control the length of this last_read time by setting the last_read argument. last_read defaults to two seconds.

Once Netmiko does this last read, it then checks if this last read is empty or not. If there is data (i.e. it is not empty), then Netmiko says "oooops" and returns back to the main reading loop. Basically, there is more output data to process so let's keep reading.

Ultimately Netmiko will keep repeating this process until either: 1) read_timeout expires, or 2) there is no new data on the last read. If there is no new data on the last read, Netmiko returns all the data previously read.

 
How can you modify send_command_timing's behavior?

There are three main ways that you can control the behavior of send_command_timing: 1) increase last_read, 2) modify read_timeout, 3) set read_timeout=0.

def send_command_timing(
    self,
    command_string: str,
    last_read: float = 2.0,
    read_timeout: float = 120.0
    # A bunch of other arguments
)

If you are running into cases where you are not capturing all the data you require, then you should increase the last_read time.

data = conn.send_command_timing(
    "ping 8.8.8.8",
    last_read=8.0
) 
Basically, some commands will have output gaps that are longer than the two second default. In these cases, you should set last_read to be longer than the longest gaps in the output. Determining this might require some trial-and-error.

The downside of increasing last_read is that it will meaningfully slowdown send_command_timing.

If, instead, you are executing a command that is continuously outputting data for a long period of time and you're running into the ReadTimeout exception, then you should increase read_timeout.

data = conn.send_command_timing(
    "show ip bgp",
    read_timeout=600
) 

Finally, if you never want Netmiko to cease reading due to a read_timeout, then you can set read_timeout=0. In this case, Netmiko will keep reading until last_read completes successfully.

data = conn.send_command_timing(
    "show ip bgp",
    read_timeout=0
) 

Regards,


[PyNet Learning Python] - Lesson5 / Functions and the Python Debugger

Note: There is a table of contents for each video at the bottom of this email including timestamps to where various content is located. This should be helpful in navigating the videos.

﻿In this email of Learning Python we are going to cover the following:
 
Functions (Part1)
Video link https://vimeo.com/247570174
Length is 8 minute
 
Functions (Part2)
Video link https://vimeo.com/247581011
Length is 11 minutes
 
Misc Topics (Part1)
Video link https://vimeo.com/247582360
Length is 10 minutes
 
Misc Topics (Part2)
Video link https://vimeo.com/247655574
Length is 8 minutes
 
Python Debugger (pdb)
Video link https://vimeo.com/247724017
Length is 10 minutes

Additional Content:

A Byte of Python, Functions
https://t.dripemail2.com/c/eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJkZXRvdXIiLCJpc3MiOiJtb25vbGl0aCIsInN1YiI6ImRldG91cl9saW5rIiwiaWF0IjoxNjU3NjE4MjI2LCJuYmYiOjE2NTc2MTgyMjYsImFjY291bnRfaWQiOiI0MjU0NDk3IiwiZGVsaXZlcnlfaWQiOiJpcjVhbGRhb2lyMGp0cms2OG1sMCIsInVybCI6Imh0dHBzOi8vcHl0aG9uLnN3YXJvb3BjaC5jb20vZnVuY3Rpb25zLmh0bWw_X19zPTNuaTk2Y3J1c3d2MmEzN2JtbGF4In0.6RLRhvC8snKphP8SPatKcjAHWB6B5OyGFYxm-sPM87o

How to use the Python Debugger
https://t.dripemail2.com/c/eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJkZXRvdXIiLCJpc3MiOiJtb25vbGl0aCIsInN1YiI6ImRldG91cl9saW5rIiwiaWF0IjoxNjU3NjE4MjI2LCJuYmYiOjE2NTc2MTgyMjYsImFjY291bnRfaWQiOiI0MjU0NDk3IiwiZGVsaXZlcnlfaWQiOiJpcjVhbGRhb2lyMGp0cms2OG1sMCIsInVybCI6Imh0dHBzOi8vd3d3LmRpZ2l0YWxvY2Vhbi5jb20vY29tbXVuaXR5L3R1dG9yaWFscy9ob3ctdG8tdXNlLXRoZS1weXRob24tZGVidWdnZXI_X19zPTNuaTk2Y3J1c3d2MmEzN2JtbGF4In0.w1uAwhLJFMXOyN7adZUth_LeFz1vkRLXt4fkzn2N_po

Exercises

Reference code for these exercises is posted on GitHub at:
    https://github.com/ktbyers/pynet/tree/master/learning_python/lesson5


1a. Create an ssh_conn function. This function should have three parameters: ip_addr, username, and password. The function should print out each of these three variables and clearly indicate which variable it is printing out.

Call this ssh_conn function using entirely positional arguments.

Call this ssh_conn function using entirely named arguments.

Call this ssh_conn function using a mix of positional and named arguments.


1b. Expand on the ssh_conn function from exercise1 except add a fourth parameter 'device_type' with a default value of 'cisco_ios'. Print all four of the function variables out as part of the function's execution.

Call the 'ssh_conn2' function both with and without specifying the device_type

Create a dictionary that maps to the function's parameters. Call this ssh_conn2 function using the **kwargs technique.


2.  Create a function that randomly generates an IP address for a network. The default base network should be '10.10.10.'. For simplicity the network will always be a /24.

You should be able to pass a different base network into your function as an argument.

Randomly pick a number between 1 and 254 for the last octet and return the full IP address.

You can use the following to randomly generate the last octet:
import random
random.randint(1, 254)

Call your function using no arguments.
Call your function using a positional argument.
Call your function using a named argument.

For each function call print the returned IP address to the screen.


3. Similar to lesson3, exercise4 write a function that normalizes a MAC address to the following format:

01:23:45:67:89:AB

This function should handle the lower-case to upper-case conversion.

It should also handle converting from '0000.aaaa.bbbb' and from '00-00-aa-aa-bb-bb' formats.

The function should have one parameter, the mac_address. It should return the normalized MAC address

Single digit bytes should be zero-padded to two digits. In other words, this:

a:b:c:d:e:f

should be converted to:

0A:0B:0C:0D:0E:0F

Write several test cases for your function and verify it is working properly.


4. Copy your solution from exercise3 to exercise4. Add an 'import pdb' and pdb.set_trace() statement outside of your function (i.e. where you have your function calls).

Inside of pdb, experiment with:
Listing your code.
Using 'next' and 'step' to walk through your code. Make sure you understand the difference between next and step.
Experiment with 'up' and 'down' to move up and down the code stack.
Use p <variable> to inspect a variable.
Set a breakpoint and run your code to the breakpoint.
Use '!command' to change a variable (for example !new_mac = [])


CLASS OUTLINE

1. Functions (Part1) (VIDEO1)
   A. How to define   [0:04]
   B. How to call   [0:35]
   C. Return values   [1:41]
   D. Adding positional arguments   [3:21]
   E. Adding named arguments   [4:54]
   F. Default values   [7:13]

2. Functions (Part2) (VIDEO2)
   A. Calling with *args   [1:57]
   B. Calling with **kwargs   [3:45]
   C. Passing mutables as function arguments   [4:49]
   D. Variables are local to the function   [7:59]

3. Misc Topics (Part1) (VIDEO3)
   A. Classes   [0:23]
      1. Why you might want to use classes   [0:43]
      2. Syntax for creating a class   [2:16]
   B. Modules   [5:15]
      1. What is a module   [5:38]
      2. Importing a module you have created   [5:54]
      3. Calling your imported function   [6:05]
      4. How Python finds something using sys.path   [6:40]
      5. Two ways to perform imports   [7:10]

4. Misc Topics (Part2) (VIDEO4)
   A. Packages   [0:41]
   B. List comprehensions   [1:55]
   C. Lambda functions   [4:47]

5. Python’s Debugger (PDB) (VIDEO5)
   A. The (Pdb) shell   [0:08]
   B. Listing lines using 'list'   [0:52]
   C. Using 'step (s)' to step through a program   [1:27]
   D. 'args' to look at arguments of a function   [1:56]
   E. 'p' to print variables   [2:01]
   F. 'pp' to pretty print   [2:10]
   G. 'up' to move up the stack   [2:27]
   H. 'down' to move down the stack   [2:56]
   I. execute until the return statement   [3:15]
   J. Executing using 'python -m pdb'   [4:10]
   K. Using 'next (n)'   [5:11]
   L. Difference between step and next   [5:56]
   N. Setting a breakpoint   [6:13]
   O. 'continue' to execute until the breakpoint   [6:24]
   P. Use '!<command>' to execute python code   [6:48]
   Q. Debugging principles   [7:54]
      1. Get information out of your program   [8:08]
      2. Quick feedback loop   [8:15]
      
   
[Pynet] - Netmiko4: ConnLogOnly


This article was originally published on July 7th, 2022.

 
This article is part of my periodic mailings on Python and Network Automation. In these articles, I try to provide information that is useful to network engineers who are automating tasks in their environment. Note, this content is not directly a part of the Learning Python course.

![image](https://user-images.githubusercontent.com/31605766/178773865-7d581c29-b9d1-4944-8acf-928e7c9bf9d3.png)

One pattern that Netmiko users frequently implement is a series of try/except statements to handle various errors that occur during the initial Netmiko connection.

 

try:
    conn = ConnectHandler(**device)
except NetmikoAuthenticationException:
    # do something / log failure
    return
except NetmikoTimeoutException:
    # do something / log failure
    return
except Exception:
    # Unknown exception: do something / log failure
    return

# The connection succeeded!
print(conn.find_prompt()) 

This pattern is so common that I created a new Netmiko factory function that replicates this boilerplate code.

This new Netmiko entry point is named ConnLogOnly.

import sys
from netmiko import ConnLogOnly

# device dictionary not shown
conn = ConnLogOnly(**device)
if conn is None:
    # Errors will be logged in 'netmiko.log'
    sys.exit("Logging in failed")

print(conn.find_prompt())
conn.disconnect() 

ConnLogOnly is a replacement for ConnectHandler and operates similarly. It takes all of the standard Netmiko connection arguments and returns a Netmiko object of the properly class with an established connection.

ConnLogOnly will automatically handle all connection exceptions (unlike ConnectHandler). In other words, you should never receive an unhandled connection exception when invoking ConnLogOnly().

Instead of receiving an exception, ConnLogOnly will either return: 1) a Netmiko connection object, or 2) None.

A value of None indicates that the connection failed.

Any exceptions that occurred during the connection process will be automatically logged. By default this will be to a file named "netmiko.log".

 

Okay, okay, would you just give me some examples already?
 
import sys
from netmiko import ConnLogOnly

device1 = {
    "host": "cisco3.domain.com",
    "username": "admin",
    "password": "cisco123",
    "device_type": "cisco_ios",
}

conn = ConnLogOnly(**device1)
if conn is None:
    sys.exit("Logging in failed")

print("\nWorking case:\n")
print(conn.find_prompt())
conn.disconnect() 

Executing this code yields:

$ python example.py 

Working case:

cisco3# 

In this case the connection worked, and we printed out the device's prompt.



But what happens when the connection fails?
Here we change our password to an invalid value and then re-execute our code.

$ cat example.py | grep password
    "password": "invalid",

$ python example.py
Logging in failed

$ echo $?
1 

We can see that our connection failed.

Now let's check the "netmiko.log" file.

$ date
Thu Jun 30 15:08:46 PDT 2022

# Yep, that file was just updated.
$ ls -ltr netmiko.log 
-rw-rw-r-- 1 ktbyers ktbyers 8788 Jun 30 15:07 netmiko.log

$ tail -25 netmiko.log 

# Only showing the last entry in the log file.
2022-06-30 15:07:11,203 ERROR netmiko.ssh_dispatcher 
Authentication failure to: cisco3.domain.com:22 (cisco_ios)

Authentication to device failed.

Common causes of this problem are:
1. Invalid username and password
2. Incorrect SSH-key file
3. Connecting to the wrong device

Device settings: cisco_ios cisco3.domain.com:22


Authentication failed.
We can see that our authentication failed and Netmiko provides us some details about the error.



What happens if we fail in a different way—let's try an invalid DNS name.
 

$ grep host example.py
    "host": "cisco3.bogus.com",

$ python example.py 
Logging in failed

$ date
Thu Jun 30 15:13:35 PDT 2022

$ ls -ltr netmiko.log 
-rw-rw-r-- 1 ktbyers ktbyers 9018 Jun 30 15:13 netmiko.log

$ tail netmiko.log 
# Only last log entry shown
2022-06-30 15:13:29,624 ERROR netmiko.ssh_dispatcher Device failed due to a 
DNS failure, hostname cisco3.bogus.com

Once again we can see that we failed to connect and that an error was logged to our "netmiko.log" file.



What are some other things we can configure using ConnLogOnly?
Using ConnLogOnly you can configure the log file name, specify the logging level, and specify the log file format.

Note, all of these arguments are optional.

def ConnLogOnly(
    log_file: str = "netmiko.log",
    log_level: Optional[int] = None,
    log_format: Optional[str] = None,
    **kwargs: Any,
) -> Optional["BaseConnection"]: 

Here we override the default log_file name:

conn = ConnLogOnly(log_file="my_file.txt", **device1)
if conn is None:
    sys.exit("Logging in failed")

And we can change the default logging level:

import logging
from netmiko import ConnLogOnly

device1 = { 
    "host": "cisco3.domain.com",
    "username": "admin",
    "password": "invalid",
    "device_type": "cisco_ios",
}

conn = ConnLogOnly(log_level=logging.DEBUG, **device1)
if conn is None:
    sys.exit("Logging in failed")




What outstanding issues are there with ConnLogOnly?
Currently, ConnLogOnly only allows you to specify your log file name, log level, or log formatting a single time in a given Python program. This issue is tracked here.

Additionally, ConnLogOnly does not support the use of a context manager. This also implies that you must explicitly call Netmiko's disconnect() method when you are done using your Netmiko connection object.


[PyNet Learning Python] - Lesson6 / Netmiko

Note: There is a table of contents for each video at the bottom of this email including timestamps to where various content is located. This should be helpful in navigating the videos.


﻿In this email of Learning Python we are going to cover the following:
 
Netmiko Introduction and Basics 
Video link https://vimeo.com/254569911
Length is 8 minutes
 
Netmiko Show Commands
Video link https://vimeo.com/254578980
Length is 13 minutes
 
Netmiko and Prompting
Video link https://vimeo.com/254587832
Length is 12 minutes
 
Netmiko and TextFSM
Video link https://vimeo.com/254611876
Length is 10 minutes
 
Netmiko Config Changes
Video link https://vimeo.com/254614073
Length is 8 minutes
 
Netmiko Troubleshooting
Video link https://vimeo.com/254786724
Length is 9 minutes


Additional Content:

Netmiko Readme

Netmiko Examples

Netmiko Tutorial
This tutorial is a bit old, but still should be generally correct.


Exercises

Reference code for these exercises is posted on GitHub at:
    https://github.com/ktbyers/pynet/tree/master/learning_python/lesson6

Note, you will need some sort of a network device to work on these exercises. This can be a virtual or physical device. Make sure you are only working on test or lab devices.


1. Using Netmiko, establish a connection to a network device and print out the device's prompt.


2. Use send_command() to send a show command down the SSH channel. Retrieve the results and print the results to the screen.


3. Find a command on your device that has additional prompting. Use send_command_timing to send the command down the SSH channel. Capture the output and handle the additional prompting.


4. Use send_config_set() and send_config_from_file() to make configuration changes. 

The configuration changes should be benign. For example, on Cisco IOS I typically change the logging buffer size. 

As part of your program verify that the configuration change occurred properly. For example, use send_command() to execute 'show run' and verify the new configuration.


5. Optional, use send_command() in conjunction with ntc-templates to execute a show command. Have TextFSM automatically convert this show command output to structured data.


6. Optional, connect to three networking devices one after the other. Use send_command() to execute a show command on each of these devices. Print this output to the screen.



CLASS OUTLINE
1. Netmiko Introduction and Basics (VIDEO1)
   A. Netmiko overview   [00:05]
      1. Alternate libraries   [00:36]
      2. Netmiko supported platforms   [1:00]
   B. Establishing a connection   [2:02]
      1. device_type   [3:35]
      2. Passing connection arguments using a dictionary   [5:00]
 
2. Netmiko Show Commands (VIDEO2)
   A. Using the .enable() method   [00:47]
   B. Executing show commands   [4:14]
      1. Command echo, trailing prompt are removed   [5:42]
      2. Executing multiple commands in sequence   [6:35]
   C. Changing the terminating search pattern   [7:48]
   D. Other platforms (Arista, Juniper)   [8:57]
      1. Convert to a loop structure   [10:26]
 
3. Netmiko and Prompting (VIDEO3)
   A. Multiline commands (i.e. additional prompting)   [00:36]
      1. Handling of additional prompting   [1:16]
   B. Commands that take longer than expected   [6:53]
      1. Using delay_factor   [9:13]
      2. Using global_delay_factor   [10:11]
 
4. Netmiko and TextFSM (VIDEO4)
   A. Integrating to TextFSM   [1:23]
      1. Using ntc-templates   [2:03]
      2. How to use TextFSM in Netmiko   [2:17]
      3. How Netmiko finds the templates   [4:20]
         a. Use 'git clone' for installation   [5:25]
      4. Listing of templates   [6:22]
      5. Using an environment variable   [7:34]
 
5. Netmiko and Config Changes (VIDEO5)
   A. Making configuration changes   [00:05]
      1. How to use send_config_set()   [1:28]
      2. Juniper commit() example   [2:39]
      3. Separate 'write memory' is required   [4:25]

6. Netmiko Troubleshooting (VIDEO6)
   A. Logging all reads and writes   [0:40]
   B. Using write_channel() and read_channel()   [3:50]
   C. Misc items   [6:55]
      1. Secure Copy   [6:59]
      2. Telnet and Serial support   [7:32]
      3. Terminal server   [8:19]
 
 
 
 
 [PyNet Learning Python] - Lesson7 / Jinja2, YAML and JSON
 
 ﻿In this email of Learning Python we are going to cover the following:
 
Jinja2 Basics
Video link https://vimeo.com/257997257
Length is 7 minutes
 
Jinja2 For-Loops and Conditionals
Video link https://vimeo.com/257999160
Length is 9 minute
 
Jinja2 and CSV
Video link https://vimeo.com/258142987
Length is 5 minutes
 
Jinja2 Dictionaries and Nested Loops
Video link https://vimeo.com/258145504
Length is 11 minutes
 
YAML Basics
Video link https://vimeo.com/258161182
Length is 9 minutes
 
YAML Part2
Video link https://vimeo.com/258169427
Length is 10 minutes
 
Using Python to Write YAML
Video link https://vimeo.com/258171559
Length is 3 minutes
 
JSON
Video link https://vimeo.com/258178243
Length is 5 minutes
 
Managing Data Structures
Video link https://vimeo.com/258181273
Length is 5 minutes



Additional Content:

Jinja2 Documentation
http://t.dripemail2.com/c/eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJkZXRvdXIiLCJpc3MiOiJtb25vbGl0aCIsInN1YiI6ImRldG91cl9saW5rIiwiaWF0IjoxNjU4ODI3NzgxLCJuYmYiOjE2NTg4Mjc3ODEsImFjY291bnRfaWQiOiI0MjU0NDk3IiwiZGVsaXZlcnlfaWQiOiJ4YndjbjNrZGNtaHhocDBlcGx2OCIsInVybCI6Imh0dHA6Ly9qaW5qYS5wb2Nvby5vcmcvZG9jcy8yLjEwL3RlbXBsYXRlcy8_X19zPTNuaTk2Y3J1c3d2MmEzN2JtbGF4In0.cfb3t-Oy8LPZOeACvZT4QgnTrxdh2tykwMsCGODNBn4

YAML Syntax Basics
http://t.dripemail2.com/c/eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJkZXRvdXIiLCJpc3MiOiJtb25vbGl0aCIsInN1YiI6ImRldG91cl9saW5rIiwiaWF0IjoxNjU4ODI3NzgxLCJuYmYiOjE2NTg4Mjc3ODEsImFjY291bnRfaWQiOiI0MjU0NDk3IiwiZGVsaXZlcnlfaWQiOiJ4YndjbjNrZGNtaHhocDBlcGx2OCIsInVybCI6Imh0dHA6Ly9kb2NzLmFuc2libGUuY29tL2Fuc2libGUvbGF0ZXN0L1lBTUxTeW50YXguaHRtbD9fX3M9M25pOTZjcnVzd3YyYTM3Ym1sYXgifQ.SsCfOF76yXZZg8HcllfnvM9U9GmfiXMpg4_Sq6iiLfk



Exercises

Reference code for these exercises is posted on GitHub at:
    https://github.com/ktbyers/pynet/tree/master/learning_python/lesson7



1a. Use Jinja2 templating to render the following:
vlan 
   name 

Your template should be inside of your Python program for simplicity.

The output from processing your template should be as follows. This should be printed to stdout.
vlan 400
   name red400

1b. Using a conditional in a Jinja2 template, generate the following output:
crypto isakmp policy 10
 encr aes
 authentication pre-share
 group 5
crypto isakmp key my_key address 1.1.1.1 no-xauth
crypto isakmp keepalive 10 periodic

The encryption of aes, and the Diffie-Hellman group should be variables in the template.

Additionally this entire ISAKMP section should only be added if the isakmp_enable variable is set to True.

Your template should be inside your Python program for simplicity.


1c. Using Jinja2 templating and a for-loop inside the template, generate the following configuration snippet:
vlan 501
   name blue501
vlan 502
   name blue502
vlan 503
   name blue503
vlan 504
   name blue504
vlan 505
   name blue505
vlan 506
   name blue506
vlan 507
   name blue507
vlan 508
   name blue508

Your template should be inside your Python program for simplicity.

It is fine for your VLAN IDs to be out of order in the generated configuration (for example, VLAN ID 508 can come before VLAN ID 504).


2. Using Python and Jinja2 templating generate the following OSPF configuration:
interface vlan 1
   ip ospf priority 100

router ospf 10
   passive-interface default
   no passive-interface Vlan1
   no passive-interface Vlan2
   network 10.10.10.0/24 area 0.0.0.0
   network 10.10.20.0/24 area 0.0.0.0
   network 10.10.30.0/24 area 0.0.0.0
   max-lsa 12000

The following items should be variables in your Jinja2 template:
​ospf_process_id
ospf_priority
ospf_active_interfaces (i.e. the non-passive interfaces)
ospf_area0_networks (the three networks that are specified as belonging to area0)

Your template should be in an external file.

Your template should also use a conditional to control whether this is output or not:
interface vlan 1
   ip ospf priority 100

If the 'ospf_priority variable is defined', then include that section. If 'ospf_priority' is not defined then only include the 'router ospf 10' section.


3a. Create a YAML file that defines a list of interface names. Use the expanded form of YAML.

Use a Python script to read in this YAML list and print it to the screen.

The output of your Python script should be:
['Ethernet1', 'Ethernet2', 'Ethernet3', 'Ethernet4', 'Ethernet5', 'Ethernet6', 'Ethernet7', 'Management1', 'Vlan1']


3b. Expand the data structure defined earlier in exercise3a. This time you should have an 'interfaces' key that refers to a dictionary.

Use Python to read in this YAML data structure and print this to the screen.

The output of your Python script should look as follows (in other words, your YAML data structure should yield the following when read by Python). You YAML data structure should be written in expanded YAML format.

{'interfaces': {
    'Ethernet1': {'mode': 'access', 'vlan': 10},
    'Ethernet2': {'mode': 'access', 'vlan': 20},
    'Ethernet3': {'mode': 'trunk',
                  'native_vlan': 1,
                  'trunk_vlans': 'all'}
    }
}
​
4. Take the YAML file and corresponding data structure that you defined in exercise3b:
{'interfaces': {
    'Ethernet1': {'mode': 'access', 'vlan': 10},
    'Ethernet2': {'mode': 'access', 'vlan': 20},
    'Ethernet3': {'mode': 'trunk',
                  'native_vlan': 1,
                  'trunk_vlans': 'all'}
    }
}

From this YAML data input source, use Jinja templating to generate the following configuration output:

interface Ethernet1
  switchport mode access
  switchport access vlan 10
interface Ethernet2
  switchport mode access
  switchport access vlan 20
interface Ethernet3
  switchport mode trunk
  switchport trunk native vlan 1
  switchport trunk allowed vlan all

The following should all be variables in your Jinja template (the names may be different than below, but they should be variabilized and not be hard-coded in your template).
interface_name
switchport_mode
access_vlan
native_vlan
trunk_vlans

All your Jinja2 variables should be retrieved from your YAML file. 

This exercise might be challenging.



CLASS OUTLINE

1. Jinja2 Basics (VIDEO1)
   A. What is Jinja2?   [00:11]
      1. Jinja2 is also used in Ansible   [2:11]
   B. Jinja2 basic use   [2:22] 
      1. Cisco configuration example   [2:33]
      2. Variables embedded using    [3:57]
      3. Expanding to more variables   [5:17]

2. Jinja2 For-loops and Conditionals (VIDEO2)
   A. Decoupling the template from the code   [00:08]
   B. Jinja2 and for-loops   [2:10]
      1. Embedding a for-loop in the template   [2:40]
      2. Controlling whitespace   [5:16]
   C. Jinja2 and conditionals   [6:35]
      1. How much logic in a Jinja2 template   [7:47]

3. Jinja2 and a CSV File (VIDEO3)
   A. Reading data from an external CSV source   [00:06]
      1. Using CSV DictReader   [1:12]
      2. Adding additional CSV rows   [3:17]

4. Jinja2 dictionaries and nested for-loops (VIDEO4)
   A. Looping over Jinja2 dictionaries using .items()   [1:22]
   B. Looping over Jinja2 lists   [3:24]
   C. Jinja2 nested for-loops   [4:31]
   D. Jinja2 nested conditionals   [7:58]
   E. Jinja2 dictionaries accessing keys   [9:36]

5. YAML Basics (VIDEO5)
   A. Introduction to YAML   [00:04]
      1. Why do we care about YAML?   [00:18]
      2. What is serialization?   [00:38]
      3. YAML is used in Ansible and Salt   [2:27]
   B. Basic YAML
      1. Creating a list   [2:57]
      2. Creating a dictionary   [6:20]

6. YAML Part2 (VIDEO6)
   A. YAML basic data types   [00:12]
      1. Strings   [00:15]
      2. Quoting strings   [00:43]
      3. Booleans   [1:22]
      4. Integers   [3:16]
   B. YAML and complex data structures   [3:43]
      1. Dictionaries containing dictionaries   [3:52]
      2. Dictionaries containing lists   [6:21]
   C. YAML expanded form and compressed form   [8:03]
      1. YAML is a superset of JSON   [8:17]

7. Writing YAML using Python (VIDEO7)

8. JSON (VIDEO8)
   A. What is JSON?   [00:02]  
   B. Comparing Python to JSON   [2:09]
   C. Writing JSON out to a file   [1:44]
   D. Reading JSON in Python   [3:39]
   E. Talking about APIs and JSON   
      1. Why do we care about JSON?   [4:29]
      2. Some APIs that use JSON (Arista eAPI, NX-API)   [4:35]
      3. REST APIs frequently use JSON   [4:49]

9. Managing Data Structures (VIDEO9)
   A. Complex data structures   [00:35]
      1. Dictionaries that contain lists or dictionaries   
      2. Lists that contains dictionaries or lists   
   B. Handling complex data structures   [1:19]
      1. Peeling back a layer at a time   [2:03]
         a. Dictionaries   [2:17]
         b. Lists   [3:34]    
   C. Creating complex data structures in Python   [4:51]
   
   
   
   



