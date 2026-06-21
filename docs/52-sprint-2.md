### 5.2.2. Sprint 2

#### *5.2.2.1. Sprint Planning 2*

Para el desarrollo del segundo sprint nos centramos en el elaboración del frontend de nuetra aplicación, para ello lo  dividimos de acuerdo a la cantidad de bounded context con cada integrante del grupo (fueron 5 bounded context, 1 por cada integrante). En el Frontend podemos encontrar Dashboard, Reservaciones de estacionamiento, Suscripciones, Recibos, Favoritos y Historial de estacionamientos visitados.

| **Sprint #** | 2 |
| --- | --- |
| **Sprint Planning Background** | |
| **Date** | 2026-05-05 |
| **Time** | 6:00 PM |
| **Location** | Reunión virtual |
| **Prepared By** | Adrian Ruiz Mideyros |
| **Attendees** | Adrian Ruiz Mideyros, Nestor Alonso Rojas Tello, Paul Alexandro Espinoza Lopez, Cesar Jair Contreras Rojas, Johan Alexis Contreras Granados |
| **Sprint 1 Review Summary** | During Sprint 1, the team successfully established the initial project foundations, including repository configuration, cloud infrastructure setup, GitFlow workflow definition, and collaborative development standards using Conventional Commits. In addition, the team refined the Lean UX process to better align the value proposition with the identified User Personas and business problem. The initial Product Backlog was reorganized to improve traceability between User Stories, acceptance criteria, Impact Mapping, and the defined project scope. |
| **Sprint 1 Retrospective Summary** | During the retrospective, the team identified the need to improve the specificity and consistency of User Stories and acceptance criteria to ensure complete alignment with the project scope and Lean UX Canvas. The team also agreed to strengthen documentation quality, maintain consistent English writing standards, and include more alternative user flows and responsive design considerations in future prototypes. Additionally, the team reinforced the mandatory use of GitFlow, Conventional Commits, branch naming conventions, and task estimation practices for all future sprints. |
| **Sprint Goal & User Stories** | |
| **Sprint 2 Goal** | Our focus is on delivering a responsive, fast, and fully navigable static Landing Page using HTML, CSS, and JavaScript, including multilingual support and a clear value proposition aligned with the identified User Personas. This sprint also aims to strengthen the visual identity, improve user flows, and validate the business idea through an accessible and responsive user experience. Success will be confirmed when users can navigate the deployed Landing Page seamlessly across different devices and clearly understand the platform’s innovative value proposition. |
| **Sprint 1 Velocity** | 10 Story Points (Velocidad estimada para el primer ciclo del equipo). |
| **Sum of Story Points** | 10 |

#### *5.2.2.2. Aspect Leaders and Collaborators*

A continuación se detalla la matriz de liderazgo y colaboración (LACX) para brindar claridad en la comunicación del equipo durante el desarrollo de las tareas de este Sprint.

| Team Member (Last Name, First Name) | GitHub Username | Bounded context IoT | Bounded context profiles | Bounded context Payment | Bounded context Occupancy | Bounded context Infrastructure |
| --- | --- | --- | --- | --- | --- | --- |
| Ruiz Mideyros, Adrian | @AdrixRyz | L | C | C | C | C |
| Rojas Tello, Nestor Alonso | @nes-ro | C | C | L | C | C |
| Espinoza Lopez, Paul Alexandro | @R3memo | C | L | C | C | C |
| Contreras Rojas, Cesar Jair | @CesarJrCR | C | C | C | L | C |
| Contreras Granados, Johan Alexis | @johancg04 | C | C | C | C | L |

#### *5.2.2.3. Sprint Backlog 2*

El sprint Backlog se centra en la elaboración del frontend principal de SpotGo, esto incluye el diseño responsivo, el dashboard y el acceso por roles tanto el de administrador como el de conductor. Es gracias a estas implementaciones que hemos logrado una aplicación interactiva conectada a servicios simulados para validar la experiencia antes de agregar las API's

