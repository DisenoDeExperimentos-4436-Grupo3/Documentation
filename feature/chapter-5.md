## Capítulo V: Product Implementation, Validation & Deploymentt

### 5.1. Software Configuration Management.

La Gestión de Configuración de Software (SCM, por sus siglas en inglés) es una disciplina en el desarrollo de software encargada de identificar, controlar y rastrear los componentes del software a lo largo de su ciclo de vida. Esta metodología facilita la administración organizada de cambios en documentos, códigos y otros elementos durante el proceso de desarrollo, garantizando así una gestión eficiente y ordenada. Su objetivo principal es mejorar la eficiencia del equipo de desarrollo y minimizar los errores. (Martin, 2023)

### 5.1.1. Software Development Environment Configuration.

**Directrices de Desarrollo para Horizon**

En esta sección, presentaremos las convenciones y prácticas recomendadas que hemos adoptado en HTML, CSS y JavaScript para el desarrollo de Horizon, nuestro software innovador dirigido a startups del sector del desarrollo de software. Estas directrices están orientadas a asegurar una estructura coherente, facilitar la mantenibilidad del código y optimizar la funcionalidad de nuestra plataforma para la gestión de proyectos e iniciativas. A continuación, detallaremos cómo aplicamos estas prácticas en cada una de las tecnologías utilizadas.

**Definición de Requisitos**

Antes de iniciar el desarrollo, es crucial definir claramente los requisitos de Horizon. Estos requisitos incluyen las funcionalidades clave que deseamos proporcionar, tales como:

- **Automatización de Tareas:** Implementación de herramientas que optimicen y automaticen tareas repetitivas para mejorar la eficiencia.
- **Gestión de Información Robusta:** Uso de bases de datos para una administración efectiva de la información del proyecto.
- **Características Personalizables:** Opciones adaptables a las necesidades específicas de cada startup.
- **Colaboración Eficiente:** Funcionalidades que faciliten la colaboración efectiva entre equipos, incluyendo soporte para metodologías ágiles.

**Elección de la Tecnología**

Con base en los requisitos, hemos seleccionado las siguientes tecnologías para Horizon:

- **Frontend:** Angular para una interfaz de usuario dinámica y receptiva, que permita una interacción fluida con las herramientas de gestión y análisis.

- **Configuración del Entorno de Desarrollo** ItelliJ IDEA

  - **Editor de Código**: IntelliJ IDEA.
  - **Propósito**: Desarrollo de software y edición de código.
  - **Ruta de descarga**: https://www.jetbrains.com/idea/download/

- **Editor de Código:** Visual Studio Code

  - **Propósito:** Desarrollo y edición de código con soporte extensivo para JavaScript y herramientas de desarrollo.
  - **Ruta de descarga:** https://code.visualstudio.com/

- **Control de Versiones:** Git, con repositorios en GitHub.
  - **Propósito:** Gestión de versiones y colaboración en el código.
  - **Ruta de descarga:** https://git-scm.com/
  - **Repositorio:** https://github.com/Firtness/Horizon.git

**Product UX/UI Design**

- **UI/UX:** Crear una interfaz amigable y accesible para los usuarios.
  - **Herramienta:** Figma
  - **Propósito:** Diseño de prototipos y interfaces de usuario.
  - **Ruta del Figma**: https://www.figma.com/design/PQMlg7QzupwYT1ef3eXdEG/LandingPage-WireFrame-ManageWise?node-id=15-131&node-type=canvas&t=PXmYxR9lGN4kX4l0-0

![FIGMA](../assets/images/FIGMA2.png)

**Software Development**
**HTML:**

- **Descripción:** El lenguaje base de etiquetado para aplicaciones web sera empleado en este proyecto.
- **Enlace:** https://www.w3schools.com/html/default.asp
  **CSS:**
- **Descripción:** Cascade Styles Sheet maneja el diseño visual de la landing page.
- **Enlace:** https://www.w3schools.com/css/default.asp

Con Horizon, buscamos no solo ofrecer herramientas de gestión de proyectos eficientes, sino también actuar como un socio estratégico para las startups, facilitando su crecimiento y éxito en el competitivo mercado tecnológico.

### 5.1.2. Source Code Management.

**Gestión de Cambios en el Código Fuente con GitHub**

En esta sección, nuestro equipo detalla los métodos y la estructura organizativa para gestionar los cambios en el código fuente utilizando GitHub como plataforma de control de versiones. Hemos configurado un repositorio remoto en GitHub para almacenar el código fuente y facilitar la colaboración entre los miembros del equipo. Los URLs de los repositorios son los siguientes:

- **Landing Page**: https://github.com/Horizon-ManageWise/LandingPage.git
- **Frontend Web Applications**: https://github.com/Horizon-ManageWise/Frontend-Web-Applications.git
- **Backend Web Applications**: https://github.com/Horizon-ManageWise/Backend-Web-Applications.git

**Estructura del Repositorio**

Hemos organizado el repositorio en ramas específicas para diferentes etapas del desarrollo, garantizando un flujo de trabajo ordenado y eficiente. La estructura de ramas es la siguiente:

- **Main branch (rama principal):** Contiene la versión estable y lista para producción del software.
- **Develop branch:** Contiene el código en desarrollo que se integrará en la rama principal después de ser probado y validado.

Además, para el desarrollo de nuevas funcionalidades, creamos ramas específicas siguiendo las convenciones de nomenclatura:

- **Feature branches:** Ramas dedicadas al desarrollo de nuevas características. La nomenclatura para estas ramas es `feature/nueva-funcionalidad`.

Implementamos GitFlow, un modelo de ramificación diseñado por Vincent Driessen, que incluye las siguientes ramas:

- **Main branch:** Rama principal que alberga el código estable y preparado para producción.
- **Develop branch:** Rama de desarrollo donde se integran nuevas funcionalidades y correcciones antes de ser fusionadas a la rama principal.
- **Feature branches:** Creadas a partir de `develop` para añadir nuevas características, siguiendo la nomenclatura `feature/nueva-funcionalidad`.
- **Release branches:** Preparadas para la liberación de nuevas versiones, permitiendo pruebas finales y corrección de errores antes del despliegue a producción.
- **Hotfix branches:** Utilizadas para corregir errores críticos en producción, siguiendo la nomenclatura `hotfix/correccion-critica`.

**Mensajes de Commits**

Adoptamos el estándar Conventional Commits para los mensajes de nuestros commits, lo que facilita la comprensión del historial de cambios y la automatización de versiones. Ejemplos de mensajes son:

- **feat:** Añadir nueva funcionalidad, por ejemplo, `feat: implementar sistema de notificaciones`.
- **fix:** Corregir errores, por ejemplo, `fix: solucionar problema con la validación de datos`.
- **docs:** Actualizar documentación, por ejemplo, `docs: actualizar guía de instalación`.
- **style:** Aplicar formato, por ejemplo, `style: ajustar estilo de código según las pautas`.
- **refactor:** Mejorar el código sin cambiar su funcionalidad, por ejemplo, `refactor: optimizar el rendimiento del módulo de usuario`.
- **test:** Añadir o modificar pruebas, por ejemplo, `test: añadir pruebas para la funcionalidad de autenticación`.

**Documentación**

La documentación del proyecto se encuentra en el archivo `README.md` dentro del repositorio. Este archivo proporciona detalles sobre la configuración, el uso del software y las guías para contribuir al proyecto.

### 5.1.3. Source Code Style Guide & Conventions.

En el _Source Code Style Guide_, presentaremos las convenciones, estilos, diseños y principios aplicados en los lenguajes utilizados durante el desarrollo de nuestro producto. Los lenguajes y herramientas empleados incluyen:

**LENGUAJES UTILIZADOS**

- **_HTML_** : Estructura del contenido en la web, utilizando etiquetas semánticas para mejorar la accesibilidad.
- **_CSS_**: Estilos y diseño visual del software, garantizando una experiencia de usuario óptima.
- **_JavaScript_**: Lógica y funcionalidad interactiva, permitiendo la automatización y personalización del software.
- **_TypeScript_**: Superset de JavaScript que añade tipado estático y otras características para mejorar la mantenibilidad y la detección de errores en tiempo de compilación.

**HTML**

- **Nombres Descriptivos:** Utiliza nombres de clases e IDs que sean descriptivos y significativos, facilitando la comprensión del propósito de cada elemento. Por ejemplo, en lugar de `box`, usa `project-card`.

- **Indentación:** Indenta correctamente el código HTML para mejorar la legibilidad y mantener una estructura clara.

- **Etiquetas Semánticas:** Emplea etiquetas semánticas apropiadas, como `<header>`, `<nav>`, `<main>`, y `<footer>`, para mejorar la accesibilidad y el SEO del sitio.
- **Comentarios:** Usa comentarios para explicar secciones complejas o partes importantes del código HTML, facilitando la comprensión para otros desarrolladores.

**CSS**

- **Nombres Descriptivos:** Utiliza nombres de clases y selectores que sean descriptivos y coherentes para facilitar la identificación y el mantenimiento de los estilos. Por ejemplo, usa `btn-submit` en lugar de `btn`.
- **Agrupación y Comentarios:** Agrupa propiedades relacionadas y separa secciones de CSS con comentarios claros, como /_ Estilos de botones _/. Esto organiza el código y facilita su navegación.
- **Preferencia por Clases:** Prefiere el uso de clases en lugar de IDs para estilos reutilizables y más flexibles.
- **Compatibilidad y Prefijos:** Utiliza prefijos de vendedor y asegúrate de que el código sea compatible con diferentes navegadores cuando sea necesario.
- **Medidas Relativas:** Usa medidas relativas como `em`, `rem`, y `%` en lugar de medidas absolutas para mejorar la flexibilidad y la accesibilidad del diseño.

**JavaScript**

- **Nombres Descriptivos:** Usa nombres de variables y funciones que sean descriptivos y significativos para que el código sea autoexplicativo, `fetchProjectData` en lugar de `getData`..
- **Comentarios:** Incluye comentarios para explicar la lógica compleja o el propósito de las funciones. Esto facilita la comprensión y el mantenimiento del código.
- **Espacios y Sangrías:** Utiliza espacios en blanco y sangrías para mejorar la legibilidad del código. Sigue un estilo consistente en todo el código.
- **Modularidad:** Evita la creación de funciones globales. Utiliza módulos o patrones de diseño para modularizar el código y evitar conflictos de nombres.
- **Convención de Nombres:** Emplea `camelCase` para nombrar variables y funciones, siguiendo una convención consistente.

**TypeScript**

- **Tipado Estático:** Utiliza el tipado estático de TypeScript para definir los tipos de variables, parámetros de funciones y retornos. Esto ayuda a detectar errores de manera anticipada. Por ejemplo, en lugar de `let age = "25"`, define el tipo correctamente: `let age: number = 25`.

- **Interfaces y Tipos Personalizados:** Define interfaces y tipos personalizados para describir la forma de los objetos y otros datos complejos. Esto mejora la claridad del código y facilita su mantenimiento. Ejemplo:

  ```typescript
  interface Project {
    id: number;
    name: string;
    description: string;
  }
  ```

- **Decoradores y Clases:** Emplea clases y decoradores para aprovechar las características orientadas a objetos de TypeScript, facilitando la organización del código, especialmente en Angular. Ejemplo de clase:

  ```typescript
  class User {
    constructor(public name: string, public age: number) {}
  }
  ```

- **Manejo de Errores en Tiempo de Compilación:** TypeScript permite identificar errores en tiempo de compilación, lo que reduce problemas en tiempo de ejecución. Aprovecha este control para escribir código más seguro.

- **Convención de Nombres:** Sigue las mismas convenciones de JavaScript, utilizando `camelCase` para variables y funciones, pero aplicando también la convención `PascalCase` para clases e interfaces.

- **Convenciones y Nomenclaturas:** Es necesario definir las convenciones y nomenclaturas que se utilizarán en el proyecto. Esto incluye el uso de `camelCase` para variables y funciones, `PascalCase` para clases e interfaces, y nombres de métodos descriptivos para mejorar la legibilidad del código.

**Comentarios**

- **Propósito y Complejidad:** Utiliza comentarios para explicar el propósito de bloques de código, funciones o partes complejas del código. Asegúrate de que añadan valor y contexto.
- **Actualización de Comentarios:** Mantén los comentarios actualizados a medida que el código evoluciona para evitar información desactualizada.
- **Evita Comentarios Redundantes:** Evita comentarios obvios o redundantes que no añaden información útil. Los comentarios deben proporcionar claridad y contexto adicional.

**Convenciones y Nomenclaturas**

- **Referencias de Nomenclatura:** Para la nomenclatura de elementos, adoptaremos convenciones inspiradas en **BEM (Block Element Modifier)** y **OOCSS (Object-Oriented CSS)**, promoviendo claridad y reutilización.

- **Estructura de Nombres:** Los nombres de las clases deben ser compuestos por tres partes: bloque, elemento y modificador. Por ejemplo, un botón de envío puede llamarse `btn--primary`, donde `btn` es el bloque y `primary` es el modificador.

### 5.1.4. Software Deployment Configuration.

En los siguientes pasos se explicará cómo llevar a cabo la implementación de nuestro sitio web utilizando GitHub Pages

**Deploy con GitHub Pages:**
En primer lugar, accedemos al repositorio de GitHub donde se encuentra nuestro proyecto y luego navegamos hacia la configuración del repositorio.

![Settings](../assets/images/settings.png)

Dentro del menú de ajustes, elegimos la opción "Pages".
![Settings](../assets/images/image.png)

**Control de Versiones**

- **Uso de Git:** Mantén un historial completo de cambios y facilita el manejo de diferentes versiones del código.

En la sección de GitHub Pages, escogemos la rama principal (main) en el menú desplegable de la sección "Branch" y guardamos la configuración presionando el botón "Save".
Después de unos momentos, recibiremos el enlace a nuestro sitio web publicado en GitHub Pages.

### 5.2 Landing Page, Services & Applications Implementation.

El desarrollo, testeo y despliegue de nuestra landing page es importante para que nuestros clientes puedan acceder a la información sobre nuestra empresa y producto a través de una interfaz con diseño responsivo, navegación intuitiva y solo con información relevante. Esta primera etapa nos permite crear un diseño conceptual sobre la estética que nuestra aplicación completa y lista para su uso. Estas etapas nos ayudaran a dar una primera impresión a los clientes para validar ideas e identificar problemas que se deben solucionar.

### 5.2.1 . Sprint 1

El primer sprint es una etapa importante en nuestro marco de gestión de proyectos de metodología ágil Scrum. En este periodo, agendamos reuniones con el objetivo de conocer mejor las características de cada integrante, y delegamos tareas para materializar el diseño y funcionalidades ya establecidas, para transformarlos en un landing page funcional y que cumple las heurísticas.

#### 5.2.1.1 Sprint Planning 1.

El sprint planning es una reunion antes de cada sprint en la metodologia Scrum donde el equipo elige las user stories que va a transformar en un producto tangible. Tambien define que como se van a separar los trabajos y quien sera responsable. Nuestro objetivo sera construir un plan resolubre en un tiempo determinado que sera lo que dure el sprint, para crearlo fomentaremos la colaboracion para que todos sepan y entiendas los objetivos y prioridades.

