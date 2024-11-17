# Diseño Orientado a Objetos
## Objetivo

Al finalizar esta clase, los estudiantes comprenderán los principios fundamentales del diseño orientado a objetos (OO), las propiedades clave que caracterizan este enfoque, y los mecanismos de herencia utilizados para crear jerarquías de clases en sistemas de software. Además, podrán aplicar estos conceptos en ejemplos prácticos usando Java.

## 1. Definición del Diseño Orientado a Objetos

### Concepto Básico

El Diseño Orientado a Objetos (OO) es un enfoque de desarrollo de software que organiza el diseño del sistema en torno a "objetos," que son instancias de "clases." Estos objetos encapsulan datos y comportamientos relacionados, y se comunican entre sí mediante métodos.

<p align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/pTB0EiLXUC8?si=oJSD02ENYkF4dtHz" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

### Objetos

:::{figure} ../../images/objects.png
---
width: 70% 
name: objeto
---
Características de un objeto. 
:::

::::{grid}

:::{grid-item}
:margin: auto auto 0 0
:columns: 6
```{figure} ../../images/roles1.png
---
width: 100% 
name:
---
Comportamiento de los objetos.
```
:::
:::{grid-item}
:margin: auto auto 0 0
:columns: 6
```{figure} ../../images/roles.png
---
width: 100% 
name: cliclovidaobjetos
---
Ciclo de vida de los objetos.
```
:::
::::


### Clases

:::{figure} ../../images/class.png
---
width: 70% 
name:
---
Ilustración de la definición de una clase.
:::


### Historia y Evolución
El diseño orientado a objetos surgió en la década de 1960 con lenguajes como Simula y Smalltalk, y se popularizó en los años 80 y 90 con lenguajes como C++ y Java. Hoy en día, es un enfoque fundamental en el desarrollo de software moderno.

#### Generaciones y Estructuras
- First-generation languages (1954–1958)
  - FORTRAN I &emsp;&emsp; Mathematical expressions
  - ALGOL 58  &emsp;&nbsp;  &emsp; Mathematical expressions
  - Flowmatic &emsp;&nbsp;&nbsp; &emsp; Mathematical expressions
  - IPL V &emsp; &emsp; &emsp; &emsp; Mathematical expressions
  
:::{figure} ../../images/topology1.png
---
width: 80% 
name:
---

:::

- Second-generation languages (1959–1961)
  - FORTRAN II &emsp;&emsp; Subroutines, separate compilation
  - ALGOL 60 &emsp;&emsp; &emsp;Block structure, data types
  - COBOL &emsp;&emsp; &emsp; &emsp;Data description, file handling
  - Lisp &emsp;&emsp;&emsp;&emsp;&emsp; &emsp;List processing, pointers, garbage collection
:::{figure} ../../images/topology2.png
---
width: 80% 
name:
---

:::

- Third-generation languages (1962–1970)
  - PL/1 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp; FORTRAN + ALGOL + COBOL
  - ALGOL 68 &emsp;&emsp; &emsp; Rigorous successor to ALGOL 60
  - Pascal &emsp;&emsp;&emsp;&emsp; &emsp;Simple successor to ALGOL 60
  - Simula &emsp;&emsp;&emsp;&emsp;&emsp; Classes, data abstraction
:::{figure} ../../images/topology3.png
---
width: 80% 
name:
---

:::

- The generation gap (1970–1980)
Many different languages were invented, but few endured. However, the following are worth noting:
  - C &emsp; &emsp; &emsp; &emsp;&emsp;&emsp;&emsp;Efficient; small executables
  - FORTRAN 77 &emsp; &emsp; ANSI standardization
- Object-orientation boom (1980–1990, but few languages survive)
  - Smalltalk 80  &emsp; &emsp; &emsp; Pure object-oriented language
  - C++ &emsp; &emsp; &emsp; &emsp; &emsp;&emsp; Derived from C and Simula
  - Ada83 &emsp; &emsp; &emsp; &emsp; &emsp; Strong typing; heavy Pascal influence
  - Eiffel &emsp; &emsp; &emsp; &emsp;&emsp;&emsp;  Derived from Ada and Simula
- Emergence of frameworks (1990–today)
  Much language activity, revisions, and standardization have occurred, leading to programming frameworks.
  - Visual Basic &emsp; &emsp; &emsp;  Eased development of the graphical user interface (GUI) for Windows applications
  - Java &emsp; &emsp; &emsp; &emsp; &emsp;&emsp; Successor to Oak; designed for portability
  - Python &emsp; &emsp; &emsp; &emsp; &emsp;   Object-oriented scripting language
  - J2EE &emsp; &emsp; &emsp; &emsp;&emsp;&emsp;  Java-based framework for enterprise computing
  - .NET &emsp; &emsp; &emsp; &emsp;&emsp;&emsp;  Microsoft’s object-based framework
  - Visual C# &emsp; &emsp; &emsp; &emsp; Java competitor for the Microsoft .NET
  Framework
  - Visual Basic .NET &emsp; Visual Basic for the Microsoft .NET Framework
  
:::{figure} ../../images/topology4.png
---
width: 80% 
name:
---

:::

:::{figure} ../../images/topology5.png
---
width: 80% 
name:
---

:::

### Importancia en el Desarrollo de Software
El enfoque orientado a objetos facilita el diseño de sistemas complejos al promover la reutilización de código, la modularidad y la claridad en la estructura del software. Este enfoque es crucial para construir sistemas escalables, mantenibles y fáciles de entender.

### Ventajas del Diseño OO:

- **Modularidad**: Dividir un sistema en objetos ayuda a gestionar la complejidad y facilita el mantenimiento.
- **Reutilización**: Las clases y objetos pueden ser reutilizados en diferentes partes del sistema o en otros proyectos.
- **Flexibilidad**: El diseño OO permite modificaciones y ampliaciones sin afectar la estructura completa del sistema.

