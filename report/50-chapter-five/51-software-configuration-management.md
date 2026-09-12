## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration

Para el desarrollo de VitaLink se utilizarán diferentes herramientas de software que permitirán gestionar las actividades correspondientes al ciclo de vida del producto, incluyendo la gestión del proyecto, análisis de requisitos, diseño UX/UI, desarrollo de software, documentación, control de versiones y despliegue.

---

#### Project Management

Para la gestión del proyecto y organización del Product Backlog se utilizará **Trello** como herramienta de planificación y seguimiento. Esta permitirá organizar las actividades correspondientes a cada Sprint, distribuir responsabilidades entre los integrantes y visualizar el avance de las tareas del proyecto.

Asimismo, se utilizará **GitHub Issues** para registrar incidencias y actividades relacionadas directamente con los repositorios, permitiendo mantener trazabilidad sobre los cambios y tareas técnicas realizadas durante el desarrollo.

**Enlaces:**

- [Trello](https://trello.com/)
- [GitHub Issues](https://docs.github.com/en/issues)

---

#### Requirements Management

Para la gestión y análisis de requisitos se utilizarán **UXPressia** y **Miro** como herramientas de apoyo para la elaboración de diferentes artefactos relacionados con el entendimiento de los usuarios y la definición del producto.

**UXPressia** será utilizada para la elaboración de User Personas, Empathy Maps, User Journey Maps e Impact Maps, permitiendo representar las necesidades, comportamientos y objetivos de los usuarios de VitaLink.

**Miro** será utilizado como espacio de trabajo colaborativo para organizar ideas, realizar análisis visuales y desarrollar diferentes actividades relacionadas con el descubrimiento, definición y planificación del producto.

Los criterios de aceptación correspondientes a las User Stories y Technical Stories serán redactados utilizando **Gherkin**, permitiendo definir escenarios mediante la estructura Given-When-Then.

La documentación de requisitos será almacenada dentro del repositorio del Project Report utilizando archivos Markdown gestionados mediante GitHub.

**Enlaces:**

- [UXPressia](https://uxpressia.com/)
- [Miro](https://miro.com/)
- [Gherkin Documentation](https://cucumber.io/docs/gherkin/)

---

#### Product UX/UI Design

Para el diseño de la experiencia e interfaz de usuario de VitaLink se utilizará **Figma** como herramienta principal para la elaboración de Wireframes, Mock-ups y Prototypes.

Asimismo, **Miro** será utilizado como herramienta colaborativa para organizar flujos e ideas relacionadas con la experiencia del usuario.

Para la elaboración de diagramas complementarios se utilizará **Lucidchart**.

La Frontend Web Application seguirá los principios de Material Design y utilizará **Angular Material** como biblioteca de componentes para mantener consistencia visual entre las diferentes interfaces del producto.

**Enlaces:**

- [Figma](https://www.figma.com/)
- [Miro](https://miro.com/)
- [Lucidchart](https://www.lucidchart.com/)
- [Angular Material](https://material.angular.io/)
- [Material Design](https://m3.material.io/)

---

#### Software Development

La solución VitaLink estará compuesta por una Landing Page, una Frontend Web Application y RESTful Web Services.

La Landing Page será desarrollada utilizando **HTML5, CSS3 y JavaScript**, permitiendo construir una interfaz web responsive orientada a comunicar la propuesta de valor de VitaLink.

La Frontend Web Application será desarrollada utilizando **Angular Framework** junto con **TypeScript**, además de HTML5 y CSS3 para la estructura y presentación de las interfaces.

Los RESTful Web Services serán desarrollados utilizando **Java**, **Spring Boot Framework** y **Spring Data JPA**, permitiendo implementar la lógica de negocio y gestionar la persistencia de información de VitaLink.

Como entornos de desarrollo se utilizarán **Visual Studio Code** para el desarrollo de componentes frontend, Landing Page y documentación, e **IntelliJ IDEA** para el desarrollo de los RESTful Web Services.

Para la gestión de dependencias de la Frontend Web Application se utilizarán **Node.js** y **NPM**.

**Enlaces:**

- [Angular](https://angular.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [Java](https://www.java.com/)
- [Spring Boot](https://spring.io/projects/spring-boot)
- [Spring Data JPA](https://spring.io/projects/spring-data-jpa)
- [Visual Studio Code](https://code.visualstudio.com/)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/)
- [Node.js](https://nodejs.org/)
- [NPM](https://www.npmjs.com/)

---
#### Software Architecture and Database Design

Para la documentación de la arquitectura del software se utilizará **Structurizr**, permitiendo elaborar los diagramas correspondientes al C4 Model y representar la estructura de los diferentes componentes que conforman VitaLink.

Para la elaboración de diagramas UML y otros modelos visuales se utilizará **Lucidchart**, permitiendo representar componentes, relaciones y procesos del sistema.

Para el diseño y modelado de la base de datos se utilizará **MySQL Workbench**, permitiendo representar tablas, atributos, claves primarias, claves foráneas, restricciones y relaciones correspondientes al modelo de datos de VitaLink.

**Enlaces:**

- [Structurizr](https://structurizr.com/)
- [Lucidchart](https://www.lucidchart.com/)
- [MySQL Workbench](https://www.mysql.com/products/workbench/)

---

#### Software Documentation

La documentación general del proyecto será elaborada mediante archivos **Markdown** almacenados dentro del repositorio público del Project Report en GitHub.

Para la documentación de los RESTful Web Services se utilizará **OpenAPI Specification mediante Swagger**, permitiendo documentar los endpoints disponibles, métodos HTTP, parámetros, requests y responses correspondientes a los servicios implementados.

**Repositorios actuales del proyecto:**

- Project Report Repository:  
https://github.com/CodeBrokers-VitaLink/upc-pre-202620-1asi0729-7737-CodeBrokers-Report

- Landing Page Repository:  
https://github.com/CodeBrokers-VitaLink/upc-pre-202620-1asi0729-7737-CodeBrokers-Landin_Page

**Enlaces:**

- [Markdown Guide](https://www.markdownguide.org/)
- [OpenAPI Specification](https://swagger.io/specification/)
- [Swagger](https://swagger.io/)

---

#### Software Version Control

Para el control de versiones y trabajo colaborativo se utilizarán **Git** y **GitHub**.

Git será utilizado como sistema distribuido de control de versiones, mientras que GitHub permitirá almacenar y administrar los diferentes repositorios del proyecto.

El equipo utilizará **GitFlow Workflow** para organizar las ramas de desarrollo, **Conventional Commits** para mantener un historial de modificaciones ordenado y **Semantic Versioning** para identificar las versiones liberadas de los productos de VitaLink.

**Enlaces:**

- [Git](https://git-scm.com/)
- [GitHub](https://github.com/)

---

## 5.1.2. Source Code Management

Para el seguimiento de modificaciones y el trabajo colaborativo durante el desarrollo de VitaLink se utilizará **Git** como sistema de control de versiones y **GitHub** como plataforma para almacenar y administrar los repositorios del proyecto.

Cada producto de software contará con su propio repositorio, permitiendo mantener separados los diferentes componentes de la solución y facilitando su desarrollo, mantenimiento y despliegue.

| Producto | Repositorio | Enlace |
|----------|-------------|--------|
| Landing Page | CodeBrokers Landing Page | https://github.com/CodeBrokers-VitaLink/upc-pre-202620-1asi0729-7737-CodeBrokers-Landin_Page |
| Frontend Web Application | Pendiente | Pendiente |
| RESTful Web Services | Pendiente | Pendiente |

El repositorio correspondiente a los RESTful Web Services almacenará el código fuente del backend junto con los archivos correspondientes a las pruebas unitarias, pruebas de integración y pruebas de aceptación necesarias para comprobar el correcto funcionamiento de los servicios implementados.

---

### GitFlow Workflow

Para organizar el desarrollo colaborativo se utilizará **GitFlow Workflow**, permitiendo separar las versiones estables del producto de los cambios que todavía se encuentran en desarrollo.

Las principales ramas utilizadas serán:

- `main`: contendrá las versiones estables y aprobadas de los productos.
- `develop`: será utilizada como rama principal de integración durante el desarrollo.
- `feature`: permitirá desarrollar nuevas funcionalidades o modificaciones de manera independiente.
- `release`: permitirá preparar nuevas versiones antes de incorporarlas a la rama principal.
- `hotfix`: permitirá realizar correcciones urgentes sobre versiones existentes.

Las ramas de funcionalidades serán creadas a partir de `develop`. Una vez finalizados y revisados los cambios, estos serán integrados nuevamente a `develop` mediante Pull Requests.

Cuando se alcance una versión estable del producto, los cambios correspondientes serán preparados mediante una rama `release` antes de ser incorporados a `main`.

---

### Branch Naming Convention

Para mantener una nomenclatura uniforme durante el desarrollo, las ramas utilizarán nombres descriptivos utilizando **kebab-case**.

Las ramas serán organizadas según el propósito de cada modificación utilizando las siguientes estructuras:

- `feature/<nombre-funcionalidad>` para nuevas funcionalidades.
- `release/<version>` para preparación de nuevas versiones.
- `hotfix/<version>` para correcciones urgentes.

Esta convención permitirá identificar fácilmente el propósito de cada rama y mantener organizado el flujo de trabajo del equipo.

---

#### Software Architecture and Database Design

Para la documentación de la arquitectura del software se utilizará **Structurizr**, permitiendo elaborar los diagramas correspondientes al C4 Model y representar la estructura de los diferentes componentes que conforman VitaLink.

Para la elaboración de diagramas UML y otros modelos visuales se utilizará **Lucidchart**, permitiendo representar componentes, relaciones y procesos del sistema.

Para el diseño y modelado de la base de datos se utilizará **MySQL Workbench**, permitiendo representar tablas, atributos, claves primarias, claves foráneas, restricciones y relaciones correspondientes al modelo de datos de VitaLink.

**Enlaces:**

- [Structurizr](https://structurizr.com/)
- [Lucidchart](https://www.lucidchart.com/)
- [MySQL Workbench](https://www.mysql.com/products/workbench/)

---

#### Software Documentation

La documentación general del proyecto será elaborada mediante archivos **Markdown** almacenados dentro del repositorio público del Project Report en GitHub.

Para la documentación de los RESTful Web Services se utilizará **OpenAPI Specification mediante Swagger**, permitiendo documentar los endpoints disponibles, métodos HTTP, parámetros, requests y responses correspondientes a los servicios implementados.

**Repositorios actuales del proyecto:**

- Project Report Repository:  
https://github.com/CodeBrokers-VitaLink/upc-pre-202620-1asi0729-7737-CodeBrokers-Report

- Landing Page Repository:  
https://github.com/CodeBrokers-VitaLink/upc-pre-202620-1asi0729-7737-CodeBrokers-Landin_Page

**Enlaces:**

- [Markdown Guide](https://www.markdownguide.org/)
- [OpenAPI Specification](https://swagger.io/specification/)
- [Swagger](https://swagger.io/)

---

#### Software Version Control

Para el control de versiones y trabajo colaborativo se utilizarán **Git** y **GitHub**.

Git será utilizado como sistema distribuido de control de versiones, mientras que GitHub permitirá almacenar y administrar los diferentes repositorios del proyecto.

El equipo utilizará **GitFlow Workflow** para organizar las ramas de desarrollo, **Conventional Commits** para mantener un historial de modificaciones ordenado y **Semantic Versioning** para identificar las versiones liberadas de los productos de VitaLink.

**Enlaces:**

- [Git](https://git-scm.com/)
- [GitHub](https://github.com/)

---

### Semantic Versioning

Para identificar las versiones liberadas de VitaLink se utilizará **Semantic Versioning**, siguiendo la estructura:



El componente **MAJOR** representa cambios importantes que pueden generar incompatibilidad con versiones anteriores del producto.

El componente **MINOR** representa la incorporación de nuevas funcionalidades manteniendo compatibilidad con versiones existentes.

El componente **PATCH** representa correcciones de errores o mejoras menores que no modifican la compatibilidad del sistema.

Ejemplos:

- `v1.0.0`: Primera versión estable del producto.
- `v1.1.0`: Incorporación de nuevas funcionalidades compatibles.
- `v1.1.1`: Corrección de errores sobre una versión existente.

---

### Conventional Commits

Para mantener un historial de cambios organizado y comprensible, los commits seguirán la especificación **Conventional Commits**.

La estructura utilizada será:


Los principales tipos utilizados serán:

| Tipo | Descripción |
|------|-------------|
| `feat` | Incorporación de nuevas funcionalidades. |
| `fix` | Corrección de errores. |
| `docs` | Cambios relacionados con documentación. |
| `style` | Cambios de formato que no modifican la funcionalidad. |
| `refactor` | Reestructuración del código sin modificar su comportamiento. |
| `test` | Incorporación o modificación de pruebas. |
| `chore` | Tareas de mantenimiento o configuración. |

Ejemplos:


feat(landing): add hero section

fix(auth): correct user authentication

docs(report): update sprint documentation

test(service): add service unit tests

### 5.1.3. Source Code Style Guide & Conventions

Para mantener uniformidad, legibilidad y facilidad de mantenimiento en el código fuente de VitaLink se establecerán convenciones comunes para los diferentes lenguajes y tecnologías utilizados durante el desarrollo.

La nomenclatura utilizada en el código será escrita en **inglés**, independientemente del lenguaje de programación empleado. Asimismo, se utilizarán nombres descriptivos que permitan identificar claramente la responsabilidad de variables, funciones, métodos, clases y componentes.

Para **HTML** se utilizarán elementos semánticos siempre que sea posible, manteniendo una estructura ordenada y una indentación consistente. Los identificadores y nombres de clases serán descriptivos y estarán escritos en inglés.

Para **CSS** se mantendrá una organización consistente de los estilos y se utilizarán nombres descriptivos para las clases. Se buscará evitar la duplicación innecesaria de estilos y mantener una separación clara entre estilos generales y específicos de cada componente.

Para **JavaScript** se utilizarán nombres claros para las variables y funciones, manteniendo una estructura organizada que facilite la comprensión y mantenimiento del código.

Para el desarrollo de la Frontend Web Application con **Angular y TypeScript** se seguirán las convenciones recomendadas por Angular y Google TypeScript Style Guide. Los componentes, servicios, clases, interfaces, variables y métodos utilizarán nombres descriptivos en inglés y estarán organizados de forma modular.

Para el desarrollo de los RESTful Web Services con **Java y Spring Boot** se seguirá Google Java Style Guide y las convenciones recomendadas para proyectos desarrollados con Spring Boot. Se mantendrá una separación adecuada entre controladores, servicios, repositorios, entidades y demás componentes de la aplicación.

Los criterios de aceptación correspondientes a User Stories y Technical Stories serán redactados utilizando **Gherkin**, siguiendo la estructura Given-When-Then y procurando que cada escenario represente un comportamiento verificable del sistema.

Asimismo, durante el desarrollo se mantendrán las siguientes convenciones generales:

- Utilizar nomenclatura en inglés.
- Utilizar nombres descriptivos.
- Evitar abreviaciones innecesarias.
- Mantener una indentación consistente.
- Evitar duplicación innecesaria de código.
- Mantener una estructura modular.
- Separar adecuadamente las responsabilidades entre componentes.
- Mantener consistencia entre los diferentes repositorios de VitaLink.

Estas convenciones permitirán mantener una estructura uniforme en el código desarrollado y facilitarán la colaboración, comprensión y mantenimiento de VitaLink durante las diferentes etapas del proyecto.


### 5.1.4. Software Deployment Configuration

En esta sección se detalla la configuración requerida para desplegar la Landing Page del proyecto. El propósito es asegurar que, a partir del código fuente disponible en los repositorios, se pueda realizar una publicación funcional y accesible para los usuarios.

#### Despliegue de Landing Page

La Landing Page de VitaLink será desarrollada utilizando **HTML, CSS y JavaScript**, y será publicada mediante **GitHub Pages**, un servicio gratuito proporcionado por GitHub para alojar sitios web estáticos.

Pasos para el despliegue:

1. Se creará un repositorio independiente en GitHub para almacenar el código fuente correspondiente a la Landing Page.

2. Se subirán los archivos del proyecto, incluyendo código HTML, CSS, JavaScript y los recursos estáticos necesarios para el funcionamiento del sitio.

3. En la configuración del repositorio se habilitará GitHub Pages, seleccionando la rama `main` y la carpeta raíz `/` como fuente de publicación.

4. GitHub Pages generará automáticamente una URL pública mediante la cual la Landing Page podrá ser visualizada y utilizada por los usuarios.

**Repositorio:** [https://github.com/CodeBrokers-VitaLink/upc-pre-202620-1asi0729-7737-CodeBrokers-Landin_Page]
.

**URL desplegada:** Pendiente de completar.

