# 🎵 Tech & EDM Festival

Un sitio web moderno y responsive para un festival de música electrónica, desarrollado con HTML, SASS y JavaScript. Presenta una experiencia visual atractiva con navegación fluida, galería de imágenes interactiva y automatización de tareas con Gulp.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-ISC-green.svg)
![Node](https://img.shields.io/badge/node-%3E%3D14.0.0-brightgreen.svg)

## ✨ Características

- **Diseño Responsive**: Adaptado a dispositivos móviles (480px), tablets (768px) y desktop (1200px+)
- **Navegación Fija**: Header que se fija al hacer scroll para facilitar la navegación
- **Galería Interactiva**: Modal con animaciones fadeIn/fadeOut para visualizar imágenes en tamaño completo
- **Scroll Suave**: Navegación entre secciones con efecto smooth scroll
- **Resaltado Dinámico**: Los enlaces de navegación se destacan según la sección visible
- **Optimización de Imágenes**: Generación automática de formatos modernos (AVIF, WebP) con fallback a JPG
- **Video Hero**: Sección de video con overlay degradado y contenido superpuesto
- **Minificación**: CSS y JavaScript optimizados para producción

## 🎨 Secciones

1. **Header**: Navegación principal con logo y menú responsive
2. **Video Hero**: Presentación impactante con video de fondo y información del evento
3. **Sobre el Festival**: Información general y fecha del evento
4. **Lineup**: Programación de artistas por día y escenario (Techno / EDM)
5. **Galería**: Colección de imágenes del festival (16 fotos)
6. **Boletos**: Pases disponibles (1 día y 2 días) con detalles y precios
7. **Footer**: Información de copyright

## 🛠️ Tecnologías Utilizadas

### Frontend
- **HTML5**: Estructura semántica
- **SASS/SCSS**: Preprocesador CSS con arquitectura modular
- **JavaScript (ES6+)**: Funcionalidades interactivas
- **CSS Grid & Flexbox**: Layouts responsivos
- **Normalize.css**: Consistencia entre navegadores

### Build Tools
- **Gulp 5.0.0**: Automatización de tareas
- **Sass 1.83.0**: Compilación de SCSS
- **Terser**: Minificación de JavaScript
- **Sharp 0.33.5**: Procesamiento y optimización de imágenes
- **Glob**: Búsqueda de archivos

## 📁 Estructura del Proyecto

```
festival-musica/
├── src/
│   ├── scss/
│   │   ├── base/
│   │   │   ├── _normalize.scss
│   │   │   ├── _variables.scss
│   │   │   ├── _mixins.scss
│   │   │   ├── _global.scss
│   │   │   └── _index.scss
│   │   ├── layout/
│   │   │   ├── _header.scss
│   │   │   ├── _video.scss
│   │   │   ├── _festival.scss
│   │   │   ├── _lineup.scss
│   │   │   ├── _galeria.scss
│   │   │   ├── _boletos.scss
│   │   │   ├── _footer.scss
│   │   │   └── _index.scss
│   │   └── app.scss
│   ├── js/
│   │   └── app.js
│   └── img/
│       └── gallery/
│           ├── full/
│           └── thumb/
├── build/
│   ├── css/
│   │   └── app.css
│   ├── js/
│   │   └── app.js
│   └── img/
├── video/
├── gulpfile.js
├── package.json
└── index.html
```

## 🚀 Instalación

### Prerrequisitos
- Node.js >= 14.0.0
- NPM o Yarn

### Pasos

1. **Clonar el repositorio**
```bash
git clone https://github.com/tu-usuario/festival-musica.git
cd festival-musica
```

2. **Instalar dependencias**
```bash
npm install
```

3. **Iniciar modo desarrollo**
```bash
npm run dev
```

El comando `npm run dev` ejecutará Gulp y:
- Compilará SASS a CSS
- Minificará JavaScript
- Optimizará imágenes (genera formatos AVIF, WebP y JPG)
- Creará thumbnails de la galería
- Vigilará cambios en archivos

## 📝 Scripts Disponibles

```bash
# Desarrollo con watch mode
npm run dev

# Compilar SASS manualmente
npm run sass
```

## 🎯 Tareas de Gulp

El archivo `gulpfile.js` incluye las siguientes tareas:

- **`css`**: Compila SCSS a CSS con sourcemaps
- **`js`**: Minifica JavaScript con Terser
- **`imagenes`**: Convierte imágenes a formatos AVIF, WebP y JPG optimizados
- **`crop`**: Genera thumbnails (250x180px) para la galería
- **`dev`**: Modo desarrollo con watch automático
- **`default`**: Ejecuta todas las tareas en serie

## 🎨 Paleta de Colores

```scss
$verde: #4CB8B3;      // Color principal / Techno
$rosa: #F53756;       // Acento / EDM
$amarillo: #FDDA00;   // Destacado
$morado: #752F97;     // Gradientes
$negro: #000000;      // Texto
$blanco: #FFFFFF;     // Backgrounds
```

## 📱 Breakpoints Responsive

```scss
$telefono: 480px;
$tablet: 768px;
$desktop: 1200px;
$desktopXL: 1400px;
```

## 🔧 Mixins SASS Disponibles

```scss
@mixin telefono { /* min-width: 480px */ }
@mixin tablet { /* min-width: 768px */ }
@mixin desktop { /* min-width: 1200px */ }
@mixin desktopXL { /* min-width: 1400px */ }
@mixin contenedor { /* width: 95%, max-width: 120rem */ }
@mixin grid($columnas, $gap) { /* CSS Grid */ }
@mixin resetear-lista { /* Reinicia estilos de listas */ }
```

## 🎭 Funcionalidades JavaScript

### Navegación
- **`navegacionFija()`**: Fija el header al hacer scroll
- **`scrollNav()`**: Smooth scroll a secciones
- **`resaltarEnlace()`**: Resalta el enlace activo según la sección visible

### Galería
- **`crearGaleria()`**: Genera dinámicamente 16 imágenes
- **`mostrarImagen(i)`**: Abre modal con imagen completa
- **`cerrarModal()`**: Cierra modal con animación fadeOut

## 🌐 Navegadores Soportados

- Chrome (últimas 2 versiones)
- Firefox (últimas 2 versiones)
- Safari (últimas 2 versiones)
- Edge (últimas 2 versiones)

## 📸 Optimización de Imágenes

El proyecto incluye procesamiento automático de imágenes:

- **Formatos**: AVIF, WebP, JPG
- **Calidad**: 80%
- **Thumbnails**: 250x180px (centro recortado)
- **Carpetas**: `full/` para originales, `thumb/` para miniaturas

## 🎥 Formato de Video

El proyecto soporta múltiples formatos de video:
- MP4 (H.264)
- WebM
- OGV (Ogg)

## 📦 Dependencias de Desarrollo

```json
{
  "glob": "^11.0.0",
  "gulp": "^5.0.0",
  "gulp-sass": "^6.0.0",
  "gulp-terser": "^2.1.0",
  "sass": "^1.83.0",
  "sharp": "^0.33.5"
}
```

## 🎪 Lineup de Artistas

### Viernes 21 - Techno
- Adam Beyer, Carl Cox, HI-LO, Amelie Lens, CamelPhat, ARTBAT

### Viernes 21 - EDM
- David Guetta, Tiësto, Martin Garrix, Steve Aoki, Afrojack, Vintage Culture

### Sábado 22 - Techno
- Reinier Zonneveld, Eric Prydz, Deadmau5, Joris Voorn, Nina Kraviz, Argy

### Sábado 22 - EDM
- Armin Van Buuren, Calvin Harris, Hardwell, Above & Beyond, Diplo, Steve Angello

## 💡 Características Técnicas

- **Arquitectura CSS**: BEM (Block Element Modifier)
- **Metodología SCSS**: 7-1 Pattern simplificado
- **Grid System**: CSS Grid nativo
- **Animaciones**: CSS Keyframes + Transitions
- **Fuente**: Montserrat (Google Fonts)
- **Lazy Loading**: Implementado en imágenes
- **Sourcemaps**: Habilitados para debugging

## 👤 Autor

Jesús Andrés Hurtado Pareja

📍 Antofagasta, Chile

## 📄 Licencia

Este proyecto fue desarrollado con fines educativos y de práctica profesional. Libre para su uso y referencia en proyectos personales o académicos.

⭐️ Si te gustó este proyecto, dale una estrella en GitHub!
