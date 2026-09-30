Reconocimiento de Elementos en el Desarrollo de un Programa Informático

1. Introducción

El desarrollo de un programa informático pasa por diferentes fases desde que el programador escribe el código hasta que el ordenador puede ejecutarlo.

En esta actividad se explican los conceptos de código fuente, código objeto y código ejecutable. También se explican las fases que atraviesa un programa, incluyendo el análisis léxico, sintáctico y semántico, la generación de código intermedio, la optimización, la generación de código objeto o bytecode, el enlazado cuando corresponde y la ejecución.

Por último, se clasifican diferentes lenguajes de programación según su nivel de abstracción y su paradigma, y se analizan varios ejemplos para identificar si utilizan un paradigma imperativo o declarativo.

PARTE 1: ANÁLISIS TEÓRICO DE CONCEPTOS

1. Explicación de los conceptos básicos

1.1. Código fuente

El código fuente es el código que escribe el programador utilizando un lenguaje de programación. Está formado por instrucciones que permiten indicar al ordenador qué debe hacer.

Por ejemplo, en Java podemos tener:

public class Hola {
    public static void main(String[] args) {
        System.out.println("Hola");
    }
}

Este código es código fuente porque está escrito en un lenguaje de programación que puede leer y modificar el programador.

1.2. Código objeto

El código objeto es una representación del programa que se obtiene después de procesar y traducir el código fuente. Está más cerca del lenguaje máquina que el código fuente.

En lenguajes compilados como C, el compilador puede generar archivos de código objeto que posteriormente se utilizan para crear el programa ejecutable.

1.3. Código ejecutable

El código ejecutable es el código que está preparado para que el sistema pueda ejecutar el programa.

En un programa compilado, el código objeto puede combinarse con otras partes necesarias mediante el enlazado para obtener un archivo ejecutable.

Por ejemplo, en Windows puede ser un archivo .exe.

En Java el proceso es diferente. El código fuente .java se compila normalmente a bytecode, que se guarda en un archivo .class. Después, la JVM (Java Virtual Machine) ejecuta ese bytecode y lo adapta a la plataforma correspondiente.

2. Fases por las que pasa un programa

Desde que se escribe un programa hasta que se ejecuta, se realizan diferentes fases.

2.1. Escritura del código fuente

El programador escribe el programa utilizando un lenguaje de programación.

Por ejemplo:

int resultado = 5 + 3;

En esta fase tenemos el código fuente.

2.2. Análisis léxico

El análisis léxico consiste en analizar el código fuente y dividirlo en elementos básicos llamados tokens.

Por ejemplo:

int resultado = 5 + 3;

Se pueden identificar:

int: palabra reservada.

resultado: identificador.

=: operador de asignación.

5 y 3: números.

+: operador.

;: separador.

Esta fase permite reconocer los elementos que forman el programa.

2.3. Análisis sintáctico

El análisis sintáctico comprueba que los elementos del programa estén colocados siguiendo las reglas del lenguaje de programación.

Por ejemplo:

int resultado = 5 + 3;

tiene una estructura válida en Java.

Si se escribe una instrucción que no respeta las reglas de sintaxis del lenguaje, se produce un error de sintaxis.

2.4. Análisis semántico

El análisis semántico comprueba que las instrucciones tengan un significado correcto y que sean compatibles entre sí.

Por ejemplo:

int resultado = 5 + 3;

es correcto porque el resultado de la operación es compatible con el tipo int.

También se comprueban aspectos como los tipos de datos y el uso correcto de variables.

2.5. Generación de código intermedio

Después de analizar el programa, el compilador puede generar una representación intermedia del código.

El código intermedio es una representación situada entre el código fuente y el código que finalmente se ejecutará.

Su función es facilitar el proceso de traducción y permitir que el compilador pueda realizar transformaciones y optimizaciones antes de generar el código final.

En diferentes lenguajes y compiladores, esta representación puede tener distintas formas.

En Java, por ejemplo, el resultado de la compilación del código fuente es bytecode, almacenado normalmente en archivos .class. El bytecode es una representación intermedia diseñada para ser ejecutada por la JVM.

2.6. Optimización

La optimización consiste en realizar cambios en la representación del programa para intentar mejorar su funcionamiento sin cambiar el resultado que debe producir.

El compilador puede realizar optimizaciones para:

Reducir instrucciones innecesarias.

Mejorar el tiempo de ejecución.

Reducir el uso de memoria.

Eliminar operaciones que no son necesarias.

Por ejemplo, si una operación puede simplificarse sin cambiar el resultado, el compilador puede transformarla en una forma más eficiente.

La optimización se realiza antes de obtener el código final que será ejecutado.

2.7. Generación de código objeto o código final

Después de las fases anteriores, el compilador genera una representación que está más cerca del código que puede ejecutar la máquina.

En lenguajes como C, se puede generar código objeto, que posteriormente se utilizará para construir el ejecutable.

En Java, el compilador javac genera bytecode, que se almacena normalmente en archivos .class.

2.8. Enlazado

