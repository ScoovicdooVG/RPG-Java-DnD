# El Despertar de los Héroes (Versión 2.0)

Un videojuego RPG por turnos desarrollado en Java puro, utilizando Swing para la interfaz gráfica. Combina una arquitectura orientada a objetos robusta con mecánicas clásicas de juegos de rol de mesa (estilo D&D), incluyendo tiradas de dados (D20), gestión de inventarios y progresión de personajes.

## Características Principales

* **Sistema de Combate Dinámico:** Peleas por turnos basadas en iniciativa. Incluye ataques básicos, habilidades especiales por clase (Guerrero, Mago, Pícaro) y estados alterados (Veneno, Quemadura).
* **Retroalimentación Visual en Tiempo Real:** Interfaz gráfica "Dark Mode" con una consola de eventos y barras de vida (`JProgressBar`) que cambian de color (Verde/Amarillo/Rojo) de manera dinámica al recibir daño o curación.
* **Persistencia de Datos:** * Sistema de guardado y carga de partidas mediante serialización de objetos (`partida.sav`).
  * "Bestiario" global automatizado que registra permanentemente los monstruos descubiertos usando `HashSet` (`bestiario.dat`).
* **Motor de Audio Avanzado:** Implementación del patrón de diseño **Singleton** (`GestorAudio`) para manejar la música de fondo en bucle y la superposición de efectos de sonido sin fugas de memoria.
* **Economía y Gestión de Recursos:** Sistema completo de inventario con control de peso, transferencia de objetos entre miembros del grupo y una tienda funcional para comprar/vender equipo.

## Arquitectura y Diseño

El proyecto está estructurado utilizando principios sólidos de Programación Orientada a Objetos (POO):
* **Herencia y Polimorfismo:** Una clase base `Entidad` que define atributos y modificadores de estadísticas (Fuerza, Destreza, Constitución), de la cual heredan `Jugador` y `Monstruo`.
* **Encapsulamiento:** Lógica de negocio separada de la interfaz de usuario.
* **Manejo de Eventos y Multihilos:** Uso de `Timer` para gestionar el ritmo de los ataques enemigos y `ActionListeners` para las interacciones del usuario.
* **Sanitización de Datos:** Limpieza activa de caracteres (UTF-8/ANSI) en la consola virtual para garantizar la compatibilidad multiplataforma.

## Requisitos del Sistema

* **Java Runtime Environment (JRE):** Versión 1.8 (Java 8) o superior.
* Sistema Operativo: Windows, macOS o Linux.

## Cómo Jugar

1. Descarga el archivo `DespertarHeroes.jar` y la carpeta `assets`.
2. Asegúrate de que la carpeta `assets` (que contiene imágenes y sonidos) esté ubicada exactamente en el mismo directorio que el archivo `.jar`.
3. Ejecuta el juego haciendo doble clic sobre `DespertarHeroes.jar`.
4. En caso de ejecutarlo por consola, utiliza el comando:
   `java -jar DespertarHeroes.jar`