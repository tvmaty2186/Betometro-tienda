# Betómetro · Tienda — guía para Claude

Este repo es la Tienda de herramientas del Betómetro. Las reglas de trabajo con Matías son las mismas que en
`tvmaty2186/Betometro-Raspberry` (leé su CLAUDE.md): español rioplatense, corto y claro; muestra antes de programar
algo visual; no compilar ni publicar sin su OK; commits con autor `Matías Russo <tvmaty2186@gmail.com>`.

- Una carpeta por herramienta. Cada una con su número de versión propio (empieza en 1.0.0).
- `tienda.json` es lo que lee la Pi: no romper su formato (`formato: 1`, ver README.md).
- Las herramientas usan solo módulos de Qt que ya están en la Pi (QtQuick, QtQuick.Window, QtMultimedia; ver
  `raspios/paquetes.txt` del repo de Betómetro). En la 1.0.29 un módulo que faltaba dejó todo en negro.
- Una herramienta siempre tiene un botón «Volver a Betómetro» y termina el programa al tocarlo.
- Decisión del 08/11/2026: un solo repo para todas las herramientas; si una crece mucho, se separa después.