| Sprint #| Sprint 1|
| -- | -- |
| **Sprint Planning Background**||
| **Date**| 06/09/2024|
| **Time**| 12:00 AM|
| **Location**| Discord (Reunión virtual)|
| **Prepared By**| Jaque Peña, Estefano Oscar|
| **Attendees (to planning meeting)** | Acuña Tomás, Diego Rolin, Alejo Cárdenas, José Antonio, Arevalo Meza, John Telesforo, Sandoval Paiva, Valentino, Jaque Peña, Estefano Oscar|
| **Sprint Goal & User Stories**||
| **Sprint 1 Goal**| Nuestro enfoque está en finalizar el informe y desplegar nuestra Landing Page desde el repositorio de GitHub. Creemos que esto entrega una experiencia de usuario optimizada a nuestros clientes. Esto se confirmará cuando todas las tareas se muevan a la columna "Terminado" en Trello. |
| **Sprint 1 Velocity**| ------ |
| **Sum of Story Points**| 19 |

#### 5.2.1.2 Sprint Backlog 1.

Para el primer sprint backlog, recopilamos historias de usuario relacionadas con la página de inicio (landing page) . Para organizar y administrar estas historias de usuario, las dividimos en tareas fáciles de realizar y las asignamos a los miembros del equipo de manera efectiva, utilizamos la herramienta Trello. Nos concentramos en completar las historias de usuario durante este sprint, con el objetivo principal de crear una landing page completa con un diseño atractivo y fácil de usar. Gracias a Trello, pudimos colaborar efectivamente y seguir el progreso de las tareas, lo que nos permitió abordar y resolver
![alt text](../assets/TB1-image/Trelloo1.png)

| sprint #| Sprint 1|||||||
| -- | -- | -- | -- | -- | -- | -- | -- |
| User<br>Story || Work-Item /Task ||||||
| ID| Title| ID| Title| Description| Estimation<br>(Hours) | Assigned<br>To| Status<br>(To-do <br>/InProcess<br>/ To-Review <br>/Done) |
| Sprint #| Sprint 1|||||||
| -- | -- | -- | -- | -- | -- | -- | -- |
| User<br>Story || Work-Item / Task ||||||
| ID | Title | ID | Title | Description | Estimation<br>(Hours) | Assigned<br>To | Status<br>(To-do <br>/InProcess<br>/ To-Review <br>/Done) |
| US01 | Vista General de Beneficios y Funcionalidades | TA001 | Implementación de Sección de Beneficios | Crear y diseñar la sección de la página principal que destaque los beneficios clave de la plataforma. | 1 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA002 | Ajuste de diseño en CSS | Mejorar la presentación visual de la sección con estilos personalizados y diseño responsivo. | 2 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA003 | Optimización de JavaScript para interactividad | Añadir efectos básicos como hover o transiciones animadas a los elementos. | 1 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA004 | Prueba de compatibilidad con navegadores | Verificar que la sección de beneficios funcione correctamente en navegadores modernos. | 1 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA005 | Subir los archivos al repositorio | Cargar HTML, CSS, y JS relacionados con la sección de beneficios al repositorio y realizar pruebas. | 2 hora | Arevalo Meza, John Telesforo | Done |
| US02 | Enlaces Directos a Redes Sociales | TA006 | Implementación de Enlaces a Redes Sociales | Agregar enlaces visuales y funcionales a las redes sociales en la página principal. | 1 hora | Sandoval Paiva, Valentino | Done |
|  |  | TA007 | Diseño de iconos personalizados | Crear o adaptar iconos visuales para cada red social con estilos en CSS. | 2 hora | Sandoval Paiva, Valentino | Done |
|  |  | TA008 | Validación de enlaces y funcionalidad | Comprobar que los enlaces redirigen correctamente a las páginas correspondientes. | 1 hora | Sandoval Paiva, Valentino | Done |
|  |  | TA009 | Implementación de efectos de hover | Añadir animaciones o cambios de color cuando los usuarios pasen el ratón sobre los iconos. | 2 hora | Sandoval Paiva, Valentino | Done |
|  |  | TA010 | Subir cambios al repositorio | Actualizar los archivos HTML, CSS, y JS relacionados con esta tarea en el repositorio. | 2 hora | Sandoval Paiva, Valentino | Done |
| US03 | Registro Rápido y Simple | TA011 | Diseño e Implementación del Registro de Usuario | Crear el formulario de registro optimizado para facilitar la creación de nuevas cuentas de usuario. | 1 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA012 | Diseño de estilos personalizados para el formulario | Añadir clases y estilos en CSS para destacar campos y botones del formulario. | 2 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA013 | Validación básica en JavaScript | Implementar validación de campos obligatorios, como nombre y correo electrónico. | 1 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA014 | Pruebas de funcionalidad del formulario | Probar el formulario con diferentes casos de uso para verificar que funcione correctamente. | 2 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA015 | Subir los archivos al repositorio | Cargar el formulario junto con sus estilos y scripts al repositorio. | 1 hora | Jaque Peña, Estefano Oscar | Done |
| US04 | Iniciar Sesión Rápido y Visible | TA016 | Implementación de Enlace de Inicio de Sesión | Agregar un enlace visible para iniciar sesión en la esquina superior de la página. | 1 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA017 | Mejora de estilos del enlace de inicio de sesión | Personalizar el enlace para que sea visible y accesible desde dispositivos móviles. | 1 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA018 | Agregar animación al hacer clic | Implementar una animación al hacer clic en el enlace de inicio de sesión. | 1 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA019 | Pruebas en diferentes dispositivos | Verificar la visibilidad y funcionalidad del enlace en móviles y pantallas grandes. | 1 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA020 | Subir los cambios al repositorio | Subir el HTML, CSS, y JS relacionados con el enlace de inicio de sesión. | 1 hora | Jaque Peña, Estefano Oscar | Done |
| US05 | Resumen de la Empresa, Misión y Visión | TA021 | Creación de Sección "Acerca de Nosotros" | Desarrollar la sección "Acerca de Nosotros" con la misión, visión y valores de la empresa. | 2 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA022 | Ajuste de diseño en CSS para textos y layout | Mejorar el diseño de la sección con tipografías, colores y espaciado adecuado. | 1 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA023 | Añadir imagen representativa | Incluir una imagen o ícono que refuerce la misión y visión de la empresa. | 1 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA024 | Pruebas de diseño responsivo | Verificar que la sección se ajuste bien a diferentes tamaños de pantalla. | 1 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA025 | Subir los archivos al repositorio | Cargar HTML, CSS, y JS de esta sección al repositorio y realizar pruebas. | 1 hora | Arevalo Meza, John Telesforo | Done |
| US06 | Navegación Clara y Directa en la Página | TA026 | Diseño del Menú de Navegación | Implementar un menú de navegación intuitivo que permita a los usuarios moverse fácilmente por las secciones de la página. | 1 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA027 | Diseño de estilos personalizados para el menú | Usar CSS para resaltar la sección activa y mejorar la visibilidad del menú. | 1 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA028 | Implementación de funcionalidad de scroll | Añadir JavaScript para desplazarse suavemente entre secciones al hacer clic en los enlaces. | 1 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA029 | Pruebas de accesibilidad | Comprobar que el menú sea navegable con teclado y compatible con lectores de pantalla. | 1 hora | Jaque Peña, Estefano Oscar | Done |
|  |  | TA030 | Subir cambios al repositorio | Subir el menú junto con los estilos y scripts al repositorio. | 1 hora | Jaque Peña, Estefano Oscar | Done |
| US07 | Acceder a Preguntas Frecuentes | TA031 | Implementación de Sección de Preguntas Frecuentes | Crear y diseñar la sección de preguntas frecuentes en la página principal para ayudar a los usuarios a resolver sus dudas. | 1 hora | Sergio André Gómez Vallejos | Done |
|  |  | TA032 | Diseño de estilos personalizados para FAQ | Personalizar el diseño para que las preguntas y respuestas sean fáciles de leer. | 1 hora | Sergio André Gómez Vallejos | Done |
|  |  | TA033 | Añadir funcionalidad de colapsar/expandir | Usar JavaScript para que las respuestas se muestren o escondan al hacer clic en una pregunta. | 1 hora | Sergio André Gómez Vallejos | Done |
|  |  | TA034 | Probar funcionalidad de FAQ | Asegurar que todas las preguntas se desplieguen correctamente en diferentes navegadores. | 1 hora | Sergio André Gómez Vallejos | Done |
|  |  | TA035 | Subir cambios al repositorio | Subir los archivos de HTML, CSS, y JS relacionados con las FAQ al repositorio. | 1 hora | Sergio André Gómez Vallejos | Done |
| US08 | Contactar vía correo | TA036 | Implementación de Sección de Contacto | Crear y diseñar la sección "Contáctanos" para que los usuarios puedan contactar rápidamente en caso de problemas. | 1 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA037 | Crear diseño de formulario de contacto | Añadir campos básicos como nombre, correo electrónico, y mensaje con diseño en CSS. | 1 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA038 | Añadir validación básica en JavaScript | Implementar validaciones para asegurar que los campos requeridos estén completos antes de enviar el formulario. | 1 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA039 | Pruebas de funcionalidad del formulario | Verificar que el formulario sea funcional y se envíe correctamente. | 1 hora | Arevalo Meza, John Telesforo | Done |
|  |  | TA040 | Subir los cambios al repositorio | Subir la sección al repositorio y probar la integración con el resto de la página. | 1 hora | Arevalo Meza, John Telesforo | Done |

Link Trello: https://trello.com/invite/b/66ddd34a3a8f75b32fbdaa52/ATTI22d7710f322c2ce38799efbb188aa9556839E153/si729-2402-ws53-grupo-4-horizon-managewise 

#### 5.2.1.3 Development Evidence for Sprint Review

| Repository   | Branch | Commit Id                                | Commit Message                                                              | Commit Message Body                                                                                      | Committed on (Date)     |
| ------------ | ------ | ---------------------------------------- | --------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ----------------------- |
| Landing-page | main   | 1b462d3                                  | Initial commit                                                              | Created the README file.                                                                                 | 08/09/2024              |
| Landing-page | main   | 3cd1ffc                                  | Feat: added navbar and header                                               | Feat: added navbar and header                                                                            | 08/09/2024              |
| Landing-page | main   | 2fb452a                                  | feat: added descripcion general and beneficios sections                     | feat: added descripcion general and beneficios sections                                                  | 08/09/2024              |
| Landing-page | main   | 7fe0bdd                                  | Feat: Add nosotros                                                          | Feat: Add nosotros                                                                                       | 08/09/2024              |
| Landing-page | main   | 47d2070                                  | Feat: Add nosotros                                                          | Feat: Add nosotros                                                                                       | 08/09/2024              |
| Landing-page | main   | 280c80e                                  | nojotros add                                                                | nojotros add                                                                                             | 08/09/2024              |
| Landing-page | main   | ec30e3f                                  | AÑADIENDO MI PARTE                                                          | AÑADIENDO MI PARTE                                                                                       | 09/09/2024              |
| Landing-page | main   | 5d497e7                                  | AÑADI MI PARTE                                                              | AÑADI MI PARTE                                                                                           | 09/09/2024              |
| Landing-page | main   | c4a4795db0aa611aa25fc3f3dea4d0d9f5574ed1 | feat: Add files and update                                                  | Se añade archivos al repositorio                                                                         | 10/09/2024              |
| Landing-page | main   | 1dd9e3e004dc828fd9134f631738121951dd1cba | feat: Add funcionalidades                                                   | Se añade funcionalidades al .js                                                                          | 10/09/2024              |
| Landing-page | main   | a6dde725b27df498b1d2a3e182e6ec2ac55541d4 | feat: Agregación de estilos para un sección                                 | Se implementa estilos al landing page                                                                    | 10/09/2024              |
| Landing-page | main   | 220f08f437e7a7d9904371c4a59b488f39b8455c | feat: Añadir Preguntas frecuentes, actualización de imagenes y contactanos  | Se añade una seccion de preguntas y respuestas, la actualización de imagenes y la sección de contactanos | 10/09/2024              |



#### 5.2.1.4 Testing Suite Evidence for Sprint Review.

| Repository                                                            | Branch             | Commit Id                                | Commit Message           | Commit Message Body                         | Committed on (Date)     |
| --------------------------------------------------------------------- | ------------------ | ---------------------------------------- | ------------------------ | ------------------------------------------- | ----------------------- |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Estefano  | 4823259                                  | Initial commit           | Created the README file.                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Estefano  | a58791b                                  | feat: added US43 gherkin | feat: added US43 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Valentino  | 29d0d8e                                  | feat: added US44 gherkin | feat: added US44 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Valentino  | 9c68a0f                                  | feat: added US45 gherkin | feat: added US45 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Jhon  | 92ff505                                  | feat: added US46 gherkin | feat: added US46 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Jhon  | 6d40835                                  | feat: added US47 gherkin | feat: added US47 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Diego  | ab19556                                  | feat: added US48 gherkin | feat: added US48 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing/tree/feature/tb1-Sergio | feature/tb1-Sergio | 0813c9549f96710be687e9a3c1f1d8913b3d3c57 | feat: added US07 gherkin | Se añade la sección de Preguntas Frecuentes | 16/09/2024              |
| https://github.com/Horizon-ManageWise/Testing/tree/feature/tb1-Sergio | feature/tb1-Sergio | 451cf0957cd87a511014c1b35adc4b82a80ef9f4 | feat: added US08 gherkin | Se añade la sección de Contactanos          | 16/09/2024              |

#### 5.2.1.5 Execution Evidence for Sprint Review.

En este Sprint, los miembros del equipo de desarrollo de software de Horizon han completado y desplegado la Landing Page. A continuación, mostramos imágenes que demuestran cómo nuestra página presenta de manera clara e intuitiva la información sobre nuestro producto y nuestra empresa.

<p align="center">
  <img src="../assets/images/Execution-Evidence-for-Sprint-Review-1.png">
  <br>
  Vista general de la Landing Page, destacando el diseño limpio y moderno que permite a los usuarios navegar fácilmente por la información.
</p>

<p align="center">
  <img src="../assets/images/Execution-Evidence-for-Sprint-Review-2.png">
  <br>
  Sección de beneficios clave del producto, mostrando cómo se presentan de manera atractiva y accesible para atraer a los usuarios.
</p>

<p align="center">
  <img src="../assets/images/Execution-Evidence-for-Sprint-Review-3.png">
  <br>
  Sección de preguntas frecuentes, organizada por categorías, donde los usuarios pueden encontrar respuestas rápidas a sus dudas sobre el uso de la plataforma y área de contacto, mostrando el formulario que permite a los usuarios enviar mensajes directamente al equipo de soporte, facilitando la comunicación.
</p>

<p align="center">
  <img src="../assets/images/Execution-Evidence-for-Sprint-Review-4.png">
  <br>
  Diseño del formulario de iniciar sesión, que garantiza de forma sencilla acceder a la aplicación web.
</p>

