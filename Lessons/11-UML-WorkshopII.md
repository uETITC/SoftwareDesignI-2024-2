# Taller

## Tema Principal

Modelado de un Sistema de Gestión de Transporte Público en Bogotá, trasmilenio.

## Contexto
Bogotá, como una de las ciudades más grandes de Colombia, enfrenta diariamente desafíos en su sistema de transporte público. El sistema TransMilenio, junto con buses zonales y otros modos de transporte, se utiliza para movilizar a millones de personas. Sin embargo, uno de los principales problemas es la falta de un sistema eficiente de gestión de rutas y disponibilidad de buses. Como diseñadores de software, el reto es modelar un sistema que permita optimizar la gestión del transporte público para hacer más eficiente el uso de rutas, controlar la disponibilidad de buses y mejorar la experiencia de los usuarios.

## Objetivo del Taller
Modelar un sistema de gestión de transporte público en Bogotá utilizando diagramas UML de objetos, clases y casos de uso. Los estudiantes deberán desarrollar soluciones basadas en un problema cotidiano relacionado con el uso del transporte público. Además, deberán implementar una parte del sistema en Java, realizando modificaciones o agregaciones según las especificaciones indicadas.

## Problema a Resolver

Se te ha asignado la tarea de diseñar un **sistema de gestión de buses** para la ciudad de Bogotá. El sistema debe cumplir con los siguientes requisitos funcionales:

1. **Gestión de Rutas:** Cada bus debe estar asignado a una ruta específica. La ruta tiene un número de identificación y contiene un conjunto de paradas. El sistema debe ser capaz de mostrar las paradas y el tiempo estimado de llegada del bus a cada parada.
  
2. **Disponibilidad de Buses:** El sistema debe gestionar la disponibilidad de los buses, indicando si un bus está en operación, en mantenimiento o fuera de servicio.
  
3. **Usuarios del Transporte:** Los usuarios deben ser capaces de consultar la disponibilidad de buses en tiempo real y recibir información sobre las rutas.

4. **Asignación de Conductores:** Cada bus debe tener un conductor asignado. El sistema debe permitir la asignación y reasignación de conductores a los buses según su disponibilidad.

5. **Alertas de Mantenimiento:** El sistema debe enviar alertas cuando un bus necesite mantenimiento.

## Instrucciones:

A partir del problema descrito, realiza lo siguiente:

### 1. Implementación en Java

Implementa una versión simplificada del sistema en Java. A continuación se muestra un ejemplo básico de las clases `Bus`, `Ruta` y `Conductor`. Completa el código agregando los métodos necesarios y realiza las siguientes tareas:

- Implementa la clase `Mantenimiento` que maneje el estado de los buses.
- Añade la posibilidad de asignar y reasignar conductores a los buses.
- Implementa una función para consultar la lista de paradas y el tiempo estimado de llegada a cada parada.

```java
public class Bus {
    private String id;
    private String estado;
    private Ruta ruta;
    private Conductor conductor;

    public Bus(String id, String estado) {
        this.id = id;
        this.estado = estado;
    }

    public void asignarRuta(Ruta ruta) {
        this.ruta = ruta;
    }

    public void asignarConductor(Conductor conductor) {
        this.conductor = conductor;
    }

    public String getEstado() {
        return estado;
    }

    public void setEstado(String estado) {
        this.estado = estado;
    }

    public Ruta getRuta() {
        return ruta;
    }
}

class Ruta {
    private String numero;
    private List<Parada> paradas;

    public Ruta(String numero) {
        this.numero = numero;
        this.paradas = new ArrayList<>();
    }

    public void agregarParada(Parada parada) {
        paradas.add(parada);
    }

    public List<Parada> getParadas() {
        return paradas;
    }
}

class Parada {
    private String nombre;
    private int tiempoEstimado;

    public Parada(String nombre, int tiempoEstimado) {
        this.nombre = nombre;
        this.tiempoEstimado = tiempoEstimado;
    }

    public String getNombre() {
        return nombre;
    }

    public int getTiempoEstimado() {
        return tiempoEstimado;
    }
}

class Conductor {
    private String nombre;
    private String identificacion;

    public Conductor(String nombre, String identificacion) {
        this.nombre = nombre;
        this.identificacion = identificacion;
    }

    public String getNombre() {
        return nombre;
    }
}
```

Además, agrega dos clases que implementen herencia.

### 2. Diagrama de Clases

Desarrolla un **diagrama de clases** que represente las entidades y relaciones del sistema. El diagrama debe incluir:

- Clases: `Bus`, `Ruta`, `Conductor`, `Usuario`, `Parada`, `Mantenimiento`.
- Relaciones de **herencia**, **asociación** y **composición** donde sea aplicable.
  
**Ejemplo de clases y relaciones sugeridas:**

- **Bus:** Identificador, estado (en operación, en mantenimiento, fuera de servicio), capacidad.
- **Ruta:** Número de ruta, lista de paradas.
- **Parada:** Nombre de la parada, tiempo estimado de llegada.
- **Conductor:** Nombre, identificación, asignación a buses.
- **Mantenimiento:** Estado de mantenimiento del bus, alertas generadas.


### 3. Diagrama de Objetos

A partir del diagrama de clases, desarrolla un **diagrama de objetos** que muestre una instancia del sistema en un momento específico. Por ejemplo, un bus asignado a una ruta con su conductor y las paradas definidas.


### 4. Diagrama de Casos de Uso

Elabora un **diagrama de casos de uso** que describa los principales actores y funcionalidades del sistema de gestión de transporte público. Incluye los siguientes casos de uso principales:

- **Consultar rutas**
- **Consultar disponibilidad de buses**
- **Asignar conductor**
- **Recibir alertas de mantenimiento**
- **Consultar paradas de la ruta**

**Indicaciones:**
- Identifica los actores principales (Usuario, Administrador, Conductor).
- Usa relaciones de extensión e inclusión cuando sea necesario.


## Ejercicio

::::{admonition} Taller 6
Deben resolver todo el taller.
### Entregables

1. **Diagramas UML:**
   - Debes entregar los diagramas de casos de uso, clases y objetos en formato gráfico. Puedes usar herramientas como [Lucidchart](https://www.lucidchart.com/pages/), Draw.io o cualquier otra herramienta de modelado UML.
   
2. **Código Java:**
   - Implementa las clases descritas y realiza las modificaciones solicitadas. El código debe estar bien documentado, y el estudiante debe asegurarse de que las funcionalidades solicitadas estén correctamente implementadas.
   
3. **Reporte Final:**
   - El reporte debe incluir una breve explicación de los diagramas UML creados y una descripción del funcionamiento del código desarrollado. Asegúrate de discutir cómo se relacionan los diagramas UML con el código implementado.

:::{note}
La entrega debe hacerse por el campus en la actividad correspondiente a este tema, diagramas UML.
:::

## Criterios de Calificación

- **Claridad y precisión en los diagramas UML (30%)**: Se evaluará la correcta representación de las entidades, relaciones y casos de uso.
- **Correctitud del código (40%)**: Se evaluará si el código cumple con las funcionalidades solicitadas, incluyendo la asignación de conductores y la gestión del estado de los buses.
- **Documentación y presentación (20%)**: El reporte debe estar bien escrito y documentado, explicando cómo se implementó el sistema.
- **Creatividad y profundidad (10%)**: Se valorarán soluciones creativas y extensiones adicionales que enriquezcan el sistema.

::::