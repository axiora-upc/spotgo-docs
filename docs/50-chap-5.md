# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

Para garantizar un desarrollo fluido, estandarizado y compatible entre todos los miembros del equipo Axiora, se ha definido el siguiente entorno de desarrollo para el ecosistema SpotGo:

### 5.1.1. Software Development Environment Configuration

Se listan a continuación las herramientas utilizadas a lo largo de todo el ciclo de vida del proyecto, cubriendo desde la gestión hasta el despliegue:

* **Project & Requirements Management:**
    * **Trello:** Herramienta SaaS para la gestión ágil del Product Backlog y Sprints. [Referencia: trello.com](https://trello.com/)
    * **UXPressia:** Herramienta SaaS para la gestión de requerimientos (Journey Maps, User Personas). [Referencia: uxpressia.com](https://uxpressia.com/)
* **Product UX/UI Design:**
    * **Figma:** Herramienta SaaS para la elaboración de Wireframes, Mock-ups y Prototipos. [Referencia: figma.com](https://www.figma.com/)
* **Herramientas de Desarrollo (IDEs y Editores):**
    * **WebStorm:** IDE para el desarrollo de Frontend & Web App (Extensiones: Angular Language Service, Prettier, ESLint). [Descarga: jetbrains.com/webstorm](https://www.jetbrains.com/webstorm/)
    * **IntelliJ IDEA:** IDE optimizado para el desarrollo del Backend con Spring Boot. [Descarga: jetbrains.com/idea](https://www.jetbrains.com/idea/)
* **Stack Tecnológico y Entorno de Ejecución:**
    * **Node.js (LTS v20+):** Entorno de ejecución para Angular y la Landing Page. [Descarga: nodejs.org](https://nodejs.org/)
    * **Java Development Kit (JDK 17):** Entorno base para Spring Boot. [Descarga: oracle.com/java](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
    * **PostgreSQL & pgAdmin (v15+):** Motor de base de datos relacional y cliente de administración local. [Descarga: postgresql.org](https://www.postgresql.org/download/)
* **Herramientas de Pruebas y Documentación:**
    * **Postman:** Testeo y validación de los endpoints del backend. [Descarga: postman.com](https://www.postman.com/downloads/)
    * **Swagger (OpenAPI):** Generación automática de la documentación de la API. (Integrado en dependencias de Spring Boot).

### 5.1.2. Source Code Management

El código fuente del proyecto se gestionará utilizando **Git** como sistema de control de versiones y **GitHub** como plataforma colaborativa. Los repositorios oficiales de la organización son:

* **Landing Page:** [https://github.com/axiora-upc/spotgo-landing](https://github.com/axiora-upc/spotgo-landing)
* **Frontend Web Application:** [https://github.com/axiora-upc/spotgo-frontend](https://github.com/axiora-upc/spotgo-frontend)
* **RESTful Web Services:** [https://github.com/axiora-upc/spotgo-backend](https://github.com/axiora-upc/spotgo-backend)

**Estrategia de Ramas (GitFlow)**
Se utilizará un flujo de trabajo basado en GitFlow para proteger la estabilidad del producto:
* `main`: Rama principal. Contiene únicamente código estable, probado y desplegado en producción.
* `develop`: Rama de integración. Aquí se fusionan todas las nuevas características antes del pase a producción.
* `feature/US[ID]-[nombre]`: Ramas de desarrollo. Se crean a partir de `develop` para trabajar una User Story específica (ej. `feature/US01-client-registration`).
* `release/v[X.Y.Z]`: Ramas de preparación para producción. Congelan el código de `develop` para pruebas finales antes de pasar a `main`.
* `hotfix/[nombre]`: Ramas para corregir errores críticos detectados en producción directamente desde `main`.

**Convenciones de Versionado y Commits**
* **Semantic Versioning (SemVer 2.0.0):** Los lanzamientos oficiales en la rama `main` se etiquetarán bajo el formato `vMAJOR.MINOR.PATCH` (ej. v1.0.0).
* **Conventional Commits 1.0.0:** Todos los commits seguirán una estructura semántica (`tipo(alcance): descripción breve`) para generar un historial legible por máquinas y humanos (ej. `feat(auth): add login endpoint`, `fix(map): resolve overlap issue`, `docs: update readme`).

### 5.1.3. Source Code Style Guide & Conventions

Para mantener la legibilidad y calidad del código, todo el equipo aplicará **nomenclatura estrictamente en inglés** para clases, variables, métodos y bases de datos. Además, se adoptan las siguientes guías de estilo oficiales:

* **HTML & CSS:** Se seguirán las directrices de la [HTML Style Guide and Coding Conventions](https://www.w3schools.com/html/html5_syntax.asp) de W3C y la [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html).
* **Frontend (Angular / TypeScript):** Se respetará la [Angular Coding Style Guide](https://angular.io/guide/styleguide). Las clases usarán `PascalCase`, variables/métodos `camelCase`, y archivos `kebab-case`. Se utilizará Prettier y ESLint para automatizar el formato.
* **Backend (Spring Boot / Java):** Se aplicará la [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html). La arquitectura se dividirá en capas estrictas (Controllers, Services, Repositories, Entities). Los endpoints RESTful usarán sustantivos en plural (ej. `GET /api/v1/parking-spots`).
* **Requerimientos:** Se emplearán las [Gherkin Conventions](https://specflow.org/gherkin/gherkin-conventions-for-readable-specifications/) para la redacción estructurada de los criterios de aceptación (Given/When/Then).

### 5.1.4. Software Deployment Configuration

El despliegue del ecosistema SpotGo combinará métodos de publicación ágil desde la línea de comandos para el Frontend y prácticas de Integración/Despliegue Continuo (CI/CD) para el Backend.

* **Landing Page (Sitio Estático) & Frontend Web App:** Ambos repositorios se desplegarán utilizando la infraestructura gratuita de *GitHub Pages*. En lugar de depender de pipelines automatizados (como GitHub Actions), el equipo utilizará el paquete oficial `angular-cli-ghpages`. Este enfoque permite que, al ejecutar un único comando en la terminal local, el proyecto Angular se compile (generando la carpeta `/dist`) y sus artefactos se envíen automáticamente a la rama `gh-pages` del repositorio, sirviendo las aplicaciones globalmente con certificados SSL (HTTPS) provistos por GitHub.
* **Backend (RESTful Web Services):** Se alojará en la plataforma PaaS **Render**. El pipeline de GitHub Actions ejecutará las pruebas de Maven, empaquetará el artefacto `.jar` y ordenará a Render el reinicio del servicio con el nuevo código.
* **Base de Datos en la Nube:** Se utilizará una instancia gestionada de PostgreSQL en **Supabase**, enlazada de forma segura mediante variables de entorno (Environment Variables) al backend en Render.
