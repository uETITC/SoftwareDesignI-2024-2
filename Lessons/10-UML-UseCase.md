# Diagramas de Casos de Uso

## Introducción

El **diagrama de casos de uso** es una herramienta fundamental en el diseño de software, especialmente en las primeras etapas de desarrollo. Es parte del lenguaje de modelado UML (Unified Modeling Language) y se utiliza para representar las interacciones entre los actores (usuarios u otros sistemas) y el sistema que se está desarrollando. Este diagrama se enfoca en las funciones que el sistema debe cumplir y en las relaciones de los actores con dichas funciones, proporcionando una visión clara y comprensible de los requisitos funcionales del sistema.

## Objetivos

- Comprender la definición y las propiedades del diagrama de casos de uso.
- Aprender la sintaxis de un diagrama de casos de uso en UML.
- Aplicar el diagrama de casos de uso para representar los requisitos funcionales de un sistema.
- Desarrollar un ejemplo práctico de un diagrama de casos de uso en un proyecto de software.
  
## Definición

Un **diagrama de casos de uso** es una representación gráfica de las interacciones entre los actores externos (usuarios o sistemas) y el sistema de software que se está diseñando. En lugar de describir cómo el sistema realiza una tarea, el diagrama de casos de uso describe lo que el sistema hace desde el punto de vista del usuario.

<div align="center">

<iframe width="80%%" height="420px" src="https://www.youtube.com/embed/4emxjxonNRI?si=Qfhwi3YWRqgt0or_" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

</div>


## Propiedades

1. **Actor**: Representa una entidad externa que interactúa con el sistema. Puede ser una persona, otro sistema o una organización. Los actores están representados por figuras de palo en el diagrama.
   
2. **Caso de uso**: Una funcionalidad específica que el sistema proporciona a los actores. Está representado por un óvalo que contiene el nombre del caso de uso.
   
3. **Relaciones**: Definen cómo los actores interactúan con los casos de uso y cómo los casos de uso están relacionados entre sí. Pueden ser de dependencia, extensión o inclusión.
   
4. **Sistema**: El sistema se representa mediante un rectángulo que contiene los casos de uso y establece los límites del sistema. Los actores siempre están fuera del rectángulo, ya que son externos al sistema.

**Ejemplos**

::::{grid}

:::{grid-item}
:margin: auto auto 0 0
:columns: 6
```{figure} https://cdn-images.visual-paradigm.com/guide/uml/what-is-use-case-diagram/02-use-case-diagram-annotated.png
---
width: 100%
name: ejemplo1
---
Partes del diagrama.
```
:::
:::{grid-item}
:margin: auto auto 0 0
:columns: 6
```{figure} https://d2jdgazzki9vjm.cloudfront.net/tutorial/uml/images/uml-use-case-diagram.png
---
width: 100%
name: ejemplo2
---
Ejemplo de diagrama de casos de uso: una tienda en línea.
```
:::
::::

::::{grid}
:::{grid-item}
:margin: auto auto 0 0
:columns: 6
```{figure} https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/Use_case_restaurant_model.svg/800px-Use_case_restaurant_model.svg.png
---
width: 100%
name: ejemplo3
---
Ejemplo de diagrama de casos de uso: restaurante.
```
:::
:::{grid-item}
:margin: auto auto 0 0
:columns: 6
```{figure} https://www.uml-diagrams.org/use-case-diagrams/business-use-case-diagram-elements.png
---
width: 100%
name: ejemplo4
---
Ejemplo de diagrama de casos de uso: mini aeropuerto.
```
:::
::::

Otros ejemplos: [UML Use Case Diagram Examples](https://www.uml-diagrams.org/use-case-diagrams-examples.html).

## Sintaxis

- **Actor**: Representado con una figura de palo.
- **Caso de uso**: Representado con un óvalo que contiene el nombre de la función.
- **Relación de comunicación**: Una línea que conecta un actor con un caso de uso.
- **Relación de inclusión**: Se utiliza cuando un caso de uso incluye la funcionalidad de otro. Se representa con una flecha que apunta al caso de uso incluido, acompañada de la etiqueta "<<include>>".
- **Relación de extensión**: Se utiliza cuando un caso de uso extiende otro, agregando funcionalidad condicional. Se representa con una flecha acompañada de la etiqueta "<<extend>>".
- **Relación de dependencia**: Flecha que indica que un caso de uso depende de otro.

## Usos

Los diagramas de casos de uso se utilizan para:
- Identificar los requisitos funcionales del sistema.
- Modelar las interacciones entre los actores y el sistema.
- Facilitar la comunicación entre desarrolladores, analistas y clientes al describir el comportamiento esperado del sistema.
- Servir de base para el diseño detallado y la implementación de funcionalidades.

(ejemplo)=
## Ejemplo práctico en Java

### Caso: Sistema de Biblioteca

Un sistema de biblioteca debe permitir que los usuarios registren libros, busquen libros, y que los administradores gestionen los usuarios.

1. **Actor**: Usuario
2. **Caso de uso**: Registrar libro, Buscar libro
3. **Actor**: Administrador
4. **Caso de uso**: Gestionar usuarios

### Código básico en Java para simular una interacción:

```java
// Clase Usuario
public class Usuario {
    private String nombre;
    
    public Usuario(String nombre) {
        this.nombre = nombre;
    }
    
    public void buscarLibro(String titulo) {
        System.out.println(nombre + " está buscando el libro: " + titulo);
    }
}

// Clase Administrador que hereda de Usuario
public class Administrador extends Usuario {
    
    public Administrador(String nombre) {
        super(nombre);
    }
    
    public void gestionarUsuarios() {
        System.out.println("El administrador está gestionando usuarios.");
    }
}

// Clase Biblioteca que representa el sistema
public class Biblioteca {
    public static void main(String[] args) {
        Usuario usuario = new Usuario("Carlos");
        usuario.buscarLibro("El Quijote");
        
        Administrador admin = new Administrador("Ana");
        admin.gestionarUsuarios();
    }
}
```

### Diagrama de casos de uso:

- Actores: Usuario y Administrador
- Casos de uso: Buscar libro, Gestionar usuarios
- Relaciones: Usuario -> Buscar libro; Administrador -> Gestionar usuarios.

Agrega 2 usos más a cada actor.

## Ejercicio

:::{admonition} Taller 5
Este taller consiste en dos partes:
1. Implementa el código de la sección [Ejemplo práctico en ava](ejemplo).
2. Implementa el diagrama de casos de uso para tu proyecto. Estos diagramas deben tener al menos 3 actores y más de 4 usos por cada actor, puede agregar los que quieran.
:::

## Conclusión

El **diagrama de casos de uso** es esencial para el diseño de sistemas, ya que permite visualizar las interacciones que los usuarios tendrán con el sistema. Ayuda a identificar los requisitos funcionales y a establecer una comprensión clara entre los equipos de desarrollo y los stakeholders. Además, su simplicidad lo convierte en una herramienta ideal para modelar y comunicar las funcionalidades del sistema de manera efectiva.

## Recursos Adicionales

- [Use case diagram - Wikipedia](https://en.wikipedia.org/wiki/Use_case_diagram)
- [UML Use Case Diagrams](https://www.uml-diagrams.org/use-case-diagrams.html)
- [Use-case diagrams - IBM](https://www.ibm.com/docs/en/rational-soft-arch/9.6.1?topic=diagrams-use-case)
- [What is Use Case Diagram? - Visual Paradigm](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-use-case-diagram/)
