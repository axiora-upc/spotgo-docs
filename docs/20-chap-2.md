# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competidores

### 2.1.1. Análisis competitivo

**Competitive Analysis Landscape**

*¿Por qué llevar a cabo este análisis?*

Permite identificar cómo funcionan las soluciones actuales de estacionamiento, detectar sus limitaciones y diferenciar a Axiora mediante una mejor organización por zonas y control de usuarios.

*Logos*

| SpotGo | Apparka | iPark | Parkopedia |
| --- | --- | --- | --- |
| <img src="../assets/images/others/spotgo-logo.png" alt="spotgo-logo" width="150"/> | <img src="../assets/images/others/apparka-logo.png" alt="apparka-logo" width="150"/> | <img src="../assets/images/others/ipark-logo.png" alt="ipark-logo" width="150"/> | <img src="../assets/images/others/parkopedia-logo.png" alt="parkopedia-logo" width="150"/> |

*Perfil*

|     | SpotGo | Apparka | iPark | Parkopedia |
| --- | --- | --- | --- | --- |
| Overview | Sistema que monitorea en tiempo real los estacionamientos por zonas, organiza a sus usuarios y genera alertas por su uso indebido. | Startup peruana que ofrece una plataforma de reserva y pago de estacionamientos en línea. | Plataforma integral de gestión de estacionamientos con enfoque en IoT y control de accesos. | Directorio global de estacionamientos con información de tarifas, ubicación y horarios.  |
| Ventaja competitiva ¿Qué valor ofrece a los clientes? | Datos en tiempo real de ocupación con alta precisión, junto a la organización por zonas y control de usuarios, permitiendo reducir conflictos y mejorar la eficiencia del estacionamiento. | Facilidad de pago digital y reservas anticipadas; cobertura local en Perú. | Integración de hardware (barreras, sensores, QR) con software centralizado. | Base de datos global con información masiva y comparaciones. |

*Perfil de marketing*

|     | SpotGo | Apparka | iPark | Parkopedia |
| --- | --- | --- | --- | --- |
| Mercado Objetivo | Conductores en áreas urbanas de alta demanda de estacionamiento; municipalidades y operadores privados. | Conductores urbanos que buscan optimizar tiempo en estacionar. | Empresas, centros comerciales, universidades, hospitales. | Conductores que buscan estacionamientos cercanos en distintas ciudades.  |
| Estrategias de Marketing | Pruebas piloto en distritos con alta congestión; alianzas con municipalidades y centros comerciales. | Alianzas con playas de estacionamiento privadas; difusión digital. | Marketing institucional y convenios con operadores de parking. | SEO, integración con Google Maps, Waze y fabricantes de autos. |

*Perfil de producto*

|     | SpotGo | Apparka | iPark | Parkopedia |
| --- | --- | --- | --- | --- |
| Productos y Servicios | Sensores de proximidad, identificación de tipo de usuario, app de notificación, panel de control. | App móvil para reservar estacionamientos, pagar online y visualizar disponibilidad. | Gestión de accesos, control de cobros, administración en la nube. | Información de estacionamientos (ubicación, tarifas, reseñas). |
| Precios y costos | Costo de hardware (sensores) + suscripción mensual para acceso al servicio. | Modelo SaaS con comisión por reserva. | Costos de implementación planes de servicio. | Gratuito para usuarios; ingresos por licencias de datos. |
| Canales de distribución (Web y/o móvil) | App móvil, panel web, integración API para municipios y operadores . | App móvil y página web. | Plataforma web + app + hardware en sitio. | Web, app, APIs integradas en vehículos inteligentes. |

*Análisis SWOT*

