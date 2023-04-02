# Introducci�n:

�Saludos!
Probablemente te hayas preguntado al menos una vez c�mo se escribe un sistema operativo desde cero. Es posible que incluso tenga a�os de experiencia en programaci�n en su haber, pero su comprensi�n de los sistemas operativos a�n puede ser una colecci�n de conceptos abstractos que no se basan en la implementaci�n real. Para aquellos que nunca han construido uno, un sistema operativo puede parecer m�gico: algo misterioso que puede controlar el hardware mientras maneja las solicitudes de un programador a trav�s de la API de su lenguaje de programaci�n favorito. Aprender a construir un sistema operativo parece intimidante y dif�cil; no importa cu�nto aprenda, nunca se siente como si supiera lo suficiente. Probablemente est� leyendo este libro ahora mismo para obtener una mejor comprensi�n de los sistemas operativos y ser un mejor ingeniero de software.
Si ese es el caso, este libro es para ti. Al leer este libro, podr� encontrar las piezas que faltan que son esenciales y le permitir�n implementar su propio sistema operativo desde cero. S�, desde cero, sin pasar por ninguna capa del sistema operativo existente para demostrarte a ti mismo que eres un desarrollador de sistemas operativos. Puede preguntar: "�No es m�s pr�ctico aprender los aspectos internos de Linux?". Si y no. Aprender Linux puede ayudar a su flujo de trabajo en su trabajo diario. Sin embargo, si sigue esa ruta, a�n no lograr� el objetivo final de escribir un sistema operativo real. Al escribir su propio sistema operativo, obtendr� conocimientos que no podr� obtener simplemente aprendiendo Linux.

### Aqu� hay una lista de algunos beneficios de escribir su propio sistema operativo:
- Aprender�s c�mo funciona una computadora a nivel de hardware, y
aprender� a escribir software para administrar ese hardware directamente
- Aprender�s los fundamentos de los sistemas operativos, permiti�ndote adaptarte a cualquier sistema operativo, no solo Linux
- Para piratear las partes internas de Linux de manera adecuada, deber� escribir al menos un sistema operativo por su cuenta. Esto es como la programaci�n de aplicaciones: para escribir una aplicaci�n grande, deber� comenzar con aplicaciones simples.
- Abrir� caminos a varios dominios de programaci�n de bajo nivel, como ingenier�a inversa, exploits, creaci�n de m�quinas virtuales, emulaci�n de consolas de juegos y m�s. El lenguaje ensamblador se convertir� en una de sus herramientas m�s indispensables para el an�lisis de bajo nivel. (�Pero eso no significa que tenga que escribir su sistema operativo en ensamblador!)
- Escribir un sistema operativo es divertido

### �Por qu� otro libro sobre Sistemas Operativos?
Ya existen muchos libros y cursos sobre este tema realizados por profesores y expertos famosos. �Qui�n soy yo para escribir un libro sobre un tema tan avanzado? Si bien es cierto que existen muchos recursos de calidad, los encuentro escasos. �Alguno de ellos le muestra c�mo compilar su c�digo C y la biblioteca de tiempo de ejecuci�n C independientemente de un sistema operativo existente? La mayor�a de los libros sobre dise�o e implementaci�n de sistemas operativos solo analizan el lado del software; se omite c�mo se comunica el sistema operativo con el hardware. Se omiten detalles importantes del hardware y es dif�cil para un autodidacta encontrar recursos relevantes en Internet.
Uno de los enfoques principales de este libro es guiarlo a trav�s del proceso de lectura de la documentaci�n oficial de los proveedores para implementar su software. Los documentos oficiales de proveedores de hardware como Intel son fundamentales para implementar un sistema operativo o cualquier otro software que controle directamente el hardware. Como m�nimo, un desarrollador de sistema operativo debe poder comprender estos documentos e implementar software basado en un conjunto de requisitos de hardware. Por lo tanto, el primer cap�tulo est� dedicado a discutir los documentos relevantes y su importancia.
Otra caracter�stica distintiva de este libro es que est� centrado en �Hello World�. La mayor�a de los ejemplos giran en torno a variantes de un programa "Hello World", que lo familiarizar� con los conceptos b�sicos. Estos conceptos deben aprenderse antes de intentar escribir un sistema operativo. Cualquier cosa m�s all� de un simple ejemplo de "Hola mundo" interfiere en la ense�anza de los conceptos, lo que alarga el tiempo dedicado a comenzar a escribir un sistema operativo.
Profundicemos. Con este libro, espero proporcionar suficiente conocimiento fundamental que le abrir� las puertas para que pueda entender otros recursos. Este libro ser� muy beneficioso para los estudiantes que acaban de terminar su primer curso de C/C++. Imagina lo genial que ser�a mostrarles a los posibles empleadores que ya has creado un sistema operativo.

