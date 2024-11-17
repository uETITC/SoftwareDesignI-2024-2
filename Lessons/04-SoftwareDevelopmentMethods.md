# Métodos de Desarrollo de Software

## Objetivo

El objetivo de esta clase es proporcionar a los estudiantes una comprensión detallada de los diferentes métodos de desarrollo de software, tanto tradicionales como ágiles. Los estudiantes aprenderán sobre las características, ventajas, desventajas y aplicaciones prácticas de cada enfoque. Al finalizar la clase, los estudiantes estarán capacitados para seleccionar el método de desarrollo adecuado para diferentes tipos de proyectos de software.

## 1. Introducción a los Métodos de Desarrollo de Software

Los métodos de desarrollo de software son marcos y prácticas que guían el proceso de creación de software. Estos métodos proporcionan estructuras claras para el desarrollo, garantizando que los proyectos se completen de manera eficiente, dentro del presupuesto y cumpliendo con los requisitos del cliente.


## 2. Métodos Tradicionales

### 2.1 Cascada

**Definición:**  
El modelo en cascada es uno de los métodos más antiguos y conocidos en el desarrollo de software. Sigue un enfoque lineal y secuencial, donde cada fase del desarrollo debe completarse antes de pasar a la siguiente.

<p align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/Y_A0E1ToC_I?si=pVbKepB6S55KPsxy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

**Fases**:  
- **Requisitos:** Recopilación de todas las necesidades del cliente.
- **Diseño:** Diseño del sistema basado en los requisitos.
- **Implementación:** Codificación del software.
- **Pruebas:** Verificación y validación del software.
- **Despliegue:** Implementación del software en el entorno de producción.
- **Mantenimiento:** Corrección de errores y mejoras.

:::{figure} https://kruschecompany.com/wp-content/uploads/2021/09/Waterfall-methodology-infographic-showing-software-development-models-linear-life-cycle-phases-1536x1229.jpg
---
width: 80%
name: metodologiacascada
---
Metodología en cascada.
:::

**Ventajas:**  
- Simple y fácil de entender y utilizar.
- Adecuado para proyectos pequeños con requisitos claros y definidos.

**Desventajas:**  
- Poco flexible; difícil de retroceder a fases anteriores.
- Riesgo elevado si los requisitos no se comprenden completamente desde el principio.

**Ejemplo Práctico:**  
Desarrollo de software para sistemas integrados donde los requisitos son muy claros y no cambiarán.

### 2.2 Modelo en V

**Definición:**  
El modelo en V es una extensión del modelo en cascada, pero enfatiza la verificación y validación en cada fase del desarrollo.

**Fases:**
- Similar al modelo en cascada, pero con un enfoque paralelo en la prueba y desarrollo.

