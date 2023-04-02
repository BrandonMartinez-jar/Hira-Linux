# Introducción:

¡Saludos!
Probablemente te hayas preguntado al menos una vez cómo se escribe un sistema operativo desde cero. Es posible que incluso tenga años de experiencia en programación en su haber, pero su comprensión de los sistemas operativos aún puede ser una colección de conceptos abstractos que no se basan en la implementación real. Para aquellos que nunca han construido uno, un sistema operativo puede parecer mágico: algo misterioso que puede controlar el hardware mientras maneja las solicitudes de un programador a través de la API de su lenguaje de programación favorito. Aprender a construir un sistema operativo parece intimidante y difícil; no importa cuánto aprenda, nunca se siente como si supiera lo suficiente. Probablemente esté leyendo este libro ahora mismo para obtener una mejor comprensión de los sistemas operativos y ser un mejor ingeniero de software.
Si ese es el caso, este libro es para ti. Al leer este libro, podrá encontrar las piezas que faltan que son esenciales y le permitirán implementar su propio sistema operativo desde cero. Sí, desde cero, sin pasar por ninguna capa del sistema operativo existente para demostrarte a ti mismo que eres un desarrollador de sistemas operativos. Puede preguntar: "¿No es más práctico aprender los aspectos internos de Linux?". Si y no. Aprender Linux puede ayudar a su flujo de trabajo en su trabajo diario. Sin embargo, si sigue esa ruta, aún no logrará el objetivo final de escribir un sistema operativo real. Al escribir su propio sistema operativo, obtendrá conocimientos que no podrá obtener simplemente aprendiendo Linux.

### Aquí hay una lista de algunos beneficios de escribir su propio sistema operativo:
- Aprenderás cómo funciona una computadora a nivel de hardware, y
aprenderá a escribir software para administrar ese hardware directamente
- Aprenderás los fundamentos de los sistemas operativos, permitiéndote adaptarte a cualquier sistema operativo, no solo Linux
- Para piratear las partes internas de Linux de manera adecuada, deberá escribir al menos un sistema operativo por su cuenta. Esto es como la programación de aplicaciones: para escribir una aplicación grande, deberá comenzar con aplicaciones simples.
- Abrirá caminos a varios dominios de programación de bajo nivel, como ingeniería inversa, exploits, creación de máquinas virtuales, emulación de consolas de juegos y más. El lenguaje ensamblador se convertirá en una de sus herramientas más indispensables para el análisis de bajo nivel. (¡Pero eso no significa que tenga que escribir su sistema operativo en ensamblador!)
- Escribir un sistema operativo es divertido

### ¿Por qué otro libro sobre Sistemas Operativos?
Ya existen muchos libros y cursos sobre este tema realizados por profesores y expertos famosos. ¿Quién soy yo para escribir un libro sobre un tema tan avanzado? Si bien es cierto que existen muchos recursos de calidad, los encuentro escasos. ¿Alguno de ellos le muestra cómo compilar su código C y la biblioteca de tiempo de ejecución C independientemente de un sistema operativo existente? La mayoría de los libros sobre diseño e implementación de sistemas operativos solo analizan el lado del software; se omite cómo se comunica el sistema operativo con el hardware. Se omiten detalles importantes del hardware y es difícil para un autodidacta encontrar recursos relevantes en Internet.
Uno de los enfoques principales de este libro es guiarlo a través del proceso de lectura de la documentación oficial de los proveedores para implementar su software. Los documentos oficiales de proveedores de hardware como Intel son fundamentales para implementar un sistema operativo o cualquier otro software que controle directamente el hardware. Como mínimo, un desarrollador de sistema operativo debe poder comprender estos documentos e implementar software basado en un conjunto de requisitos de hardware. Por lo tanto, el primer capítulo está dedicado a discutir los documentos relevantes y su importancia.
Otra característica distintiva de este libro es que está centrado en “Hello World”. La mayoría de los ejemplos giran en torno a variantes de un programa "Hello World", que lo familiarizará con los conceptos básicos. Estos conceptos deben aprenderse antes de intentar escribir un sistema operativo. Cualquier cosa más allá de un simple ejemplo de "Hola mundo" interfiere en la enseñanza de los conceptos, lo que alarga el tiempo dedicado a comenzar a escribir un sistema operativo.
Profundicemos. Con este libro, espero proporcionar suficiente conocimiento fundamental que le abrirá las puertas para que pueda entender otros recursos. Este libro será muy beneficioso para los estudiantes que acaban de terminar su primer curso de C/C++. Imagina lo genial que sería mostrarles a los posibles empleadores que ya has creado un sistema operativo.

