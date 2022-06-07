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
