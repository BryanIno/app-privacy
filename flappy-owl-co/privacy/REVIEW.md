# Flappy Owl & Co — auditoría de privacidad

Fecha: 9 de noviembre de 2026. Registro técnico de mantenimiento; no forma parte
de la política dirigida al jugador.

## Alcance y evidencia

Proyecto inspeccionado: `../copy-flappy-bird`, Godot 4.5.1, versión 1.0.0,
paquete `com.byka.vuelonocturno`. El repositorio del juego no tiene commits;
la auditoría se apoya en archivos locales y en los AAB release examinados.

| Elemento | Evidencia y resultado |
| --- | --- |
| Datos persistentes | `scripts/save_store.gd`: récord (`player.best`), sonido, personaje e idioma en `user://vuelo_nocturno.cfg`; escritura temporal y renombrado. |
| Datos durante la partida | `scripts/main.gd` y `scripts/run_model.gd`: estado y puntuación en memoria, sin historial persistente ni reanudación tras cerrar. |
| Idioma del dispositivo | `scripts/game_locale.gd`: consulta local de `OS.get_locale_language()` para la opción automática. |
| Red | Revisión de scripts, escenas, configuración y dependencias: sin solicitudes HTTP, sockets, backend ni servicios de seguimiento. Los enlaces legales se abren por acción del usuario con `OS.shell_open`. |
| Permisos | `export_presets.cfg`: Internet desactivado. Manifiestos de los AAB anteriores y del nuevo: sin entradas `uses-permission`. |
| Copias | `user_data_backup/allow=false`; manifiestos con `android:allowBackup="false"`. Sin cuentas ni sincronización del desarrollador. |
| SDK | Motor Godot y componentes estándar Android. Sin plugins ni SDK de anuncios, analítica, cuentas, pagos o informes de fallos identificados en el código y el paquete inspeccionado. |
| Protección local | Archivo de configuración sin cifrado adicional del juego; almacenamiento privado Android. No se promete cifrado propio ni acceso remoto para borrar o recuperar el récord. |
| Identidad y contacto | Bryan Inostroza — BYKA Tech, Chile; `bryan.inostroza.dev@gmail.com`, coherente con los Términos existentes y la identidad confirmada en su revisión. |
| Soporte | Correo voluntario, separado del juego. Se explican dirección, mensaje, adjuntos, finalidad de respuesta y seguimiento, proveedores y solicitud de eliminación. No se inventa un plazo automático de borrado ni una configuración del buzón que no se ha auditado. |
| Sitio | HTML estático con CSS y fuentes del repositorio; sin JavaScript, formularios, cookies añadidas ni analítica. GitHub Pages registra IP para seguridad según su documentación. |

No se cambia el identificador del paquete ni el nombre técnico del archivo de
guardado: renombrarlos rompería la continuidad de las instalaciones y sus datos.
«Vuelo Nocturno» se sustituye donde era un nombre comercial visible del aviso.
Los nombres históricos en documentación de builds antiguos conservan su contexto.

## Política e integración

- Español: `/flappy-owl-co/privacy/`; inglés: `en/`; portugués brasileño: `pt-br/`.
  HTML `pt-BR` corresponde al locale Godot `pt_BR`.
- Las tres versiones contienen las mismas 12 secciones: alcance, responsable,
  información, uso, permisos, terceros, seguridad, conservación, eliminación,
  menores, cambios y contacto. Incluyen enlaces recíprocos con los Términos.
- Se reutilizan `styles.css`, las fuentes locales y `terms/terms.css` sin
  modificar el CSS compartido ni las políticas de otras aplicaciones.
- El diálogo existente «Privacidad y licencias» necesitaba corregir el nombre,
  los datos guardados, el contacto y los idiomas. Ahora incluye el texto completo
  y un enlace web por idioma; conserva literalmente las cuatro licencias.
- Las políticas incluidas en `assets/privacy*.txt` contienen los mismos párrafos
  que las páginas web. El filtro de exportación incorpora los tres archivos.
- Las preferencias locales no tienen caducidad; se eliminan al borrar datos o
  desinstalar. Se distingue expresamente borrar caché de borrar almacenamiento.
- No se afirma un público objetivo o una edad mínima que no se haya confirmado.

## Comprobaciones locales

- HTML de las seis páginas legales: idioma, número de secciones, identificadores
  únicos, anclas, rutas de CSS y fuentes y enlaces internos correctos.
- Navegador Chromium: tres versiones legibles a 360 px, sin desbordamiento
  horizontal; versión española también revisada en escritorio. Sin recursos
  externos al cargar las páginas locales.
- Godot: 97 comprobaciones de lógica, 24 de integración y 127 de personajes,
  todas correctas (248 en total).
- Comprobación adicional del diálogo en los tres idiomas: título, datos,
  instrucciones de borrado, contacto, enlace, tamaño y licencias completas;
  capturas visuales examinadas.
- AAB regenerado por cambios de recursos/UI, versión 1.0.0, código 2,
  conservando el paquete y el certificado release anterior. `bundletool validate`
  correcto; los tres textos empaquetados coinciden exactamente con los originales.
- Los scripts compilados de lógica, física, puntuación, guardado y personajes,
  así como las bibliotecas nativas, son idénticos a los del AAB anterior.

No se accede ni se publica en Google Play. El código 2 es posterior al código 1
facilitado y a los AAB locales; no se ha consultado el historial de Play Console.
No se realizó instalación en un Android físico ni se auditó la configuración del
correo. El registro final de publicación y del artefacto queda en
`../copy-flappy-bird/docs/privacy-publication.md`.

## Fuentes primarias consultadas

- [Google Play: User Data / Privacy Policy](https://support.google.com/googleplay/android-developer/answer/10144311#privacy-policy).
- [Política de privacidad de Google](https://policies.google.com/privacy).
- [GitHub Pages: Data collection](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection).
- [Declaración de privacidad de GitHub](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).
