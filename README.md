# IT Suru - Consultoría IT Especializada

[![Nuxt UI](https://img.shields.io/badge/Made%20with-Nuxt%20UI-00DC82?logo=nuxt&labelColor=020420)](https://ui.nuxt.com)

Sitio web corporativo de IT Suru, empresa de consultoría IT especializada en soluciones tecnológicas empresariales.

## Servicios Especializados

- **Networking Empresarial**: Diseño e implementación de redes corporativas de alto rendimiento
- **Seguridad Perimetral**: Protección avanzada con firewalls NGFW, IDS/IPS y detección de amenazas
- **Virtualización VMware**: Consolidación de servidores y optimización de recursos con vSphere
- **Infraestructura On-Premise**: Servidores físicos, almacenamiento SAN/NAS y sistemas de backup
- **Cloud Computing**: Migración y gestión de servicios en AWS, Azure y Google Cloud

## Tecnologías Utilizadas

- **Frontend**: Nuxt.js 4, Vue 3, TypeScript
- **UI Framework**: Nuxt UI con Tailwind CSS
- **Content Management**: Nuxt Content
- **Deployment**: GitHub Pages con GitHub Actions

## Setup del Proyecto

Instalar las dependencias:

```bash
pnpm install
```

## Servidor de Desarrollo

Iniciar el servidor de desarrollo en `http://localhost:3000`:

```bash
pnpm dev
```

## Construcción para Producción

Construir la aplicación para producción:

```bash
pnpm build
```

Generar sitio estático:

```bash
pnpm generate
```

Previsualizar la construcción de producción localmente:

```bash
pnpm preview
```

## Deployment

El sitio se despliega automáticamente en GitHub Pages mediante GitHub Actions cuando se hace push a la rama `main`.

## Estructura de Contenido

- `content/index.yml` - Página principal con información de la empresa
- `content/servicios/` - Páginas detalladas de cada servicio especializado
- `app/components/` - Componentes Vue reutilizables
- `app/pages/` - Páginas de la aplicación

## Contacto

- **Web**: https://it-suru.es
- **Email**: info@it-suru.es
- **Teléfono**: +34 657 99 20 52
- **Dirección**: C/ Sant Manuel, 5, Barcelona, 08031