**Trello link:** [https://trello.com/invite/b/6a3044b58529d68c1f19afee/ATTIa322332a59d2dc5bf472752e3591fc3f5CBEB433/axiora-trello](https://trello.com/invite/b/6a3044b58529d68c1f19afee/ATTIa322332a59d2dc5bf472752e3591fc3f5CBEB433/axiora-trello)

![Sprint Backlog 2](../assets/images/others/s2-sprint-backlog.png)

| User Story Id | User Story Title | Work-Item / Task Id | Work-Item / Task Title | Description | Estimation (Hours) | Assigned To | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| US05 | Upload Parking Croquis | TS05.1 | Develop Croquis Upload Module | Implementar el módulo de carga de croquis permitiendo subir imágenes PNG/JPG y validar formatos soportados. | 4 | @nes-ro | In Progress |
| US09 | Virtual Receipt Generation | TS09.1 | Develop Virtual Ticket Module | Llevar a cabo la generación y visualización de tickets virtuales con información del espacio asignado. | 3 | @nes-ro | Done |
| US10 | Spot Occupancy Detection | TS10.1 | Develop Occupancy Detection Logic | Aplicar la lógica de actualización automática del estado de ocupación. | 3 | @johancg04 | In Progress |
| US11 | Spot Availability Detection | TS11.1 | Develop Spot Availability Tracker | Poner en marcha la actualización automática de disponibilidad de espacios. | 4 | @CesarJrCR | In Progress |
| US13 | Availability Alerts | TS13.1 | Develop Alert Notification System | Poner en marcha sistema de alertas en tiempo real para ocupación alta e infracciones. | 4 | @nes-ro | Done |
| US14 | Real-time Admin Dashboard | TS14.1 | Develop Real-time Monitoring Dashboard | Poner en marcha dashboard en tiempo real con visualización dinámica de ocupación y filtros por zonas. | 4 | @CesarJrCR | Done |
| US15 | Client Occupancy View | TS15.1 | Develop Client Parking Map View | Implementar vista interactiva para clientes mostrando espacios disponibles y rutas asignadas. | 3 | @CesarJrCR | Done |
| US20 | Automated Electronic Billing | TS20.1 | Develop Electronic Billing Integration | Llevar a cabo generación automática de comprobantes electrónicos compatibles con SUNAT. | 3 | @CesarJrCR | Done |
| US21 | View Digital Receipts | TS21.1 | Develop Digital Receipt Viewer | Implementar módulo para visualizar y descargar comprobantes electrónicos en PDF. | 3 | @CesarJrCR | Done |
| US28 | Platform Language Selection | TS28.1 | Implement Internationalization Support | Configurar soporte i18n para Inglés y Español en la aplicación Angular. | 3 | @johancg04 | Done |

## 5.2.2.4. Development Evidence for Sprint Review

Durante el Sprint 2, el equipo implementó los módulos principales de la interfaz de usuario de la plataforma Smart Parking siguiendo una arquitectura de contexto delimitado y el flujo de trabajo GitFlow. Los siguientes commits evidencian el desarrollo de funcionalidades, la monitorización en tiempo real, la gestión administrativa, la configuración de la implementación, la gestión de suscripciones y la integración de la infraestructura realizadas durante el sprint.

| Repository | Branch | Commit Id | Commit Message | Committed By | Commit Date |
| --- | --- | --- | --- | --- | --- |
| spotgo-frontend | feature/realtime-map | af847e3 | feat: enhance RealtimeMap component with internal tab navigation for sub-routes | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 479c045 | feat: implement MonitoringStore to manage application state for monitoring context | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 15bb62c | feat: implement MonitoringApi to aggregate backend operations for monitoring context | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 38d8ef1 | feat: implement ParkingSnapshotApiEndpoint for managing /parkingSnapshot resource | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 5a30044 | feat: implement IncidentsApiEndpoint for /incidents resource | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 5121432 | feat: implement EmployeesApiEndpoint for /employees resource | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 058dbe8 | feat: implement detailed overview layout for Realtime Map with dynamic parking data | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 9880692 | feat: refactor Reports component for Realtime Map with DDD approach and incident loading | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 7dc2fb1 | feat: implement EmployeeForm component with form fields and dialog integration | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | d5fa923 | feat: enhance Employees component layout with header, empty state, and action buttons | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 71c2dce | feat: add ParkingSnapshot domain entities | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | e513fa3 | feat: add Employee entity for realtime-map Employees tab | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 17372a1 | feat: add IncidentReport entity for realtime-map reports | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 8b1cb6d | feat: implement reusable confirm dialog component with i18n support | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/analytics-view | 96c1cc2 | feat(admin): add analytics view | AdrixRyz | 2026-05-14 |
| spotgo-frontend | feature/settings-view | 73d3c4c | feat(admin): add settings view | CesarJrCR | 2026-05-14 |
| spotgo-frontend | feature/settings-view | c81f9d1 | feat(settings): implement notification preferences module | CesarJrCR | 2026-05-14 |
| spotgo-frontend | feature/settings-view | 4f62ac8 | feat(settings): add profile configuration form and validations | CesarJrCR | 2026-05-14 |
| spotgo-frontend | feature/settings-view | d1f38a0 | feat(settings): add responsive styles for settings dashboard | CesarJrCR | 2026-05-14 |
| spotgo-frontend | feature/settings-view | 8bcf531 | feat(settings): implement account settings translations | CesarJrCR | 2026-05-14 |
| spotgo-frontend | feature/payment | 722e6fc | feat: subscriptions view finalized | nes-ro | 2026-05-14 |
| spotgo-frontend | feature/payment | 53ff704 | feat: add receivs views and language for subscriptions | nes-ro | 2026-05-14 |
| spotgo-frontend | feature/payment | 5dd0462 | feat: add suscription and database json server config | nes-ro | 2026-05-14 |
| spotgo-frontend | feature/payment | 23994d2 | Merge branch 'develop' into feature/payment | nes-ro | 2026-05-14 |
| spotgo-frontend | feature/iot-monitoring | 6ac28f1 | feat(iot): implement realtime occupancy synchronization | R3memo | 2026-05-14 |
| spotgo-frontend | feature/iot-monitoring | 9d3f4bc | feat(iot): add parking sensor monitoring service | R3memo | 2026-05-14 |
| spotgo-frontend | feature/iot-monitoring | e12af74 | feat(iot): implement telemetry event handling for parking devices | R3memo | 2026-05-14 |
| spotgo-frontend | feature/iot-monitoring | b71fd55 | feat(iot): integrate realtime parking alerts with monitoring context | R3memo | 2026-05-14 |
| spotgo-frontend | feature/iot-monitoring | 43ab8d2 | feat(iot): add IoT dashboard widgets for occupancy metrics | R3memo | 2026-05-14 |
| spotgo-frontend | develop | faece7e | feat(deploy): add vercel deploy config | AdrixRyz | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 438cf91 | feat: enable lazy loading of Angular Material animations | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | f0e77bd | feat: add db.json for parking snapshot, incidents, and employee data | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | bac9356 | feat: add reports component with template, styles, and tests | johancg04 | 2026-05-14 |
| spotgo-frontend | feature/realtime-map | 07e26b3 | feat: add overview component with template, styles, and tests | johancg04 | 2026-05-14 |

#### *5.2.2.5. Execution Evidence for Sprint Review*

Durante el Sprint 2, el equipo logró implementar la primera versión funcional de la aplicación web, permitiendo la gestión y monitoreo en tiempo real de las operaciones de estacionamiento dentro de una plataforma centralizada. Durante este Sprint se desarrollaron los principales módulos frontend del sistema, incluyendo monitoreo en tiempo real, dashboards administrativos, gestión de empleados, visualización de ocupación de estacionamientos, gestión de suscripciones, configuración del sistema y visualización de analíticas.

Asimismo, se implementó la navegación dinámica entre los diferentes módulos de la aplicación mediante Angular Routing, manejo de estado utilizando stores especializados para monitoreo, componentes reutilizables y soporte multilenguaje en Español e Inglés mediante internacionalización (i18n). Además, se avanzó en la implementación de capas de integración RESTful, entidades de dominio, assemblers DTO, diálogos reutilizables e interfaces responsivas siguiendo la arquitectura basada en bounded contexts y capas definida para el proyecto.

De igual manera, se integraron configuraciones de infraestructura y despliegue utilizando Vercel, permitiendo automatizar el despliegue continuo y mejorar la accesibilidad de la aplicación durante el desarrollo iterativo. También se incorporaron funcionalidades de monitoreo en tiempo real para simular actualizaciones de ocupación de estacionamientos, seguimiento de incidentes, administración de empleados y visualización de telemetría IoT relacionada con las operaciones del estacionamiento inteligente.

A continuación, se presenta la evidencia visual de las principales vistas, módulos y funcionalidades implementadas durante el Sprint 2.

### Vista de Usuario

*Figura 85 (Dashboard)*

![Dashboard](../assets/images/figures/85-dashboard.png)

*Figura 86 (Reservations)*

![Reservations](../assets/images/figures/86-reservations.png)

*Figura 87 (Subscriptions)*

![Subscriptions](../assets/images/figures/87-subscription.png)

*Figura 88 (Receipts)*

![Receipts](../assets/images/figures/88-receipts.png)

*Figura 89 (Favorites)*

![Favorites](../assets/images/figures/89-favorites.png)

*Figura 90 (History)*

![History](../assets/images/figures/90-history.png)

### Vista de Administrador

*Figura 91 (Real Time Map - Overview)*

![Real Time Map - Overview](../assets/images/figures/91-overview.png)

*Figura 92 (Real Time Map - Reports)*

![Real Time Map - Reports](../assets/images/figures/92-reports.png)

*Figura 93 (Real Time Map - Employees)*

![Real Time Map - Employees](../assets/images/figures/93-employees.png)

*Figura 94 (Analytics)*

![Analytics](../assets/images/figures/94-analytics.png)

*Figura 95 (Settings)*

![Settings](../assets/images/figures/95-settings.png)

**Web App Demostration Video:** [https://upcedupe-my.sharepoint.com/:f:/g/personal/u202423752_upc_edu_pe/IgA2kceyaesLRLXekQjDh4ArAVEEAL0OxNcOFE_COv4X7kw?e=JoYpwY](https://upcedupe-my.sharepoint.com/:f:/g/personal/u202423752_upc_edu_pe/IgA2kceyaesLRLXekQjDh4ArAVEEAL0OxNcOFE_COv4X7kw?e=JoYpwY)

#### *5.2.2.6. Services Documentation Evidence for Sprint Review*

En esta sección se presenta la documentación de los principales Web Services implementados durante el Sprint 2 para la Web Application de SpotGo. Los servicios fueron diseñados bajo el estilo arquitectónico RESTful y documentados utilizando el estándar OpenAPI, permitiendo definir de manera clara las operaciones disponibles, los parámetros y las estructuras de request y response esperadas.

Durante este Sprint se implementaron endpoints relacionados con la gestión de perfiles administrativos, monitoreo en tiempo real, analítica de ocupación, control de incidencias, gestión de empleados, historial de reservas y procesamiento de pagos y suscripciones. Los servicios fueron integrados utilizando una API REST simulada mediante `json-server`, que expone automáticamente rutas CRUD a partir del archivo `server/db.json`, facilitando las pruebas funcionales de la aplicación frontend desarrollada en Angular sin depender de un backend productivo.

La URL base de los servicios se resuelve desde el archivo de environment: en desarrollo corresponde a `http://localhost:3000` (`environment.development.ts`) y en producción a `/api`, servida mediante Vercel a través de `index.js`. En la siguiente tabla, dicha base se referencia como `{apiUrl}`.

A continuación, se presenta la relación de endpoints implementados y documentados para este Sprint.

**Relación de endpoints implementados**

| Contexto / Módulo | Recurso (Endpoint Base) | Acciones Implementadas |
|---|---|---|
| Profiles | `/admins` | GET, PUT |
| Profiles – Favorites | `/favorites` | GET, DELETE |
| Monitoring | `/employees` | GET, POST, PUT, DELETE |
| Monitoring | `/incidents` | GET |
| Monitoring | `/parkingSnapshot` | GET, PATCH |
| Monitoring | `/spotUtilization` | GET |
| Monitoring / Parking | `/parkings` | GET, PATCH |
| Parking | `/reservations` | GET, POST, PUT |
| Parking | `/clientReports` | POST |
| Payment | `/subscriptions` | GET, PUT |
| Payment | `/clientPlans` | GET |
| Payment | `/receipts` | GET, POST |

#### *5.2.2.7. Software Deployment Evidence for Sprint Review*

Durante el sprint 2 se implementó la infraestructura de despliegue continuo para la aplicación web SpotGo utilizando Vercel. La configuración de despliegue se realizó mediante el archivo `vercel.json`, que define las rutas de redirección, los endpoints de la API simulada y las variables de entorno necesarias para la correcta ejecución de la aplicación en producción.

![Software Deployment](../assets/images/others/s2-deployment.png)

**Enlace al Frontend Desplegado (Angular):** [https://spotgo-frontend.vercel.app](https://spotgo-frontend.vercel.app)

#### *5.2.2.8. Team Collaboration Insights during Sprint*

Todos los miembros del equipo han participado activamente en la implementación de los productos del Sprint 2, lo cual se evidencia mediante los reportes de actividad y contribución del repositorio de GitHub de la organización Axiora.

![Team Insights Sprint 2](../assets/images/others/s2-insights.png)
