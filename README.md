# Bosque 4.0 — PWA

App de concentración con bosque nocturno, 16 especies, cuatro hábitats, crecimiento en cinco etapas y fauna progresiva.

## Publicar en GitHub Pages

1. Sube **todos los archivos de esta carpeta** a la raíz de tu repositorio (reemplaza el `index.html` antiguo).
2. En **Settings → Pages → Build and deployment**, selecciona **Deploy from a branch**, rama **main**, carpeta **/(root)** y guarda.
3. Abre `https://TU-USUARIO.github.io/bosque-app/` desde Safari en el iPhone.
4. Compartir → **Añadir a pantalla de inicio** → **Abrir como app** (si aparece) → Añadir.
5. Si aparece una versión antigua, cierra la app, recarga Safari o elimina el icono y vuelve a añadirlo. El service worker puede conservar temporalmente archivos antiguos.

## Comportamiento

- Temporizador real basado en `Date.now()` y marca de fin persistida. Continúa al bloquear el móvil o cerrar la app y se regulariza al volver a abrirla.
- **No hay detección ni bloqueo de otras apps**: eso requiere desarrollo nativo iOS.
- Los árboles se incorporan al bosque al finalizar la sesión; las cinco etapas se ven **durante** la sesión. Los árboles completados quedan maduros.
- Fauna: pájaros 10 árboles; ardillas 20; conejos 35; luciérnagas 50. Cada especie puede ocultarse/mostrarse tras desbloquearla.
- Los datos se guardan en `localStorage`, por dispositivo/origen. **No se sincronizan** entre Safari y la app instalada. Exporta e importa copias desde Progreso.
- La app funciona sin conexión una vez que se han almacenado los recursos. GitHub Pages es **público**: no usar para datos secretos.

## Prueba rápida

Para verificar una sesión sin esperar 15 minutos, en una copia de desarrollo usa las herramientas del navegador para cambiar el valor `end` de `bosque4-state-v1` en localStorage a una fecha pasada (milisegundos Unix) y recarga. No hagas esto en tus datos de producción.
