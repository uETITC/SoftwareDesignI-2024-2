# Supletorio: Gestión de Pedidos de Comida

## Introducción
En este taller, diseñaremos y comprenderemos tres tipos fundamentales de diagramas UML: **diagrama de estado**, **diagrama de despliegue**, y **diagrama de colaboración**, utilizando como caso de estudio un sistema digital de gestión para pedidos de comida. Este sistema permite a los usuarios realizar diversas acciones como seleccionar platillos, realizar pedidos, monitorear el estado de sus órdenes y gestionar sus cuentas. La aplicación opera en una arquitectura distribuida de tres capas, con un servidor central que conecta a una base de datos, accesible desde dispositivos de los usuarios y un sistema de cocina.

## Objetivo
- Comprender la importancia y la estructura de los diagramas UML mencionados.
- Diseñar una solución funcional que modele el flujo de estados, la arquitectura técnica y la colaboración entre los componentes del sistema.

---

## Parte 1: Diagrama de Estado

### Descripción
El diagrama de estado modelará los posibles estados por los que pasa un **pedido** dentro del sistema y las transiciones entre estos estados según los eventos.

### Requisitos
1. **Identifica los elementos clave**: El foco será el objeto **pedido** dentro del sistema.
2. **Lista los estados posibles**:
   - Estado inicial: *Pendiente*.
   - Estados intermedios: *En preparación*, *Listo para entrega*, *En camino*.
   - Estado final: *Entregado* o *Cancelado*.
3. **Define eventos de transición**:
   - *Pedido confirmado*: cambia de "Pendiente" a "En preparación".
   - *Preparación finalizada*: cambia de "En preparación" a "Listo para entrega".
   - *Pedido recogido por repartidor*: cambia de "Listo para entrega" a "En camino".
   - *Pedido entregado*: cambia de "En camino" a "Entregado".
   - *Cancelación del pedido*: cambia de "Pendiente" o "En preparación" a "Cancelado".
4. **Condicionales**:
   - Un pedido no puede ser cancelado si ya está "Listo para entrega" o en estados posteriores.
   - Solo los usuarios autenticados pueden realizar y monitorear pedidos.
   - Pedidos en estado "Cancelado" no pueden reactivarse.
5. **Incluye estados inicial y final**.
6. **Esquematiza las transiciones** mediante flechas con eventos claramente indicados.

---

## Parte 2: Diagrama de Despliegue

### Descripción
El diagrama de despliegue representará cómo el sistema de gestión de pedidos está distribuido en nodos físicos y cómo se conectan entre sí.

### Requisitos
1. **Nodos físicos**:
   - Un servidor central que aloja la aplicación web y APIs.
   - Una base de datos para almacenar información de los usuarios, pedidos y el menú.
   - Dispositivos del usuario final (laptops, smartphones).
   - Dispositivos en la cocina (tablets o pantallas para los cocineros).
   - Dispositivos para repartidores (smartphones).
2. **Artefactos**:
   - **Servidor central**:
     - Backend implementado en un framework como Django o Express.js.
     - APIs REST para comunicación cliente-servidor.
   - **Base de datos**:
     - Tablas para usuarios, pedidos, estados de pedidos y menú.
   - **Dispositivos del usuario**:
     - Frontend ejecutado en navegadores web o apps móviles.
   - **Dispositivos de cocina**:
     - Interfaz simplificada para recibir y actualizar el estado de los pedidos.
3. **Conexiones**:
   - Los dispositivos de usuarios y cocina interactúan con el servidor mediante HTTPS.
   - El servidor se conecta a la base de datos a través de una red interna segura.
4. **Detalles adicionales**:
   - Seguridad: Autenticación de usuarios y repartidores mediante JWT.
   - Rendimiento: Uso de caching para el menú y actualizaciones en tiempo real mediante WebSockets.
   - Escalabilidad: Uso de servidores en la nube para soportar alta concurrencia.
5. **Representar gráficamente** las conexiones entre nodos.

---

## Parte 3: Diagrama de Colaboración

### Descripción
El diagrama de colaboración modelará el proceso de **realizar un pedido** por parte de un usuario.

### Requisitos
1. **Caso de uso**: Modelar la interacción para que un usuario seleccione platillos y realice un pedido.
2. **Actores y objetos**:
   - Actores principales: *Usuario* y *Cocinero*.
   - Objetos: Frontend, backend, base de datos, dispositivo de cocina.
3. **Secuencia de interacciones**:
   - El usuario inicia sesión y selecciona platillos desde el frontend.
   - El frontend envía la solicitud del pedido al backend.
   - El backend verifica:
     - Si los platillos seleccionados están disponibles.
     - Si el usuario tiene métodos de pago registrados.
   - Si es válido:
     - El backend registra el pedido en la base de datos.
     - Envía la orden al dispositivo de cocina.
     - Devuelve una confirmación al frontend.
   - Si no es válido:
     - El backend envía un mensaje de error.
   - El frontend muestra al usuario el resultado.
4. **Restricciones**:
   - Los usuarios solo pueden realizar un pedido activo a la vez.
   - Los pedidos deben confirmarse en un tiempo límite de 15 minutos tras ser creados.
5. **Representación gráfica**:
   - Incluye líneas de comunicación entre los objetos.
   - Los mensajes deben estar numerados, con al menos 5 interacciones en total.

---

### Entregables
- Un diagrama de estado claro y completo para el flujo de estados del pedido.
- Un diagrama de despliegue que represente los nodos, artefactos y sus relaciones.
- Un diagrama de colaboración que modele la interacción para la funcionalidad de realizar un pedido.