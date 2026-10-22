# Casos de prueba y resultados

**API de práctica:** [JSONPlaceholder](https://jsonplaceholder.typicode.com/)  
**Capturas de ejecución previa:** 22 de octubre de 2026  
**Herramienta:** Postman

Los resultados de esta tabla se basan en capturas de una ejecución previa de esta colección de práctica. Como la colección se ha organizado de nuevo para este repositorio, importa el archivo JSON de la carpeta `postman/` y ejecuta los ocho casos nuevamente para confirmar esta versión. API-003 permanece como observación manual hasta completar la revisión colaborativa del resultado esperado.

| ID | Solicitud | Objetivo | Resultado esperado | Resultado observado | Estado |
|---|---|---|---|---|---|
| API-001 | `GET /posts` | Consultar todas las publicaciones. | Código 200 y una lista JSON con elementos. | `200 OK`; se recibió una lista JSON. Pasaron 2 de 2 validaciones automáticas. | Aprobado |
| API-002 | `GET /posts/1` | Consultar una publicación existente. | Código 200 y un objeto con el identificador 1 y los campos esperados. | `200 OK`; la respuesta incluyó el ID 1 y los campos esperados. Pasaron 2 de 2 validaciones. | Aprobado |
| API-003 | `GET /posts/9999` | Consultar una publicación inexistente. | Confirmar el comportamiento esperado para un identificador inexistente. | `404 Not Found`; cuerpo observado: `{}`. Esta solicitud no tenía aserciones automáticas configuradas. | Observación manual; revisión pendiente |
| API-004 | `GET /posts?userId=1` | Filtrar publicaciones por usuario. | Código 200 y todos los elementos asociados a `userId = 1`. | `200 OK`; la respuesta contenía publicaciones del usuario 1. Pasaron 2 de 2 validaciones. | Aprobado |
| API-005 | `POST /posts` | Enviar una solicitud válida para crear una publicación. | Código 201 y respuesta que refleje los campos enviados. | `201 Created`; la respuesta reflejó los campos en español y devolvió el ID 101. Pasaron 2 de 2 validaciones. | Aprobado |
| API-006 | `PUT /posts/1` | Enviar una actualización completa. | Código 200 y respuesta que refleje los campos enviados. | `200 OK`; la respuesta reflejó el ID, el título y el cuerpo enviados en español. Pasaron 2 de 2 validaciones. | Aprobado |
| API-007 | `PATCH /posts/1` | Actualizar solo el título de una publicación. | Código 200 y respuesta con el título actualizado. | `200 OK`; se actualizó el título. El campo `body` conservó el contenido anterior porque no se incluyó en la solicitud parcial. Pasaron 2 de 2 validaciones. | Aprobado |
| API-008 | `DELETE /posts/1` | Enviar una solicitud de eliminación. | Verificar el código y el cuerpo de respuesta documentados u observados. | `200 OK`; cuerpo observado: `{}`. Pasó 1 de 1 validación automática. | Aprobado |

## Resumen de la ejecución previa
- En las capturas registradas se ejecutaron los ocho escenarios de la versión de la colección usada previamente.
- Siete solicitudes tenían validaciones automáticas y las trece comprobaciones mostradas pasaron.
- API-003 respondió con 404 y un objeto JSON vacío; no se reporta como defecto sin confirmar antes el contrato esperado.
- Los resultados de POST, PUT, PATCH y DELETE son respuestas de una API de práctica. No prueban cambios persistentes en sus datos.
- No se ha confirmado ningún defecto en la ejecución previa.

## Verificación pendiente de esta versión
- [ ] Importar `postman/coleccion-pruebas-api.json` en Postman.
- [ ] Ejecutar los ocho casos de la colección recién organizada.
- [ ] Confirmar que las validaciones automáticas pasan y actualizar este registro si los resultados cambian.

## Revisión pendiente: API-003
La respuesta 404 es coherente con una consulta de un recurso inexistente. Aun así, la revisión se enfocará en acordar el criterio de aceptación y decidir si conviene añadir una aserción automática para el código HTTP. El cuerpo `{}` se conserva como dato observado, pero no se impone como requisito hasta que se justifique con la documentación del servicio.

## Plantilla para futuras ejecuciones
Para repetir o añadir pruebas, registrar fecha, método y URL, código HTTP, campos relevantes del JSON, resultado de las validaciones, evidencia y cualquier observación. Si un caso falla, repetirlo y comparar el resultado con un requisito o comportamiento documentado antes de abrir un informe de defecto.
