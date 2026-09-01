---
permalink: /privacy.html
---

# Política de Privacidad de CrossBit

**Última actualización:** 1 de septiembre de 2026

Esta Política de Privacidad explica cómo CrossBit ("la aplicación", "nosotros") trata
tus datos personales cuando usas la aplicación móvil CrossBit (`com.crossbit.app`) en
Android e iOS.

## 1. Responsable del tratamiento

- **Responsable:** Adrián Arroyo Pérez (persona física)
- **Domicilio:** Condesa Mencia, 123, 5C, Burgos, 09006, España
- **Contacto de privacidad:** crossbitapp@gmail.com

Para cualquier duda sobre esta política o sobre el tratamiento de tus datos, escribe a
crossbitapp@gmail.com.

## 2. Principio fundamental: tus datos de salud se quedan en tu dispositivo

CrossBit está diseñada con un enfoque local-first. Tus entrenamientos, comidas,
métricas corporales, historial de chat, planes, listas de la compra, récords,
plantillas, preferencias y configuración se almacenan localmente en el dispositivo,
principalmente en el almacenamiento `localStorage` de la aplicación. En dispositivos
nativos puede existir también una copia automática local. No hacemos una sincronización
general de estos datos con un servidor.

Los datos salen del dispositivo únicamente cuando:

1. usas el coach o una función de análisis IA en la nube y envías el mensaje, el
   contexto necesario o una imagen para obtener una respuesta;
2. creas una cuenta o usas CrossBit Pro, para tratar la identidad, el estado de la
   cuenta, la suscripción y el uso necesarios para prestar esas funciones;
3. envías voluntariamente un reporte de una respuesta IA, que incluye el contenido que
   decidas reportar; o
4. un servicio del sistema, del navegador o de un proveedor publicitario procesa los
   datos técnicos necesarios para reconocimiento de voz o anuncios, cuando activas
   esas funciones y el build las incluye.

## 3. Qué datos tratamos, con qué finalidad y con qué base legal

### 3.1. Datos almacenados solo en tu dispositivo

| Categoría | Ejemplos | Dónde se almacena |
|---|---|---|
| Entrenamientos | WODs, series, pesos, frecuencia cardiaca y récords | `localStorage` |
| Nutrición | Comidas, macros, objetivos, plan y lista de compra | `localStorage` |
| Métricas de salud | Peso, sueño, pasos, descanso y readiness | `localStorage` |
| Conversaciones con el coach | Historial de chat y briefing | `localStorage` |
| Planificación | Plantillas y calendarios de WOD, planes y preferencias | `localStorage` |
| Configuración | Objetivos, idioma, consentimientos y configuración de modelos locales | `localStorage` |

No recibimos estos datos por el mero hecho de que permanezcan en tu dispositivo.
Puedes exportarlos o importarlos desde *Ajustes → Mis datos* en formato JSON. El archivo
exportado y la copia automática local quedan bajo tu control; CrossBit no los sube a
nuestros servidores.

### 3.2. Datos de cuenta y autenticación

Puedes utilizar CrossBit en modo local sin crear una cuenta. El coach cloud y las
funciones de suscripción requieren una cuenta de **Firebase Authentication**. La
versión actual ofrece registro e inicio de sesión únicamente con email y contraseña;
el email debe verificarse antes de usar el coach cloud o gestionar una suscripción.

| Dato | Finalidad | Base legal (RGPD) |
|---|---|---|
| Dirección de email | Crear, autenticar y recuperar tu cuenta | Ejecución del contrato (art. 6.1.b) |
| Identificador único de usuario (`uid`) | Asociar tu sesión, suscripción, reportes y límites de uso | Ejecución del contrato (art. 6.1.b) |
| Estado de verificación y datos técnicos de sesión | Proteger la cuenta y controlar el acceso cloud | Ejecución del contrato (art. 6.1.b) e interés legítimo (art. 6.1.f) |

