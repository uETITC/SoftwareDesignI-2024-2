# 3. Gestión de una Biblioteca

## Introducción
En este taller, diseñaremos y comprenderemos tres tipos fundamentales de diagramas UML: **diagrama de estado**, **diagrama de despliegue**, y **diagrama de colaboración**, utilizando como caso de estudio un sistema digital de gestión para una biblioteca. Este sistema permite a los usuarios realizar diversas acciones como buscar, reservar, devolver libros, y gestionar su cuenta. La aplicación opera en una arquitectura distribuida de tres capas, con un servidor central que se conecta a una base de datos, accesible desde dispositivos de los usuarios.

## Objetivo
- Comprender la importancia y la estructura de los diagramas UML mencionados.
- Diseñar una solución funcional que modele el flujo de estados, la arquitectura técnica y la colaboración entre los componentes del sistema.
## Parte 1: Diagrama de Estado

### Descripción
El diagrama de estado modelará los posibles estados por los que pasa un **libro** dentro del sistema de la biblioteca y las transiciones entre estos estados, según los eventos.

### Requisitos
1. **Identifica los elementos clave**: El foco será el objeto **libro** dentro del sistema.
2. **Lista los estados posibles**:
   - Estado inicial: *Disponible*.
   - Estados intermedios: *Reservado*, *Prestado*, *En mantenimiento*.
   - Estado final: *Eliminado*.
3. **Define eventos de transición**:
   - *Reserva realizada*: cambia de "Disponible" a "Reservado".
   - *Préstamo aprobado*: cambia de "Reservado" a "Prestado".
   - *Devolución*: cambia de "Prestado" a "Disponible".
   - *Reporte de daño*: cambia de "Prestado" a "En mantenimiento".
4. **Condicionales**:
   - Un libro no puede ser reservado si ya está reservado o prestado.
   - Solo los usuarios autenticados pueden reservar o prestar libros.
   - Libros dañados solo pueden ser reparados por administradores.
5. **Incluye estados inicial y final**.
6. **Esquematiza las transiciones** mediante flechas con eventos claramente indicados.
## Parte 2: Diagrama de Despliegue

### Descripción
El diagrama de despliegue representará cómo el sistema de la biblioteca está distribuido en nodos físicos y cómo se conectan entre sí.

### Requisitos
1. **Nodos físicos**:
   - Un servidor central que aloja la aplicación web y APIs.
   - Una base de datos para almacenar la información de los libros, usuarios y transacciones.
   - Dispositivos del usuario final (laptops, smartphones).
2. **Artefactos**:
   - **Servidor central**:
     - Backend implementado en un framework como Django o Node.js.
     - APIs REST para comunicación cliente-servidor.
   - **Base de datos**:
     - Tablas para libros, usuarios y transacciones.
   - **Dispositivos del usuario**:
     - Frontend ejecutado en navegadores web o apps móviles.
3. **Conexiones**:
   - Dispositivos de usuarios interactúan con el servidor mediante HTTPS.
   - El servidor se conecta a la base de datos a través de una red interna segura.
4. **Detalles adicionales**:
   - Seguridad: Autenticación de usuarios (JWT o OAuth).
   - Rendimiento: Caching para reducir tiempos de respuesta en búsquedas.
   - Multiplicidad: Se permite una conexión simultánea de hasta 100 usuarios por servidor.
5. **Representar gráficamente** las conexiones entre nodos.
## Parte 3: Diagrama de Colaboración

### Descripción
El diagrama de colaboración modelará el proceso de **reserva de un libro** por parte de un usuario.

### Requisitos
1. **Caso de uso**: Modelar la interacción para que un usuario reserve un libro.
2. **Actores y objetos**:
   - Actores principales: *Usuario (lector)* y *Administrador del sistema* (en caso de conflictos).
   - Objetos: Frontend, backend, base de datos.
3. **Secuencia de interacciones**:
   - El usuario inicia sesión y solicita reservar un libro desde el frontend.
   - El frontend envía la solicitud al backend.
   - El backend verifica:
     - Si el libro está disponible.
     - Si el usuario tiene permisos y no excedió el límite de reservas.
   - Si es válido:
     - El backend actualiza el estado del libro en la base de datos.
     - Devuelve una confirmación al frontend.
   - Si no es válido:
     - El backend envía un mensaje de error.
   - El frontend muestra al usuario el resultado.
4. **Restricciones**:
   - Máximo 5 libros reservados por usuario.
   - Reservas expiran tras 48 horas si no se completan.
5. **Representación gráfica**:
   - Incluye líneas de comunicación entre los objetos.
   - Los mensajes deben estar numerados, con al menos 5 interacciones en total.
### Entregables
- Un diagrama de estado claro y completo para el flujo de estados del libro.
- Un diagrama de despliegue que represente los nodos, artefactos y sus relaciones.
- Un diagrama de colaboración que modele la interacción para la funcionalidad de reserva.
