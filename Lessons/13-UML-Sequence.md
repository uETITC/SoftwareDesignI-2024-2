# Diagramas de Secuencia

## Introducción

En el diseño de software, los diagramas de secuencia juegan un papel fundamental para representar la interacción entre objetos y componentes de un sistema a lo largo del tiempo. Estos diagramas ayudan a visualizar y entender cómo los elementos de un sistema colaboran entre sí, ilustrando el flujo de mensajes y la sincronización entre ellos. En esta clase, profundizaremos en la teoría de los diagramas de secuencia, y al finalizar realizaremos actividades prácticas para aplicar los conceptos aprendidos.

## Objetivos de la Clase

1. Entender la definición y propósito de un diagrama de secuencia.
2. Aprender la sintaxis y las propiedades de los diagramas de secuencia.
3. Conocer los elementos básicos y avanzados de un diagrama de secuencia.
4. Desarrollar habilidades para diseñar diagramas de secuencia en casos prácticos.
5. Familiarizarse con el uso de herramientas digitales para la creación de diagramas de secuencia.

## 1. Definición

<div align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/pCK6prSq8aw?si=pdYLSStCYfSZcmTj" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

Los diagramas de secuencia son un tipo de diagrama de interacción en UML que muestran cómo los objetos de un sistema se comunican mediante una secuencia temporal de mensajes. Cada diagrama representa una instancia específica del flujo de mensajes en respuesta a un evento en particular, detallando el orden en que estos mensajes son enviados y recibidos.

Estos diagramas son ampliamente utilizados para visualizar casos de uso complejos, ya que descomponen el flujo de trabajo en una serie de pasos claros y estructurados.

## 2. Propiedades

Los diagramas de secuencia poseen características específicas que facilitan su interpretación:

- **Línea de vida:** Representa la vida de un objeto desde su creación hasta su destrucción dentro de la interacción.
- **Mensajes:** Indican la comunicación entre objetos. Pueden ser de tipo síncrono, asíncrono o de retorno.
- **Activación:** Representa el período durante el cual un objeto realiza una acción en respuesta a un mensaje.
- **Banda de actores o roles:** Cada actor u objeto tiene su propio carril en el diagrama, mostrando claramente su rol en la secuencia de eventos.
- **Componentes opcionales:** Se pueden incluir marcos condicionales y de bucle para ilustrar decisiones y repeticiones en la secuencia.

:::{figure} ../../images/Figure5.43.png
---
width: 60%
name: 
---
Tipos de mensajes y notación.
:::

## 3. Sintaxis

A continuación, se describen los elementos básicos de la sintaxis en diagramas de secuencia:

- **Actores y Objetos:** Representados por rectángulos o iconos específicos. Cada actor es el origen o destino de un mensaje en el diagrama.
- **Líneas de vida:** Representadas por líneas punteadas que descienden desde el actor u objeto, mostrando su existencia durante la secuencia.
- **Mensajes:** Representados por flechas horizontales:
  - **Mensajes síncronos:** Flechas con línea continua que van desde un objeto emisor hasta el objeto receptor.
  - **Mensajes asíncronos:** Flechas con línea discontinua, representando mensajes que no requieren una respuesta inmediata.
  - **Mensajes de retorno:** Flechas con línea continua y sin cabeza de flecha, indican la devolución de un valor o respuesta.
- **Cuadros de Activación:** Rectángulos estrechos en la línea de vida que indican cuándo un objeto está activo realizando una acción.
- **Bloques condicionales y de bucle:** Enmarcados por etiquetas como `alt`, `opt` o `loop`, muestran bifurcaciones y repeticiones en el flujo.

:::{figure} ../../images/Figure5.45.png
---
width: 100%
name: 
---
Ejemplo de diagrama de secuencia sobre un invernadero pequeño.
:::

## 4. Usos

Los diagramas de secuencia son útiles para diversas etapas de desarrollo de software:

- **Especificación de casos de uso:** Ayudan a detallar cómo los actores interactúan con el sistema en escenarios específicos.
- **Desglose de requisitos funcionales:** Proveen un desglose detallado de los pasos involucrados en un proceso, alineando los requisitos funcionales con la lógica de interacción.
- **Diseño de componentes y servicios:** Visualizan la interacción entre componentes en sistemas distribuidos, mostrando cómo los servicios se comunican en tiempo real.
- **Depuración y documentación:** Facilitan la identificación de posibles problemas en la comunicación entre componentes, especialmente en sistemas concurrentes.

## Ejercicio

:::{admonition} Taller

Para aplicar lo aprendido, selecciona un caso de uso simple de una aplicación de mensajería, como enviar un mensaje directo a otro usuario. Desarrolla un diagrama de secuencia que cumpla con los siguientes pasos:

1. **Identificación de Objetos:** Define los objetos involucrados (por ejemplo, Usuario, Servidor de Mensajería, Base de Datos).
2. **Definición de Líneas de Vida y Mensajes:**
   - Muestra cómo el usuario envía el mensaje.
   - Indica cómo el servidor procesa el mensaje y lo almacena en la base de datos.
   - Visualiza el proceso de entrega del mensaje al destinatario.
3. **Incorporación de Bloques Opcionales y Bucles:**
   - Agrega un bloque condicional para verificar si el destinatario está en línea o no.
   - Incluye un bucle que simule la notificación de “escribiendo” mientras el usuario redacta el mensaje.
:::

## Recursos Adicionales

- [UML Sequence Diagrams - UML 2.5](https://www.uml-diagrams.org/sequence-diagrams.html)
- OMG (2021). *Unified Modeling Language (UML)*. [https://www.omg.org/spec/UML/](https://www.omg.org/spec/UML/)
- Visual Paradigm. *UML Sequence Diagram Tutorial*. [https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-sequence-diagram-tutorial/](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-sequence-diagram-tutorial/)