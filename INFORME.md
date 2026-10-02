# Informe de Proyecto: Cruz de Guía Sevilla

## 1. Idea del proyecto y por qué lo elegimos

La aplicación se llamará Cruz de Guía Sevilla. Es una app para el móvil que junta toda la información de las hermandades de Sevilla: sus horarios, su historia, las fotos de los pasos, cuándo son las misas y hasta la tienda de recuerdos. 

La información será 100% real porque trabajaremos codo con codo con el Consejo General de Hermandades y Cofradías. Así evitamos los rumores y las mentiras que a veces se leen en las redes sociales cuando estás en la calle.

Para programarla, usaremos dos métodos de trabajo combinados:

* El método de la Espiral: Nos sirve para pensar en los problemas antes de que ocurran. En Sevilla, el mayor peligro es la lluvia. Si empieza a llover, todo el mundo abre la app a la vez para saber qué pasa, y la app se puede romper. Este método nos obliga a preparar la app para ese momento desde el primer día.
* El método Scrum: Nos sirve para trabajar en equipo por bloques de dos semanas. Así, en las primeras dos semanas hacemos los mapas básicos, y en las siguientes añadimos cosas más difíciles como la tienda o los avisos de última hora.

## 2. Pasos para hacer la app (Fases)

Haremos el proyecto en tres pasos fundamentales dentro del ciclo de vida del software:

1. Paso 1 (Hablar y planificar): Nos reunimos con las hermandades para ver qué información nos dejan poner. También planeamos qué hacer si hay mal tiempo y los móviles se quedan sin cobertura en medio de la calle.
2. Paso 2 (Organizar y revisar): Los secretarios de las hermandades escribirán los datos de su cofradía, pero el Consejo de Sevilla tendrá que revisar y dar el visto bueno (pulsar un botón de "Aceptar") antes de que la gente pueda verlo en la app.
3. Paso 3 (Escribir el código): Nos ponemos a programar. Usaremos páginas web normales para el ordenador del Consejo y código especial para que la app funcione bien en los teléfonos móviles.

## 3. Quién va a usar la app y cómo se adapta (HCI)

La app la va a usar todo el mundo, por eso el diseño de las pantallas tiene que adaptarse a cada edad usando los principios de la Interacción Persona-Ordenador (HCI):

* Niños y jóvenes: Como quieren todo rápido, les pondremos mapas interactivos que se muevan fácil y dibujos con los colores reales de las túnicas de los nazarenos.
* Personas mayores (Ancianos): Como les cuesta más usar el móvil, la app tendrá un "Modo Fácil" con las letras muy grandes, botones gigantes y colores muy fuertes para que se vea bien en la calle aunque le dé todo el sol de la tarde.
* Uso con una mano: Cuando estás en la calle viendo una cofradía, suele haber mucha gente y a lo mejor llevas un paraguas o una silla en la otra mano. Por eso, los botones más importantes estarán abajo del todo para que llegues fácil con el dedo pulgar.

## 4. Lista de cosas que tiene y cómo funciona la app

### Cosas que HACE la app (Requisitos Funcionales)

* RF1. Ficha de la hermandad: Enseña el nombre, el año en que se fundó, las fotos de los pasos, su historia y quién es el Hermano Mayor actual e histórico.
* RF2. Calendario: Muestra los días y las horas de las misas, los cultos de todo el año y las misiones parroquiales.
* RF3. Tienda de recuerdos: Permite ver los productos de la hermandad (llaveros, medallas, libros) y reservarlos desde el teléfono.
* RF4. Avisos de tiempo (Lluvia): El Consejo puede cambiar en un segundo el estado de la cofradía a: En su iglesia, En la calle, Refugiada en otra iglesia, Volviendo a prisa o Suspendida.
* RF5. Cambio de ruta en el mapa (Lluvia): Si empieza a llover y la cofradía cambia de camino para no mojarse, el mapa cambia el dibujo de la ruta solo en ese mismo instante de forma automática.

### Cómo DEBE COMPORTARSE la app (Requisitos No Funcionales)

* RNF6. Que se lea bien (Usabilidad): La pantalla tiene que usar colores muy claros y oscuros para que se lea perfectamente bajo la luz del sol en exteriores.
* RNF7. Que valga para todos los móviles (Portabilidad): Tiene que funcionar igual de rápida y suave tanto en teléfonos Android como en los iPhones de Apple, respetando la fluidez de cada sistema operativo.
* RNF8. Seguridad: Los secretarios del Consejo necesitarán una contraseña y un código enviado a su móvil (doble factor) para cambiar los datos, así nadie puede hackear el sistema ni poner información falsa.
* RNF9. Servidores fuertes (Lluvia / Escalabilidad): Si de repente empieza a llover y pasamos de tener 100 personas conectadas a tener 50.000, las computadoras de la app en la nube deben hacerse más potentes solas en menos de dos minutos para que la aplicación no se apague ni se caiga.
* RNF10. Funcionar sin internet (Modo Offline): Si las calles se llenan de paraguas y las líneas de teléfono se colapsan por la cantidad de gente, la app no se quedará en blanco. Mostrará los últimos horarios que se descargaron la última vez que el dispositivo tuvo conexión a internet.
