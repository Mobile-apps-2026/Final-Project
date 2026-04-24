![Logo de la upc](/Assets/imagenes-caratula/logo-upc.png)

# Univeridad Peruana de Ciencias Aplicadas

# Ingeniería de Software

### Periodo: UG-1er Sementre 2026 Pregrado

### Curso: Aplicaciones para Dispositivos Móviles

### NRC: 3646

### Docente: Mayta Guillermo, Jorge Luis

## Informe del Trabajo Final

### Startup: AgroCare

### Producto: Bovix

### Integrantes:

| Codigo     | Apellidos y Nombres                |
|------------|------------------------------------|
| U201611430 | Flores Manrique, Sebastian Enrique |
| U202213553 | De las Casas Latour, Sebastián     | 
| U202310837 | Esquirva León, Miguel Juan Diego   | 
| U201924756 | Inga Hernández, Ayrton Damian      | 
| u202516291 | Meza Tataje, David                 | 

### Abril 2026

---

# Registo de Versiones del Informe

| Versión | Fecha    | Autor                              | Descrición Modificada               |
|---------|----------|------------------------------------|-------------------------------------|
| 0.1     | 12/04/26 | Flores Manrique, Sebastian Enrique | Creación del documento              |
| 0.2     | 14/04/26 | Flores Manrique, Sebastian Enrique | Capitulo 1 añadido                  | 
| 0.3     | 15/04/26 | De las Casas Latour, Sebastián     | capítulo 2, punto 2.1 y 2.3 añadido |
| 0.4     | 16/04/26 | Meza Tataje, David                 | capítulo 2, punto 2.4 añadido       |
| 0.5     | 18/04/26 | Inga Hernández, Ayrton Damian      | capítulo 2, puntoo 2.5 añadido      |
| 0.6     | 19/04/26 | Flores Manrique, Sebastian Enrique | capítulo 2, punto 2.2 y 2.6 añadido |   
| 0.7     | 20/04/26 | Esquirva León, Miguel Juan Diego   | capítulo 2, punto 2.6 añadido       | 

# Project Report Collaboration Insights