:::{figure} https://www.bdtask.com/blog/assets/plugins/ckfinder/core/connector/php/uploads/images/diagram-of-v-model.jpg
---
width: 80%
name: metodologiav
---
Metodología en V. Tomado de [V Model In Software Development-Best Practice in SDLC Process](https://www.bdtask.com/blog/v-model-in-software-development).
:::

**Ventajas:**  
- Mayor enfoque en las pruebas desde el principio.
- Adecuado para proyectos donde la calidad es crítica.

**Desventajas:**  
- Como el modelo en cascada, es inflexible y no maneja bien los cambios en los requisitos.

**Ejemplo Práctico:**  
Desarrollo de software para sistemas de control crítico, como software médico o aeroespacial.

### 2.3 Proceso Unificado Racional (RUP)

**Definición:**  
RUP es un marco iterativo que permite la personalización de procesos. Se basa en la creación de modelos visuales del sistema y en la iteración a través de varias fases del ciclo de vida del software.

<p align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/caLs9vlqSs4?si=E8wwmllhdw12GuqP" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

**Fases:**  
- **Inicio:** Definición de la visión del proyecto.
- **Elaboración:** Análisis de requisitos y diseño del sistema.
- **Construcción:** Desarrollo y prueba de componentes.
- **Transición:** Despliegue y entrega del producto final.


::::{grid}

:::{grid-item}
:margin: auto auto 0 0
:columns: 6
```{figure} https://cdn.sketchbubble.com/pub/media/catalog/product/optimized1/1/f/1f26a4b2de8657ecc76f9e29a56e6083b48c21cd0ff0be1fcc0aeca003f8f107/rational-unified-process-mc-slide1.png
---
width: 100%
name:
---
Tomado de [Rational Unified Process PowerPoint and Google Slides Template](https://www.sketchbubble.com/en/presentation-rational-unified-process.html).
```
:::

:::{grid-item}
:margin: auto auto 0 0
:columns: 6

```{figure} https://cdn.sketchbubble.com/pub/media/catalog/product/optimized1/9/d/9de4b0672a98679eb5c82edc7636bc6910c0d68b0c630e7a16053c861f8f2b28/rational-unified-process-mc-slide5.png
---
width: 100%
name:
---
Tomado de [Rational Unified Process PowerPoint and Google Slides Template](https://www.sketchbubble.com/en/presentation-rational-unified-process.html).
```
:::
::::


**Ventajas:**  
- Flexible y adaptable a diferentes tipos de proyectos.
- Enfoque iterativo que permite mejoras continuas.

**Desventajas:**  
- Puede ser complejo y difícil de gestionar en proyectos más pequeños.
- Requiere una gran cantidad de documentación y seguimiento.

**Ejemplo Práctico:**  
Desarrollo de sistemas empresariales grandes y complejos que requieren flexibilidad y adaptación continua.


## 3. Métodos Ágiles

**Definición**
Los métodos ágiles son un conjunto de enfoques de desarrollo de software diseñados para promover la flexibilidad, la colaboración y la entrega continua de valor en entornos de proyectos que requieren adaptabilidad. Surgieron en respuesta a las limitaciones de los métodos tradicionales, que a menudo son demasiado rígidos, para enfrentar los cambios rápidos en los requisitos del cliente y en el entorno del proyecto.  Promueven la flexibilidad, la colaboración y la entrega rápida de software funcional.

**Características Clave de los Métodos Ágiles:**

1. **Iterativos e Incrementales:**
   - En lugar de intentar desarrollar un sistema completo de una sola vez, los métodos ágiles dividen el trabajo en pequeños incrementos funcionales que se completan en iteraciones cortas, típicamente de dos a cuatro semanas. Cada iteración produce un incremento de software que se puede probar, revisar y mejorar en función del feedback recibido.

2. **Colaboración Estrecha con el Cliente:**
   - Los métodos ágiles fomentan una colaboración continua con el cliente o con un representante del cliente (como el Product Owner en Scrum). Esto asegura que el equipo de desarrollo entienda completamente los requisitos del cliente y pueda adaptarse rápidamente a los cambios en esos requisitos.

3. **Equipos Autogestionados:**
   - Los equipos en un entorno ágil son generalmente pequeños, multifuncionales y autogestionados. Esto significa que el equipo tiene la autonomía para decidir cómo cumplir con los objetivos del proyecto, lo que fomenta la innovación y la eficiencia.

4. **Respuesta Rápida al Cambio:**
   - Uno de los principios fundamentales de los métodos ágiles es la capacidad de adaptarse al cambio, incluso en etapas tardías del desarrollo. Esto contrasta con los métodos tradicionales, donde los cambios a menudo son costosos y difíciles de implementar.

5. **Entrega Continua de Valor:**
   - En lugar de esperar hasta el final del proyecto para entregar el producto final, los métodos ágiles buscan entregar valor al cliente de manera continua a lo largo del ciclo de vida del proyecto. Esto se logra a través de entregas frecuentes y funcionales que pueden ser evaluadas y utilizadas por el cliente.

**Manifiesto Ágil:**
El Manifiesto Ágil, publicado en 2001 por un grupo de 17 desarrolladores de software, establece los valores y principios fundamentales que guían los métodos ágiles. Los cuatro valores principales del manifiesto son:

1. **Individuos e interacciones sobre procesos y herramientas.**
2. **Software funcionando sobre documentación extensiva.**
3. **Colaboración con el cliente sobre negociación de contratos.**
4. **Responder al cambio sobre seguir un plan.**

Además, el manifiesto se acompaña de 12 principios que detallan cómo aplicar estos valores en la práctica, enfatizando la entrega temprana y continua de software, la simplicidad, y la mejora continua del equipo y el producto.

**Ventajas de los Métodos Ágiles:**

- **Mayor Flexibilidad:** Permiten adaptarse rápidamente a los cambios en los requisitos y en las prioridades del cliente.
- **Mayor Participación del Cliente:** Fomenta una comunicación constante y la colaboración con el cliente, lo que reduce el riesgo de malentendidos y errores en los requisitos.
- **Mejora Continua:** A través de la retrospección y la entrega continua de incrementos de software, los equipos ágiles pueden mejorar sus procesos y productos de manera continua.
- **Reducción del Riesgo:** Al trabajar en ciclos cortos y entregar funcionalidad continuamente, los riesgos se identifican y mitigan más rápidamente.

Los métodos ágiles han transformado la industria del software, brindando un enfoque más dinámico y centrado en el cliente para la gestión y ejecución de proyectos. Son particularmente útiles en entornos donde los requisitos son inciertos o pueden cambiar rápidamente, y donde la velocidad de entrega es una prioridad.

::::{grid}

:::{grid-item}
:margin: auto auto 0 0
:columns: 6

<iframe width="100%" height="280px" src="https://www.youtube.com/embed/8eVXTyIZ1Hs?si=VhCD2PwdcGrF_9Iq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

:::

:::{grid-item}
:margin: auto auto 0 0
:columns: 6
<iframe width="100%" height="280px" src="https://www.youtube.com/embed/zi7uGg6FVM4?si=ILn_ylo2USxYobqS" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
:::
::::

### 3.1 Programación Extrema (XP)

**Definición:**  
XP es un enfoque de desarrollo ágil que enfatiza la simplicidad, la comunicación, la retroalimentación y el coraje. Se centra en entregas frecuentes de software funcional y en la adaptación constante a los cambios en los requisitos.

<p align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/p3Zl6dLGILU?si=N5NFay6Ct6ghJ0_B" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

**Prácticas clave:**  
- **Desarrollo incremental:** Entrega de pequeñas funcionalidades en ciclos cortos.
- **Pruebas constantes:** Pruebas unitarias y de integración continuas.
- **Programación en parejas:** Dos desarrolladores trabajan juntos en una sola tarea para mejorar la calidad del código.

:::{figure} https://www.visual-paradigm.com/servlet/editor-content/scrum/the-top-7-popular-agile-development-approaches/sites/7/2018/12/extreme-programming.png
---
width: 90%
name:
---
Tomado de [The Top 7 Popular Agile Development Approaches](https://www.visual-paradigm.com/scrum/the-top-7-popular-agile-development-approaches/).
:::


**Aspectos Importantes**
- Comunicación
- Simplicidad
- Retroalimentación
- Respeto
- Valentía

**Ventajas:**  
- Alta adaptabilidad a los cambios en los requisitos.
- Mejora continua de la calidad del código.

**Desventajas:**  
- Puede ser difícil de implementar en equipos grandes.
- Requiere un alto nivel de disciplina y comunicación.

**Ejemplo Práctico:**  
Desarrollo de aplicaciones web donde los requisitos pueden cambiar con frecuencia y se requieren entregas rápidas.

### 3.2 SCRUM

**Definición:**  
SCRUM es un marco ágil que organiza el desarrollo en sprints, ciclos cortos de trabajo que normalmente duran entre 2 y 4 semanas. SCRUM se centra en la colaboración, la flexibilidad y la entrega constante de valor.


::::{grid}

:::{grid-item}
:margin: auto auto 0 0
:columns: 6

<iframe width="100%" height="280px" src="https://www.youtube.com/embed/TRcReyRYIMg?si=MnXEkEUin5_H12qq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

:::

:::{grid-item}
:margin: auto auto 0 0
:columns: 6

<iframe width="100%" height="280px" src="https://www.youtube.com/embed/2Vt7Ik8Ublw?si=m1DIQ7OWMkgPgN5x" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

:::
::::


**Roles clave:**  
- **Product Owner:** Define las prioridades y gestiona los pendientes (backlog).
- **Scrum Master:** Facilita el proceso SCRUM y elimina obstáculos.
- **Equipo de desarrollo:** Realiza el trabajo necesario para completar las tareas del sprint.

**Eventos clave:**  
- **Sprint Planning:** Planificación del trabajo a realizar en el sprint.
- **Daily Scrum:** Reunión diaria para sincronizar el trabajo y ajustar el plan.
- **Sprint Review:** Revisión del trabajo completado al final del sprint.
- **Sprint Retrospective:** Reflexión sobre el proceso para mejorarlo en el siguiente sprint.


:::{figure} https://www.visual-paradigm.com/servlet/editor-content/scrum/the-top-7-popular-agile-development-approaches/sites/7/2018/12/five-scrum-events.png
---
width: 90%
name: sprint
---
Sprint. Tomado de [The Top 7 Popular Agile Development Approaches](https://www.visual-paradigm.com/scrum/the-top-7-popular-agile-development-approaches/).
:::


:::{figure} https://donetonic.com/wp-content/uploads/2022/10/Procesos-SCRUM-1024x575.png
---
width: 90%
name: scrum
---
Procesos SCRUM. Tomado de [Pasos para configurar tu flujo de trabajo Scrum](https://donetonic.com/es/pasos-para-configurar-tu-flujo-de-trabajo-scrum/).
:::


**Ventajas:**  
- Alta transparencia y visibilidad del progreso.
- Enfoque en la entrega rápida de valor al cliente.

**Desventajas:**  
- Puede ser difícil de aplicar en proyectos donde los requisitos son muy inciertos.
- Requiere un compromiso fuerte del equipo y del Product Owner.

**Ejemplo Práctico:**  
Desarrollo de software comercial donde las prioridades pueden cambiar con frecuencia.

### 3.3 Desarrollo Adaptativo de Software (DAS)

**Definición:**  
DAS es un enfoque ágil que enfatiza la adaptación y la flexibilidad. Está diseñado para proyectos donde los requisitos no se pueden definir por completo desde el principio y pueden cambiar durante el desarrollo.

<p align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/ePNSAIJ9-Ls?si=vZN2g9yn1ESuBaDb" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

**Fases:**  
- **Especulación:** Planificación inicial con la comprensión de que los cambios son inevitables.
- **Colaboración:** Trabajo en equipo para resolver problemas a medida que surgen.
- **Aprendizaje:** Reflexión continua sobre lo que funciona y lo que no.

:::{figure} https://media.geeksforgeeks.org/wp-content/uploads/20240628160315/asd1.webp
---
width: 80%
name: asd
---
Tomado de [What is Adaptive Software Development (ASD)?](https://www.geeksforgeeks.org/adaptive-software-development-asd/).
:::

**Ventajas:**  
- Excelente para proyectos con alta incertidumbre.
- Fomenta la innovación y la experimentación.

**Desventajas:**  
- Puede ser difícil de gestionar si el equipo no está acostumbrado a la incertidumbre.
- Requiere una comunicación constante y efectiva.

**Ejemplo Práctico:**  
Proyectos de I+D donde la innovación y la experimentación son clave.

### 3.4 Desarrollo Impulsado por Características (FDD)

**Definición:**  
FDD es un enfoque ágil que se centra en la entrega de características de software que aportan valor al cliente. El desarrollo se organiza en torno a la construcción de características definidas de manera clara.

<p align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/mmlOgBWLVO4?si=Cw7GwzwoviBpiQTV" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

**Etapas:**  
- **Desarrollo del modelo:** Creación de un modelo general del sistema.
- **Construcción de la lista de características:** Identificación de todas las características del sistema.
- **Planificación por característica:** Definición de un plan de desarrollo basado en la entrega de cada característica.
- **Diseño por característica:** Diseño detallado de cada característica.
- **Construcción por característica:** Desarrollo y prueba de cada característica.

:::{figure} https://lvivity.com/wp-content/uploads/2020/06/fdd-steps.jpg
---
width: 80%
name:
---
Tomado de [7 Things You Need to Know About Feature Driven Development](https://lvivity.com/7-things-about-feature-driven-development).
:::

**Ventajas:**  
- Enfoque en la entrega constante de valor al cliente.
- Adecuado para proyectos donde las características son bien comprendidas y pueden priorizarse.

**Desventajas:**  
- Puede no ser adecuado para proyectos muy complejos o donde las características son difíciles de definir desde el principio.
- Requiere una planificación detallada y una gestión efectiva.

**Ejemplo Práctico:**  
Desarrollo de sistemas de comercio electrónico donde las características clave como el catálogo de productos, el carrito de compras, y el procesamiento de pagos deben ser implementadas de manera prioritaria.

### 3.5 Desarrollo Dinámico de Sistemas (DSDM)

**Definición:**  
DSDM es un enfoque ágil que se centra en la entrega de software funcional en plazos ajustados. Promueve la colaboración, la calidad y la entrega incremental.


::::{grid}

:::{grid-item}
:margin: auto auto 0 0
:columns: 6

<iframe width="100%" height="280px" src="https://www.youtube.com/embed/KIydGplAVo4?si=oTUwi73i11XzeVdY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

:::

:::{grid-item}
:margin: auto auto 0 0
:columns: 6

<iframe width="100%" height="280px" src="https://www.youtube.com/embed/rIlcaPEGpyg?si=1h8zgryBkcdiciy8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

:::
::::

**Principios clave:**  
- **Entrega a tiempo:** Cumplir con los plazos es más importante que completar todas las características.
- **Colaboración:** Trabajar estrechamente con los stakeholders.
- **Entrega incremental:** Entrega de software en pequeños incrementos funcionales.

**Fases:**

- Pre-proyecto
- Estudio de viabilidad
- Estudio de negocio
- Iteración del modelo funcional
- Diseño y construcción de la iteración
- Implementación
- Post-proyecto

:::{figure} https://www.toolsqa.com/gallery/Agile%20-%20Scrum/3.Feasibility-Study-and-Business-Study-in-DSDM.webp
---
width: 80%
name:
---
Tomado de [DSDM : A Step-by-Step-Guide [2019]](https://www.toolsqa.com/agile/dsdm-guide/).
:::

**Ventajas:**  
- Excelente para proyectos con plazos estrictos.
- Enfoque en la entrega rápida de valor.

**Desventajas:**  
- Puede ser difícil de aplicar en proyectos donde la calidad completa es crítica.
- Requiere una fuerte colaboración entre el equipo de desarrollo y los stakeholders.

**Ejemplo Práctico:**  
Proyectos donde el tiempo de comercialización es crítico, como en el desarrollo de productos para mercados muy competitivos.


### 3.6 Proceso Unificado Ágil (AUP)

**Definición:**  
AUP es una simplificación de RUP (Proceso Unificado Racional) que integra principios ágiles, buscando un equilibrio entre la disciplina de RUP y la flexibilidad de los métodos ágiles.  

Es un proceso de desarrollo iterativo e incremental. Las fases de elaboración, construcción y transición se dividen en una serie de iteraciones temporizadas. (En un proyecto de gran envergadura, la fase de inicio también puede dividirse en iteraciones). Cada iteración da lugar a un incremento, que es una versión del sistema que contiene una funcionalidad añadida o mejorada en comparación con la versión anterior. 

<p align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/oFbr-EcWJ4I?si=eVpE1PFtu-Mmsg3C" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

**Fases:**
- **Inicio, Elaboración, Construcción y Transición:** Similares a las fases de RUP, pero con un enfoque en la entrega incremental y continua de valor al cliente.
- **Iteración y Retroalimentación:** Al igual que en otros enfoques ágiles, AUP se basa en la iteración y la retroalimentación continua para ajustar y mejorar el software a medida que avanza el desarrollo.

:::{figure} https://www.slideteam.net/media/catalog/product/cache/1280x720/a/u/aup_software_development_phases_of_each_workflow_in_agile_unified_process_slide01.jpg
---
width: 80%
name:
---

:::

:::{figure} https://upload.wikimedia.org/wikipedia/commons/d/d9/UnifiedProcessProjectProfile20060708.png
---
width: 80%
name:
---

:::


:::{figure} https://www.slideteam.net/media/catalog/product/cache/1280x720/a/u/aup_software_development_7_disciplines_of_agile_unified_process_slide01.jpg
---
width: 80%
name:
---

:::


**Ventajas:**
- **Flexibilidad:** Combina la estructura de un proceso unificado con la adaptabilidad de los métodos ágiles, permitiendo ajustar los requisitos y prioridades a medida que se desarrolla el proyecto.
- **Enfoque en la Calidad:** Mantiene el enfoque en la calidad y en la entrega continua de valor, lo que es especialmente útil en proyectos grandes y complejos.

**Desventajas:**
- **Complejidad:** Aunque es una versión simplificada de RUP, AUP todavía puede ser más complejo que otros métodos ágiles más ligeros como SCRUM.
- **Requiere Disciplina:** Para implementar AUP de manera efectiva, se requiere una disciplina considerable en la planificación y ejecución.

**Ejemplo Práctico:**  
Proyectos de desarrollo de software empresarial que requieren un enfoque más estructurado pero que también necesitan adaptarse rápidamente a los cambios en el mercado o en las necesidades del cliente.

### 3.7 PMI-Ágil

**Definición:**  
PMI-Ágil es una combinación del enfoque tradicional de gestión de proyectos del Project Management Institute (PMI) con principios ágiles. Este enfoque busca integrar las mejores prácticas de la gestión de proyectos con la flexibilidad y adaptabilidad de los métodos ágiles.

<p align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/3DMi4T8Y_Dg?si=dbriJVIfeY3g-4J6" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

**Características Clave:**

- **Integración de Marcos:** Combina prácticas de gestión de proyectos tradicionales, como las contenidas en el PMBOK (Project Management Body of Knowledge), con marcos ágiles como SCRUM, XP, o Kanban.
- **Enfoque en el Valor:** Prioriza la entrega de valor al cliente de manera continua, adaptando el alcance y las prioridades del proyecto según sea necesario.
- **Gestión Híbrida:** Permite que diferentes partes del proyecto se gestionen utilizando enfoques diferentes. Por ejemplo, la planificación global del proyecto podría seguir un enfoque tradicional, mientras que la ejecución podría utilizar métodos ágiles.

**Ventajas:**

- **Flexibilidad:** Permite adaptar el enfoque de gestión a las necesidades específicas del proyecto y del cliente.
- **Mejora de la Comunicación:** Fomenta la colaboración continua entre los equipos y los stakeholders.
- **Mejora en la Gestión de Riesgos:** Combina la previsibilidad y el control de los métodos tradicionales con la adaptabilidad de los métodos ágiles, lo que facilita una mejor gestión de los riesgos.

**Desventajas:**

- **Complejidad:** Requiere una comprensión profunda tanto de las metodologías tradicionales como de las ágiles, lo que puede dificultar su implementación.
- **Resistencia al Cambio:** En organizaciones con una fuerte cultura de gestión de proyectos tradicional, puede haber resistencia a la adopción de prácticas ágiles.

**Ejemplo Práctico:**

Un proyecto de desarrollo de software en una gran organización que utiliza prácticas tradicionales de gestión de proyectos (como la planificación y el control detallado de costos) pero necesita la flexibilidad de los métodos ágiles para adaptarse rápidamente a los cambios en los requisitos del cliente.

**Herramientas y Técnicas:**

- **Agile Project Management (APM):** Una herramienta que combina las prácticas del PMI con la agilidad.
- **Scrum of Scrums:** Una técnica para coordinar múltiples equipos ágiles en un entorno de proyecto más grande.
- **Burn-Down Charts y Burn-Up Charts:** Gráficos utilizados para seguir el progreso del proyecto en entornos ágiles.

**PMI y Certificación:**

- **PMI-ACP (Agile Certified Practitioner):** Una certificación ofrecida por PMI que valida el conocimiento y la experiencia en la gestión de proyectos ágiles.
- **PMBOK Guide - Seventh Edition:** Incluye principios ágiles como parte de las mejores prácticas de gestión de proyectos.

<p align="center">
<iframe width="80%" height="420px" src="https://www.youtube.com/embed/K7YMEFjh724?si=9MDs03hte3nU_ooj" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

### 3.8 Otros

#### Lean Approach

:::{figure} https://www.visual-paradigm.com/servlet/editor-content/scrum/the-top-7-popular-agile-development-approaches/sites/7/2020/01/lean-principles.png
---
width: 100%
name: lean
---
Principios de la metodología Lean.
:::

#### Kanban Board

:::{figure} https://www.visual-paradigm.com/servlet/editor-content/scrum/the-top-7-popular-agile-development-approaches/sites/7/2020/01/kanban-board.png
---
width: 70%
name: kanban
---
Ejemplo de la metodología Kanban Board. Tomado de [The Top 7 Popular Agile Development Approaches](https://www.visual-paradigm.com/scrum/the-top-7-popular-agile-development-approaches/).
::: 


#### DevOps

:::{figure} https://agilefirst.io/content/images/size/w2000/2022/06/agile-devops.png
---
width: 90%
name: devops
---
Ejempo de la metodología DevOps. Tomado de [Agile DevOps](https://agilefirst.io/agile-devops/).
:::

#### Design Thinking

#### Crystal

#### SAFe

## 4. Tabla Comparativa

| **Método** | **Características** | **Ventajas** | **Desventajas** | **Aplicaciones** |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| **Cascada**                         | - Secuencial <br> - Fases claramente definidas (Requisitos, Diseño, Implementación, Verificación, Mantenimiento)                                          | - Fácil de entender y gestionar <br> - Buen control de proyecto <br> - Adecuado para proyectos con requisitos claros y bien definidos                                           | - Difícil de adaptar a cambios <br> - Riesgo de errores tardíos <br> - No se ajusta bien a proyectos con requisitos cambiantes                                                  | - Proyectos con requisitos bien definidos y estables                                                                 |
| **Modelo en V**                     | - Similar a Cascada, pero con pruebas en paralelo <br> - Enfatiza la verificación y validación en cada fase                                              | - Mejora la calidad mediante pruebas continuas <br> - Estructura clara y organizada <br> - Buena trazabilidad entre desarrollo y pruebas                                        | - Similar a Cascada en términos de falta de flexibilidad <br> - No se adapta bien a proyectos con cambios frecuentes en los requisitos                                          | - Proyectos críticos en los que la validación es clave                                                                  |
| **RUP (Proceso Unificado Racional)**| - Iterativo e incremental <br> - Cuatro fases principales: Inicio, Elaboración, Construcción, Transición <br> - Fuerte enfoque en la arquitectura         | - Adaptable a diferentes tipos de proyectos <br> - Buen manejo de riesgos <br> - Enfoque iterativo que permite ajustes continuos                                               | - Complejidad en la implementación <br> - Requiere un esfuerzo considerable en documentación <br> - Puede ser costoso                                                          | - Proyectos de software grandes y complejos                                                                            |
| **XP (Extreme Programming)**        | - Ágil <br> - Fomenta la colaboración intensa <br> - Desarrollo en iteraciones cortas <br> - Pruebas unitarias continuas                                  | - Alta calidad de código <br> - Flexibilidad y capacidad de respuesta a cambios <br> - Entrega rápida y continua de software funcional                                           | - Requiere alta participación del cliente <br> - Puede ser difícil de gestionar en equipos grandes <br> - Alto grado de disciplina y comunicación necesaria                     | - Proyectos de desarrollo de software pequeños a medianos, con requisitos cambiantes                                    |
| **SCRUM**                           | - Ágil <br> - Basado en sprints de duración fija <br> - Roles definidos (Scrum Master, Product Owner, Equipo de Desarrollo)                                | - Fomenta la adaptabilidad y la entrega continua <br> - Mejora la transparencia y la comunicación <br> - Incrementos funcionales regulares                                      | - Puede ser difícil de escalar en proyectos muy grandes <br> - Requiere un cambio cultural y organizacional para su implementación efectiva                                     | - Proyectos donde los requisitos pueden cambiar frecuentemente                                                            |
| **DAS (Desarrollo Ágil de Software)**| - Ágil <br> - Iterativo e incremental <br> - Fuerte enfoque en la colaboración y el cliente                                                              | - Fomenta la adaptabilidad y la entrega continua <br> - Mejora la transparencia y la comunicación <br> - Flexibilidad en la respuesta a cambios                                  | - Requiere alta participación del cliente <br> - Puede ser difícil de gestionar en equipos grandes <br> - No es adecuado para proyectos con requisitos muy estables            | - Proyectos que requieren una entrega rápida y adaptación continua                                                      |
| **Desarrollo Dinámico de Sistemas** | - Ágil <br> - Iterativo e incremental <br> - Fuerte enfoque en la colaboración y la flexibilidad                                                          | - Flexible y adaptable a cambios <br> - Participación activa de los usuarios <br> - Enfocado en la entrega de valor                                                              | - Requiere alta participación del cliente <br> - Puede ser difícil de gestionar en equipos grandes <br> - No es adecuado para proyectos con requisitos muy estables            | - Proyectos con un enfoque en la entrega rápida de valor                                                                  |
| **Impulsado por Características**   | - Ágil <br> - Basado en el desarrollo y entrega de características individuales <br> - Enfocado en la funcionalidad específica                           | - Fomenta la adaptabilidad y la entrega continua <br> - Mejora la transparencia y la comunicación <br> - Flexibilidad en la respuesta a cambios                                  | - Requiere alta participación del cliente <br> - Puede ser difícil de gestionar en equipos grandes <br> - No es adecuado para proyectos con requisitos muy estables            | - Proyectos que requieren una entrega rápida y adaptación continua                                                      |
| **Proceso Unificado Ágil (AUP)**    | - Iterativo e incremental <br> - Basado en RUP con principios ágiles <br> - Fases de inicio, elaboración, construcción, transición                         | - Combina estructura con flexibilidad <br> - Buen manejo de riesgos <br> - Ajustes continuos en respuesta a cambios                                                             | - Más complejo que otros métodos ágiles <br> - Requiere disciplina en la planificación y ejecución <br> - Puede ser costoso en tiempo y recursos                              | - Proyectos grandes y complejos que requieren estructura pero con necesidad de adaptabilidad                              |
| **PMI-Ágil**                        | - Híbrido <br> - Combina prácticas tradicionales de PMI con principios ágiles <br> - Integración de PMBOK con SCRUM, XP, y otros marcos ágiles              | - Flexibilidad para adaptarse a diferentes proyectos <br> - Mejora en la gestión de riesgos <br> - Buena comunicación y colaboración continua                                    | - Requiere comprensión profunda de ambas metodologías <br> - Complejidad en su implementación <br> - Posible resistencia en entornos tradicionales                            | - Proyectos grandes y complejos en entornos empresariales                                                                 |

Esta tabla proporciona una visión general de las diferencias y similitudes entre los diversos métodos de desarrollo de software, facilitando la elección del enfoque más adecuado según las características específicas del proyecto.


## Conclusión

La clase sobre métodos de desarrollo de software ha explorado un amplio espectro de enfoques, desde los tradicionales como el modelo en cascada y el modelo en V, hasta los ágiles como SCRUM y XP, incluyendo también enfoques híbridos como PMI-Ágil y AUP. Cada método tiene sus propias fortalezas y debilidades, lo que resalta la importancia de seleccionar el enfoque adecuado para cada proyecto en función de factores como el tamaño del proyecto, la claridad de los requisitos, y la necesidad de adaptabilidad.

En un entorno de desarrollo de software cada vez más dinámico y complejo, comprender estos métodos es esencial para gestionar proyectos de manera efectiva, asegurando la entrega de valor al cliente y la satisfacción de los requisitos de calidad y tiempo. Los estudiantes deben estar preparados para aplicar estos conocimientos en situaciones del mundo real, seleccionando y adaptando el método de desarrollo más adecuado para cada circunstancia, contribuyendo así al éxito de los proyectos de software.

## Ejercicio

::::{admonition} Taller 2
Basados en el problema del proyecto asignado, seleccionen una metodología tradicional y 3 metodologías ágil para diseñar una solución al problema. De ser necesario inventen los requisitos y emulen los roles que se necesitan para cada metodología. 
::::

## Recursos Adicioanles

- [Project Management Institute - Agile Certified Practitioner (PMI-ACP)](https://www.pmi.org/certifications/agile-acp)
- [PMI's Pulse of the Profession](https://www.pmi.org/learning/thought-leadership/pulse)