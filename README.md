# Portfolio 2026 — Jose Luis Ortiz Sánchez

Sitio personal / portfolio de Jose Luis Ortiz Sánchez, Fullstack Developer especializado en PHP/Laravel, Node.js, React y Flutter.

Pensado como reemplazo estático de [luisjdev.com](https://luisjdev.com) (aún no desplegado).

## Stack

Sitio 100% estático, sin frameworks ni build step:

- HTML5
- CSS3 (variables, grid/flexbox, animaciones on-scroll con `IntersectionObserver`)
- JavaScript vanilla

## Estructura

```
.
├── index.html            # Contenido y estructura de todas las secciones
├── css/
│   └── style.css         # Estilos, tema oscuro y responsive
├── js/
│   └── main.js           # Menú móvil, scroll-spy y animaciones on-scroll
└── assets/
    ├── favicon.svg
    ├── Jose_Luis_Ortiz_CV.pdf   # CV descargable desde el sitio
    └── cv-source.html           # Fuente HTML del CV (se convierte a PDF)
```

## Secciones

- **Hero** — presentación, disponibilidad y enlaces de contacto
- **Sobre mí** — resumen profesional y stats
- **Experiencia** — timeline de experiencia laboral y educación
- **Tecnologías** — stack agrupado por categoría (frontend, backend, bases de datos, IA, devops)
- **Proyectos** — trabajo destacado con enlaces a Google Play / repositorios
- **Contacto** — email, LinkedIn y GitHub

## Desarrollo local

No requiere instalación de dependencias. Basta con servir la carpeta con cualquier servidor estático, por ejemplo:

```bash
python -m http.server 8000
```

y abrir `http://localhost:8000`.

## CV

El PDF en `assets/Jose_Luis_Ortiz_CV.pdf` se genera a partir de `assets/cv-source.html` usando impresión headless de Chromium/Edge:

```bash
msedge --headless --disable-gpu --no-pdf-header-footer --print-to-pdf-no-header \
  --print-to-pdf="assets/Jose_Luis_Ortiz_CV.pdf" "assets/cv-source.html"
```

## Licencia

Contenido y código de uso personal — © Jose Luis Ortiz Sánchez.