- Link del repositorio del informe: [https://github.com/Mobile-apps-2026/Final-Project](https://github.com/Mobile-apps-2026/Final-Project)

A lo largo del proyecto, el equipo ha estado comprometido en la creación del informe en diferentes fases. Las tareas principales que se han abarcado
- La realización de una investigación del negocio y la problemática a resolver, recopilando información relevante de fuentes confiables que nos permitieron comprender mejor el sector y las necesidades de los usuarios.
- La redacción de los capítulos del informe, incluyendo la descripción de la startup, el perfil de la solución, los segmentos objetivo, los competidores, las entrevistas, el needfinding, la especificación de requerimientos y el diseño del producto.

# Contenido

## Tabla de contenidos

* [Capítulo I: Presentación](#capítulo-i-introducción)
    * [1.1. *Startup Profile*](#11-startup-profile)
        * [1.1.1. Descripción del Startup](#111-descripción-del-startup)
        * [1.1.2. Perfiles de integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)
    * [1.2. *Solution Profile*](#12-solution-profile)
        * [1.2.1. Antecedentes y problemática](#121-antecedentes-y-problemática)
        * [1.2.2. Lean UX Process](#122-lean-ux-process)
            * [1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)
            * [1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)
            * [1.2.2.3. Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)
            * [1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)
    * [1.3. *Segmentos objetivos*](#13-segmentos-objetivos)
* [Capítulo II: Requirements Development and Software Solution Design](#capítulo-ii-requirements-development-and-software-solution-design)
    * [2.1. *Competidores*](#21-competidores)
        * [2.1.1. Análisis competitivo](#211-análisis-competitivo)
        * [2.1.2. Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)
    * [2.2. *Entrevistas*](#22-entrevistas)
        * [2.2.1. Diseño de entrevistas](#221-diseño-de-entrevistas)
        * [2.2.2. Registro de entrevistas](#222-registro-de-entrevistas)
        * [2.2.3. Análisis de entrevistas](#223-análisis-de-entrevistas)
    * [2.3. *Needfinding*](#23-needfinding)
        * [2.3.1. User Personas](#231-user-personas)
        * [2.3.2. User Task Matrix](#232-user-task-matrix)
        * [2.3.3. User Journey Mapping](#233-user-journey-mapping)
        * [2.3.4. Empathy Mapping](#234-empathy-mapping)
        * [2.3.5. Big Picture EventStorming](#235-big-picture-eventstorming)
        * [2.3.6. Ubiquitous Language](#236-ubiquitous-language)
    * [2.4. *Requirements specification*](#24-requirements-specification)
        * [2.4.1. User Stories](#241-user-stories)
        * [2.4.2. Impact Mapping](#242-impact-mapping)
        * [2.4.3. Product Backlog](#243-product-backlog)
    * [2.5. *Strategic-Level Domain-Driven Design*](#25-strategic-level-domain-driven-design)
        * [2.5.1. EventStorming](#251-eventstorming)
            * [2.5.1.1. Candidate Context Discovery](#2511-candidate-context-discovery)
            * [2.5.1.2. Domain Message Flows Modeling](#2512-domain-message-flows-modeling)
            * [2.5.1.3. Bounded Context Canvases](#2513-bounded-context-canvases)
        * [2.5.2. Context Mapping](#252-context-mapping)
        * [2.5.3. Software Architecture](#253-software-architecture)
            * [2.5.3.1. Software Architecture Context Level Diagrams](#2531-software-architecture-context-level-diagrams)
            * [2.5.3.2. Software Architecture Container Level Diagrams](#2532-software-architecture-container-level-diagrams)
            * [2.5.3.3. Software Architecture Deployment Diagrams](#2533-software-architecture-deployment-diagrams)
    * [2.6. *Tactical-Level Domain-Driven Design*](#26-tactical-level-domain-driven-design)
        * [2.6.1. Bounded Context: ](#261-bounded-context)
            * [2.6.1.1. Domain Layer](#2611-domain-layer)
            * [2.6.1.2. Interface Layer](#2612-interface-layer)
            * [2.6.1.3. Application Layer](#2613-application-layer)
            * [2.6.1.4. Infrastructure Layer](#2614-infrastructure-layer)
            * [2.6.1.5. Bounded Context Software Architecture Component Level Diagrams](#2615-bounded-context-software-architecture-component-level-diagrams)
            * [2.6.1.6. Bounded Context Software Architecture Code Level Diagrams](#2616-bounded-context-software-architecture-code-level-diagrams)
                * [2.6.1.6.1. Bounded Context Domain Layer Class Diagrams](#26161-bounded-context-domain-layer-class-diagrams)
                * [2.6.1.6.2. Bounded Context Database Design Diagram](#26162-bounded-context-database-design-diagram)
* [Capítulo III: Solution UI/UX Design](#capítulo-iii-solution-uiux-design)
* [Capítulo IV: Product Implementation & Validation](#capítulo-iv-product-implementation--validation)
* [Conclusiones](#conclusiones)

# Student Outcome
**Criterio:** La capacidad de adquirir y aplicar nuevos conocimientos según sea
necesario, utilizando estrategias deaprendizaje apropiadas.

En el siguiente cuadro se describe las accionesrealizadas y enunciados de conclusiones
por parte del grupo, que permiten sustentar el haber alcanzado el logro del ABET –
EAC - Student Outcome 7.

## ABET – EAC – Student Outcome 7

**Criterio:** *La capacidad de adquirir y aplicar nuevos conocimientos según sea necesario, utilizando estrategias de aprendizaje apropiadas.*

En el siguiente cuadro se describe las acciones realizadas y enunciados de conclusiones por parte del grupo, que permiten sustentar el haber alcanzado el logro del ABET – EAC – Student Outcome 7.

| **Criterio específico** | **Acciones realizadas**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | **Conclusiones**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Actualiza conceptos y conocimientos necesarios para su desarrollo profesional y en especial para su proyecto en soluciones de software. | **Flores Manrique, Sebastian Enrique** <br> - AV1: Investigué los fundamentos del Lean UX Process para elaborar los Problem Statements, Assumptions, Hypothesis Statements y el Lean UX Canvas del proyecto Bovix. Adquirí conocimientos sobre la técnica 5W's y 2H's para estructurar el análisis de antecedentes y problemática del sector ganadero peruano. Estudié metodologías de segmentación de mercado para definir los dos segmentos objetivo: productores ganaderos y veterinarios especializados. <br><br> **De las Casas Latour, Sebastián** <br> - AV1: Actualicé mis conocimientos en análisis competitivo para identificar competidores de Bovix y elaborar estrategias y tácticas diferenciadoras. Investigué técnicas de diseño y conducción de entrevistas para el levantamiento de información con usuarios de ambos segmentos objetivo. Estudié herramientas de Needfinding como User Personas, User Task Matrix, User Journey Mapping y Empathy Mapping para comprender las necesidades reales de ganaderos y veterinarios. <br><br> **Esquirva León, Miguel Juan Diego** <br> - AV1: Adquirí conocimientos sobre Big Picture EventStorming y Ubiquitous Language para modelar el dominio del problema ganadero. Investigué la metodología de especificación de requisitos mediante User Stories, Impact Mapping y Product Backlog para estructurar el alcance funcional de Bovix. Estudié los principios del Strategic-Level Domain-Driven Design, incluyendo EventStorming, Candidate Context Discovery, Domain Message Flows y Bounded Context Canvases. <br><br> **Inga Hernández, Ayrton Damian** <br> - AV1: Investigué los fundamentos del modelo C4 para elaborar los diagramas de arquitectura de software a nivel de contexto, contenedor y despliegue. Adquirí conocimientos sobre Context Mapping y las relaciones entre bounded contexts para diseñar la arquitectura estratégica de Bovix. Estudié la arquitectura por capas (Interface, Application, Domain, Infrastructure) dentro del enfoque de Tactical-Level DDD para documentar los bounded contexts Identity and Access Management y Profile Management. <br><br> **Meza Tataje, David** <br> - AV1: Investigué los patrones tácticos de Domain-Driven Design (entidades, value objects, agregados, repositorios, servicios de dominio) para documentar el Domain Layer del bounded context Livestock Management. Adquirí conocimientos sobre el modelo C4 a nivel de componentes para elaborar los diagramas de arquitectura del bounded context. Estudié el diseño de bases de datos relacionales y diagramas UML de clases para representar la persistencia y estructura del dominio ganadero. | AV1: El equipo incorporó un conjunto amplio y diverso de metodologías y herramientas nuevas durante el desarrollo del proyecto Bovix, que abarcaron desde el análisis del dominio del problema (Lean UX, 5W's y 2H's, Needfinding) hasta el diseño arquitectónico de la solución (DDD estratégico y táctico, modelo C4, UML). Cada integrante identificó proactivamente las brechas en su conocimiento y tomó acciones concretas para cubrirlas mediante el estudio de documentación técnica, bibliografía especializada y recursos en línea.                                                                                                                                                                           |
| Reconoce la necesidad del aprendizaje permanente para el desempeño profesional y el desarrollo de proyectos en soluciones de software. | **Flores Manrique, Sebastian Enrique** <br> - AV1: Reconocí que la construcción de una propuesta de valor sólida para Bovix requería comprender a profundidad tanto el contexto del sector ganadero peruano como las metodologías de validación de hipótesis de negocio, lo que me motivó a estudiar Lean UX Process y técnicas de segmentación de usuarios como parte de mi desarrollo profesional. <br><br> **De las Casas Latour, Sebastián** <br> - AV1: Identifiqué que el levantamiento de información con usuarios reales exige el dominio de técnicas de investigación cualitativa como entrevistas estructuradas y herramientas de Needfinding, reconociendo que estas competencias son esenciales para cualquier ingeniero de software que diseñe soluciones centradas en el usuario. <br><br> **Esquirva León, Miguel Juan Diego** <br> - AV1: Comprendí que el modelado del dominio del problema mediante EventStorming y la definición del Ubiquitous Language son prácticas profesionales que requieren actualización constante, ya que permiten alinear al equipo técnico con el negocio y reducir la ambigüedad en el desarrollo de software. Reconocí además que la especificación de requisitos mediante User Stories e Impact Mapping es una habilidad transversal indispensable en proyectos de software modernos. <br><br> **Inga Hernández, Ayrton Damian** <br> - AV1: Reconocí que el diseño de arquitecturas de software escalables y bien documentadas mediante el modelo C4 y los principios de DDD estratégico es una competencia profesional que exige aprendizaje continuo, dado que estas metodologías evolucionan constantemente en la industria del software. Me comprometí a profundizar en Context Mapping y arquitectura de microservicios a lo largo del proyecto. <br><br> **Meza Tataje, David** <br> - AV1: Identifiqué que el diseño táctico de software bajo DDD, incluyendo la documentación de capas, diagramas de clases UML y modelos de base de datos, demanda una actualización permanente de conocimientos de ingeniería de software, y reconocí que esta disciplina es clave para construir sistemas mantenibles, escalables y alineados con las reglas del negocio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | AV1: El equipo reconoce de manera colectiva que el desarrollo de soluciones de software de calidad exige una actitud de aprendizaje permanente y proactivo. A lo largo de esta entrega, cada integrante identificó de forma autónoma las áreas de conocimiento que debía fortalecer, ya sea en análisis de usuarios, modelado de dominio, arquitectura de software o diseño táctico, y tomó acciones concretas para hacerlo. |


# Objetivos SMART

| Integrantes | Objetivos SMART                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| --- |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|Flores Manrique, Sebastian Enrique | - Desarrollar una especialización técnica en un área relevante de la ingeniería de software, como desarrollo backend, frontend o ingeniería de datos, en un periodo de cuatro meses posteriores a la graduación, mediante la culminación de al menos dos cursos certificados y la implementación de un mínimo de dos proyectos aplicados que evidencien el uso de buenas prácticas de desarrollo, patrones de diseño y estándares de calidad.<br><br> -Al finalizar la carrera de Ingeniería de Software, lograr la inserción en el mercado laboral como desarrollador de software junior en un plazo máximo de seis meses, mediante la postulación constante a un promedio de diez ofertas laborales mensuales, el fortalecimiento de un portafolio profesional con al menos tres proyectos completos y documentados, y la preparación sistemática para procesos de selección a través de la práctica regular de entrevistas técnicas y resolución de problemas. |
|De las Casas Latour, Sebastián | - Obtener un certificado de desarrollo móvil dentro de los primeros seis meses después de mi graduación. <br><br> - Desarrollar y pubicar una aplicación móvil en la play store dentro del primer año después de mi graduación. |
|Esquirva León, Miguel Juan Diego | Desarrollar e implementar una solución de software basada en arquitectura de dominio (DDD) y microservicios, integrando los Bounded Contexts de gestión ganadera, salud veterinaria, pagos y notificaciones, antes de finalizar la carrera, evidenciando el uso de buenas prácticas de diseño, separación de responsabilidades y documentación técnica clara.<br><br>- Fortalecer mi perfil profesional para la inserción laboral como desarrollador de software junior, en un plazo máximo de seis meses después de graduarme, mediante la creación de un portafolio con al menos tres proyectos completos y funcionales, la postulación constante a ofertas laborales del sector tecnológico y la preparación continua en entrevistas técnicas y resolución de problemas de ingeniería de software. |
|Inga Hernández, Ayrton Damian| - Especializarme en una tecnología de backend completando al menos 2 cursos certificados y desarrollando 1 proyecto avanzado con arquitectura escalable en un plazo de 10 meses tras mi graduación<br><br>- Construir y mantener un portafolio profesional en línea y un perfil activo en LinkedIn y GitHub, publicando al menos 1 proyecto o mejora mensual durante los primeros 6 meses después de graduarme. |
|Meza Tataje, David |  -Desarrollar y consolidar un portafolio profesional en el área de ingeniería de software antes de finalizar la carrera, mediante la implementación de al menos tres proyectos completos que integren buenas prácticas de desarrollo, control de versiones con Git y documentación técnica en GitHub, evidenciando competencias en desarrollo de software full stack.n<br><br> -Lograr la inserción laboral como desarrollador de software junior en un plazo máximo de seis meses después de la graduación, mediante la postulación constante a oportunidades laborales del sector tecnológico, la preparación continua en entrevistas técnicas y la mejora progresiva del portafolio con proyectos aplicados y funcionales.
