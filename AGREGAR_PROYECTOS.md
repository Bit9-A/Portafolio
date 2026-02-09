# Cómo Agregar Nuevos Proyectos

Este portafolio utiliza un sistema basado en datos para los proyectos. Para agregar un nuevo proyecto, simplemente edita el archivo JSON.

## Ubicación del archivo

`src/data/projects.json`

## Estructura de un proyecto

```json
{
  "id": "nombre-unico",
  "tag": "Etiqueta del Proyecto",
  "title": "Título del Proyecto",
  "description": "Descripción detallada del proyecto...",
  "tech": ["Tecnología1", "Tecnología2", "Tecnología3"],
  "icon": "nombre_icono_material",
  "image": "nombre-imagen.webp",
  "frontendUrl": "https://github.com/usuario/repo-frontend",
  "backendUrl": "https://github.com/usuario/repo-backend",
  "demoUrl": "https://demo.ejemplo.com",
  "featured": true
}
```

## Campos explicados

- **id**: Identificador único (obligatorio)
- **tag**: Etiqueta que aparece arriba del título (obligatorio)
- **title**: Nombre del proyecto (obligatorio)
- **description**: Descripción del proyecto (obligatorio)
- **tech**: Array de tecnologías usadas (obligatorio)
- **icon**: Nombre del icono de Material Symbols (obligatorio)
- **image**: Nombre del archivo de imagen en `src/assets/` (opcional)
- **frontendUrl**: URL del repositorio frontend (opcional)
- **backendUrl**: URL del repositorio backend (opcional)
- **demoUrl**: URL de la demo en vivo (opcional)
- **featured**: `true` para mostrar en el carrusel principal (obligatorio)

## Tipos de botones según URLs

### Proyecto con Frontend y Backend

Si defines `frontendUrl` y `backendUrl`, se mostrarán dos botones con iconos de GitHub:

- Botón "Frontend" → enlaza a `frontendUrl`
- Botón "Backend" → enlaza a `backendUrl`

### Proyecto con Demo

Si solo defines `demoUrl`, se mostrará:

- Botón "Ver Demo" → enlaza a `demoUrl`

### Proyecto sin URLs

Si no defines ninguna URL, se mostrará:

- Botón "Próximamente" (deshabilitado)

## Ejemplo: Agregar un nuevo proyecto

1. Abre `src/data/projects.json`
2. Agrega tu proyecto en ambos idiomas (en y es):

```json
{
  "en": [
    // ... proyectos existentes
    {
      "id": "mi-nuevo-proyecto",
      "tag": "Web App",
      "title": "My Awesome Project",
      "description": "A revolutionary web application that...",
      "tech": ["Vue.js", "Firebase", "Tailwind"],
      "icon": "web",
      "image": "mi-proyecto.webp",
      "demoUrl": "https://mi-proyecto.com",
      "featured": true
    }
  ],
  "es": [
    // ... proyectos existentes
    {
      "id": "mi-nuevo-proyecto",
      "tag": "Aplicación Web",
      "title": "Mi Proyecto Increíble",
      "description": "Una aplicación web revolucionaria que...",
      "tech": ["Vue.js", "Firebase", "Tailwind"],
      "icon": "web",
      "image": "mi-proyecto.webp",
      "demoUrl": "https://mi-proyecto.com",
      "featured": true
    }
  ]
}
```

3. Si agregaste una imagen, colócala en `src/assets/`
4. ¡Listo! El proyecto aparecerá automáticamente en el carrusel

## Notas importantes

- Los proyectos con `"featured": true` aparecen en el carrusel principal
- Mantén el mismo `id` en ambos idiomas (en y es)
- Las imágenes deben estar en formato `.webp`, `.png`, `.jpg` o `.jpeg`
- Los iconos deben ser nombres válidos de [Material Symbols](https://fonts.google.com/icons)