## Requisitos previos
### Conocimientos básicos de circuitos
- Conceptos básicos de electricidad: átomos, electrones, protones, neutrones, flujo de corriente.
- Ley de Ohm.
Si no está familiarizado con estos conceptos, puede aprenderlos rápidamente (aquí) [http://www.allaboutcircuits.com/textbook/], leyendo el capítulo 1 y el capítulo 2.

### Programación en C en particular
- Declaraciones / definiciones de variables y funciones.
- Mientras que los bucles.
- Punteros y punteros de función.
- Algoritmos fundamentales y estructuras de datos en C.

### Conceptos básicos de Linux
- Saber navegar por el directorio con la interfaz de linea de comandos (CLI)
- Saber invocar un comando con opciones.
- Saber canalizar la salida a otro programa.

### Escritura táctil.
Como vamos a usar Linux, la escritura táctil ayuda. Sé que la velocidad de escritura no se relaciona con la resolución de problemas, pero al menos su velocidad de escritura debe ser lo suficientemente rápida como para no permitir que se interponga y degrade la experiencia de aprendizaje.
En general, asumo que el lector tiene conocimientos básicos de programación en C y puede usar un IDE para construir y ejecutar un programa.

## Lo que aprenderás en este libro
- Cómo escribir un sistema operativo desde cero leyendo hojas de datos de hardware. En el mundo real, no podrá consultar a Google para obtener una respuesta rápida.
- Escribir código de forma independiente. No tiene sentido copiar y pegar código. El verdadero aprendizaje ocurre cuando resuelves problemas por tu cuenta. Se proporcionan algunos ejemplos para ayudar a poner en marcha su trabajo, pero la mayoría de los problemas son suyos para conquistarlos. Sin embargo, las soluciones están disponibles en línea para usted después de intentarlo.
- Un panorama general de cómo cada capa de una computadora se relaciona entre sí, desde el hardware hasta el software.
- Cómo usar Linux como entorno de desarrollo y herramientas comunes para la programación de bajo nivel.
- Cómo se estructura un programa para que pueda ejecutarse un sistema operativo.
- Cómo depurar un programa que se ejecuta directamente en hardware con gdb y QEMU.
- Vinculación y carga en bare metal x86_64, con C puro. Sin biblioteca estándar. Sin sobrecarga de tiempo de ejecución.

## De qué no trata este libro
- Ingeniería eléctrica: el libro analiza algunos conceptos de la ingeniería electrónica y eléctrica solo en la medida en que el software opera en metal desnudo.
- Libros sobre cómo usar Linux o cualquier tipo de sistema operativo: Aunque Linux se usa como un entorno de desarrollo y como un medio para demostrar conceptos de sistemas operativos de alto nivel, no es el enfoque de este libro.
- Desarrollo del kernel de Linux: Ya hay muchos libros de alta calidad sobre este tema.
- Libros de sistemas operativos centrados en algoritmos: este libro se centra más en la plataforma de hardware real (Intel x86_64) y en cómo escribir un sistema operativo que utilice la compatibilidad con el sistema operativo de la plataforma de hardware.
 
## La organización del libro

__Parte 1:__ proporciona una base para el aprendizaje del sistema operativo.
- Capítulo 1: explica brevemente la importancia de los documentos de dominio. Los documentos son cruciales para la experiencia de aprendizaje, por lo que merecen un capítulo.
- Capítulo 2: explica las capas de abstracciones del hardware al software. La idea es proporcionar información sobre cómo se ejecuta el código físicamente.
- Capítulo 3: proporciona la arquitectura general de una computadora, luego presenta un modelo de computadora de muestra que usará para escribir un sistema operativo.
- Capítulo 4: presenta el lenguaje ensamblador x86 mediante el uso de los manuales de Intel, junto con las instrucciones de uso común. Este capítulo proporciona ejemplos detallados de cómo la sintaxis de alto nivel se corresponde con el ensamblado de bajo nivel, lo que le permite leer cómodamente el código ensamblador generado. Es necesario leer el código ensamblador al depurar un sistema operativo.
- Capítulo 5: disecciona ELF en detalle. Solo al comprender cómo es la estructura de un programa a nivel binario, puede construir uno que se ejecute en bare metal.
- Capítulo 6: presenta el depurador de gdb con ejemplos extensos de los comandos de uso común. Después de familiarizar al lector con gdb, proporciona información sobre cómo funciona un depurador. Este conocimiento es esencial para construir un programa depurable en el metal desnudo

__Parte 2:__ presenta cómo escribir un gestor de arranque para arrancar un kernel. De ahí el nombre de “Fundamentos”. Después de dominar esta parte, el lector puede continuar con la siguiente parte, que es una guía para escribir un sistema operativo. Sin embargo, si al lector no le gusta la presentación, puede buscar en otra parte, como [OSDev_Wiki](http://wiki.osdev.org/).
- Capítulo 7: presenta qué es el gestor de arranque, cómo escribir uno en ensamblador y cómo cargarlo en QEMU, un emulador de hardware. Este proceso implica escribir comandos repetitivos y largos, por lo que se aplica GNU Make para mejorar la productividad al automatizar las partes repetitivas y simplificar la interacción con el proyecto. Este capítulo también demuestra el uso de GNU Make en contexto.
- Capítulo 8: introduce la vinculación al explicar el proceso de reubicación al combinar archivos de objetos. Además de un gestor de arranque y un sistema operativo escrito en C, esta es la última pieza del rompecabezas necesaria para crear programas depurables en hardware completo, incluido el gestor de arranque escrito en ensamblador y un sistema operativo escrito en C.

__Parte 3:__ brinda orientación sobre cómo escribir un sistema operativo, ya que debe implementar un sistema operativo por su cuenta y estar orgulloso de su creación. La guía consiste en explicaciones más sencillas y coherentes de los conceptos necesarios, desde el hardware hasta el software, para implementar las características de un sistema operativo. Sin esa guía, perderá tiempo recopilando información distribuida a través de varios documentos e Internet. Luego proporciona un plan sobre cómo mapear los conceptos al código.