|     | SpotGo | Apparka | iPark | Parkopedia |
| --- | --- | --- | --- | --- |
| Fortalezas | Datos en tiempo real, tecnología simple y precisa; adaptable a distintos entornos. | Local, conoce mercado peruano; interfaz sencilla. | Infraestructura tecnológica completa (IoT + software). | Base de datos global; integración en autos inteligentes. |
| Debilidades | Requiere inversión inicial en sensores; depende de la aceptación de usuarios y municipios. | Depende de acuerdos con playas privadas; sin sensores en tiempo real. | Alto costo de implementación; complejo para usuarios pequeños. | Información no siempre en tiempo real; depende de terceros. |
| Oportunidades | Alianzas con municipalidades, centros comerciales, universidades. | Expandirse a más distritos y alianzas municipales. | Escalar en Latinoamérica; integración con smart cities. | Aliarse con municipios para ofrecer datos más exactos. |
| Amenazas | Entrada de competidores grandes con recursos (Google, Waze, Parkopedia). | Competencia con apps globales y nuevas startups IoT. | Aparición de soluciones más baratas y modulares. | Startups locales con datos en vivo vía sensores. |

### 2.1.2. Estrategias y tácticas frente a competidores

1. Diferenciación mediante IoT y datos en tiempo real:
A diferencia de soluciones como Apparka o Parkopedia, que dependen de reportes manuales o información de terceros, el sistema propuesto utiliza sensores IoT instalados en cada espacio de estacionamiento, permitiendo:
\- Detección automática de ocupación en tiempo real
\- Actualización inmediata de disponibilidad
\- Reducción de errores y desactualización de información
Esto convierte al sistema en una solución más precisa, confiable y automatizada, siendo su principal ventaja competitiva. 

2. Modelo modular y escalable:
A diferencia de soluciones como iPark, que requieren inversiones elevadas desde la implementación inicial, el sistema se diseña bajo un enfoque modular:
\- Implementación por etapas (por zonas o niveles de estacionamiento)
\- Escalabilidad desde pequeños estacionamientos hasta infraestructuras complejas (aeropuertos, centros comerciales, hospitales, universidades)
\- Reducción de barreras de entrada para adopción inicial
Esto permite una mayor flexibilidad económica y técnica para los operadores.
  
3. Gestión inteligente por tipos de usuario
El sistema incorpora un enfoque diferenciado según el tipo de usuario:
\- Clientes regulares: búsqueda rápida de espacios disponibles
\- Taxistas y transportistas: zonas asignadas o priorizadas en centros comerciales y aeropuertos
\- Administración del estacionamiento: control total de ocupación y flujos
\- Colaboradores internos: acceso a zonas operativas específicas
 
4. Experiencia de usuario centrada en información inmediata
La aplicación prioriza la toma de decisiones rápida mediante:
\- Notificaciones en tiempo real sobre disponibilidad
\- Mapas de ocupación del estacionamiento
\- Rutas sugeridas hacia espacios libres
Esto reduce significativamente el tiempo de búsqueda de estacionamiento y mejora la experiencia del conductor. 

5. Posicionamiento de SmartParking para ciudades inteligentes
El sistema no se plantea únicamente como una aplicación de estacionamiento, sino como una infraestructura de movilidad urbana inteligente, aportando valor a:
\- Centros comerciales y empresas (mayor rotación de vehículos y clientes)
\- Ciudadanos (optimización del tiempo de búsqueda de estacionamiento)
Este enfoque permite diferenciarse de aplicaciones convencionales de parking
 
6. Analítica de datos y soporte a la toma de decisiones
El sistema incluye un módulo de analítica avanzada para administradores, permitiendo:
\- Tasas de ocupación por hora y zona
\- Identificación de horas pico
\- Rotación de vehículos
\- Ingresos estimados por estacionamiento 

## 2.2. Entrevistas

### 2.2.1. Diseño de entrevistas



### 2.2.2. Registro de entrevistas



### 2.2.3. Análisis de entrevistas



## 2.3. Needfinding

### 2.3.1. User Personas



### 2.3.2. User Task Matrix



### 2.3.3. User Journey Mapping



### 2.3.4. Empathy Mapping



## 2.4. Big Picture EventStorming



## 2.5. Ubiquitous Language


