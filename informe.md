# Reconocimiento de Elementos en el Desarrollo de un Programa Informático

## 1. Introducción

El desarrollo de un programa informático pasa por diferentes fases desde que el programador escribe el código hasta que el ordenador puede ejecutarlo.

En esta actividad se explican los conceptos de código fuente, código objeto y código ejecutable. También se explican las fases que atraviesa un programa y se clasifican diferentes lenguajes de programación según su nivel de abstracción y su paradigma.

Por último, se analizan varios ejemplos para identificar si utilizan un paradigma imperativo o declarativo y se compara la forma imperativa y declarativa de realizar una actividad cotidiana.

---

# PARTE 1: ANÁLISIS TEÓRICO DE CONCEPTOS

## 1. Explicación de los conceptos básicos

### 1.1. Código fuente

El **código fuente** es el código que escribe el programador utilizando un lenguaje de programación. Está formado por instrucciones que permiten indicar al ordenador qué debe hacer.

Por ejemplo, en Java podemos tener:

```java
public class Hola {
    public static void main(String[] args) {
        System.out.println("Hola");
    }
}
```

Este código es código fuente porque está escrito en un lenguaje de programación que puede entender y modificar el programador.

El código fuente es la primera parte del proceso de desarrollo de un programa.

### 1.2. Código objeto

El **código objeto** es el resultado que se obtiene después de que el código fuente haya sido procesado por un compilador.

El código objeto está en una forma más cercana al lenguaje que puede procesar el ordenador, pero todavía puede necesitar otros pasos para convertirse en un programa ejecutable completo.

Por ejemplo, cuando se compila un programa escrito en un lenguaje como C, el compilador puede generar un archivo de código objeto.

### 1.3. Código ejecutable

El **código ejecutable** es el código que ya está preparado para que el sistema pueda ejecutar el programa.

En un programa compilado, el código objeto puede combinarse con otras partes necesarias mediante el enlazado para crear un archivo ejecutable.

Un ejemplo sería un archivo `.exe` en Windows.

En el caso de Java, el funcionamiento es diferente: el código fuente `.java` se compila normalmente a **bytecode**, que se guarda en un archivo `.class`. Después, la **JVM (Java Virtual Machine)** interpreta o compila ese bytecode durante la ejecución para que pueda ejecutarse en el ordenador.

---

## 2. Fases por las que pasa un programa

Desde que se escribe un programa hasta que se ejecuta, se realizan diferentes procesos.

### 2.1. Escritura del código fuente

El programador escribe el programa utilizando un lenguaje de programación.

Por ejemplo:

```java
int resultado = 5 + 3;
```

En esta fase tenemos el código fuente.

### 2.2. Análisis léxico

El análisis léxico consiste en analizar el código y dividirlo en elementos básicos llamados **tokens**.

Por ejemplo:

```java
int resultado = 5 + 3;
```

Se pueden identificar elementos como:

- `int`: palabra reservada.
- `resultado`: identificador.
- `=`: operador de asignación.
- `5` y `3`: números.
- `+`: operador.
- `;`: separador.

El análisis léxico permite comprobar que los elementos utilizados pertenecen al lenguaje.

### 2.3. Análisis sintáctico

El análisis sintáctico comprueba que los elementos están colocados siguiendo las reglas del lenguaje.

Por ejemplo, en Java:

```java
int resultado = 5 + 3;
```

tiene una estructura válida.

En cambio, si se escribe una instrucción con una estructura que no cumple las reglas del lenguaje, se produce un error de sintaxis.

### 2.4. Análisis semántico

El análisis semántico comprueba que el significado de las instrucciones sea correcto.

Por ejemplo:

```java
int resultado = 5 + 3;
```

es correcto porque el resultado de la operación es compatible con el tipo `int`.

Sin embargo, una operación que intente asignar un tipo de dato incompatible puede producir un error semántico o de tipos.

### 2.5. Compilación y generación de código

Una vez analizado el programa, el compilador transforma el código fuente en otra representación.

En lenguajes compilados como C, normalmente se genera código objeto que posteriormente puede utilizarse para crear el ejecutable.

En Java, el compilador `javac` transforma el código fuente `.java` en **bytecode**, almacenado normalmente en un archivo `.class`.

### 2.6. Enlazado

En los programas que utilizan código objeto, el enlazador puede unir diferentes partes del programa y las bibliotecas necesarias.

El resultado puede ser un programa ejecutable.

### 2.7. Ejecución

Finalmente, el programa se ejecuta.

En un programa tradicional compilado, el procesador ejecuta las instrucciones correspondientes al código máquina.

En Java, la JVM ejecuta el bytecode y lo adapta a la plataforma en la que se está ejecutando el programa.

