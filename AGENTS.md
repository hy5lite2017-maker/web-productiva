# Proyecto: web-productiva

## Descripción
Sitio web futurista multi-página con temática neón naranja (#ff8c00), fondo negro, grises y efectos de glow. Totalmente responsive para móviles. Hosteado en GitHub Pages.

## Estructura de archivos
```
/ (raíz)
├── index.html             # Página principal con carrusel, parallax, loader, hamburger
├── login.html             # Inicio de sesión con toggle de contraseña
├── registro.html          # Registro con toggle de contraseña
├── desarrollo-web.html    # Servicio: Desarrollo Web
├── diseno-ui-ux.html      # Servicio: Diseño UI/UX
├── consultoria.html       # Servicio: Consultoría
├── soporte-tecnico.html   # Servicio: Soporte Técnico
├── portafolio.html        # Portafolio
├── contacto.html          # Contacto
├── style.css              # Único archivo CSS (~20KB) — TODOS los estilos globales
├── AGENTS.md              # Este archivo — contexto para continuar la sesión
└── imagenes/              # Imágenes locales (carrusel, fondo, etc.)
    ├── fondo.jpg
    ├── images (1).jpg
    ├── images (2).jpg
    ├── images (3).jpg
    ├── images (4).jpg
    ├── images (5).jpg
    ├── images (6).jpg
    └── images (7).jpg
```

## Paleta de colores
- Fondo: `#000`, `#0d0d0d`, `#1a1a1a`
- Acento neón: `#ff8c00` (naranja)
- Texto: `#999`, `#ccc`, `#fff`
- Bordes: `#1a1a1a`, `#2a2a2a`, `#333`

## Características implementadas
- **Carrusel**: 4 slides con imágenes locales, texto superpuesto en `.slide-content` semitransparente, flechas de navegación, dots, auto-play cada 4s
- **Líneas neón**: 6 líneas animadas (`.linea1`–`.linea6`) con grosores 3–7px, colores naranja/rojo/gris, movimiento independiente con `@keyframes`
- **Parallax**: JS en todas las páginas — las líneas se mueven a diferentes velocidades al hacer scroll
- **Loader**: overlay full-screen con doble anillo giratorio neón + texto "Cargando..." con puntos animados. Se oculta con fade al cargar la página
- **Hamburger menu**: para móvil (<768px), menú vertical desplegable con toggle JS. Dropdown "Servicios" se abre al tocar en móvil
- **Navbar desktop**: fija, centrada, con dropdown hover
- **Perfil**: botón circular con SVG de persona, fondo semitransparente, backdrop-filter blur
- **Registro**: botón pill con SVG de usuario+, fondo semitransparente
- **Service pages**: icono en caja semitransparente 100×100 con blur y hover scale
- **Footer**: fijo con backdrop-filter blur, enlaces, SVGs de YouTube/Instagram/WhatsApp
- **Auth forms**: login y registro con inputs flotantes, toggle de contraseña (SVG ojo)
- **Responsive**: 2 breakpoints (768px y 480px)

## Textos de servicio (tono impactante y moderno)
| Página | Texto |
|--------|-------|
| Desarrollo Web | "Webs y aplicaciones con tecnología de punta. Rápidos, seguros y diseñados para crecer contigo." |
| Diseño UI/UX | "Interfaces que enamoran. Experiencias memorables diseñadas para las personas, no solo para las pantallas." |
| Consultoría | "Estrategia digital que impulsa tu negocio. Decisiones inteligentes basadas en datos y experiencia." |
| Soporte Técnico | "Soporte técnico cuando lo necesitas. Resolvemos, optimizamos y mantenemos tu negocio en marcha." |
| Portafolio | "Proyectos que marcan la diferencia. Innovación, calidad y excelencia en cada línea de código." |
| Contacto | "Hablemos. Cuéntanos tu idea y la hacemos realidad. Estamos listos para construir el futuro contigo." |

## Convenciones de código
- No usar comentarios en HTML/CSS/JS (excepto separadores de secciones)
- No usar bibliotecas externas ni iconos — todo es CSS puro + SVGs inline
- No emojis en producción (usar SVGs inline para iconos)
- `style.css` contiene TODOS los estilos globales; no hay CSS por página
- GitHub Pages URL: `https://[usuario].github.io/web-productiva/`

## Componentes reutilizables (presentes en TODAS las páginas)
- `.loader-overlay` + `.loader-ring` + `.loader-text` — loader de carga
- `.profile-box` > `.profile-btn` — botón perfil con SVG persona
- `.register-btn-box` > `.register-nav-btn` — botón registro/login con SVG
- `.navbar` > `.hamburger` + `.nav-menu` — menú de navegación
- `.fondo-glow` — glow central pulsante
- `.linea.linea1`–`.linea6` — líneas neón animadas con parallax
- `.site-footer` — footer fijo con blur

## JS global (en todas las páginas)
- `toggleMenu()` — abre/cierra hamburger menu
- `.dropbtn` click handler en móvil — toggle dropdown Servicios
- `window.load` — oculta loader con fade
- `window.scroll` — parallax de líneas

## Pendiente / Mejoras posibles
- (ninguna — proyecto funcional y completo)

## Notas importantes
- No hay git configurado en esta máquina; subir a GitHub manualmente vía navegador
- No hay npm/node disponible en esta máquina
- Las imágenes del carrusel están en `imagenes/` con nombres tipo `images (3).jpg`
- El botón de perfil (👤) actualmente no tiene funcionalidad — es placeholder
