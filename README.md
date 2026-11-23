# Feed regional de pronunciación para MZ TTS

Este repositorio es solo un **esqueleto público de distribución**. Por ahora el feed está vacío: no publica paquetes `.mzrp`, reglas de pronunciación, diccionarios, datos de voz ni código de la aplicación.

## Archivos y endpoint

- `feed.json`: índice del feed, actualmente con `packages: []`.
- `feed-v1.schema.json`: contrato JSON para futuras entradas.
- `index.html`: página sencilla de estado.

Cuando GitHub Pages quede publicado, el índice estará en:

`https://mariozepedazepeda-ship-it.github.io/MZ-TTS-regional-feed/feed.json`

## Qué no hace todavía

GitHub Pages solo sirve los archivos estáticos de este repositorio. **MZ TTS aún no consulta este feed ni descarga o actualiza paquetes en segundo plano**; esta publicación no cambia la aplicación y no evita todavía una importación manual. La integración local `.mzrp` es independiente. La pantalla accesible para elegir una región y el descargador en segundo plano siguen pendientes.

Las actualizaciones de los archivos de este repositorio tampoco se generan solas: alguien tendría que revisar y publicar cambios aprobados. La publicación automática de páginas de GitHub tras un cambio en la rama no equivale a crear, revisar o instalar automáticamente diccionarios.

## Requisitos antes de añadir un paquete

Cada futura entrada deberá apuntar a un paquete `.mzrp` válido y declarar su formato, perfil, versión, procedencia, licencia, atribución, cantidad de reglas y SHA-256. Los derechos y la atribución de cada fuente deben revisarse antes de publicarla. No se incluyen aquí muestras de diccionarios ni datos de terceros.

El SHA-256 permite comprobar que los bytes coinciden con el hash declarado; **no demuestra por sí solo quién produjo o aprobó ese hash**. Un descargador futuro no debe tratar este índice sin firma como una raíz de confianza: primero necesitará una comprobación de autenticidad confiable, además de validar el paquete localmente.

El repositorio es público. Todo archivo que se agregue será visible públicamente; no subir datos personales, voces, diccionarios o paquetes sin autorización y revisión de procedencia/licencia.
