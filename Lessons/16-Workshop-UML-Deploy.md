# Taller

## Tema Principal

Diagrama de despliegue para una aplicación web de anime.

## Introducción al Ejercicio

La construcción de aplicaciones web requiere entender no solo la lógica interna del sistema, sino también cómo se distribuyen sus componentes en diferentes servidores y dispositivos. En este ejercicio, diseñarás un **diagrama de despliegue UML** para una aplicación web que permite a los usuarios explorar, buscar y gestionar información sobre animes. Este diagrama debe representar los nodos (servidores, bases de datos, dispositivos) y sus conexiones, destacando cómo interactúan para soportar las funcionalidades de la aplicación.

## Requisitos del Sistema

La aplicación web debe cumplir con los siguientes requisitos básicos:

1. Los usuarios pueden buscar animes por título, género o popularidad.
2. Los usuarios registrados pueden crear listas de "animes por ver".
3. La aplicación debe almacenar información en una base de datos.
4. La funcionalidad de búsqueda utiliza una API externa para obtener datos actualizados sobre animes.
5. La aplicación debe ser accesible desde navegadores web y dispositivos móviles.

## Instrucciones del Ejercicio

### 1. **Establecer los nodos del sistema:**  
   Identifica los elementos físicos o lógicos que participan en el despliegue del sistema, como:
   - Servidor web.
   - Base de datos.
   - API externa.
   - Navegadores web y dispositivos móviles de los usuarios.

### 2. **Modelar las conexiones:**  
   Define cómo los nodos interactúan entre sí. Por ejemplo:
   - Conexión HTTP entre el navegador y el servidor web.
   - Conexión segura (HTTPS) para el consumo de la API externa.
   - Interacción entre el servidor web y el sistema de base de datos.

### 3. **Especificar las tecnologías involucradas:**  
   En cada nodo, indica las tecnologías utilizadas. Por ejemplo:
   - Servidor web: Tomcat o Spring Boot.
   - Base de datos: MySQL o PostgreSQL.
   - API: API de terceros como MyAnimeList o AniList.

### 4. **Diseñar el diagrama de despliegue UML:**  
   Usa notación UML para representar:
   - **Nodos** como cajas tridimensionales (ej.: servidor, base de datos, dispositivo).
   - **Componentes internos** del servidor (controladores, servicios, etc.).
   - **Conexiones** entre nodos con etiquetas que indiquen el protocolo (HTTP, HTTPS, JDBC, etc.).

## Criterios de Evaluación

- Correcta identificación de los nodos y sus roles.
- Representación clara de las conexiones y flujos de datos entre los nodos.
- Inclusión de tecnologías relevantes para el desarrollo web.
- Coherencia en la sintaxis del diagrama UML.

## Escenario Detallado

Imagina que la aplicación web de anime tiene los siguientes componentes específicos:

1. **Frontend:**  
   Una interfaz desarrollada con HTML, CSS, y JavaScript que interactúa con el servidor a través de AJAX o REST APIs.

2. **Backend:**  
   Un servidor web desarrollado en Java usando Spring Boot (o Tomcat, Wildfly, etc). Este servidor gestiona solicitudes, consultas a la base de datos, y el consumo de la API externa.

3. **Base de Datos:**  
   Una base de datos MySQL que almacena información sobre usuarios registrados, listas de animes, y búsquedas recientes.

4. **API Externa:**  
   Se utiliza una API externa como MyAnimeList para obtener información sobre animes que no están en la base de datos local.

5. **Dispositivos de los Usuarios:**  
   Los usuarios pueden acceder a la aplicación desde navegadores web y dispositivos móviles.

## Producto Final

Al finalizar este ejercicio, deberás entregar:

1. **Diagrama de despliegue UML:**  
   Representa gráficamente los nodos, componentes y conexiones.

2. **Descripción textual del diagrama:**  
   Explica cada nodo y su función, así como las tecnologías utilizadas.

## Ejemplo de Descripción para el Diagrama

- **Servidor Web:** Implementado en Spring Boot, se encarga de recibir solicitudes de los usuarios, procesar datos y enviarlos al frontend.  
- **Base de Datos MySQL:** Almacena información estructurada sobre los usuarios y sus listas de anime.  
- **Dispositivo del Usuario:** Navegadores o aplicaciones móviles que permiten a los usuarios interactuar con el sistema.  
- **API Externa:** Proporciona datos adicionales sobre animes no almacenados en la base de datos interna.  

## Ejercicio

::::{admonition} Taller
Realizar el taller completo siguiendo las instrucciones. Pueden hacerlo el Lucidchart Draw.io o donde gusten. Deben subir un archivo en formato markdown con el diagrama y un texto corto que describa el diagrama, también pueden subir un enlace a GitHub con el archivo.

:::{tip}
Si optan por subir el archivo markdown no olviden subir la imagen.
:::
::::

## Conclusión

Este ejercicio te permitirá comprender cómo se despliega una aplicación web en un entorno real y cómo los componentes interactúan físicamente. Al final, serás capaz de diseñar un diagrama de despliegue coherente y profesional que refleje el funcionamiento de un sistema completo.

## Recursos Adicionales

- [Deployment Diagrams Overview - UML 2.5](https://www.uml-diagrams.org/deployment-diagrams-overview.html)