### Resumen del proceso

```text
Código fuente
      ↓
Análisis léxico
      ↓
Análisis sintáctico
      ↓
Análisis semántico
      ↓
Compilación
      ↓
Código objeto / bytecode
      ↓
Enlazado (cuando corresponda)
      ↓
Código ejecutable
      ↓
Ejecución
```

---

# 3. Clasificación de los lenguajes de programación

Los lenguajes de programación pueden clasificarse de diferentes maneras. En esta actividad se clasifican según su **nivel de abstracción** y según su **paradigma de programación**.

## 3.1. Nivel de abstracción

### Lenguajes de alto nivel

Los lenguajes de alto nivel están más cerca de la forma de expresarse de las personas y son más fáciles de leer y escribir que los lenguajes de bajo nivel.

**Ejemplos:**

- Java.
- Python.

**Java:** utiliza una sintaxis relativamente sencilla y permite desarrollar aplicaciones sin tener que trabajar directamente con las instrucciones del procesador.

**Python:** utiliza una sintaxis sencilla y permite escribir programas de forma bastante cercana al lenguaje humano.

### Lenguajes de nivel medio

Los lenguajes de nivel medio permiten trabajar con elementos de alto nivel, pero también ofrecen posibilidades para trabajar con aspectos más cercanos al hardware.

**Ejemplos:**

- C.
- C++.

**C:** permite trabajar con estructuras propias de lenguajes de alto nivel y también con memoria y direcciones mediante punteros.

**C++:** incorpora características de alto nivel, como la programación orientada a objetos, pero también permite trabajar de forma cercana al hardware.

### Lenguajes de bajo nivel

Los lenguajes de bajo nivel están muy relacionados con la arquitectura del ordenador y con las instrucciones que puede ejecutar el procesador.

**Ejemplos:**

- Ensamblador.
- Lenguaje máquina.

**Ensamblador:** utiliza instrucciones simbólicas que representan operaciones del procesador.

**Lenguaje máquina:** está formado por instrucciones representadas mediante códigos que el procesador puede ejecutar directamente.

---

# 4. Paradigmas de programación

## 4.1. Paradigma imperativo

En el paradigma imperativo se indica **cómo realizar una tarea**. El programa describe una serie de instrucciones y pasos que se deben ejecutar.

**Ejemplos de lenguajes:**

- Java.
- C.

**Java:** permite indicar instrucciones que se ejecutan en un determinado orden y modificar variables durante la ejecución.

**C:** permite crear programas mediante instrucciones, condiciones, bucles y modificaciones de datos.

### Ejemplo

```java
int total = 0;

for (int numero : numeros) {
    total = total + numero;
}
```

En este ejemplo se indican los pasos que se deben realizar para obtener el total.

---

## 4.2. Paradigma declarativo

En el paradigma declarativo se indica **qué resultado se quiere obtener**, sin tener que especificar todos los pasos necesarios para conseguirlo.

**Ejemplos de lenguajes:**

- SQL.
- Prolog.

**SQL:** permite indicar qué información se quiere obtener de una base de datos sin indicar paso a paso cómo debe recorrer internamente los datos.

**Prolog:** permite expresar hechos y reglas para que el sistema pueda obtener resultados a partir de ellos.

### Ejemplo

```sql
SELECT nombre
FROM empleados
WHERE edad > 30;
```

En este caso se indica qué información se quiere obtener: los nombres de los empleados mayores de 30 años.

---

# PARTE 2: ACTIVIDAD PRÁCTICA Y DE ANÁLISIS

## 1. Identificación de paradigmas de programación

### Fragmento 1

**Descripción:**

Un programa recorre una lista de números sumándolos uno por uno hasta obtener el total.

**Paradigma: Imperativo.**

**Justificación:**

Es imperativo porque se describen los pasos que debe realizar el programa. Primero recorre la lista y después suma los números uno por uno hasta obtener el resultado.

Se indica **cómo** realizar la operación.

---

### Fragmento 2

**Descripción:**

Una consulta a una base de datos busca empleados mayores de 30 años y devuelve solo sus nombres.

**Paradigma: Declarativo.**

**Justificación:**

Es declarativo porque se indica qué información se quiere obtener, es decir, los nombres de los empleados que tienen más de 30 años.

No se explica cómo debe recorrer internamente la base de datos para conseguir ese resultado.

Se indica **qué** resultado se quiere obtener.

---

### Fragmento 3

**Descripción:**

Un programa calcula el factorial de un número `n`, definiendo que el factorial de 0 es 1 y que, para números mayores, se multiplica el número por el factorial del número anterior.

**Paradigma: Declarativo.**

**Justificación:**

