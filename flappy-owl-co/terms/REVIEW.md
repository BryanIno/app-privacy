# Flappy Owl & Co: alcance y revisión de los términos

Fecha: 8 de noviembre de 2026. Documento de mantenimiento para el desarrollador;
no forma parte de las condiciones dirigidas al jugador ni acredita revisión por abogado.

## Alcance y evidencia

- Sitio existente: HTML/CSS estáticos, GitHub Pages, rama `main`, raíz del repositorio.
  Se reutilizan `styles.css`, Geist local y las clases `policy-site` y `policy-page`.
  El CSS adicional está limitado a los nuevos documentos. No hay JavaScript,
  cookies añadidas, analítica ni dependencias nuevas.
- Juego inspeccionado en modo de solo lectura: proyecto local `copy-flappy-bird`.
  `project.godot` identifica Flappy Owl & Co 1.0.0, Godot 4 y los idiomas
  `es`, `en`, `pt_BR`. No hay un commit del juego al que fijar esta revisión:
  su repositorio local aún no tiene commits. No se ejecutaron Godot ni builds Android.
- `scripts/save_store.gd` y sus llamadas en `scripts/main.gd`: récord, sonido,
  personaje e idioma en almacenamiento local; no persistencia de la partida en curso.
- `export_presets.cfg`: permiso de Internet y copia de seguridad Android desactivados.
  README, scripts, escenas y configuración examinados: sin cuentas, backend,
  funciones sociales, anuncios, compras, suscripciones ni SDK de analítica identificados.
  Esto describe el código local; no se certifica el binario publicado en Google Play.
- Nombre del responsable y país de operación confirmados por el titular durante
  esta tarea: Bryan Inostroza, BYKA Tech, Chile. No se inventó razón social,
  domicilio postal, registro de empresa ni clasificación por edades.
- En el sitio no existe una política de privacidad web de Flappy Owl & Co.
  Por eso no se añade un enlace a una página inexistente. El aviso del juego
  está accesible desde «Privacidad y licencias».
- HTML usa `pt-BR` (BCP 47), correspondiente al `pt_BR` de Godot. Español es
  la URL principal y `x-default`; las versiones `en/` y `pt-br/` tienen URL
  propia, canonical y enlaces recíprocos `hreflang`. No se impone un idioma
  preferente para reducir derechos. Las tres versiones contienen las mismas
  16 secciones y condiciones.

## Pendientes antes de considerar definitivo el contenido jurídico

1. Revisión profesional de aceptación por instalación/uso y capacidad de menores,
   obligaciones de información del proveedor (incluido si corresponde publicar
   domicilio), garantías, responsabilidad y cambios de condiciones según los
   países de distribución. La elección de ley chilena conserva las normas
   imperativas de otros países y no impone tribunales exclusivos en Chile.
2. Confirmar en Play Console la clasificación, público objetivo, gratuidad,
   distribución territorial y que la versión distribuida coincide con el código
   inspeccionado. No se tuvo acceso a esa configuración ni se alteró.
3. Revisar la titularidad y las licencias de recursos, tipografías, motor y marca.
   Se preservan expresamente las licencias de terceros y excepciones legales;
   no se afirma que todos los elementos sean propiedad exclusiva del desarrollador.
4. Corregir en una tarea autorizada el aviso de privacidad incluido en el juego:
   `assets/privacy.txt` aún se titula «Vuelo Nocturno» y solo menciona récord y
   sonido, aunque el código también guarda personaje e idioma. No se modificó.
5. Crear/publicar por separado una política de privacidad exacta con el nombre
   actual y enlazarla desde los términos cuando exista. La URL de términos no
   sustituye el campo obligatorio de política de privacidad de Google Play.
   La publicación de estos términos no demuestra el cumplimiento integral de
   las políticas de Google Play. Integración dentro del juego y AAB quedan
   fuera de esta tarea.
6. Revisar con asesoría las tres traducciones jurídicas en conjunto. La revisión
   técnica de equivalencia no constituye traducción jurídica certificada.

## Validaciones locales

- Enlaces y recursos: directorio principal y los tres HTML; 27 referencias por
  versión, incluidos anclas, idiomas, correo, hojas de estilo y fuente.
- Estructura: un `h1`, 16 `h2`, 16 secciones identificadas, identificadores únicos,
  mismo orden de secciones y metadatos de idioma/canonical coherentes.
- Chromium: 320, 360, 393, 412, 768 y 1440 px, en los tres idiomas, con índice
  abierto y cerrado (36 combinaciones), sin desbordamiento horizontal.
- Texto al 200 % sobre 320 px: sin desbordamiento en los tres idiomas.
- Teclado en las tres versiones: salto al contenido, foco visible, selector de
  idioma, apertura del índice y navegación a secciones mediante Enter.
- Emulación Android Pixel 7, JavaScript desactivado mediante Chrome DevTools:
  navegación real entre los tres idiomas, apertura del índice y anclas operativas.
  No se probó en un teléfono Android físico ni se realizó una auditoría WCAG completa.
- Contraste calculado frente al fondo compartido: texto 17,39:1, texto secundario
  7,73:1, enlaces 5,50:1; todos superan 4,5:1. Objetivos del selector de idioma de
  al menos 44 px de alto. Zoom permitido, sin animaciones ni rastreadores añadidos.
- Solo se solicita HTML, CSS y la fuente local Geist (aproximadamente 52 KB de
  contenido sin compresión en una carga inicial del documento español).
- Carioca, Linterna FX, PIN / SPIN, CSS y fuente compartidos: comprobados mediante
  HTTPS público con estado 200 y contenido idéntico a los archivos originales.
- `git diff --check` sin incidencias. No se modifican páginas legales existentes,
  CSS compartido, fuentes ni archivos del juego.

## Fuentes consultadas

- [SERNAC: artículo 4 de la Ley 19.496, derechos irrenunciables](https://www.sernac.cl/portal/609/w3-propertyvalue-58672.html).
- [Google Play: datos de usuario y política de privacidad](https://support.google.com/googleplay/android-developer/answer/10144311?hl=es).
- [Web Interface Guidelines](https://github.com/vercel-labs/web-interface-guidelines/blob/main/command.md),
  para la revisión técnica de accesibilidad e interfaz.

Las fuentes orientan la redacción y revisión; no implican aprobación oficial
de Google, SERNAC ni otra autoridad.
