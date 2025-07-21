# TechDesign Solutions - Landing Page

Este repositorio contiene el desarrollo de una landing page moderna y responsiva para **TechDesign Solutions**, una empresa especializada en el desarrollo de plataformas de comercio electrónico y soluciones digitales personalizadas.

El objetivo principal de este proyecto es demostrar la implementación de las mejores prácticas en desarrollo front-end, incluyendo la modularidad CSS con Sass, la metodología BEM, el uso avanzado de un framework CSS (Bootstrap 5.3.7), y una estructura de proyecto organizada y mantenible.

## 🚀 Características y Tecnologías Destacadas

Este proyecto ha sido construido aplicando las siguientes tecnologías y principios:

* **HTML5 Semántico:** Estructura clara y accesible del contenido.
* **Sass (SCSS):** Utilizado como preprocesador CSS principal para modularizar, organizar y optimizar los estilos.
    * **Variables Globales:** Colores, tipografía, espaciado y sombras definidos centralmente en `_config.scss` para una personalización y coherencia total.
    * **Archivos Parciales:** Estilos divididos en categorías lógicas (`abstracts`, `base`, `components`, `layout`) para facilitar la gestión y escalabilidad del CSS.
    * **Metodología BEM (Bloque, Elemento, Modificador):** Aplicada rigurosamente para una nomenclatura de clases explícita y un CSS altamente mantenible y reutilizable.

* **Bootstrap 5.3.7:** Implementado vía npm para:
    * **Sistema de Grid Responsivo (Mobile First):**Diseño adaptativo (`row` y `col-xx-xx`) concebido bajo la filosofía `Mobile First`. Esto asegura que la página sea completamente funcional y estéticamente agradable en dispositivos móviles desde el inicio, y luego se adapta fluidamente a tablets y desktops.
    * **Componentes Reutilizables:** Uso de componentes como Navbar, Botones, Formularios.
    * **Personalización Avanzada de Colores:** Se sobrescriben las variables por defecto de Bootstrap (ej. `$primary`, `$info`, `$dark`) con los valores de la paleta de colores definida en `_config.scss`. Esta estrategia permite:
        * Utilizar las clases de utilidad de Bootstrap (ej., `text-info`, `bg-dark`, `btn-primary`) directamente en el HTML, y estas automáticamente aplicarán los colores personalizados de la marca.
        * Mantener la paleta de colores centralizada y fácil de modificar.
        * Reducir la necesidad de escribir CSS personalizado en nuestros parciales para cada instancia de color o fondo, reservando los parciales para el diseño estructural y de componentes complejos.

* **Diseño Responsivo Integral:** La página se adapta fluidamente a diferentes tamaños de pantalla, asegurando una experiencia visual consistente y funcional en cualquier dispositivo (ej. footer de 3 columnas en desktop).
* **Footer "Sticky":** Implementación de un footer que se adhiere a la parte inferior de la ventana, independientemente de la longitud del contenido de la página, utilizando Flexbox.
* **Git:** Control de versiones del proyecto.

## ✨ Secciones de la Landing Page

La landing page incluye las siguientes secciones principales:

* **Navbar Fijo:** Navegación superior responsiva con menú hamburguesa en dispositivos móviles y logo de la marca.
* **Sección Hero:** Un banner de bienvenida con imagen de fondo, overlay oscuro para mejorar la legibilidad del texto principal y un llamado a la acción.
* **Sección Servicios:** Presenta los servicios de la empresa mediante tarjetas estilizadas, organizadas en un grid responsivo con efectos hover.
* **Galería de Clientes:** Muestra los logos de clientes en un formato circular y responsivo, con un diseño de grid que se adapta a múltiples columnas según el tamaño de la pantalla.
* **Sección Contacto:** Incluye un formulario de contacto con campos estilizados, listo para la interacción del usuario.
* **Footer:** Un pie de página de tres columnas en escritorio (información de contacto, descripción, redes sociales y copyright), que se apila de forma ordenada en dispositivos más pequeños, con centrado vertical del párrafo de descripción.