## 2. Propiedades del Diseño Orientado a Objetos

### Encapsulamiento
El encapsulamiento es el proceso de ocultar los detalles internos de un objeto y exponer solo lo necesario a través de una interfaz pública. Esto se logra mediante el uso de modificadores de acceso (público, privado, protegido) en las clases de Java.

:::{figure} ../../images/encapsulation.png
---
width: 80% 
name: encapsulamiento
---
Ilustración.
:::

### Abstracción
La abstracción permite a los desarrolladores centrarse en lo esencial, ignorando los detalles complejos que no son relevantes en un contexto particular. Las clases abstractas e interfaces en Java ayudan a lograr la abstracción.
:::{figure} ../../images/abstraction0.png
---
width: 80% 
name: abstraccion
---
Ilustración.
:::
### Modularidad
La modularidad divide el software en partes manejables, llamadas "módulos" o "clases", que pueden desarrollarse, probarse y mantener de forma independiente.
:::{figure} ../../images/modularity.png
---
width: 80% 
name: modularidad
---
Ilustración.
:::

### Polimorfismo
El polimorfismo permite que un objeto se comporte de diferentes maneras según el contexto. En Java, se implementa mediante la sobrecarga de métodos y la implementación de interfaces.

## 3. Mecanismos de Herencia en el Diseño Orientado a Objetos

### Definición y Propósito de la Herencia
La herencia es un mecanismo que permite que una clase (subclase o clase hija) herede atributos y métodos de otra clase (superclase o clase padre). Esto facilita la reutilización de código y la creación de jerarquías de clases que reflejan relaciones "es-un" (is-a) en el mundo real.


::::{grid}

:::{grid-item}
:margin: auto auto 0 0
:columns: 7

```{figure} ../../images/subclass.png
---
width: 100% 
name:
---
Ilustración de la herencia.
```
:::
:::{grid-item}
:margin: auto auto 0 0
:columns: 5

```{figure} ../../images/abstraction.png
---
width: 80% 
name:
---
Ilustración de la jerarquia.
```
:::
::::

### Tipos de Herencia
- **Herencia Simple:** Una clase hereda de una única superclase.
- **Herencia Múltiple:** Una clase hereda de más de una superclase. (No soportada directamente en Java, pero se puede simular mediante interfaces).
- **Herencia Jerárquica:** Varias clases heredan de una misma superclase.
- **Herencia Multinivel:** Una clase hereda de una subclase que a su vez es una subclase de otra clase.

### Implementación de la Herencia en Java
```java
class Vehiculo {
    String marca;
    int año;

    public Vehiculo(String marca, int año) {
        this.marca = marca;
        this.año = año;
    }

    public void encender() {
        System.out.println("El vehículo está encendido.");
    }
}

class Coche extends Vehiculo {
    int puertas;

    public Coche(String marca, int año, int puertas) {
        super(marca, año);
        this.puertas = puertas;
    }

    @Override
    public void encender() {
        System.out.println("El coche está encendido.");
    }
}
```
### Problemas y Buenas Prácticas en la Herencia
- **Problemas de Herencia Múltiple:** Java no soporta herencia múltiple para evitar la ambigüedad que podría surgir.
- **Uso Juicioso de la Herencia:** Se recomienda usar la herencia solo cuando hay una verdadera relación "es-un" entre las clases. De lo contrario, la composición podría ser más apropiada.

## 4. Ejemplo Práctico en Java

### Modelado de un Sistema de Gestión de Vehículos
   - Crear clases `Vehiculo`, `Coche`, `Moto` y `Camion`.
   - Implementar características comunes como `marca`, `año`, y métodos como `encender()` en la clase `Vehiculo`.
   - Extender `Vehiculo` para que `Coche`, `Moto` y `Camion` hereden sus atributos y métodos.
   - Utilizar polimorfismo para implementar métodos como `encender()` de manera diferente en cada subclase.

### Implementación del Ejemplo en Java
   ```java
   class Vehiculo {
       protected String marca;
       protected int año;

       public Vehiculo(String marca, int año) {
           this.marca = marca;
           this.año = año;
       }

       public void encender() {
           System.out.println("El vehículo está encendido.");
       }
   }

   class Coche extends Vehiculo {
       public Coche(String marca, int año) {
           super(marca, año);
       }

       @Override
       public void encender() {
           System.out.println("El coche está encendido.");
       }
   }

   class Moto extends Vehiculo {
       public Moto(String marca, int año) {
           super(marca, año);
       }

       @Override
       public void encender() {
           System.out.println("La moto está encendida.");
       }
   }

   public class TestVehiculos {
       public static void main(String[] args) {
           Vehiculo miCoche = new Coche("Toyota", 2020);
           Vehiculo miMoto = new Moto("Harley", 2021);

           miCoche.encender();
           miMoto.encender();
       }
   }
   ```


## 5. Conclusión

El diseño orientado a objetos es una herramienta poderosa para crear sistemas de software robustos y mantenibles. A través de la encapsulación, la abstracción, la modularidad y el polimorfismo, los desarrolladores pueden construir soluciones flexibles y escalables. La herencia, cuando se usa adecuadamente, permite la reutilización efectiva del código y la creación de estructuras jerárquicas que reflejan las relaciones naturales en el sistema. Sin embargo, es importante usar la herencia con cuidado y considerar alternativas como la composición cuando sea más apropiado. El dominio de estos conceptos permitirá a los estudiantes diseñar e implementar software de alta calidad en Java. 


## Recursos Adicionales

- [Fundamental Concepts of Object Oriented Programming](https://www.youtube.com/watch?v=m_MQYyJpIjg)