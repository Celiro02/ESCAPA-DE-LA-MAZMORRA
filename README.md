# ESCAPA-DE-LA-MAZMORRA
Juego de mazmorra
Sistema de Mazmorra en Consola
Descripción
Juego desarrollado en Python para simular un RPG de mazmorra en consola. Permite mover un personaje, luchar contra enemigos, recoger objetos y gestionar inventario, con almacenamiento persistente de partidas.

Características
✅ Mover al personaje por la mazmorra usando comandos (W A S D)
✅ Combate con enemigos y jefe final.
✅ Cofres, trampas y loot interactivo.
✅ Inventario para almacenar objetos y usarlos estratégicamente.
✅ Guardado y carga de partidas en archivo JSON.
✅ Menú principal y comandos de consola intuitivos.

Instalación y Uso:

Ejecutar el programa: python main.py
Seleccionar opción en el menú principal
Seguir las instrucciones de movimiento y combate
Guardar o cargar partida con los comandos save y load

Estructura de Datos
Player: Clase que almacena estado del jugador
hp, atk, defense, gold, level, exp
x, y → posición en la mazmorra
inventory → lista de objetos
Dungeon: Clase que representa el mapa
size → tamaño del mapa
grid → matriz que contiene el tipo de casilla (0: vacío, 1: enemigo, 2: cofre, 3: trampa, 4: jefe)
Enemy: Clase para enemigos
level, hp, atk, defense

Funciones Principales

main(): Controla el flujo principal del juego y el menú
guardar_partida(player, dungeon): Guarda el estado actual en save.json
cargar_partida(): Carga el estado guardado desde save.json
show_stats(player): Muestra estadísticas actuales del jugador
handle_event(player, tile): Gestiona eventos al moverse (combate, cofres, trampas, jefe)
combat(player, enemy): Lógica de combate jugador vs enemigo
loot_event(player): Gestiona cofres y objetos
trap_event(player): Aplica daño de trampas
boss_fight(player): Maneja el enfrentamiento final con el jefe