Las contraseñas las gestiona Firebase Authentication; CrossBit no recibe ni almacena
la contraseña en texto claro. Firebase puede conservar los datos de autenticación y la
información técnica necesaria para mantener la sesión conforme a su propia política.

### 3.3. Datos de cuenta, suscripción y uso en nuestros servicios cloud

Para prestar el coach cloud, aplicar las cuotas y gestionar CrossBit Pro tratamos en
Firestore la información mínima necesaria:

| Dato | Finalidad | Conservación técnica |
|---|---|---|
| `uid`, nivel (`free`/`pro`) y expiración del nivel Pro | Autenticación, acceso y estado de la cuenta | Hasta completar la eliminación de la cuenta, salvo obligaciones aplicables |
| Metadatos de conciliación de suscripción (tipo, identificador y marca temporal del evento) | Aplicar cambios de compra, renovación, transferencia, reembolso o expiración en orden | Hasta completar la eliminación o la caducidad técnica correspondiente |
| Contadores mensuales de unidades IA | Aplicar límites y prevenir abuso | Hasta 40 días |
| Recibos opacos de idempotencia | Evitar cobros lógicos duplicados cuando se reintenta una petición | Hasta 40 días |
| Recibos técnicos de webhooks de compra | Procesar una entrega de RevenueCat una sola vez | Hasta 90 días |
| Checkpoint técnico de eliminación | Reanudar, reintentar y verificar el borrado | Registro mínimo del flujo; la implementación actual no configura una caducidad automática específica; no contiene salud ni chat |

Los cuerpos y las respuestas de las peticiones del chat no se guardan en Firestore.

### 3.4. Pagos y suscripciones

Las compras de CrossBit Pro se realizan mediante Google Play o App Store. **RevenueCat**
gestiona técnicamente el customer y el estado de la suscripción para que el servicio
pueda reconocer el nivel Pro. No recibimos ni almacenamos los datos de tu tarjeta o
medio de pago. RevenueCat, Google Play y Apple pueden conservar sus propios registros
conforme a sus políticas y a las obligaciones fiscales o contables aplicables.

