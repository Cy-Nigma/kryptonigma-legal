# Sitio Legal y Tutorial — Kryptonigma

Este sitio contiene los 3 documentos que la app debe enlazar por URL en vez de empaquetar dentro del APK:

- `terminos.html` — Términos y Condiciones de Uso
- `privacidad.html` — Política de Privacidad (la URL que exige Google Play)
- `tutorial.html` — Tutorial de uso con espacio para capturas de pantalla
- `index.html` — redirige automáticamente a Términos y Condiciones
- `assets/style.css` — estilos compartidos por las 3 páginas
- `assets/img/` — carpeta donde van las capturas de pantalla

## Capturas de pantalla incluidas

El tutorial ya incluye 10 capturas reales de la app en `assets/img/`:

- `onboarding-0-carga.jpg` — pantalla de carga
- `onboarding-1-idioma.jpg` — selección de idioma
- `onboarding-1-aviso.jpg` — aviso de privacidad ("Antes de empezar")
- `onboarding-2-correo.jpg` — correo de respaldo
- `menu-lateral.jpg` — menú lateral completo
- `boveda-raiz.jpg` — vista de la bóveda raíz
- `centro-cifrado.jpg` — Centro de Cifrado con archivo seleccionado
- `notas-seguras-vacio.jpg` — Editor de Notas Seguras vacío
- `notas-seguras-escrito.jpg` — Editor de Notas Seguras con texto
- `llave-encriptacion.jpg` — pantalla para definir la llave
- `eliminar-confirmacion.jpg` — confirmación de eliminación

## Cómo agregar más capturas (pantallas pendientes)

Cuando tengas capturas de Método de Seguridad, Cambiar PIN, Compartir archivo, Ver archivo desencriptado, Respaldar/Restaurar Bóveda o Exportar Kit de Emergencia:

1. Súbelas a `assets/img/` con un nombre descriptivo.
2. En `tutorial.html`, agrega un nuevo bloque `step-card` siguiendo el mismo patrón que los existentes:

```html
<div class="step-card">
  <div class="screenshot-frame">
    <img src="assets/img/NOMBRE-DE-TU-IMAGEN.jpg" alt="Descripción de la pantalla">
  </div>
  <div>
    <h3>Título del paso</h3>
    <p>Explicación de qué hace esta pantalla.</p>
  </div>
</div>
```

## Cómo publicar gratis en GitHub Pages

1. Crea un repositorio nuevo en GitHub, por ejemplo `kryptonigma-legal` (puede ser público).
2. Sube todos estos archivos manteniendo la estructura de carpetas (`assets/style.css`, `assets/img/...`, y los `.html` en la raíz).
3. Ve a **Settings → Pages** del repositorio.
4. En "Source", selecciona la rama `main` y la carpeta `/ (root)`.
5. Guarda. GitHub te dará una URL como:
   `https://[tu-usuario].github.io/kryptonigma-legal/`
6. Las URLs finales quedarán así:
   - Privacidad: `https://[tu-usuario].github.io/kryptonigma-legal/privacidad.html`
   - Términos: `https://[tu-usuario].github.io/kryptonigma-legal/terminos.html`
   - Tutorial: `https://[tu-usuario].github.io/kryptonigma-legal/tutorial.html`

Esa URL de Privacidad es la que se ingresa en la Google Play Console, en la sección "Política de Privacidad" del listado de la app.

## Actualizar contenido después de publicar

Cualquier cambio futuro (nueva versión de términos, nuevas capturas, etc.) solo requiere subir el archivo actualizado al repositorio — no hace falta sacar una nueva versión del APK.
