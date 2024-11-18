# Diagramas de Colaboración / Comunicación

## Introducción

Los **diagramas de colaboración** en UML son herramientas que se utilizan para representar la interacción entre objetos en un sistema. Estos diagramas muestran cómo los objetos colaboran y se comunican para cumplir una tarea específica, destacando las relaciones y secuencias de mensajes entre ellos. Comprender los diagramas de colaboración es esencial en el diseño de software, ya que permiten visualizar y modelar la comunicación en sistemas orientados a objetos de manera clara y estructurada.

En esta clase, exploraremos los aspectos más importantes de los diagramas de colaboración, incluyendo su definición, propiedades, sintaxis y usos. A través de ejemplos prácticos, veremos cómo estos diagramas pueden mejorar el entendimiento de un sistema y facilitar el diseño de software de calidad.

## Definición

Un **diagrama de colaboración** en UML es un diagrama de interacción que ilustra cómo los objetos en un sistema interactúan para lograr una funcionalidad. A diferencia de los **diagramas de secuencia**, los diagramas de colaboración se enfocan más en la estructura organizativa de los objetos, resaltando sus relaciones y la forma en que colaboran en lugar del orden exacto en que ocurren las interacciones.

<div align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/TL4ABTx_RtE?si=Id6aTxu5oF6Ptd9G" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

## Colaboración vs Secuencia

Ambos diagramas proporcionan la misma información, pero el diagrama de secuencia hace hincapié en el tiempo en su disposición y el diagrama de comunicación hace hincapié en los objetos que se comunican en su disposición.
El tiempo está implícito en los diagramas de secuencia (se deduce por la posición vertical), mientras que se da explícitamente en los diagramas de comunicación (mediante números).

En otras palabras, la principal diferencia entre los diagramas de comunicación y los diagramas de secuencia es que los diagramas de secuencia son buenos para mostrar la lógica secuencial, pero no son tan buenos para ofrecer una «visión global», mientras que los diagramas de comunicación son exactamente lo contrario.

## Propiedades

1. **Enfoque en la Estructura**: Los diagramas de colaboración representan cómo los objetos están organizados y cómo se comunican para alcanzar un objetivo específico.
2. **Interacciones entre Objetos**: Muestran los mensajes que se envían entre objetos, indicando el flujo de información en el sistema.
3. **Número de Referencias**: Cada línea de interacción tiene un número que indica la secuencia de mensajes, aunque no es el enfoque principal del diagrama.
4. **Relaciones Estructurales**: Ponen énfasis en los vínculos entre los objetos y su colaboración, destacando cómo estos vínculos soportan el flujo de mensajes.

## Sintaxis

La sintaxis básica de los diagramas de colaboración incluye:

- **Objetos**: Representados por rectángulos que contienen el nombre del objeto y su clase, separados por dos puntos (`objeto:Clase`). Los objetos pueden tener un rol específico en la colaboración.
- **Líneas de Asociación**: Enlazan los objetos que se comunican entre sí, indicando una relación estructural.
- **Mensajes**: Se representan con etiquetas en las líneas de asociación, y cada mensaje tiene un número que representa el orden relativo. Los mensajes se escriben en notación `n: mensaje`, donde `n` es el número de secuencia.
  
Ejemplo de sintaxis:

```
Pedido:ClasePedido -> Cliente:ClaseCliente
2: verificarDisponibilidad()
3: procesarPago()
```

## Usos

Los diagramas de colaboración son especialmente útiles en:

1. **Modelado de Interacciones Complejas**: Son ideales para sistemas donde el flujo de mensajes depende de una estructura organizacional compleja entre objetos.
2. **Análisis de Responsabilidades**: Ayudan a identificar claramente las responsabilidades de cada objeto en una colaboración.
3. **Diseño de Sistemas Orientados a Objetos**: Facilitan la identificación de relaciones entre objetos en la fase de diseño.
4. **Simulación de Escenarios de Negocio**: Permiten modelar procesos empresariales donde diferentes actores colaboran y se comunican para cumplir un objetivo común.

(codigo)=
## Ejemplo Código Java

Aunque los diagramas de colaboración no tienen una traducción directa en código, el siguiente ejemplo en Java representa la interacción entre objetos en un sistema de gestión de pedidos:

```java
class Cliente {
    private String nombre;
    private Pedido pedido;

    public Cliente(String nombre) {
        this.nombre = nombre;
    }

    public void crearPedido(Inventario inventario, String item) {
        pedido = new Pedido(this);
        pedido.verificarDisponibilidad(inventario, item);
    }
}

class Pedido {
    private Cliente cliente;

    public Pedido(Cliente cliente) {
        this.cliente = cliente;
    }

    public void verificarDisponibilidad(Inventario inventario, String item) {
        if (inventario.estaDisponible(item)) {
            inventario.actualizarStock(item);
            System.out.println("Pedido procesado para: " + cliente.getNombre());
        } else {
            System.out.println("Item no disponible.");
        }
    }
}

class Inventario {
    private Map<String, Integer> stock;

    public Inventario() {
        stock = new HashMap<>();
        stock.put("ProductoA", 10);
    }

    public boolean estaDisponible(String item) {
        return stock.getOrDefault(item, 0) > 0;
    }

    public void actualizarStock(String item) {
        stock.put(item, stock.get(item) - 1);
    }
}
```

En este ejemplo, los objetos `Cliente`, `Pedido`, e `Inventario` interactúan para realizar el pedido, simulando la colaboración en el sistema.

## Ejercicio

:::{admonition} Taller
Agreguen 3 clases más al código anterior, [ejemplo](codigo). Después, utilizando el código completo deben crear un proceso que utilice todas las clases a un problema que propongan que sea coherente con el código. Este problema debe constar de mínimo 5 caminos, el diagrama debe llegar a utilizar el número 5, que sean coherentes.

Además, es necesario agregar una descripción corta sobre cuál es el problema que se esta solucionando.

**Entregables**

Archivo markdown con la descripción y diagrama de comunicación.
:::

## Conclusiones

Los diagramas de colaboración son herramientas valiosas para visualizar cómo los objetos colaboran entre sí en un sistema. A través de estos diagramas, los desarrolladores pueden entender y diseñar de forma clara las interacciones necesarias para cumplir con ciertos requisitos. Además, estos diagramas permiten a los diseñadores de software identificar relaciones y dependencias entre objetos, lo cual es clave para el diseño de software eficaz y orientado a objetos.

## Recursos Adicionales

### Guías y Tutoriales

- [UML Communication Diagrams Overview](https://www.uml-diagrams.org/communication-diagrams.html)
- [What is UML Collaboration Diagram?](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-uml-collaboration-diagram/)
- [UML Collaboration Diagram](https://www.javatpoint.com/uml-collaboration-diagram)


### Videos

-  [UML Communication Diagram ](https://www.youtube.com/watch?v=Xe0VZ2Fw7FQ)
