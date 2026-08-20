# RSU FCA — Pasaporte de Horas RSU

Herramienta de Rumi Académico para que los estudiantes de la FCA registren su
participación en proyectos sociales, voluntariados y actividades de
capacitación, y sigan el avance de sus 40 horas de Responsabilidad Social
Universitaria (RSU) en un solo lugar.

Es un único archivo HTML autocontenido (sin backend propio): usa el
almacenamiento persistente de Claude (`window.storage`) para guardar
actividades, inscripciones y el progreso de cada estudiante, y EmailJS para
notificarte por Gmail cada vez que alguien se inscribe.

---

## 1. Crear el repositorio en GitHub

1. Entra a **[github.com/unmsm-rumi](https://github.com/unmsm-rumi)** (o la
   cuenta/organización donde tienes los demás proyectos de Rumi).
2. Haz clic en **New repository**.
3. En **Repository name** escribe exactamente:
   ```
   rsu_fca
   ```
4. Déjalo como **Public** (para que GitHub Pages funcione gratis).
5. No marques ninguna casilla de "Add a README" ni ".gitignore" (lo vamos a
   subir manualmente).
6. Haz clic en **Create repository**.

## 2. Subir los archivos

1. Dentro del repositorio recién creado, haz clic en
   **"uploading an existing file"** (o el botón **Add file → Upload files**).
2. Arrastra estos dos archivos a la ventana:
   - `index.html` ← el archivo principal de la herramienta (**debe llamarse
     exactamente `index.html`**, no `rsu_fca.html` ni otro nombre, o GitHub
     Pages no lo va a reconocer como página de inicio).
   - `README.md` ← este mismo archivo, para que quede documentado en el repo.
3. Escribe un mensaje de commit corto, por ejemplo `Primera versión del
   Pasaporte RSU`.
4. Haz clic en **Commit changes**.

## 3. Activar GitHub Pages

1. Dentro del repositorio, ve a **Settings** (pestaña superior).
2. En el menú izquierdo, haz clic en **Pages**.
3. En **Source**, selecciona:
   - Branch: **main**
   - Folder: **/ (root)**
4. Haz clic en **Save**.
5. Espera 1-2 minutos. GitHub va a mostrar un mensaje como:
   > Your site is live at `https://unmsm-rumi.github.io/rsu_fca/`

Ese es el enlace que vas a compartir con los estudiantes.

## 4. Acceder al panel de gestión

El botón de administración está oculto para los estudiantes por seguridad.
Para entrar como equipo Rumi, agrega `?admin=1` al final del enlace:

```
https://unmsm-rumi.github.io/rsu_fca/?admin=1
```

Ahí verás el botón **"Panel de gestión (equipo Rumi)"**. Te va a pedir el
código de acceso (por defecto `RUMI2026` — puedes cambiarlo editando
`RSU_ADMIN_CODE` dentro de `index.html` en GitHub, sin necesidad de programas
externos: solo entra al archivo en GitHub, haz clic en el lápiz ✏️ para
editar, busca esa línea, cámbiala y da "Commit changes").

Desde el panel puedes:
- Publicar nuevas actividades (proyectos sociales, voluntariados, talleres,
  conversatorios, simposios, conferencias).
- Confirmar o rechazar inscripciones pendientes.
- Ver cuántos correos de EmailJS llevas usados este mes.
- Descargar un CSV con todos los registros.

## 5. Notas importantes

- **EmailJS**: las notificaciones por inscripción usan tu cuenta de EmailJS
  (`service_4ea37ij` / plantilla `template_ww4usvq`). El plan gratis permite
  200 correos al mes; la herramienta deja de enviar automáticamente antes de
  llegar al límite, así que las inscripciones nunca se ven afectadas aunque
  se agote la cuota — solo revisa el panel de "Confirmaciones pendientes" con
  más frecuencia esos días.
- **Datos compartidos**: toda la información (actividades, cupos,
  inscripciones, horas por estudiante) vive en un almacenamiento compartido
  entre todos los que abran el enlace. No es un Excel ni una base de datos
  que puedas explorar directamente fuera de la página — para eso está el
  botón de exportar CSV dentro del panel.
- **Actualizar la herramienta**: si en el futuro quieres que te ayude a
  cambiar algo (colores, textos, nuevos campos, etc.), pídemelo aquí en el
  chat, te doy el archivo `index.html` actualizado y solo tienes que volver a
  subirlo a GitHub (Add file → Upload files, sobrescribiendo el anterior).
