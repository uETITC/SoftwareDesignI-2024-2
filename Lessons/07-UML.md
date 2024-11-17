# Lenguaje de Modelado (UML)

## Objetivo
Familiarizar a los estudiantes con el Lenguaje Unificado de Modelado (UML), una herramienta fundamental para el diseño de software. Se abordarán la sintaxis básica, las propiedades del lenguaje, sus aspectos conceptuales y técnicos, así como los diferentes tipos de diagramas que se utilizan en el desarrollo de software, tanto estáticos como dinámicos y de implementación.


## 1. Definición del Lenguaje Unificado de Modelado (UML)

UML es un lenguaje de modelado gráfico estandarizado utilizado para visualizar, especificar, construir y documentar los componentes de sistemas orientados a objetos. Este lenguaje proporciona una forma común de modelar tanto el diseño estructural como el comportamiento de un sistema, lo que facilita la comunicación entre los diferentes actores del proceso de desarrollo (desarrolladores, analistas, clientes, etc.).


## 2. Sintaxis Básica de UML

UML utiliza una serie de elementos gráficos para representar los diferentes aspectos de un sistema. Estos elementos incluyen:

- **Clases:** Representadas por un rectángulo con tres divisiones (nombre, atributos, métodos).
- **Relaciones:** Existen diferentes tipos de relaciones en UML, como la asociación, la herencia, la agregación, la composición y la dependencia. Se representan mediante diferentes tipos de líneas y flechas.
- **Objetos:** Se representan con un rectángulo con subrayado y muestran una instancia de una clase específica.
- **Componentes y Paquetes:** Representan módulos de software o subsistemas y se visualizan con formas rectangulares o como carpetas.

**Ejemplo de representación de una clase:**
```
+---------------------------+
|    Persona                |
+---------------------------+
| + nombre: String          |
| + edad: int               |
+---------------------------+
| + getNombre():String      |
| + setEdad(edad: int): void|
+---------------------------+
```

---

## 3. Propiedades del Lenguaje UML

- **Estándar:** UML es un estándar de facto para modelar software orientado a objetos. Fue desarrollado y es mantenido por la Object Management Group (OMG).
- **Flexibilidad:** Se puede utilizar para modelar cualquier tipo de sistema, no solo aplicaciones orientadas a objetos, sino también sistemas de información, sistemas embebidos y más.
- **Interoperabilidad:** UML se puede integrar fácilmente con diferentes lenguajes de programación (como Java, C#, etc.) y herramientas de desarrollo.
- **Visualización clara:** Facilita la comunicación entre los equipos de desarrollo al proporcionar una representación visual del sistema.


## 4. Aspectos Conceptuales y Técnicos de UML

- **Aspectos Conceptuales:**
  - UML permite representar tanto la **estructura** del sistema (diagramas de clases, de objetos, de componentes) como su **comportamiento** (diagramas de secuencia, diagramas de actividades).
  - UML facilita el **análisis y diseño** en las etapas tempranas del desarrollo, permitiendo realizar ajustes y mejoras antes de la implementación.

- **Aspectos Técnicos:**
  - UML está diseñado para ser **independiente del lenguaje de programación**, lo que lo convierte en una herramienta flexible.
  - Se puede integrar con herramientas CASE (Computer-Aided Software Engineering) para generar código automáticamente a partir de los diagramas.
  - **Modelado orientado a objetos:** UML se basa en los principios de la programación orientada a objetos (clases, objetos, herencia, encapsulación, etc.).

## 5. Tipos de Diagramas en UML

UML se divide en diferentes tipos de diagramas que permiten capturar distintos aspectos del sistema. Estos diagramas se agrupan en tres categorías principales:

### Diagramas Estáticos (Estructurales)

Estos diagramas modelan la estructura estática del sistema, es decir, la forma en que se organizan sus componentes.

- **Diagrama de clases:** Muestra la estructura del sistema mediante la representación de clases, atributos, métodos y las relaciones entre ellas.
- **Diagrama de objetos:** Representa instancias de clases en un momento específico, mostrando cómo los objetos se relacionan entre sí.
- **Diagrama de componentes:** Modela los módulos o componentes del sistema y sus relaciones.
- **Diagrama de paquetes:** Muestra cómo se agrupan las clases y otros elementos en paquetes o módulos lógicos.

### Diagramas Dinámicos (De Comportamiento)

Estos diagramas representan el comportamiento dinámico del sistema, es decir, cómo cambian los estados de los objetos o cómo se comunican entre sí a lo largo del tiempo.

- **Diagrama de secuencia:** Representa cómo los objetos interactúan en una secuencia temporal mediante el intercambio de mensajes.
- **Diagrama de actividades:** Modela el flujo de trabajo o las actividades del sistema, mostrando la lógica de los procesos.
- **Diagrama de casos de uso:** Muestra las interacciones entre los actores externos (usuarios u otros sistemas) y el sistema a través de diferentes casos de uso.
- **Diagrama de estado:** Representa los diferentes estados por los que pasa un objeto a lo largo de su ciclo de vida.

### Diagramas de Implementación

Estos diagramas se utilizan para modelar los aspectos físicos y de implementación de un sistema.

- **Diagrama de despliegue:** Muestra la arquitectura física del sistema, especificando cómo se distribuyen los componentes en hardware.
- **Diagrama de componentes:** Además de su uso estructural, puede mostrar cómo los componentes se implementan físicamente y cómo interactúan en tiempo de ejecución.


## Conclusión

El Lenguaje Unificado de Modelado (UML) es una herramienta esencial para cualquier ingeniero de software. Su flexibilidad, estandarización y capacidad para representar tanto la estructura como el comportamiento del sistema lo convierten en un recurso poderoso en el ciclo de vida del desarrollo de software. Los diagramas UML permiten visualizar, analizar y construir sistemas complejos de manera organizada y clara, mejorando la colaboración entre equipos y minimizando errores en la implementación.


## Ejercicio

:::{admonition} Taller 3
**Objetivo:** Aplicar los conceptos de UML aprendidos en clase para diseñar un sistema de gestión de biblioteca.

**Descripción:**  
Diseña el modelo UML para un sistema de biblioteca que permita gestionar préstamos de libros. Incluye:
- Un diagrama de clases que represente `Libro`, `Usuario`, `Préstamo`, y `Bibliotecario`.
- Un diagrama de secuencia para el proceso de préstamo de un libro.
- Un diagrama de casos de uso que muestre las interacciones entre los usuarios y el sistema.
:::

## Recursos Adicionales

### Guías

- [UML Class Diagram Tutorial](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-class-diagram-tutorial/)
- [UML 2.5 Diagrams Overview](https://www.uml-diagrams.org/uml-25-diagrams.html)
- [UML - Overview](https://www.tutorialspoint.com/uml/uml_overview.htm)
- [UML Diagrams Full Course (Unified Modeling Language) ](https://www.youtube.com/watch?v=WnMQ8HlmeXc)
- [Documentación oficial de UML](https://www.uml.org/)
- OMG Unified Modeling Language (UML), Version 2.5.1. (2017). Object Management Group. https://www.omg.org/spec/UML/2.5.1/
  
### Diagramas

- [Class Diagrams](https://mermaid.js.org/syntax/classDiagram.html)
- [Diagrams](https://app.diagrams.net/)
- [Lucid](https://lucid.app/lucidchart/5abff1a4-9b1b-4733-beac-12ba84090954/edit?invitationId=inv_84d69e5b-1ed5-463e-be69-63a6ebdf9f51&page=0_0#)
- [yFiles - UML](https://live.yworks.com/demos/showcase/uml/)
