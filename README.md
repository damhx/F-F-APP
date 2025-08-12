# FandF APP
# Diseño reflexivo de endpoints (App de transporte tipo Uber)

# Preguntas guía:

1. ¿Qué entiendes por “endpoint” en el contexto de una API?

- Un "endpoint" es una URL a la que un cliente puede hacer una solicitud para acceder a una funcionalidad o recurso proporcionado.

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

- Información financiera:
Números de tarjetas de crédito/débito.
Códigos CVV.
Cuentas bancarias.
Historial de transacciones.

4. ¿Por qué es importante definir bien los métodos HTTP (GET, POST, PUT/PATCH, DELETE) en cada endpoint?

- Cada método HTTP tiene un propósito en específico, usarlos correctamente permite que una aplicación sea más fácil de entender para otros desarrolladores.

5. ¿Qué tipo de información requiere autenticación en este sistema?

- Datos personales, tanto de los conductores y pasajeros, solicitud de viajes, calificaciones e historiales de pago.

6. ¿Cómo manejarías la seguridad de la ubicación de conductores y pasajeros?

- Por transmisión cifrada (HTTPS), siempre transmite datos de ubicación por canales seguros.

7. ¿Qué pasaría si un viaje es solicitado y no hay conductores disponibles? ¿Cómo debería responder la API?

- Cuando un usuario solicita un viaje, pero no hay conductores disponibles en la zona, la apicación no debe fallar silenciosamente ni dar una respuesta genérica. En su lugar, debe responder claramente con un estado que el cliente pueda entender y manejar, indicando que no se ha encontrado un conductor cercano.

8. ¿Cómo identificarías los recursos principales de esta aplicación?

- Son aquellas entidades claves que representan algunos objetos del dominio, como: usuarios, viajes, pagos, calificaciones y vehículos.

9. ¿Qué ventajas tendría versionar la API (por ejemplo, `/v1/...`) desde el inicio?

- Para amntener una escalabilidad dentro del API, y no haya alguna interferencia entre actualizaciones y/o cambios.

10. ¿Por qué es importante documentar las respuestas de error y no solo las exitosas?

- Para poder tener un registro general del API, y el saber que está fallando nos permite saber con exactitud a qué debemos darle una solución y como hacerlo.



# Roles & permisos:
# Pasajero:
- Solicitar viaje.
- Historial de viajes.
- Aceptar, rechazar o cancelar viajes.
- Proponer valor del viaje.
- Calificar el servicio brindado por el conductor.
- Comentar sobre el servicio prestado.
- Seleccionar la opción de pago.

# Conductor:
- Hisorial de viajes.
- Aceptar, rechazar o cancelar viajes.
- Proponer valor del viaje.
- Dejar comentarios sobre el pasajero.
- Calificar el pasajero.
- Total ganancias.

# Administrador:
- Vista general de la aplicación.
- Historial de conductores.
- Estadisticas.
- Suspender cuentas.



# Recursos principales:

- auth: inicio de sesión y registro.
- users: gestión de cuentas.
- admin: control de sistema por parte del administrador.
- rides: solicitudes y estados de viajes.
- ratings: evaluaciones mutuas entre pasajeros y conductores.
- vehicles: datos de vehículos registrados.
- payments: gestión y confirmación de pagos.



# Tabla de endpoints:

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