<p align="center">
  <img src="../assets/images/Execution-Evidence-for-Sprint-Review-5.png">
  <br>
  Diseño del formulario de registro, que enfatiza la simplicidad y la facilidad de uso, asegurando que los nuevos usuarios puedan registrarse sin complicaciones.
</p>

#### 5.2.1.7 Software Deployment Evidence for Sprint Review.

**Resumen**
Durante este Sprint, nos hemos enfocado en el despliegue de la landing page. Las actividades realizadas incluyen la configuración del entorno de desarrollo y el despliegue inicial del sitio. A continuación, se detalla el proceso seguido para el despliegue de la landing page.

**Actividades Realizadas**

- Creación de Cuentas y Configuración de Recursos:

Proveedor de Hosting: Selección y configuración de la cuenta en el proveedor de hosting para desplegar la landing page.
Configuración del Entorno: Establecimiento del entorno de desarrollo y producción para la landing page.

- Configuración de Proyectos para Integración:

Repositorio de Código: Configuración del repositorio en GitHub para la integración continua y despliegue automático.
Automatización: Configuración de scripts y herramientas para la automatización del despliegue.

- Despliegue de la Landing Page:

Subida de Archivos: Transferencia de archivos y recursos al servidor de hosting.
Verificación: Comprobación de que la landing page se despliega correctamente y está accesible en la web.

**Deploy del Landing Page**
![deploy](../assets/images/deploy_tb1.png)
**Capturas de Pantalla**

- Repositorio de Landing Page:
  ![alt text](../assets/images/foto_repositorio.jpg)

**Enlace al Repositorio**: https://github.com/Rampart-SaboresCercanos/Landing-page

#### 5.2.1.8 Team Collaboration Insights during Sprint.

En esta sección, se presenta un análisis detallado de la colaboración del equipo durante el Sprint. Durante este sprint, las actividades de implementación se organizaron siguiendo una metodología ágil, garantizando una colaboración fluida entre los miembros del equipo. Se exponen capturas de los analíticos de colaboración y de los commits realizados en GitHub, lo que permite visualizar la contribución individual de cada miembro del equipo.

- Diseño y Desarrollo:
  Diseño de la Landing Page: Desarrollo y diseño completo de la landing page, incluyendo la creación de secciones y funcionalidad.
  Implementación: Realización de las tareas de codificación, pruebas y ajustes necesarios para completar la página.
- Documentación y Despliegue:
  Documentación: Creación de documentación relevante para la landing page, incluyendo capturas de pantalla y descripciones.
  Despliegue: Configuración del entorno de despliegue y transferencia de archivos al servidor.

**Landing Page**

![Commits](../assets/TB1-new/landingc1.jpeg)
![Commits](../assets/TB1-new/landingc2.jpeg)

- Estefano Oscar Jaque Peña: 2
- Diego Rolin Acuña Tomas: 1
- John Telesforo Arevalo Meza: 10
- Valentino Sandoval Paiva: 1
- Sergio André Gómez Vallejos: 8

**Report:**

![alt text](../assets/TB1-new/commitsall2.jpeg)

![alt text](../assets/TB1-new/commitall1.jpeg)

![alt text](../assets/TB1-image/commitsreport3.jpeg)

![Commits](../assets/TB1-image/commitsreport3.jpeg)

- Estefano Oscar Jaque Peña: 55
- Diego Rolin Acuña Tomas: 52
- John Telesforo Arevalo Meza: 40
- Valentino Sandoval Paiva: 59
- Sergio André Gómez Vallejos: 13


### 5.2.2 Sprint 2

Durante el Sprint 2, nuestro enfoque principal fue el desarrollo de la primera aplicación web del proyecto Horizon utilizando Angular, además de mejorar la landing page previamente desarrollada. Este sprint fue fundamental para implementar las primeras funcionalidades de la aplicación, asegurando también la inclusión de la funcionalidad de internacionalización (i18n).

#### 5.2.2.1 Sprint Planning 2.

En este Sprint 2, durante la reunión de planificación, el equipo seleccionará las historias de usuario que se convertirán en resultados concretos. Además, se definirá cómo se distribuirán las tareas y quién se encargará de cada una. Nuestro objetivo será construir un plan viable que se pueda completar dentro del tiempo establecido para este sprint. Para ello, fomentaremos la colaboración, asegurándonos de que todos conozcan y comprendan tanto los objetivos como las prioridades del trabajo.


| Sprint #                            | Sprint 2                                                                                                                                                                                                                                                                                   |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Sprint Planning Background**      |                                                                                                                                                                                                                                                                                            |
| **Date**                            | 10/10/2024                                                                                                                                                                                                                                                                                 |
| **Time**                            | 12:00 AM                                                                                                                                                                                                                                                                                   |
| **Location**                        | Discord (Reunión virtual)                                                                                                                                                                                                                                                                  |
| **Prepared By**                     | Jaque Peña, Estefano Oscar                                                                                                                                                                                                                                                                 |
| **Attendees (to planning meeting)** | Alejo Cárdenas, José Antonio, Arevalo Meza, John Telesforo, Sandoval Paiva, Valentino, Jaque Peña, Estefano Oscar, Sergio Gómez                                                                                                                                                |
| **Sprint Goal & User Stories**      |                                                                                                                                                                                                                                                                                            |
| **Sprint 2 Goal**                   | Nuestro enfoque está en finalizar el informe y desplegar nuestra Aplicación Web desde firebase. Creemos que esto entrega una experiencia de usuario optimizada a nuestros clientes. Esto se confirmará cuando todas las tareas se muevan a la columna "Terminado" en Trello. |
| **Sprint 2 Velocity**               | 19 |
| **Sum of Story Points**             | 63 |

#### 5.2.2.2 Sprint Backlog 2.

Para el segundo sprint backlog, recopilamos historias de usuario relacionadas a la aplicación web. Para organizar y administrar estas historias de usuario, las dividimos en tareas fáciles de realizar y las asignamos a los miembros del equipo de manera efectiva, utilizamos la herramienta Trello. Nos concentramos en completar las historias de usuario durante este sprint, con el objetivo principal de crear una aplicación web mas concreta y completa con un diseño atractivo y fácil de usar. Gracias a Trello, pudimos colaborar efectivamente y seguir el progreso de las tareas, lo que nos permitió abordar y resolver.
![alt text](../assets/TB1-image/Trelloo1.png)

| Sprint #  | Sprint 2|||||||
|--|--|--|--|--|--|--|--|
| User<br>Story || Work-Item / Task ||||||
| ID        | Title| ID| Title| Description| Estimation<br>(Hours) | Assigned<br>To| Status<br>(To-do <br>/InProcess<br>/ To-Review <br>/Done) |
| US09      | Creación de user stories| TA001| Implementación en frontend| Crear funcionalidad para agregar user stories en el frontend| 6 horas| Arevalo Meza, John Telesforo| Done|
||| TA002| Integración con el repositorio| Subir cambios al repositorio en GitHub para la funcionalidad de creación de user stories| 4 horas| Arevalo Meza, John Telesforo   | Done|
||| TA003| Crear component en angular| Crear component en angular| 1 hora| Arevalo Meza, John Telesforo   | Done|
||| TA004| Verificar la correcta creacion mediante un mensaje en consola 1h|Verificar la correcta creacion mediante un mensaje en consola | 1 hora| Arevalo Meza, John Telesforo   | Done|
| US10| Modificación de user stories| TA005| Implementación en frontend | Crear funcionalidad para modificar user stories en el frontend| 6 horas| Arevalo Meza, John Telesforo| Done|
||| TA006| Integración con el repositorio | Integración con el repositorio| 1 horas| Arevalo Meza, John Telesforo| Done|
||| TA007| Crear component en angular | Crear component en angular| 1 hora| Arevalo Meza, John Telesforo| Done|
||| TA008| Verificar correcta modificacion mediante mensaje en consola |Verificar correcta modificacion mediante mensaje en consola | 1 hora| Arevalo Meza, John Telesforo| Done|
| US11| Eliminación de user stories| TA009| Implementación en frontend| Crear funcionalidad para eliminar user stories en el frontend| 5 horas| Arevalo Meza, John Telesforo | Done|
||| TA010| Integración con el repositorio| Subir cambios al repositorio en GitHub para la funcionalidad de eliminación de user stories| 6 horas| Arevalo Meza, John Telesforo| Done|
||| TA011| Crear component en angular | Crear component en angular | 1 hora| Arevalo Meza, John Telesforo| Done|
||| TA012| Verificar correcta eliminación mediante mensaje en consola | Verificar correcta eliminación mediante mensaje en consola | 1 hora| Arevalo Meza, John Telesforo| Done|
| US12| Creación de user epics| TA013| Implementación en frontend| Crear funcionalidad para agregar epics en el frontend| 5 horas| Arevalo Meza, John Telesforo| Done|
||| TA014| Integración con el repositorio| Subir cambios al repositorio en GitHub para la funcionalidad de creación de epics| 5 horas| Arevalo Meza, John Telesforo   | Done|
||| TA015| Crear component en angular |Crear component en angular | 1 hora| Arevalo Meza, John Telesforo   | Done|
||| TA016| Verificar correcta creacion mediante mensaje en consola | Verificar correcta creacion mediante mensaje en consola | 1 hora| Arevalo Meza, John Telesforo   | Done|
|US13| Modificación de user epics| TA017| Implementación en frontend| Crear funcionalidad para modificar epics en el frontend| 5 horas| Arevalo Meza, John Telesforo| Done|
||| TA018| Integración con el repositorio| Subir cambios al repositorio en GitHub para la funcionalidad de modificación de epics| 6 horas| Arevalo Meza, John Telesforo| Done|
||| TA019| Verificar correcta modificacion mediante mensaje en consola | Verificar correcta modificacion mediante mensaje en consola | 1 hora| Arevalo Meza, John Telesforo| Done|
||| TA020| Crear component en angular | Crear component en angular | 1 hora| Arevalo Meza, John Telesforo| Done|
| US14| Eliminación de user epics| TA021| Implementación en frontend| Crear funcionalidad para eliminar epics en el frontend| 5 horas| Arevalo Meza, John Telesforo| Done|
||| TA022| Integración con el repositorio| Subir cambios al repositorio en GitHub para la funcionalidad de eliminación de epics| 7 horas| Arevalo Meza, John Telesforo   | Done|
||| TA023| Verificar correcta eliminacion mediante mensaje en consola | Verificar correcta eliminacion mediante mensaje en consola | 1 hora| Arevalo Meza, John Telesforo   | Done|
||| TA024| Crear component | Crear component | 1 hora| Arevalo Meza, John Telesforo   | Done|
| US15| Creación de tasks| TA025| Implementación en frontend| Crear funcionalidad para agregar tasks en el frontend| 1 horas| Arevalo Meza, John Telesforo | Done|
||| TA026| Integración con el repositorio| Subir cambios al repositorio en GitHub para la funcionalidad de creación de tasks| 5 horas| Arevalo Meza, John Telesforo| Done|
||| TA027| Creacion de component | Creacion de component | 1 hora| Arevalo Meza, John Telesforo| Done|
||| TA028| Verificar correcta creacion mediante mensaje en consola | Verificar correcta creacion mediante mensaje en consola | 1 hora| Arevalo Meza, John Telesforo| Done|
|US35| Crear una nueva incidencia|TA0529| Implementación en frontend| Crear funcionalidad para crear nuevas incidencias en el frontend|6 horas|Jaque Peña, Estefano Oscar| Done|
||| TA031| Integración con el repositorio| Subir cambios al repositorio en GitHub para la funcionalidad de creación de incidencias|5 horas| Jaque Peña, Estefano Oscar| Done|
||| TA032| Creacion de component | Creacion de component |1 hora| Jaque Peña, Estefano Oscar| Done|
||| TA033| Verificar correcta creacion mediante mensaje en consola | Verificar correcta creacion mediante mensaje en consola |1 hora| Jaque Peña, Estefano Oscar| Done|
| US36|Visualizar las incidencias|TA034|Implementación en frontend|Crear funcionalidad para ver incidencias en el frontend|7 hora|Jaque Peña, Estefano Oscar| Done|
|||TA035|Integración con el repositorio| Subir cambios al repositorio en GitHub para la funcionalidad de visualización de incidencias| 5 hora| Jaque Peña, Estefano Oscar| Done|
|||TA036|Crear component en angular | Crear component en angular | 1 hora| Jaque Peña, Estefano Oscar| Done|
| US37| Editar una incidencia| TA037| Implementación en frontend| Crear funcionalidad para editar incidencias en el frontend| 8 hora| Jaque Peña, Estefano Oscar|Done|
||| TA038|Integración con el repositorio|Subir cambios al repositorio en GitHub para la funcionalidad de edición de incidencias| 5 hora| Jaque Peña, Estefano Oscar   | Done|
||| TA039|Crear component en angular |Crear component en angular | 1 hora| Jaque Peña, Estefano Oscar   | Done|
||| TA040|Verificar correcta modificacion mediante mensaje en consola |Verificar correcta modificacion mediante mensaje en consola | 1 hora| Jaque Peña, Estefano Oscar   | Done|
|US38|Eliminar una incidencia|TA041|Implementación en frontend| Crear funcionalidad para eliminar incidencias en el frontend| 7 hora| Jaque Peña, Estefano Oscar|Done|
|||TA042|Integración con el repositorio|Subir cambios al repositorio en GitHub para la funcionalidad de eliminación de incidencias| 5 hora| Jaque Peña, Estefano Oscar|Done|
|||TA043|Crear component en angular |Crear component en angular | 1 hora| Jaque Peña, Estefano Oscar|Done|
|||TA044|Verificar correcta eliminacion mediante mensaje en consola |Verificar correcta eliminacion mediante mensaje en consola | 1 hora| Jaque Peña, Estefano Oscar|Done|
|US27|Editar el acceso de miembros al proyecto|TA045|Implementación en frontend| Implementación en frontend| 3 hora| Sergio Gomez|Done|
|||TA046|Integración con el repositorio|Subir cambios al repositorio en GitHub para la funcionalidad| 1 hora| Sergio Gomez|Done|
|||TA047|Crear component en angular |Crear component en angular | 1 hora| Jaque Peña, Sergio Gomez|Done|
|||TA048|Verificar correcta eliminacion mediante mensaje en consola |Verificar correcta eliminacion mediante mensaje en consola | 1 hora| Sergio Gomez|Done|
|US28|Ver la información de usuario de los miembros|TA049|Implementación en frontend| Implementación en frontend| 3 hora| Sergio Gomez|Done|
|||TA050|Integración con el repositorio|Subir cambios al repositorio en GitHub para la funcionalidad| 1 hora| Sergio Gomez|Done|
|||TA051|Crear component en angular |Crear component en angular | 1 hora| Jaque Peña, Sergio Gomez|Done|
|US29|EdAsignar roles a los miembros del equipo|TA052|Implementación en frontend| Implementación en frontend| 3 hora| Sergio Gomez|Done|
|||TA053|Integración con el repositorio|Subir cambios al repositorio en GitHub para la funcionalidad| 1 hora| Sergio Gomez|Done|
|||TA054|Crear component en angular |Crear component en angular | 1 hora| Jaque Peña, Sergio Gomez|Done|
|US30|Conocer Información del Perfil de un Miembro|TA055|Implementación en frontend| Implementación en frontend| 3 hora| Sergio Gomez|Done|
|||TA056|Integración con el repositorio|Subir cambios al repositorio en GitHub para la funcionalidad| 1 hora| Sergio Gomez|Done|
|||TA057|Crear component en angular |Crear component en angular | 1 hora| Jaque Peña, Sergio Gomez|Done|
|US31|Ver Habilidades de Cada Miembro|TA058|Implementación en frontend| Implementación en frontend| 3 hora| Sergio Gomez|Done|
|||TA059|Integración con el repositorio|Subir cambios al repositorio en GitHub para la funcionalidad| 1 hora| Sergio Gomez|Done|
|||TA060|Crear component en angular |Crear component en angular | 1 hora| Jaque Peña, Sergio Gomez|Done|

