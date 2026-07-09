# Conclusiones

## Sprint 1 – Landing Page y documentación del proyecto

- **Sobre el análisis del problema y la investigación del usuario:** Se concluye que las entrevistas realizadas a administradores y conductores permitieron validar la existencia de problemas recurrentes relacionados con la búsqueda de estacionamiento, congestión interna, mala señalización y falta de control operativo. Esta fase permitió identificar necesidades reales del mercado y construir una propuesta de valor centrada en optimizar la experiencia de estacionamiento mediante tecnología inteligente.

- **Sobre la propuesta de valor y validación inicial:** La elaboración de la *Landing Page* permitió comunicar de forma clara los objetivos, beneficios y funcionalidades principales de SpotGo, funcionando como un medio de validación temprana de la idea de negocio. Se evidenció que presentar una interfaz informativa y accesible favorece la comprensión del problema y fortalece el interés de potenciales usuarios y clientes B2B.

- **Sobre la documentación y modelado del proyecto:** La construcción del reporte técnico permitió consolidar los hallazgos del *Problem Statement*, *Needfinding*, *User Personas*, *Empathy Maps*, *Journey Maps*, *Event Storming* y *Ubiquitous Language*, generando una visión integral del dominio del negocio. Asimismo, el uso de metodologías como *Domain-Driven Design (DDD)* facilitó la identificación de *Bounded Contexts* y responsabilidades del sistema desde etapas tempranas.

- **Sobre la definición de requerimientos:** La especificación inicial de *User Stories* y criterios de aceptación permitió transformar necesidades de usuarios en funcionalidades concretas, proporcionando una guía estructurada para el desarrollo de los siguientes sprints y reduciendo ambigüedades en la planificación técnica.

## Sprint 2 – Desarrollo Frontend

- **Sobre el diseño e implementación de interfaces:** Se concluye que el desarrollo frontend permitió transformar los requerimientos funcionales en interfaces visuales e interactivas alineadas con las necesidades identificadas en el Sprint 1. La implementación de vistas enfocadas en administración, monitoreo, autenticación y gestión de estacionamientos permitió materializar la propuesta conceptual en una experiencia digital tangible.

- **Sobre la experiencia de usuario (UX/UI):** La construcción de componentes visuales, navegación estructurada y organización por roles de usuario permitió priorizar la facilidad de uso y comprensión del sistema. La visualización por zonas, dashboards y componentes reutilizables contribuyeron a mejorar la claridad de la información presentada al usuario final.

- **Sobre la arquitectura frontend:** La modularización de componentes y separación de responsabilidades dentro del frontend permitió mantener un código más organizado, reutilizable y escalable. Esto facilita futuras integraciones con servicios backend, APIs REST y actualizaciones en tiempo real sin comprometer la mantenibilidad del sistema.

- **Sobre el avance funcional del producto:** El Sprint 2 permitió evidenciar un progreso significativo en la construcción del producto mínimo viable (*MVP*), al contar con prototipos funcionales navegables que representan los principales flujos del sistema, los cuales fueron posteriormente conectados con servicios backend reales en el Sprint 3.

## Sprint 3 – Desarrollo Backend

- **Sobre el diseño e implementación de la API REST:** Se concluye que el desarrollo backend permitió transformar los requerimientos funcionales en servicios REST documentados y desplegados, alineados con los bounded contexts definidos en la arquitectura del sistema. La implementación de endpoints para parking, reservas, recibos, suscripciones y detección de spots permitió consolidar la lógica de negocio de SpotGo en una capa de servicios real y consumible.

- **Sobre la documentación de servicios:** La documentación de todos los endpoints mediante OpenAPI/Swagger permitió establecer un contrato claro entre el frontend y el backend, facilitando la integración entre ambas capas y la validación de los flujos de usuario por parte del equipo y los stakeholders. Esto contribuyó a reducir ambigüedades y acelerar el proceso de integración.

- **Sobre la arquitectura backend:** La organización del backend por bounded contexts (Parking, Billing, etc) siguiendo principios de Domain-Driven Design permitió mantener una separación clara de responsabilidades, favoreciendo la escalabilidad y el mantenimiento independiente de cada módulo. El uso de GitFlow con ramas por feature garantizó una integración ordenada y trazable del código.

- **Sobre el avance funcional del producto:** El Sprint 3 permitió reemplazar progresivamente los datos simulados por servicios reales, habilitando flujos end-to-end funcionales tanto para el rol de conductor como para el de administrador. El despliegue del backend en Railway y su integración con el frontend desplegado en Vercel representan un avance significativo hacia un producto completamente funcional.

- **Conclusión general del proyecto:** Finalmente, se concluye que SpotGo cuenta ahora con una arquitectura full-stack operativa, donde el frontend y el backend trabajan de forma integrada sobre una base de datos PostgreSQL en producción. El trabajo desarrollado en los tres sprints permitió validar el problema, estructurar la solución, materializar la experiencia de usuario y consolidar los servicios que la sustentan, estableciendo una base sólida para futuras iteraciones, integraciones IoT y escalamiento del sistema.

## Sprint 4 – Integración IAM y consolidación full-stack

- **Sobre la implementación del módulo IAM:** Se concluye que la incorporación del módulo de Identity and Access Management (IAM) permitió habilitar flujos de autenticación reales en la plataforma, incluyendo el registro de clientes, login con generación de tokens JWT y registro de tenants B2B. Esto representó un avance crítico en la seguridad del sistema, al reemplazar el acceso abierto previo por un esquema de autenticación y autorización basado en roles, gestionado mediante Spring Security en el backend y guards de ruta en el frontend Angular.

- **Sobre la consolidación de endpoints REST pendientes:** El Sprint 4 permitió completar los bounded contexts que habían quedado parcialmente implementados en sprints anteriores, incluyendo la asignación de perfiles Staff, la configuración de zonas de estacionamiento, la gestión de suscripciones B2C y el panel de facturación B2B. Esto consolidó la cobertura funcional de la API REST y garantizó que todos los flujos principales del sistema cuenten con servicios reales documentados en Swagger.

- **Sobre la integración de pagos y confirmación asíncrona:** La integración completa del módulo de pagos digitales mediante Stripe API, incluyendo el endpoint webhook para la confirmación asíncrona de eventos de pago, permitió cerrar el ciclo de cobro de la plataforma tanto para el flujo B2C como para el B2B. Esto habilitó transacciones reales y trazables dentro del sistema, alineadas con los requerimientos de facturación electrónica definidos desde etapas tempranas del proyecto.

- **Sobre la arquitectura y seguridad del sistema:** La incorporación de Spring Security en el backend y la implementación de AuthStore con guards de autenticación en el frontend permitieron establecer una capa de seguridad transversal coherente con la arquitectura DDD adoptada. La separación de roles entre conductor y administrador, gestionada desde el módulo IAM, garantiza que cada usuario acceda únicamente a los recursos y vistas que le corresponden.

- **Conclusión general del proyecto:** Finalmente, se concluye que SpotGo cuenta con una plataforma full-stack completamente integrada, donde el módulo IAM, los servicios REST, el sistema de pagos y el frontend Angular operan de forma cohesionada sobre una base de datos PostgreSQL desplegada en Railway. El trabajo desarrollado a lo largo de los cuatro sprints permitió validar el problema, estructurar la solución, materializar la experiencia de usuario, consolidar los servicios backend y asegurar el acceso mediante autenticación real, estableciendo una base sólida y escalable para futuras integraciones IoT y evolución del producto.
