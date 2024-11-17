# Segundo

## Tema del Parcial

Implementación de un Gestión de Animes en una Página Web.

## Instrucciones
En este examen, se evaluará tu comprensión sobre la gestión de animes en un sistema web utilizando diferentes diagramas UML (clases, objetos, actividades, y casos de uso). Además, se te proporcionará un código en Java que deberás analizar, pero **no necesitas ejecutarlo**. Debes demostrar tu capacidad para interpretar el código, crear diagramas coherentes y entender cómo interactúan los elementos del sistema. Sigue las instrucciones paso a paso y asegúrate de cumplir con todos los requerimientos.

## Contexto del Sistema
Se te pide modelar y analizar un sistema para la gestión de animes en una página web. El sistema debe permitir a los usuarios ver listas de animes, registrarse, iniciar sesión, agregar animes a su lista de favoritos, y dejar comentarios sobre ellos.

## Requerimientos
1. **Usuarios**: Pueden registrarse, iniciar sesión, buscar animes, agregarlos a favoritos, y dejar comentarios.
2. **Administradores**: Pueden agregar, editar y eliminar animes, así como gestionar comentarios inapropiados.
3. **Animes**: Cada anime tiene título, género, número de episodios, y descripción.
4. **Comentarios**: Los usuarios pueden dejar comentarios sobre los animes.


## Sección 1: Diagrama de Clases 

### Requerimientos
Dibuja un **Diagrama de Clases UML** que modele las siguientes entidades y relaciones:
1. **Usuario**, que puede ser **Administrador** o **Usuario Regular**.
2. **Anime**, que tiene atributos como título, género, episodios, y descripción.
3. **Comentario**, relacionado con el **Usuario** y el **Anime**.
4. Relaciones de herencia entre **Usuario** y sus tipos (Administrador y Usuario Regular).
5. Relaciones de asociación entre **Usuario** y **Anime** para indicar los animes favoritos.

### Puntos Clave
- Asegúrate de que los atributos y métodos clave estén incluidos en cada clase.
- Usa las relaciones adecuadas (herencia, asociación) entre las clases.



## Sección 2: Diagrama de Objetos

### Requerimientos
Dibuja un **Diagrama de Objetos UML** que represente una instancia específica del sistema en funcionamiento. Usa los siguientes objetos como base:
1. Un **Usuario Regular** llamado "Carlos" que ha agregado "Naruto" y "One Piece" a su lista de favoritos.
2. Un **Administrador** llamado "Ana" que está gestionando el anime "Attack on Titan".
3. Un **Comentario** hecho por "Carlos" sobre "Naruto" diciendo "¡Me encanta este anime!".

### Puntos Clave
- Representa los objetos con atributos específicos y relaciones claras.
- Muestra cómo interactúan entre sí los objetos del sistema.


## Sección 3: Diagrama de Actividades

### Requerimientos
Dibuja un **Diagrama de Actividades UML** que modele el flujo de acciones en el sistema de gestión de animes puede involucrar varios procesos y decisiones importantes. Aquí se evalúa cómo los estudiantes pueden representar el flujo de las acciones necesarias para que un **Usuario** explore, interactúe y administre su cuenta, y cómo un **Administrador** gestiona el contenido de la plataforma.

**Acciones para el Usuario:**
1. **Inicio de Sesión**: El usuario ingresa sus credenciales y el sistema verifica su validez. Dependiendo de si es válido o no, el flujo puede continuar o retornar a la solicitud de credenciales.
2. **Explorar Animes**: El usuario puede buscar o filtrar animes por categorías, popularidad o recientes. 
3. **Añadir a Favoritos**: Una vez encontrado un anime, el usuario puede agregarlo a su lista de favoritos.
4. **Comentar en un Anime**: Si el usuario ya ha iniciado sesión, puede escribir un comentario en un anime específico.
5. **Valorar un Anime**: El usuario puede asignar una calificación a un anime, lo cual impacta el sistema de recomendaciones.
6. **Actualizar Perfil**: El usuario puede actualizar su información personal y preferencias.
7. **Cerrar Sesión**: El usuario finaliza su sesión.
8. **Reporte de Anime Inapropiado**: En cualquier momento, el usuario puede reportar contenido inapropiado, activando una acción que será procesada por el administrador.

