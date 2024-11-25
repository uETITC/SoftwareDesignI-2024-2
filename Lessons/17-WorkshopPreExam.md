# Taller: Gestión de Notas

## Introducción
En este taller, diseñaremos y comprenderemos tres tipos fundamentales de diagramas UML: **diagrama de estado**, **diagrama de despliegue**, y **diagrama de colaboración**, utilizando como caso de estudio una página web de una universidad. Esta página permite a los usuarios gestionar notas de estudiantes (subir, eliminar, modificar, consultar). La aplicación se ejecuta en un servidor centralizado de la universidad y accede a una base de datos, permitiendo a los usuarios acceder desde dispositivos diversos.

En cualquier aplicación se busca que su arquitectura sea de tres capas, es decir, que existan al menos 3 entidades que interactúan en el intercambio de datos. Podría pensarse con que existan 3 dispositivos con funcionalidades específicas:

:::{figure} https://www.zirous.com/wp-content/uploads/2022/10/Untitled-5-01.png.webp
---
name: tresCapas
width: 80%
---
Ejemplo de arquitectura de 3 capas. Tomado de [Three-Tier Architecture Approach for Custom Applications](https://www.zirous.com/2022/11/15/three-tier-architecture-approach-for-custom-applications-2/).
:::

## Objetivo
- Aprender la importancia y estructura de cada tipo de diagrama UML.
- Aplicar los conceptos al diseño de una solución funcional para una aplicación real.
   Generar un entendimiento claro del flujo de estados, despliegue técnico y colaboración entre elementos del sistema.

## Parte 1: Diagrama de Estado

### Descripción
El diagrama de estado modela los posibles estados del sistema o de un componente específico (como una entidad usuario o nota) y cómo transitan entre ellos según los eventos.

### Instrucciones
1. **Identifica los elementos clave**: Determina qué entidad será el foco del diagrama (por ejemplo, una "Nota").
2. **Lista los estados posibles**: Documenta todos los estados relevantes por los que puede pasar el objeto "Nota". Ejemplo:
   - Estado inicial (e.g., *Nota no creada*).
   - Estados intermedios (e.g., *Nota guardada*, *Nota editada*).
   - Estado final (e.g., *Nota eliminada*).
   - Estado inexistente (e.g., *Nota no existe*)
3. **Define los eventos de transición**: Describe las acciones o condiciones que provocan el cambio de un estado a otro, como:
   - **Creación de una nueva nota:** Un evento "subir nota" puede llevar a la transición del estado "inexistente" a "creada". 
   - **Modificación de contenido:** Un evento "editar" puede cambiar el estado de "creada" a "modificada".  
   - **Eliminación de una nota:** Un evento "eliminar" cambiará el estado de "creada" o "modificada" a "eliminada".
4. **Incluir estados inicial y final**:  
   - Marca claramente el estado inicial (por ejemplo, **inexistente**) y los posibles estados finales (como **eliminada** o cualquier estado terminal).
  
5. **Agrega condiciones**: Si alguna transición depende de una regla (e.g., permisos del usuario), asegúrate de indicarlo. Agregar al menos 3 condicionales.
6. **Esquematiza las transiciones**: Conecta los estados entre sí mediante líneas, indicando los eventos y condiciones asociadas.

## Parte 2: Diagrama de Despliegue

### Descripción
El diagrama de despliegue representa la arquitectura física del sistema, mostrando cómo se distribuyen los componentes de software en hardware.

### Instrucciones
1. **Identifica los nodos físicos**:
   - **Servidor** de la universidad que aloja la aplicación.
   - **Base de datos** donde se almacenan las notas.
   - **Dispositivos del usuario** (e.g., laptops, smartphones, tablets).
2. **Establecer los artefactos**:  
   - Relaciona los artefactos de software con los nodos físicos:  
     - El **servidor de la universidad** contiene el sistema web, y las APIs.  
     - La **base de datos** contiene los códigos de la creación y población de las tablas y consultas
     - Los **dispositivos de usuario** ejecutan un navegador o una aplicación cliente que interactúa con el servidor.  
3. **Establece conexiones**: Define cómo se comunican estos nodos. Ejemplo:
   - Los usuarios acceden al servidor mediante HTTP/HTTPS.
   - El servidor se conecta con la base de datos mediante una red interna segura.
4. **Desglosa componentes del software**:
   - Servidor web (por ejemplo, un backend en Node.js, Tomcat, o Django).
   - Frontend accesible desde navegadores.
   - API REST para la comunicación entre cliente y servidor.
4. **Define las relaciones**: Representa cómo los nodos interactúan entre sí, describiendo protocolos y mecanismos de comunicación. Pueden agregar la multiplicidad.
5. **Incluye detalles de seguridad y rendimiento**:
   - Mecanismos de autenticación para los usuarios.
   - Firewall o servicios de protección en la comunicación servidor-usuario.

## Parte 3: Diagrama de Colaboración

### Descripción
El diagrama de colaboración (o de interacción) muestra cómo los objetos del sistema interactúan para cumplir una funcionalidad específica. En este caso, modelaremos el proceso de **modificación de una nota**.

### Instrucciones
1. **Define el caso de uso**: Selecciona una funcionalidad (e.g., modificar una nota) y detalla los pasos necesarios para que ocurra.
2. **Identifica los actores y objetos**:
   - Actores principales (e.g., profesor, estudiante, administrador del sistema).
   - Objetos del sistema involucrados (e.g., frontend, backend, base de datos).
3. **Secuencia de interacciones**:
   - Detalla cómo el actor inicia la interacción (e.g., el usuario solicita la modificación).
   - Explica cómo los componentes colaboran:
     - El frontend envía la solicitud al backend.
     - El backend valida la solicitud y consulta la base de datos.
     - La base de datos actualiza la información.
     - El backend devuelve una respuesta al frontend.
     - El frontend informa al usuario.
4. **Representación gráfica**:
   - Establece una relación directa entre los objetos mediante líneas de comunicación.
   - Indica el flujo de mensajes en un orden lógico y claro.
