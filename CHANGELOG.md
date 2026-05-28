# Historial de cambios
Todas las mejoras y modificaciones notables de este proyecto serán documentadas en este archivo.

## [1.0.0] - 2026-05-09
### Agregado
- Inicialización del repositorio, junto con su estructura y archivos base.
- Creación de la clase `Mapa.jack`, `Main.jack`, `Teclado.jack`, `Juego.jack`, `Jugador.jack`, `Enemigo.jack` y `Validador.jack`.

## [1.0.1] - 2026-05-10
### Modificado
- Se modifico la arquitectura del proyecto para que fuera mas entendible y facil de usar.

## [1.0.2] - 2026-05-11
### Agregado
- `LICENSE.md` con la licencia del proyecto.
- `CONTRIBUTORS.md` con los contribuidores del proyecto.
- `CHANGELOG.md` con el historial de cambios.

### Modificado
- `Main.jack`: Se agregó la lógica para la prueba de la clase `Mapa.jack`.
- `Mapa.jack`: Implementación de un laberinto básico para la prueba de la lógica del juego.

## [1.0.3] - 2026-05-13
### Modificado
- `Mapa.jack`: Rediseño completo para utilizar dimensiones estáticas de 256x128 píxeles (cuadrícula de 8x16). Se hardcodeó el laberinto inicial, se incluyó renderizado de alto rendimiento directo en memoria y se definió un punto de "escape".
- - `Main.jack` : Agregar la parte de creacion de la semilla, la cual nos ayuda a las dos clases anteriores para lo aleatorio.
  
## [1.0.4] - 2026-05-17
- `Enemigo.jack`: Creacion de las clase, con sus metodos para la logica del enemigo 
- `Random.jack` : Creacion de la clase que nos ayuda a que la posicion del enemigo en cada jugada sea diferente

## [1.0.5] - 2026-05-20
### Agregado
- Interfaz de inicio y menú de selección con opciones de modo, forma del jugador y forma del enemigo en `Main.jack`.
- Lógica de bucle del juego, controles de jugador, detección de victoria/derrota y pantalla de fin/reintento en `Main.jack`.
- `Documentacion_Maze_Runner.docx`. Allí se comenzó a detallar la funcionalidad de cada una de las clases, los campos y las variables que compone a cada una

### Modificado
- `Jugador.jack`: se mejoró la forma y tamaño, movimiento con colisiones, dibujo dinámico y borrado de su posición anterior.
- `Enemigo.jack`: Cambio de la lógica de movimiento, nuevo método de paso seguro, dibujo con varias formas y tamaño, y aparición aleatoria válida sobre el mapa.
- `Mapa.jack`: ajustes en el diseño del laberinto y en la definición de muros internos.

## [1.1.0] - 2026-05-24
### Agregado
- `Teclado.jack`: Nueva clase utilitaria que abstrae la lectura de inputs del usuario (direcciones, opciones, confirmaciones) y la generación de la semilla aleatoria según el tiempo de respuesta.
- `Validador.jack`: Nueva clase encargada de verificar la lógica de estado del juego (límites de partidas por memoria, colisiones y detección de victoria).
- `Juego.jack`: Nueva clase que actúa como *Game Manager*, orquestando el *game loop* y manejando el renderizado de la interfaz de inicio, fin y recarga.

### Modificado
- `Main.jack`: Refactorizado de principio a fin. Se extrajo toda la lógica a clases especializadas, dejando el `Main` como un punto de entrada limpio que solo inicializa y arranca `Juego`.
- `Enemigo.jack`: Mejora sustancial en la Inteligencia Artificial:
  - IA Predictiva: El enemigo intenta calcular el futuro movimiento del jugador para tender emboscadas si está lejos, y persecución directa si está cerca.
  - Algoritmo de Rutas (Greedy BFS): Reescritura del algoritmo de persecución usando Distancia Manhattan, resolviendo los errores donde el enemigo quedaba atascado en pasillos y paredes con forma de U.
- `Juego.jack`: Se ajustó el *tick rate* haciéndolo significativamente más desafiante y rápido en todos los modos.

## [1.1.1] - 2026-05-28
### Agregado
- `README.md`: Se añadio la descripción del proyecto y las instrucciones de ejecución.

### Modificado
- `CONTRIBUTORS.md`: Se calificaron entre los contribuidores del proyecto.