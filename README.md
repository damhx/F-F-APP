# FandF APP
# Diseño reflexivo de endpoints (App de transporte tipo Uber)

# Preguntas guía:

1. ¿Qué entiendes por “endpoint” en el contexto de una API?

- Un "endpoint" es una URL a la que un cliente puede hacer una solicitud para acceder a una funcionalidad o recurso proporcionado por esa API.

2. ¿Cuál es la diferencia entre un endpoint público y uno privado?

- La diferencia entre un endpoint público y uno privado radica principalmente en el nivel de acceso y seguridad que se requiere para cada uno, por ejemplo:

endpoint público:
- Acceso sin autenticación.
- Puede ser utilizado por cualquiera, no necesita inicio de sesión o sus credenciales.
- Generalmente se usa para tipo de información abierta, que no requiere seguridad.

endpoint privado:
- Requiere autenticación y en algunas ocasiones autorización.
- Solo pueden acceder usuarios o sistemas que tengan credenciales válidas.
- Se usa para acciones con información sensible o mucha seguridad.

3. ¿Qué información de un usuario consideras confidencial y no debería exponerse?

- 

4. ¿Por qué es importante definir bien los métodos HTTP (GET, POST, PUT/PATCH, DELETE) en cada endpoint?

- 

5. ¿Qué tipo de información requiere autenticación en este sistema?

- 

6. ¿Cómo manejarías la seguridad de la ubicación de conductores y pasajeros?

- 

7. ¿Qué pasaría si un viaje es solicitado y no hay conductores disponibles? ¿Cómo debería responder la API?
8. ¿Cómo identificarías los recursos principales de esta aplicación?
9. ¿Qué ventajas tendría versionar la API (por ejemplo, `/v1/...`) desde el inicio?
10. ¿Por qué es importante documentar las respuestas de error y no solo las exitosas?
