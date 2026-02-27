#Java RPG: El Despertar de los Héroes
Este es un juego de rol de consola desarrollado en Java. El objetivo es guiar a un grupo de aventureros a través de diversas zonas, mejorar sus estadísticas mediante el equipamiento y derrotar al Rey Demonio al alcanzar el nivel de experiencia requerido.

##Mecánicas de Juego
* Exploración: Se realizan tiradas de Sabiduria para detectar tesoros ocultos o generar encuentros con monstruos aleatorios.

* Combate por Turnos: El orden de actuación se determina mediante un sistema de Iniciativa. Las acciones disponibles incluyen atacar, utilizar pociones de curación o pasar el turno realizando una tirada de salvación de Destreza.

* Gestión de Inventario: El sistema incluye un límite de carga basado en el Peso (kg). Tanto el oro como el equipo recolectado ocupan espacio en la mochila.

* Economía: A través de la Tienda de Droh'k Azher, el usuario puede adquirir suministros o vender objetos del botín para obtener oro.

* Equipamiento: Permite gestionar Armas y Armaduras que modifican directamente los atributos de Fuerza y Defensa del personaje.

##Sistema de Guardado y Carga
El progreso se almacena mediante la serialización de objetos en un archivo local denominado partida.sav.

* Guardar: Se debe seleccionar la opción 5 en el menú principal para persistir los datos antes de cerrar la aplicación.

* Cargar: El sistema verifica la existencia del archivo de guardado al iniciar. Si existe, permite al usuario retomar la aventura desde el último estado guardado.

##Bestiario
Los enemigos han sido categorizados según su dificultad de encuentro:

* Nivel Bajo: Slime, Zombie, Esqueleto, Goblin.

* Nivel Medio: Orco, Huargo, Hobgoblin, Gárgola.

* Nivel Alto: Oso Lechuza, Dragón Blanco Joven.

* Jefe Final: El Rey Demonio. Este enemigo aparece como encuentro mandatorio una vez que un jugador alcanza el Nivel 5.

##Créditos y Atribuciones
* Desarrollador: Víctor García / Scoovicdoo.

* Inspiración: Las estadísticas y nomenclaturas de los monstruos están basadas en el Manual de Monstruos de D&D 5ta Edición (2014).

* Tecnología: El proyecto ha sido desarrollado íntegramente utilizando el lenguaje de programación Java.

##Instrucciones de Ejecución
* Descargar el archivo compilado con extensión .jar.

* Abrir una terminal o consola de comandos en el directorio donde se encuentre el archivo.

* Ejecutar el siguiente comando: java -jar MiJuegoRPG.jar.