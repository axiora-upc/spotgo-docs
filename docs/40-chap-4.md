# Capítulo IV: Product Design

## 4.1. Style Guidelines

Esta sección establece un repositorio centralizado de diseño que permite mantener la consistencia visual y funcional del sistema SpotGo. Este repositorio incluye la definición de assets, tipografías, paleta de colores, reglas de espaciado y lineamientos de interacción, los cuales son utilizados de forma uniforme por todo el equipo de desarrollo. El objetivo es asegurar una presentación coherente, facilitar la escalabilidad del producto y reducir inconsistencias durante la implementación. Para ello, se toman como base principios de diseño centrado en el usuario, consistencia visual, accesibilidad y eficiencia en la interacción.

### 4.1.1. General Style Guidelines

Los General Style Guidelines definen las decisiones visuales fundamentales del sistema, incluyendo branding, tipografía, colores, espaciado y tono de comunicación, sustentadas en principios UX/UI y en las necesidades identificadas en los usuarios.

**Branding**

El branding de SpotGo fue diseñado para transmitir confianza, eficiencia y modernidad, valores clave en un sistema que gestiona información en tiempo real. Se emplea un color primario azul oscuro (#1A237E), comúnmente asociado con seguridad y tecnología, reforzando la percepción de confiabilidad en el servicio. El logotipo utiliza formas geométricas con bordes redondeados (rounded-lg), lo que reduce la rigidez visual y genera una experiencia más amigable y accesible para el usuario. Esta combinación permite equilibrar profesionalismo con cercanía.

**Typography**

La tipografía principal seleccionada es Inter, acompañada de fuentes de respaldo (ui-sans-serif, system-ui). Esta elección se fundamenta en su alta legibilidad en pantallas digitales, su adecuada altura de x (x-height) y su diseño optimizado para interfaces modernas. Se definió una jerarquía tipográfica clara:

- **Títulos principales:** text-xl font-bold
- **Subtítulos y navegación:** text-sm font-medium
- **Etiquetas e indicadores:** text-xs font-semibold
- **Datos críticos (tiempo, códigos):** font-mono

El uso limitado de pesos tipográficos (medium, semibold, bold) evita ruido visual y mejora la comprensión rápida de la información.

**Colors**

La paleta de colores sigue un enfoque semántico, donde cada color representa un estado o acción específica dentro del sistema:

- **Primary (Azul oscuro #1A237E):** acciones principales, ---navegación activa
- **Secondary (Azul brillante #2979FF):** interacciones, enlaces, foco
- **Success (Verde #00C853):** espacios disponibles, acciones exitosas
- **Warning (Naranja):** alertas de tiempo o expiración
- **Destructive (Rojo):** errores críticos o acciones irreversibles
- **Occupied (Gris):** espacios no disponibles

*Figura 12 (Color Palette)*
![Color Palette](../assets/images/figures/12-color-palette.png)

Una decisión clave es el uso de gris para espacios ocupados en lugar de rojo, con el fin de evitar generar estrés innecesario en el usuario. Esta estrategia reduce la carga cognitiva y mejora la interpretación visual del mapa.

**Spacing**

Se implementa un sistema de espaciado basado en una escala modular de 8px, alineado con CSS. Esto incluye valores como 8px, 16px, 24px y 32px para márgenes, paddings y separación entre componentes.

- Espaciado interno de contenedores: 24px
- Separación entre elementos relacionados: 8px–16px
- Separación entre secciones: 24px–32px

Este sistema garantiza consistencia visual, alineación precisa y facilita la escalabilidad del diseño.

**Tone of Communication**

El tono de comunicación definido es directo, funcional y conciso, evitando frases largas o ambiguas. Ejemplos incluyen:

- “Live updates”
- “Reserve”

Este enfoque responde a usuarios en contextos de alta carga cognitiva (conductores en movimiento), permitiendo una rápida comprensión de la información sin distracciones innecesarias.

**Design System**

El sistema de diseño se basa en tecnologías modernas como typescript, angular, css y html5 lo que permite la creación de componentes reutilizables, accesibles y consistentes. Este enfoque facilita el mantenimiento del sistema, reduce la duplicación de estilos y asegura una experiencia uniforme en toda la aplicación.

### 4.1.2. Web Style Guidelines

Los Web Style Guidelines definen los estándares visuales y de interacción para interfaces web responsivas, asegurando una experiencia consistente, eficiente y accesible.

**Responsive Design**

El diseño utiliza layouts flexibles basados en Flexbox y Grid, evitando dimensiones fijas. Se implementan contenedores adaptables y unidades relativas para garantizar una correcta visualización en diferentes resoluciones.

**Navigation System**

Se adopta un patrón de navegación tipo dashboard, compuesto por:

- **Sidebar persistente:** permite acceso rápido a las secciones principales
- **Navbar superior fija:** contiene acciones globales y estado del sistema

Este enfoque permite mantener el contexto del usuario en todo momento, reduciendo la desorientación y mejorando la eficiencia en la navegación.

**UI Components**

Se definen componentes reutilizables como:

- Botones (primarios, secundarios, estados hover/active)
- Tarjetas (cards) para información estructurada
- Indicadores de estado (disponible, ocupado, alerta)
- Badges y etiquetas informativas

Estos componentes siguen patrones consistentes en tamaño, color y comportamiento, facilitando su reconocimiento por parte del usuario.

**Visual Feedback**

El sistema incorpora mecanismos de retroalimentación visual para mejorar la interacción:

- Animaciones suaves (hover, transitions)
- Cambios de estado visibles en botones e interfaces
- Notificaciones discretas (ej. icono de alerta)

Esto permite al usuario entender rápidamente el resultado de sus acciones y el estado del sistema.

**Accessibility**

Se consideran principios de accesibilidad como:

- Contraste adecuado-
- Tamaños mínimos de interacción-
- Navegación mediante teclado
- Uso de múltiples indicadores (color + texto + iconos)

Esto garantiza una experiencia inclusiva para diferentes tipos de usuarios.

**Relación con el problema**

Todas las decisiones de diseño están alineadas con los problemas identificados en los usuarios:

- **Reducción del tiempo de búsqueda:** mediante visualización clara y en tiempo real
- **Mejor organización:** gracias a estructuras visuales jerárquicas
- **Disminución del estrés:** uso de colores suaves, información clara y feedback inmediato

## 4.2. Information Architecture

En esta sección se definen las decisiones que orientan la organización del contenido en las experiencias web de SpotGo, incluyendo el Landing Page y la aplicación. La arquitectura de la información busca facilitar que los usuarios conductores (B2C) y operadores de estacionamientos (B2B) encuentren la información y funcionalidades de manera rápida e intuitiva.

Para ello, se aplican principios de claridad, jerarquía y orientación a tareas, priorizando en conductores la búsqueda y reserva de espacios, y en operadores la gestión y monitoreo del estacionamiento. Asimismo, se establecen sistemas de organización, etiquetado, navegación y búsqueda que aseguran una experiencia consistente, reduciendo la carga cognitiva y mejorando la usabilidad del sistema.

### 4.2.1. Organization Systems

En esta sección se definen los sistemas de organización del contenido utilizados en la plataforma SpotGo, considerando el Landing Page y las aplicaciones web para conductores y administradores (operadores). El objetivo es estructurar la información de manera clara para que cada tipo de usuario encuentre lo que necesita sin esfuerzo.

Para el Landing Page, se utiliza principalmente una organización jerárquica (visual hierarchy) y por audiencia (audience-based). El contenido está estructurado en secciones claramente diferenciadas como For Drivers y For Operators, permitiendo que cada segmento identifique rápidamente la información relevante. Asimismo, se emplea una organización secuencial, guiando al usuario a través de bloques como How it works, Pricing y FAQ, lo que facilita la comprensión progresiva del servicio desde la propuesta de valor hasta la conversión.

Para el segmento de conductores, dentro de la aplicación web, se aplica una organización por tareas (task-based) y jerárquica. Las funcionalidades se agrupan en secciones como Dashboard, Reservations, Subscription, Receipts, Favorites y History, permitiendo acceso directo a las acciones principales del usuario. Esta estructura reduce la carga cognitiva y optimiza la eficiencia en la interacción.

Además, en los flujos principales como la reserva de estacionamiento o la extensión del tiempo, se utiliza una organización secuencial (step-by-step), guiando al usuario de forma clara desde la selección del espacio hasta la confirmación de la acción.

Por otro lado, para el segmento de administradores (operadores), se emplea una combinación de organización jerárquica y matricial. En el panel Insights Hub, la información se presenta mediante dashboards que agrupan métricas clave como ocupación, ingresos y rendimiento por zonas, permitiendo analizar múltiples variables de manera simultánea. Esta estructura facilita la toma de decisiones basada en datos en tiempo real.

Adicionalmente, se utilizan distintos esquemas de categorización según el tipo de contenido:

- Por funcionalidad en conductores (reservas, pagos, historial).
- Por métricas y gestión en operadores (analytics, monitoreo, configuración).
- Cronológico en secciones como History y Receipts, donde la información se organiza por fechas para facilitar el seguimiento.

En conjunto, estos sistemas de organización permiten una experiencia clara, intuitiva y eficiente, alineada con los objetivos del sistema SpotGo de reducir el tiempo de búsqueda, mejorar el control del usuario y optimizar la gestión de estacionamientos.

### 4.2.2. Labeling Systems

En esta sección se definen las etiquetas utilizadas para representar la información dentro de la plataforma SpotGo, priorizando claridad, simplicidad y consistencia para facilitar la comprensión tanto de conductores como de administradores del sistema.

Para el segmento de conductores, se emplean etiquetas cortas, directas y orientadas a la acción, como “Reserve”, “Extend Time”, “Favorites”, “Receipts” y “History”. Estas permiten que el usuario identifique rápidamente las funcionalidades principales sin generar carga cognitiva, manteniendo coherencia con el flujo de uso de la aplicación.

Por otro lado, para el segmento de administradores (operadores), como se observa en el panel Insights Hub, se utilizan etiquetas más funcionales y orientadas a gestión y análisis, tales como “Analytics”, “Real-time Map”, “Settings”, “Average Occupancy”, “Peak Hour”, “Total Revenue” y “System Health”. Estas etiquetas reflejan métricas clave del negocio y permiten una interpretación rápida del estado del sistema, facilitando la toma de decisiones.

Asimismo, se emplean etiquetas de estado consistentes en ambos segmentos, como “Available”, “Occupied”, “Reserved” y “Active”, lo que asegura uniformidad en la interpretación de la información a lo largo de toda la plataforma.

Finalmente, todas las etiquetas han sido diseñadas con el objetivo de reducir ambigüedad, mantener un lenguaje claro y funcional, y garantizar que cada elemento de la interfaz comunique su propósito de forma inmediata, alineándose con el enfoque de usabilidad y eficiencia del sistema SpotGo.

### 4.2.3. SEO Tags and Meta Tags

En esta sección se definen los SEO Tags y Meta Tags de SpotGo, considerando tanto el Landing Page como las principales vistas de la aplicación web. Estos elementos han sido diseñados estratégicamente para reflejar la propuesta de valor del sistema optimizar la experiencia de estacionamiento para conductores y operadores y mejorar su posicionamiento en motores de búsqueda.

**Landing Page**

- **Title:**
SpotGo – Smart parking, for both sides of the curb.
- **Meta Description:**
Drivers find and reserve open spots in seconds with live IoT data. Operators manage spaces, monitor occupancy and grow revenue from a single dashboard.
- **Keywords:**
For drivers, For Operators, How it works, Princing, FAQ
- **Author:**
Axiora

**Clientes**

*Dashboard*

- **Title:**
SpotGo Dashboard
- **Meta Description:**
Access live parking data, view available spots, manage reservations, and monitor your active parking session in real time.
- **Keywords:**
Live updates, Availble Nearby, Active Reservation, Saved Locations, Avg.Savings
- **Author:**
Axiora

*Reservations Page*

- **Title:**
My Reservations
- **Meta Description:**
Manage tour active and upcoming bookings.
- **Keywords:**
Extend Time, Navigate, Active, Upcoming
- **Author:**
Axiora

*Subscription Page*

- **Title:**
Subscription
- **Meta Description:**
Manage your monthly parking pass and billing preferences.
- **Keywords:**
Available Plans, Payment method, Auto-renewal
- **Author:**
Axiora

*Receipts Page*

- **Title:**
Digital Receipts
- **Meta Description:**
Access, download, and email your parking transaction history
- **Keywords:**
Total receipts, Total Spoent, This month, PDF, Email, Paid Refunded
- **Author:**
Axiora

*Favorites Page*

- **Title:**
Favorites
- **Meta Description:**
 n° saved locations
- **Keywords:**
Navigate, Reserve
- **Author:**
Axiora

*Parking History Page*

- **Title:**
Parking History
- **Meta Description:**
n° pas reservations
- - **Keywords:**
Rate, Spot
- **Author:**
Axiora

**Administradores**

*Analytics*

- **Title:**
Insights Hub
- **Meta Description:**
Real time performance and occupancy intelligence.
- **Keywords:**
Average Occupancy, Peak Hour, Total Revenue, System Health
- **Author:**
Axiora

*Employees*
- **Title:** 
Watch your employees, their assassinated parking spot if they have one. If they’re on duty or they’re off
- **Meta Description:**
Watch your employees, their assassinated parking spot if they have one. If they’re on duty or they’re off
- **Keywords:**
On Duty
- **Author:**
Axiora

*Overview*
- **Title:**
Main Terminal Hub
- **Meta Description:**
Real-time telemetry from Sector 04-A Smart Grid
- **Keywords:**
Export Logs, Refresh Sync, Total Spaces, Currently Available
- **Author:**
Axiora

*Report*

- **Title:**
Reports
- **Meta Description:**
Watch a series of records which englove, accidents inside the building, missing reservations, etc.
- **Keywords:**
Unathorized parking
- **Author:**
Axiora

### 4.2.4. Searching Systems

En esta sección se definen los mecanismos de búsqueda implementados en la plataforma SpotGo, con el objetivo de facilitar a los usuarios la localización rápida de información relevante y evitar que se sientan perdidos frente al volumen de datos disponible.

Para el segmento de conductores, el sistema de búsqueda se centra en la ubicación y disponibilidad de estacionamientos. Se incorpora una barra de búsqueda (“Search parking locations…”) que permite encontrar espacios mediante nombre, dirección o identificador. Además, se complementa con un sistema de filtros dinámicos, como Available, EV Charging, Covered y Valet, los cuales ayudan a refinar los resultados según las necesidades del usuario.

Asimismo, el mapa interactivo actúa como un sistema de búsqueda visual, donde los usuarios pueden identificar espacios disponibles en tiempo real mediante indicadores de estado (available, occupied, reserved). Esta combinación de búsqueda textual y visual reduce significativamente el tiempo necesario para encontrar un estacionamiento.

En secciones como Receipts y History, se implementa una búsqueda específica por contenido, permitiendo filtrar información mediante datos como ubicación, número de reserva o identificador de transacción. Esto facilita el acceso rápido a registros pasados sin necesidad de recorrer listas extensas.

Por otro lado, para el segmento de administradores (operadores), el sistema incluye una barra de búsqueda orientada a la exploración de datos (“Search analytics…”), permitiendo localizar información dentro del dashboard. Además, los datos se organizan mediante filtros temporales como Today, Last 7 Days y Custom, lo que facilita el análisis de métricas en distintos periodos.

Finalmente, los resultados de búsqueda se presentan de forma clara y estructurada: en listas organizadas (para recibos e historial) o mediante visualizaciones gráficas y métricas (en el caso de operadores). Esto asegura que los usuarios no solo encuentren la información, sino que puedan interpretarla fácilmente.

En conjunto, los Searching Systems de SpotGo combinan búsqueda textual, filtros y visualización interactiva, permitiendo una experiencia eficiente, intuitiva y alineada con el objetivo principal del sistema: reducir el tiempo de búsqueda y mejorar la toma de decisiones del usuario.

### 4.2.5. Navigation Systems

En esta sección se describen los sistemas de navegación utilizados en SpotGo, los cuales guían a los usuarios a través del Landing Page y las aplicaciones web, permitiéndoles cumplir sus objetivos de manera eficiente y sin fricción.

Para el Landing Page, se emplea una navegación global superior (top navigation bar) con accesos directos a secciones clave como For Drivers, For Operators, How it works, Pricing y FAQ. Esta navegación permite a los usuarios desplazarse de manera rápida entre contenidos informativos. Asimismo, se incorporan Call To Action (CTA) visibles como “I’m a Driver” y “I’m a Parking Operator”, que dirigen al usuario hacia su flujo correspondiente dentro del sistema. La estructura de la página también favorece una navegación secuencial vertical (scroll-based navigation), donde el usuario recorre progresivamente la propuesta de valor, funcionalidades, métricas y testimonios.

Para el segmento de conductores, dentro de la aplicación web, se utiliza una navegación lateral persistente (sidebar navigation) que incluye secciones como Dashboard, Reservations, Subscription, Receipts, Favorites y History. Este tipo de navegación permite acceso constante a las funcionalidades principales sin necesidad de regresar a una página inicial, reduciendo la fricción en la interacción.

Además, se implementa una navegación contextual, donde el usuario puede ejecutar acciones directamente desde los componentes de la interfaz, como “Reserve”, “Extend Time”, “Navigate” o “Rate”. Estas acciones están ubicadas estratégicamente dentro del flujo del usuario, facilitando la toma de decisiones sin cambiar de vista.

También se incluye una navegación basada en estados, donde elementos como “Active Now” permiten acceder rápidamente a la sesión de estacionamiento en curso, reforzando la visibilidad de la información más relevante en tiempo real.

Por otro lado, para el segmento de administradores (operadores), se emplea una navegación lateral similar, con secciones como Real-time Map, Analytics y Settings. Esta estructura permite gestionar diferentes aspectos del sistema desde un mismo entorno. Asimismo, dentro del dashboard Insights Hub, se utiliza una navegación contextual y por filtros, como Today, Last 7 Days y Custom, facilitando la exploración de datos y métricas según distintos criterios.

Finalmente, en toda la plataforma se mantiene consistencia en los patrones de navegación, utilizando etiquetas claras, jerarquía visual y accesos directos, lo que permite a los usuarios orientarse fácilmente y completar sus tareas de forma rápida y efectiva.

En conjunto, estos sistemas de navegación garantizan una experiencia fluida, intuitiva y centrada en el usuario, alineada con los objetivos de SpotGo de reducir la fricción, mejorar la accesibilidad y optimizar la interacción tanto para conductores como para operadores.

## 4.3. Landing Page UI Design

### 4.3.1. Landing Page Wireframe

*Figura 13 (Landing Page Wireframe)*
![Landing Page Wireframe](../assets/images/figures/13-wireframe-landing-page.png)

### 4.3.2. Landing Page Mock-up

*Figura 14 (Landing Page Mock-up)*
![Landing Page Mock-up](../assets/images/figures/14-mockup-landing-page.png)

## 4.4. Web Applications UX/UI Design

En esta sección se presenta la propuesta de diseño UX/UI de las aplicaciones web de SpotGo, describiendo la estructura visual, los elementos de interfaz y los patrones de interacción que guían la experiencia del usuario.

El diseño está orientado a los dos segmentos del sistema: usuarios y administradores, priorizando una interacción clara, eficiente y alineada con sus necesidades. Asimismo, se asegura la coherencia con los Style Guidelines y la Information Architecture, garantizando una experiencia intuitiva y consistente en toda la plataforma.

### 4.4.1. Web Applications Wireframes

**Client View**

*Figura 15 (Wireframe Login)*
![Wireframe](../assets/images/figures/15-wireframe-login.png)

*Figura 16 (Dashboard)*
![Wireframe](../assets/images/figures/16-wireframe-dashboard.png)

*Figura 17 (My Reservations)*
![Wireframe](../assets/images/figures/17-wireframe-reservation.png)

*Figura 18 (Subscription)*
![Wireframe](../assets/images/figures/18-wireframe-subcription.png)

*Figura 19 (Receipts)*
![Wireframe](../assets/images/figures/19-wireframe-receipts.png)

*Figura 20 (Favorites)*
![Wireframe](../assets/images/figures/20-wireframe-favorites.png)

*Figura 21 (Parking History)*
![Wireframe](../assets/images/figures/21-wireframe-history.png)

**Admin View**

*Figura 22 (Analytics - Insights Hub)*
![Wireframe](../assets/images/figures/22-wireframe-analytics.png)

*Figura 23 (Overview - Real time map)*
![Wireframe](../assets/images/figures/23-wireframe-overview-real-time-map.png)

*Figura 24 (Overview - Main terminal hub)*
![Wireframe](../assets/images/figures/24-wireframe-main-terminal-hub.png)

*Figura 25 (Reports)*
![Wireframe](../assets/images/figures/25-wireframe-report.png)

*Figura 26 (Reports List)*
![Wireframe](../assets/images/figures/26-wireframe-report-list.png)

*Figura 27 (Employees)*
![Wireframe](../assets/images/figures/27-wireframe-employees.png)

*Figura 28 (Employees List)*
![Wireframe](../assets/images/figures/28-wireframe-employees-list.png)

### 4.4.2. Web Applications Wireflow Diagrams

**Client Wireflows**

*Figura 29 (Registro)*
![Wireflow](../assets/images/figures/29-wireflow-registro.png)

*Figura 30 (Buscar estacionamiento)*
![Wireflow](../assets/images/figures/30-wireflow-buscar-estacionamiento.png)

*Figura 31 (Reservar espacio)*
![Wireflow](../assets/images/figures/31-wireflow-reservar-espacio.png)

*Figura 32 (Recibos digitales)*
![Wireflow](../assets/images/figures/32-wireflow-recibos-digitales.png)

*Figura 33 (Suscripciones)*
![Wireflow](../assets/images/figures/33-wireflow-suscripciones.png)

*Figura 34 (Extender tiempo)*
![Wireflow](../assets/images/figures/34-wireflow-extender-tiempo.png)

*Figura 35 (Historial y calificacion)*
![Wireflow](../assets/images/figures/35-wireflow-historial-calificar.png)

*Figura 36 (Historial y calificacion)*
![Wireflow](../assets/images/figures/36-wireflow-eliminar-parking.png)

**Admin Wireflows**

*Figura 37 (Observar parametros del analisis)*
![Wireflow](../assets/images/figures/37-wireflow-observar-parametros.png)

*Figura 38 (Eliminar Parking)*
![Wireflow](../assets/images/figures/38-wireflow-eliminar-parking.png)

*Figura 39 (Vista de Reportes)*
![Wireflow](../assets/images/figures/39-wireflow-vista-reportes.png)

*Figura 40 (Vista de Empleados)*
![Wireflow](../assets/images/figures/40-wireflow-vista-empleados.png)

### 4.4.3. Web Applications Mock-ups

**Admin View**

*Figura 41 (SpotGo Analytics & Patterns)*
![Mockups](../assets/images/figures/41-mockup-spotgo-analytics&Ppatterns.png)

*Figura 42 (SpotGo Analytics - Patterns)*
![Mockups](../assets/images/figures/42-mockup-spotgo-analytics-patterns.png)

*Figura 43 (SpotGo Insight hub)*
![Mockups](../assets/images/figures/43-mockup-spotGo-personnel-log.png)

*Figura 44 (SpotGo Employees)*
![Mockups](../assets/images/figures/44-mockup-spotgo-real-time.png)

*Figura 45 (SpotGo List Reports)*
![Mockups](../assets/images/figures/45-mockup-spotgo-list-reports.png)

*Figura 46 (Main Terminal Hub)*
![Mockups](../assets/images/figures/46-mockup-terminal-main-hub.png)

*Figura 47 (Report)*
![Mockups](../assets/images/figures/47-mockups-report.png)

*Figura 48 (List Employees)*
![Mockups](../assets/images/figures/48-mockup-list-employees.png)

**Client View**

*Figura 49 (Dashboard)*
![Mockups](../assets/images/figures/49-mockup-dashboard.png)

*Figura 50 (Favorites)*
![Mockups](../assets/images/figures/50-mockup-favorites.png)

*Figura 51 (Parking History)*
![Mockups](../assets/images/figures/51-mockup-ParkingHistory.png)

*Figura 52 (Receipts)*
![Mockups](../assets/images/figures/52-mockup-Receipts.png)

*Figura 53 (Reservation)*
![Mockups](../assets/images/figures/53-mockup-Reservation.png)

*Figura 54 (Subscription)*
![Mockups](../assets/images/figures/54-mockup-Subcription.png)

### 4.4.4. Web Applications User Flow Diagrams

**Client User Flows**

*Figura 55 (Registro)*
![UserFlow](../assets/images/figures/55-userflow-registro.png)

*Figura 56 (Buscar estacionamiento)*
![UserFlow](../assets/images/figures/56-userflow-buscar-estacionamiento.png)

*Figura 57 (Reservar Espacio)*
![UserFlow](../assets/images/figures/57-userflow-reservar-espacio.png)

*Figura 58 (Recibos Digitales)*
![UserFlow](../assets/images/figures/58-userflow-recibos-digitales.png)

*Figura 59 (Suscripciones)*
![UserFlow](../assets/images/figures/59-userflow-suscripciones.png)

*Figura 60 (Extender tiempo)*
![UserFlow](../assets/images/figures/60-userflow-extenter-tiempo.png)

*Figura 61 (Eliminar Parking)*
![UserFlow](../assets/images/figures/61-userflow-eliminar-parking.png)

*Figura 62 (Consultar historial y calificar experiencia)*
![UserFlow](../assets/images/figures/62-userflow-historial-experiencia.png)

**Admin User Flows**

*Figura 63 (Observar parametros del analisis)*
![UserFlow](../assets/images/figures/63-userflow-observar-parametros.jpg)

*Figura 64 (Eliminar Parking)*
![UserFlow](../assets/images/figures/64-userflow-eliminar-parking.jpg)

*Figura 65 (Vista de Reportes)*
![UserFlow](../assets/images/figures/65-userflow-vista-reportes.jpg)

*Figura 66 (Vista de Empleados)*
![UserFlow](../assets/images/figures/66-userflow-vista-empleados.jpg)

## 4.5. Web Applications Prototyping

- Landing Page Prototype Link: [https://www.figma.com/proto/LMAhXrMKRKaUJjckWtSebJ/spotgo-design?node-id=544-1511&p=f&t=HysI4gRVQ5NX5T7W-0&scaling=scale-down-width&content-scaling=fixed&starting-point-node-id=544%3A1511](https://www.figma.com/proto/LMAhXrMKRKaUJjckWtSebJ/spotgo-design?node-id=544-1511&p=f&t=HysI4gRVQ5NX5T7W-0&scaling=scale-down-width&content-scaling=fixed&starting-point-node-id=544%3A1511)
- Client Prototype Link: [https://www.figma.com/proto/LMAhXrMKRKaUJjckWtSebJ/spotgo-design?node-id=93-3977&t=rTgWt8HVJ9AypDPo-0&scaling=scale-down-width&content-scaling=fixed&page-id=1%3A2&starting-point-node-id=93%3A3977](https://www.figma.com/proto/LMAhXrMKRKaUJjckWtSebJ/spotgo-design?node-id=93-3977&t=rTgWt8HVJ9AypDPo-0&scaling=scale-down-width&content-scaling=fixed&page-id=1%3A2&starting-point-node-id=93%3A3977)
- Admin Prototype Link: [https://www.figma.com/proto/LMAhXrMKRKaUJjckWtSebJ/spotgo-design?node-id=413-222&t=rTgWt8HVJ9AypDPo-0&scaling=scale-down-width&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=413%3A222](https://www.figma.com/proto/LMAhXrMKRKaUJjckWtSebJ/spotgo-design?node-id=413-222&t=rTgWt8HVJ9AypDPo-0&scaling=scale-down-width&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=413%3A222)

## 4.6. Domain-Driven Software Architecture

### 4.6.1. Design-Level EventStorming

Se utilizó la guía de Philippe Bourgau, proporcionada en la rúbrica del Final Problem Statement, para llevar a cabo el proceso de Design-Level EventStorming, con el objetivo de identificar los Bounded Contexts, siguiendo sus etapas:

- Unstructured Exploration
- Timelines
- Pain Points
- Pivotal Points
- Commands
- Policies
- Read Models
- External Systems
- Aggregates
- Bounded Contexts

Miro Board Link: https://miro.com/welcomeonboard/V2xyaEY4TCtuVTdxSEYvWlJwdFNGZkkvNmJnSDc2dUhrWkQ4MjlvOFB2dVQzd3hadHFBVXpROVE4UGFDbVI3NXY1NDFuam5BMVg3R1hKZEswQWV3TThSN09OOXpNNklYZDlJV2R6Z2hjSFJ6L2NzdGo1MXhGamo1WVVFMFdwaWNyVmtkMG5hNDA3dVlncnBvRVB2ZXBnPT0hdjE=?share_link_id=953121470391

*Figura 67 (Design Level EventStorming)*  
![Design Level EventStorming](../assets/images/figures/67-design-level-event-storming.jpg)

### 4.6.2. Software Architecture Context Diagram

*Figura 68 (C4 Context Diagram)*
![C4 Context Diagram](../assets/images/figures/68-context-diagram.png)

### 4.6.3. Software Architecture Container Diagrams

*Figura 69 (C4 Container Diagram)*
![C4 Container Diagram](../assets/images/figures/69-container-diagram.png)

### 4.6.4. Software Architecture Components Diagrams

*Figura 70 (C4 Component Diagram 1)*
![C4 Component Diagram 1](../assets/images/figures/70-component-diagram-1.png)

*Figura 71 (C4 Component Diagram 2)*
![C4 Component Diagram 2](../assets/images/figures/71-component-diagram-2.png)

*Figura 72 (C4 Component Diagram 3)*
![C4 Component Diagram 3](../assets/images/figures/72-component-diagram-3.png)

*Figura 73 (C4 Component Diagram 4)*
![C4 Component Diagram 4](../assets/images/figures/73-component-diagram-4.png)

*Figura 74 (C4 Component Diagram 5)*
![C4 Component Diagram 5](../assets/images/figures/74-component-diagram-5.png)

*Figura 75 (C4 Component Diagram 6)*
![C4 Component Diagram 6](../assets/images/figures/75-component-diagram-6.png)

## 4.7. Software Object-Oriented Design

### 4.7.1. Class Diagrams

*Figura 76 (Bounded Context 1)*
![Class Diagram](../assets/images/figures/76-bounded-class-1.png)

*Figura 77 (Bounded Context 2)*
![Class Diagram](../assets/images/figures/77-bounded-class-2.png)

*Figura 78 (Bounded Context 3)*
![Class Diagram](../assets/images/figures/78-bounded-class-3.png)

*Figura 79 (Bounded Context 4)*
![Class Diagram](../assets/images/figures/79-bounded-class-4.png)

*Figura 80 (Bounded Context 5)*
![Class Diagram](../assets/images/figures/80-bounded-class-5.png)

*Figura 81 (Bounded Context 6)*
![Class Diagram](../assets/images/figures/81-bounded-class-6.png)

## 4.8. Database Design

### 4.8.1. Database Diagrams

*Figura 82 (Database Diagram)*
![Database Diagram](../assets/images/figures/82-database-diagram.png)
