# Tabla de contenido

- Introducci�n

### Parte 1: Preliminar

1. Documentos de dominio
     - Dominios problem�ticos
     - Documentos para implementar un dominio de problema
     - Documentos para escribir un Sistema Operativo x56

2. Del hardware al software: capas de abstracci�n
     - La implementaci�n f�sica de un bit.
     - M�s all� de los transitores: puertas l�gicas digitales
     - M�s all� de las puertas l�gicas: lenguaje m�quina
     - Abstracci�n

3. Arquitectura inform�tica
     - �Que es una computadora?
     - Arquitectura de Computadores
     - arquitectura x86
     - Conjunto de chips Intel Q35
     - Entorno de ejecuci�n x86

4. Asamblea x86 y C
     - Objeto de volcado
     - Lectura de la salida
     - Manuales Intel
     - Experimentar con c�digo ensamblador
     - Anatom�a de una Instrucci�n de Montaje
     - Comprender una instrucci�n en detalle.
     - Ejemplo: instrucci�n jmp
     - Examinar los datos compilados
     - Examinar el c�digo compilado

5. La anatom�a de un programa
     - Documentos de referencia
     - Cabecera ELF
     - Tabla de encabezado de secci�n
     - Comprender la secci�n en profundidad
     - Tabla de encabezado del programa
     - Segmentos vs secciones

6. Inspecci�n y depuraci�n en tiempo de ejecuci�n
     - Un programa de muestra
     - Inspecci�n est�tica de un programa
     - Inspecci�n en tiempo de ejecuci�n de un programa.
     - C�mo funcionan los depuradores: una breve introducci�n

## Parte 2: Bases

7. Cargador de arranque
     - Proceso de arranque x86
     - Uso de los servicios del BIOS
     - Proceso de arranque
     - Ejemplo de gestor de arranque
     - Compilar y cargar
     - Cargar un programa desde el gestor de arranque
     - Mejorar la productividad con scripts

8. Vinculaci�n y carga sobre metal desnudo
     - Comprender las reubicaciones con readelf
     - Creaci�n de binarios ELF con scripts de enlace.
     - Tiempo de ejecuci�n de C: alojado frente a independiente
     - Cargador de arranque depurable en bare metal
     - Programa depurable en bare metal

## Parte 3: Programaci�n del kernel

9. Descriptores x86
     - Conceptos b�sicos del sistema operativo
     - Conductores
     - Espacio de usuario y espacio del kernel
     - Segmento de memoria
     - Descriptor de segmento
     - Tipos de descriptores de segmento
     - Alcance del descriptor
     - Selector de segmento
     - Mejora: Bootloader con descriptros

10. Proceso
     - Conceptos
     - Proceso
     - Hilos
     - Tarea: concepto x86 de un proceso
     - Estructura de datos de tareas
     - Implementaci�n de Procesos
     - Hito: refactorizaci�n de c�digo

11. Interrumpir
12. Gesti�n de memoria
13. Sistema de archivos