En determinados lenguajes compilados, el enlazado consiste en combinar el código objeto con otras partes necesarias, como bibliotecas, para crear el programa final.

Esta fase es habitual en lenguajes como C.

No todos los lenguajes realizan el proceso exactamente de la misma manera.

2.9. Código ejecutable

Después de completar los pasos necesarios, se obtiene el código preparado para ejecutar el programa.

En un sistema tradicional de compilación, el enlazado puede producir un archivo ejecutable.

Por ejemplo:

programa.exe

En Java, en cambio, se ejecuta el bytecode mediante la JVM, por lo que el proceso es diferente al de un ejecutable nativo tradicional.

2.10. Ejecución

Finalmente, el programa se ejecuta.

En un programa compilado de forma tradicional, el procesador ejecuta las instrucciones de código máquina correspondientes.

En Java, la JVM ejecuta el bytecode y puede interpretarlo o compilarlo durante la ejecución para adaptarlo al procesador y al sistema donde se está ejecutando.

2.11. Resumen de las fases

El proceso completo puede representarse de la siguiente manera:

Código fuente
      ↓
Análisis léxico
      ↓
Análisis sintáctico
      ↓
Análisis semántico
      ↓
Código intermedio
      ↓
Optimización
      ↓
Código objeto / bytecode
      ↓
Enlazado (cuando corresponda)
      ↓
Código ejecutable / programa preparado para ejecutarse
      ↓
Ejecución

Estas fases pueden variar según el lenguaje de programación, el compilador y la plataforma utilizada, pero representan de forma general el proceso de transformación de un programa desde el código escrito por el programador hasta su ejecución.

3. Clasificación de los lenguajes de programación

Los lenguajes de programación pueden clasificarse de diferentes maneras. En esta actividad se clasifican según su nivel de abstracción y según su paradigma de programación.

3.1. Nivel de abstracción

Lenguajes de alto nivel

Los lenguajes de alto nivel están más cerca de la forma de expresarse de las personas y son más fáciles de leer y escribir que los lenguajes de bajo nivel.

Ejemplos:

Java.

Python.

Java: utiliza una sintaxis que permite desarrollar aplicaciones sin trabajar directamente con las instrucciones del procesador.

Python: tiene una sintaxis sencilla y permite escribir programas de forma relativamente cercana al lenguaje humano.

Lenguajes de nivel medio

Los lenguajes de nivel medio permiten trabajar con elementos propios de lenguajes de alto nivel y también ofrecen mecanismos para trabajar con aspectos más cercanos al hardware.

Ejemplos:

C.

C++.

C: permite utilizar estructuras de alto nivel y también trabajar directamente con memoria mediante punteros.

C++: incorpora características de alto nivel, como la programación orientada a objetos, y también permite trabajar con recursos de bajo nivel.

Lenguajes de bajo nivel

Los lenguajes de bajo nivel están muy relacionados con la arquitectura del ordenador y con las instrucciones que puede ejecutar el procesador.

Ejemplos:

Ensamblador.

Lenguaje máquina.

Ensamblador: utiliza instrucciones simbólicas que representan operaciones del procesador.

Lenguaje máquina: utiliza instrucciones codificadas de una forma que el procesador puede ejecutar directamente.

4. Paradigmas de programación

4.1. Paradigma imperativo

En el paradigma imperativo se indica cómo realizar una tarea. El programa describe una serie de instrucciones y pasos que se deben ejecutar.

Ejemplos de lenguajes:

Java.

C.

Java: permite indicar instrucciones que se ejecutan en un determinado orden y modificar variables durante la ejecución.

C: permite crear programas mediante instrucciones, condiciones, bucles y modificaciones de datos.

Ejemplo

int total = 0;

for (int numero : numeros) {
    total = total + numero;
}

En este ejemplo se indican los pasos necesarios para obtener el total.

4.2. Paradigma declarativo

En el paradigma declarativo se indica qué resultado se quiere obtener, sin tener que especificar todos los pasos necesarios para conseguirlo.

Ejemplos de lenguajes:

SQL.

Prolog.

SQL: permite indicar qué información se quiere obtener de una base de datos sin indicar paso a paso cómo debe recorrer internamente los datos.

Prolog: permite expresar hechos y reglas para que el sistema pueda obtener resultados a partir de ellos.

Ejemplo

SELECT nombre
FROM empleados
WHERE edad > 30;

En este caso se indica qué información se quiere obtener: los nombres de los empleados mayores de 30 años.

PARTE 2: ACTIVIDAD PRÁCTICA Y DE ANÁLISIS

1. Identificación de paradigmas de programación

Fragmento 1

Descripción:

Un programa recorre una lista de números sumándolos uno por uno hasta obtener el total.

Paradigma: Imperativo.

Justificación:

Es imperativo porque se describen los pasos que debe realizar el programa. Primero recorre la lista y después suma los números uno por uno hasta obtener el resultado.

Se indica cómo realizar la operación.

Fragmento 2

Descripción:

Una consulta a una base de datos busca empleados mayores de 30 años y devuelve solo sus nombres.

