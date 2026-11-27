# ReportaYA: app Android

Reporta incidencias urbanas (huecos, alumbrado, basura...) con foto y ubicación, y
sigue su atención por la municipalidad. Proyecto académico de la Universidad de Lima.

## Cómo entrar

Es **una sola app para todos**: lo que ves depende de la cuenta con la que inicias sesión.

| Quién | Desde dónde | Cuenta |
|---|---|---|
| Ciudadano | APK en Android, o la versión web en iPhone/PC | Se registra solo en *Registrarse* y entra al instante |
| Operador municipal | La misma app (o la web, cómodo desde la PC) | Cuenta entregada por el administrador |
| Técnico | La misma app | Cuenta entregada por el administrador |

**Versión web (iPhone, PC, cualquier navegador):** https://enzoordonez.github.io/ReportaYA-App/
En iPhone, ábrela en Safari y usa *Compartir > Agregar a inicio* para tenerla como app.

## Descargar (Android)

**[Descargar ReportaYA 1.1.3 (APK, 56 MB)](https://github.com/EnzoOrdonez/ReportaYA-App/releases/latest)**

Enlace directo alternativo: [apk/ReportaYA-1.1.3.apk](https://github.com/EnzoOrdonez/ReportaYA-App/raw/main/apk/ReportaYA-1.1.3.apk)

SHA-256: `2713f8264190fa0627203cc3c93e2f0236bf59e9a10a5c6d27287d5a8b66aa8f`

## Instalar

1. Si tienes la **1.1.0**, **1.1.1** o **1.1.2**, instala la 1.1.3 encima (se actualiza sin perder nada).
   Si tienes una versión anterior a la 1.1.0, **desinstálala primero**: estaba firmada
   con otra llave y Android no deja actualizar encima.
2. Abre el APK descargado. Si Android lo pide, permite *Instalar apps desconocidas*
   para tu navegador o gestor de archivos.
3. Abre la app y toca **Regístrate**. La cuenta queda activa al instante (no hace falta
   confirmar el correo).

## Novedades de la 1.1.3

- Etiquetas de estado, botones y avisos con colores de contraste suficiente (4,5:1 o más).
- Textos con tildes en la recuperación de contraseña, en el mapa y en el correo con el código.
- Los avisos ya no prometen una notificación: indican que el ciudadano verá el resultado en el detalle de su reporte.
- Las pestañas de la pantalla del técnico se leen sobre el fondo verde.

## Novedades de la 1.1.2

- El técnico vuelve a su bandeja al finalizar un reporte y el operador a la cola al rechazarlo.
- Cada reporte y cada cierre técnico llevan de 1 a 3 fotos; el aviso muestra el código del reporte.
- Accesibilidad: contraste del texto, áreas táctiles de 48 dp, etiquetas para el lector de
  pantalla y textos del sistema en español. Sin cortes con el texto ampliado al 200 %.
- En tablet y PC la app se centra con un ancho de lectura en lugar de estirarse.
- Ortografía corregida en las pantallas.

## Servidor

La app usa el backend en la nube `https://reportaya-api-mcg4.onrender.com`
(código: [EnzoOrdonez/reportaya-api](https://github.com/EnzoOrdonez/reportaya-api)).
Está en el plan gratis de Render: si nadie lo usó en 15 minutos, el servidor se apaga
y tarda alrededor de un minuto en volver. Un servicio externo (cron-job.org) lo consulta
cada 10 minutos para mantenerlo despierto y, si aun así está dormido, la app lo despierta
apenas se abre y avisa en el login mientras arranca.

Desde la pantalla de inicio de sesión, el botón **Servidor** permite apuntar la app a
otra dirección (por ejemplo, un backend local en `http://IP-DE-TU-PC:8081`).

## Créditos

App: [jeffangeloss/ReportaYA-Front](https://github.com/jeffangeloss/ReportaYA-Front).
Backend: [Yotzuga/ReportaYA-Backend](https://github.com/Yotzuga/ReportaYA-Backend).