Consulta las políticas de [RevenueCat](https://www.revenuecat.com/privacy),
[Google Play](https://policies.google.com/privacy) y
[Apple](https://www.apple.com/legal/privacy/).

### 3.5. Datos enviados al coach IA en la nube

Cuando usas el coach cloud, tu mensaje y el contexto necesario —por ejemplo,
entrenamientos, comidas o métricas relevantes para tu pregunta— se envían a **Gemini
3.5 Flash mediante Vertex AI (Google Cloud)** para generar la respuesta. Las imágenes
y otros archivos solo se envían cuando activas la función correspondiente.

- Antes del primer envío solicitamos un consentimiento específico para IA cloud. Sin
  sesión verificada o sin ese consentimiento, la petición no se envía.
- Nuestro cloud-proxy reenvía la petición y la respuesta en memoria. No guarda el cuerpo
  de la petición ni la respuesta y sus registros contienen solo metadatos técnicos,
  como método, ruta, estado, duración y `uid`, para seguridad y diagnóstico.
- Google Cloud procesa el contenido conforme a las condiciones de Vertex AI. La
  configuración del servicio puede implicar conservación limitada para caché o
  supervisión contra abusos; consulta las condiciones de Google Cloud para esos
  tratamientos. CrossBit no usa el contenido del coach para crear un historial de
  actividad ni para entrenar sus propios modelos.

La versión actual no ofrece un modo para introducir una clave propia de Gemini (BYOK).
El coach cloud usa el proxy autenticado de CrossBit; el coach en el dispositivo usa el
modelo local descargado.

### 3.6. Reportes voluntarios de contenido generado por IA

Si pulsas **Reportar** sobre una respuesta del coach, envías voluntariamente el texto
de esa respuesta, el motivo que elijas, el identificador del mensaje y la fecha. El
reporte se asocia a tu `uid`, se usa para moderación y seguridad, y se elimina
automáticamente en un máximo de **30 días** o antes si eliminas tu cuenta.

### 3.7. Cámara, fotos, micrófono y reconocimiento de voz

| Permiso o función | Finalidad | Tratamiento |
|---|---|---|
| Cámara o fototeca | Fotografiar o adjuntar comidas y WODs | La foto se procesa para el análisis solicitado y el resultado se guarda localmente. Si usas el análisis cloud, la imagen se envía a Vertex AI; CrossBit no guarda la foto en sus servidores. |
| Micrófono y reconocimiento de voz | Crear registros o dictar mensajes | El sistema, el navegador o el dispositivo puede realizar la transcripción. CrossBit recibe el texto resultante; si lo envías al coach cloud, se trata como un mensaje cloud. |

Estos permisos solo se solicitan al activar la función correspondiente y puedes
revocarlos desde los ajustes del sistema operativo.

### 3.8. Health Connect (Android)

En Android puedes conectar CrossBit con **Health Connect** y autorizar la lectura de
pasos, sesiones de sueño, frecuencia cardiaca, frecuencia cardiaca en reposo e
hidratación. CrossBit usa esos datos para mostrar métricas de actividad, recuperación y
tendencias en la aplicación. No escribe datos en Health Connect ni los comparte con
otros desarrolladores. Permanecen en el dispositivo salvo que actives una función del
coach cloud que necesite ese contexto; en ese caso se aplica la sección 3.5.

### 3.9. Modelos IA en el dispositivo

Opcionalmente puedes descargar modelos para ejecutar IA **localmente**. Las descargas
pueden proceder de **Hugging Face** y requerir un token de acceso que introduces tú.
El token y la inferencia permanecen en el dispositivo; Hugging Face puede tratar tu
dirección IP y los datos de la descarga conforme a su propia política.

### 3.10. Publicidad contextual

Cuando el build nativo de release tiene activada la integración publicitaria, CrossBit
puede mostrar un banner contextual de Google Mobile Ads únicamente a cuentas Gratis
en Inicio, Calendario de Plan y Progreso. Las cuentas Pro no muestran banners. No se
usan datos de salud, entrenamientos, nutrición, readiness, email ni Firebase `uid` para
segmentar los anuncios y la aplicación no solicita rastreo entre aplicaciones ni
IDFA.

Google UMP solicita o actualiza el consentimiento antes de cargar anuncios y ofrece
**Opciones de privacidad** en Ajustes cuando la región lo exige. Las solicitudes de
anuncios se configuran como no personalizadas; Google puede tratar datos técnicos
necesarios para servir y medir anuncios conforme a su política.

## 4. Categorías especiales de datos

Los datos de entrenamiento, nutrición y métricas corporales pueden constituir datos
relativos a la salud (categoría especial del art. 9 RGPD). Solo se tratan fuera del
dispositivo cuando tú activas y utilizas una función cloud que necesita ese contexto,
con el consentimiento explícito solicitado antes del envío. Puedes evitar nuevos
envíos dejando de usar el coach cloud y utilizando el modo local.

## 5. Destinatarios y encargados del tratamiento

No vendemos tus datos. Los compartimos únicamente cuando es necesario para prestar la
función solicitada, con proveedores que actúan en sus respectivos roles:

| Proveedor | Función | Política |
|---|---|---|
| Google (Firebase Authentication, Firestore, Cloud Run, Vertex AI y, si se activa, Mobile Ads/UMP) | Cuenta, metadatos cloud, inferencia IA y anuncios contextuales | [Política de privacidad de Google](https://policies.google.com/privacy) |
| RevenueCat | Gestión técnica de suscripciones y entitlement | [Política de privacidad de RevenueCat](https://www.revenuecat.com/privacy) |
| Google Play / Apple App Store | Distribución y procesamiento del pago | [Google](https://policies.google.com/privacy) / [Apple](https://www.apple.com/legal/privacy/) |
| Hugging Face | Descarga opcional de modelos locales | [Política de Hugging Face](https://huggingface.co/privacy) |

El proveedor del reconocimiento de voz puede variar según el sistema operativo o el
navegador que utilices.

## 6. Transferencias internacionales

Algunos proveedores pueden tratar datos fuera del Espacio Económico Europeo, incluido
Estados Unidos. Cuando corresponda, las transferencias se basan en las garantías
previstas por la normativa aplicable, como Cláusulas Contractuales Tipo o el marco
UE-EE. UU. de privacidad, según el proveedor y el servicio. La inferencia mediante
Vertex AI puede configurarse en regiones de la UE.

## 7. Plazos de conservación

| Dato | Conservación |
|---|---|
| Entrenamientos, comidas, métricas, chat y planificación local | Hasta que los borres o desinstales la aplicación; las copias exportadas se conservan donde tú las guardes |
| Perfil técnico de cuenta | Hasta completar la eliminación de la cuenta, salvo obligaciones aplicables |
| Contadores y recibos de idempotencia | Hasta 40 días, salvo eliminación anterior |
| Recibos técnicos de webhooks de compra | Hasta 90 días, salvo eliminación anterior |
| Reportes voluntarios de contenido IA | Hasta 30 días, salvo eliminación anterior |
| Checkpoint técnico de eliminación | Mientras sea necesario para completar, reintentar o verificar el flujo; la implementación actual no configura una caducidad automática específica |
| Registros de RevenueCat, Google Play y App Store | Según las políticas de esos proveedores y las obligaciones fiscales o contables aplicables |
| Retención del proveedor de IA | Según las condiciones y la configuración aplicables de Vertex AI |

## 8. Tus derechos y cómo eliminar tus datos

Puedes ejercer, según corresponda, los derechos de acceso, rectificación, supresión,
limitación, oposición, portabilidad y retirada del consentimiento.

- **Acceso y portabilidad:** exporta tus datos desde *Ajustes → Mis datos → Exportar
  mis datos* en formato JSON.
- **Supresión local:** usa *Ajustes → Mis datos → Borrar datos locales*. Esta acción
  borra los registros, la configuración y la copia automática del dispositivo, pero no
  modifica tu cuenta cloud.
- **Supresión de cuenta cloud:** usa *Ajustes → Cuenta → Eliminar cuenta cloud*. El
  flujo pide reautenticación y confirmación; borra los datos cloud descritos en la
  [Política de eliminación de datos](https://adr-arroyo.github.io/crossbit-legal/delete-account.html).
- **Solicitud sin la aplicación:** utiliza la [página pública de eliminación](https://adr-arroyo.github.io/crossbit-legal/delete-account.html)
  o escribe a crossbitapp@gmail.com desde el email asociado a la cuenta.
- **Otros derechos o reclamaciones:** escribe a crossbitapp@gmail.com.

También puedes presentar una reclamación ante la autoridad de control competente. En
España, es la [Agencia Española de Protección de Datos (AEPD)](https://www.aepd.es/).

## 9. Menores

CrossBit no está dirigida a menores de 18 años y no recogemos conscientemente datos de
menores. Si crees que un menor nos ha facilitado datos, contáctanos para eliminarlos.

## 10. Seguridad

Aplicamos medidas técnicas y organizativas razonables, como cifrado en tránsito
(HTTPS/TLS), tokens de autenticación de corta duración, acceso a Firestore solo desde
el proxy autorizado, diagnóstico sin contenidos sensibles y ausencia de claves
privadas de API en el build del modo cloud. Ningún sistema es completamente seguro,
pero trabajamos para proteger tus datos.

## 11. Cambios en esta política

Podemos actualizar esta política. Publicaremos la versión vigente en
https://adr-arroyo.github.io/crossbit-legal/privacy.html con su fecha de actualización
y, cuando los cambios sean materiales, te informaremos dentro de la aplicación.

## 12. Contacto

Adrián Arroyo Pérez — crossbitapp@gmail.com — Condesa Mencia, 123, 5C, Burgos, 09006,
España.
