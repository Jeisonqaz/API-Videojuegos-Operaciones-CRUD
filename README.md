#API Básica de Videojuegos

Descripción:

Esta API REST fue desarrollada con Java y Spring Boot con el objetivo de implementar y conocer las funcionalidades principales de una API.

La aplicación funciona como un catálogo básico de videojuegos, permitiendo crear, consultar, actualizar y eliminar registros. Cada videojuego contiene información como su nombre, género y plataforma.

Durante el desarrollo se utilizaron diferentes componentes de Spring Boot, como `@GetMapping`, `@PostMapping`, `@PutMapping`, `@DeleteMapping`, `@PathVariable` y `@RequestParam`.

Asimismo, el proyecto fue desarrollado como una aplicación académica para demostrar el funcionamiento de una API REST y la implementación de operaciones CRUD utilizando persistencia de datos.

La información de los videojuegos se almacena utilizando JPA, Hibernate y una base de datos H2.

Funcionalidades:

- Permite buscar los videojuegos por medio de su ID.
- Permite buscar los videojuegos por medio de su genero.
- Permite realizar consultas del listado de los videojuegos existentes.
- Permite agregar nuevos videojuegos por medio de un POST.
- Permite actualizar información de algun vieojuego por medio de un PUT.
- Permite eliminar un videojuego por medio de su ID.
- Por medio de la aplicación Bruno se validan las conexiones y errores de los endpoints como los códigos 200, 201, 204 y 404



Instrucciones de ejecución:

Utilizamos los siguientes parámetros:

GET /videojuegos --> Para obtener la información del listado de los videojuegos existentes.
GET /videojuegos/{id} --> Para obtener la información de ese videojuego
GET /videojuegos/buscar?genero={genero} --> Para buscar un videojuego por su genero

POST /videojuegos --> Para agregar un nuevo videojuego en el listado (El id en el listado se asigna de forma automática) utilizando la siguiente estructura:

{
  "nombre": "God of War Ragnarök",
  "genero": "Acción",
  "plataforma": "PlayStation 5"
}

PUT /videjojuegos/{id} --> Para actualizar la información de algun videojuego 

{
  "nombre": "God of War 1",
  "genero": "Aventura",
  "plataforma": "PC"
}

DELTE /videojuegos/{id} --> Para eliminar algun videojuego, lo cual al buscar el eliminado nos debe de arrojar un error 404, lo
cual refleja que se elimino de forma correcta.


Y para ejecutar el proyecto en general, se debe iniciar la aplicación de SpringBoot con el comando: 

.\mvnw.cmd spring-boot:run

Y la api estaría disponible en el siguiente enlace:  http://localhost:8080