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

