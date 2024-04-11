Documentación de API para Gestión de Productos
Esta API proporciona funcionalidades para la gestión de usuarios, carritos de compra y productos en un sistema de comercio electrónico. A continuación, se detallan las rutas disponibles y su funcionamiento:

Rutas de Usuarios
Obtener todos los usuarios
Ruta: GET /api/users
Descripción: Devuelve todos los usuarios registrados en el sistema.
Requisitos de acceso: Solo los usuarios con roles de "admin" o "premium" pueden acceder.
Respuestas:
200 OK: Lista de usuarios recuperada exitosamente.
500 Error interno del servidor.
Cambiar el rol de un usuario a premium
Ruta: PUT /api/users/premium/:uid
Descripción: Cambia el rol de un usuario a "premium".
Parámetros de ruta:
uid: ID del usuario a modificar.
Respuestas:
200 OK: Rol de usuario actualizado exitosamente a "premium".
404 Usuario no encontrado.
500 Error interno del servidor.
Rutas de Carritos
Crear un nuevo carrito
Ruta: POST /api/cart
Descripción: Crea un nuevo carrito en el sistema.
Requisitos de acceso: No se requiere autenticación.
Respuestas:
200 OK: Carrito creado exitosamente.
500 Error interno del servidor.
Obtener el precio total de un carrito
Ruta: GET /api/cart/:id/total
Descripción: Obtiene el precio total de un carrito específico.
Parámetros de ruta:
id: ID del carrito.
Respuestas:
200 OK: Precio total del carrito obtenido exitosamente.
500 Error interno del servidor.
Obtener información del carrito
Ruta: GET /api/cart/info
Descripción: Obtiene información detallada del carrito, incluyendo precios y productos.
Requisitos de acceso: No se requiere autenticación.
Respuestas:
200 OK: Información del carrito obtenida exitosamente.
404 El carrito está vacío o no se encontró.
500 Error interno del servidor.
Agregar producto al carrito
Ruta: POST /api/cart/agregar
Descripción: Agrega un producto al carrito del usuario actual.
Requisitos de acceso: Solo los usuarios con roles de "premium" o "admin" pueden agregar productos al carrito.
Respuestas:
200 OK: Producto agregado al carrito con éxito.
401 El usuario no tiene permiso para agregar productos al carrito.
500 Error interno del servidor.
Otras Rutas
Obtener categorías de productos
Ruta: GET /api/products
Descripción: Obtiene todas las categorías de productos disponibles en la base de datos.
Requisitos de acceso: No se requiere autenticación.
Respuestas:
200 OK: Categorías de productos obtenidas exitosamente.
500 Error interno del servidor.
Esta documentación describe las rutas disponibles en la API junto con sus descripciones, requisitos de acceso y respuestas esperadas.