## 📁 Estructura del Proyecto

La estructura del proyecto sigue las mejores prácticas de desarrollo front-end y la metodología 7-1 de Sass para una organización lógica y modular:
```

├── assets/
│   ├── css/
│   │   └── style.css          # Archivo CSS compilado final (no se edita directamente)
│   ├── img/                   # Imágenes y recursos gráficos del proyecto
│   ├── js/
│   │   └── main.js            # Archivo JavaScript (para futuras interacciones)
│   └── scss/                  # Archivos fuente de Sass (código fuente CSS)
│       ├── abstracts/         # Variables globales, mixins, funciones
│       │   └── _config.scss   #   -> Variables de diseño (colores, fuentes, espaciados, etc.)
│       ├── base/              # Estilos base para elementos HTML
│       │   ├── _global-styles.scss #   -> Estilos generales del body y el "Sticky Footer"
│       │   ├── _reset.scss         #   -> Reseteo de estilos CSS (incluye box-sizing: border-box;)
│       │   └── _typography.scss    #   -> Estilos base para tipografía (fuentes, tamaños de Hx, párrafos)
│       ├── components/        # Estilos para componentes reutilizables
│       │   ├── _button.scss        #   -> Estilos para botones personalizados
│       │   ├── _service-card.scss  #   -> Estilos para las tarjetas de servicio
│       │   └── _contact-form.scss  #   -> Estilos para el formulario de contacto
│       ├── layout/            # Estilos para el diseño y estructura de secciones específicas
│       │   ├── _clients.scss       #   -> Estilos para la sección de clientes
│       │   ├── _contact.scss       #   -> Estilos para la sección de contacto (wrapper del formulario)
│       │   ├── _footer.scss        #   -> Estilos para el pie de página
│       │   ├── _header.scss        #   -> Estilos para el encabezado y el navbar
│       │   └── _hero.scss          #   -> Estilos para la sección hero
│       └── _custom.scss           # Punto de entrada de Sass: Importa Bootstrap y todos los parciales del proyecto.
├── node_modules/              # Módulos de Node.js (incluyendo Bootstrap SCSS y JS)
├── index.html                 # Página principal (la landing page)
├── package.json               # Archivo de configuración de npm (dependencias del proyecto)
├── package-lock.json          # Bloqueo de dependencias de npm
└── README.md                  # Este archivo
```
## ⚙️ Configuración y Uso Local

Para configurar y ejecutar este proyecto en tu entorno local, sigue estos pasos:

1.  **Clonar el Repositorio:**
    Abre tu terminal o línea de comandos y ejecuta:
    ```bash
    git clone [text](https://github.com/Ardana98/TechDesign.git)
    cd techdesign-solutions
    ```

2.  **Instalar Dependencias:**
    Asegúrate de tener [Node.js](https://nodejs.org/) y [npm](https://www.npmjs.com/) instalados en tu sistema. Luego, instala las dependencias del proyecto (principalmente Bootstrap y Sass):
    ```bash
    npm install
    ```

3.  **Compilar Sass (Modo "Watch"):**
    Para que los cambios que realices en tus archivos `.scss` se compilen automáticamente a `assets/css/style.css` cada vez que guardes, ejecuta el siguiente comando en la raíz de tu proyecto:
    ```bash
    sass --watch assets/scss/custom.scss:assets/css/style.css
    ```
    Mantén esta terminal abierta mientras trabajas en tus estilos.

4.  **Abrir el Proyecto en el Navegador:**
    Una vez que Sass esté compilando, simplemente abre el archivo `index.html` en tu navegador web preferido para visualizar la landing page.

## 🤝 Contribución

Las contribuciones, sugerencias y reportes de errores son bienvenidos. Por favor, siéntete libre de abrir un "issue" o enviar un "pull request" si deseas colaborar.