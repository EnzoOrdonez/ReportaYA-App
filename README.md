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

**[Descargar ReportaYA 1.1.4 (APK, 56 MB)](https://github.com/EnzoOrdonez/ReportaYA-App/releases/latest)**

Enlace directo alternativo: [apk/ReportaYA-1.1.4.apk](https://github.com/EnzoOrdonez/ReportaYA-App/raw/main/apk/ReportaYA-1.1.4.apk)

SHA-256: `59da3b457fbf8e8be7412d55a71cb3be437b66438da263d73f8b9c9aacc57e31`

## Instalar

1. Si tienes una versión desde la **1.1.0** hasta la **1.1.3**, instala la 1.1.4 encima (se actualiza sin perder nada).
   Si tienes una versión anterior a la 1.1.0, **desinstálala primero**: estaba firmada
   con otra llave y Android no deja actualizar encima.
2. Abre el APK descargado. Si Android lo pide, permite *Instalar apps desconocidas*
   para tu navegador o gestor de archivos.
3. Abre la app y toca **Registrarse**. Acepta el aviso de privacidad; la cuenta queda activa
   al instante (no hace falta confirmar el correo).

## Novedades de la 1.1.4

- Al crear un reporte la app pide tu ubicación una sola vez y marca el punto en el mapa; el
  botón *Mi ubicación* la vuelve a pedir. Si niegas el permiso, tocas el mapa como antes.
- Aviso de alcance: ReportaYA es una simulación académica, el número del reporte no es un
  expediente municipal y se muestran los números de emergencia 105, 116 y 106.
- Aviso de privacidad antes de registrarte (se guarda la fecha y la versión aceptadas) y
  consultable desde el login.
- Antes de enviar ves un resumen del reporte y puedes añadir una referencia del lugar.
- Cada foto pesa como máximo 2 MB y debe ser JPG o PNG.
- Recuperar contraseña: el correo trae un botón que abre la web con el código puesto, y en la
  app puedes pegar el código con *Pegar código*. Cambiar la contraseña cierra tus otras sesiones.
- Seguridad: contraseña de al menos 8 caracteres, bloqueo de 5 minutos tras 5 intentos
  fallidos y cierre de sesión que invalida el token en el servidor.
- Se ocultó el selector de servidor (mantén presionado el título *ReportaYA* para verlo).

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

Para pruebas, mantén presionado el título **ReportaYA** en el login: aparece el botón
**Servidor**, que permite apuntar la app a otra dirección (por ejemplo, un backend local en
`http://IP-DE-TU-PC:8081`).

## Créditos

App: [jeffangeloss/ReportaYA-Front](https://github.com/jeffangeloss/ReportaYA-Front).
Backend: [Yotzuga/ReportaYA-Backend](https://github.com/Yotzuga/ReportaYA-Backend).
