# Patrones de Diseño

## Objetivo
Comprender el concepto de patrones de diseño en el contexto del desarrollo de software, familiarizarse con los diferentes tipos de patrones, y estudiar los patrones de diseño propuestos por el grupo GoF (Gang of Four) en detalle.



::::{grid}

:::{grid-item}
:margin: auto auto 0 0
:columns: 6
<iframe width="100%" height="280px" src="https://www.youtube.com/embed/tAuRQs_d9F8?si=bExT4XQ-DuCorxH2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

:::
:::{grid-item}

<iframe width="100%" height="280px" src="https://www.youtube.com/embed/tv-_1er1mWI?si=M4ONrTowdRuMPBLR" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

:::
::::

## 1. Contexto General de Patrones de Diseño

Los patrones de diseño son soluciones repetibles a problemas comunes que se encuentran en el diseño de software. Aunque no son directamente soluciones en código, ofrecen una guía para resolver problemas de diseño estructural o de comportamiento. Son herramientas valiosas para mejorar la reutilización del código, la mantenibilidad y la escalabilidad de las aplicaciones.

Un patrón de diseño no es una receta que se puede seguir al pie de la letra, sino más bien un esquema que puede ser adaptado dependiendo de las necesidades específicas de la aplicación. Estos patrones encapsulan buenas prácticas, facilitando la creación de software que sea flexible, robusto y fácil de mantener.


## 2. Tipos de Patrones de Diseño

Los patrones de diseño se clasifican en tres categorías principales según el problema que resuelven y la estructura que organizan:

### 1. Patrones Creacionales
Los patrones creacionales abordan problemas relacionados con la creación de objetos. Estos patrones permiten al sistema ser flexible en cómo y cuándo se crean los objetos, mejorando la reutilización y desacoplando la creación del objeto de su uso directo.

- **Factory Method:** Define una interfaz para crear un objeto, pero deja que las subclases decidan qué clase concreta instanciar. Este patrón es útil cuando la clase base no puede predecir qué clases concretas se deben crear.
- **Singleton:** Asegura que una clase tenga solo una instancia y proporciona un punto de acceso global a esa instancia. Este patrón es ideal cuando se necesita una única instancia, como en la gestión de recursos compartidos (bases de datos, registros).

- **Builder:** Facilita la creación de objetos complejos descomponiéndolo en pasos separados, evitando un constructor con demasiados parámetros. Este patrón es útil cuando se necesita construir objetos con muchas opciones o configuraciones.

### 2. Patrones Estructurales
Los patrones estructurales se centran en la composición de clases y objetos, facilitando la creación de sistemas más complejos mediante la combinación de objetos o clases existentes de manera eficiente. Estos patrones aseguran que las clases y los objetos estén organizados de manera óptima para cumplir los requisitos del diseño.

- **Adapter:** Convierte la interfaz de una clase en otra que el cliente espera, permitiendo que las clases con interfaces incompatibles trabajen juntas.
  - **Ejemplo:** En un sistema de pagos, un adaptador podría permitir que una nueva pasarela de pago se integre sin cambiar el sistema base.
  
- **Decorator:** Permite agregar funcionalidad a un objeto de manera dinámica sin modificar su estructura original. Este patrón es útil cuando se quiere añadir comportamientos a objetos sin heredar de ellos.


### 3. Patrones de Comportamiento
Estos patrones están orientados a la interacción y comunicación entre los objetos. Se centran en cómo los objetos intercambian información y cooperan para realizar tareas complejas. Los patrones de comportamiento ayudan a controlar el flujo de ejecución y las interacciones dentro de un sistema.

- **Observer:** Establece una relación de dependencia entre objetos para que cuando uno cambie su estado, los dependientes sean notificados automáticamente. Este patrón es ideal para sistemas donde múltiples partes necesitan reaccionar ante eventos.
  - **Ejemplo:** Un sistema de monitoreo de stock donde diferentes aplicaciones (como un frontend web y una aplicación de notificaciones) reaccionan a cambios en el inventario.
  
- **Strategy:** Permite definir una familia de algoritmos y elegir uno de ellos en tiempo de ejecución, encapsulando cada algoritmo en su propia clase y permitiendo que se intercambien sin modificar el código del cliente.

Estos tipos de patrones son aplicables en distintos contextos y ayudan a diseñar sistemas más modulares, flexibles y mantenibles. Cada patrón tiene un propósito específico que optimiza la estructura y el comportamiento de las aplicaciones en entornos complejos.

## 3. Patrones GOF (Gang of Four)

El concepto de patrones de diseño fue popularizado por los autores Erich Gamma, Richard Helm, Ralph Johnson y John Vlissides en su famoso libro *"Design Patterns: Elements of Reusable Object-Oriented Software"* (1994). Estos cuatro autores son conocidos como el "Gang of Four" (GoF) y su libro clasifica y detalla 23 patrones de diseño, que se dividen en las tres categorías principales mencionadas anteriormente.

A continuación, se presentan algunos de los patrones más conocidos del GoF:

### Patrones Creacionales del GoF
- **Factory Method:** Proporciona una interfaz para crear objetos, pero deja que las subclases decidan qué clase instanciar.
- **Singleton:** Garantiza que una clase tenga solo una instancia y proporciona un punto de acceso global a ella.

- **Builder:** Facilita la construcción de un objeto complejo paso a paso, sin depender de la implementación concreta del objeto.

### Patrones Estructurales del GoF
- **Adapter:** Permite que interfases incompatibles trabajen juntas convirtiendo la interfaz de una clase en otra.
- **Facade:** Proporciona una interfaz simplificada a un grupo de clases complejas.
- **Decorator:** Añade funcionalidad a un objeto de manera dinámica sin alterar su estructura.

### Patrones de Comportamiento del GoF
- **Observer:** Permite que un objeto, llamado "sujeto", notifique a otros objetos ("observadores") cuando se produce un cambio de estado.
- **Strategy:** Define una familia de algoritmos y permite a los clientes elegir el que se aplicará durante la ejecución.
- **Command:** Encapsula una solicitud como un objeto, permitiendo la parametrización de las acciones que se ejecutarán en el futuro.


## Conclusión

El uso de patrones de diseño es fundamental para mejorar la calidad, eficiencia y sostenibilidad del software. Los patrones de diseño ayudan a resolver problemas recurrentes, proporcionando un lenguaje común para los diseñadores y desarrolladores de software. Los patrones GoF han sido una referencia central para la comunidad de desarrollo orientado a objetos, y su comprensión es clave para cualquier programador Java que desee construir sistemas robustos y escalables.


## Ejercicio Práctico (en proceso)

1. **Implementar el patrón Singleton en un sistema de registro de eventos.**
   - Crea una clase `Logger` que permita registrar mensajes de eventos y asegúrate de que solo exista una instancia de `Logger` en todo el sistema.

2. **Aplicar el patrón Observer.**
   - Crea un sistema de notificaciones donde varios usuarios observan cambios en el estado de un servicio (por ejemplo, un servicio de noticias o una actualización de stock de productos). Al cambiar el estado, todos los usuarios suscritos deben ser notificados automáticamente.

## Recursos Adicionales

- [Design Patterns - Refactoring Guru](https://refactoring.guru/design-patterns)
- [Design Patterns - Source Making](https://sourcemaking.com/design_patterns)