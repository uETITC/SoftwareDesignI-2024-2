# Diagramas de Estado

## Introducción

El diagrama de estado en UML (Unified Modeling Language) es una herramienta visual que modela los diferentes estados de un objeto y los eventos que lo hacen cambiar de un estado a otro. Este tipo de diagrama es esencial para el análisis y diseño de software, ya que permite representar el comportamiento de objetos complejos en sistemas dinámicos.

## Objetivos

- Comprender el concepto y la función de los diagramas de estado en UML.
- Aprender a identificar y definir los estados y transiciones de un objeto.
- Practicar la construcción de un diagrama de estado para representar el ciclo de vida de un objeto.

## Definición

Un diagrama de estado, también conocido como **diagrama de máquina de estados**, es un tipo de diagrama UML que representa los diferentes **estados** de un objeto a lo largo de su vida útil y los **eventos** que provocan cambios entre esos estados. Este tipo de diagrama es especialmente útil para modelar objetos que tienen comportamientos variables, como elementos de sistemas de control o interacción de usuario.

Los diagramas de estado pueden modelar no solo el comportamiento interno de un objeto, sino también cómo reacciona a estímulos externos.

<div align="center">

<iframe width="80%" height="420px" src="https://www.youtube.com/embed/_6TFVzBW7oo?si=odqnUpw8C1OxXaPL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

</div>

## Propiedades

1. **Estado**: Representa una situación en la que un objeto cumple ciertas condiciones, realiza ciertas actividades o espera un evento.
2. **Transición**: Es el cambio de un estado a otro debido a un evento. Se representa con una flecha que conecta los estados.
3. **Evento**: Una ocurrencia que provoca una transición.
4. **Acción**: Una tarea o actividad que se ejecuta durante una transición o en un estado específico.
5. **Estado Inicial y Estado Final**: El estado inicial es donde comienza el diagrama, y el estado final indica dónde termina el comportamiento modelado.

## Sintaxis

En un diagrama de estado, la sintaxis se basa en los siguientes elementos básicos:

- **Estados**: Se representan con rectángulos de bordes redondeados.
- **Transiciones**: Son flechas que indican el cambio de un estado a otro.
- **Eventos**: Los eventos que desencadenan transiciones se colocan junto a la flecha de transición.
- **Acciones**: En algunos casos, las acciones asociadas a una transición o estado pueden indicarse junto al evento o dentro del estado.
- **Estado Inicial**: Representado con un círculo negro sólido.
- **Estado Final**: Representado con un círculo negro dentro de otro círculo.

### Ejemplo de Sintaxis

```text
[Estado Inicial] --> Estado1
Estado1 --Evento1--> Estado2
Estado2 --Evento2--> Estado Final
```

## Usos

- **Modelado del ciclo de vida de un objeto**: Útil para objetos que tienen estados bien definidos, como transacciones bancarias, procesos de pedido en línea, y sistemas de control de acceso.
- **Representación de sistemas de control**: Ideal para sistemas que dependen de estados y eventos, como una máquina de vending o un semáforo.
- **Simulación de flujo de trabajo**: Facilita la representación de procesos que involucran varios estados, como el flujo de aprobación de documentos o el procesamiento de solicitudes.
- **Definición de comportamiento de interfaces de usuario**: Ayuda a modelar cómo la interfaz cambia en respuesta a acciones del usuario.

## Ejemplo: Orden de Compra

Imaginemos un sistema de e-commerce que procesa órdenes de compra. Los estados de la orden podrían incluir:

1. **Orden creada**
2. **Orden en proceso**
3. **Orden enviada**
4. **Orden entregada**
5. **Orden cancelada**

Y las transiciones entre estos estados se producen por eventos específicos:

- **Crear Orden**: Transición de estado inicial a "Orden creada".
- **Procesar Orden**: Transición de "Orden creada" a "Orden en proceso".
- **Enviar Orden**: Transición de "Orden en proceso" a "Orden enviada".
- **Entregar Orden**: Transición de "Orden enviada" a "Orden entregada".
- **Cancelar Orden**: Transición de cualquier estado a "Orden cancelada" si hay una cancelación.

```text
[Inicio] --> Orden creada
Orden creada --Procesar Orden--> Orden en proceso
Orden en proceso --Enviar Orden--> Orden enviada
Orden enviada --Entregar Orden--> Orden entregada
Orden creada --Cancelar Orden--> Orden cancelada
Orden en proceso --Cancelar Orden--> Orden cancelada
Orden enviada --Cancelar Orden--> Orden cancelada
```

## Ejercicio

:::{admonition} Taller
1. **Definir un caso de estudio**: Elige un objeto que cambie de estado en un contexto de negocio (por ejemplo, "Reserva de Hotel" o "Solicitud de Empleo").
2. **Identificar estados y transiciones**: Lista los estados que puede tener el objeto a lo largo de su ciclo de vida, así como los eventos que provocan cambios.
3. **Dibujar el diagrama de estado**: Representa el ciclo de vida del objeto utilizando los elementos básicos de UML.
4. **Añadir detalles**: Identifica y añade eventos y acciones específicas en cada transición o estado, si es necesario.
5. **Explicar el flujo**: Describe el flujo completo, asegurándote de que los eventos y transiciones representen el comportamiento del objeto de forma coherente.
:::

## Conclusión

Los diagramas de estado UML son herramientas fundamentales para modelar comportamientos dinámicos y complejos en sistemas. A través de la identificación de estados y eventos, estos diagramas facilitan la representación del ciclo de vida de los objetos, permitiendo diseñar sistemas más intuitivos y funcionales.

## Recursos Adicionales

### Guías y Tutoriales

- [Documentación UML en Diagramas de Estado](https://www.uml-diagrams.org/state-machine-diagrams.html)
- [All You Need to Know about State Diagrams](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/about-state-diagrams/)
- [What is State Machine Diagram?](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-state-machine-diagram/)
- [IBM: State Machine Diagrams](https://www.ibm.com/docs/en/rational-soft-arch/9.6.1?topic=diagrams-state-machine)
- [UML Tutorial](https://creately.com/diagram-type/uml)

### Videos

- [1.3.7 – UML State Diagram - Object-Oriented Design](https://www.youtube.com/watch?v=qICdYjJA-Ps)
- [UML State Diagram Tutorial](https://www.youtube.com/watch?v=iaX11vYFhZ4)