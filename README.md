# TechDesign Solutions - Portal Web Rediseñado

Este repositorio contiene el desarrollo de una interfaz web básica (landing page) para TechDesign Solutions, una empresa especializada en el desarrollo de plataformas de comercio electrónico. El objetivo de este proyecto es implementar una interfaz modular y escalable, aplicando metodologías modernas de desarrollo web y utilizando Bootstrap 5.3.7 para una experiencia responsiva y eficiente.

## 🚀 Tecnologías Utilizadas

* **HTML5:** Estructura semántica del contenido.
* **Sass (SCSS):** Preprocesador CSS para estilos modulares y mantenibles.
* **Bootstrap 5.3.7 (vía npm):** Framework CSS para componentes reutilizables y sistema de grilla responsivo.
* **BEM (Bloque, Elemento, Modificador):** Metodología de nomenclatura CSS para una estructura de clases clara y escalable.
* **Git:** Control de versiones del proyecto.

## ✨ Características Principales

* **Landing Page de una Sola Página (`index.html`):** Contiene todas las secciones clave del portal.
* **Diseño Responsivo:** Adaptabilidad a diferentes tamaños de pantalla (móviles, tablets, desktops) gracias a Bootstrap Grid.
* **Estilos Modulares con Sass:** Organización del código CSS en archivos parciales para facilitar la gestión y escalabilidad.
* **Adopción de Metodología BEM:** Nombres de clases consistentes y claros para una mejor legibilidad y mantenimiento del CSS.
* **Personalización de Bootstrap:** Sobrescritura de las variables por defecto de Bootstrap (colores, tipografía, espaciado, etc.) para alinear el framework con la identidad visual de TechDesign Solutions.
* **Footer "Sticky":** Implementación de un footer que se mantiene siempre en la parte inferior de la ventana, incluso con contenido corto.

## 📁 Estructura del Proyecto

La estructura del proyecto sigue las mejores prácticas para un desarrollo front-end organizado, especialmente en lo que respecta a Sass:
```
├── assets/
│   ├── css/
│   │   └── style.css          # Archivo CSS compilado por Sass
│   ├── img/                   # Imágenes del proyecto (placeholders iniciales)
│   ├── js/
│   │   └── main.js            # Archivo JavaScript principal
│   └── scss/                  # Archivos fuente de Sass
│       ├── abstracts/
│       │   └── _config.scss   # Variables globales (colores, fuentes, espaciados, etc.)
│       ├── base/
│       │   ├── _global-styles.scss # Estilos globales del body, sticky footer
│       │   ├── _reset.scss         # Reseteo de estilos CSS (box-sizing: border-box)
│       │   └── _typography.scss    # Estilos base para tipografía
│       ├── components/
│       │   ├── _button.scss        # Estilos para botones personalizados
│       │   ├── _service-card.scss  # Estilos para tarjetas de servicio
│       │   └── _contact-form.scss  # Estilos para el formulario de contacto
│       ├── layout/
│       │   ├── _about.scss         # Estilos para la sección "Nosotros"
│       │   ├── _clients.scss       # Estilos para la sección "Clientes"
│       │   ├── _contact.scss       # Estilos para la sección "Contacto" (layout)
│       │   ├── _footer.scss        # Estilos para el footer principal
│       │   ├── _header.scss        # Estilos para el header y la navegación
│       │   ├── _hero.scss          # Estilos para la sección hero
│       │   ├── _reason.scss        # Estilos para la sección "Por qué elegirnos"
│       │   └── _services-section.scss # Estilos para la sección "Servicios"
│       └── _custom.scss           # Punto de entrada de Sass: importa Bootstrap y todos los parciales
├── node_modules/              # Módulos de Node.js (incluyendo Bootstrap)
├── index.html                 # Página principal del portal
├── package.json               # Archivo de configuración de npm
├── package-lock.json          # Bloqueo de dependencias de npm
└── README.md                  # Este archivo
```
## ⚙️ Configuración y Uso Local

Para configurar y ejecutar este proyecto localmente, sigue estos pasos:

1.  **Clona el repositorio:**
    ```bash
    git clone <URL_DEL_REPOSITORIO>
    cd techdesign-solutions
    ```
    (Nota: `<URL_DEL_REPOSITORIO>` será la URL de tu repo en GitHub una vez que lo subas).

2.  **Instala las dependencias:**
    Asegúrate de tener Node.js y npm instalados. Luego, instala las dependencias del proyecto (principalmente Bootstrap y Sass):
    ```bash
    npm install
    ```

3.  **Compila Sass (Modo "Watch"):**
    Para que los cambios en tus archivos Sass se compilen automáticamente a CSS, ejecuta el siguiente comando en la raíz de tu proyecto:
    ```bash
    sass --watch assets/scss/custom.scss:assets/css/style.css
    ```

4.  **Abre el Proyecto:**
    Abre el archivo `index.html` en tu navegador web preferido para ver la interfaz.

## 🤝 Contribución

Las contribuciones son bienvenidas. Si tienes sugerencias o encuentras problemas, por favor, abre un "issue" o envía un "pull request".

## 📄 Licencia

Este proyecto está bajo la licencia [MIT](https://opensource.org/licenses/MIT).
*(O la licencia que decidas usar)*

---