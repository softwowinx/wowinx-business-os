# wowinX Spatial Business OS

Portal interno de estrategia y decisión de wowinX (líneas **WX180** y **BeFootball**).
Página estática única (`index.html`) servida en GitHub Pages.

## Acceso

El portal está protegido con **Supabase Auth**. El contenido no se incluye en el
archivo: se carga desde Supabase únicamente tras iniciar sesión. La gestión de
usuarios (alta, reset de contraseña, baja) se hace desde la pestaña **Usuarios**,
visible solo para administradores.

- Login: email + contraseña.
- Cada usuario puede cambiar su propia contraseña desde el portal.
- Un administrador puede dar de alta y resetear usuarios.

## Técnico

- `index.html` — única página (HTML/CSS/JS inline; logo y favicon en base64).
- Auth, contenido (`bos_content`) y gestión de usuarios (Edge Function `bos-usuarios`)
  en Supabase. La clave del cliente es la *publishable key* (pública por diseño).
