# Tabla de contenido

- Introducción

### Parte 1: Preliminar

1. Documentos de dominio
     - Dominios problemáticos
     - Documentos para implementar un dominio de problema
     - Documentos para escribir un Sistema Operativo x56

2. Del hardware al software: capas de abstracción
     - La implementación física de un bit.
     - Más allá de los transitores: puertas lógicas digitales
     - Más allá de las puertas lógicas: lenguaje máquina
     - Abstracción

3. Arquitectura informática
     - ¿Que es una computadora?
     - Arquitectura de Computadores
     - arquitectura x86
     - Conjunto de chips Intel Q35
     - Entorno de ejecución x86

4. Asamblea x86 y C
     - Objeto de volcado
     - Lectura de la salida
     - Manuales Intel
     - Experimentar con código ensamblador
     - Anatomía de una Instrucción de Montaje
     - Comprender una instrucción en detalle.
     - Ejemplo: instrucción jmp
     - Examinar los datos compilados
     - Examinar el código compilado

5. La anatomía de un programa
     - Documentos de referencia
     - Cabecera ELF
     - Tabla de encabezado de sección
     - Comprender la sección en profundidad
     - Tabla de encabezado del programa
     - Segmentos vs secciones

6. Inspección y depuración en tiempo de ejecución
     - Un programa de muestra
     - Inspección estática de un programa
     - Inspección en tiempo de ejecución de un programa.
     - Cómo funcionan los depuradores: una breve introducción

## Parte 2: Bases

7. Cargador de arranque
     - Proceso de arranque x86
     - Uso de los servicios del BIOS
     - Proceso de arranque
     - Ejemplo de gestor de arranque
     - Compilar y cargar
     - Cargar un programa desde el gestor de arranque
     - Mejorar la productividad con scripts

8. Vinculación y carga sobre metal desnudo
     - Comprender las reubicaciones con readelf
     - Creación de binarios ELF con scripts de enlace.
     - Tiempo de ejecución de C: alojado frente a independiente
     - Cargador de arranque depurable en bare metal
     - Programa depurable en bare metal

## Parte 3: Programación del kernel

9. Descriptores x86
     - Conceptos básicos del sistema operativo
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
     - Implementación de Procesos
     - Hito: refactorización de código

11. Interrumpir
12. Gestión de memoria
13. Sistema de archivos