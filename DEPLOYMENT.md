# Guía de Despliegue - MVV Natural USA

## El problema actual

Vercel está desplegando un commit antiguo (07a9f9e) que no incluye las dependencias necesarias para Tailwind CSS v4.

## Solución: Pasos para desplegar correctamente

### 1. Asegúrate de que todos los archivos estén actualizados en GitHub

Los archivos críticos que deben estar en tu repositorio:
- `package.json` (debe incluir `@tailwindcss/postcss`)
- `postcss.config.mjs` (configuración de PostCSS)
- `astro.config.mjs` (configuración de Astro)
- Todos los archivos en `src/`

### 2. Elimina el lockfile antiguo

En tu máquina local, ejecuta:
\`\`\`bash
rm pnpm-lock.yaml
\`\`\`

### 3. Reinstala las dependencias

\`\`\`bash
pnpm install
\`\`\`

Esto generará un nuevo `pnpm-lock.yaml` con todas las dependencias correctas, incluyendo `@tailwindcss/postcss`.

### 4. Verifica que el build funcione localmente

\`\`\`bash
pnpm run build
\`\`\`

Si el build es exitoso localmente, continúa al siguiente paso.

### 5. Sube los cambios a GitHub

\`\`\`bash
git add .
git commit -m "Fix: Add @tailwindcss/postcss dependency"
git push origin main
\`\`\`

### 6. Redespliega en Vercel

Vercel debería detectar automáticamente el nuevo commit y redesplegar. Si no lo hace:
- Ve a tu dashboard de Vercel
- Selecciona el proyecto MVV
- Haz clic en "Redeploy" en el último deployment

## Verificación

Una vez desplegado, verifica que:
- El sitio carga correctamente
- Los estilos de Tailwind se aplican
- Todas las páginas funcionan (inicio, productos, testimonios, FAQ, contacto)

## Archivos clave del proyecto

\`\`\`
mvv-natural-usa/
├── package.json              # Dependencias (incluye @tailwindcss/postcss)
├── postcss.config.mjs        # Configuración PostCSS para Tailwind v4
├── astro.config.mjs          # Configuración de Astro
├── src/
│   ├── pages/               # Páginas del sitio
│   ├── layouts/             # Layout base
│   ├── components/          # Componentes reutilizables
│   └── styles/              # Estilos globales
└── public/                  # Archivos estáticos
\`\`\`

## Soporte

Si el problema persiste después de seguir estos pasos:
1. Verifica que el commit más reciente en GitHub incluya todos los archivos
2. Revisa los logs de build en Vercel para errores específicos
3. Asegúrate de que no haya archivos de Next.js mezclados (app/, next.config.js, etc.)
\`\`\`

```file=".npmrc"
# Configuración de pnpm para el proyecto
auto-install-peers=true
shamefully-hoist=true
