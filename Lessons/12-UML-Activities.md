# Diagramas Actividades

## Introducción
Los diagramas de actividades son una herramienta fundamental en el diseño de software para modelar el flujo de trabajo o comportamiento dinámico dentro de un sistema. Este tipo de diagrama, parte esencial del Lenguaje Unificado de Modelado (UML), permite representar la secuencia de acciones y decisiones que un sistema realiza para completar una tarea. En esta clase, exploraremos la definición, propiedades, sintaxis y usos de los diagramas de actividades, con ejemplos prácticos que ayudarán a comprender su aplicabilidad en el diseño de software.

## Objetivos
1. Comprender la definición y las propiedades de los diagramas de actividades.
2. Aprender a identificar y utilizar la sintaxis básica de los diagramas de actividades.
3. Aplicar diagramas de actividades para modelar flujos de trabajo en un sistema.
4. Desarrollar la habilidad de interpretar y crear diagramas de actividades utilizando ejemplos prácticos.

## Definición
Un diagrama de actividades es una representación gráfica que modela el flujo de control y las actividades dentro de un proceso o sistema. Se utiliza para describir cómo una actividad o conjunto de acciones se lleva a cabo, las decisiones que se toman en el camino y los posibles estados finales. Los diagramas de actividades son útiles para visualizar procesos complejos, mostrando cómo se interrelacionan los pasos y las decisiones en un sistema.

## Propiedades
- **Orientación a procesos**: Un diagrama de actividades se centra en el flujo de las actividades o acciones dentro de un sistema, mostrando la secuencia de tareas.
- **Paralelismo**: Permite modelar actividades que pueden ejecutarse en paralelo.
- **Decisiones y ramificaciones**: Integra condiciones de decisión que permiten la ramificación de caminos, dependiendo de ciertas condiciones.
- **Estados iniciales y finales**: Define un estado de inicio y uno o varios estados finales, marcando el comienzo y fin de un flujo de trabajo.
- **Concurrencia**: Permite modelar acciones que pueden ocurrir simultáneamente dentro de un sistema.

## Sintaxis
Los diagramas de actividades se basan en una serie de símbolos estandarizados que representan las acciones, decisiones, bifurcaciones y uniones en el flujo de control. Los principales elementos de la sintaxis de un diagrama de actividades incluyen:

- **Elipse o rectángulo redondeado**: Representa una actividad o acción.
- **Flechas**: Indican el flujo de control entre las actividades.
- **Rombo**: Indica una decisión, donde el flujo puede seguir distintos caminos según las condiciones.
- **Barras**: Se utilizan para la sincronización de flujos paralelos o concurrentes, indicando cuándo deben iniciarse o unirse varias actividades.
- **Círculo sólido**: Representa el estado inicial.
- **Círculo rodeado de otro círculo**: Representa el estado final.


El diagrama de actividades utiliza varios elementos gráficos para representar las diferentes partes del flujo de trabajo. Los más importantes son:

1. **Actividad (Activity)**: Representada como un rectángulo redondeado que describe una tarea o acción.
2. **Flechas de flujo (Control Flow)**: Representan el flujo de control entre las actividades.
3. **Nodo de inicio (Initial Node)**: Representa el comienzo del flujo de trabajo y se dibuja como un círculo negro sólido.
4. **Nodo de finalización (Final Node)**: Representa el final del flujo y se dibuja como un círculo con un punto en su interior.
5. **Decisiones (Decision Node)**: Representadas como un rombo, indican que hay diferentes caminos que puede tomar el flujo en función de una condición.
6. **Unión/División (Fork/Join)**: Representan puntos donde el flujo de control se divide o se sincroniza en procesos paralelos.
7. **Objeto (Object Node)**: Representa un objeto que es el resultado de una actividad o que es usado en una actividad.

## Usos
Los diagramas de actividades tienen diversas aplicaciones en el desarrollo y diseño de software:

- **Modelar flujos de trabajo**: Son útiles para visualizar procesos empresariales o flujos de trabajo en aplicaciones.
- **Describir procesos de negocio**: Ayudan a identificar, mejorar o automatizar procesos en sistemas complejos.
- **Especificar comportamiento de casos de uso**: Complementan los diagramas de casos de uso, mostrando los pasos necesarios para completar un caso de uso en particular.
- **Planificación de tareas concurrentes**: Permiten identificar y representar tareas que pueden ejecutarse en paralelo.
  
## Ejemplo
Supongamos que estamos modelando el proceso de compra en una tienda en línea. Este proceso incluye las siguientes actividades: seleccionar productos, agregar al carrito, pagar, y recibir una confirmación.

```text
Inicio → Selección de productos → [Carrito lleno?] → Agregar al carrito → Pagar → [Pago exitoso?] → Confirmación → Fin
                                 ↓
                                 Agregar más productos
```

Este ejemplo ilustra un proceso donde el usuario puede decidir agregar más productos o proceder con el pago, y el sistema decide si el pago fue exitoso para continuar con la confirmación.

## Ejercicio Práctico: Sistema de Cinema

Se te ha asignado la tarea de diseñar un **sistema de cine** que permita gestionar las reservas de boletos de cine para diferentes funciones. El sistema debe contemplar los siguientes pasos desde la perspectiva del cliente:

1. **Inicio del proceso de reserva**: El cliente inicia sesión en el sistema o crea una cuenta si no tiene una.
   
2. **Selección de película y función**: El cliente elige una película de la cartelera y selecciona una función específica con fecha y hora.

3. **Selección de asientos**: Después de elegir la función, el cliente selecciona los asientos disponibles en el cine.

