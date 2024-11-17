# Taller

## Tema Principal

Diagramas de Clases y Objetos para una tienda simple.

## Objetivo:
El propósito de este taller es que los estudiantes identifiquen y traduzcan los componentes del código Java en diagramas UML de clases y objetos, con un enfoque en la representación de relaciones de **herencia** y **asociación**. Este ejercicio les permitirá visualizar cómo se estructuran y relacionan las clases en un sistema con más detalle.

## Instrucciones:
1. Se proporciona un código en Java que simula la gestión de una librería, ahora con relaciones de **herencia** y **asociación**.
2. El estudiante deberá:
   - Crear el **diagrama de clases UML**, identificando las relaciones de herencia y asociación.
   - Crear el **diagrama de objetos UML**, representando instancias de las clases y su interacción.

## Código a Analizar:

```java
// Clase Producto
public class Producto {
    private String nombre;
    private double precio;

    public Producto(String nombre, double precio) {
        this.nombre = nombre;
        this.precio = precio;
    }

    public String getNombre() {
        return nombre;
    }

    public double getPrecio() {
        return precio;
    }
}

// Clase Libro (Hereda de Producto)
public class Libro extends Producto {
    private String autor;

    public Libro(String nombre, String autor, double precio) {
        super(nombre, precio);
        this.autor = autor;
    }

    public String getAutor() {
        return autor;
    }
}

// Clase Revista (Hereda de Producto)
public class Revista extends Producto {
    private int numeroEdicion;

    public Revista(String nombre, int numeroEdicion, double precio) {
        super(nombre, precio);
        this.numeroEdicion = numeroEdicion;
    }

    public int getNumeroEdicion() {
        return numeroEdicion;
    }
}

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

// Clase Pedido (Asociación con Producto y Cliente)
public class Pedido {
    private Producto producto;  // Asociación con Producto (Libro o Revista)
    private Cliente cliente;

    public Pedido(Producto producto, Cliente cliente) {
        this.producto = producto;
        this.cliente = cliente;
    }

    public Producto getProducto() {
        return producto;
    }

    public Cliente getCliente() {
        return cliente;
    }

    public void detallesPedido() {
        System.out.println("Cliente: " + cliente.getNombre() + " ha pedido el producto '" 
            + producto.getNombre() + "' con un precio de " + producto.getPrecio());
    }
}

// Clase Principal
public class Main {
    public static void main(String[] args) {
        Libro libro = new Libro("El Quijote", "Miguel de Cervantes", 29.99);
        Revista revista = new Revista("National Geographic", 203, 5.99);
        Cliente cliente = new Cliente("Juan Pérez", "juan.perez@example.com");

        Pedido pedido1 = new Pedido(libro, cliente);
        Pedido pedido2 = new Pedido(revista, cliente);

        pedido1.detallesPedido();
        pedido2.detallesPedido();
    }
}
```

## Ejercicio

::::{admonition} Taller 5

### Tareas

1. **Diagrama de Clases UML**:
   - Identifique las clases **Producto**, **Libro**, **Revista**, **Cliente**, y **Pedido**.
   - Modele la **herencia** entre la clase base `Producto` y sus subclases `Libro` y `Revista`.
   - Establezca las relaciones de **asociación** entre `Pedido` y `Producto`, y entre `Pedido` y `Cliente`.
   - Defina correctamente los atributos y métodos de cada clase, con las visibilidades adecuadas (`private`, `public`).

2. **Diagrama de Objetos UML**:
   - Cree un diagrama de objetos que muestre las instancias de `Libro`, `Revista`, `Cliente`, y `Pedido` creadas en el método `main`. Por lo menos tres objetos por clase, excepto del main.
   - Modele la asociación entre los objetos en esta ejecución (por ejemplo, el `pedido1` está asociado a una instancia de `Libro` y a una instancia de `Cliente`).

## Entrega
- Los estudiantes deberán entregar:
   - Un diagrama de **clases UML** que represente la estructura del código con herencia y asociaciones.
   - Un diagrama de **objetos UML** que modele las instancias de los objetos en el método `main`.
   - Adjuntar una explicación breve justificando las relaciones y decisiones de modelado.
- Pantallazos con el código funcionando. Realizar algunas pruebas

## Criterios de Evaluación

1. **Claridad y precisión del diagrama de clases** (40%):
   - Identificación correcta de las relaciones de herencia y asociación.
   - Uso adecuado de visibilidad para los atributos y métodos.

2. **Exactitud del diagrama de objetos** (40%):
   - Representación adecuada de las instancias y relaciones entre objetos en tiempo de ejecución.

3. **Presentación y justificación del trabajo** (20%):
   - Entrega clara, con diagramas bien estructurados y una explicación coherente.
::::

## Conclusión:
Este taller permite que los estudiantes practiquen la traducción de un código Java con relaciones de herencia y asociación a diagramas UML de clases y objetos, desarrollando habilidades clave para el diseño y comprensión de sistemas orientados a objetos.