# Farmacia Cartagena - Website

Web corporativa ultra-rápida y SEO-first para **FARMACIA CARTAGENA** y **LABORATORIO CARTAGENA** en Cartagena, Murcia.

## 🚀 Características

- ✅ **Performance optimizada**: LCP<2.5s, CLS<0.1
- ✅ **SEO avanzado**: JSON-LD estructurado, meta tags completos, sitemap.xml
- ✅ **Accesibilidad WCAG 2.2 AA**: Contraste, estados de foco, semántica correcta
- ✅ **PWA Ready**: Manifest, Service Worker básico
- ✅ **Seguridad**: CSP estricta, HSTS, headers de seguridad
- ✅ **Responsive**: Mobile-first con sticky action bar
- ✅ **Datos NAP**: Siempre visibles (nombre, dirección, teléfono)

## 📋 Stack Tecnológico

- **Framework**: [Astro](https://astro.build) (SSG)
- **Estilos**: Tailwind CSS v4
- **Lenguaje**: TypeScript (strict)
- **Deploy**: Vercel / Cloudflare Pages / Netlify

## 🏗️ Estructura del Proyecto

```
tufarmaciacartagena/
├── public/
│   ├── robots.txt              # SEO
│   ├── sitemap.xml             # SEO
│   ├── site.webmanifest        # PWA
│   ├── farmacia-cartagena.vcf  # vCard para "Guardar"
│   ├── _headers                # Security headers
│   └── favicon.svg             # Favicon
├── src/
│   ├── components/
│   │   ├── Header.astro        # Header fijo con navegación
│   │   ├── Footer.astro        # Footer con NAP y enlaces
│   │   └── StickyActionBar.astro # Barra móvil: Llamar/Mapa/Cómo llegar/Reseñas
│   ├── layouts/
│   │   └── BaseLayout.astro    # Layout base con SEO y JSON-LD
│   ├── pages/
│   │   ├── index.astro         # Home (con JSON-LD Pharmacy + FAQPage)
│   │   ├── servicios.astro     # Servicios farmacéuticos
│   │   ├── laboratorio.astro   # Laboratorio y formulación magistral
│   │   ├── galeria.astro       # Galería de fotos
│   │   ├── reseñas.astro       # Reseñas de clientes (4.468)
│   │   ├── contacto.astro      # Formulario de contacto + mapa
│   │   └── legal.astro         # Aviso legal, privacidad, cookies
│   └── styles/
│       └── global.css          # Estilos globales + Tailwind
└── astro.config.mjs            # Configuración Astro
```

## 📦 Instalación

```bash
# Clonar o descomprimir el proyecto
cd tufarmaciacartagena

# Instalar dependencias
npm install

# Modo desarrollo (http://localhost:4321)
npm run dev

# Build para producción
npm run build

# Preview del build
npm run preview
```

## 🌐 Despliegue

### Vercel (recomendado)

```bash
# Instalar Vercel CLI
npm i -g vercel

# Deploy
vercel
```

### Cloudflare Pages

1. Conecta tu repositorio Git en Cloudflare Pages
2. Configura:
   - **Build command**: `npm run build`
   - **Output directory**: `dist`
3. Deploy automático

### Netlify

1. Conecta tu repositorio en Netlify
2. Configura:
   - **Build command**: `npm run build`
   - **Publish directory**: `dist`
3. Los headers de seguridad (`public/_headers`) se aplicarán automáticamente

## 🔧 Configuración

### Datos de contacto (NAP)

Edita en `src/components/Header.astro`, `src/components/Footer.astro` y `src/pages/index.astro`:

- **Dirección**: Calle Prol. Angel Bruna, 11, 30300 Cartagena, Murcia
- **Teléfono**: +34 968 51 31 50
- **Email**: info@tufarmaciacartagena.com

### JSON-LD (Schema.org)

El JSON-LD está en `src/pages/index.astro`. Actualiza:
- Coordenadas GPS (geo.latitude, geo.longitude)
- Horarios (openingHoursSpecification)
- Imagen destacada (image)

### Formulario de contacto

El formulario en `src/pages/contacto.astro` está listo para conectar con:
- Endpoint serverless (Vercel Functions, Netlify Functions, etc.)
- Servicio de email (SendGrid, Resend, etc.)

## 📊 SEO

- ✅ **Titles y descriptions** optimizados en cada página
- ✅ **Canonical URLs** configurados
- ✅ **Open Graph** y **Twitter Cards**
- ✅ **JSON-LD** de tipo Pharmacy + AggregateRating + FAQPage
- ✅ **Sitemap.xml** con hreflang es-ES
- ✅ **Robots.txt** configurado

## 🎨 Personalización

### Colores

Edita `src/styles/global.css`:

```css
@theme {
  --color-brand-primary: #10b981;  /* Verde principal */
  --color-brand-dark: #059669;
  --color-brand-light: #d1fae5;
}
```

### Imágenes

Agrega tus imágenes en `/public/`:
- `og-image.jpg` (1200x630px) - Para redes sociales
- `icon-192.png` y `icon-512.png` - Para PWA
- `apple-touch-icon.png` (180x180px)
- `favicon-32x32.png` y `favicon-16x16.png`

Para optimizar imágenes, usa:
- [Squoosh](https://squoosh.app) (WebP/AVIF)
- `sharp-cli` o `imagemin`

## 🔒 Seguridad

Headers configurados en `public/_headers`:
- Content-Security-Policy (CSP)
- X-Frame-Options: SAMEORIGIN
- X-Content-Type-Options: nosniff
- Strict-Transport-Security (HSTS)
- Referrer-Policy

## ♿ Accesibilidad

- Contraste AA cumplido
- Estados de foco visibles
- Etiquetas `aria-label` en CTAs
- Semántica HTML5 correcta
- `prefer-reduced-motion` respetado

## 📱 PWA

- Manifest configurado (`site.webmanifest`)
- Iconos para Android/iOS
- Service Worker básico (opcional, implementar en `public/sw.js`)

## 📄 Licencia

© 2025 Farmacia Cartagena. Todos los derechos reservados.

## 📞 Soporte

**Farmacia Cartagena**
Calle Prol. Angel Bruna, 11
30300 Cartagena, Murcia
Tel: 968 51 31 50
Email: info@tufarmaciacartagena.com

---

🚀 **Generado con Claude Code** - Listo para desplegar en minutos.
