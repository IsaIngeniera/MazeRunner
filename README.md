# MazeRunner

Un emocionante juego de laberintos y supervivencia, desarrollado íntegramente en **Jack**.

## Descripción
**MazeRunner** es un juego interactivo donde controlas a un personaje que debe encontrar la salida de un laberinto estático. La dificultad radica en un enemigo equipado con Inteligencia Artificial que te perseguirá a lo largo del mapa. 

El proyecto fue construido aplicando principios de Programación Orientada a Objetos (POO), estructurado en diversas clases para mantener el código modular, escalable y optimizado para el entorno del Hack Computer.

## Características Principales

*   **Inteligencia Artificial:** El enemigo no solo te sigue de forma básica. Utiliza un algoritmo de búsqueda guiado por **Distancia Manhattan** y un **modelo predictivo** que intenta anticiparse a tus movimientos para tenderte emboscadas.
*   **Gráficos y Renderizado Optimizado:** El mapa es renderizado directamente en la memoria para lograr el mejor rendimiento. Cuenta con una resolución adaptada de 256x128 píxeles en una cuadrícula lógica de 8x16.
*   **Menú Interactivo y Personalización:** Al inicio, el jugador puede:
    *   Elegir entre diferentes **modos de dificultad** que modifican la velocidad y el comportamiento del juego.
    *   Cambiar la **forma visual del jugador** o la **forma del enemigo**.
*   **Semillas semi-aleatorias Dinámicas:** La aleatoriedad (para la aparición de enemigos) se basa en el tiempo de respuesta del usuario (interacciones de teclado), asegurando un escenario impredecible y único en cada sesión.
*   **Gestión Completa de Estados de Juego:** Pantallas de Inicio, Juego, Fin de Partida (Victoria/Derrota), y opción para reintentar fácilmente.

## Arquitectura del Proyecto

El código fuente (ubicado en `src/`) se distribuye en varias clases especializadas:

*   `Main.jack`: Punto de entrada del programa. Su única labor es inicializar y arrancar el motor del juego.
*   `Juego.jack`: El *Game Manager* principal. Orquesta el *game loop*, controla la velocidad de los *ticks* y maneja las transiciones entre las distintas pantallas (menú, juego, fin).
*   `Mapa.jack`: Define y dibuja el mapa/laberinto, manejando el renderizado estático y las posiciones de las paredes.
*   `Jugador.jack`: Modela al personaje principal. Controla sus coordenadas, su movimiento en base a colisiones, y sus formas de dibujo.
*   `Enemigo.jack`: Contiene la lógica de la IA (perseguir, predecir) y el movimiento seguro alrededor de las paredes del laberinto.
*   `Validador.jack`: Clase utilitaria de reglas. Comprueba victorias, derrotas, colisiones entre entidades, y límites de memoria de la partida.
*   `Teclado.jack`: Abstracción superior para leer el input del usuario y generar semillas aleatorias en base al tiempo que tarda el jugador en confirmar opciones.
*   `Random.jack`: Algoritmos de generación de números aleatorios a partir de la semilla generada.

## Cómo Jugar / Ejecución

Dado que está programado en Jack, puedes jugarlo en el entorno virtual de Nand2Tetris, siguiendo los siguientes pasos:

1.  Dirigete al [Nand2Tetris](https://nand2tetris.github.io/web-ide/compiler).
2.  Abre el **JackCompiler** y compila todos los archivos de la carpeta `src/`.
3.  Hazlo correr y esto te llevará al entorno de máquina virtual de Nand2Tetris.
4.  Selecciona la velocidad maxima, dale a **Run** y activa el teclado.

## Equipo y Contribuidores
El proyecto ha sido desarrollado de forma colaborativa. 
Para ver detalles de los aportes de cada desarrollador (Isabella Ocampo Sanchez, Maria Laura Tafur Gomez, y Juan Manuel Hernandez Martelo), consulta el archivo [CONTRIBUTORS.md](./CONTRIBUTORS.md).

## Licencia y Cambios
*   Este proyecto está protegido bajo la licencia descrita en [LICENSE.md](./LICENSE.md).
*   Para revisar el historial de desarrollo, decisiones de diseño y versiones de este proyecto, consulta el archivo [CHANGELOG.md](./CHANGELOG.md).