4. **Método de pago**: El cliente selecciona el método de pago (tarjeta de crédito, débito o PayPal).

5. **Pago**: El sistema procesa el pago. Si el pago es exitoso, se genera un boleto electrónico. Si el pago falla, se le da la opción al cliente de intentar nuevamente o cancelar la operación.

6. **Envío de confirmación**: Después de una compra exitosa, se envía una confirmación por correo electrónico al cliente, que incluye los detalles de la reserva y el boleto.

7. **Fin del proceso**: El cliente cierra sesión o sigue navegando por el sistema.

Tu tarea es modelar este flujo en un **diagrama de actividades UML**. Debes identificar los **actores**, **decisiones** y **procesos concurrentes**. Presta atención a los momentos donde el cliente puede decidir entre diferentes caminos (como elegir un método de pago o decidir entre intentar el pago nuevamente o cancelar la operación).

### Requisitos
1. Identificar las **actividades** clave y las **transiciones** entre ellas.
2. Utilizar **ramas de decisión** donde existan alternativas (por ejemplo, el pago fallido).
3. Incorporar **actividades concurrentes** si es necesario (como la opción de recibir un correo de confirmación y seguir navegando en el sistema).
4. Utilizar las **notas UML** cuando sea necesario para explicar ciertas decisiones del diagrama.


### Código Java

Te proporciono un ejemplo de un sistema básico en Java que realiza algunas de las funcionalidades descritas en el problema.

```java
import java.util.*;

public class CinemaSystem {

    private static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        System.out.println("Bienvenido al sistema de cinema.");
        iniciarSesion();
    }

    // Simulación del inicio de sesión o creación de cuenta
    private static void iniciarSesion() {
        System.out.println("1. Iniciar sesión");
        System.out.println("2. Crear cuenta");
        int opcion = scanner.nextInt();
        if (opcion == 1) {
            System.out.println("Iniciando sesión...");
        } else {
            System.out.println("Creando nueva cuenta...");
        }
        seleccionarPelicula();
    }

    // Selección de película
    private static void seleccionarPelicula() {
        System.out.println("Selecciona una película:");
        System.out.println("1. Película A");
        System.out.println("2. Película B");
        int peliculaSeleccionada = scanner.nextInt();
        seleccionarFuncion();
    }

    // Selección de función
    private static void seleccionarFuncion() {
        System.out.println("Selecciona una función:");
        System.out.println("1. 10:00 AM");
        System.out.println("2. 3:00 PM");
        int funcionSeleccionada = scanner.nextInt();
        seleccionarAsientos();
    }

    // Selección de asientos
    private static void seleccionarAsientos() {
        System.out.println("Selecciona tus asientos (ej. A1, A2):");
        String asientos = scanner.next();
        realizarPago();
    }

    // Procesar el pago
    private static void realizarPago() {
        System.out.println("Selecciona método de pago:");
        System.out.println("1. Tarjeta de crédito");
        System.out.println("2. PayPal");
        int metodoPago = scanner.nextInt();

        if (procesarPago()) {
            System.out.println("Pago exitoso. Enviando confirmación...");
            enviarConfirmacion();
        } else {
            System.out.println("Error en el pago. ¿Quieres intentar nuevamente? (1. Sí, 2. No)");
            int reintento = scanner.nextInt();
            if (reintento == 1) {
                realizarPago();
            } else {
                System.out.println("Reserva cancelada.");
            }
        }
    }

    // Simulación del procesamiento de pago
    private static boolean procesarPago() {
        // Simular que el pago a veces falla
        Random random = new Random();
        return random.nextBoolean();
    }

    // Enviar confirmación de la reserva
    private static void enviarConfirmacion() {
        System.out.println("Confirmación enviada a tu correo.");
    }
}
```

### Consideraciones
1. **Inicio**: Inicia con la actividad de "Iniciar sesión o Crear cuenta".
2. **Selección de Película y Función**: Las actividades deben representar la selección de una película y su correspondiente función.
3. **Selección de Asientos**: Una actividad para la selección de asientos disponibles.
4. **Método de Pago**: Rama de decisión que bifurca en distintos métodos de pago.
5. **Pago**: Bifurcación basada en el éxito o fracaso del pago. Se necesita una rama de decisión que contemple el reintento o cancelación del proceso.
6. **Confirmación y Fin**: Después de un pago exitoso, la actividad de enviar la confirmación debe llevar a la finalización del proceso o permitir al cliente seguir navegando.


## Conclusiones
El diagrama de actividades es una herramienta visual poderosa para modelar el comportamiento dinámico dentro de un sistema, facilitando la comprensión de procesos complejos. Su capacidad para representar flujos de control, decisiones, y actividades concurrentes es esencial para diseñar software eficiente y bien estructurado. Mediante la representación gráfica, los diagramas de actividades ofrecen una manera clara de entender y comunicar el flujo de acciones en un sistema, mejorando tanto el diseño como la implementación del software.

## Recursos Adicionales

### Guías y Tutoriales

- [Activity Diagrams - UML2.5](https://www.uml-diagrams.org/activity-diagrams.html)
- [What is Activity Diagram?](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-activity-diagram/)
- [UML Activity Diagram Tutorial - Lucidchart](https://www.lucidchart.com/pages/uml-activity-diagram)
- [UML 2 Tutorial - Activity Diagram](https://sparxsystems.com/resources/tutorials/uml2/activity-diagram.html)
- Object Management Group (OMG). UML Resource Page. [https://www.omg.org/spec/UML](https://www.omg.org/spec/UML)

### Videos

- [UML 2.0 Activity Diagrams ](https://www.youtube.com/watch?v=XFTAIj2N2Lc)