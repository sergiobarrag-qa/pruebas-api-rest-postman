# Proyecto de pruebas de API REST con Postman

## Descripción
Proyecto práctico de aseguramiento de calidad (QA) para diseñar, ejecutar y documentar pruebas de una API REST pública. El propósito es practicar el análisis de respuestas HTTP, la validación de datos JSON, el diseño de casos de prueba y la documentación de resultados reproducibles.

## Objetivos
- Diseñar casos de prueba para operaciones de consulta, filtrado, creación y actualización.
- Ejecutar solicitudes HTTP con Postman.
- Validar códigos de respuesta y campos relevantes del JSON.
- Registrar los resultados reales sin asumir que una respuesta diferente constituye automáticamente un defecto.
- Revisar un escenario negativo con otro estudiante de QA y documentar las conclusiones de la colaboración.

## Herramientas y recurso de práctica
- **Postman:** ejecución de solicitudes y validaciones automáticas.
- **GitHub:** control de versiones y documentación del proyecto.
- **JSONPlaceholder:** [API REST pública de práctica](https://jsonplaceholder.typicode.com/).

JSONPlaceholder utiliza datos ficticios y simula las operaciones de escritura. Por lo tanto, las respuestas satisfactorias de POST, PUT, PATCH y DELETE no demuestran que los datos se hayan guardado o modificado permanentemente en el servidor.

## Alcance de las pruebas
La colección cubre ocho escenarios:
1. Consultar todas las publicaciones.
2. Consultar una publicación por su identificador.
3. Consultar un identificador inexistente.
4. Filtrar publicaciones por usuario.
5. Enviar una solicitud de creación.
6. Enviar una solicitud de actualización completa.
7. Enviar una solicitud de actualización parcial.
8. Enviar una solicitud de eliminación.

## Estructura del repositorio
```text
pruebas-api-rest-postman/
├── README.md
├── casos-de-prueba.md
├── postman/
│   ├── instrucciones.md
│   └── coleccion-pruebas-api.json
├── informes-de-defectos/
│   └── plantilla-informe.md
└── colaboracion/
    └── registro-colaboracion.md
```

## Estado del proyecto
- [x] Alcance y objetivos documentados.
- [x] Ocho solicitudes preparadas en Postman.
- [x] Ejecución inicial de los ocho escenarios realizada.
- [x] Resultados observados documentados.
- [ ] Revisar en colaboración el caso API-003 y confirmar los criterios para validarlo.
- [ ] Registrar la contribución y las conclusiones de la revisión entre compañeros.

## Resumen de la ejecución documentada
En las capturas de Postman del 22 de octubre de 2026 se observan ocho solicitudes ejecutadas en la versión de la colección que se trabajó previamente. En siete casos había validaciones automáticas: pasaron las trece comprobaciones mostradas. El caso API-003 devolvió `404 Not Found` con un cuerpo JSON vacío (`{}`), pero no tenía aserciones automáticas; por eso se mantiene como observación pendiente de revisión, no como defecto confirmado.

**Verificación pendiente de esta versión del repositorio:** importa la colección JSON incluida aquí y vuelve a ejecutar los ocho casos. Aunque los escenarios se prepararon con base en los resultados observados, esta versión recién organizada de la colección todavía debe comprobarse de punta a punta antes de considerar cerrada la ejecución.

Los detalles se encuentran en [Casos de prueba y resultados](casos-de-prueba.md).

## Criterio de documentación
Los nombres de los casos, las explicaciones, las validaciones y los datos de ejemplo enviados por el proyecto están en español. Algunos nombres de métodos HTTP, rutas y campos JSON se conservan tal cual porque forman parte de la interfaz técnica de la API. Los textos ficticios originales devueltos por las consultas también pueden estar en inglés.

## Responsable
Sergio Barragán — repositorio de práctica para su portafolio de QA.
