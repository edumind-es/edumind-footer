# @edumind/footer

Componente footer canónico del ecosistema EDUmind.

## Instalación

```bash
# Configurar el registry primero (una sola vez por proyecto)
npm config set @edumind:registry http://localhost:4873

# Instalar
npm install @edumind/footer
```

## Uso básico

```tsx
import { EDUmindFooter } from '@edumind/footer';
import '@edumind/footer/styles';

// En tu componente:
<EDUmindFooter
  appName="Liga EDUmind"
  version="2.1.0"
  versionStage="Beta"
  locale="es"
/>
```

## Props principales

| Prop | Tipo | Default | Descripción |
|------|------|---------|-------------|
| `appName` | `string` | — | Nombre de la app (obligatorio) |
| `version` | `string` | — | Versión semver (obligatorio) |
| `versionStage` | `Alpha\|Beta\|RC\|Stable` | — | Etapa de desarrollo |
| `locale` | `es\|en\|gl` | `'es'` | Idioma del footer |
| `density` | `full\|compact` | `'full'` | Densidad visual |
| `author` | `string` | `'EDUmind Team'` | Autor en el copyright |
| `homeHref` | `string` | — | URL del botón inicio |
| `previousPage` | `NavigationLink` | — | Enlace anterior |
| `nextPage` | `NavigationLink` | — | Enlace siguiente |
| `feedbackUrl` | `string` | `mailto:contacto@edumind.es` | URL de feedback |
| `showVersion` | `boolean` | `true` | Mostrar badge de versión |
| `hideNavigation` | `boolean` | `false` | Ocultar nav anterior/siguiente |

## Personalización con CSS

El componente usa variables CSS que heredan del sistema de diseño EDUmind:

```css
.mi-app {
  --footer-bg: #0f1117;        /* Fondo dark */
  --footer-text: #7a8099;      /* Texto */
  --footer-link: #4f8ef7;      /* Links */
  --mundo-fisico: #10b981;     /* Color "Apoyar" */
}
```

## Actualizar el paquete (para mantenimiento)

```bash
# Desde /var/www/edumind-footer-pkg
npm version patch   # 1.0.0 → 1.0.1
npm publish
```

Los proyectos que usen `"@edumind/footer": "^1.0.0"` recibirán la actualización
con `npm update @edumind/footer`.

## Instalación desde GitHub

```bash
npm install github:edumind-es/edumind-footer
```

## Licencia

Software libre con doble licencia **AGPL-3.0-or-later OR EUPL-1.2** (ver `LICENSE`).
EDUmind® es una marca registrada — ver `TRADEMARKS.md`.