Se puede considerar declarativo porque la lógica se expresa mediante una definición recursiva del resultado:

- `factorial(0) = 1`
- `factorial(n) = n * factorial(n - 1)`

La descripción define la relación que debe cumplirse para obtener el resultado, en lugar de indicar una secuencia detallada de pasos mediante un bucle.

---

### Fragmento 4

**Descripción:**

Un programa filtra productos con precios superiores a 10 dólares recorriendo una lista y comprobando cada producto uno por uno.

**Paradigma: Imperativo.**

**Justificación:**

Es imperativo porque se explica cómo realizar el proceso: recorrer la lista, comprobar cada producto y seleccionar los que tienen un precio superior a 10 dólares.

Se detallan los pasos que debe seguir el programa.

---

## 2. Actividad en grupo

### Actividad cotidiana elegida: preparar una tortilla de patatas

Para comparar los enfoques imperativo y declarativo, se ha elegido la actividad cotidiana de preparar una tortilla de patatas.

---

## 2.1. Forma imperativa

En la forma imperativa se indican los pasos que hay que realizar:

1. Pelar las patatas.
2. Cortar las patatas en trozos pequeños.
3. Calentar aceite en una sartén.
4. Añadir las patatas a la sartén.
5. Cocinar las patatas hasta que estén blandas.
6. Sacar las patatas y escurrirlas.
7. Batir los huevos en un recipiente.
8. Mezclar las patatas con los huevos.
9. Calentar de nuevo la sartén.
10. Añadir la mezcla.
11. Cocinar la tortilla por un lado.
12. Darle la vuelta.
13. Cocinarla por el otro lado.
14. Retirar la tortilla cuando esté preparada.

En esta descripción se explica **cómo** realizar la actividad paso a paso.

---

## 2.2. Forma declarativa

En la forma declarativa no se detallan todos los pasos. Se indica principalmente el resultado que se quiere conseguir:

> Obtener una tortilla de patatas preparada y lista para comer.

En este caso no se explica detalladamente cómo se deben cortar las patatas, cómo se deben cocinar o cómo se debe dar la vuelta a la tortilla.

Se indica el **resultado final que se quiere conseguir**.

---

## 2.3. Comparación entre el enfoque imperativo y declarativo

| Aspecto | Imperativo | Declarativo |
|---|---|---|
| Qué indica | Cómo realizar la tarea | Qué resultado se quiere obtener |
| Forma de trabajo | Se detallan los pasos | Se define el resultado |
| Ejemplo | Pelar, cortar, cocinar, mezclar y dar la vuelta | Obtener una tortilla de patatas preparada |
| Control sobre el proceso | Mayor | Menor |
| Cantidad de instrucciones | Normalmente mayor | Normalmente menor |
| Ventaja principal | Permite controlar el orden de las acciones | Permite centrarse en el resultado |
| Desventaja principal | Puede requerir muchas instrucciones | No detalla cómo se realiza cada paso |

### Ventajas del enfoque imperativo

- Permite controlar detalladamente el proceso.
- Indica el orden de las acciones.
- Es útil cuando necesitamos saber exactamente qué pasos se deben realizar.
- Facilita controlar cada operación del programa.

### Desventajas del enfoque imperativo

- Puede necesitar muchas instrucciones.
- El código puede ser más largo.
- El programador tiene que describir muchos detalles del proceso.

### Ventajas del enfoque declarativo

- Permite centrarse en el resultado que se quiere conseguir.
- Puede necesitar menos instrucciones.
- Oculta detalles internos que no son necesarios para el usuario.

### Desventajas del enfoque declarativo

- Se tiene menos control directo sobre los pasos internos.
- Para algunas tareas puede ser necesario conocer cómo funciona internamente el sistema.
- El resultado depende de que el lenguaje o sistema sepa cómo realizar lo que se ha solicitado.

---

# 3. Conclusiones

En esta actividad se han estudiado diferentes elementos relacionados con el desarrollo de programas informáticos.

Se ha aprendido que el **código fuente** es el código escrito por el programador, mientras que el **código objeto** es una representación obtenida después del procesamiento del código fuente y el **código ejecutable** es el que está preparado para ejecutar el programa.

También se han estudiado diferentes fases del procesamiento de un programa, como el análisis léxico, el análisis sintáctico, el análisis semántico y la compilación.

Además, se han clasificado los lenguajes según su nivel de abstracción en alto, medio y bajo. También se han diferenciado los paradigmas imperativo y declarativo.

Finalmente, mediante los ejemplos prácticos se ha comprobado que el paradigma imperativo se centra en explicar **cómo** realizar una tarea, mientras que el paradigma declarativo se centra principalmente en indicar **qué** resultado se quiere obtener.
