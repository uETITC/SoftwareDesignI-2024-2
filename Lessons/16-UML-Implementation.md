# Diagramas de Despliegue / Implementación

## Introducción  
Los diagramas de implementación son una herramienta esencial en el diseño de software, ya que permiten representar cómo los componentes de un sistema se implementan físicamente en hardware o software. A través de esta clase, exploraremos su definición, propiedades, usos, ejemplos y aplicaciones en proyectos reales.

## Definición  
Un diagrama de implementación es un tipo de diagrama UML (Unified Modeling Language) que ilustra la distribución física de los artefactos de software en nodos de hardware o dispositivos. Estos diagramas representan cómo los componentes de software interactúan con los elementos de hardware, así como las relaciones entre ellos.

<div align="center">
  <iframe width="80%" height="420px" src="https://www.youtube.com/embed/nTtQwGoUUNc?si=OMqXCiZbP8yNyQTq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>


## Propiedades  
1. **Representación física**: Muestra la disposición de los elementos de software en nodos de hardware reales.  
2. **Artefactos y nodos**: Los artefactos representan unidades de software, como archivos ejecutables o bibliotecas. Los nodos representan dispositivos de hardware o ambientes de ejecución.  
3. **Relaciones y dependencias**: Define conexiones entre nodos y artefactos para indicar dependencias físicas o lógicas.  

## Sintaxis  
Un diagrama de implementación utiliza los siguientes elementos:  
- **Nodos**: Representados como cajas tridimensionales, indican dispositivos de hardware o ambientes de ejecución.  
- **Artefactos**: Representados como rectángulos, muestran componentes de software.  
- **Conexiones**: Líneas que representan asociaciones o dependencias entre nodos y artefactos.  
- **Estereotipos**: Notaciones adicionales que añaden significado, como `<<server>>` o `<<database>>`.

::::{grid}

:::{grid-item}
:margin: auto auto 0 0
:columns: 6

```{figure} ../../images/Figure5.17.png
---
width: 80% 
name: artefactos
---
Notación de Artefactos para `HeatingController.exe`.
```

:::

:::{grid-item}
:margin: auto auto 0 0
:columns: 6

```{figure} ../../images/Figure5.18.png
---
width: 80% 
name: notods
---
Notación para dos nodos conectados.
```

:::
::::


## Usos  
1. Modelar arquitecturas físicas de sistemas distribuidos.  
2. Documentar la infraestructura de despliegue de un sistema.  
3. Identificar dependencias críticas entre hardware y software.  
4. Facilitar la planificación del despliegue y la integración de sistemas.  

## Ejemplos  

### 1. **Sistema web**:  
   - Nodos: Servidor web, servidor de base de datos y cliente.  
   - Artefactos: Archivo WAR para el servidor web, esquema SQL para la base de datos.  

```text
+------------------+             +--------------------+
|  <<Server>>      |             |  <<Database>>      |
|  Web Server      |             |  DB Server         |
|  - myApp.war     |             |  - schema.sql      |
+------------------+             +--------------------+
         |                                |
         |          Connection            |
         +--------------------------------+
```

### 2. **Aplicación móvil**:  
   - Nodos: Dispositivo móvil y servidor backend.  
   - Artefactos: APK de la aplicación y API REST en el backend.  

```text
+------------------+             +---------------------+
| <<Device>>       |             |  <<Server>>         |
|  Mobile Device   |             |  Backend Server     |
|  - app.apk       |             |  - api.jar          |
+------------------+             +---------------------+
         |                                |
         |       API Communication        |
         +--------------------------------+
```

### 3. Sistema de Control de Ambiente

```{figure} ../../images/Figure5.19.png
---
width: 70% 
name: EnvironmentalControlSystem
---
Ejemplo de un sistema de control de ambiente, `EnvironmentalControlSystem`.
```

### 4. Aplicación Web

```{figure} https://www.uml-diagrams.org/examples/deployment-example-web-network.png
---
width: 100% 
name: aplicacionweb
---
Un ejemplo de diagrama de red para aplicación web con configuración DMZ de dos cortafuegos.
```

### 5. Cliente / Servidor

```{figure} https://cdn-images.visual-paradigm.com/guide/uml/what-is-deployment-diagram/05-deployment-diagram-tcpip-example.png
---
width: 100% 
name: corporate
---
Ejemplo de cliente / servidor TCP/IP.
```


