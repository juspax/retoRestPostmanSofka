# Prueba Rest Tienda De Mascotas

_Para esta prueba el proyecto tiene una serie de solicitudes para interactuar con la API de una tienda de mascotas, donde se realizan las operaciones de agregar, consultar, actualizar y buscar mascotas. La colección ha sido diseñada en Postman y se incluye en este repositorio para facilitar la automatización y prueba de la API. _

## Funcionalidades Cubiertas 🚀

_1. Añadir una mascota a la tienda _

1. Método: POST
2. Descripción: Se agrega una nueva mascota a la tienda, proporcionando detalles como ID, nombre, categoría, etiquetas y estatus.
3. URL: https://petstore.swagger.io/

```
{
  "id": 12345,
  "name": "Fido",
  "category": {
    "id": 1,
    "name": "Dog"
  },
  "photoUrls": [
    "https://example.com/photo.jpg"
  ],
  "tags": [
    {
      "id": 1,
      "name": "friendly"
    }
  ],
  "status": "available"
}

```
4. Respuesta esperada: Código 200 con el objeto JSON de la mascota añadida.

----------------------------------------------------------------

_2. Consultar la mascota ingresada previamente (Búsqueda por ID)_

1. Método: GET
2. Descripción: Consulta los detalles de la mascota agregada anteriormente utilizando su ID.
3. URL: https://petstore.swagger.io/
4. Parámetro de Ruta: petId (ID de la mascota previamente ingresada)
5. Respuesta esperada: Código 200 con el objeto JSON de la mascota.
------------------------------------------------------------------------

_3. Actualizar el nombre y el estatus de la mascota_

1. Método: PUT
2. Descripción: Actualiza el nombre de la mascota y su estatus a "sold".
3. URL:  https://petstore.swagger.io/

```
{
  "id": 12345,
  "name": "Buddy",
  "category": {
    "id": 1,
    "name": "Dog"
  },
  "photoUrls": [
    "https://example.com/photo.jpg"
  ],
  "tags": [
    {
      "id": 1,
      "name": "friendly"
    }
  ],
  "status": "sold"
}

```
4. Respuesta esperada: Código 200 confirmando la actualización.

-------------------------------------------------------------------------

_4. Consultar la mascota modificada por estatus (Búsqueda por estatus)_

1. Método: GET
2. Descripción: Realiza una consulta de todas las mascotas que tengan un estatus específico (por ejemplo, "sold").
3. URL: https://petstore.swagger.io/
4. Respuesta esperada: Código 200 con una lista de mascotas que tienen el estatus "sold".

------------------------------------------------------------------------------

## Conclusiones 🚀

El ejercicio de pruebas funcionales sobre la API de PetStore ha permitido validar la integración y el correcto funcionamiento de las principales operaciones relacionadas con la gestión de mascotas en una tienda virtual. Utilizando una herramienta de pruebas de servicios REST, se realizaron las siguientes pruebas con éxito:

1. Añadir una mascota a la tienda: Se envió una solicitud POST con un cuerpo JSON detallando la nueva mascota. La prueba confirmó que el servicio acepta y procesa correctamente los datos, almacenando la información de la mascota en el sistema.

2. Consultar la mascota ingresada previamente (Búsqueda por ID): Se utilizó una solicitud GET para buscar la mascota agregada mediante su ID. La respuesta fue un objeto JSON con todos los datos de la mascota, validando la integridad de la operación de búsqueda.

3. Actualizar el nombre y estatus de la mascota a "sold": Mediante una solicitud PUT, se actualizó el nombre y el estatus de la mascota a "sold". El servicio respondió con éxito, reflejando los cambios realizados en el nombre y el estatus de la mascota.

4. Consultar la mascota modificada por estatus (Búsqueda por estatus): La prueba de búsqueda por estatus, utilizando una solicitud GET, devolvió todas las mascotas con el estatus "sold", incluida la previamente actualizada. Esto demostró la capacidad del servicio para filtrar las mascotas según su estado actual.

Entradas, Salidas y Variables

Entradas: Los cuerpos JSON enviados en las solicitudes POST y PUT que incluían detalles como ID, nombre, categoría y estatus de la mascota.
Salidas: Las respuestas en formato JSON recibidas desde el servidor, confirmando la adición, consulta y actualización de las mascotas.
Variables: Se utilizaron variables como petId (para la consulta por ID) y status (para la búsqueda por estatus), las cuales se capturaron y gestionaron correctamente durante las pruebas.

Conclusión Final:

Las pruebas realizadas muestran que la API de PetStore es capaz de gestionar correctamente las operaciones de añadir, consultar y actualizar mascotas. El servicio responde de forma eficiente a las solicitudes REST y mantiene la integridad de los datos. Estos resultados respaldan la funcionalidad de la API para ser utilizada en un entorno de producción donde se espera la correcta interacción entre usuarios y el sistema de gestión de mascotas.



