# MY HD

App para Android que procesa videos MP4/MOV directamente en el telefono, sin recodificar ni comprimir.
El original no se modifica: se crea una copia nueva llamada `NOMBRE_MY_method.mp4`.

## Archivos del repositorio
| Archivo | Para que sirve |
|---|---|
| `index.html` | La app (pantalla, barra turbo y procesamiento) |
| `manifest.json`, `sw.js` | Permiten instalarla como app desde Chrome |
| `icon-192.png`, `icon-512.png` | Iconos de la app |
| `package.json`, `capacitor.config.json` | Configuracion para crear el APK |
| `build-apk.yml` | Receta que GitHub usa para compilar el APK (ver paso 3) |
| `README.md` | Estas instrucciones |

## 1. Crear el repositorio (desde el telefono)
1. En github.com toca **+ > New repository**. Nombre: `my-hd`. **Public**. **Create repository**.
2. Toca **uploading an existing file** y sube los 9 archivos sueltos (no el zip, no carpetas). **Commit changes**.

## 2. Version web instalable (opcional)
**Settings > Pages**, Branch `main`, carpeta `/ (root)`, **Save**. En 1-2 minutos abre `https://TU-USUARIO.github.io/my-hd/` en Chrome > menu > **Instalar app**.

## 3. Crear el APK
1. Abre `build-apk.yml` en tu repo, toca el lapiz (editar) y en el nombre del archivo escribe `.github/workflows/build-apk.yml`. **Commit changes**. Esto mueve el archivo a su carpeta.
2. Ve a la pestana **Actions**. Si pide permiso, toca **I understand my workflows, go ahead and enable them**.
3. Entra a **Construir APK > Run workflow**. Tarda unos 5-10 minutos.
4. Cuando termine con check verde, ve a **Releases** (en la pagina principal del repo), abre la mas reciente y descarga **MY-HD.apk**.
5. Abre el APK en el telefono. Android pedira permitir "instalar apps desconocidas" para tu navegador; aceptalo.

## Guardar videos en el APK
Al terminar de procesar se abre el menu de compartir de Android: elige **Archivos / Guardar en el dispositivo**, Fotos, Drive, etc.

## Actualizar
Sube el archivo nuevo con el mismo nombre (Add file > Upload files). El APK se recompila solo y aparece una nueva version en Releases.