**Acciones para el Administrador:**
1. **Revisión de Animes Reportados**: Recibe una notificación cuando un anime es reportado por un usuario. Puede optar por eliminar el contenido, enviarlo a revisión, o cerrar el reporte.
2. **Añadir Nuevos Animes**: El administrador sube contenido nuevo, asigna categorías y actualiza la base de datos.
3. **Gestionar Usuarios**: Puede bloquear, suspender o modificar el estatus de los usuarios.
4. **Auditoría de Comentarios**: Revisa comentarios que han sido reportados o marcados como inapropiados. Puede eliminar, editar o aprobar el comentario.
5. **Revisión de Estadísticas**: El administrador revisa las métricas del sistema, como animes más populares, comentarios recientes o usuarios activos.
6. **Moderación de Anime**: Puede cambiar la visibilidad de un anime para restringir su visualización a usuarios de ciertas categorías o edades.

### Puntos Clave
- Muestra claramente las decisiones (condiciones) en el flujo.
- Asegúrate de que las actividades estén correctamente etiquetadas y conectadas.

## Sección 4: Diagrama de Casos de Uso

### Requerimientos
Dibuja un **Diagrama de Casos de Uso UML** que modele cómo los actores principales interactúan con el sistema y qué funcionalidades específicas están disponibles para cada uno. Los estudiantes deberán identificar los casos de uso principales, así como las extensiones y dependencias que surgen en ciertas acciones.

**Casos de Uso para el Usuario:**
1. **Inicio de Sesión**: El usuario accede al sistema ingresando sus credenciales.
2. **Explorar Animes**: Permite al usuario buscar y filtrar contenido dentro de la plataforma.
3. **Añadir a Favoritos**: Tras encontrar un anime de interés, el usuario puede agregarlo a su lista de favoritos.
4. **Comentar en un Anime**: Permite al usuario dejar opiniones sobre animes específicos.
5. **Valorar un Anime**: El usuario puede asignar una calificación a un anime.
6. **Reportar Anime Inapropiado**: Los usuarios pueden alertar al administrador sobre contenido inadecuado.
7. **Actualizar Perfil**: Permite modificar la información de la cuenta del usuario.
8. **Cerrar Sesión**: Finaliza la sesión actual del usuario.

**Casos de Uso para el Administrador:**
1. **Gestionar Usuarios**: El administrador puede cambiar el estatus de los usuarios (suspender, bloquear, modificar permisos).
2. **Añadir Nuevos Animes**: El administrador tiene la capacidad de cargar y gestionar el catálogo de animes.
3. **Eliminar o Modificar Animes**: El administrador puede eliminar contenido inapropiado o modificar información de un anime.
4. **Auditar Comentarios**: Revisa comentarios reportados o inapropiados y decide si deben ser eliminados o aprobados.
5. **Revisión de Estadísticas**: El administrador revisa las métricas de la plataforma para asegurar el buen funcionamiento.
6. **Moderación de Reportes**: Gestiona los reportes que llegan desde los usuarios y toma las acciones correspondientes.
7. 
### Puntos Clave
- Representa claramente los actores y los casos de uso principales.
- Asegúrate de mostrar las relaciones de extensión o inclusión cuando sea necesario.

## Sección 5: Código Java

A continuación, se te presenta un código que gestiona la funcionalidad de usuarios y animes en el sistema web. Lee el código detenidamente y contesta las preguntas que siguen.

### Código Java:

