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
