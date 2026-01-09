Trhoncal Homes – Catálogo (ZIP listo)
======================================

Estructura incluida:
- index.html  → Catálogo con mapa (Leaflet), formulario y enlace a Panel.
- panel.html  → Panel simple con contraseña (front-end). Clave por defecto: trhoncal2025
- /assets     → Imágenes FICTICIAS con los mismos nombres que ya usas. Cámbialas por las reales.
- /data/desarrollos.json → Plantilla de datos por si migramos a lectura dinámica.

Cómo usar el Panel hoy:
- Es sólo de apoyo (sin backend). Guarda en localStorage del navegador.
- Puedes exportar el JSON para reemplazar /data/desarrollos.json más adelante.
- Para producción con escritura real, conectaremos Apps Script o un micro-API.

Seguridad del Panel:
- Protección básica por contraseña del lado del cliente (no expone datos sensibles).
- Cambia la clave en panel.html (const PASSWORD = "trhoncal2025").

Mapa:
- Leaflet con círculos tomando lat/lng/r de las tarjetas del index.
- En el futuro se puede leer /data/desarrollos.json para no duplicar info.


Actualización (versión dinámica con filtros):
- index.html ahora carga data/desarrollos.json y renderiza tarjetas + mapa.
- Filtros: búsqueda, zona, tipo, estatus, precio mínimo/máximo, crédito.
- Agrega más desarrollos desde el PANEL (exporta JSON) o editando data/desarrollos.json.