## Requisitos previos
### Conocimientos b�sicos de circuitos
- Conceptos b�sicos de electricidad: �tomos, electrones, protones, neutrones, flujo de corriente.
- Ley de Ohm.
Si no est� familiarizado con estos conceptos, puede aprenderlos r�pidamente (aqu�) [http://www.allaboutcircuits.com/textbook/], leyendo el cap�tulo 1 y el cap�tulo 2.

### Programaci�n en C en particular
- Declaraciones / definiciones de variables y funciones.
- Mientras que los bucles.
- Punteros y punteros de funci�n.
- Algoritmos fundamentales y estructuras de datos en C.

### Conceptos b�sicos de Linux
- Saber navegar por el directorio con la interfaz de linea de comandos (CLI)
- Saber invocar un comando con opciones.
- Saber canalizar la salida a otro programa.

### Escritura t�ctil.
Como vamos a usar Linux, la escritura t�ctil ayuda. S� que la velocidad de escritura no se relaciona con la resoluci�n de problemas, pero al menos su velocidad de escritura debe ser lo suficientemente r�pida como para no permitir que se interponga y degrade la experiencia de aprendizaje.
En general, asumo que el lector tiene conocimientos b�sicos de programaci�n en C y puede usar un IDE para construir y ejecutar un programa.

## Lo que aprender�s en este libro
- C�mo escribir un sistema operativo desde cero leyendo hojas de datos de hardware. En el mundo real, no podr� consultar a Google para obtener una respuesta r�pida.
- Escribir c�digo de forma independiente. No tiene sentido copiar y pegar c�digo. El verdadero aprendizaje ocurre cuando resuelves problemas por tu cuenta. Se proporcionan algunos ejemplos para ayudar a poner en marcha su trabajo, pero la mayor�a de los problemas son suyos para conquistarlos. Sin embargo, las soluciones est�n disponibles en l�nea para usted despu�s de intentarlo.
- Un panorama general de c�mo cada capa de una computadora se relaciona entre s�, desde el hardware hasta el software.
- C�mo usar Linux como entorno de desarrollo y herramientas comunes para la programaci�n de bajo nivel.
- C�mo se estructura un programa para que pueda ejecutarse un sistema operativo.
- C�mo depurar un programa que se ejecuta directamente en hardware con gdb y QEMU.
- Vinculaci�n y carga en bare metal x86_64, con C puro. Sin biblioteca est�ndar. Sin sobrecarga de tiempo de ejecuci�n.

## De qu� no trata este libro
- Ingenier�a el�ctrica: el libro analiza algunos conceptos de la ingenier�a electr�nica y el�ctrica solo en la medida en que el software opera en metal desnudo.
- Libros sobre c�mo usar Linux o cualquier tipo de sistema operativo: Aunque Linux se usa como un entorno de desarrollo y como un medio para demostrar conceptos de sistemas operativos de alto nivel, no es el enfoque de este libro.
- Desarrollo del kernel de Linux: Ya hay muchos libros de alta calidad sobre este tema.
- Libros de sistemas operativos centrados en algoritmos: este libro se centra m�s en la plataforma de hardware real (Intel x86_64) y en c�mo escribir un sistema operativo que utilice la compatibilidad con el sistema operativo de la plataforma de hardware.
 
## La organizaci�n del libro

__Parte 1:__ proporciona una base para el aprendizaje del sistema operativo.
- Cap�tulo 1: explica brevemente la importancia de los documentos de dominio. Los documentos son cruciales para la experiencia de aprendizaje, por lo que merecen un cap�tulo.
- Cap�tulo 2: explica las capas de abstracciones del hardware al software. La idea es proporcionar informaci�n sobre c�mo se ejecuta el c�digo f�sicamente.
- Cap�tulo 3: proporciona la arquitectura general de una computadora, luego presenta un modelo de computadora de muestra que usar� para escribir un sistema operativo.
- Cap�tulo 4: presenta el lenguaje ensamblador x86 mediante el uso de los manuales de Intel, junto con las instrucciones de uso com�n. Este cap�tulo proporciona ejemplos detallados de c�mo la sintaxis de alto nivel se corresponde con el ensamblado de bajo nivel, lo que le permite leer c�modamente el c�digo ensamblador generado. Es necesario leer el c�digo ensamblador al depurar un sistema operativo.
- Cap�tulo 5: disecciona ELF en detalle. Solo al comprender c�mo es la estructura de un programa a nivel binario, puede construir uno que se ejecute en bare metal.
- Cap�tulo 6: presenta el depurador de gdb con ejemplos extensos de los comandos de uso com�n. Despu�s de familiarizar al lector con gdb, proporciona informaci�n sobre c�mo funciona un depurador. Este conocimiento es esencial para construir un programa depurable en el metal desnudo

__Parte 2:__ presenta c�mo escribir un gestor de arranque para arrancar un kernel. De ah� el nombre de �Fundamentos�. Despu�s de dominar esta parte, el lector puede continuar con la siguiente parte, que es una gu�a para escribir un sistema operativo. Sin embargo, si al lector no le gusta la presentaci�n, puede buscar en otra parte, como (OSDev_Wiki)[http://wiki.osdev.org/].
- Cap�tulo 7: presenta qu� es el gestor de arranque, c�mo escribir uno en ensamblador y c�mo cargarlo en QEMU, un emulador de hardware. Este proceso implica escribir comandos repetitivos y largos, por lo que se aplica GNU Make para mejorar la productividad al automatizar las partes repetitivas y simplificar la interacci�n con el proyecto. Este cap�tulo tambi�n demuestra el uso de GNU Make en contexto.
- Cap�tulo 8: introduce la vinculaci�n al explicar el proceso de reubicaci�n al combinar archivos de objetos. Adem�s de un gestor de arranque y un sistema operativo escrito en C, esta es la �ltima pieza del rompecabezas necesaria para crear programas depurables en hardware completo, incluido el gestor de arranque escrito en ensamblador y un sistema operativo escrito en C.

__Parte 3:__ brinda orientaci�n sobre c�mo escribir un sistema operativo, ya que debe implementar un sistema operativo por su cuenta y estar orgulloso de su creaci�n. La gu�a consiste en explicaciones m�s sencillas y coherentes de los conceptos necesarios, desde el hardware hasta el software, para implementar las caracter�sticas de un sistema operativo. Sin esa gu�a, perder� tiempo recopilando informaci�n distribuida a trav�s de varios documentos e Internet. Luego proporciona un plan sobre c�mo mapear los conceptos al c�digo.