Paradigma: Declarativo.

Justificación:

Es declarativo porque se indica qué información se quiere obtener: los nombres de los empleados que tienen más de 30 años.

No se explica cómo debe recorrer internamente la base de datos para conseguir ese resultado.

Se indica qué resultado se quiere obtener.

Fragmento 3

Descripción:

Un programa calcula el factorial de un número n, definiendo que el factorial de 0 es 1 y que, para números mayores, se multiplica el número por el factorial del número anterior.

Paradigma: Declarativo.

Justificación:

Se puede considerar declarativo porque la lógica se expresa mediante una definición recursiva del resultado:

factorial(0) = 1

factorial(n) = n * factorial(n - 1)

La descripción define la relación que debe cumplirse para obtener el resultado, en lugar de indicar una secuencia detallada de pasos mediante un bucle.

Fragmento 4

Descripción:

Un programa filtra productos con precios superiores a 10 dólares recorriendo una lista y comprobando cada producto uno por uno.

Paradigma: Imperativo.

Justificación:

Es imperativo porque se explica cómo realizar el proceso: recorrer la lista, comprobar cada producto y seleccionar los que tienen un precio superior a 10 dólares.

Se detallan los pasos que debe seguir el programa.

2. Actividad en grupo

Actividad cotidiana elegida: preparar una tortilla de patatas

Para comparar los enfoques imperativo y declarativo, se ha elegido la actividad cotidiana de preparar una tortilla de patatas.

2.1. Forma imperativa

En la forma imperativa se indican los pasos que hay que realizar:

Pelar las patatas.

Cortar las patatas en trozos pequeños.

Calentar aceite en una sartén.

Añadir las patatas a la sartén.

Cocinar las patatas hasta que estén blandas.

Sacar las patatas y escurrirlas.

Batir los huevos en un recipiente.

Mezclar las patatas con los huevos.

Calentar de nuevo la sartén.

Añadir la mezcla.

Cocinar la tortilla por un lado.

Darle la vuelta.

Cocinarla por el otro lado.

Retirar la tortilla cuando esté preparada.

En esta descripción se explica cómo realizar la actividad paso a paso.

2.2. Forma declarativa

En la forma declarativa no se detallan todos los pasos. Se indica principalmente el resultado que se quiere conseguir:

Obtener una tortilla de patatas preparada y lista para comer.

En este caso no se explica detalladamente cómo se deben cortar las patatas, cómo se deben cocinar o cómo se debe dar la vuelta a la tortilla.

Se indica el resultado final que se quiere conseguir.

2.3. Comparación entre el enfoque imperativo y declarativo

Aspecto

Imperativo

Declarativo

Qué indica

Cómo realizar la tarea

Qué resultado se quiere obtener

Forma de trabajo

Se detallan los pasos

Se define el resultado

Ejemplo

Pelar, cortar, cocinar, mezclar y dar la vuelta

Obtener una tortilla de patatas preparada

Control sobre el proceso

Mayor

Menor

Cantidad de instrucciones

Normalmente mayor

Normalmente menor

Ventaja principal

Permite controlar el orden de las acciones

Permite centrarse en el resultado

Desventaja principal

Puede requerir muchas instrucciones

No detalla cómo se realiza cada paso

Ventajas del enfoque imperativo

Permite controlar detalladamente el proceso.

Indica el orden de las acciones.

Es útil cuando necesitamos saber exactamente qué pasos se deben realizar.

Facilita controlar cada operación del programa.

Desventajas del enfoque imperativo

Puede necesitar muchas instrucciones.

El código puede ser más largo.

El programador tiene que describir muchos detalles del proceso.

Ventajas del enfoque declarativo

Permite centrarse en el resultado que se quiere conseguir.

Puede necesitar menos instrucciones.

Oculta detalles internos que no son necesarios para el usuario.

Desventajas del enfoque declarativo

Se tiene menos control directo sobre los pasos internos.

Para algunas tareas puede ser necesario conocer cómo funciona internamente el sistema.

El resultado depende de que el lenguaje o sistema sepa cómo realizar lo que se ha solicitado.

3. Conclusiones

En esta actividad se han estudiado diferentes elementos relacionados con el desarrollo de programas informáticos.

Se ha aprendido que el código fuente es el código escrito por el programador, mientras que el código objeto es una representación obtenida después del procesamiento del código fuente y el código ejecutable es el que está preparado para ejecutar el programa.

También se han estudiado las diferentes fases del procesamiento de un programa: análisis léxico, análisis sintáctico, análisis semántico, generación de código intermedio, optimización, generación de código objeto o bytecode, enlazado cuando corresponde y ejecución.

Además, se han clasificado los lenguajes según su nivel de abstracción en alto, medio y bajo, y se han diferenciado los paradigmas imperativo y declarativo.

Finalmente, mediante los ejemplos prácticos se ha comprobado que el paradigma imperativo se centra en explicar cómo realizar una tarea, mientras que el paradigma declarativo se centra principalmente en indicar qué resultado se quiere obtener.
