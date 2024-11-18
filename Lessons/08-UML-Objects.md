# Diagramas de Objetos

## Objetivo
Entender los **Diagramas de Objetos** dentro del contexto de UML (Lenguaje de Modelado Unificado), su definición, propiedades, sintaxis, y los usos comunes en el diseño de software. Aprenderemos cómo representan instancias de clases en un momento específico y cómo son útiles para visualizar el estado de un sistema.

## Definición
Un **diagrama de objetos** en UML es una representación gráfica que muestra instancias concretas de clases (objetos) en un sistema, junto con los valores de sus atributos en un instante particular. Mientras que un **diagrama de clases** describe la estructura estática de un sistema (clases, atributos y métodos), el diagrama de objetos muestra una instantánea del sistema en ejecución, con instancias específicas de esas clases.

## Propiedades
- **Especificidad**: Muestra un conjunto concreto de objetos y las relaciones entre ellos en un momento determinado.
- **Temporalidad**: Los diagramas de objetos representan una "instantánea" del estado de los objetos en tiempo de ejecución.
- **Similitud con los Diagramas de Clases**: Los objetos mostrados en estos diagramas corresponden a clases en un diagrama de clases, pero con valores asignados a sus atributos.
- **Representación de Relaciones**: Permiten visualizar las asociaciones, agregaciones o composiciones entre objetos, tal como se modelaron en el diagrama de clases.

## Sintaxis
La **sintaxis básica** de un diagrama de objetos en UML se asemeja a la de los diagramas de clases, pero en lugar de mostrar clases, muestra instancias de esas clases. Los principales componentes de la sintaxis incluyen:

1. **Objetos**: Se representan con un rectángulo, que tiene el siguiente formato:
   - **Nombre del objeto**: Se muestra en la parte superior del rectángulo. Se escribe como `nombreObjeto:nombreClase` (donde `nombreObjeto` es opcional).
   - **Atributos**: Dentro del rectángulo, se listan los atributos del objeto con sus valores actuales.

   Ejemplo de sintaxis:
   ```
   objetoUsuario:Usuario
   nombre = "Juan Pérez"
   email = "juan@example.com"
   ```

2. **Relaciones**: Los objetos pueden estar conectados mediante líneas que representan asociaciones. Estas líneas pueden ser:
   - **Líneas simples**: Representan una asociación o relación entre los objetos.
   - **Agregación o Composición**: Las mismas reglas de los diagramas de clases aplican aquí. La agregación se muestra con un rombo vacío en el extremo de la línea, y la composición con un rombo lleno.

3. **Multiplicidad**: En los diagramas de objetos también se puede indicar la multiplicidad de las relaciones, por ejemplo `1..*` para indicar "uno o muchos".

## Ejemplo

```
pedido1:Pedido       cliente1:Cliente
-------------------  ---------------------
numero = "12345"     nombre = "Laura"
fecha = "15/09/2024" email = "laura@mail.com"
total = "$500"
```

En este ejemplo, `pedido1` es una instancia de la clase `Pedido` y `cliente1` es una instancia de la clase `Cliente`.

### Usos
Los diagramas de objetos tienen varios usos clave en el diseño de software:

1. **Visualización del Estado del Sistema**: Los diagramas de objetos permiten visualizar cómo se comporta un sistema en un momento específico. Esto puede ser útil para entender cómo interactúan los objetos en un escenario particular.
   
2. **Depuración y Validación**: Estos diagramas son útiles durante las etapas de diseño y desarrollo para validar que el modelo de clases se está implementando correctamente y que los objetos están interaccionando como se espera. También se utilizan en la depuración de aplicaciones para comparar el estado del sistema en ejecución con el modelo diseñado.
   
3. **Modelado Dinámico**: A diferencia del diagrama de clases, que muestra una vista general del sistema, el diagrama de objetos permite ver una versión "en vivo" del sistema y entender las interacciones dinámicas entre los objetos.

4. **Documentación**: Se utilizan para documentar cómo debería funcionar el sistema bajo ciertas condiciones o escenarios.


## Ejercicio

::::{admonition} Taller 4

### Instrucciones
1. **Entender el Código Java**: A continuación, se proporciona un fragmento de código Java. Debes analizar el código para identificar las instancias de las clases, sus atributos, y cómo se relacionan entre sí.
2. **Crear el Diagrama de Objetos en UML**: Basado en las instancias creadas en el código, debes construir un diagrama de objetos en UML. Recuerda utilizar la sintaxis correcta para representar objetos y las relaciones entre ellos.
3. **Explicar el Diagrama**: Una vez creado el diagrama, escribe una breve explicación del mismo, describiendo los objetos, atributos, y relaciones representadas.

