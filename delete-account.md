---
permalink: /delete-account.html
---

# Política de eliminación de datos y de la cuenta — CrossBit

Esta página está disponible en una **URL pública** para que puedas solicitar el borrado
sin instalar la aplicación.

**Última actualización:** 1 de septiembre de 2026

En CrossBit puedes eliminar tus datos y tu cuenta en cualquier momento. Como la mayoría
de tus datos (entrenamientos, comidas, métricas, chat) se guardan **únicamente en tu
dispositivo**, su eliminación es inmediata y local.

## 1. Eliminar los datos guardados en tu dispositivo

Tienes dos opciones:

- **Desde la app:** *Ajustes → Mis datos → Borrar datos locales*. Esto borra
  todos los registros locales (entrenamientos, comidas, métricas, historial de chat,
  planes, récords, plantillas, preferencias y configuración), además de la copia
  automática local cuando exista.
- **Desinstalando la aplicación:** al desinstalar CrossBit, el sistema operativo
  elimina el almacenamiento local de la app. Las copias exportadas o guardadas en la
  carpeta de documentos del dispositivo pueden permanecer y debes borrarlas también
  si quieres eliminar todas las copias.

> 💡 Antes de borrar, puedes guardar una copia con *Ajustes → Mis datos → Exportar mis
> datos* (archivo JSON).

## 2. Eliminar tu cuenta y los datos del servidor

Si creaste una cuenta para usar el entrenador IA en la nube o CrossBit Pro, puedes
eliminar la cuenta y los datos asociados:

- **Desde la app:** *Ajustes → Cuenta → Eliminar cuenta cloud*. Te pediremos tu
  contraseña para reautenticar la sesión y una confirmación explícita.
- **Desde la web (sin la app):** escríbenos a **crossbitapp@gmail.com** desde la dirección asociada a tu cuenta, indicando "Eliminar cuenta CrossBit".

### Qué se elimina

| Dato | ¿Se elimina? | Plazo |
|------|--------------|-------|
| Cuenta de autenticación (Firebase Auth) | Sí | Al completar el flujo de borrado remoto |
| Documento de usuario (nivel y expiración de suscripción) | Sí | Al completar el flujo de borrado remoto |
| Customer y estado de suscripción en RevenueCat | Se solicita su eliminación como parte del flujo | Según RevenueCat y la tienda |
| Contadores de uso e idempotencia técnica | Sí (o por caducidad automática) | ≤ 40 días |
| Recibos técnicos de webhooks de compra | Sí (o por caducidad automática) | ≤ 90 días |
| Reportes voluntarios de contenido IA | Sí | Inmediato al borrar; ≤ 30 días si no se borra la cuenta |
| Checkpoint técnico del borrado | Registro mínimo para completar o verificar la solicitud; no contiene salud ni chat | Mientras sea necesario; la implementación actual no configura una caducidad automática específica |
| Datos locales del dispositivo | Los eliminas tú (sección 1) | Inmediato |

### Qué puede conservarse

- **Registros de facturación y compra** gestionados por **Google Play**, **App Store**
  y **RevenueCat** pueden conservarse durante el plazo exigido por sus políticas y por
  la normativa fiscal y contable. Para cancelar una suscripción activa, utiliza las
  herramientas de gestión de la tienda correspondiente.

## 3. Cancelar la suscripción

Eliminar la cuenta **no cancela automáticamente** una suscripción activa ni borra los
registros que las tiendas deban conservar. Cancélala
desde los ajustes de suscripciones de tu cuenta de **Google Play** o **App Store** para
evitar futuras renovaciones.

## 4. Contacto

Para cualquier solicitud relacionada con tus datos: **crossbitapp@gmail.com**.
