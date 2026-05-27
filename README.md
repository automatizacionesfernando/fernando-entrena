# Fit Fernando - Instrucciones de despliegue

App PWA personal de fitness con seguimiento de pesas, cardio, comidas y peso corporal.

## Funcionalidades

- **Hoy**: vista del día con rutina programada según día de la semana
- **Pesas**: rutinas A/B/C con tus pesos de inicio precargados, registro de series y reps
- **Cardio**: progresión de 10 semanas de intervalos en cinta
- **Comidas**: checklist diario + menú base lun-jue y fin de semana
- **Peso**: registro con gráfico de evolución, línea de objetivo (100 kg), histórico
- **Temporizador de descanso**: botón flotante naranja, presets de 60s/90s/2min/3min, vibración + pitido al terminar
- **Exportar/Importar JSON**: respaldo de todos tus datos

Los datos se guardan en el `localStorage` del navegador del móvil. No se envían a ningún servidor.

## Despliegue en GitHub Pages (15 min)

### 1. Crear repositorio

1. Entra a [github.com](https://github.com) y haz login
2. Click en el `+` arriba a la derecha → **New repository**
3. Nombre: `fit-fernando` (o el que quieras)
4. Marca **Public** (necesario para Pages gratis)
5. NO marques "Add a README" (vamos a subir el nuestro)
6. **Create repository**

### 2. Subir el archivo

**Opción A — Por web (sin terminal):**

1. En la página del repo recién creado, click en **uploading an existing file**
2. Arrastra el archivo `index.html` desde tu carpeta
3. Abajo, en "Commit changes", escribe: `primera versión`
4. Click **Commit changes**

**Opción B — Por terminal (si ya usas git):**

```bash
cd carpeta-donde-está-index.html
git init
git add index.html
git commit -m "primera versión"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/fit-fernando.git
git push -u origin main
```

### 3. Activar GitHub Pages

1. En el repo, ve a **Settings** (pestaña arriba a la derecha)
2. En el menú lateral izquierdo, busca **Pages**
3. En "Source" elige: **Deploy from a branch**
4. En "Branch" elige: **main** y carpeta **/ (root)**
5. Click **Save**
6. Espera 1-2 minutos. Te aparecerá arriba un mensaje verde con tu URL:
   `https://TU_USUARIO.github.io/fit-fernando/`

### 4. Instalar en el móvil

1. Abre esa URL en el navegador del móvil (Chrome en Android, Safari en iPhone)
2. **Android (Chrome)**: menú de tres puntos → **Instalar app** o **Añadir a pantalla principal**
3. **iPhone (Safari)**: botón compartir (cuadradito con flecha hacia arriba) → **Añadir a pantalla de inicio**
4. Te aparecerá un icono en la pantalla principal como si fuera una app nativa
5. Al abrirla, ocupa toda la pantalla sin barra del navegador

## Cómo actualizar la app

Cuando quieras cambios:
1. Edita `index.html` (puedes hacerlo directamente en github.com, click en el archivo → icono lápiz)
2. **Commit changes**
3. En 1-2 min, el cambio está en línea
4. Refresca la app en el móvil (en algunos casos hay que cerrarla y abrirla de nuevo)

## Cómo respaldar tus datos

En la app → pestaña **Peso** → abajo del todo: **Exportar respaldo**. Te descarga un JSON. Guárdalo en Drive o donde quieras.

Para restaurar: **Importar respaldo** → eliges el archivo JSON.

## Datos precargados

- Peso inicial: **106 kg**
- Objetivo: **100 kg**
- Pesos de inicio en rutinas: los que me dijiste (remo 60, jalón 70, bíceps 12, tríceps 20, press pecho subido a 14 sugerido, hombros subido a 10 sugerido)
- Semana de cardio: **1** (2 min camina / 1 min corre)

Puedes ajustar todo desde dentro de la app.

## Privacidad

- Tus datos viven SOLO en tu teléfono (localStorage del navegador)
- GitHub solo aloja el archivo `index.html`, no tus datos
- El repo puede ser público sin riesgo: nadie ve tus pesos ni tu peso corporal
