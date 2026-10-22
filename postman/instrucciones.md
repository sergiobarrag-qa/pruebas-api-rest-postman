# Instrucciones para Postman

## Importar la colección
1. Abre Postman.
2. Selecciona **Importar**.
3. Selecciona el archivo `coleccion-pruebas-api.json` de esta carpeta.
4. Comprueba que aparezca la colección **Pruebas de API REST - JSONPlaceholder**.
5. Ejecuta cada solicitud individualmente y revisa el código HTTP, el cuerpo de respuesta y la pestaña de resultados de prueba.

## Configuración
La colección utiliza la variable `baseUrl` con este valor:

```text
https://jsonplaceholder.typicode.com
```

## Recomendaciones
- Empieza por las solicitudes GET para familiarizarte con la estructura de las respuestas.
- Revisa las validaciones automáticas después de cada ejecución.
- En POST, PUT y PATCH, verifica los datos de la pestaña **Body** antes de enviar la solicitud.
- Guarda evidencia cuando sea relevante y registra el resultado real en `../casos-de-prueba.md`.
- No marques un caso como fallido solo porque una respuesta no coincide con una suposición: confirma primero cuál es el resultado esperado.
- Recuerda que esta API simula las operaciones de escritura; sus respuestas no significan que los datos queden modificados permanentemente.