Link Trello: https://trello.com/invite/b/66ddd34a3a8f75b32fbdaa52/ATTI22d7710f322c2ce38799efbb188aa9556839E153/si729-2402-ws53-grupo-4-horizon-managewise


#### 5.2.2.3 Development Evidence for Sprint Review.

| Repository   | Branch | Commit Id                                | Commit Message                                                              | Commit Message Body                                                                                      | Committed on (Date)     |
| ------------ | ------ | ---------------------------------------- | --------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ----------------------- |
| https://github.com/Horizon-ManageWise/Horizon/pull/60 |feature/Sprint2-sprintBacklog-services_Documentation_Evidence|75c0c75| Se realizo la agregacion de los videos y paginas| Created the README file.|25/09/2024|
| https://github.com/Horizon-ManageWise/Horizon/pull/59 | development | 6548432   | feat:Testing Suite Evidence for Sprint Review  | feat:Testing Suite Evidence for Sprint Review  | 25/09/2024|
| https://github.com/Horizon-ManageWise/Horizon/pull/58 |development|a19b6ac |feature:Sprint Backlog 2 update|Se realizo una actualizacion del product backlog | 25/09/2024|
| https://github.com/Horizon-ManageWise/Horizon/pull/57 | development | 29ca9f3 i   | feature/execution-evidence-from-sprint-review|feature/execution-evidence-from-sprint-review | 24/09/2024              |
| https://github.com/Horizon-ManageWise/Horizon/pull/56 | docs/landingpage-deployment-evidence | 7fe8f1f   | feature: added landing page deployment evidence | feature: added landing page deployment evidence | 24/09/2024              |
| https://github.com/Horizon-ManageWise/Horizon/pull/50 | fix/diagrama-clases | 6e41532 | feature: Add bounded context Reports images and Information | feature: Add bounded context Reports images and Information | 24/09/2024              |
| Frontend-Web-Application| tp1/Sergio-Gómez   | 4414741cd8540f7c729a524faf2f27e85e011fb2                | feat: add files   |Se añade los archivos al github | 27/09/2024  |
| Frontend-Web-Application| tp1/Sergio-Gómez   | f742ac5c292376710b9fe719260090f7e3d31efd         | feat: fix a error  | Se arregla un error  | 27/09/2024   |
| Frontend-Web-Application | tp1/Sergio-Gómez   | 341fced91af0e0632ad2bd4b5249e075c1e12faf          | fead: add section Timeline  | Se añade la sección Timeline con cada detaller y historias de usuario    | 27/09/2024   |
| Frontend-Web-Application | tp1/Sergio-Gómez   | 530b500fddfe8d2c252f76443404057d398b3737     | Feat:add section Statistic   | Se añade la sección de estadistica con un diagrama de barras por cada sprint | 27/09/2024  |

#### 5.2.2.4 Testing Suite Evidence for Sprint Review.


| Repository                                                            | Branch             | Commit Id                                | Commit Message           | Commit Message Body                         | Committed on (Date)     |
| --------------------------------------------------------------------- | ------------------ | ---------------------------------------- | ------------------------ | ------------------------------------------- | ----------------------- |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Estefano  | 4823259                                  | Initial commit           | Created the README file.                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Estefano  | a58791b                                  | feat: added US43 gherkin | feat: added US43 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Valentino  | 29d0d8e                                  | feat: added US44 gherkin | feat: added US44 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Valentino  | 9c68a0f                                  | feat: added US45 gherkin | feat: added US45 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Jhon  | 92ff505                                  | feat: added US46 gherkin | feat: added US46 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Jhon  | 6d40835                                  | feat: added US47 gherkin | feat: added US47 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Diego  | ab19556                                  | feat: added US48 gherkin | feat: added US48 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing/tree/feature/tb2-Sergio | feature/tb2-Sergio | 0813c9549f96710be687e9a3c1f1d8913b3d3c57 | feat: added US13 gherkin | Se añade el db Timeline | 27/10/2024              |
| https://github.com/Horizon-ManageWise/Testing/tree/feature/tb2-Sergio | feature/tb2-Sergio | 451cf0957cd87a511014c1b35adc4b82a80ef9f4 | feat: added US14 gherkin | Se añade el db Statistic | 27/10/2024              |

Link del repositorio del testing: https://github.com/Horizon-ManageWise/Testing

### 5.2.2.5. Execution Evidence for Sprint Review.
Durante este segundo sprint los integrantes del equipo desarrollaron los diferentes bounded context del dominio de ManageWise, con ayuda del framework Angular y los componentes de Angular Material.

* John Arevalo 
<br>

![alt text](../assets/images/bounded-context-task.jpg)

<br>

![alt text](../assets/images/create-task2.png)
<br>

Link Video: https://drive.google.com/drive/folders/1rvTZbtVs2qm98oGLgsAnPNa0LdZUxVGQ?usp=drive_link

* Jose Alejo 
<br>

![alt text](../assets/images/ManageWiseCalendar.png)

<br>

![alt text](../assets/images/ManageWiseCalendar2.png)
<br>

Link Video: https://drive.google.com/file/d/1v8EwJOrF5gchaASTJghXZPNo3dXT1mUW/view?usp=sharing

* Estefano Jaque - bounded context Reportes
<br>

![alt text](../assets/images/exevidencJaque.jpg)

Link Video: https://drive.google.com/file/d/11q8YnRJGMzfx-n6AbBIfxvugxmS4xuVw/view?usp=sharing

* Valentino Sandoval - bounded context Reportes
<br>

![alt text](../assets/images/TP_images/BDTools.jpeg)

Link Video: https://drive.google.com/file/d/1EGZlBOQEw8RfEzKQKlg4hFatObwWQRFM/view?usp=sharing 

- Diego Acuña - bounded context Members
  <br>

![alt text](../assets/images/BC-member/ManageWise-members-1.png)

Link Video: https://drive.google.com/file/d/13PZa8b2W9nk5ZUygtHGwDKG9wxmd99qW/view?usp=sharing

### 5.2.2.6. Services Documentation Evidence for Sprint Review. 
**Introducción:**
Durante este Sprint, se logró la documentación y despliegue de varios Endpoints correspondientes a los diferentes *bounded contexts* implementados por el equipo. Se utilizó OpenAPI para describir de forma estructurada los servicios Web desarrollados. A continuación, se presenta la relación de los Endpoints, las acciones soportadas y la respectiva documentación disponible.

Esta documentación incluye los verbos HTTP utilizados, sintaxis de llamadas, parámetros, ejemplos de respuesta, así como capturas de la interacción con los Web Services utilizando datos de muestra. También se proporciona el URL del repositorio de los Web Services y los *commit IDs* correspondientes al trabajo realizado en la documentación durante este Sprint.

### Tabla de Endpoints Documentados

| Bounded Context   | Endpoint                     | Acción    | Verbo HTTP | Parámetros               | Ejemplo de Respuesta | Documentación/URL     |
|-------------------|------------------------------|-----------|------------|--------------------------|----------------------|-----------------------|
| Herramientas      | `/api/tools`                  | Obtener lista de herramientas | GET | `?category={string}`     | `[{"id": 1, "name": "Tool A"}]` |Herramientas: https://managewise-7c633.web.app/tool/tools|
| Calendar          | `/api/calendar/events`        | Crear evento | POST       | `{"title": string, "date": string}` | `{"id": 1, "title": "Event A"}` | Calendar: https://managewisecalendar.web.app/calendar/activities |
| Reportes          | `/api/reports`                | Obtener reportes generados | GET  | `?type={string}`          | `[{"id": 1, "type": "weekly"}]` | Reportes: https://managewise-reports.web.app/reports |
| Tareas            | `/api/tasks/{id}`             | Eliminar tarea | DELETE   | `{id: int}`               | `{"message": "Task deleted"}` | Tareas:https://daos-2402-managewise-tasks.web.app/tasks |
| Miembros          | `/api/members`                | Listar miembros | GET    | `?role={string}`          | `[{"id": 1, "name": "Member A"}]` | Miembros:https://managewise-si729-team-manage.web.app/member/members |

### Ejemplos de Respuesta y Explicación

#### **GET** `/api/tools`
**Descripción**: Obtiene una lista de herramientas filtradas por categoría (opcional).

**Parámetros**:
- `category`: Filtro opcional para la categoría de la herramienta (string).

**Ejemplo de Llamada**:

GET /api/tools?category=software

**Ejemplo de Respuesta**:
db.json:<br>

 {<br>
      "id": 2,<br>
      "projectName": "Proyecto 2",<br>
      "transmitter": "Desarrollador",<br>
      "issuerName": "Carlos Ramírez",<br>
      "title": "Problemas con la base de datos",<br>
      "Summary": "El servidor de base de datos se ha caído durante varias horas.",<br>
      "detailedDescription": "El servidor de base de datos ha estado inactivo desde las 8:00 AM, afectando la disponibilidad de la plataforma.",<br>
      "dateTime": "24 de septiembre-11:15 AM",<br>
      "assignedTo": "Equipo de Infraestructura",<br>
      "priority": "Alta",<br>
      "suggestedActions": "Reiniciar el servidor y revisar la configuración de la base de datos."<br>
    },<br>

### Capturas de Pantalla

A continuación, se presentan algunas capturas de pantalla que muestran la interacción con los servicios Web, utilizando datos de muestra:

**Captura 1**: Visualización de la lista de reportes `/api/tools`.

![alt text](../assets/images/reportes_endpoint.png)

### Repositorio y Commits

- **Repositorio de Web Services**: 

- GitHub - Proyecto Web Services: https://github.com/Horizon-ManageWise/Horizon

