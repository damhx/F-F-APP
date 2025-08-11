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

- Datos personales. (En algunos casos):
Nombre completo.
Número de identificación.
Número de celular.
Dirección física.
Fecha de nacimiento.
Correo electrónico.

- Credenciales de acceso:
Contraseña.
API keys asociadas a usuarios.
Preguntas y/o respuestas de seguridad.

- Información financiera:
Números de tarjetas de crédito/débito.
Códigos CVV.
Cuentas bancarias.
Historial de transacciones.

4. ¿Por qué es importante definir bien los métodos HTTP (GET, POST, PUT/PATCH, DELETE) en cada endpoint?

- Cada método HTTP tiene un propósito en específico, usarlos correctamente permite un buna API sea más fácil de entender para otros desarrolladores.
- GET: Obtener datos.
- POST: Crear un recurso nuevo.
- PUT: Reemplazar completamente un recurso.
- PATCH: Actualizar parcialmente un recurso.
- DELETE: Eliminar un recurso.

5. ¿Qué tipo de información requiere autenticación en este sistema?

- Datos personales, tanto de los conductores y pasajeros.

6. ¿Cómo manejarías la seguridad de la ubicación de conductores y pasajeros?

- Por transmisión cifrada (HTTPS/TLS), siempre transmite datos de ubicación por canales seguros (HTTPS).

7. ¿Qué pasaría si un viaje es solicitado y no hay conductores disponibles? ¿Cómo debería responder la API?

- Cuando un usuario solicita un viaje, pero no hay conductores disponibles en la zona, la API no debe fallar silenciosamente ni dar una respuesta genérica. En su lugar, debe responder claramente con un estado que el cliente pueda entender y manejar.

8. ¿Cómo identificarías los recursos principales de esta aplicación?

- Para identificar los recursos principales de la aplicación, lo ideal es enfocarse en las entidades centrales del negocio y los objetos con los que interactúan los usuarios y el sistema. Estos recursos serán la base para diseñar los endpoints de una API RESTful, estructurar la base de datos y aplicar reglas de negocio.

9. ¿Qué ventajas tendría versionar la API (por ejemplo, `/v1/...`) desde el inicio?

-

10. ¿Por qué es importante documentar las respuestas de error y no solo las exitosas?

-
