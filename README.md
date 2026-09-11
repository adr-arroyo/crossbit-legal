# CrossBit Legal

Documentos legales finales de CrossBit para su publicación en Google Play, App Store y
la web pública del proyecto.

**Versión publicada:** 2 de septiembre de 2026

## Documentos

- [Política de Privacidad](./privacy.md)
- [Términos y Condiciones](./terms.md)
- [Aviso médico](./medical-disclaimer.md)
- [Eliminación de datos y cuenta](./delete-account.md)
- [Soporte](./support.md)

También hay versiones en [inglés](./en/).

## app-ads.txt — publicación y verificación

El archivo [app-ads.txt](./app-ads.txt) contiene únicamente la línea pública
proporcionada por AdMob. Se conserva como texto plano UTF-8 sin BOM, con un salto
de línea final y sin IDs de aplicación, unidades de anuncio ni credenciales.

GitHub Pages está configurado para servir la raíz `/` de la rama `main`, sin
dominio personalizado. La URL del archivo de este repositorio es
[app-ads.txt del sitio legal](https://adr-arroyo.github.io/crossbit-legal/app-ads.txt).

Con el hostname actual, la URL de rastreo que debe resolver AdMob es
[app-ads.txt en la raíz del dominio](https://adr-arroyo.github.io/app-ads.txt).
Según la [guía de rastreo de AdMob](https://support.google.com/admob/answer/9679128?hl=en),
esa ruta debe servir el archivo o redirigir a él; publicarlo solo bajo
`/crossbit-legal/` no satisface este requisito.

La copia de la raíz se publica desde el repositorio
[`adr-arroyo.github.io`](https://github.com/adr-arroyo/adr-arroyo.github.io), cuya
configuración de Pages sirve `/` de la rama `master`. Ambas copias de
`app-ads.txt` deben mantenerse idénticas. El sitio web que debe figurar en Play
es [CrossBit Legal](https://adr-arroyo.github.io/crossbit-legal/).

Tras cada publicación, comprobar sin autenticación que ambas URLs del archivo
devuelven HTTP 200 con texto plano y el mismo SHA-256 que el archivo local, y
que privacidad y eliminación siguen accesibles. No imprimir el cuerpo del
archivo ni sus identificadores en logs. La vinculación y verificación en AdMob
se realizan en U5.

## Datos del proyecto

- **Aplicación:** CrossBit
- **Autenticación cloud:** Firebase Authentication con email y contraseña
- **IA cloud:** Gemini 3.7 Flash vía el proxy autenticado de CrossBit y Vertex AI
- **Suscripciones:** CrossBit Pro mediante RevenueCat y las tiendas correspondientes
- **Publicidad:** banners contextuales para cuentas Gratis cuando el build de release la activa; consentimiento mediante Google UMP
- **Datos de salud y actividad:** almacenamiento local en el dispositivo; no hay sincronización general con un servidor

## Estado de los documentos

Las páginas públicas mantienen las mismas condiciones en español e inglés y reflejan el
flujo actual de cuenta, coach cloud, reportes voluntarios de contenido IA, suscripciones,
publicidad contextual y eliminación de datos.