- **Commits relacionados con la documentación**:
  - Managewise-Herramientas: https://github.com/SoyValzzz/Managewise-tools 
  - Managewise-Calendar https://github.com/Firtness/ManageWiseCalendar
  - Managewise-Reportes: (https://github.com/estefanojaque/Managewise-reportes)
  - Managewise-Tareas: https://github.com/JohnArvlo/my-json-server-tareas 
  
   Documentación de Tareas

### Resumen de Acciones del Equipo

| Integrante        | Acciones Realizadas                            |
|-------------------|------------------------------------------------|
| Valentino Sandoval | Diseño e implementación de bounded context herramientas |
| Jose Alejo        | Diseño e implementación de bounded context Calendar |
| Estefano Jaque    | Diseño e implementación de bounded context Reportes |
| John Arevalo      | Diseño e implementación de bounded context Tareas |
| Diego Acuña       | Diseño e implementación de bounded context Miembros |

Este Sprint se centró en mejorar la documentación de los Web Services desarrollados para cada uno de los bounded contexts, facilitando su integración y uso en futuras iteraciones.

### 5.2.2.7. Software Deployment Evidence for Sprint Review. 

Para la entrega del segundo sprint, se desplego la landing page, de manera completamente funcional y mejorada. Cumpliendo los user stories relacionados a la misma. De la misma forma se desplego la web application de manera parcial, pues faltan algunas secciones que se implementarán en el siguiente sprint.

Link landing page: https://horizon-managewise.github.io/LandingPage/

![alt text](../assets/images/Execution-Evidence-for-Sprint-Review-4.png)
![alt text](../assets/images/Execution-Evidence-for-Sprint-Review-5.png)
![alt text](../assets/images/Execution-Evidence-for-Sprint-Review-1.png)
![alt text](../assets/images/Execution-Evidence-for-Sprint-Review-2.png)
![alt text](../assets/images/Execution-Evidence-for-Sprint-Review-3.png)

<br>

#### Web Application:

* John Arevalo  

![alt text](../assets/images/bounded-context-task.jpg)

Link: https://daos-2402-managewise-tasks.web.app/tasks

* Estefano Oscar Jaque Peña  
**Internacionalización:**  
English:
![alt text](../assets/images/TP_images/ENReports.png)
Español:
![alt text](../assets/images/TP_images/ESReports.png)
**ADD Reports:**
![alt text](../assets/images/TP_images/ADDReports.png)
![alt text](../assets/images/TP_images/ADDReports2.png)

**EDIT Reports:**
![alt text](../assets/images/TP_images/EDITReports.png)

![alt text](../assets/images/TP_images/EDITReports2.png)

**DELETE Reports**  
Se eliminara el report que tiene todas las partes con PRUEBA EDIT

![alt text](../assets/images/TP_images/EDITReports2.png)

![alt text](../assets/images/TP_images/DELETEReports.png)

**Link:**  
https://managewise-reports.web.app

* Jose Alejo  

![alt text](../assets/images/ManageWiseCalendar.png)

![alt text](../assets/images/ManageWiseCalendar2.png)

Link: https://managewisecalendar.web.app/calendar/activities


* Valentino Sandoval
**ADD Tools:**
![alt text](../assets/images/TP_images/ADDTOOLS1.jpeg)
![alt text](../assets/images/TP_images/ADDTOOLS2.jpeg)



**EDIT Tools:**
![alt text](../assets/images/TP_images/EDIT.jpeg)


**DELETE Tools**  
Se eliminara el report que tiene todas las partes con PRUEBA EDIT

![alt text](../assets/images/TP_images/DELETE.jpeg)

Link: 

https://managewise-vsp.web.app


- Diego Acuña - bounded context Members
  <br>

![alt text](../assets/images/BC-member/ManageWise-members-1.png)

Link : https://managewise-si729-member.web.app/member/members

### 5.2.2.8. Team Collaboration Insights during Sprint.

|Integrante|Acciones realizadas durante el sprint|
|-|-|
| Valentino Sandoval|Diseño e implementacion de bounded context herramientas|
| Jose Alejo|Diseño e implementacion de bounded context Calendar|
| Estefano Jaque|Diseño e implementacion de bounded context Reportes|
| John Arevalo| Diseño e implementacion de bounded context Tareas|
| Diego Acuña|Diseño e implementacion de bounded context Miembros|

![alt text](../assets/images/Insigths.jpg)

### 5.2.3 Sprint 3

Durante el Sprint 3, nuestro enfoque principal fue el desarrollo del BackEnd de Horizon utilizando java, además de mejorar el FrontEnd. Este sprint fue fundamental para implementar las primeras funcionalidades del BackEnd.

#### 5.2.3.1 Sprint Planning 3.

En este Sprint 3, durante la reunión de planificación, el equipo seleccionará las historias de usuario que se convertirán en resultados concretos. Además, se definirá cómo se distribuirán las tareas y quién se encargará de cada una. Nuestro objetivo será construir un plan viable que se pueda completar dentro del tiempo establecido para este sprint. Para ello, fomentaremos la colaboración, asegurándonos de que todos conozcan y comprendan tanto los objetivos como las prioridades del trabajo.

| Sprint #| Sprint 3                                                                                                                                                                                                                                                                                   |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Sprint Planning Background**      |                                                                                                                                                                                                                                                                                            |
| **Date**| 27/10/2024 |                                                                                                                                                                                                                                                                                |
| **Time**                            | 12:00 AM                                                                                                                                                                                                                                                                                   |
| **Location**                        | Discord (Reunión virtual)                                                                                                                                                                                                                                                                  |
| **Prepared By**                     | Jaque Peña, Estefano Oscar                                                                                                                                                                                                                                                                 |
| **Attendees (to planning meeting)** |  José Antonio, Arevalo Meza, John Telesforo, Sandoval Paiva, Valentino, Jaque Peña, Estefano Oscar, Sergio Gómez                                                                                                                                                |
| **Sprint Goal & User Stories**      |                                                                                                                                                                                                                                                                                            |
| **Sprint 3 Goal**                   | Nuestro enfoque está en finalizar el BackEnd individual, cada uno con su Bounded Context lanzarlo localmente. Creemos que esto, nos ayudara a mejorar y a entender el BackEnd. Esto se confirmará cuando todas las tareas se muevan a la columna "Terminado" en Trello. |
| **Sprint 3 Velocity**               | 63 |
| **Sum of Story Points**             | 316 |

#### 5.2.3.2 Sprint Backlog 3.
Para el tercer sprint backlog, recopilamos historias de usuario relacionadas al Backend. Para organizar y administrar estas historias de usuario, las dividimos en tareas fáciles de realizar y las asignamos a los miembros del equipo de manera efectiva, utilizamos la herramienta Trello. Nos concentramos en completar las historias de usuario durante este sprint. Gracias a Trello, pudimos colaborar efectivamente y seguir el progreso de las tareas, lo que nos permitió abordar y resolver.
![alt text](../assets/TB1-image/Trelloo1.png)

| Sprint # | Sprint 3|||||||
|--|--|--|--|--|--|--|--|
| User Story || Work-Item / Task||||||
|ID |Title|ID|Title|Description|Estimation (Hours)|Assigned To|Status|
| TS001| Endpoint para visualizar Miembros del equipo    | TA001| implementar el endpoint "/api/members"  | implementar el endpoint "/api/members"  | 2 horas     | Sergio Gómez       | Done    |
||| TA002| realizar pruebas de respuesta del endpoint | realizar pruebas de respuesta del endpoint. | 2 horas| Sergio Gómez| Done|
||| TA003| creacion de queries | creacion de queries. | 1 hora| Sergio Gómez| Done|
||| TA004| definir e implementar query service y service impls  | definir e implementar query service y service impls. | 1 hora| Sergio Gómez| Done|
||| TA005| creacion de aggregates | creacion de aggregates. | 1 hora| Sergio Gómez| Done|
||| TA006| implementar controller | implementar controller. | 1 hora| Sergio Gómez| Done|
| TS002| Endpoint para eliminacion de miembro | TA007| implementar el endpoint "/api/members/member-id" | implementar el endpoint "/api/members/member-id"  | 3 horas| Sergio Gómez| Done|
||| TA008| realizar pruebas de respuesta del endpoint | realizar pruebas de respuesta del endpoint. | 1 hora| Sergio Gómez| Done|
||| TA009| creacion de queries y aggregates | creacion de queries y aggregates  | 2 hora| Sergio Gómez| Done|
||| TA010| definir e implementar query service y service impls | definir e implementar query service y service impls. | 1 hora| Sergio Gómez| Done|
||| TA011| implementar controller | implementar controller | 1 hora| Sergio Gómez| Done|
| TS003| Endpoint para gestión de videoconferencias | TA012| implementar el endpoint "/api/meeting" | implementar el endpoint "/api/meeting"  | 5 horas| Valentino Sandoval| Done|
||| TA013| realizar pruebas de respuesta endpoints | realizar pruebas de respuesta endpoints | 3 horas| Valentino Sandoval| Done|
||| TA014| Crear y definir los aggregates| Crear y definir los aggregates | 1 hora| Valentino Sandoval| Done|
||| TA015| Crear y definir resources y commands | Crear y definir resources y commands  | 2 horas| Valentino Sandoval| Done|
||| TA016| crear y definir queryservice | crear y definir queryservice  | 1 hora| Valentino Sandoval| Done|
||| TA017| crear y definir repositories | crear y definir repositories  | 1 hora| Valentino Sandoval| Done|
||| TA018| crear e implementar commandserviceimpls | crear e implementar commandserviceimpls | 1 hora| Valentino Sandoval| Done|
||| TA019| crear e implementar queryserviceimpls  | crear e implementar queryserviceimpls   | 1 hora| Valentino Sandoval| Done|
||| TA020| crear controller | crear controller  | 1 hora| Valentino Sandoval| Done|
| TS004| Endpoint para gestión de grabaciones de videoconferencias | TA021| Implementar el endpoint "/api/meetings/recordings" | Implementar el endpoint "/api/meetings/recordings" | 5 horas| Valentino Sandoval| Done|
||| TA022| Probar filtrado de grabaciones | Probar filtrado de grabaciones | 1 hora| Valentino Sandoval| Done|
||| TA023| Validar edición de enlaces de grabación | Validar edición de enlaces de grabación  | 1 hora| Valentino Sandoval| Done|
||| TA024| realizar pruebas de respuesta endpoints | realizar pruebas de respuesta endpoints  |3 horas| Valentino Sandoval| Done|
||| TA025| Crear y definir los aggregates | Crear y definir los aggregates  | 1 hora| Valentino Sandoval| Done|
||| TA026| Crear y definir resources y commands | Crear y definir resources y commands  | 2 horas| Valentino Sandoval| Done|
||| TA027| crear y definir queryservice | crear y definir queryservice | 1 hora| Valentino Sandoval| Done|
||| TA028| crear y definir repositories | crear y definir repositories | 1 hora| Valentino Sandoval| Done|
||| TA029| crear e implementar commandserviceimpls | crear e implementar commandserviceimpls | 1 hora| Valentino Sandoval| Done|
||| TA030| crear e implementar queryserviceimpls | crear e implementar queryserviceimpls  | 1 hora| Valentino Sandoval| Done|
||| TA031| crear controller | crear controller | 1 hora| Valentino Sandoval| Done|
| US26| Visualización de detalles de videoconferencias | TA032| Implementacion en frontend | Implementacion en frontend | 3 horas| Valentino Sandoval| Done|
||| TA033| Itegracion con el repositorio | Itegracion con el repositorio | 2 horas| Valentino Sandoval| Done|
||| TA034| Crear Componenten angular | Crear Componenten angular  | 1 hora| Valentino Sandoval| Done|
||| TA035| Verificar la correcta visualizacion de detalles | Verificar la correcta visualizacion de detalles  | 1 hora| Valentino Sandoval| Done|
| US25| Gestión de grabaciones de videoconferencias | TA036| Implementacion en frontend | Implementacion en frontend | 1 hora| Valentino Sandoval| Done|
||| TA037| Itegracion con el repositorio | Itegracion con el repositorio  | 1 hora| Valentino Sandoval| Done|
||| TA038| Crear Componenten angular | Crear Componenten angular  | 1 hora| Valentino Sandoval| Done|
||| TA039| Verificar lectura de datos | Verificar lectura de datos  | 1 hora| Valentino Sandoval| Done|
| TS005| Endpoint para creación de User Stories en el Backlog | TA040| Implementar el endpoint "/api/backlog/user-stories/" | Implementar el endpoint "/api/backlog/user-stories/"  | 3 horas| John Arevalo| Done|
||| TA041| realizar pruebas de respuesta endpoint | realizar pruebas de respuesta endpoint  |2 horas| John Arevalo| Done|
||| TA042| Crear y definir los aggregates | Crear y definir los aggregates  | 1 hora| John Arevalo| Done|
||| TA043| Crear y definir commands  | Crear y definir commands |1 horas| John Arevalo| Done|
||| TA044| crear y definir repositories | crear y definir repositories | 1 hora| John Arevalo| Done|
||| TA045| crear e implementar commandserviceimpls | crear e implementar commandserviceimpls | 1 hora| John Arevalo| Done|
||| TA046| crear controller | crear controller  | 1 hora| John Arevalo| Done|
||| TA047| Crear y definir resources | Crear y definir resources | 1 hora| John Arevalo| Done|
| TS006| Endpoint para modificación de User Stories | TA048| Implementar el endpoint "/api/backlog/user-stories/{id}" | Implementar el endpoint "/api/backlog/user-stories/{id}" | 3 horas| John Arevalo| Done|
||| TA049| Crear y definir los aggregates | Crear y definir los aggregates  | 1 hora| John Arevalo| Done|
||| TA050| Crear y definir commands y resources | Crear y definir commands y resources  |2 horas| John Arevalo| Done|
||| TA051| Implementacion de CommandService | Implementacion de CommandService  | 1 hora| John Arevalo| Done|
||| TA052| crear e implementar commandserviceimpls | crear e implementar commandserviceimpls  | 1 hora| John Arevalo| Done|
||| TA053| crear controller | crear controller  | 1 hora| John Arevalo| Done|
| TS007| Endpoint para creación de incidencias | TA054| Implementar el endpoint "/api/issues" | Implementar el endpoint "/api/issues"  |2 horas| Estefano Jaque| Done|
||| TA055| Probar creación de incidencias | Probar creación de incidencias | 1 hora| Estefano Jaque| Done|
||| TA056| Validar manejo de datos de incidencia faltantes | Validar manejo de datos de incidencia faltantes | 1 hora| Estefano Jaque| Done|
||| TA057| Crear y definir ValueObjects | Crear y definir ValueObjects  | 1 hora| Estefano Jaque| Done|
||| TA058| Crear y definir Aggregate | Crear y definir Aggregate. | 1 hora| Estefano Jaque| Done|
||| TA059| Crear Commands y Resources | Crear Commands y Resources | 1 hora| Estefano Jaque| Done|
||| TA060| Crear y definir CommandService | Crear y definir CommandService | 1 hora| Estefano Jaque| Done|
||| TA061| Crear y definir Repository | Crear y definir Repository  | 1 hora| Estefano Jaque| Done|
||| TA062| Crear e implementar CommandServiceImpls | Crear e implementar CommandServiceImpls  | 1 hora| Estefano Jaque| Done|
||| TA063| Implementacion en Controller | Implementacion en Controller  |2 horas| Estefano Jaque| Done|
| TS008| Endpoint para actualización de incidencias | TA064| Implementar el endpoint "/api/issues/{id}" | Implementar el endpoint "/api/issues/{id}" |2 horas| Estefano Jaque| Done|
||| TA065| Probar actualización de incidencias | Probar actualización de incidencias  | 1 hora| Estefano Jaque| Done|
||| TA066| Validar manejo de incidencias no encontradas | Validar manejo de incidencias no encontradas  | 1 hora| Estefano Jaque| Done|
||| TA067| Crear Command | Crear Command  | 1 hora| Estefano Jaque| Done|
||| TA068| Definir CommandService | Definir CommandService  | 1 hora| Estefano Jaque| Done|
||| TA069| Implementar CommandSeviceIpmls | Implementar CommandSeviceIpmls | 1 hora| Estefano Jaque| Done|
||| TA070| Implementar en Controller | Implementar en Controller  | 2 horas| Estefano Jaque| Done|
| US16| Modificación de tasks | TA071| Implementación en frontend | Implementación en frontend | 2 horas| John Arevalo| Done|
||| TA072| Integración con el repositorio | Integración con el repositorio | 1 hora| John Arevalo| Done|
||| TA073| Creacion de component en agular | Creacion de component en agular  | 2 horas| John Arevalo| Done|
||| TA074| Verificar que se modificara la task mediante confirmacion | Verificar que se modificara la task mediante confirmacion | 1 hora| John Arevalo| Done|
| US17| Eliminación de tasks | TA075| Implementación en frontend | Implementación en frontend  |2 horas| John Arevalo| Done|
||| TA076| Integración con el repositorio  Integración con el repositorio | 2 horas| John Arevalo| Done|
||| TA077| Creacion de component en agular | Creacion de component en agular  | 1 hora| John Arevalo| Done|
||| TA078| Actualizar el service | Actualizar el service  | 1 hora| John Arevalo| Done|
| US18| Vista centrada en backlog items | TA079| Implementación en frontend | Implementación en frontend  | 2 horas| John Arevalo| Done|
||| TA080| Integración con el repositorio | Integración con el repositorio  | 1 hora| John Arevalo| Done|
||| TA081| Creacion de component en agular | Creacion de component en agular  |2 horas| John Arevalo| Done|
||| TA082| validar que se muestren los datos de los items correctamente | validar que se muestren los datos de los items correctamente  | 1 hora| John Arevalo| Done|
||| TA083| agregar secciones para task , epic, user story | agregar secciones para task , epic, user story  | 1 hora| John Arevalo| Done|
| US19| Visualización del product backlog| TA084| Implementación en frontend | Implementación en frontend  | 2 horas| John Arevalo| Done|
||| TA085| Integración con el repositorio | Integración con el repositorio  | 1 hora| John Arevalo| Done|
||| TA086| Creacion de component en agular | Creacion de component en agular | 1 hora| John Arevalo| Done|
||| TA087| validar que se visualiza en seccion backlog | validar que se visualiza en seccion backlog  | 1 hora| John Arevalo| Done|
| US20| Asignación de backlog items a un sprint | TA088| Implementación en frontend | Implementación en frontend  | 2 horas| John Arevalo| Done|
||| TA089| Integración con el repositorio | Integración con el repositorio | 1 hora| John Arevalo| Done|
||| TA090| Creacion de component en agular | Creacion de component en agular | 1 hora| John Arevalo| Done|
||| TA091| Implementar logica para asignar spinrt id a user story | Implementar logica para asignar spinrt id a user story  | 1 hora| John Arevalo| Done|
||| TA092| verificar correcta asignacion a sprint | verificar correcta asignacion a sprint  | 1 hora| John Arevalo| Done|
| US21| Gestión de sprints | TA093| Implementación en frontend | Implementación en frontend |2 horas| John Arevalo| Done|
||| TA094| Integración con el repositorio | Integración con el repositorio  | 1 hora| John Arevalo| Done|
||| TA095| Creacion de component en agular | Creacion de component en agular | 1 hora| John Arevalo| Done|
||| TA096| Validar gestion | Validar gestion  | 1 hora| John Arevalo| Done|
| US22| Gestión de nuevas videoconferencias desde la sección de Reuniones | TA097| Implementación en frontend | Implementación en frontend  | 2 horas| Valentino Sandoval| Done|
||| TA098| Integración con el repositorio | Integración con el repositorio  | 1 hora| Valentino Sandoval| Done|
||| TA099| Creacion de component en agular | Creacion de component en agular  | 1 hora| Valentino Sandoval| Done|
||| TA100| Verificar correacta creacion | Verificar correacta creacion  | 1 hora| Valentino Sandoval| Done|
| US23| Edición de videoconferencias existentes | TA101| Implementación en frontend | Implementación en frontend  | 2 horas| Valentino Sandoval| Done|
||| TA102| Integración con el repositorio | Integración con el repositorio | 1 hora| Valentino Sandoval| Done|
||| TA103| Creacion e implementacion de component en agular | Creacion e implementacion de component en agular  | 1 hora| Valentino Sandoval| Done|
||| TA104| verificar que las videoconferencias se editen correctamente | verificar que las videoconferencias se editen correctamente  | 1 hora| Valentino Sandoval| Done|
| US24| Eliminación de videoconferencias | TA105| Implementación en frontend | Implementación en frontend  |2 horas| Valentino Sandoval| Done|
||| TA106| Integración con el repositorio | Integración con el repositorio  | 1 hora| Valentino Sandoval| Done|
||| TA107| Creacion e implementacion de component en agular | Creacion e implementacion de component en agular | 1 hora| Valentino Sandoval| Done|
||| TA108| verificar que la videoconferencia se elimine correctamente | verificar que la videoconferencia se elimine correctamente  | 1 hora| Valentino Sandoval| Done|
| US32| Visualización de User Stories en el Timeline | TA109| Implementación en frontend | Implementación en frontend | 2 horas| Sergio Gómez| Done|
||| TA110| Integración con el repositorio | Integración con el repositorio | 1 hora| Sergio Gomez| Done|
||| TA111| Creacion e implementacion de component en agular | Creacion e implementacion de component en agular  | 1 hora| Sergio Gomez| Done|
||| TA112| verificar que las user stories se muestren en la timeline | verificar que las user stories se muestren en la timeline | 1 hora| Sergio Gomez| Done|
| US33| Estimación de Esfuerzo en User Stories | TA113| Implementación en frontend | Implementación en frontend. | 2 horas| Sergio Gómez| Done|
||| TA114| Integración con el repositorio | Integración con el repositorio | 1 hora| Sergio Gomez| Done|
||| TA115| Creacion e implementacion de component en agular | Creacion e implementacion de component en agular | 1 hora| Sergio Gomez| Done|
||| TA116| Verificar que se visualice correctamente la estimación | Verificar que se visualice correctamente la estimación  | 1 hora| Sergio Gomez| Done|
| US34| Visualización de Estadísticas del Rendimiento del Equipo | TA117| Implementación en frontend | Implementación en frontend  | 2 horas| Sergio Gómez| Done|
||| TA118| Integración con el repositorio | Integración con el repositorio  | 1 hora| Sergio Gomez| Done|
||| TA119| Creacion e implementacion de component en agular | Creacion e implementacion de component en agular  | 1 hora| Sergio Gomez| Done|
||| TA120| Verificar que se visualicen las user stories completadas y no | Verificar que se visualicen las user stories completadas y no | 1 hora| Sergio Gomez| Done|
| US39| Ver reporte de una incidencia | TA121| Implementación en frontend | Implementación en frontend | 2 horas| Estefano Jaque| Done|
||| TA122| Integración con el repositorio | Integración con el repositorio  | 1 hora| Estefano Jaque| Done|
||| TA123| Creacion e implementacion de component en agular | Creacion e implementacion de component en agular | 1 hora| Estefano Jaque| Done|
||| TA124| Verificar que se acceda a informacion detallada del reporte | Verificar que se acceda a informacion detallada del reporte  | 1 hora| Estefano Jaque| Done|
| US40| Ver historial de una incidencia | TA125| Implementación en frontend | Implementación en frontend | 2 horas| Estefano Jaque| Done|
||| TA126| Integración con el repositorio | Integración con el repositorio  | 1 hora| Estefano Jaque| Done|
||| TA127| Creacion e implementacion de component en agular | Creacion e implementacion de component en agular  | 1 hora| Estefano Jaque| Done|
||| TA128| Verificar que todos los cambios se guarden en el historial | Verificar que todos los cambios se guarden en el historial | 1 hora| Estefano Jaque| Done|
| US41| Creación automática de los eventos creación y asignación del issue | TA129| Implementación en frontend | Implementación en frontend | 2 horas| Estefano Jaque| Done|
||| TA130| Integración con el repositorio | Integración con el repositorio | 1 hora| Estefano Jaque| Done|
||| TA131| Creacion e implementacion de component en agular | Creacion e implementacion de component en agular | 1 hora| Estefano Jaque| Done|
||| TA132| Validar creacion automatica | Validar creacion automatica  | 1 hora| Estefano Jaque| Done|
| US42| Filtrar incidencias por Sprint y Prioridad | TA133| Implementación en frontend | Implementación en frontend. | 2 horas| Estefano Jaque| Done|
||| TA134| Integración con el repositorio | Integración con el repositorio  | 1 hora| Estefano Jaque| Done|
||| TA135| Creacion e implementacion de component en agular | Creacion e implementacion de component en agular | 1 hora| Estefano Jaque| Done|
||| TA136| Validar filtrado | Validar filtrado  | 1 hora| Estefano Jaque| Done|


Link Trello: https://trello.com/invite/b/66ddd34a3a8f75b32fbdaa52/ATTI22d7710f322c2ce38799efbb188aa9556839E153/si729-2402-ws53-grupo-4-horizon-managewise 


#### 5.2.3.3 Development Evidence for Sprint Review.

Para el backend, optamos por genrar un .jar del proyecto, con ayuda del comando mvn clean package, para posteriormente subir este proyecto a un repositorio y conectarlo con microsoft azure mediate github.

String connector para ingresar a la base de datos de postgress
![Ejemplo de Imagen](../assets/TB2/backlog/backend/azure1.jpg)

Dominio del servicio, asi como el repositorio del mismo
![Ejemplo de Imagen](../assets/TB2/backlog/backend/azure2.png)

Repositorio con los comandos en workflows.yml
![Ejemplo de Imagen](../assets/TB2/backlog/backend/github.png)



| Repository   | Branch | Commit Id                                | Commit Message                                                              | Commit Message Body                                                                                      | Committed on (Date)     |
| ------------ | ------ | ---------------------------------------- | --------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ----------------------- |
| Backend-Web-Applications | dev   | 1b462d3                                  | feat: add dates of timeline  |Se añade los datos para el db timeline  | 27/09/2024  |
| Backend-Web-Applications | dev   | 3cd1ffc                                  | feat: add dates of statistic              | Se añade los datos para el db statistic  | 27/09/2024   |
| Backend-Web-Applications | dev   | 2fb452a                                  | feat: added descripcion general and beneficios sections                     | feat: added descripcion general and beneficios sections                                                  | 27/09/2024   |
| Backend-Web-Applications | dev   | 7fe0bdd                                  | Feat: Add nosotros                                                          | Feat: Add nosotros                                                                                       | 27/09/2024  |
| Backend-Web-Applications | dev   | 47d2070                                  | Feat: Add nosotros                                                          | Feat: Add nosotros                                                                                       |27/09/2024   |
| managewise-backend       | dev   | 922ad0f| feat: add members bd backend  |feat: add members bd backend   | 02/11/2024  |
|  managewise-backend | dev   | 3cd1ffc| feat: add meetingController| feat: add meetingController.| 02/11/2024   |
|  managewise-backend | dev   | f48083d| feat: Add issues bounded context| feat: Add issues bounded context| 02/11/2024|
|  managewise-backend | dev   | 00a082d| feat: added task list controller| feat: added task list controller| 02/11/2024  |
|  managewise-backend | dev   | 90d1dfa| feat: added backlog items entities and lists| feat: added backlog items entities and lists|01/11/2024   |

#### 5.2.3.4 Testing Suite Evidence for Sprint Review.


| Repository                                                            | Branch             | Commit Id                                | Commit Message           | Commit Message Body                         | Committed on (Date)     |
| --------------------------------------------------------------------- | ------------------ | ---------------------------------------- | ------------------------ | ------------------------------------------- | ----------------------- |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Estefano  | 4823259                                  | Initial commit           | Created the README file.                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Estefano  | a58791b                                  | feat: added US43 gherkin | feat: added US43 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Valentino  | 29d0d8e                                  | feat: added US44 gherkin | feat: added US44 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Valentino  | 9c68a0f                                  | feat: added US45 gherkin | feat: added US45 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Jhon  | 92ff505                                  | feat: added US46 gherkin | feat: added US46 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Jhon  | 6d40835                                  | feat: added US47 gherkin | feat: added US47 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing                         | feature/tb1-Diego  | ab19556                                  | feat: added US48 gherkin | feat: added US48 gherkin                    | 19/09/2024              |
| https://github.com/Horizon-ManageWise/Testing/tree/feature/tb2-Sergio | feature/tb2-Sergio | 0813c9549f96710be687e9a3c1f1d8913b3d3c57 | feat: added US13 gherkin | Se añade el db Timeline | 27/10/2024              |
| https://github.com/Horizon-ManageWise/Testing/tree/feature/tb2-Sergio | feature/tb2-Sergio | 451cf0957cd87a511014c1b35adc4b82a80ef9f4 | feat: added US14 gherkin | Se añade el db Statistic | 27/10/2024              |

Link del repositorio del testing: https://github.com/Horizon-ManageWise/Testing

#### 5.2.3.5 Execution Evidence for Sprint Review.

- Acontinuación se entrega el enlace a la landing page desplegada, actualizada y la última version: https://horizon-managewise.github.io/LandingPage/

![Ejemplo de Imagen](../assets/TB2/backlog/Landingpage/lan1.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/Landingpage/lan2.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/Landingpage/lan3.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/Landingpage/lan4.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/Landingpage/lan5.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/Landingpage/lan6.jpeg)

- **INICIO DE SESION**

![Ejemplo de Imagen](../assets/TB2/backlog/Landingpage/lan7.jpeg)

- **REGISTRO DE USUARIO**

![Ejemplo de Imagen](../assets/TB2/backlog/Landingpage/lan8.jpeg)

## FrontEnd

- **Bounded Context: Stadistics**

![Ejemplo de Imagen](../assets/TB2/backlog/front/es1.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/front/es2.jpeg)

- **Bounded Context: Backlog**

![Ejemplo de Imagen](../assets/TB2/backlog/front/es3.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/front/es4.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/front/es5.jpeg)


- **Bounded Context: Issues**

Alumno: Estefano Oscar Jaque Peña - U202225466

![Ejemplo de Imagen](../assets/TB2/backlog/front/es6.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/front/es7.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/front/es8.jpeg)

video explicativo: En el About the product 
https://drive.google.com/drive/folders/11fY4sH9mdNNPkHBJyJAXibVjLx6tnq7-?usp=sharing

Link repositorio Issues: https://github.com/estefanojaque/Managewise-FrontEnd-issues 

link deploy: https://managewise-reports-f0302.web.app/issues

- **Bounded Context: Meeting**

![Ejemplo de Imagen](../assets/TB2/backlog/front/es9.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/front/es10.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/front/es11.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/front/es12.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/front/es13.jpeg)

#### 5.2.3.6 Services Documentation Evidence for Sprint Review.

Link al repositorio de backend: https://github.com/Horizon-ManageWise/managewise-backend

<h3>Backlog Bounded Context</h3>

**MembersController**

|Tag| Http Verbs | Endpoint| Summary| Description| OperationId|
|-|-|-|-|-|-|
| Epics | GET| /api/v1/members| Get all members| Retrieve all embers| GetAllMembers|
| Epics | GET| /api/v1/members/{id}| Get members by members ID  | Get an epic by its id | GetMembersById |
| Epics | POST | /api/v1/members/| Create a new Member| Create a new Member| CreateMember|
| Epics | DELETE| /api/v1/members/{id}| Delete an Member| Remove an specific Member| DeleteMember|
| Epics | PUT| /api/v1/members/{id}| Update an Member| Update an specific Member| UpdateMember|

![Ejemplo de Imagen](../assets/TB2/backlog/members/swagger3.png)
![Ejemplo de Imagen](../assets/TB2/backlog/members/pgadmin.png)

**EpicsController**

|Tag| Http Verbs | Endpoint| Summary| Description| OperationId|
|-|-|-|-|-|-|
| Epics | GET| /api/v1/epics| Get all recordings| Retrieve all epics| GetAllEpics|
| Epics | GET| /api/v1/epics/{id}| Get epics by epic ID  | Get an epic by its id | GetEpicById |
| Epics | POST| /api/v1/epics| Create a new epic| Create a new epic| CreateEpic|
| Epics | DELETE| /api/v1/epics/{id}| Delete an epic| Remove an specific epic| DeleteEpic|

<br>

**SprintsController**

|Tag| Http Verbs | Endpoint| Summary| Description| OperationId|
|-|-|-|-|-|-|
| Sprints | GET| /api/v1/sprint| Get all sprints| Retrieve all sprints| GetAllSprints|
| Sprints | GET| /api/v1/sprint/{id}| Get sprint by sprint Id  | Get a sprint by its id | GetSprintById |
| Sprints | POST| /api/v1/sprint| Create a new sprint| Create a new sprint| CreateSprint|
| Sprints | DELETE| /api/v1/sprint/{id}| Delete an sprint| Remove an specific sprint| DeleteSprint|

<br>

**UserStoriesController**

| Tag| HTTP Verb | Endpoint| Summary| Description| OperationId|
|-|-|-|-|-|-|
| User Stories  | GET| /api/v1/user-stories| Get all user stories| Retrieve all user stories| GetAllUserStories|
| User Stories  | GET| /api/v1/user-stories/{id}| Get user story by ID| Get a user story by its ID| GetUserStoryById|
| User Stories  | POST| /api/v1/user-stories| Create a new user story| Create a new user story| CreateUserStory|
| User Stories  | PUT| /api/v1/user-stories/{id}| Update user story| Update an existing user story| UpdateUserStory|
| User Stories  | DELETE| /api/v1/user-stories/{id}| Delete user story| Remove a specific user story| DeleteUserStory|
| User Stories  | POST| /api/v1/user-stories/{id}/task-items/{taskid} | Create a new task| Add a new task to a specific user story | CreateTaskInUserStory |

![Ejemplo de Imagen](../assets/TB2/backlog/swagger1.png)

![Ejemplo de Imagen](../assets/TB2/backlog/swagger2.png)

![Ejemplo de Imagen](../assets/TB2/backlog/pgadmin.png)

<h3> Meeting Bounded Context</h3>

**MeetingController**

| Tag      | Http Verbs | Endpoint                   | Summary                  | Description                | OperationId               |
|----------|------------|----------------------------|--------------------------|----------------------------|---------------------------|
| Meetings | POST       | /api/v1/meetings           | Create a new meeting     | Create a new meeting       | CreateMeeting             |
| Meetings | GET        | /api/v1/meetings           | Get all meetings         | Retrieve all meetings      | GetAllMeetings            |
| Meetings | GET        | /api/v1/meetings/{meetingId} | Get meeting by id        | Retrieve a meeting by ID   | GetMeetingById            |
| Meetings | PUT        | /api/v1/meetings/{meetingId} | Update a meeting         | Update an existing meeting  | UpdateMeeting             |
| Meetings | DELETE     | /api/v1/meetings/{meetingId} | Delete a meeting         | Remove a meeting           | DeleteMeeting             |

**RecordingController**

| Tag        | Http Verbs | Endpoint                              | Summary                        | Description                          | OperationId             |
|------------|------------|---------------------------------------|--------------------------------|--------------------------------------|-------------------------|
| Recordings | GET        | /api/recordings                       | Get all recordings             | Retrieve all recordings              | GetAllRecordings        |
| Recordings | GET        | /api/recordings/meeting/{meetingId}  | Get recordings by meeting ID   | Retrieve recordings for a specific meeting | GetRecordingsByMeetingId |
| Recordings | GET        | /api/recordings/meeting/name/{meetingTitle} | Get recordings by meeting title | Retrieve recordings for meetings by title | GetRecordingsByMeetingTitle |
| Recordings | POST       | /api/recordings                       | Create a new recording         | Create a new recording               | CreateRecording         |
| Recordings | DELETE     | /api/recordings/{recordingId}        | Delete a recording             | Remove a specific recording          | DeleteRecording         |


![Ejemplo de Imagen](../assets/TB2/backlog/backend/back1.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/backend/back2.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/backend/backe3.jpeg)

![Ejemplo de Imagen](../assets/TB2/backlog/backend/backen4.jpeg)


<h3> Issue Bounded Context</h3>

**IssueController**

|Tag|Http Verbs|Endpoint|Summary|Description|OperationId|
|--|--|--|--|--|--|
| Issues | GET       | /api/v1/issues/{issueId}             | Get issue by ID           | Retrieve a specific issue         | GetIssueById      |
| Issues | PUT       | /api/v1/issues/{issueId}             | Update an issue           | Modify an existing issue          | updateIssue       |
| Issues | DELETE    | /api/v1/issues/{issueId}             | Delete an issue           | Remove a specific issue           | deleteIssue       |
| Issues | GET       | /api/v1/issues                       | Get all issues            | Retrieve all issues               | getAllIssues      |
| Issues | POST      | /api/v1/issues                       | Create a new issue        | Add a new issue                   | createIssue       |
| Issues | GET       | /api/v1/issues/{issueId}/events      | Get issue events          | Retrieve events for a specific issue | getAllEventsByIssueId |
| Issues | POST      | /api/v1/issues/{issueId}/events      | Create a new event        | Add a new event to a specific issue | createEvent     |

![alt text](../assets/TB2/backlog/issues/swagger.png)

![alt text](../assets/TB2/backlog/issues/pgadmin4.png) 

![alt text](../assets/TB2/backlog/issues/getissuebyid.png)

#### 5.2.3.7 Software Deployment Evidence for Sprint Review.

- Para poder realizar la sección del Sprint Se decidió usar la plataforma de Figma donde se realizaron los mockups, wireframes y demás de manera colaborativa por parte del equipo y, con esta misma plataforma, se realizó el prototipo de la aplicacion.

- Para poder entrar al figma del grupo es necesario contar con una cuenta ya registrada y haber iniciado sesión en la plataforma mencionada.


- En este Sprint, hemos llevado a cabo diversas actividades relacionadas con el despliegue (Deployment) de nuestra plataforma, asegurando que todos los componentes estén correctamente configurados y listos para su uso. Las actividades de despliegue abarcan múltiples productos, incluyendo la Landing Page, aplicaciones web y servicios web. A continuación, se detallan los pasos realizados, junto con capturas de pantalla que ilustran el proceso y brindan una visión clara de cada etapa.

Landing Page Para la Landing Page se ha implementado utilizando GitHub Pages, lo que facilita su acceso y gestión.

![Ejemplo de Imagen](../assets/TB2/backlog/des1.jpeg)

- En la seccion pages, dentro de la configuracion del repositorio, escoger la rama deseada y seleccionar save para hacer el deploy de esta.

![Ejemplo de Imagen](../assets/TB2/backlog/des2.jpeg)

- Pasados unos minutos se generará el link para acceder a la landing page.

![Ejemplo de Imagen](../assets/TB2/backlog/des3.jpeg)

- Adicionalmente Podemos seleccionar use your GitHub pages website en las opciones de about del repositorio, para poder acceder de una manera mas rapida al link.

Finalmente nos dará un link directo a la Landing page desplegada: https://horizon-managewise.github.io/LandingPage/

Link de explicacion del FrontEnd: https://drive.google.com/drive/folders/11fY4sH9mdNNPkHBJyJAXibVjLx6tnq7-?usp=sharing 

Link 

Para el backend, optamos por genrar un .jar del proyecto, con ayuda del comando mvn clean package, para posteriormente subir este proyecto a un repositorio y conectarlo con microsoft azure mediate github.

![Ejemplo de Imagen](../assets/TB2/backlog/backend/azure1.jpg)

![Ejemplo de Imagen](../assets/TB2/backlog/backend/azure2.png)

![Ejemplo de Imagen](../assets/TB2/backlog/backend/github.png)


#### 5.2.3.8 Team Collaboration Insights during Sprint.

En esta sección, el equipo detalla el proceso de implementación de las actividades realizadas durante el Sprint, destacando la colaboración y el esfuerzo conjunto en la creación de los productos. Se presentan capturas de pantalla de los analíticos de colaboración y los commits en GitHub, que reflejan la participación activa de cada miembro del equipo.

Participación del Equipo Todos los miembros del equipo han contribuido de manera significativa en la implementación de los siguientes productos:

Landing Page: Cada integrante aportó en diferentes aspectos del diseño y desarrollo de la landing page, asegurando que la interfaz sea atractiva y funcional. En esta ultima versión de la landing page no se realizo ningun gran cambio significativo en las ultimas semanas.

**Landing Page**

![Commits](../assets/TB1-new/landingc1.jpeg)

![Commits](../assets/TB1-new/landingc2.jpeg)

- Estefano Oscar Jaque Peña: 2
- John Telesforo Arevalo Meza: 10
- Valentino Sandoval Paiva: 1
- Sergio André Gómez Vallejos: 8

**Report:**


- Estefano Oscar Jaque Peña: 
- John Telesforo Arevalo Meza: 
- Valentino Sandoval Paiva: 
- Sergio André Gómez Vallejos: 

## Frontend:

![alt text](../assets/TB2/backlog/commil1.jpeg)

![alt text](../assets/TB2/backlog/commil2.jpeg)

- Estefano Oscar Jaque Peña: 3
- John Telesforo Arevalo Meza: 5
- Valentino Sandoval Paiva: 1
- Sergio André Gómez Vallejos: 5

**Backend:**

- Estefano Oscar Jaque Peña: 
- John Telesforo Arevalo Meza: 
- Valentino Sandoval Paiva: 
- Sergio André Gómez Vallejos: 

## 5.2.4. Sprint 4

Durante el Sprint 4, nuestro enfoque principal fue el desarrollo del BackEnd Y FronEnd de Horizon utilizando java y angular. Este sprint fue fundamental y primordial para implementar las ultimas funcionalidades del BackEnd y FronEnd, además de lograr la unión y deploy de la última version de ambos servicios.

### 5.2.4.1.  Sprint Planning 4

En este Sprint 4, durante la reunión de planificación, el equipo seleccionará las historias de usuario restantes, para convertirlas en resultados concretos. Además, se distribuirán las tareas de manera equitativa para poder culminar con estas en el tiempo establecido. Para ello, se fomentará la colaboración, asegurandonos que todos tengan un nivel similar de conocimiento en las diferentes áreas, teniendo siempre en cuenta los objetivos del trabajo.

| Sprint # | Sprint 4 |
|-|-|
| **Sprint Planning Background**| |
| **Date**| 13/11/2024 | |
| **Time**| 3:00 PM |
| **Location** | Discord (Reunión virtual)|
| **Prepared By**| Jaque Peña, Estefano Oscar|
| **Attendees (to planning meeting)** |Arevalo Meza, John, Sandoval Paiva, Valentino, Jaque Peña, Estefano, Sergio Gómez|
| **Sprint Goal & User Stories** | |
| **Sprint 4 Goal** | Nuestro meta culminar detalles en el backlog, para unir todos los bounded contexts con los patrones necesarios y posteriormente hacer el deploy del servicio final, para hacer lo mismo con el frontend y unir ambas partes. Creemos que esto nos ayudará a comprender como se relacionan ambos servicios. Lo mencionado se confirmará cuando todas las tareas del sprint 4 en el trello grupal se encuentren con el tag "Done"|
| **Sprint 4 Velocity** | 92 |
| **Sum of Story Points** | 18 |

### 5.2.4.2. Sprint Backlog 4

![alt text](../assets/TB1-image/Trelloo1.png)


| Sprint # | Sprint 4 |||||||
|----------|----------|---------|----------------------------|-----------------------------------------------|------------------|------------------|--------|
| User Story | | Work-Item / Task | |||||||
| ID | Title | ID | Title | Description | Estimation (Hours) | Assigned To | Status |
| US43 | Iniciar sesión (Sign In) | TA001 | Crear componente de inicio de sesión en Angular | Crear el componente en Angular para gestionar el inicio de sesión de los usuarios | 2 horas | Sandoval Paiva, Valentino | Done |
| US43 | Iniciar sesión (Sign In) | TA002 | Implementar formulario de ingreso de credenciales (usuario y contraseña) | Implementar un formulario en Angular para la entrada de usuario y contraseña | 3 horas | Arevalo Meza, John Telesforo | Done |
| US43 | Iniciar sesión (Sign In) | TA003 | Implementar lógica de validación de credenciales en el frontend | Validar las credenciales ingresadas en el frontend antes de enviarlas al servidor | 4 horas | Sergio Gomez | Done |
| US43 | Iniciar sesión (Sign In) | TA004 | Redirigir al usuario a la página principal al iniciar sesión exitosamente | Después de un inicio de sesión exitoso, redirigir al usuario a la página principal | 3 horas | Sandoval Paiva, Valentino | Done |
| US43 | Iniciar sesión (Sign In) | TA005 | Mostrar mensaje de error si las credenciales son incorrectas | Mostrar un mensaje de error si el usuario ingresa credenciales incorrectas | 2 horas | Arevalo Meza, John Telesforo | Done |
| US43 | Iniciar sesión (Sign In) | TA006 | Implementar manejo de sesión para persistencia del estado de login | Implementar un sistema de manejo de sesión para mantener al usuario autenticado | 3 horas | Arevalo Meza, John Telesforo | Done |
| US43 | Iniciar sesión (Sign In) | TA007 | Validar campos de entrada para asegurar que el correo electrónico y la contraseña sean válidos | Asegurar que el correo electrónico y la contraseña ingresados sean válidos antes de enviarlos al servidor | 2 horas | Sandoval Paiva, Valentino | Done |
| US44 | Registro de usuario (Sign Up) | TA008 | Crear componente de registro en Angular | Crear el componente en Angular para el registro de nuevos usuarios | 2 horas | Arevalo Meza, John Telesforo | Done |
| US44 | Registro de usuario (Sign Up) | TA009 | Implementar formulario de registro (correo electrónico, contraseña, confirmación de contraseña) | Implementar el formulario para la entrada de datos de registro, incluyendo correo electrónico, contraseña y confirmación de contraseña | 3 horas | Sergio Gomez | Done |
| US44 | Registro de usuario (Sign Up) | TA010 | Implementar lógica de validación de correo electrónico único | Asegurar que el correo electrónico ingresado no esté ya registrado en la base de datos | 4 horas | Arevalo Meza, John Telesforo | Done |
| US44 | Registro de usuario (Sign Up) | TA011 | Validar la fortaleza de la contraseña y su coincidencia con la confirmación | Validar que la contraseña tenga la fortaleza adecuada y que coincida con la confirmación | 3 horas | Sandoval Paiva, Valentino | Done |
| US44 | Registro de usuario (Sign Up) | TA012 | Redirigir al usuario a la página de inicio de sesión después de un registro exitoso | Después de un registro exitoso, redirigir al usuario a la página de inicio de sesión | 3 horas | Arevalo Meza, John Telesforo | Done |
| US44 | Registro de usuario (Sign Up) | TA013 | Mostrar mensaje de error si el correo electrónico ya está registrado | Mostrar un mensaje de error si el correo electrónico ya está registrado | 2 horas | Arevalo Meza, John Telesforo | Done |
| US44 | Registro de usuario (Sign Up) | TA014 | Implementar lógica para manejar el registro en la base de datos | Implementar la lógica para registrar un nuevo usuario en la base de datos | 4 horas | Sergio Gomez | Done |
| TS009 | Endpoint para registro de usuarios (sign up) | TA015 | Implementar el endpoint "/api/auth/signup" | Implementar el endpoint "/api/auth/signup" para el registro de nuevos usuarios | 2 horas | Estefano Jaque | Done |
| TS009 | Endpoint para registro de usuarios (sign up) | TA016 | Validación de datos de entrada | Validar la solicitud POST con los datos de registro (correo electrónico, contraseña) | 2 horas | Sandoval Paiva, Valentino | Done |
| TS009 | Endpoint para registro de usuarios (sign up) | TA017 | Validación de correo y contraseña | Asegurar que los datos de entrada sean correctos (validación de correo electrónico único y contraseña válida) | 3 horas | Estefano Jaque | Done |
| TS009 | Endpoint para registro de usuarios (sign up) | TA018 | Lógica para registrar usuario | Implementar la lógica para registrar un nuevo usuario en la base de datos | 3 horas | Estefano Jaque | Done |
| TS009 | Endpoint para registro de usuarios (sign up) | TA019 | Respuesta exitosa | Responder con un código 201 Created cuando el registro sea exitoso | 1 hora | Estefano Jaque | Done |
| TS009 | Endpoint para registro de usuarios (sign up) | TA019 | Manejo de error usuario ya registrado | Implementar manejo de errores para cuando el correo electrónico ya esté registrado, respondiendo con código 409 Conflict | 2 horas | Estefano Jaque | Done |
| TS009 | Endpoint para registro de usuarios (sign up) | TA020 | Probar registro de usuario | Probar el endpoint de registro de usuario con datos válidos e inválidos | 2 horas | Estefano Jaque | Done |
| TS010 | Endpoint para inicio de sesión (sign in) "/api/auth/signin" | TA021 | Implementar el endpoint "/api/auth/signin" | Implementar el endpoint "/api/auth/signin" para el inicio de sesión de usuarios | 2 horas | Estefano Jaque | Done |
| TS010 |Endpoint para inicio de sesión (sign in) | TA022 | Validación de credenciales | Validar la solicitud POST con las credenciales de inicio de sesión (usuario y contraseña) | 2 horas | Estefano Jaque | Done |
| TS010 | Endpoint para inicio de sesión (sign in) | TA023 | Verificación de usuario y contraseña | Verificar que el usuario exista en la base de datos y que las credenciales sean correctas | 3 horas | Sandoval Paiva, Valentino | Done |
| TS010 | Endpoint para inicio de sesión (sign in) | TA024 | Generación de token de acceso | Implementar la lógica de autenticación y generación de un token de acceso | 3 horas | Estefano Jaque | Done |
| TS010 | Endpoint para inicio de sesión (sign in) | TA025 | Respuesta exitosa | Responder con un código 200 OK y el token de acceso cuando el inicio de sesión sea exitoso | 2 horas | Sergio Gomez | Done |
| TS010 | Endpoint para inicio de sesión (sign in) | TA026 | Manejo de error credenciales incorrectas | Implementar manejo de errores para credenciales incorrectas, respondiendo con código 401 Unauthorized | 2 horas | Estefano Jaque | Done |
| TS010 | Endpoint para inicio de sesión (sign in) | TA027 | Probar inicio de sesión | Probar el endpoint de inicio de sesión con credenciales correctas e incorrectas | 2 horas | Estefano Jaque | Done |

Link Trello: https://trello.com/invite/b/66ddd34a3a8f75b32fbdaa52/ATTI22d7710f322c2ce38799efbb188aa9556839E153/si729-2402-ws53-grupo-4-horizon-managewise 

### 5.2.4.3. Development Evidence for Sprint Review


| Repository   | Branch | Commit Id                                | Commit Message                                                              | Commit Message Body                                                                                      | Committed on (Date)     |
| ------------ | ------ | ---------------------------------------- | --------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ----------------------- |
| managewise-backend | dev   | 1b462d3                                  | feat: add dates of timeline  |Se añade los datos para el db timeline  | 10/11/2024  |
| managewise-backends | dev   | 3cd1ffc                                  | feat: add dates of statistic              | Se añade los datos para el db statistic  | 10/11/2024   |
| managewise-backend | dev   | 2fb452a                                  | feat: added descripcion general and beneficios sections                     | feat: added descripcion general and beneficios sections                                                  | 10/11/2024   |
| managewise-backend | dev   | 7fe0bdd                                  | Feat: Add nosotros                                                          | Feat: Add nosotros                                                                                       | 10/11/2024  |
| managewise-backend | dev   | 47d2070                                  | Feat: Add nosotros                                                          | Feat: Add nosotros                                                                                       |10/1/2024   |
| managewise-backend       | dev   | 922ad0f| feat: add members bd backend  |feat: add members bd backend   | 14/11/2024  |
|  managewise-backend | dev   | 3cd1ffc| feat: add meetingController| feat: add meetingController.| 14/11/2024   |
|  managewise-backend | dev   | f48083d| feat: Add issues bounded context| feat: Add issues bounded context| 14/11/2024|
|  managewise-backend | dev   | 00a082d| feat: added task list controller| feat: added task list controller| 14/11/2024  |
|  managewise-backend | dev   | 90d1dfa| feat: added backlog items entities and lists| feat: added backlog items entities and lists|14/11/2024   |

### 5.2.4.4. Testing Suite Evidence for Sprint Review


| Repository                                                            | Branch             | Commit Id                                | Commit Message           | Commit Message Body                         | Committed on (Date)     |
| --------------------------------------------------------------------- | ------------------ | ---------------------------------------- | ------------------------ | ------------------------------------------- | ----------------------- |
| https://github.com/Horizon-ManageWise/Testing/tree/feature/TF                         | feature/TF  | 1ffda47a4cd0b4bbb26ea2b3e94dae52c554c12d                                  | Initial commit           | Created the README file.                    | 14/11/2024              |
| https://github.com/Horizon-ManageWise/Testing/tree/feature/TF                         | feature/TF  | 1ffda47a4cd0b4bbb26ea2b3e94dae52c554c12d                                  | feat: added US43 gherkin | feat: added US43 gherkin                    | 14/11/2024              |
| https://github.com/Horizon-ManageWise/Testing/tree/feature/TF                        | feature/TF  | 1ffda47a4cd0b4bbb26ea2b3e94dae52c554c12d                                  | feat: added US44 gherkin | feat: added US44 gherkin                    | 14/11/2024               |
| https://github.com/Horizon-ManageWise/Testing/tree/feature/TF                        | feature/TF  | 1ffda47a4cd0b4bbb26ea2b3e94dae52c554c12d                                  | feat: added TS009 gherkin | feat: added TS009 gherkin                    | 14/11/2024               |
|https://github.com/Horizon-ManageWise/Testing/tree/feature/TF                        | feature/TF  | 1ffda47a4cd0b4bbb26ea2b3e94dae52c554c12d                                  | feat: added TS010 gherkin | feat: added TS010 gherkin                    | 14/11/2024  |


Link del repositorio del testing: https://github.com/Horizon-ManageWise/Testing

### 5.2.4.5. Execution Evidence for Sprint Review

**URL FRONTEND Y BACKEND DESPLEGADO**: https://frontend-test-managewise.vercel.app/sign-in

**URL FRONTEND**: https://frontend-test-managewise.vercel.app

**URL BACKEND**: https://managewise-ffbua6fpfmbteaeq.brazilsouth-01.azurewebsites.net/api/v1/

## **MEMBERS BOUNDED CONTEXT**

En este bounded context members se muestra una lista donde se puede editar o eliminar, incluso agregar un nuevo miembro con su rol correspondiente.

**FRONTEND**

![alt text](../assets/TF/members1.jpg)

**BACKEND**

![alt text](../assets/TF/meeting88.png)

**FRONTEND**

![alt text](../assets/TF/members3.jpg)

**BACKEND**

![alt text](../assets/TF/members4.jpg)

**FRONTEND**

![alt text](../assets/TF/members5.jpg)

**BACKEND**

![alt text](../assets/TF/members6.jpg)

**BACKEND**

![alt text](../assets/TF/members7.jpg)


## **MEETING BOUNDED CONTEXT**

En este bounded context meeting, se conecta con el bounded context Members al mostrar una lista de todos los miembros agregados en dicho bounded context donde se pueden editar los miembros que van a pertenecer a dicha reunion.

**FRONTEND**

![alt text](../assets/TF/meeting1.png)

**BACKEND**

![alt text](../assets/TF/meetingB.png)

**FRONTEND**

![alt text](../assets/TF/meeting2.png)

**BACKEND**

![alt text](../assets/TF/meeting3.png)

**FRONTEND**

![alt text](../assets/TF/meeting4.png)

**BACKEND**

![alt text](../assets/TF/meeting5.png)


## **ISSUES BOUNDED CONTEXT**

En este bounded context Issues, se realiza , siguiendo el PATRON ACL, la validación de existencia de el miembro que insertaré en mis atributos de mi issues como madeBy y AssignedTo ,ademaas de la validacion de la existencia de un nombre de Sprint creado , para poder asignarle este issues por crear.Todo esto debido a que para publicar una incidencia deberemos escribir el creador de esta incidencia y a quien le asigna solucionar el problema y para ello deben existir estos miembros en el proyecto , y se debe asociar a un Sprint por lo que se debe validar que este Sprint existe. De la misma manera, se debe poner solo los valores
HIGH,LOW,MEDIUM para el priority del issues y TO_DO, IN_PROGRESS y DONE para el status , por ultimo se debe poner las fechas de creacion(createdIn) y resolutionDate que es una estimación en si de la fecha limite para la resolucion del problema como un Date DD-MM-YYYY.

Aca se observa como se crea un issues desde el front:
![alt text](../assets/TF/is1.png)

![alt text](../assets/TF/is2.png)

**BACKEND**
Get de Issues:
![alt text](../assets/TF/is3.png)

**FRONTEND**
Para añadir un evento, le damos click a añadir evento y ponemos los datos , luego de ello cuando se valide que es usuario que lo crea existe entonces se crea el evento , se puede ver la viosualizacion en back y front.
![alt text](../assets/TF/is4.png)

![alt text](../assets/TF/is5.png)

**INTERNALIZACIÓN**
se pued ver en español ahora, en la anteriores fotos se encontraba en ingles.
![alt text](../assets/TF/is6.png)

**FILTROS DE BUSQUEDA**
Se puede filtrar la busqueda tanto por Nombre de sprints como por prioridad ded Issue
![alt text](../assets/TF/is7.png)

**BACKLOG BOUNDED CONTEXT**

Se muestra la ultima version del Backend del bounded context BACKLOG. Donde se pueden añadir User stories, con sus epics correspondiente.

**FRONTEND**

![alt text](../assets/TF/ep1.png)

![alt text](../assets/TF/ep2.png)

![alt text](../assets/TF/ep3.png)

**BACKEND**

![alt text](../assets/TF/ep5.png)


### 5.2.4.6. Services Documentation Evidence for Sprint Review

**URL FRONTEND Y BACKEND DESPLEGADO**: https://frontend-test-managewise.vercel.app/sign-in

**URL FRONTEND**: https://frontend-test-managewise.vercel.app

**URL BACKEND**: https://managewise-ffbua6fpfmbteaeq.brazilsouth-01.azurewebsites.net/api/v1/

## **MEMBERS BOUNDED CONTEXT**

Se muestra la ultima version del Backend del bounded context Members, en donde se muestra cada acción del BackEnd de Members:

**BACKEND**

![alt text](../assets/TF/membersBACK.jpg)

![alt text](../assets/TF/members8.jpg)

![alt text](../assets/TF/members9.jpg)


## **MEETING BOUNDED CONTEXT**

Se muestra la ultima version del Backend del bounded context Meeting, en donde se conecta con el bounded context Members:

**BACKEND**

![alt text](../assets/TF/meetingBACK.png)

![alt text](../assets/TF/meeting3.png)

![alt text](../assets/TF/meeting5.png)


## **ISSUES BOUNDED CONTEXT**

Se muestra la ultima version del Backend del bounded context Issues, en donde se conecta con el bounded context Members y Sprint para validacion en el momento de su creacion como de la actualizacion de un issue, ademas tambien se genera la misma validacion de member existente para la creacion del evento dedl issue:

**BACKEND**

![alt text](../assets/TF/is8.png)

Post:
Se puede añadir y dentro de esto se genera las validaciones del existsBy para que no se cree un mismo issue asignado a un mismo SPRINT 
y la validacion del PATRON ACL fetchMemberIdByFullName para que no se genere un Issue el Sprint asociado no ha sido creado,de la misma manera con Member que debe ser creado previamente para poder nombrar al creador del issue y al que se le asigna el Issue(fetchMemberIdByFullName) ademas que no se puede crear un Issue si
no se ha puesto el estado y prioridad de manera correcta , por ele LOW o TO_DO

![alt text](../assets/TF/fetchissue.png)

![alt text](../assets/TF/is9.png)

Get:
Se puede obtener todos los issues
![alt text](../assets/TF/is10.png)

Put:
Se puede actualizar y se valida los existBy ademas de el uso del patron ACL para la validacion del member existente 

![alt text](../assets/TF/updissu.png)

![alt text](../assets/TF/putissue.jpg)

geteventbyIssuId:
Se puede obtener el evento generado y se puede visualizar segun el id que insertes.
![alt text](../assets/TF/getevent.jpg)

post event:
Se puede añadir el evento en base al id del issue que ya fue creado, para la creacion de este evento tambien se usa la validacion con fetch que viene 
![alt text](../assets/TF/eventpsot.jpg)

**BACKLOG BOUNDED CONTEXT**

**BACKEND**

![alt text](../assets/TF/ep5.png)

![alt text](../assets/TF/ep6.png)

![alt text](../assets/TF/ep7.png)

### 5.2.4.7. Software Deployment Evidence for Sprint Review

- En este Sprint, hemos llevado a cabo diversas actividades relacionadas con el despliegue (Deployment) de nuestra plataforma, asegurando que todos los componentes estén correctamente configurados y listos para su uso. Las actividades de despliegue abarcan múltiples productos, incluyendo la Landing Page, aplicaciones web y servicios web. A continuación, se detallan los pasos realizados, junto con capturas de pantalla que ilustran el proceso y brindan una visión clara de cada etapa.

Landing Page Para la Landing Page se ha implementado utilizando GitHub Pages, lo que facilita su acceso y gestión.

![Ejemplo de Imagen](../assets/TB2/backlog/des1.jpeg)

- En la seccion pages, dentro de la configuracion del repositorio, escoger la rama deseada y seleccionar save para hacer el deploy de esta.

![Ejemplo de Imagen](../assets/TB2/backlog/des2.jpeg)

- Pasados unos minutos se generará el link para acceder a la landing page.

![Ejemplo de Imagen](../assets/TB2/backlog/des3.jpeg)

- Adicionalmente Podemos seleccionar use your GitHub pages website en las opciones de about del repositorio, para poder acceder de una manera mas rapida al link.

Finalmente nos dará un link directo a la Landing page desplegada: https://horizon-managewise.github.io/LandingPage/

Link de explicacion del FrontEnd: https://drive.google.com/drive/folders/11fY4sH9mdNNPkHBJyJAXibVjLx6tnq7-?usp=sharing 

Link 

Para el backend, optamos por genrar un .jar del proyecto, con ayuda del comando mvn clean package, para posteriormente subir este proyecto a un repositorio y conectarlo con microsoft azure mediate github.

![Ejemplo de Imagen](../assets/TB2/backlog/backend/azure1.jpg)

![Ejemplo de Imagen](../assets/TB2/backlog/backend/azure2.png)

![Ejemplo de Imagen](../assets/TB2/backlog/backend/github.png)


**Frontend**
A continuación, se mostrara como se desplego el frontend.

![Ejemplo de Imagen](../resources/deployFrontend.png)

![Ejemplo de Imagen](../resources/deployFrontend1.png)

### 5.2.4.8. Team Collaboration Insights during Sprint


En esta sección, el equipo detalla el proceso de implementación de las actividades realizadas durante el Sprint, destacando la colaboración y el esfuerzo conjunto en la creación de los productos. Se presentan capturas de pantalla de los analíticos de colaboración y los commits en GitHub, que reflejan la participación activa de cada miembro del equipo.

Participación del Equipo Todos los miembros del equipo han contribuido de manera significativa en la implementación de los siguientes productos:

Landing Page: Cada integrante aportó en diferentes aspectos del diseño y desarrollo de la landing page, asegurando que la interfaz sea atractiva y funcional. En esta ultima versión de la landing page no se realizo ningun cambio, por lo que los commits no cambian.

**Landing Page**

![Commits](../assets/TB1-new/landingc1.jpeg)

![Commits](../assets/TB1-new/landingc2.jpeg)

- Estefano Oscar Jaque Peña: 2
- John Telesforo Arevalo Meza: 10
- Valentino Sandoval Paiva: 1
- Sergio André Gómez Vallejos: 8


## Frontend:

![alt text](../assets/TB2/backlog/commil1.jpeg)

![alt text](../assets/TB2/backlog/commil2.jpeg)

- Estefano Oscar Jaque Peña: 3
- John Telesforo Arevalo Meza: 5
- Valentino Sandoval Paiva: 1
- Sergio André Gómez Vallejos: 5

**Backend:**

![alt text](../assets/TB2/backlog/commil1.jpeg)

![alt text](../assets/TB2/backlog/commil2.jpeg)


- Estefano Oscar Jaque Peña: 
- John Telesforo Arevalo Meza: 
- Valentino Sandoval Paiva: 
- Sergio André Gómez Vallejos: 



### 5.3 Video About-the-Product.
Link del vídeo: 

