# PlanoVivo: Sistema de Newsletter Automatizado con IA y Aprobación Humana

Entrega Final · Ecosistema de Automatización IA Autónomo para Negocios
Autora: Gisel · Stack: n8n (Cloud) · Notion · Claude (Anthropic) · Gmail

## Qué hace el sistema

Toma ideas de contenido desde Notion, usa Claude para clasificar su prioridad (Haiku 4.5) y redactar un newsletter según la guía de marca y el segmento objetivo (Sonnet 4.6), lo somete a aprobación humana por email con hasta 3 revisiones y, una vez aprobado, lo envía de forma personalizada solo a los suscriptores activos del segmento. Estados, versiones, destinatarios, Thread ID, tokens, costo y errores quedan registrados en Notion.

## Enlaces

- Dashboard de control y base de datos en Notion (vista pública, modo lectura): https://app.notion.com/p/PlanoVivo-3e5db0e9cfab808e8946cb293b99517c?source=copy_link


## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `PlanoVivo_Documentacion_Entrega_Final.pdf` | Diagrama de arquitectura, manual operativo de datos, matriz de costos, seguridad y resiliencia, dashboard de control |
| `planovivo-newsletter-automation.json` | Flujo exportado de n8n (sin credenciales) |
| `evidencias/` | Capturas de pantalla del proceso de construcción y de las pruebas |

## Criterios de la rúbrica y dónde encontrarlos

| Criterio | Ubicación |
|---|---|
| Mapa de arquitectura | PDF, sección 1 |
| Estructuras de datos documentadas | PDF, sección 2 (tablas, relaciones y esquemas JSON) |
| Optimización de costos | PDF, sección 3 (matriz de decisión de modelos y costo real por ejecución) |
| Seguridad y resiliencia | PDF, sección 4 (minimización de datos, rutas de error, Human-in-the-loop) |
| Dashboard de control | Enlace público arriba + PDF, sección 5 |

## Pruebas realizadas

Camino feliz completo, envío a varios suscriptores, segmentación respetando bajas, datos faltantes, máximo de revisiones, simulación de caída de la API en IA 1 y en IA 2, y ejecución automática en producción. Más de 20 ejecuciones en total.

## Seguridad

Las credenciales (Anthropic, Notion, Gmail) se guardan en el gestor de credenciales de n8n y no están incluidas en el JSON exportado. A la IA nunca se le envían datos personales de los suscriptores.
