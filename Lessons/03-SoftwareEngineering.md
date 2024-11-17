# Ingeniería de Software

## Objetivo 

Introducir a los estudiantes en los fundamentos de la ingeniería de software, proporcionando una comprensión clara de su definición, los principales problemas que enfrenta la disciplina, y el ciclo de vida del software. Los estudiantes aprenderán cómo estos elementos interactúan en la práctica del desarrollo de software y cómo aplicarlos en proyectos reales para producir software de alta calidad y sostenible.

## 1. Definición de Ingeniería de Software

La ingeniería de software es una disciplina que abarca un conjunto de metodologías, herramientas, y prácticas destinadas a la creación, mantenimiento, y gestión de sistemas de software de manera sistemática, disciplinada y cuantificable. A diferencia de la simple programación, la ingeniería de software se enfoca en todo el proceso de desarrollo, desde la concepción de la idea hasta el mantenimiento del software una vez que está en producción.

### Características Clave
  - **Sistemática:** Uso de métodos organizados y planificados en el desarrollo de software.
  - **Cuantificable:** Medición y control de los procesos y productos del software.
  - **Disciplina:** Aplicación de principios y normas para garantizar la calidad y consistencia.

  ```java
  // Ejemplo básico de un proceso sistemático
  public class SoftwareDevelopment {
      public static void main(String[] args) {
          String[] etapas = {"Requisitos", "Diseño", "Implementación", "Pruebas", "Mantenimiento"};
          for (String etapa : etapas) {
              System.out.println("Etapa: " + etapa);
          }
      }
  }
  ```

### Principios

:::{figure} ../../images/principles.png
---
width: 50%
name: principios
---
Principios fundamentales de la ingeniería de software.
:::


## 2. Principales Problemas en Ingeniería de Software

Desarrollar software a gran escala presenta varios desafíos, entre los que se destacan:

- **Gestión de Requisitos:**
  - Los requisitos del software suelen cambiar a lo largo del tiempo, lo que puede complicar el proceso de desarrollo. La gestión efectiva de estos cambios es crucial para el éxito del proyecto.

- **Calidad del Software:**
  - Asegurar que el software cumpla con los estándares de calidad en términos de funcionalidad, rendimiento, seguridad y usabilidad es uno de los mayores retos en la ingeniería de software.

- **Costos y Plazos:**
  - Los proyectos de software a menudo enfrentan presiones de tiempo y presupuesto. La mala estimación y la falta de planificación pueden llevar a sobrecostos y retrasos significativos.

- **Mantenimiento:**
  - El software requiere actualizaciones y correcciones constantes, lo que a menudo consume más recursos que el desarrollo inicial. Mantener el software limpio y bien documentado es esencial para facilitar su mantenimiento.


## 3. Ciclo de Vida del Software

El ciclo de vida del software describe las etapas a través de las cuales el software pasa desde su concepción hasta su retiro. Cada modelo de ciclo de vida ofrece un enfoque diferente para la gestión de estas etapas.

:::{figure} ../../images/lifecycle.png
---
width: 70%
name: ciclodevida
---
El ciclo de vida de la ingeniería de software.
:::


### Modelos de Ciclo de Vida
  - **Modelo en Cascada:** Un enfoque secuencial donde cada fase debe completarse antes de comenzar la siguiente. Es adecuado para proyectos con requisitos bien definidos desde el inicio.


::::{grid}

:::{grid-item}
:margin: auto auto 0 0
:columns: 6
```{figure} https://edea.juntadeandalucia.es/bancorecursos/file/00bf7c9d-90e4-4665-b6c5-09c91749a989/1/es-an_2017022012_9122843.zip/CicloDeVidaEnCascada.png
---
width: 100%
name: cascada
---
Ciclo de vida de la ingeniería de software en cascada. Tomade de [5.1. Ciclo de vida clásico o en cascada](https://edea.juntadeandalucia.es/bancorecursos/file/00bf7c9d-90e4-4665-b6c5-09c91749a989/1/es-an_2017022012_9122843.zip/51_ciclo_de_vida_clsico_o_en_cascada.html?temp.hn=true&temp.hb=true).
```
:::
:::{grid-item}
:margin: auto auto 0 0
:columns: 6
```{figure} https://kruschecompany.com/wp-content/uploads/2021/09/Waterfall-methodology-infographic-showing-software-development-models-linear-life-cycle-phases-1536x1229.jpg
---
width: 100%
name: cascadametodologia
---
Metodología del desarrollo de software en cascada. Tomado de [What is the Waterfall software development methodology and is it still relevant?](https://kruschecompany.com/waterfall-software-development-methodology/).
```
:::
::::

  - **Modelo Iterativo:** Permite la repetición de fases y es ideal para proyectos donde los requisitos no están completamente definidos desde el principio.
  
  ```java
  // Ejemplo simplificado de una iteración en un ciclo de vida ágil
  public class IteracionAgil {
      public static void main(String[] args) {
          for (int i = 1; i <= 3; i++) {
              System.out.println("Iteración " + i + ": Planificación, Desarrollo, Pruebas, Revisión.");
          }
      }
  }
  ```

  - **Modelo Ágil:** Un enfoque iterativo e incremental que enfatiza la colaboración del equipo, la flexibilidad y la entrega continua de valor al cliente. Es especialmente útil en entornos dinámicos y con cambios frecuentes en los requisitos.

## Ejemplo POO

:::{figure} ../../images/example_design.png
---
width: 80%
name:
---
Ejemplificación del paradigma de programación orientada a objetos (poo).
:::


## Conclusión

La ingeniería de software es una disciplina fundamental para el desarrollo de sistemas complejos y escalables. A través de esta clase, los estudiantes han explorado la definición, los principales problemas, y el ciclo de vida del software, comprendiendo cómo estos elementos se integran en la práctica del desarrollo de software. El ejercicio práctico proporcionó una oportunidad para aplicar estos conceptos en un proyecto real, reforzando la importancia de un enfoque sistemático y disciplinado en la creación de software de calidad.


## Recursos Adicionales

### Guías y Tutoriales

- [software-engineering](https://github.com/floe/software-engineering/tree/master)
- [Software & Software Engineering](https://www.se.rit.edu/~se361/Slides/se361_Chapter_01.pdf)
- [Software Engineering PPT](https://calicut-university.teachics.org/teaching-presentations/software-engineering-ppt/)

### Videos
- [20 System Design Concepts Explained in 10 Minutes ](https://www.youtube.com/watch?v=i53Gi_K3o7I)