:::{admonition} Código Java
:class: dropdown

```java
// Clase Cliente
public class Cliente {
    private String nombre;
    private String email;

    public Cliente(String nombre, String email) {
        this.nombre = nombre;
        this.email = email;
    }

    public String getNombre() {
        return nombre;
    }

    public String getEmail() {
        return email;
    }
}
// Clase Producto
public class Producto {
    private String nombreProducto;
    private double precio;

    public Producto(String nombreProducto, double precio) {
        this.nombreProducto = nombreProducto;
        this.precio = precio;
    }

    public String getNombreProducto() {
        return nombreProducto;
    }

    public double getPrecio() {
        return precio;
    }
}
// Clase Pedido
public class Pedido {
    private Cliente cliente;
    private Producto producto;
    private int cantidad;

    public Pedido(Cliente cliente, Producto producto, int cantidad) {
        this.cliente = cliente;
        this.producto = producto;
        this.cantidad = cantidad;
    }

    public Cliente getCliente() {
        return cliente;
    }

    public Producto getProducto() {
        return producto;
    }

    public int getCantidad() {
        return cantidad;
    }

    public double calcularTotal() {
        return cantidad * producto.getPrecio();
    }

    public static void main(String[] args) {
        Cliente cliente1 = new Cliente("Juan Pérez", "juan.perez@mail.com");
        Cliente cliente2 = new Cliente("Laura Gómez", "laura.gomez@mail.com");

        Producto producto1 = new Producto("Laptop", 1200.00);
        Producto producto2 = new Producto("Smartphone", 800.00);

        Pedido pedido1 = new Pedido(cliente1, producto1, 1);
        Pedido pedido2 = new Pedido(cliente2, producto2, 2);
    }
}
```
:::

### Tareas

1. **Identificación de Objetos**:
   - ¿Cuáles son las instancias creadas en el `main`?
   - ¿Qué atributos tienen esas instancias?

2. **Crear el Diagrama de Objetos**:
   - Utiliza una herramienta de modelado o dibuja el diagrama de objetos a mano (siguiendo la sintaxis de UML). Asegúrate de incluir:
     - Las instancias `cliente1`, `cliente2`, `producto1`, `producto2`, `pedido1`, `pedido2`.
     - Los valores actuales de sus atributos.
     - Las relaciones entre los objetos (`Pedido` tiene una relación con `Cliente` y `Producto`).

3. **Explicación del Diagrama**:
   - Escribe un breve párrafo explicando los objetos representados, sus relaciones, y el estado del sistema mostrado en el diagrama.


### Ejemplo de Objetos

#### Instancias
- `cliente1:Cliente` → nombre: "Juan Pérez", email: "juan.perez@mail.com"
- `cliente2:Cliente` → nombre: "Laura Gómez", email: "laura.gomez@mail.com"
- `producto1:Producto` → nombreProducto: "Laptop", precio: 1200.00
- `producto2:Producto` → nombreProducto: "Smartphone", precio: 800.00
- `pedido1:Pedido` → cliente: cliente1, producto: producto1, cantidad: 1
- `pedido2:Pedido` → cliente: cliente2, producto: producto2, cantidad: 2


### Criterios de Evaluación

1. **Exactitud del Diagrama**: El diagrama debe reflejar correctamente las instancias de objetos y las relaciones descritas en el código.
2. **Sintaxis UML**: Se evaluará el uso correcto de la sintaxis UML, incluyendo la representación de objetos, atributos, y relaciones.
3. **Explicación del Diagrama**: La explicación debe ser clara y coherente, describiendo adecuadamente las relaciones entre los objetos.

::::


## Conclusión

Los diagramas de objetos son una herramienta importante en UML que permiten ver el estado y las relaciones de las instancias de clases en un momento específico. Son útiles tanto en la fase de diseño como en la de desarrollo de software para visualizar y validar el comportamiento del sistema en tiempo de ejecución. Entender cómo funcionan los diagramas de objetos y cómo se relacionan con los diagramas de clases es fundamental para un correcto modelado orientado a objetos.



## Recursos Adicionales

### Guías y Tutoriales


- [UML Class Diagram Tutorial](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-class-diagram-tutorial/)
- [UML 2.5 Diagrams Overview](https://www.uml-diagrams.org/uml-25-diagrams.html)
- [What is Unified Modeling Language (UML)?](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-uml/)


### Diagramas

- [PlantUML](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml)
- [LucidChart](https://www.lucidchart.com/pages/)
- [StarUML](https://staruml.io/)
- [Mermaid](https://mermaid.js.org/)