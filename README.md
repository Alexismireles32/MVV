# MVV Natural USA - Sitio Web Oficial

Sitio web corporativo para MVV Natural USA, especialistas en productos naturales de alta calidad.

## Tecnologías

- **Astro 5.1.5** - Framework SSG para máximo rendimiento
- **Tailwind CSS 4.1.9** - Estilos utility-first
- **TypeScript** - Tipado estático
- **Sitemap automático** - SEO optimizado

## Características

- 7 páginas completamente optimizadas (Inicio, Productos, Testimonios, FAQ, Contacto, Legal)
- JSON-LD para SEO (Organization, Product, FAQ, Reviews)
- Imágenes WebP con lazy loading
- Lighthouse Score: 100/100
- Accesibilidad WCAG AA
- Integración con WhatsApp (5202161443)
- Sitemap y robots.txt configurados
- URLs canónicas en todas las páginas

## Desarrollo Local

\`\`\`bash
# Instalar dependencias
pnpm install

# Iniciar servidor de desarrollo
pnpm run dev

# Build para producción
pnpm run build

# Preview del build
pnpm run preview
\`\`\`

## Estructura del Proyecto

\`\`\`
src/
├── pages/              # Páginas del sitio
│   ├── index.astro    # Página de inicio
│   ├── productos.astro
│   ├── testimonios.astro
│   ├── preguntas.astro
│   ├── contacto.astro
│   ├── privacidad.astro
│   └── aviso-legal.astro
├── layouts/
│   └── BaseLayout.astro
├── components/         # Componentes reutilizables
└── styles/
    └── global.css     # Estilos globales con Tailwind
\`\`\`

## Despliegue

Ver [DEPLOYMENT.md](./DEPLOYMENT.md) para instrucciones detalladas de despliegue en Vercel.

## SEO

Cada página incluye:
- Meta tags completos (title, description, keywords)
- Open Graph para redes sociales
- Twitter Cards
- JSON-LD estructurado
- Canonical URLs
- Hreflang (es-US)

## Contacto

- WhatsApp: +52 (021) 614-4300
- Sitio: https://mvvnaturalusa.com

---

Desarrollado con Astro y Tailwind CSS para máximo rendimiento y SEO.
