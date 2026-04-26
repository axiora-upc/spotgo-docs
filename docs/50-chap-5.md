# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

Para garantizar un desarrollo fluido, estandarizado y compatible entre todos los miembros del equipo Axiora, se ha definido el siguiente entorno de desarrollo para el ecosistema SpotGo:

**Herramientas de Desarrollo (IDEs y Editores)**

* **Frontend & Web App:** WebStorm. Extensiones obligatorias: Angular Language Service, Prettier - Code formatter, ESLint.
* **Backend & APIs:** IntelliJ IDEA, optimizado para el desarrollo con Spring Boot.

**Stack Tecnológico y Entorno de Ejecución**

* **Frontend:** Node.js (LTS versión 20.x o superior) y el framework Angular (TypeScript) para la Web App y Landing Page.
* **Backend:** Java Development Kit (JDK 17) y Spring Boot 3.x para el núcleo lógico, RESTful APIs y procesamiento de los sensores IoT.
* **Base de Datos:** PostgreSQL local (v15+) y pgAdmin para el modelado relacional de inquilinos, usuarios y registros de parqueo.

**Herramientas de Pruebas y Documentación**

* **Postman:** Para el testeo y validación de los endpoints del backend (Check-in, Check-out, webhooks de Stripe).
* **Swagger (OpenAPI):** Para la documentación interactiva de la API (US35).

### 5.1.2. Source Code Management

El código fuente del proyecto se gestionará utilizando **Git** como sistema de control de versiones y **GitHub** como plataforma de alojamiento, aplicando un enfoque estructurado para el trabajo colaborativo.

**Estrategia de Ramas (GitFlow)**

Se utilizará un flujo de trabajo basado en GitFlow para proteger la estabilidad del producto:
* `main`: Rama principal. Contiene únicamente código estable, probado y desplegado en producción.
* `develop`: Rama de integración. Aquí se fusionan todas las nuevas características antes del pase a producción.
* `feature/US[ID]-[nombre]`: Ramas de desarrollo temporal. Se crean a partir de `develop` para trabajar una User Story específica (ej. `feature/US01-client-registration`). Al terminar, se integran a `develop` mediante un *Pull Request* (PR).
* `hotfix/[nombre]`: Ramas para corregir errores críticos detectados en `main`.

**Convención de Commits (Conventional Commits)**

Para mantener un historial limpio y autodescriptivo (alineado al enfoque *Docs-as-Code*), todos los commits deben seguir esta estructura: `tipo(alcance): descripción breve`.
* `feat:` Para una nueva funcionalidad (ej. `feat(auth): add login endpoint`).
* `fix:` Para solucionar un error (ej. `fix(map): resolve spot overlap issue`).
* `docs:` Para cambios en la documentación (`.md`).
* `style:` Cambios de formato (espacios, comas) que no afectan la lógica.

### 5.1.3. Source Code Style Guide & Conventions

Para mantener la legibilidad y calidad del código en todo el equipo, se adoptan las siguientes guías de estilo oficiales:

**Para el Frontend (Angular / TypeScript)**

* Se seguirá la [Angular Coding Style Guide](https://angular.io/guide/styleguide) oficial.
* **Nomenclatura:** Las clases y modelos usarán `PascalCase` (ej. `ParkingSpot`). Las variables y métodos usarán `camelCase` (ej. `getUserProfile`). Los archivos de componentes usarán `kebab-case` (ej. `parking-map.component.ts`).
* **Formateo:** Uso de *Prettier* configurado a 2 espacios de indentación y *ESLint* para detectar antipatrones en TypeScript.

**Para el Backend (Spring Boot / Java)**

* Se aplicará la [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html).
* **Arquitectura:** División estricta en capas (Controllers, Services, Repositories, Entities).
* **APIs RESTful:** Los endpoints deben usar sustantivos en plural y seguir los verbos HTTP estándar (GET para obtener, POST para crear, PUT/PATCH para actualizar, DELETE para eliminar). Ejemplo: `GET /api/v1/parking-spots`.

### 5.1.4. Software Deployment Configuration

El despliegue de SpotGo se automatizará utilizando prácticas de Integración Continua y Despliegue Continuo (CI/CD) para asegurar entregas rápidas y confiables en cada Sprint.

**Infraestructura en la Nube**

* **Frontend (Landing Page & Web App):** Se desplegará en **Vercel**, el cual ofrece integración directa con GitHub para compilar y servir aplicaciones Angular globalmente con certificados SSL (HTTPS) automáticos.
* **Backend (Spring Boot API):** Se alojará en la plataforma PaaS **Render**, configurada para ejecutar el `.jar` generado por Maven.
* **Base de Datos en la Nube:** Instancia de PostgreSQL gestionada (Supabase) conectada de forma segura al backend.

**Pipeline de CI/CD (GitHub Actions)**

Se configurarán flujos de trabajo en `.github/workflows/` que se ejecutarán automáticamente al hacer *push* o *Pull Request* hacia la rama `main`:
1.  **Build & Test:** Compila el código (Angular y Java) y ejecuta pruebas unitarias. Si una prueba falla, el despliegue se detiene.
2.  **Deploy:** Si el paso anterior es exitoso, los artefactos se suben a los servidores de producción de manera automática, sin intervención manual.
