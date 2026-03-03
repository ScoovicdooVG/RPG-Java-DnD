# El Despertar de los Heroes (Version 2.0.1)

Un videojuego RPG por turnos desarrollado en Java puro, utilizando Swing para la interfaz grafica. Combina una arquitectura orientada a objetos robusta con mecanicas clasicas de juegos de rol de mesa (estilo D&D), incluyendo tiradas de dados (D20), gestion de inventarios, sistema de clases y progresion de personajes.

## Caracteristicas Principales

* Sistema de Clases y Recursos: Tres clases jugables con mecanicas y fuentes de poder unicas. 
  - Guerrero: Especialista en resistencia y daño fisico. Utiliza puntos de Energia para ejecutar su "Golpe Demoledor".
  - Picaro: Combatiente agil y letal. Consume Energia para realizar un "Ataque Furtivo" basado en su destreza.
  - Mago: Maestro de las artes arcanas. Depende de sus puntos de Mana (MP) para lanzar una "Bola de Fuego" capaz de infligir daño continuo por quemadura.
* Equipamiento Restringido por Clase: El inventario cuenta con una validacion estricta. Las armas y armaduras solo pueden ser equipadas si coinciden con la especialidad del heroe (ej. los Magos solo pueden equipar tunicas, orbes y bastones; los Guerreros dominan cotas de malla y hachas; los Picaros requieren equipo ligero y espadas gemelas).
* Nuevo Sistema de Consumibles: Ampliacion del botin y la tienda con objetos especificos para la gestion de recursos y estados. Incluye pociones de curacion (pequeña, mediana, grande), Pociones de Mana exclusivas para Magos, Bebidas Energeticas para Guerreros y Picaros, Antidotos para curar el envenenamiento y Cremas para aliviar quemaduras.
* Retroalimentacion Visual en Tiempo Real: Interfaz grafica "Dark Mode" con una consola de eventos y un sistema de barras dobles (JProgressBar) que monitorea los Puntos de Vida (HP) y los Puntos de Magia/Energia (MP) de todo el grupo de forma dinamica.
* Persistencia de Datos: Sistema de guardado y carga de partidas mediante serializacion de objetos (partida.sav) y un "Bestiario" global automatizado (bestiario.dat).
* Motor de Audio Avanzado: Implementacion del patron de diseño Singleton (GestorAudio) para manejar la musica de fondo en bucle y la superposicion de efectos de sonido.
* Economia y Gestion de Inventario: Sistema completo con control de peso en mochila, transferencia de objetos entre miembros del grupo, menu inteligente de uso de consumibles y una tienda funcional para interactuar con la economia del juego.

## Arquitectura y Diseño (Ingenieria de Software)

El proyecto esta estructurado utilizando principios solidos de Programacion Orientada a Objetos (POO):
* Herencia y Polimorfismo: Una clase base Entidad que define atributos y modificadores de estadisticas (Fuerza, Destreza, Constitucion), de la cual heredan Jugador y Monstruo.
* Manejo de Eventos y Multihilos: Uso de Timer para gestionar el ritmo de los ataques enemigos creando pausas naturales, y ActionListeners para las interacciones del usuario en los menus Swing.
* Sanitizacion y Seguridad de Datos: Implementacion de normalizacion de cadenas de texto (.toLowerCase() y remocion de tildes) para garantizar comparaciones logicas seguras, prevencion de NullPointerExceptions y compatibilidad total multiplataforma.

## Requisitos del Sistema

* Java Runtime Environment (JRE): Version 1.8 (Java 8) o superior.
* Sistema Operativo: Windows, macOS o Linux.

## Como Jugar

1. Descargar el archivo DespertarHeroes_v2.0.1.zip (o el archivo .jar y la carpeta assets de forma manual).
2. Extraer los archivos. Asegurarse de que la carpeta assets (que contiene imagenes y sonidos) este ubicada exactamente en el mismo directorio que el archivo .jar.
3. Ejecutar el juego haciendo doble clic sobre el archivo .jar.
4. En caso de ejecutarlo por consola para ver logs de depuracion, utilizar el comando en la terminal:
   java -jar DespertarHeroes.jar