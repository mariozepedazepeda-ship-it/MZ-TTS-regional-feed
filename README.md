# Feed regional de pronunciación para MZ TTS

El feed publica el primer conjunto **Chile (es-CL) — Extenso**, versión **1.0.0**, con **24.918 reglas ortográficas de palabras** en tres fragmentos: 9.976, 9.961 y 4.981 reglas. Se excluyeron 82 propuestas pendientes de frases y topónimos. El conjunto no incluye fonemas ni datos de voz.

## Índice y archivos

El índice estático es [`feed.json`](https://mariozepedazepeda-ship-it.github.io/MZ-TTS-regional-feed/feed.json) y usa el formato v2, que describe cada release como un conjunto de fragmentos. El contrato vigente está en [`feed-v2.schema.json`](./feed-v2.schema.json). Se conserva [`feed-v1.schema.json`](./feed-v1.schema.json) para documentar el formato anterior. Los tres archivos `.mzrp` publicados están en [`packages/`](./packages/).

## Activación y actualizaciones

Publicar el feed **no cambia la APK ni activa el overlay por sí solo**. En MZ TTS 1.6.41, el usuario debe elegir Extenso, seleccionar el overlay regional de Chile y aplicar el conjunto; la aplicación valida y activa los tres fragmentos de forma atómica. **General sigue siendo el modo predeterminado** y no descarga ni aplica overlays.

La actualización automática es opcional. Si se habilita con Extenso y un overlay regional activo, la aplicación revisa el feed aproximadamente cada 24 horas, con conexión a internet y batería suficiente. También se puede consultar y aplicar un conjunto desde los ajustes regionales.

## Procedencia y licencia

Las grafías se adaptaron de VoiceGarden español v0.6.1, que atribuye los datos de Wiktionary bajo **CC BY-SA 4.0** y a sus colaboradores. La lista spa-LatAm v0.6.1 bajo MIT se usó solo para priorizar; no se incorporó al paquete. No se usaron fonemas. [Fuente: VoiceGarden español v0.6.1](https://github.com/AACTools/voicegarden-lexicons/releases/tag/v0.6.1).

Cada fragmento declara procedencia, licencia, atribución, fuente, número de reglas y SHA-256. El hash comprueba que los bytes descargados coinciden con los anunciados, pero por sí solo no prueba quién creó o aprobó ese hash. El feed no está firmado: la aplicación debe validar el origen HTTPS, los metadatos, cada paquete y el conjunto completo antes de activarlo.

El repositorio es público. Los paquetes y documentos añadidos aquí son visibles públicamente; no se deben subir datos personales, voces ni contenido sin autorización y revisión de procedencia y licencia.
