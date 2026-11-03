# AFA Arlequín – web

Web estática de la Asociación de Familias (AFA) de la EIM Arlequín. Todo está en un solo archivo (`index.html`): no necesita servidor, base de datos ni compilación.

La web tiene 4 apartados (Inicio, Calendario, Información y Contacto). *Información* agrupa La asociación, Grupos de trabajo y La escuela. Se pasa de uno a otro deslizando a los lados o con el menú de pestañas fijo abajo; en escritorio también con las flechas del teclado. El ancho máximo en escritorio es de 1400 px.

## Ver la web en local

Abre `index.html` con doble clic en cualquier navegador.

## Publicarla con GitHub Pages

1. Sube `index.html`, la carpeta `img/`, `README.md` y `.nojekyll` a la raíz de un repositorio de GitHub.
2. En el repositorio, ve a **Settings → Pages**.
3. En **Build and deployment**, elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`, y guarda.
4. En un par de minutos la web estará en https://afaarlequin.github.io/web/.

## Cómo editar el contenido

Todo está en `index.html`. Los puntos que se cambian con más frecuencia están marcados con comentarios:

- **Anuncios (apartado *Inicio*)**: se leen del blog https://afaarlequin.blogspot.com (cuenta afa.arlequin@gmail.com). Para publicar uno, envía un correo a la dirección secreta de Blogger (Configuración → Correo electrónico): el asunto es el título y las fotos adjuntas van dentro del anuncio. Para editar o borrar, usa Blogger. El blog debe tener el acceso de lectura público y el feed en "Completo"; puede estar oculto a los buscadores.
- **Calendario de Google**: en el apartado *Calendario*, el `data-src` del `<iframe id="cal">`. Debe ser el ID de un calendario **público** (Configuración del calendario → Integrar calendario).
- **Actas, Cuentas y Junta Directiva**: en el apartado *Información*, los `href` de esas tres tarjetas. Comprueba que estén compartidos como "Cualquier persona con el enlace".
- **Grupos de trabajo**: cada bloque es un desplegable (`<details>`). Las fotos se añaden dentro del `<div class="fotos">` de cada bloque, guardando las imágenes en `img/actividades/`.
- **Buzón de sugerencias**: formulario anónimo del apartado *Contacto*. Usa el servicio gratuito [Web3Forms](https://web3forms.com), que reenvía cada sugerencia a afa.arlequin@gmail.com con el asunto «sugerencias web». La clave (`access_key`) está en el propio formulario: es pública por diseño y solo sirve para enviar a ese correo.
- **Correos de contacto**: la lista del apartado *Contacto*.
- **Logo**: está en la carpeta `img/` (`logo.jpg` es el original; `logo-icono.png` es el árbol recortado para la cabecera y `favicon.png` el icono de la pestaña).
- **Año del pie de página**: aparece en el `<footer>` de cada apartado.

El archivo `.nojekyll` indica a GitHub Pages que sirva los archivos tal cual, sin procesarlos.