### 6. Servidor Bancario

```{figure} https://templates.visual-paradigm.com/repository/images/be5d1c7f-5879-4942-b090-e3d9160b7f79/deployment-diagram-design/uml-deployment-diagram-mortgage-application.png
---
width: 100% 
name: bank
---
Arquitectura de un sistema distribuido de solicitud de hipotecas.
```

## Aplicaciones  

- **Ingeniería de software**: Documentar el despliegue en proyectos de desarrollo de software.  
- **DevOps**: Planificar la integración continua y la implementación continua (CI/CD).  
- **Infraestructura TI**: Diseñar sistemas distribuidos con múltiples servidores y redes.  
- **Análisis de riesgos**: Identificar vulnerabilidades en la comunicación entre nodos.  

## Ejercicio

::::{admonition} Taller
## Diseño del Despliegue de una Aplicación de Streaming de Música  

Imagina que estás trabajando en un equipo de desarrollo que diseña una aplicación de streaming de música para jóvenes. El sistema debe permitir a los usuarios escuchar canciones en línea, crear playlists, y descargar música para escuchar sin conexión. 

La infraestructura debe incluir:  
- Una aplicación móvil (cliente).  
- Un servidor backend para la lógica de negocio.  
- Un servidor de base de datos para almacenar las canciones, las playlists y la información de los usuarios.  
- Un sistema de almacenamiento en la nube para alojar los archivos de música.

**Instrucciones:**  
1. Diseña un **diagrama de implementación** que represente la infraestructura del sistema.  
2. Incluye los nodos y artefactos necesarios, como la aplicación móvil, los servidores, y las conexiones entre ellos.  
3. Asegúrate de identificar estereotipos relevantes (ejemplo: `<<Mobile App>>`, `<<Cloud Storage>>`).  
4. Representa las dependencias entre los componentes, como la conexión de la aplicación móvil con el backend y la integración del backend con el almacenamiento en la nube.  

**Puntos clave para el diagrama:**  
- **Nodos requeridos**:  
  - Cliente móvil.  
  - Servidor backend.  
  - Servidor de base de datos.  
  - Servidor de almacenamiento en la nube.  

- **Artefactos a incluir**:  
  - Archivo APK de la aplicación móvil (`musicApp.apk`).  
  - Archivo JAR para el backend (`musicAPI.jar`).  
  - Esquema de base de datos (`db_schema.sql`).  
  - Archivos de música alojados en la nube (`songs.zip`).  

:::{tip}
Agreguen elementos (artefactos, nodos, requisitos, etc) que sean pertinentes para mejoren el diagrama.
:::

**Entrega:**  
- Realiza el diagrama utilizando una herramienta como Lucidchart o Draw.io.  
- Describe brevemente las conexiones entre los nodos y justifica las decisiones de diseño.  

**Preguntas para reflexionar:**  
1. ¿Cómo aseguraste que el sistema es escalable y seguro?  
2. ¿Qué otras tecnologías podrías incluir para mejorar la experiencia del usuario?  
3. ¿Qué sucedería si uno de los nodos fallara? ¿Cómo lo resolverías?
::::

## Conclusiones  

Los diagramas de implementación son herramientas poderosas para entender y documentar cómo un sistema de software interactúa con su entorno físico. Su uso facilita la comunicación entre desarrolladores, arquitectos y administradores de infraestructura, asegurando una implementación eficiente y alineada con los requisitos del proyecto.

## Recursos Adicionales


### Guías y Tutoriales
- [What is Deployment Diagram?](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-deployment-diagram/)
- [UML 2 Tutorial - Deployment Diagram](https://sparxsystems.com/resources/tutorials/uml2/deployment-diagram.html)
- [Deployment Diagrams Overview - UML 2.5](https://www.uml-diagrams.org/deployment-diagrams-overview.html)
- [Deployment Diagrams: Purpose, Components, and Best Practices](https://www.archimetric.com/deployment-diagrams-purpose-components-and-best-practices/)

### Videos

- [Creación de diagramas de despliegue](https://www.youtube.com/watch?v=n3xKtvnzMjo)
- [Diagrama de Despliegue - 22 - Tutorial UML en español ](https://www.youtube.com/watch?v=NSB0ATJUavA)