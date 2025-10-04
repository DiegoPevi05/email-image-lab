# Email Image Lab

Un repositorio mínimo con imágenes de prueba pensadas para email marketing (anchos de 600px, variantes @2x, y fotos con diferentes calidades JPG).

## ¿Para qué sirve?
- Probar **dimensiones** (600px desktop, 300–375px móvil, @2x retina).
- Comparar **pesos** (JPG q40/q70/q90).
- Validar **render** en clientes de correo (Gmail, Outlook, Apple Mail).

## Estructura
```
/images
  logo-120x40.png
  logo-240x80@2x.png
  hero-600x200.jpg
  hero-1200x400@2x.jpg
  banner-600x300.png
  banner-1200x600@2x.png
  photo-600x400-q40.jpg
  photo-600x400-q70.jpg
  photo-600x400-q90.jpg
  thumb-300.jpg
  thumb-600@2x.jpg
index.html
README.md
```

## Publicarlo con GitHub Pages
1. Crea un repo nuevo en GitHub (por ejemplo, `email-image-lab`).  
2. Sube estos archivos (o arrastra el ZIP descomprimido).
3. En **Settings → Pages**, selecciona **Source: Deploy from a branch** y elige **Branch: main / Root**.
4. Tu sitio quedará en: `https://<tu-usuario>.github.io/email-image-lab/`  
   Las imágenes quedarán en URLs como:  
   `https://<tu-usuario>.github.io/email-image-lab/images/hero-600x200.jpg`

> Consejo: en emails usa siempre **URLs absolutas** a tus imágenes.

## Snippet para HTML de email
```html
<!-- Bloque hero 600px con retina -->
<table role="presentation" width="100%" cellpadding="0" cellspacing="0">
  <tr>
    <td align="center">
      <img src="https://<tu-usuario>.github.io/email-image-lab/images/hero-600x200.jpg"
           width="600" height="200" alt="Hero" style="display:block;border:0;outline:0;">
    </td>
  </tr>
</table>

<!-- Logo normal y 2x -->
<img src="https://<tu-usuario>.github.io/email-image-lab/images/logo-120x40.png"
     width="120" height="40" alt="Logo">
<!-- O retina -->
<img src="https://<tu-usuario>.github.io/email-image-lab/images/logo-240x80@2x.png"
     width="120" height="40" alt="Logo (retina)"> <!-- misma dimensión renderizada -->
```

## Recomendaciones rápidas
- **Ancho base 600px** para el contenedor principal.
- Sube versiones **@2x** (el atributo `width` controla el render y mejora nitidez en pantallas retina).
- **PNG** para logos/arte plano, **JPG** para fotos. Evita WebP/HEIC (aún hay clientes sin soporte).
- Mantén fotos entre **60–200 KB** si puedes (calidad 60–75).
- Siempre pon `width` y `height` como atributos, y `style="display:block"` para evitar gaps en algunos clientes.
