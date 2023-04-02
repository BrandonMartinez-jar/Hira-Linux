# Tabla de contenido

- [Introducci�n](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Introduccion.md)

### Parte 1: Preliminar

1. [Documentos de dominio](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Documentos%20de%20dominio.md)
     - Dominios problem�ticos
     - Documentos para implementar un dominio de problema
     - Documentos para escribir un Sistema Operativo x56

2. [Del hardware al software: capas de abstracci�n](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Del%20hardware%20al%20software.md)
     - La implementaci�n f�sica de un bit.
     - M�s all� de los transitores: puertas l�gicas digitales
     - M�s all� de las puertas l�gicas: lenguaje m�quina
     - Abstracci�n

3. [Arquitectura inform�tica](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Arquitectura%20informatica.md)
     - �Que es una computadora?
     - Arquitectura de Computadores
     - arquitectura x86
     - Conjunto de chips Intel Q35
     - Entorno de ejecuci�n x86

4. [Asamblea x86 y C](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Asamblea%20x86%20y%20C.md)
     - Objeto de volcado
     - Lectura de la salida
     - Manuales Intel
     - Experimentar con c�digo ensamblador
     - Anatom�a de una Instrucci�n de Montaje
     - Comprender una instrucci�n en detalle.
     - Ejemplo: instrucci�n jmp
     - Examinar los datos compilados
     - Examinar el c�digo compilado

5. [La anatom�a de un programa](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Anatomia%20de%20un%20programa.md)
     - Documentos de referencia
     - Cabecera ELF
     - Tabla de encabezado de secci�n
     - Comprender la secci�n en profundidad
     - Tabla de encabezado del programa
     - Segmentos vs secciones

6. [Inspecci�n y depuraci�n en tiempo de ejecuci�n](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Inspeccion%20y%20depuracion%20en%20tiempo%20de%20ejecucion.md)
     - Un programa de muestra
     - Inspecci�n est�tica de un programa
     - Inspecci�n en tiempo de ejecuci�n de un programa.
     - C�mo funcionan los depuradores: una breve introducci�n

## Parte 2: Bases

7. [Cargador de arranque](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Cargador%20de%20arranque.md)
     - Proceso de arranque x86
     - Uso de los servicios del BIOS
     - Proceso de arranque
     - Ejemplo de gestor de arranque
     - Compilar y cargar
     - Cargar un programa desde el gestor de arranque
     - Mejorar la productividad con scripts

8. [Vinculaci�n y carga sobre metal desnudo](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Vinculacion%20y%20carga%20sobre%20metal.md)
     - Comprender las reubicaciones con readelf
     - Creaci�n de binarios ELF con scripts de enlace.
     - Tiempo de ejecuci�n de C: alojado frente a independiente
     - Cargador de arranque depurable en bare metal
     - Programa depurable en bare metal

## Parte 3: Programaci�n del kernel

9. [Descriptores x86](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Descriptores%20x86.md)
     - Conceptos b�sicos del sistema operativo
     - Conductores
     - Espacio de usuario y espacio del kernel
     - Segmento de memoria
     - Descriptor de segmento
     - Tipos de descriptores de segmento
     - Alcance del descriptor
     - Selector de segmento
     - Mejora: Bootloader con descriptros

10. [Proceso](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Proceso.md)
     - Conceptos
     - Proceso
     - Hilos
     - Tarea: concepto x86 de un proceso
     - Estructura de datos de tareas
     - Implementaci�n de Procesos
     - Hito: refactorizaci�n de c�digo

11. [Interrumpir](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Interrumpir.md)
12. [Gesti�n de memoria](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Gestion%20de%20memoria.md)
13. [Sistema de archivos](https://github.com/BrandonMartinez-jar/Hira-Linux/blob/main/Spanish/Sistema%20de%20archivos.md)