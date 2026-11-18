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

**[Descargar ReportaYA 1.1.0 (APK, 55 MB)](https://github.com/EnzoOrdonez/ReportaYA-App/releases/latest)**

Enlace directo alternativo: [apk/ReportaYA-1.1.0.apk](https://github.com/EnzoOrdonez/ReportaYA-App/raw/main/apk/ReportaYA-1.1.0.apk)

SHA-256: `1fd9bbd83d42aa86af010c590b4b4f162abc61b237f9bd0d120727aca66e5e0d`

## Instalar

1. Si tenías una versión anterior de ReportaYA, **desinstálala primero**: esta versión
   está firmada con otra llave y Android no la deja actualizar encima.
2. Abre el APK descargado. Si Android lo pide, permite *Instalar apps desconocidas*
   para tu navegador o gestor de archivos.
3. Abre la app y toca **Regístrate**. La cuenta queda activa al instante (no hace falta
   confirmar el correo).

## Servidor

La app usa el backend en la nube `https://reportaya-api-mcg4.onrender.com`
(código: [EnzoOrdonez/reportaya-api](https://github.com/EnzoOrdonez/reportaya-api)).
Está en el plan gratis de Render: si nadie lo usó en un rato, la primera petición
puede tardar alrededor de un minuto mientras el servidor despierta. Este repositorio
lo mantiene despierto con un ping cada 10 minutos (`.github/workflows/mantener-activo.yml`).

Desde la pantalla de inicio de sesión, el botón **Servidor** permite apuntar la app a
otra dirección (por ejemplo, un backend local en `http://IP-DE-TU-PC:8081`).

## Créditos

App: [jeffangeloss/ReportaYA-Front](https://github.com/jeffangeloss/ReportaYA-Front).
Backend: [Yotzuga/ReportaYA-Backend](https://github.com/Yotzuga/ReportaYA-Backend).
