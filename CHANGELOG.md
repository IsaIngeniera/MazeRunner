# Historial de cambios
Todas las mejoras y modificaciones notables de este proyecto serán documentadas en este archivo.

## [1.0.0] - 2026-05-09
### Agregado
- Inicialización del repositorio, junto con su estructura y archivos base.
- Creación de la clase 'Mapa.jack', ´Main.jack´,´Teclado.jack´,´Juego.jack´,´Jugador.jack´,´Enemigo.jack´ y ´Validador.jack´

## [1.0.1] - 2026-05-10
### Modificado
- Se modifico la arquitectura del proyecto para que fuera mas entendible y facil de usar.

## [1.0.2] - 2026-05-11
### Agregado
- README.md con la descripción del proyecto y los objetivos.
- LICENSE.md con la licencia del proyecto.
- CHANGELOG.md con el historial de cambios.

### Modificado
- ´Main.jack´: Se agregó la lógica para la prueba de la clase ´Mapa´.
- ´Mapa.jack´: Implementación de un laberinto básico para la prueba de la lógica del juego.

## [1.0.3] - 2026-05-13
### Modificado
- `Mapa.jack`: Rediseño completo para utilizar dimensiones estáticas de 256x128 píxeles (cuadrícula de 8x16). Se hardcodeó el laberinto inicial, se incluyó renderizado de alto rendimiento directo en memoria y se definió un punto de "escape".
- - `Main.jack` : Agregar la parte de creacion de la semilla, la cual nos ayuda a las dos clases anteriores para lo aleatorio.
  
## [1.0.4] - 2026-05-17
- `Enemigo.jack`: Creacion de las clase, con sus metodos para la logica del enemigo 
- `Random.jack` : Creacion de la clase que nos ayuda a que la posicion del enemigo en cada jugada sea diferente

## [1.0.5] - 2026-05-24
### Agregado
- Interfaz de inicio y menú de selección con opciones de modo, forma del jugador y forma del enemigo en `Main.jack`.
- Lógica de bucle del juego, controles de jugador, detección de victoria/derrota y pantalla de fin/reintento en `Main.jack`.
- `Documentacion_Maze_Runner.docx`. Allí se comenzó a detallar la funcionalidad de cada una de las clases, los campos y las variables que compone a cada una

### Modificado
- `Jugador.jack`: se mejoró la forma y tamaño, movimiento con colisiones, dibujo dinámico y borrado de su posición anterior.
- `Enemigo.jack`: Cambio de la lógica de movimiento, nuevo método de paso seguro, dibujo con varias formas y tamaño, y aparición aleatoria válida sobre el mapa.
- `Mapa.jack`: ajustes en el diseño del laberinto y en la definición de muros internos.


## [1.0.6] - 2026-05-



## [1.0.7] - 2026-06-



## [1.0.8] - 2026-06-



## [1.0.9] - 2026-06-



## [1.1.0] - 2026-05-



## [1.1.1] - 2026-05-



## [1.1.2] - 2026-05-



## [1.1.3] - 2026-05-


