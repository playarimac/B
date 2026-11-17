# Mi TV Deportes v4.0 · reproductor nativo ExoPlayer

**Novedad v4.0:** el video ya no lo reproduce el navegador interno (hls.js) sino **ExoPlayer**, el reproductor nativo de Android
(decodificador por hardware, reintentos propios, cambio automático de fuente, vigilante anticongelamiento).
Esto solo funciona en las **opciones B y C** (las que compilan el proyecto `android/`). La opción A (convertidores online)
sigue usando el reproductor antiguo.

Si la app se cierra sola, al abrirla de nuevo aparece en rojo, arriba, el motivo anotado.

# Mi TV Deportes (interfaz: www/index.html)

## Opción A · La más rápida (sin PC, ~5 min): ZIP → APK online
1. Crea un ZIP que contenga SOLO `index.html` (en la raíz del ZIP, no dentro de una carpeta).
2. Sube el ZIP a un convertidor "HTML ZIP → APK" (AppsGeyser, APKBuild.org u otro similar), pon nombre "Mi TV Deportes" y genera el APK.
3. Pasa el APK a la TV (USB o app "Send Files to TV") e instálalo (permite "orígenes desconocidos").
Limitación: estos convertidores no incluyen el proxy antibloqueo nativo, y algunos canales pueden no abrir.

## Opción B · La mejor (Android Studio, con antibloqueo nativo)
1. Instala Android Studio. 2. File → Open → carpeta `android/`. 3. Espera a que sincronice.
4. Build → Build Bundle(s)/APK(s) → Build APK(s). 5. "locate" → `app-release.apk`.
(`www/index.html` ya está dentro del proyecto; si lo editas, vuelve a compilar.)

## Opción C · GitHub (automático): sube esta carpeta (con .github) → Actions → Releases.

Control remoto: flechas/OK navegan · Atrás sale de pantalla completa · Menú/Info/Rojo = calidad · Canal +/- cambia de canal (estas teclas solo en opciones B y C).
