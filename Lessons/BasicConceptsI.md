# Fundamentos del Diseño de Software

---

## Objetivo
Entender los conceptos fundamentales del diseño de software, incluyendo la definición de modelos, sistemas, y sistemas de información. Se discutirá la importancia del diseño de software, los problemas comunes que se enfrentan, y se explorarán ejemplos prácticos en Java para ilustrar estos conceptos.


## 1. Definiciones Básicas

### 1.1 ¿Qué es el Diseño de Software?

Hay muchas definiciones de diseño de software, cada una con un enfoque diferente. La palabra *diseño* es a la vez verbo y sustantivo, lo que aumenta la ambigüedad, ya que puede referirse tanto a un proceso (diseñar) como al resultado de este proceso (un diseño). La definición práctica de diseño de software (el proceso) es *la construcción de abstracciones de datos y computación y la organización de estas abstracciones en una aplicación de software funcional*. Al principio puede parecer demasiado restrictivo, pero si tenemos en cuenta todo lo que puede significar el término abstracción (variables, clases, objetos, etc.), vemos que tenemos bastante flexibilidad para interpretar lo que significa el diseño de software.

<center>

[![Software Design](https://img.youtube.com/vi/Fi3_BjVzpqk/hqdefault.jpg)](https://www.youtube.com/watch?v=Fi3_BjVzpqk)

</center>

#### Espacio de Diseño

En la práctica, el proceso de diseño consiste esencialmente en tomar decisiones. *¿Usamos una lista o una pila? ¿Qué servicios debe ofrecer esta interfaz? ¿Dónde debe gestionarse el error?* Considerar el diseño como una toma de decisiones nos lleva al concepto de **espacio de diseño**. Un espacio de diseño puede imaginarse como un espacio geométrico n-dimensional en el que cada dimensión corresponde a un atributo de calidad del diseño. Los atributos típicos de la calidad del diseño de software son la *comprensibilidad*, la *reutilización* y la *facilidad de implementación*. Dentro de este espacio de diseño, cada decisión de diseño específica (o conjunto coherente de decisiones) corresponde a una coordenada en el espacio que representa la consecuencia de la decisión.

<p align="center">
  <img src="https://raw.githubusercontent.com/prmr/SoftwareDesign/master/modules/figures/m01-DesignSpace.png" alt="Sublime's custom image" width=90%/>
</p>

Otros factor importante esw la *robustez* (resistencia a los errores).

### 1.2 ¿Qué es un modelo?
Un modelo es una representación abstracta y simplificada de un sistema o proceso real. Los modelos se utilizan para entender, analizar y predecir el comportamiento de sistemas complejos sin necesidad de trabajar directamente con el sistema real.

<center>

[![Software Design](https://img.youtube.com/vi/uWuNfhDvZz8/hqdefault.jpg)](https://www.youtube.com/watch?v=uWuNfhDvZz8)

</center>


- **Ejemplo**: En Java, una clase que representa una entidad del mundo real, como un `Empleado`, es un modelo. Contiene atributos como `nombre`, `edad`, `salario`, y métodos para manipular estos datos.

```java
public class Empleado {
    private String nombre;
    private int edad;
    private double salario;

    public Empleado(String nombre, int edad, double salario) {
        this.nombre = nombre;
        this.edad = edad;
        this.salario = salario;
    }

    // Métodos getter y setter
    public String getNombre() { return nombre; }
    public void setNombre(String nombre) { this.nombre = nombre; }

    public int getEdad() { return edad; }
    public void setEdad(int edad) { this.edad = edad; }

    public double getSalario() { return salario; }
    public void setSalario(double salario) { this.salario = salario; }
}
```

Complemento: [What is a Model? ](https://www.youtube.com/watch?v=OKA4_J5yeoU)

### 1.3 ¿Qué es diseño de software?
El diseño de software es el proceso de definir la arquitectura, los componentes, las interfaces y otros aspectos de un sistema de software. Este proceso es crucial para garantizar que el software sea eficiente, mantenible y cumpla con los requisitos del usuario.

- **Ejemplo**: Diseñar un sistema que gestione las operaciones de una biblioteca. Aquí, el diseño incluye la definición de las clases `Libro`, `Usuario`, `Préstamo`, y sus interacciones.

### 1.4 ¿Qué es un sistema?
Un sistema es un conjunto de componentes interrelacionados que trabajan juntos para lograr un objetivo común. En informática, un sistema puede ser un conjunto de software y hardware que interactúan para realizar una tarea específica.

<center>

[![Software Design](https://img.youtube.com/vi/Fd-zhGXgHUs/hqdefault.jpg)](https://www.youtube.com/watch?v=Fd-zhGXgHUs)

</center>

- **Ejemplo**: Un sistema de gestión de inventarios en un almacén, que incluye bases de datos, aplicaciones de software y dispositivos de hardware.

Complemento: [Systems Thinking! ](https://www.youtube.com/watch?v=GPW0j2Bo_eY)

### 1.5 ¿Qué es un sistema de información?
Un sistema de información es un tipo de sistema que recopila, procesa, almacena y distribuye información para apoyar la toma de decisiones y el control en una organización.

- **Ejemplo**: Un sistema de gestión académica que maneja los datos de estudiantes, cursos, y calificaciones.


## 2. Problemas en el Diseño de Software

### 2.1 Complejidad
El software es inherentemente complejo, y a medida que los sistemas crecen, su complejidad aumenta, lo que hace más difícil su mantenimiento y evolución.

- **Ejemplo**: Un sistema de comercio electrónico que necesita integrar pasarelas de pago, gestión de inventarios, y servicio al cliente. La complejidad radica en garantizar que todos estos subsistemas funcionen correctamente y se integren bien.

### 2.2 Escalabilidad
Diseñar software que pueda crecer en capacidad para manejar más usuarios, transacciones, o datos es un reto significativo.

- **Ejemplo**: Un sitio web de noticias que debe manejar picos de tráfico durante eventos importantes. Si no está bien diseñado, el sistema podría fallar bajo alta carga.

### 2.3 Mantenibilidad
El software debe ser fácil de modificar y mejorar. Un diseño deficiente puede llevar a un "código espagueti", donde el código está tan entrelazado que es difícil de entender y cambiar.

- **Ejemplo**: Si el código de un sistema de nómina no está bien estructurado, agregar una nueva regla de cálculo de impuestos podría requerir cambios en múltiples lugares, aumentando el riesgo de errores.

### 2.4 Seguridad
Los sistemas de software deben estar diseñados para resistir ataques y proteger la integridad y confidencialidad de los datos.

- **Ejemplo**: Un sistema bancario que debe proteger las transacciones financieras y los datos de los clientes frente a accesos no autorizados.

### 2.5 Otros

- Falta de documentación: Sin una adecuada documentación, mantener y evolucionar el software se vuelve difícil.
- Incompatibilidad de requisitos: A veces, los requisitos pueden ser conflictivos o cambiantes, lo que complica el proceso de diseño.

## 3. Discusión 


¿Cómo influyen los problemas mencionados en el éxito de un proyecto de software? Reflexiona sobre un proyecto en el que has trabajado y cómo el diseño afectó el resultado.

## 4. Ejercicios

### 1. Identificación de Modelos en Sistemas Reales

Objetivo: Reconocer y definir modelos en sistemas de software existentes.

**Instrucciones:**

1. **Describir el Modelo:** Elige un sistema de software con el que estés familiarizado (por ejemplo, una aplicación bancaria, un sistema de gestión de estudiantes, o una tienda en línea).
2. **Identificar Clases:** Define al menos tres clases que formarían parte del modelo de este sistema. Describe brevemente los atributos y métodos de cada clase.
3. **Relacionar Clases:** Explica cómo estas clases interactúan entre sí dentro del sistema.
4. **Diagrama UML:** Dibuja un diagrama UML de clases que represente el modelo.

**Ejemplo**: Para una tienda en línea, las clases podrían ser `Producto`, `Cliente`, y `Orden`. Describe cómo `Cliente` puede realizar una `Orden` que contiene múltiples `Productos`.


### 2. Problemas Comunes en el Diseño de Software

Lee un caso de estudio sobre un proyecto de software que enfrentó problemas debido a un mal diseño (puedes utilizar ejemplos reales o ficticios). Identifica y analiza los problemas de diseño que llevaron al fracaso o a los desafíos en el proyecto.

**Tareas:**
- Identifica los problemas de diseño en el caso de estudio.
- Propón soluciones alternativas que podrían haberse implementado.
- Reflexiona sobre cómo estos problemas pueden evitarse en futuros proyectos.

**Objetivo:**
Reconocer y analizar problemas comunes en el diseño de software.


### 3.  Diseño de un Sistema de Información

Diseña un sistema de información para una pequeña biblioteca que permita gestionar préstamos de libros, devoluciones, y el registro de usuarios. Define las clases necesarias y cómo interactuarán entre sí.

**Tareas:**
- Define las clases `Libro`, `Usuario`, `Préstamo`, y cualquier otra que consideres relevante.
- Especifica los métodos que cada clase deberá implementar.
- Describe cómo las clases interactuarán para gestionar un préstamo de libro.
- Dibuja un diagrama UML para visualizar el sistema de información.

**Objetivo:**
Aplicar el concepto de sistema de información a un escenario realista y estructurado.

#### 4. Análisis y Diseño de un Sistema

Dado un conjunto de requisitos, diseña un sistema para gestionar un pequeño supermercado. El sistema debe permitir la gestión de productos, clientes, y ventas.

**Tareas:**
- Define las clases necesarias (`Producto`, `Cliente`, `Venta`, etc.).
- Especifica las relaciones entre las clases.
- Desarrolla un diagrama UML para representar el diseño del sistema.
- Escribe pseudocódigo para un método que permita realizar una venta y actualizar el inventario.

**Objetivo:**
Ejercitar la capacidad de diseñar un sistema completo a partir de requisitos dados.

## Conclusión

El diseño de software es un pilar fundamental en la ingeniería de software, ya que define la estructura y el comportamiento de los sistemas que desarrollamos. A través de esta clase, hemos explorado conceptos clave como modelos, sistemas, y sistemas de información, así como los problemas comunes que pueden surgir durante el diseño de software. Estos conceptos no solo son teóricos, sino que tienen un impacto directo en la calidad, mantenibilidad y escalabilidad del software que construimos.

Al comprender y aplicar correctamente estos principios, estarás mejor preparado para enfrentar los desafíos que surgen en la creación de sistemas complejos. Un buen diseño de software no solo facilita el desarrollo inicial, sino que también asegura que el sistema pueda adaptarse y evolucionar con el tiempo, ofreciendo un valor sostenible y duradero.

Es esencial recordar que el diseño de software es un proceso iterativo, en el que aprenderás y mejorarás con la práctica y la experiencia. Cada decisión de diseño que tomes tiene implicaciones significativas para el futuro del proyecto, por lo que es crucial abordarlo con cuidado, considerando tanto las necesidades actuales como las posibles exigencias futuras.

Con este conocimiento como base, estarás mejor equipado para diseñar soluciones de software que no solo funcionen hoy, sino que también puedan crecer y adaptarse en el futuro.


## Referencias

- *Introduction to Software Design with Java*. Martin P. Robillard. Springer 2022, segunda edición.
- [Java Programming: Principles of Software Design](https://www.coursera.org/learn/java-programming-design-principles)


---

¿Hay algún tema específico que desees que profundicemos más o alguna pregunta sobre los ejemplos presentados?