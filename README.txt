BOSQUE 3.0 — PROTOTIPO WEB PARA iPHONE

1. Abre index.html en un navegador de ordenador para probarlo.
2. Para usarlo desde Safari en iPhone, publica index.html en un alojamiento HTTPS estático (por ejemplo, GitHub Pages o Netlify).
3. En Safari iOS, pulsa Compartir > Añadir a pantalla de inicio.
4. Los árboles se guardan localmente en el navegador del dispositivo mediante localStorage.

IMPORTANTE: Esta versión es una aplicación web/prototipo, NO una aplicación iOS nativa. No puede bloquear aplicaciones, detectar desbloqueos ni garantizar sesiones en segundo plano. Para eso habrá que construir la app en SwiftUI y solicitar los permisos FamilyControls y las extensiones apropiadas de Screen Time.

PROGRESIÓN
- Cuatro familias de cuatro especies, 16 especies en total.
- Cinco etapas visuales: semilla, brote, joven, desarrollado, maduro.
- Fauna: pájaros (10), ardillas (20), conejos (35), luciérnagas (50).
- Vista de bosque panorámico con río meandriforme y hábitats en cuatro cuadrantes.
- Simulación de sesiones: botones para avanzar, completar o abandonar.
- Persistencia local en el navegador.

SIGUIENTE ETAPA NATIVA
- Xcode + SwiftUI para vistas y animaciones.
- SwiftData para sesiones, árboles y desbloqueos.
- FamilyControls, ManagedSettings, DeviceActivity para autorización y restricciones permitidas por iOS.
- Reglas explícitas de pérdida del árbol (abandonar sesión o desactivar restricciones, según las capacidades y permisos reales).
- Pruebas en dispositivo físico y firma de desarrollo.
