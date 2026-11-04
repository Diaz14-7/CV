# CV Web

Currículum web personal de **Álvaro Díaz Pérez**, hecho con [Astro](https://astro.build) y organizado por componentes. Es una página de una sola pantalla con navegación por secciones, un carrusel con efecto LED rojo y un diseño oscuro con acento rojo.

- GitHub: [Diaz14-7](https://github.com/Diaz14-7)
- LinkedIn: [Álvaro Díaz Pérez](https://www.linkedin.com/in/%C3%A1lvaro-d%C3%ADaz-p%C3%A9rez-300b28445)

## Características

- **Menú fijo y translúcido** con efecto de desenfoque. Cada opción baja suavemente a su apartado y la casa devuelve al inicio.
- **Opciones sombreadas:** pasan de gris oscuro a negro al pasar el ratón.
- **Carrusel horizontal** con desplazamiento y anclaje al centro. Cada foto lleva a su apartado y tiene un resplandor rojo animado.
- **Cinco apartados:** Sobre mí, Habilidades, Formación, Experiencia y Contacto, además del carrusel de inicio.
- **Enlaces externos:** GitHub y LinkedIn desde el menú y el pie, y los logos de las empresas en Experiencia llevan a sus webs.
- **Diseño adaptable (responsive):** en pantallas estrechas las cuadrículas y columnas se reorganizan.

## Tecnologías

- Astro (componentes `.astro`)
- HTML y CSS, con los estilos dentro de cada componente
- Sin frameworks de interfaz ni JavaScript propio

## Requisitos

- [Node.js](https://nodejs.org) 18 o superior
- npm

## Puesta en marcha

```bash
# Instalar dependencias
npm install

# Servidor de desarrollo (http://localhost:4321)
npm run dev

# Generar la versión de producción en /dist
npm run build

# Previsualizar la versión de producción
npm run preview
```

## Estructura del proyecto

```text
/
├── public/                  # Imágenes y logos (se sirven desde la raíz: /logo.png)
├── src/
│   ├── components/
│   │   ├── Cabecera.astro       # Menú fijo con casa, apartados, GitHub y LinkedIn
│   │   ├── Carrusel.astro       # Fotos con efecto LED rojo
│   │   ├── SobreMi.astro        # Texto de presentación e ilustración
│   │   ├── Habilidades.astro    # Cuadrícula de tecnologías
│   │   ├── Formacion.astro      # Lista numerada de estudios
│   │   ├── Experiencia.astro    # Empresas con logo, puesto y años
│   │   └── Contacto.astro       # Contacto, redes y franja final
│   ├── layouts/
│   │   └── Layout.astro         # Estructura HTML base y estilos globales
│   └── pages/
│       └── index.astro          # Página única que une todos los componentes
├── astro.config.mjs
└── package.json
```

## Imágenes necesarias

Las imágenes no se incluyen en el código y deben estar en la carpeta `public/` con estos nombres. Si usas otros, cambia la ruta en el componente correspondiente.

| Componente  | Archivos                                                                                                       |
| ----------- | -------------------------------------------------------------------------------------------------------------- |
| Cabecera    | `casa.png`, `github.png`, `linkedin.png`                                                                       |
| Carrusel    | `sobre-mi.jpg`, `habilidades.jpg`, `formacion.jpg`, `experiencia.jpg`                                          |
| Sobre mí    | `muneco.png`                                                                                                   |
| Habilidades | `java.png`, `html.png`, `css.png`, `mysql.png`, `spring.png`, `javascript.png`, `angular.png`, `ingles.png`    |
| Formación   | `logo-daw.png`, `logo-bachillerato.png`, `logo-fundacion.png`                                                  |
| Experiencia | `soltel.png`, `google.png`, `amazon.png`, `microsoft.png`                                                      |
| Contacto    | `logo-alvaro.png`, `facebook.png`, `instagram.png`, `tiktok.png`, `github-circulo.png`, `linkedin-circulo.png` |

## Personalización

- **Textos y datos:** se editan directamente en cada componente. Los apartados de Habilidades, Formación y Experiencia están escritos a mano, sin props, así que basta con cambiar su HTML.
- **Alineación:** el menú y todas las secciones comparten `max-width: 1100px` y el mismo margen lateral de `5rem`. Si cambias uno, cambia el otro para que sigan alineados.
- **Altura del menú:** `scroll-margin-top` y `min-height` de las secciones dependen de la altura del menú (56 px). Si la cambias, actualiza ese valor en todos los componentes.
- **Efecto LED:** se ajusta en `Carrusel.astro`. Para quitar el latido, elimina la propiedad `animation` de `.tarjeta`.
- **Colores:** fondo `#141414`, tarjetas `#1f1f1f`, rojo del menú `rgba(163, 10, 16)` y rojo de la franja final `#8b0000`.
- **Datos de contacto:** el correo, el teléfono y los enlaces de Facebook, Instagram y TikTok de `Contacto.astro` son provisionales. Sustitúyelos por los reales.

## Inspiraciones de diseño

| Parte             | Inspiración                   |
| ----------------- | ----------------------------- |
| Paleta de colores | Netflix                       |
| Cabecera          | Apple                         |
| Carrusel          | Apple (página del iPhone Duo) |
| Sobre mí          | Duolingo                      |
| Habilidades       | Sevilla FC                    |
| Formación         | Spotify                       |
| Experiencia       | Disney+                       |
| Contacto y footer | Tarrago                       |

## Despliegue

Tras `npm run build`, la carpeta `dist/` contiene la web estática y se puede publicar en servicios como GitHub Pages, Netlify o Vercel. Las rutas de las imágenes empiezan por `/` (por ejemplo `/logo.png`), sin `/public`, que es lo que necesita el sitio publicado.

## Autor

**Álvaro Díaz Pérez**.