```java
import java.util.ArrayList;
import java.util.List;

// Clase Usuario
class Usuario {
    private String nombre;
    private String email;
    private List<Anime> favoritos;
    private List<Comentario> comentarios;

    public Usuario(String nombre, String email) {
        this.nombre = nombre;
        this.email = email;
        this.favoritos = new ArrayList<>();
        this.comentarios = new ArrayList<>();
    }

    // Método para agregar un anime a favoritos
    public void agregarAnimeFavorito(Anime anime) {
        favoritos.add(anime);
        System.out.println(this.nombre + " ha agregado " + anime.getTitulo() + " a favoritos.");
    }

    // Método para eliminar un anime de favoritos
    public void eliminarAnimeFavorito(Anime anime) {
        favoritos.remove(anime);
        System.out.println(this.nombre + " ha eliminado " + anime.getTitulo() + " de favoritos.");
    }

    // Método para dejar un comentario
    public void dejarComentario(Anime anime, String texto) {
        Comentario comentario = new Comentario(this, anime, texto);
        comentarios.add(comentario);
        anime.agregarComentario(comentario);
        System.out.println(this.nombre + " comentó en " + anime.getTitulo() + ": " + texto);
    }

    // Getters
    public String getNombre() {
        return nombre;
    }

    public String getEmail() {
        return email;
    }

    public List<Anime> getFavoritos() {
        return favoritos;
    }

    public List<Comentario> getComentarios() {
        return comentarios;
    }
}

// Clase Administrador 
class Administrador extends Usuario {

    public Administrador(String nombre, String email) {
        super(nombre, email);
    }

    // Método para agregar un nuevo anime
    public void agregarAnime(Anime anime, List<Anime> listaAnimes) {
        listaAnimes.add(anime);
        System.out.println("El administrador " + this.getNombre() + " ha agregado el anime: " + anime.getTitulo());
    }

    // Método para eliminar un anime
    public void eliminarAnime(Anime anime, List<Anime> listaAnimes) {
        listaAnimes.remove(anime);
        System.out.println("El administrador " + this.getNombre() + " ha eliminado el anime: " + anime.getTitulo());
    }

    // Método para gestionar comentarios (eliminar comentarios inapropiados)
    public void eliminarComentario(Comentario comentario, Anime anime) {
        anime.eliminarComentario(comentario);
        System.out.println("El administrador " + this.getNombre() + " ha eliminado un comentario en " + anime.getTitulo());
    }
}

// Clase Anime
class Anime {
    private String titulo;
    private String genero;
    private int episodios;
    private String descripcion;
    private List<Comentario> comentarios;

    public Anime(String titulo, String genero, int episodios, String descripcion) {
        this.titulo = titulo;
        this.genero = genero;
        this.episodios = episodios;
        this.descripcion = descripcion;
        this.comentarios = new ArrayList<>();
    }

    // Método para agregar un comentario
    public void agregarComentario(Comentario comentario) {
        comentarios.add(comentario);
    }

    // Método para eliminar un comentario
    public void eliminarComentario(Comentario comentario) {
        comentarios.remove(comentario);
    }

    // Getters
    public String getTitulo() {
        return titulo;
    }

    public String getGenero() {
        return genero;
    }

    public int getEpisodios() {
        return episodios;
    }

    public String getDescripcion() {
        return descripcion;
    }

    public List<Comentario> getComentarios() {
        return comentarios;
    }
}

// Clase Comentario
class Comentario {
    private Usuario autor;
    private Anime anime;
    private String texto;

    public Comentario(Usuario autor, Anime anime, String texto) {
        this.autor = autor;
        this.anime = anime;
        this.texto = texto;
    }

    // Getters
    public Usuario getAutor() {
        return autor;
    }

    public Anime getAnime() {
        return anime;
    }

    public String getTexto() {
        return texto;
    }
}

// Clase principal para ejecutar el sistema
public class Main {
    public static void main(String[] args) {
        // Lista de animes en el sistema
        List<Anime> listaAnimes = new ArrayList<>();

        // Creación de usuarios y administrador
        Usuario usuario1 = new Usuario("Carlos", "carlos@example.com");
        Administrador admin1 = new Administrador("Ana", "ana@example.com");

        // Creación de animes
        Anime anime1 = new Anime("Naruto", "Shonen", 220, "Un joven ninja busca ser el mejor.");
        Anime anime2 = new Anime("One Piece", "Aventura", 1000, "Piratas buscando el tesoro One Piece.");

        // Acciones del administrador
        admin1.agregarAnime(anime1, listaAnimes);
        admin1.agregarAnime(anime2, listaAnimes);

        // Acciones del usuario
        usuario1.agregarAnimeFavorito(anime1);
        usuario1.dejarComentario(anime1, "¡Me encanta este anime!");

        // Acciones del administrador: eliminar comentario
        admin1.eliminarComentario(anime1.getComentarios().get(0), anime1);

        // Usuario elimina anime de favoritos
        usuario1.eliminarAnimeFavorito(anime1);
    }
}
```

## Entregables

Los entregables son imágenes de cada diagrama en formato PNG.

### Fin del Examen.