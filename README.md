# Foro Hub 👩‍💻

Foro Hub es una aplicación de foro diseñada para facilitar la comunicación y discusión entre usuarios. Esta aplicación permite a los usuarios crear tópicos, responder a los mismos y participar en discusiones.


## Características ⚙️

- Registro y autenticación de usuarios.
- Creación, edición y eliminación de tópicos.
- Respuesta a tópicos existentes.
- Listado de usuarios y tópicos.
- Autenticación mediante JWT.

## Tecnologías utilizadas ⚒️

- Java
- Spring Boot
- Spring Security
- JWT (JSON Web Tokens)
- JPA (Java Persistence API)
- H2 Database (para desarrollo y pruebas)
- Postman (para pruebas de API)

## Estructura del proyecto 🖥️

- **Entities**: Clases de entidad que representan las tablas de la base de datos.
- **Dto**: Clases de Data Transfer Object utilizadas para transferir datos entre el cliente y el servidor.
- **Repository**: Interfaces que extienden JpaRepository para realizar operaciones CRUD en las entidades.
- **Service**: Clases de servicio que contienen la lógica de negocio.
- **Controller**: Clases de controlador que manejan las solicitudes HTTP.
- **Security**: Clases relacionadas con la configuración de seguridad y la autenticación.

## Instalación 🚧

Clona este repositorio:
```
git clone https://github.com/DevMGcode/Chanllege-Foro_Hub.git
```

Navega al directorio del proyecto:
```
cd ForoHub
```
- Abre el proyecto en tu IDE favorito (por ejemplo, IntelliJ IDEA o Eclipse).
- Configuración
- Base de datos: MySQL 📈


La aplicación estará disponible en `http://localhost:8080`.

Endpoints principales:
- `/login`: Endpoint para autenticación de usuarios. Envía una solicitud POST con un JSON que contiene `username` y `password`.
- `/usuarios`: Endpoint para listar usuarios. Requiere autenticación mediante un token JWT.
- `/topicos`: Endpoint para manejar la creación, actualización y eliminación de tópicos.

### Ejemplos de solicitudes 📑

- Autenticación 🔐

Solicitud:
```
POST http://localhost:8080/login
```
Body:
```
{
    "username": "nombre_usuario",
    "password": "contraseña"
}
```
Respuesta:
```
{
    "token": "jwt_token_generado"
}
```
- Crear un tópico 📝

Solicitud:
```
GET http://localhost:8080/topico/topicos
```
Headers:
```
Authorization: Bearer jwt_token_generado
Content-Type: application/json
```
Body:
```
{
  "totalPages": 1,
  "totalElements": 3,
  "size": 3,
  "content": [
    {
      "id": 1,
      "title": "Tecnología e Innovación",
      "message": "Discusión sobre los avances tecnológicos y su impacto en la sociedad.",
      "status": "ACTIVO",
      "usuario_Id": 1,
      "curso": "Introducción a la Tecnología",
      "date": "2024-08-01T10:00:00.000Z"
    },
    {
      "id": 2,
      "title": "Salud y Bienestar",
      "message": "Exploración de temas relacionados con la salud física y mental.",
      "status": "ACTIVO",
      "usuario_Id": 2,
      "curso": "Cuidado Personal",
      "date": "2024-08-02T14:00:00.000Z"
    },
    {
      "id": 3,
      "title": "Ciencia y Medio Ambiente",
      "message": "Análisis de problemas ambientales y soluciones científicas.",
      "status": "ACTIVO",
      "usuario_Id": 3,
      "curso": "Ecología Aplicada",
      "date": "2024-08-03T16:30:00.000Z"
    }
  ],
  "number": 0,
  "sort": "desc",
  "first": true,
  "last": true,
  "numberOfElements": 3,
  "pageable": {
    "offset": 0,
    "sort": "desc",
    "paged": true,
    "unpaged": false,
    "pageNumber": 0,
    "pageSize": 3
  },
  "empty": false
}


```

## Licencia 🚀
Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.
# Chanllege-Foro_Hub
# Chanllege-Foro_Hub
