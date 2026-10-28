# Nube Unificada

Plataforma propia de almacenamiento en la nube, con gestor de archivos, usuarios, temas personalizables y soporte para conectar cuentas de Google Drive, OneDrive, MEGA y Dropbox desde la misma web.

## Características

- Gestión de usuarios con login y sesiones
- Gestor de archivos (subida, descarga, papelera, enlaces compartidos con contraseña)
- Subidas por trozos (chunked uploads) para archivos grandes
- Temas personalizables desde la interfaz
- Panel de ajustes: perfil, contraseña, correo, seguridad
- Conexión de cuentas externas de almacenamiento (Google Drive, OneDrive, MEGA, Dropbox) vía rclone
- Backend construido en Node.js puro, sin dependencias externas

## Stack

- **Backend:** Node.js (sin frameworks externos)
- **Almacenamiento externo:** rclone
- **Base de datos:** archivo local (SQLite/JSON, según configuración)

## Requisitos

- Node.js instalado en el servidor
- rclone configurado para las integraciones de nube externas
- Un dominio o subdominio propio apuntando al servicio (opcional, recomendado)

## Instalación

```bash
git clone https://github.com/mcnetstudio/mi-nube-unificada.git
cd mi-nube-unificada
node server.js
```

Por defecto corre en `http://localhost:3000`.

## Configuración

Revisa el archivo de configuración del proyecto para ajustar:

- Puerto de escucha
- Rutas de almacenamiento de datos y archivos subidos
- Credenciales de OAuth para las integraciones de Drive/OneDrive/Dropbox

*(Pendiente: documentar variables de entorno específicas)*

## Uso

1. Accede a la interfaz web.
2. Crea tu cuenta de administrador en el primer arranque (instalación guiada).
3. Desde **Ajustes → Almacenamiento**, conecta las cuentas externas que quieras usar.
4. Administra archivos, usuarios y temas desde el panel principal.

## Seguridad

- Las sesiones y contraseñas se manejan con buenas prácticas de seguridad (hashing, tokens).
- Los enlaces compartidos pueden protegerse con contraseña.
- Se recomienda servir la aplicación detrás de HTTPS (por ejemplo, vía Cloudflare Tunnel).

## Roadmap

- Más proveedores de almacenamiento externo
- Mejoras de rendimiento en subidas grandes
- Panel de actividad y auditoría

## Contacto

Para soporte o dudas, escribe a **contacto@mc-gt.online**.

## Licencia

Este proyecto se distribuye bajo la licencia [MIT](LICENSE).

---

Desarrollado por **McNetStudio** — Costa Rica.
