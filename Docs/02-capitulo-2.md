# Capítulo II: Requirements Development and Software Solution Design
Este capítulo presenta el proceso de desarrollo de requerimientos y el diseño de la solución de software para Bovix. Se aborda el análisis competitivo del mercado, el proceso de entrevistas con los segmentos objetivo, el needfinding, la especificación de requerimientos mediante User Stories y Product Backlog, y el diseño arquitectónico de la solución a nivel estratégico y táctico bajo el enfoque de Domain-Driven Design (DDD).
## 2.1. Competidores
En esta sección se analiza el panorama competitivo del mercado de gestión ganadera digital, identificando las principales soluciones existentes y evaluando sus fortalezas, debilidades, oportunidades y amenazas en relación con Bovix. Este análisis permite definir estrategias y tácticas diferenciadas que posicionen a Bovix de manera efectiva en el mercado.
### 2.1.1. Análisis Competitivo 

<table border="1" cellpadding="6" cellspacing="0" style="border-collapse:collapse; width:100%; font-family:Arial, sans-serif;">
  <thead>
    <tr>
      <th colspan="6" scope="col" style="background:#f2f2f2;"><strong>Competitive Analysis Landscape</strong></th>
    </tr>
    <tr>
      <th colspan="2" rowspan="2" scope="row">¿Por qué realizar este análisis?</th>
      <td colspan="4" style="">
        <strong>Escriba en el recuadro la pregunta que busca responder o el objetivo de este análisis.</strong>
      </td>
    </tr>
    <tr>
      <td colspan="4" style="">
        El objetivo del análisis es obtener una perspectiva clara sobre qué brechas estratégicas existen en el mercado que otras soluciones no estén abarcando, obteniendo así un factor diferenciador de nicho que permita posicionar nuestro producto como idóneo para MYPES centradas en el sector agrario.
      </td>
    </tr>
    <tr>
      <th colspan="2" scope="row">(En la cabecera colocar por cada competidor nombre y logo)</th>
      <th scope="column" style="width:20%; text-align:center;">
        Bovix<br>
        <img src="" alt="Bovix logo" style="max-width:100px; display:block; margin:6px auto;">
      </th>
      <th scope="column" style="width:20%; text-align:center;">
        CattleMax<br>
        <img src="..\Assets\cattlemaxlogo.png" alt="competidor 1 logo" style="max-width:100px; display:block; margin:6px auto;">
      </th>
      <th scope="column" style="width:20%; text-align:center;">
        Herdwatch<br>
        <img src="..\Assets\herdwatchlogo.png" alt="competidor 2 logo" style="max-width:100px; display:block; margin:6px auto;">
      </th>
      <th scope="column" style="width:20%; text-align:center;">
        AgriWebb<br>
        <img src="..\Assets\AgriWebblogo.jpg" alt="competidor 3 logo" style="max-width:100px; display:block; margin:6px auto;">
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row" rowspan="2">Perfil</th>
      <th scope="row">Overview</th>
      <td>Startup peruana de tecnología agropecuaria enfocada en digitalizar la gestión ganadera mediante una plataforma móvil y web.</td>
      <td>Software especializado en gestión ganadera con más de 20 años en el mercado, enfocado en registro detallado de datos productivos y reproductivos.</td>
      <td>Aplicación móvil enfocada en facilidad de uso y operación en campo, con fuerte enfoque “mobile-first”.</td>
      <td>Plataforma empresarial para gestión ganadera a gran escala, con enfoque en trazabilidad, cumplimiento y operaciones multi-finca.</td>
    </tr>
    <tr>
      <th scope="row">Ventaja competitiva</th>
      <td>Accesible, simple y adaptada a la realidad rural peruana, combinando bajo costo, funcionamiento en baja conectividad y enfoque local.</td>
      <td>Profundidad y precisión en la gestión de datos ganaderos, especialmente en aspectos reproductivos y genéticos.</td>
      <td>Facilidad de uso en dispositivos móviles, diseñada para registrar información directamente en campo.</td>
      <td>Escalabilidad empresarial y trazabilidad integral, ideal para operaciones ganaderas grandes o multi-finca.</td>
    </tr>
    <tr>
      <th scope="row" rowspan="2">Perfil de Marketing</th>
      <th scope="row">Mercado Objetivo</th>
      <td>Ganaderos pequeños y medianos en Perú y Latinoamérica; Empresas ganaderas en crecimiento (no enterprise)</td>
      <td>Ganaderos medianos y grandes; Operaciones especializadas (genética, reproducción, pedigree)</td>
      <td>Pequeños y medianos ganaderos; Usuarios que priorizan simplicidad y uso en campo</td>
      <td>Empresas ganaderas grandes; Operaciones multi-propiedad; Mercados internacionales</td>
    </tr>
    <tr>
      <th scope="row">Estrategias de Marketing</th>
      <td>Marketing digital móvil-first (Facebook, WhatsApp, TikTok rural); Estrategia freemium para captar usuarios</td>
      <td>Enfoque en precisión técnica y datos avanzados; Marketing dirigido a productores profesionales; Reputación basada en experiencia y confiabilidad (legacy software)</td>
      <td>Diferenciación por facilidad de uso; Enfoque en productividad diaria; Freemium (entrada gratuita para captar usuarios)</td>
      <td>Posicionamiento como solución enterprise; Inversión en expansión global y financiamiento; Enfoque en cumplimiento normativo y escalabilidad </td>
    </tr>
    <tr>
      <th scope="row" rowspan="3">Perfil de Productos</th>
      <th scope="row">Productos y servicios</th>
      <td>Registro de ganado (identificación individual); Historial de salud y tratamientos
Control reproductivo; Gestión de alimentación</td>
      <td>Registro completo del ganado (salud, reproducción, genética); Reportes avanzados y análisis de datos; Gestión de inventario y productividad</td>
      <td>Perfiles individuales de animales; Seguimiento de salud y reproducción; Alertas y recordatorios; Registros financieros básicos</td>
      <td>Gestión integral del ganado; Trazabilidad completa; Reportes avanzados; Integraciones con otros sistemas</td>
    </tr>
    <tr>
      <th scope="row">Precios y costos</th>
      <td>Freemium (versión básica gratuita); Suscripción mensual o anual de bajo costo(menos de 100$)</td>
      <td>Suscripción: $199 – $399/año; Prueba gratuita</td>
      <td>Plan gratuito (limitado); Planes pagados: $119 – $299/año</td>
      <td>Desde $500 hasta $5,000+/año</td>
    </tr>
    <tr>
      <th scope="row">Canales de distribución</th>
      <td>App móvil (Android principalmente); Plataforma web</td>
      <td>Plataforma web (cloud); Venta directa online (SaaS)</td>
      <td>App móvil (Android/iOS); Plataforma web sincronizada (cloud)</td>
      <td>Plataforma web + app móvil; Ventas B2B directas; Implementaciones empresariales</td>
    </tr>
    <tr>
      <th scope="row" rowspan="5">Análisis SWOT</th>
      <th scope="col" colspan="5" style=" text-align:left;">
        Realice esto para su startup y sus competidores. Sus fortalezas deberían apoyar sus oportunidades y contribuir a lo que ustedes definen como su posible ventaja competitiva.
      </th>
    </tr>
    <tr>
      <th scope="row">Fortalezas</th>
      <td>Mobile-first con funcionamiento offline; Bajo costo y accesibilidad; Adaptación al contexto rural latinoamericano; UX simple (rápida adopción)</td>
      <td>Alta precisión y profundidad técnica; Reputación consolidada</td>
      <td>Facilidad de uso (mobile-first); Rápida adopción por pequeños productores</td>
      <td>Escalabilidad y trazabilidad empresarial; Solución robusta para grandes operaciones</td>
    </tr>
    <tr>
      <th scope="row">Debilidades</th>
      <td>Marca nueva y baja confianza inicial; Menor capacidad técnica (analítica avanzada); Recursos limitados (startup)</td>
      <td>Complejidad de uso; Poco adaptado a mercados emergentes</td>
      <td>Funcionalidad limitada; Poca adaptación local en LATAM</td>
      <td>Alto costo; Complejidad de implementación</td>
    </tr>
    <tr>
      <th scope="row">Oportunidades</th>
      <td>Baja digitalización del sector ganadero en Perú/LATAM; Crecimiento de conectividad móvil rural; Necesidad de soluciones accesibles para pequeños productores</td>
      <td>Demanda de análisis avanzado en ganadería especializada</td>
      <td>Crecimiento del uso de apps en campo</td>
      <td>Digitalización de empresas ganaderas grandes</td>
    </tr>
    <tr>
      <th scope="row">Amenazas</th>
      <td>Entrada de soluciones globales al mercado LATAM; Resistencia al cambio tecnológico; Limitaciones económicas del usuario rural</td>
      <td>Soluciones más simples y accesibles</td>
      <td>Apps más completas o adaptadas al contexto</td>
      <td>Soluciones más económicas y simples</td>
    </tr>
  </tbody>
</table>

### 2.1.2. Estrategias y tácticas frente a competidores

**1. Estrategia de Cercanía y Confianza**
Generar confianza inicial mostrando acompañamiento directo y humano, reduciendo la ansiedad tecnológica.

**Tácticas:**
- Ofrecer sesiones 1:1 gratuitas de inducción para cada nuevo cliente.  
- Crear un servicio de soporte vía WhatsApp/Telegram con tiempos de respuesta cortos y lenguaje claro.  

**2. Estrategia de Transparencia y Justicia en Costos**
Posicionar a Bovix como una marca honesta, justa y alineada a la realidad económica de las PYMES.  

**Tácticas:**
- Diseñar un esquema de precios simple y comunicativo (ej. “lo que ves es lo que pagas”).  
- Publicar comparativas abiertas con competidores, destacando dónde Bovix ofrece más valor.  
- Elaborar campañas de comunicación que destaquen el compromiso con la transparencia y el desarrollo local.  

**3. Estrategia de Comunidad y Educación Tecnológica**
Transformar a clientes temerosos en promotores de la digitalización mediante una comunidad activa y educativa.  

**Tácticas:**
- Crear la **Comunidad Bovix PYME Digital** con foros, webinars y espacios de networking.  
- Publicar guías prácticas y casos de éxito de clientes peruanos que usen la plataforma.  
- Organizar eventos híbridos (presenciales + online) para compartir aprendizajes y fomentar la innovación colaborativa.

**4. Estrategia de Adaptación a la Cultura Peruana**
Diferenciar a Bovix al construir una experiencia profundamente conectada con la cultura, idioma y prácticas de negocio locales.  

**Tácticas:**
- Desarrollar contenidos de capacitación con ejemplos y casos de uso de sectores típicos peruanos.  
- Usar un lenguaje cercano en la interfaz y la comunicación (ej. mensajes amigables, expresiones familiares al emprendedor peruano).   
- Generar alianzas con instituciones peruanas (SUNAT, PRODUCE, municipalidades) para reforzar el cumplimiento normativo y la identidad local.  

## 2.2. Entrevistas
En esta sección se documenta el proceso de entrevistas realizadas con representantes de los dos segmentos objetivo: productores ganaderos y veterinarios especializados. El objetivo fue comprender sus necesidades, rutinas de trabajo, puntos de dolor y expectativas frente a una solución digital de gestión ganadera. Los hallazgos obtenidos son la base del proceso de Needfinding desarrollado en la sección siguiente.
### 2.2.1. Diseño de entrevistas

### Segmento #1: Productores Ganaderos (Independientes y Empresariales)

Bovix ha desarrollado preguntas específicas para conocer las necesidades, experiencias y expectativas de los productores ganaderos, tanto independientes como empresariales. Buscamos ayudarlos a gestionar mejor sus operaciones, optimizar el cuidado de sus animales y evaluar su impacto productivo y comercial. A través de una plataforma intuitiva, Bovix ofrece herramientas que mejoran la eficiencia, el control sanitario y la toma de decisiones, simplificando los procesos diarios del productor y mejorando la calidad de su ganadería.

**Preguntas para las entrevistas:**

1. ¿Cuántos animales maneja actualmente su empresa y cómo varía esa cantidad durante el año?
2. Si su empresa tuviera acceso a una plataforma digital para gestión ganadera, ¿qué funciones considera imprescindibles para mejorar la eficiencia?
3. ¿Cuáles son los mayores retos que enfrentan en la gestión ganadera a gran escala y cómo los abordan hoy en día?
4. ¿Qué tipo de información o datos son clave para la toma de decisiones en su operación ganadera?
5. ¿Qué funcionalidades le gustaría tener para facilitar la gestión del personal y la planificación de tareas?
6. ¿Qué tipo de informes o análisis considera importantes para evaluar el desempeño de su empresa?
7. ¿Cómo le gustaría interactuar con proveedores y socios comerciales a través de una plataforma como VacApp?
8. ¿Qué tan importante es que una aplicación como VacApp se adapte a los procesos actuales de su empresa?
9. ¿Qué aspectos considera que deberían ser completamente personalizables dentro de la plataforma?
10. ¿Qué mejoras espera obtener al integrar una solución como VacApp en su operación ganadera?

### Segmento #2: Veterinarios Especializados

Bovix ha formulado un conjunto de preguntas orientadas a comprender los métodos de trabajo, los desafíos de campo y las necesidades técnicas de los veterinarios especializados. Nuestro propósito es facilitarles la gestión del historial clínico, el seguimiento reproductivo y el control de tratamientos en los diferentes rebaños que atienden. Mediante una herramienta digital integrada, Bovix busca agilizar el registro de diagnósticos y optimizar la comunicación directa con los productores, permitiendo a los profesionales brindar un servicio médico más eficiente, preciso y organizado.

**Preguntas para las entrevistas:**

1. ¿Cómo registra y gestiona los historiales clínicos de los animales que atiende? (Perfil y tareas)
2. ¿Qué información le suele faltar al llegar a una ganadería para dar un diagnóstico? (Puntos de dolor)
3. ¿Cómo se comunica y coordina habitualmente con los productores ganaderos? (Hábitos)
4. ¿Qué datos previos del animal considera obligatorios antes de su evaluación? (Necesidades)
5. ¿Cómo lleva el control de las vacunas y desparasitaciones de sus clientes? (Tareas y herramientas actuales)
6. ¿Qué problemas enfrenta para anotar datos durante el trabajo de campo o sin internet? (Frustraciones técnicas)
7. ¿En qué le ayudaría compartir información médica en tiempo real con el productor? (Expectativas)
8. ¿Qué tres funciones serían indispensables para usted en una app veterinaria? (Necesidades funcionales)
9. ¿Cómo le resultaría más fácil entregar y controlar las recetas médicas o indicaciones? (Usabilidad)
10. ¿Cuál sería el mayor beneficio para su trabajo al usar una plataforma como Bovix? (Metas/Objetivos)

### 2.2.2. Registro de entrevistas

### Segmento #1: Productores Ganaderos (Independientes y Empresariales)

### Entrevista 1
**Entrevistado:** Ximena Flores Manrique

**Edad:** 22 años

**Distrito:** Villa María del Triunfo

<img src="../Assets/entrevista-ganadero1.png" alt="entrevista-ganadero1" width="50%">

**Minuto de inicio:** 00:01

**Link de la entrevista:**  [Entrevista](https://acortar.link/LGQIqe)

**Resumen de la entrevista:**

La entrevista revela que Ximena, de 22 años y residente de Villa María, gestiona su granja con un enfoque metódico, pragmático y orientado a resultados, apoyándose fuertemente en el criterio de veterinarios para establecer planes de bioseguridad, vacunación y alimentación que prevengan pérdidas económicas por enfermedades. Actualmente, lleva sus registros de forma manual o en hojas de cálculo, pero busca dar el salto a una aplicación multiplataforma que pueda consultar tanto en campo desde su iPhone como en su laptop Windows a través de Google Chrome. Ella espera que esta herramienta tecnológica le permita automatizar cronogramas, sugerir el uso de medicamentos, controlar el balance financiero y crear fichas individuales para cada animal desde su nacimiento, facilitando así la dosificación exacta de alimento según su etapa de crecimiento y permitiéndole tomar decisiones rápidas y precisas para optimizar su negocio.

### Entrevista 2
**Entrevistado:** Sandro Dincla

**Edad:** 18 años

**Distrito:**

<img src="../Assets/entrevista-ganadero2.png" alt="entrevista-ganadero1" width="50%">

**Minuto de inicio:** 03:25

**Link de la entrevista:**  [Entrevista](https://acortar.link/LGQIqe)

**Resumen de la entrevista:**

La entrevista realizada a Sandro Dincla, de 18 años, revela que participa en la gestión de la granja familiar de aves y cerdos con un enfoque práctico y flexible. Aunque se apoya en veterinarios externos para el cuidado de la salud animal y en mercados locales para la compra de alimentos diferenciados por especie, Sandro lleva actualmente un registro netamente manual en cuadernos sobre las fechas de vacunación y pesaje. Él considera que este método tradicional es su mayor desafío operativo, ya que le genera una importante pérdida de tiempo al realizar el conteo de los animales y buscar información específica en papel. Al realizar la entrevista de forma remota a través de una plataforma de videollamada —lo que demuestra su familiaridad con canales de interacción digitales utilizando una computadora o laptop con cámara, micrófono y navegador web—, expresa su deseo de optimizar sus procesos mediante una aplicación móvil que destaque por su usabilidad y falta de complejidad. Para él, la solución tecnológica ideal debe incluir recordatorios automatizados para vacunas y pesajes, un directorio con números de especialistas (veterinarios y proveedores) siempre disponible para emergencias, y un módulo de alimentación que, si bien le sugiera raciones por animal, le otorgue el control manual para ajustar las cantidades basándose en su propio criterio.

### Entrevista 3
**Entrevistado:** Fernando Valencia

**Edad:** 18 años

**Distrito:** Pueblo Libre

<!-- Aqui colocan un screeshot de la entrevista -->

**Minuto de inicio:** 06:51

**Link de la entrevista:** [Entrevista](https://acortar.link/LGQIqe)


### Segmento #2: Veterinarios Especializados

### Entrevista 1
**Entrevistado:** Johan Bottger

**Edad:** 21

**Distrito:** San Borja

<img src="..\Assets\Captura de pantalla de entrevista 1 vet.png" alt="entrevista-veterinario1" width="50%">

**Minuto de inicio:** 14:22

**Link de la entrevista:** [Entrevista](https://acortar.link/LGQIqe)

**Resumen de la entrevista:**
En la entrevista se muestra como Johan, practicante en una veterianria especializada en el campo, explica cómo lleva a cabo su trabajo. Las dificultades que más suele encontrar son la falta de información clave al momento del diagnóstico, como antecedentes médicos, vacunaciones o cambios en la alimentación. A esto se suma una comunicación poco estructurada con los ganaderos, generalmente a través de aplicaciones de mensajería, donde la información puede perderse o no quedar registrada adecuadamente. El trabajo en zonas rurales presenta además limitaciones técnicas, como la falta de conexión a internet y condiciones adversas que dificultan el registro de datos en tiempo real. Esto impacta directamente en la eficiencia y precisión del servicio. Frente a este contexto, el veterinario valora altamente una solución digital que permita registrar información de manera offline, centralizar historiales clínicos, automatizar el control de tratamientos y mejorar la comunicación con los productores. También considera clave poder compartir indicaciones médicas de forma clara y accesible.

### Entrevista 2
**Entrevistado:** Ricardo Salazar

**Edad:** 25

**Distrito:** Jesus Maria

<img src="..\Assets\entrevista_miniatura_entrevista-2.png" alt="-" width="50%">

<!-- Aqui colocan un screeshot de la entrevista -->

**Minuto de inicio:** 21:03

**Link de la entrevista:** [Entrevista](https://acortar.link/LGQIqe)

**Resumen de la entrevista:**
En la entrevista, Ricardo Salazar, veterinario con 5 años de experiencia, describe cómo realiza su trabajo en el campo. Utiliza cuadernos para anotar en campo y luego traslada la información a Excel para mantener un registro ordenado. También guarda fotos y notas en su celular. Las dificultades principales que enfrenta incluyen la falta de historial clínico completo en las ganaderías, especialmente en datos sobre vacunas y tratamientos previos, lo que dificulta un control efectivo y diagnóstico preciso. La comunicación con los ganaderos se realiza principalmente por llamadas y WhatsApp, con poca frecuencia por correo electrónico, y las visitas se coordinan según la urgencia. En las zonas rurales, la falta de señal y la necesidad de atender solo a los animales complican el registro rápido de datos. Ricardo valora mucho una aplicación veterinaria que permita registrar el historial clínico, controlar vacunas y operar sin conexión a internet para facilitar su trabajo. Prefiere enviar recetas e indicaciones médicas de forma digital, aunque en algunos casos se requieren formatos físicos por la edad de algunos usuarios. Finalmente, destaca que el uso de una plataforma como Bobix ahorra tiempo, organiza mejor la información y permite ofrecer un servicio más preciso a los productores.  


### Entrevista 3
**Entrevistado:** Alonso Medina

**Edad:** 37

**Distrito:** Surco

<!-- Aqui colocan un screeshot de la entrevista -->

**Minuto de inicio:** 26:00

**Link de la entrevista:** [Entrevista](https://acortar.link/LGQIqe)

### 2.2.3. Análisis de entrevistas

## 2.3. Needfinding
En esta sección se consolida el análisis de las necesidades de los usuarios a partir de la información recopilada en las entrevistas. Se presentan los User Personas, el User Task Matrix, el User Journey Mapping, el Empathy Mapping, el Big Picture EventStorming y el Ubiquitous Language del dominio, herramientas que permiten construir una comprensión profunda del contexto y las motivaciones de los usuarios de Bovix.
### 2.3.1. User Personas 
Los user persona que se muestran a continuación, fueron realizados a partir de la información recopilada de la sección de entrevistas. Estos nos ayudarán a describir de forma general nuestro segmento objetivo.

- Productores Ganaderos

<img src="..\Assets\User Persona 1.png">

<div style="page-break-after: always;"/>


- Veterinarios Especializados

<img src="..\Assets\User Persona 2.png">

### 2.3.2. User Task Matrix

En esta sección se presenta el user task matrix de los segmentos objetivos, con el fin de indentificar la frecuencia de las actividades realizadas por los usuarios, y de esta manera se refleja la importancia de determinadas tareas.

<table>
    <thead>
        <tr>
            <th>Task</th>
            <th colspan="2">Productores Ganaderos</th>
            <th colspan="2">Veterinarios Especializados</th>
        </tr>
        <tr>
            <th></th>
            <th>Frecuencia</th>
            <th>Importancia</th>
            <th>Frecuencia</th>
            <th>Importancia</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Registrar información del ganado</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Media</td>
            <td>Media</td>
        </tr>
        <tr>
            <td>Monitorear salud de los animales</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Alta</td>
        </tr>
        <tr>
            <td>Detectar enfermedades o anomalías</td>
            <td>Media</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Alta</td>
        </tr>
        <tr>
            <td>Coordinar atención veterinaria</td>
            <td>Media</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Alta</td>
        </tr>
        <tr>
            <td>Administrar tratamientos médicos</td>
            <td>Media</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Alta</td>
        </tr>
        <tr>
            <td>Gestionar alimentación del ganado</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Baja</td>
            <td>Media</td>
        </tr>
        <tr>
            <td>Controlar reproducción (monta, parto)</td>
            <td>Media</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Alta</td>
        </tr>
        <tr>
            <td>Evaluar productividad (leche/carne)</td>
            <td>Media</td>
            <td>Alta</td>
            <td>Media</td>
            <td>Media</td>
        </tr>
        <tr>
            <td>Organizar registros e historial</td>
            <td>Media</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Alta</td>
        </tr>
        <tr>
            <td>Tomar decisiones operativas</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Alta</td>
            <td>Alta</td>
        </tr>
        <tr>
            <td>Coordinar personal o actividades</td>
            <td>Baja</td>
            <td>Media</td>
            <td>Baja</td>
            <td>Media</td>
        </tr>
        <tr>
            <td>Gestionar múltiples clientes/animales</td>
            <td>Baja</td>
            <td>Media</td>
            <td>Alta</td>
            <td>Alta</td>
        </tr>
    </tbody>
</table>

En base al User Task Matrix presentado, podemos destacar las siguientes tareas con mayor frecuencia e importancia para cada segmento de usuarios:

### Productores Ganaderos:
- Gestionar alimentación	
    - Explicación: La alimentación es la tarea sobre la que más control tienen los productores ganaderos.
- Tomar decisiones operativas	
    - Explicación: La toma de decisiones en muy importante ya que estas afectan al desenvolvimiento del negocio.
### Veterinarios Especializados:
- Monitorear salud de los animales
    - Explicación: Resulta una prioridad para los veterinarios tener un seguimiento del estado de los animales que atienden.
- Administrar tratamientos
    - Explicación: La administración adecuade de los tratamientos es vital paara asegurar el bienestar del animal.

### 2.3.3. User Journey Mapping
En esta sección se presentan los User Journey Mapping de los segmentos objetivos, que realizamos con el fin de dar a entender cómo se siente nuestro usuario en este momento, detallando cada paso que realiza y las emociones que experimenta.

- Productores Ganaderos

<img src="..\Assets\Customer journey map 1.png">

- Veterinarios Especializados

<img src="..\Assets\Customer journey map 2.png">

### 2.3.4. Empathy Mapping
En esta sección mostramos los empathy mapping de los segmentos objetivos realizados con la información recopilada de componentes anteriores.

- Productores Ganaderos

<img src="..\Assets\Empathy map 1.png">

- Veterinarios Especializados

<img src="..\Assets\Empathy map 2.png">

### 2.3.5. Big Picture EventStorming
A continuación se presenta el Big Picture EventStorming del dominio de Bovix, elaborado con el fin de modelar de forma colaborativa los principales eventos de negocio que ocurren en el sistema. Este artefacto permitió al equipo identificar los flujos clave de la gestión ganadera y veterinaria, así como detectar los límites naturales entre los diferentes contextos del dominio, sentando las bases para la definición de los Bounded Contexts.

<img src="..\Assets\Big Picture Eventstorming.jpg">

### 2.3.6. Ubiquitous Language

-**Animal Health (Salud animal):** Estado físico y fisiológico del ganado, que incluye la prevención, diagnóstico y tratamiento de enfermedades para asegurar su bienestar y productividad.

-**Breeding (Reproducción):** Proceso de cría de animales con el objetivo de mejorar características genéticas, aumentar la productividad y mantener la sostenibilidad del hato.

-**Calving (Parto bovino)** Proceso mediante el cual una vaca da a luz a un ternero, evento clave para el ciclo productivo del ganado.

-**Cattle (Ganado bovino)** Conjunto de animales de la especie bovina criados para la producción de carne, leche u otros productos derivados.

-**Disease Prevention (Prevención de enfermedades)** Conjunto de prácticas orientadas a evitar la aparición de enfermedades en el ganado, incluyendo vacunación, control sanitario y manejo adecuado.

-**Feed Management (Gestión de alimentación)** Planificación, control y suministro de alimentos al ganado para asegurar su nutrición adecuada y maximizar su rendimiento productivo.

-**Herd (Hato / Rebaño)** Grupo de animales de una misma especie que son gestionados como una unidad dentro de una explotación ganadera.

-**Herd Management (Gestión del hato)** Conjunto de actividades relacionadas con el control, monitoreo y optimización del ganado, incluyendo salud, reproducción, alimentación y productividad.

-**Livestock (Ganado)** Término general que engloba a los animales criados para fines productivos, como bovinos, ovinos, caprinos, entre otros.

-**Productivity (Productividad)** Medida del rendimiento del ganado en términos de producción de carne, leche u otros productos, en relación con los recursos utilizados.

-**Traceability (Trazabilidad)** Capacidad de rastrear la historia, ubicación y estado de un animal a lo largo de su vida productiva.

-**Vaccination (Vacunación)** Administración de vacunas para prevenir enfermedades y fortalecer el sistema inmunológico del ganado.

-**Veterinary Care (Atención veterinaria)** Servicios profesionales destinados al diagnóstico, tratamiento y prevención de enfermedades en animales.

-**Animal Welfare (Bienestar animal)** Condición en la que el animal se encuentra sano, cómodo, bien alimentado y libre de sufrimiento innecesario.

-**Farm (Explotación ganadera)** Unidad productiva donde se cría y gestiona el ganado para fines comerciales o de subsistencia.

-**Livestock Monitoring (Monitoreo del ganado)** Seguimiento continuo del estado de los animales, incluyendo salud, ubicación, comportamiento y productividad.

-**Weight Gain (Ganancia de peso)** Incremento del peso corporal del animal en un periodo determinado, indicador clave de su crecimiento y alimentación.

## 2.4. Requirements specification
En esta sección se formaliza la especificación de requerimientos del sistema Bovix. Se definen las User Stories organizadas por épicas, el Impact Mapping de los principales objetivos de negocio, y el Product Backlog priorizado. Estos artefactos constituyen la guía para el desarrollo iterativo e incremental del producto.
### 2.4.1. User Stories
Los User Stories representan una herramienta fundamental dentro de las metodologías ágiles para capturar los
requerimientos funcionales desde la perspectiva del usuario. Cada historia describe una necesidad concreta, quién la
necesita y con qué propósito, facilitando la planificación, priorización y desarrollo iterativo del sistema. Esta técnica
garantiza que cada funcionalidad responda a una necesidad real, fomentando un desarrollo orientado al valor y
alineado con las expectativas del usuario final.

<!-- ======================= EP001 ======================= -->

<h2>EP001 — Informarse sobre el Producto</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">
  <tr>
    <th>Epic ID</th>
    <th>Título</th>
    <th>Descripción</th>
  </tr>

  <tr>
    <td>EP001</td>
    <td>Informarse sobre el Producto</td>
    <td>
      Como visitante, deseo explorar la landing page de Bovix para conocer las funcionalidades,
      beneficios y servicios que ofrece la plataforma para la gestión ganadera.
    </td>
  </tr>
</table>

<br>

<!-- ======================= US001 ======================= -->

<h3>US001</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US001</td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP001</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Explorar Landing Page</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como visitante, quiero explorar la landing page para conocer las funcionalidades,
      características y beneficios que ofrece Bovix.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Visualización de contenido principal</b><br>
      Dado que el visitante accede a la landing page.<br>
      Cuando navega por las diferentes secciones.<br>
      Entonces el sistema muestra información clara y organizada sobre Bovix.<br><br>

  <b>E02: Navegación responsiva</b><br>
      Dado que el visitante utiliza distintos dispositivos.<br>
      Cuando accede a la landing page.<br>
      Entonces el contenido se adapta correctamente al tamaño de pantalla.<br><br>

  <b>E03: Navegación entre secciones</b><br>
      Dado que el visitante interactúa con el menú de navegación.<br>
      Cuando selecciona una sección específica.<br>
      Entonces el sistema desplaza correctamente hacia la sección correspondiente.

  </td>
  </tr>

</table>

<br>

<!-- ======================= US002 ======================= -->

<h3>US002</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US002</td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP001</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Visualización de Funcionalidades y Servicios</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como visitante, quiero visualizar las funcionalidades y servicios de Bovix
      para comprender cómo la plataforma puede ayudar en la gestión ganadera.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Visualización de funcionalidades</b><br>
      Dado que el visitante accede a la sección de funcionalidades.<br>
      Cuando revisa el contenido disponible.<br>
      Entonces el sistema muestra información detallada sobre los servicios de Bovix.<br><br>

  <b>E02: Información organizada</b><br>
      Dado que el visitante navega por la sección informativa.<br>
      Cuando consulta las funcionalidades del sistema.<br>
      Entonces el contenido se presenta de manera clara y estructurada.

  </td>
  </tr>

</table>

<br>

<!-- ======================= US003 ======================= -->

<h3>US003</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US003</td>
    <td>Visitante</td>
    <td>Media</td>
    <td>EP001</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Contacto con Bovix</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como visitante, quiero acceder a información de contacto para comunicarme
      con el equipo de Bovix y resolver dudas sobre la plataforma.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">
    <b>E01: Visualización de información de contacto</b><br>
      Dado que el visitante accede a la sección de contacto.<br>
      Cuando revisa la información disponible.<br>
      Entonces el sistema muestra medios de comunicación válidos.<br><br>
    <b>E02: Envío de formulario de contacto</b><br>
      Dado que el visitante completa el formulario de contacto.<br>
      Cuando envía información válida.<br>
      Entonces el sistema confirma correctamente el envío del mensaje.

   </td>
  </tr>

</table>

<br><br>

<!-- ======================= TS001 ======================= -->

<h2>TS001 — Implementación de Landing Page</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS001</td>
    <td>Developer</td>
    <td>Alta</td>
    <td>EP001</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Desarrollo de Landing Page Responsiva</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar la landing page responsiva de Bovix
      para mostrar información del producto y permitir la navegación entre secciones.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">
    <b>E01: Implementación de estructura visual</b><br>
      Dado que el desarrollo de la landing page ha iniciado.<br>
      Cuando se implementan las secciones principales.<br>
      Entonces el sistema muestra correctamente el contenido visual del producto.<br><br>
    <b>E02: Adaptación responsive</b><br>
      Dado que la landing page es visualizada en distintos dispositivos.<br>
      Cuando el usuario accede desde móvil, tablet o desktop.<br>
      Entonces el diseño se adapta correctamente.<br><br>
    <b>E03: Navegación funcional</b><br>
      Dado que el menú de navegación está implementado.<br>
      Cuando el usuario selecciona una opción.<br>
      Entonces el sistema dirige correctamente a la sección correspondiente.
    </td>
  </tr>

</table>

<br>

<!-- ======================= TS002 ======================= -->

<h2>TS002 — Implementación de Formulario de Contacto</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS002</td>
    <td>Developer</td>
    <td>Media</td>
    <td>EP001</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Desarrollo de Formulario de Contacto</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar el formulario de contacto
      para permitir que los visitantes envíen consultas al equipo de Bovix.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Validación de campos</b><br>
      Dado que el visitante completa el formulario.<br>
      Cuando omite campos obligatorios.<br>
      Entonces el sistema muestra mensajes de validación.<br><br>

  <b>E02: Envío exitoso</b><br>
      Dado que el visitante ingresa información válida.<br>
      Cuando envía el formulario.<br>
      Entonces el sistema confirma correctamente el envío del mensaje.

  </td>
  </tr>

</table>


<!-- ======================= EP002 ======================= -->

<h2>EP002 — Gestión de Acceso y Autenticación</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Epic ID</th>
    <th>Título</th>
    <th>Descripción</th>
  </tr>

  <tr>
    <td>EP002</td>
    <td>Gestión de Acceso y Autenticación</td>
    <td>
      Como ganadero, deseo registrarme e iniciar sesión en la plataforma Bovix
      para acceder de manera segura a las funcionalidades del sistema.
    </td>
  </tr>

</table>

<br>

<!-- ======================= US004 ======================= -->

<h3>US004</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US004</td>
    <td>Ganadero</td>
    <td>Alta</td>
    <td>EP002</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Registro de Usuario</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero crear una cuenta en Bovix
      para acceder a las funcionalidades de gestión ganadera.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Registro exitoso</b><br>
      Dado que el ganadero completa correctamente el formulario de registro.<br>
      Cuando envía la información solicitada.<br>
      Entonces el sistema crea la cuenta correctamente.<br><br>

  <b>E02: Campos obligatorios incompletos</b><br>
      Dado que el usuario intenta registrarse.<br>
      Cuando omite información obligatoria.<br>
      Entonces el sistema muestra mensajes de validación.<br><br>

  <b>E03: Correo electrónico inválido</b><br>
      Dado que el usuario ingresa un correo incorrecto.<br>
      Cuando intenta completar el registro.<br>
      Entonces el sistema rechaza la operación y muestra un mensaje de error.

   </td>
  </tr>

</table>

<br>

<!-- ======================= US005 ======================= -->

<h3>US005</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US005</td>
    <td>Ganadero</td>
    <td>Alta</td>
    <td>EP002</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Inicio de Sesión</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero iniciar sesión en la plataforma
      para acceder a mi información y funcionalidades personalizadas.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Inicio de sesión exitoso</b><br>
      Dado que el usuario posee una cuenta registrada.<br>
      Cuando ingresa credenciales válidas.<br>
      Entonces el sistema permite el acceso correctamente.<br><br>

   <b>E02: Credenciales incorrectas</b><br>
      Dado que el usuario intenta iniciar sesión.<br>
      Cuando ingresa datos inválidos.<br>
      Entonces el sistema muestra un mensaje de error.<br><br>

   <b>E03: Persistencia de sesión</b><br>
      Dado que el usuario inicia sesión correctamente.<br>
      Cuando navega por la aplicación.<br>
      Entonces el sistema mantiene activa la sesión del usuario.

   </td>
  </tr>

</table>

<br>

<!-- ======================= US006 ======================= -->

<h3>US006</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US006</td>
    <td>Ganadero</td>
    <td>Media</td>
    <td>EP002</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Cerrar Sesión</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero cerrar sesión de manera segura
      para proteger la información de mi cuenta.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Cierre de sesión exitoso</b><br>
      Dado que el usuario mantiene una sesión activa.<br>
      Cuando selecciona la opción de cerrar sesión.<br>
      Entonces el sistema finaliza correctamente la sesión.<br><br>

   <b>E02: Redirección posterior</b><br>
      Dado que el usuario cerró sesión correctamente.<br>
      Cuando finaliza el proceso.<br>
      Entonces el sistema redirige a la pantalla principal o login.

  </td>
  </tr>

</table>

<br><br>

<!-- ======================= TS003 ======================= -->

<h2>TS003 — Implementación de Registro de Usuarios</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS003</td>
    <td>Developer</td>
    <td>Alta</td>
    <td>EP002</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">API de Registro de Usuarios</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar el endpoint de registro
      para permitir la creación segura de cuentas de usuario.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

   <b>E01: Registro exitoso mediante API</b><br>
      Dado que el endpoint de registro está disponible.<br>
      Cuando se envía información válida.<br>
      Entonces el sistema retorna una respuesta exitosa.<br><br>

  <b>E02: Validación de datos</b><br>
      Dado que el usuario envía información incompleta o inválida.<br>
      Cuando el sistema procesa la solicitud.<br>
      Entonces el endpoint rechaza la operación y muestra errores de validación.<br><br>

  <b>E03: Seguridad de contraseña</b><br>
      Dado que el usuario crea una cuenta.<br>
      Cuando la contraseña es almacenada.<br>
      Entonces el sistema aplica hash de seguridad antes de persistirla.

   </td>
  </tr>

</table>

<br>

<!-- ======================= TS004 ======================= -->

<h2>TS004 — Implementación de Autenticación JWT</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS004</td>
    <td>Developer</td>
    <td>Alta</td>
    <td>EP002</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Sistema de Autenticación JWT</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar autenticación basada en JWT
      para gestionar sesiones seguras dentro de Bovix.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

   <b>E01: Generación de token</b><br>
      Dado que el usuario inicia sesión correctamente.<br>
      Cuando el sistema valida las credenciales.<br>
      Entonces se genera un token JWT válido.<br><br>

  <b>E02: Validación de sesión</b><br>
      Dado que el usuario realiza solicitudes autenticadas.<br>
      Cuando el token JWT es válido.<br>
      Entonces el sistema permite el acceso a los recursos protegidos.<br><br>

  <b>E03: Rechazo de token inválido</b><br>
      Dado que el usuario utiliza un token inválido o expirado.<br>
      Cuando intenta acceder a recursos protegidos.<br>
      Entonces el sistema rechaza la solicitud.

  </td>
  </tr>

</table>
<br><br>

<!-- ======================= EP003 ======================= -->

<h2>EP003 — Gestión de Ganado</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Epic ID</th>
    <th>Título</th>
    <th>Descripción</th>
  </tr>

  <tr>
    <td>EP003</td>
    <td>Gestión de Ganado</td>
    <td>
      Como ganadero, deseo registrar y administrar la información de mis animales
      para mantener un control organizado y actualizado del ganado.
    </td>
  </tr>

</table>

<br>

<!-- ======================= US007 ======================= -->

<h3>US007</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US007</td>
    <td>Ganadero</td>
    <td>Alta</td>
    <td>EP003</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Registro de Ganado</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero registrar nuevos animales
      para mantener actualizado el inventario de mi ganado.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Registro exitoso de animal</b><br>
      Dado que el ganadero accede al formulario de registro.<br>
      Cuando ingresa correctamente los datos del animal.<br>
      Entonces el sistema almacena la información exitosamente.<br><br>

   <b>E02: Validación de campos obligatorios</b><br>
      Dado que el usuario intenta registrar un animal.<br>
      Cuando omite campos requeridos.<br>
      Entonces el sistema muestra mensajes de validación.<br><br>

   <b>E03: Registro inválido</b><br>
      Dado que el usuario ingresa datos incorrectos.<br>
      Cuando envía el formulario.<br>
      Entonces el sistema rechaza el registro y muestra un mensaje de error.

   </td>
  </tr>

</table>

<br>

<!-- ======================= US008 ======================= -->

<h3>US008</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US008</td>
    <td>Ganadero</td>
    <td>Alta</td>
    <td>EP003</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Consulta de Información del Ganado</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero consultar la información de mis animales
      para acceder rápidamente a sus datos registrados.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Consulta exitosa</b><br>
      Dado que existen animales registrados.<br>
      Cuando el ganadero realiza una búsqueda válida.<br>
      Entonces el sistema muestra la información correspondiente.<br><br>

   <b>E02: Búsqueda sin resultados</b><br>
      Dado que el usuario realiza una búsqueda.<br>
      Cuando no existen coincidencias registradas.<br>
      Entonces el sistema informa que no se encontraron resultados.

   </td>
  </tr>

</table>

<br>

<!-- ======================= US009 ======================= -->

<h3>US009</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US009</td>
    <td>Ganadero</td>
    <td>Media</td>
    <td>EP003</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Actualización de Información del Ganado</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero actualizar la información de mis animales
      para mantener datos precisos y actualizados dentro del sistema.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Actualización exitosa</b><br>
      Dado que el animal existe en el sistema.<br>
      Cuando el usuario modifica correctamente la información.<br>
      Entonces el sistema actualiza los datos exitosamente.<br><br>

  <b>E02: Validación de datos</b><br>
      Dado que el usuario edita información del animal.<br>
      Cuando ingresa datos inválidos.<br>
      Entonces el sistema rechaza la operación y muestra un mensaje de error.

  </td>
  </tr>

</table>

<br>

<!-- ======================= US010 ======================= -->

<h3>US010</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US010</td>
    <td>Ganadero</td>
    <td>Media</td>
    <td>EP003</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Gestión de Lotes de Ganado</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero organizar mis animales en lotes
      para administrar de manera más eficiente mi ganado.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Creación de lote</b><br>
      Dado que el usuario accede al módulo de lotes.<br>
      Cuando registra información válida del lote.<br>
      Entonces el sistema crea correctamente el lote.<br><br>

   <b>E02: Asignación de animales</b><br>
      Dado que existen animales registrados.<br>
      Cuando el usuario asigna animales a un lote.<br>
      Entonces el sistema actualiza correctamente la información del lote.

   </td>
  </tr>

</table>

<br><br>

<!-- ======================= TS005 ======================= -->

<h2>TS005 — API de Registro de Ganado</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS005</td>
    <td>Developer</td>
    <td>Alta</td>
    <td>EP003</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Implementación de Endpoint para Registro de Ganado</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar el endpoint de registro de animales
      para almacenar la información del ganado dentro de la plataforma.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Registro exitoso mediante API</b><br>
      Dado que el endpoint se encuentra disponible.<br>
      Cuando se envían datos válidos del animal.<br>
      Entonces el sistema retorna una respuesta exitosa.<br><br>

   <b>E02: Validación de datos</b><br>
      Dado que se reciben datos inválidos.<br>
      Cuando el sistema procesa la solicitud.<br>
      Entonces el endpoint rechaza la operación con un mensaje de error.<br><br>

   <b>E03: Persistencia de información</b><br>
      Dado que el registro es válido.<br>
      Cuando la operación finaliza.<br>
      Entonces el sistema almacena correctamente la información en la base de datos.

  </td>
  </tr>

</table>

<br>

<!-- ======================= TS006 ======================= -->

<h2>TS006 — API de Consulta y Actualización de Ganado</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS006</td>
    <td>Developer</td>
    <td>Alta</td>
    <td>EP003</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Implementación de Endpoints de Consulta y Edición</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar endpoints de consulta y actualización
      para gestionar la información registrada del ganado.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Consulta de información</b><br>
      Dado que existen animales registrados.<br>
      Cuando el usuario realiza una solicitud GET válida.<br>
      Entonces el sistema devuelve la información correspondiente.<br><br>

   <b>E02: Actualización de registros</b><br>
      Dado que el animal existe en el sistema.<br>
      Cuando el usuario envía información válida para editar.<br>
      Entonces el sistema actualiza correctamente los datos.<br><br>
    <b>E03: Manejo de errores</b><br>
      Dado que se realiza una solicitud inválida.<br>
      Cuando el sistema procesa la operación.<br>
      Entonces el endpoint devuelve mensajes de error apropiados.

  </td>
  </tr>

</table>

<br>

<!-- ======================= TS007 ======================= -->

<h2>TS007 — Gestión de Lotes de Ganado</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS007</td>
    <td>Developer</td>
    <td>Media</td>
    <td>EP003</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Implementación de Gestión de Lotes</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar funcionalidades para la creación
      y administración de lotes de ganado.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

   <b>E01: Creación de lotes</b><br>
      Dado que el usuario registra información válida.<br>
      Cuando solicita crear un lote.<br>
      Entonces el sistema almacena correctamente el lote.<br><br>

  <b>E02: Asociación de animales</b><br>
      Dado que existen animales registrados.<br>
      Cuando el usuario asigna animales a un lote.<br>
      Entonces el sistema actualiza correctamente las relaciones correspondientes.

   </td>
  </tr>

</table>


<br><br>

<!-- ======================= EP004 ======================= -->

<h2>EP004 — Gestión de Alimentación y Salud Animal</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">
  <tr>
    <th>Epic ID</th>
    <th>Título</th>
    <th>Descripción</th>
  </tr>

  <tr>
    <td>EP004</td>
    <td>Gestión de Alimentación y Salud Animal</td>
    <td>
      Como ganadero, deseo gestionar la alimentación y monitorear la salud de mis animales
      para mantener un mejor control sanitario y productivo del ganado.
    </td>
  </tr>
</table>

<br>

<!-- US011 -->

<h3>US011</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">
  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US011</td>
    <td>Ganadero</td>
    <td>Alta</td>
    <td>EP004</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Registro de Alimentación</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero registrar la alimentación de mis animales para controlar su consumo y mejorar su productividad.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">
      <b>E01: Registro exitoso de alimentación</b><br>
      Dado que el ganadero accede al módulo de alimentación.<br>
      Cuando registra correctamente la información alimentaria.<br>
      Entonces el sistema almacena el registro y confirma la operación.<br><br>

   <b>E02: Datos inválidos</b><br>
      Dado que el ganadero registra información alimentaria.<br>
      Cuando existen campos vacíos o datos incorrectos.<br>
      Entonces el sistema muestra un mensaje de validación.
  </td>
  </tr>
</table>

<br>

<!-- US012 -->

<h3>US012</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">
  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US012</td>
    <td>Ganadero</td>
    <td>Alta</td>
    <td>EP004</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Monitoreo de Salud Animal</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero monitorear el estado de salud de mis animales para detectar enfermedades y mantener actualizado su historial sanitario.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">
      <b>E01: Consulta de estado sanitario</b><br>
      Dado que existen registros médicos del animal.<br>
      Cuando el ganadero consulta la información sanitaria.<br>
      Entonces el sistema muestra el historial y estado de salud actualizado.<br><br>

  <b>E02: Historial no disponible</b><br>
      Dado que el animal no tiene registros sanitarios.<br>
      Cuando el usuario consulta la información.<br>
      Entonces el sistema informa que no existen datos registrados.
  </td>
  </tr>
</table>

<br>

<!-- US013 -->

<h3>US013</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">
  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US013</td>
    <td>Ganadero</td>
    <td>Alta</td>
    <td>EP004</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Registro de Vacunas</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero registrar las vacunas aplicadas a mis animales
      para mantener actualizado su historial sanitario y controlar próximas dosis.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Registro exitoso de vacuna</b><br>
      Dado que el ganadero accede al módulo sanitario.<br>
      Cuando registra correctamente la información de la vacuna aplicada.<br>
      Entonces el sistema almacena el registro y actualiza el historial del animal.<br><br>

  <b>E02: Validación de datos obligatorios</b><br>
      Dado que el usuario registra una vacuna.<br>
      Cuando faltan campos obligatorios o existen datos inválidos.<br>
      Entonces el sistema muestra mensajes de validación.<br><br>

  <b>E03: Consulta de vacunas registradas</b><br>
      Dado que existen vacunas registradas.<br>
      Cuando el usuario consulta el historial sanitario.<br>
      Entonces el sistema muestra las vacunas aplicadas al animal.

   </td>
  </tr>
</table>

<br>

<!-- US014 -->

<h3>US014</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">
  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US014</td>
    <td>Ganadero</td>
    <td>Media</td>
    <td>EP004</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Generación de Alertas Sanitarias</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero recibir alertas sanitarias para actuar rápidamente ante riesgos de salud o vacunaciones pendientes.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">
      <b>E01: Generación automática de alertas</b><br>
      Dado que existe una condición sanitaria importante.<br>
      Cuando el sistema detecta un riesgo o evento próximo.<br>
      Entonces el sistema genera una alerta para el usuario.<br><br>

  <b>E02: Notificación de vacunación pendiente</b><br>
      Dado que existe una vacuna próxima a vencer.<br>
      Cuando la fecha programada se aproxima.<br>
      Entonces el sistema envía una notificación al ganadero.
  </td>
  </tr>
</table>

<br><br>


<!-- ======================= EP005 ======================= -->

<h2>EP005 — Reportes y Seguimiento Ganadero</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">
  <tr>
    <th>Epic ID</th>
    <th>Título</th>
    <th>Descripción</th>
  </tr>

  <tr>
    <td>EP005</td>
    <td>Reportes y Seguimiento Ganadero</td>
    <td>
      Como ganadero, deseo visualizar reportes, estadísticas y seguimiento sanitario
      del ganado para mejorar la toma de decisiones y mantener un mejor control
      productivo y de salud animal.
    </td>
  </tr>
</table>

<br>

<!-- ======================= US015 ======================= -->

<h3>US015</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US015</td>
    <td>Ganadero</td>
    <td>Alta</td>
    <td>EP005</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Visualización de Reportes Productivos</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero visualizar reportes productivos
      para analizar el rendimiento y estado general de mi ganado.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Generación de reportes</b><br>
      Dado que existen registros productivos almacenados.<br>
      Cuando el ganadero solicita un reporte.<br>
      Entonces el sistema genera información consolidada del ganado.<br><br>

  <b>E02: Reporte sin información disponible</b><br>
      Dado que el usuario solicita un reporte.<br>
      Cuando no existen registros suficientes.<br>
      Entonces el sistema informa que no es posible generar el reporte.

   </td>
  </tr>

</table>

<br>

<!-- ======================= US016 ======================= -->

<h3>US016</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US016</td>
    <td>Ganadero</td>
    <td>Alta</td>
    <td>EP005</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Consulta de Historial Sanitario</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero consultar el historial sanitario de mis animales
      para realizar seguimiento de vacunas, controles y estado de salud.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

   <b>E01: Consulta exitosa del historial</b><br>
      Dado que el animal posee registros sanitarios.<br>
      Cuando el ganadero consulta la información.<br>
      Entonces el sistema muestra el historial actualizado del animal.<br><br>

   <b>E02: Historial no disponible</b><br>
      Dado que el usuario consulta un animal sin registros.<br>
      Cuando el sistema procesa la solicitud.<br>
      Entonces el sistema informa que no existen datos sanitarios registrados.

  </td>
  </tr>

</table>

<br>

<!-- ======================= US017 ======================= -->

<h3>US017</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>US017</td>
    <td>Ganadero</td>
    <td>Media</td>
    <td>EP005</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Visualización de Alertas y Estadísticas Sanitarias</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como ganadero, quiero visualizar alertas y estadísticas sanitarias
      para identificar riesgos y eventos importantes relacionados con la salud del ganado.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">
     <b>E01: Visualización de estadísticas sanitarias</b><br>
      Dado que existen registros sanitarios almacenados.<br>
      Cuando el usuario accede al módulo estadístico.<br>
      Entonces el sistema muestra información consolidada y actualizada.<br><br>

  <b>E02: Generación de alertas sanitarias</b><br>
      Dado que existe una condición de riesgo o vacunación pendiente.<br>
      Cuando el sistema detecta un evento importante.<br>
      Entonces el sistema genera una alerta para el ganadero.

  </td>
  </tr>

</table>

<br><br>

<!-- ======================= EP006 ======================= -->

<h2>EP006 — APIs y Servicios Backend</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">
  <tr>
    <th>Epic ID</th>
    <th>Título</th>
    <th>Descripción</th>
  </tr>

  <tr>
    <td>EP006</td>
    <td>APIs y Servicios Backend</td>
    <td>
      Como developer, deseo implementar APIs REST, servicios backend
      y mecanismos de persistencia para soportar las funcionalidades
      principales de la plataforma Bovix.
    </td>
  </tr>
</table>

<br>

<!-- ======== TS008 ========= -->

<h3>TS008</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS008</td>
    <td>Developer</td>
    <td>Alta</td>
    <td>EP006</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Implementación de Autenticación JWT y Control de Sesiones</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar autenticación basada en JWT
      y control de sesiones seguras para proteger el acceso a los recursos de Bovix.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

   <b>E01: Generación de token JWT</b><br>
      Dado que el usuario inicia sesión correctamente.<br>
      Cuando el sistema valida las credenciales.<br>
      Entonces el backend genera un token JWT válido.<br><br>

   <b>E02: Protección de endpoints</b><br>
      Dado que existen endpoints protegidos.<br>
      Cuando el usuario realiza solicitudes autenticadas.<br>
      Entonces el sistema valida correctamente el token JWT.<br><br>

  <b>E03: Rechazo de sesiones inválidas</b><br>
      Dado que el usuario utiliza un token inválido o expirado.<br>
      Cuando intenta acceder a recursos protegidos.<br>
      Entonces el sistema rechaza la solicitud.

   </td>
  </tr>

</table>

<br>

<!-- ======================= TS009 ======================= -->

<h3>TS009</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS009</td>
    <td>Developer</td>
    <td>Alta</td>
    <td>EP006</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Implementación de Endpoints REST para Gestión de Ganado</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar endpoints REST
      para registrar, consultar y actualizar información del ganado.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

   <b>E01: Registro de animales</b><br>
      Dado que el endpoint de ganado está disponible.<br>
      Cuando se envía información válida del animal.<br>
      Entonces el sistema almacena correctamente el registro.<br><br>

   <b>E02: Consulta de información</b><br>
      Dado que existen animales registrados.<br>
      Cuando se realiza una solicitud GET válida.<br>
      Entonces el sistema devuelve la información correspondiente.<br><br>

   <b>E03: Actualización de registros</b><br>
      Dado que el animal existe en el sistema.<br>
      Cuando se envía información válida para editar.<br>
      Entonces el sistema actualiza correctamente los datos.

   </td>
  </tr>

</table>

<br>

<!-- ======================= TS010 ======================= -->

<h3>TS010</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS010</td>
    <td>Developer</td>
    <td>Media</td>
    <td>EP006</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Implementación de Gestión de Lotes y Relaciones entre Animales</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar funcionalidades backend
      para administrar lotes y relaciones entre animales registrados.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Creación de lotes</b><br>
      Dado que el usuario registra información válida.<br>
      Cuando solicita crear un lote.<br>
      Entonces el sistema almacena correctamente el lote.<br><br>

   <b>E02: Asociación de animales</b><br>
      Dado que existen animales registrados.<br>
      Cuando se asignan animales a un lote.<br>
      Entonces el sistema actualiza correctamente las relaciones correspondientes.<br><br>

   <b>E03: Persistencia de relaciones</b><br>
      Dado que la operación es válida.<br>
      Cuando el sistema procesa la solicitud.<br>
      Entonces la información queda almacenada correctamente en la base de datos.

  </td>
  </tr>

</table>

<br>

<!-- ======================= TS011 ======================= -->

<h3>TS011</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS011</td>
    <td>Developer</td>
    <td>Alta</td>
    <td>EP006</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Implementación de Endpoints para Gestión Sanitaria y Vacunas</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar endpoints sanitarios
      para registrar vacunas, monitorear salud animal y consultar historial sanitario.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

   <b>E01: Registro sanitario exitoso</b><br>
      Dado que el endpoint sanitario está disponible.<br>
      Cuando se envía información válida.<br>
      Entonces el sistema almacena correctamente el registro.<br><br>

  <b>E02: Consulta de historial sanitario</b><br>
      Dado que existen registros sanitarios.<br>
      Cuando el usuario consulta el historial del animal.<br>
      Entonces el sistema devuelve la información actualizada.<br><br>

   <b>E03: Validación de información</b><br>
      Dado que se reciben datos incompletos o inválidos.<br>
      Cuando el sistema procesa la solicitud.<br>
      Entonces el endpoint rechaza la operación y muestra errores de validación.

  </td>
  </tr>

</table>

<br>

<!-- ======================= TS012 ======================= -->

<h3>TS012</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">

  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>TS012</td>
    <td>Developer</td>
    <td>Media</td>
    <td>EP006</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">Implementación de Generación de Reportes y Estadísticas</td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como developer, necesito implementar servicios backend
      para consolidar reportes productivos y estadísticas sanitarias del ganado.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

   <b>E01: Generación de reportes</b><br>
      Dado que existen registros almacenados.<br>
      Cuando el usuario solicita un reporte.<br>
      Entonces el sistema genera información consolidada correctamente.<br><br>

   <b>E02: Generación de estadísticas sanitarias</b><br>
      Dado que existen datos sanitarios registrados.<br>
      Cuando el sistema procesa la información.<br>
      Entonces se generan estadísticas actualizadas.<br><br>

   <b>E03: Manejo de ausencia de datos</b><br>
      Dado que no existen registros suficientes.<br>
      Cuando el usuario solicita información estadística.<br>
      Entonces el sistema informa que no existen datos disponibles.

  </td>
  </tr>

</table>

<br><br>

<br><br>



<!-- ======================= EP007 ======================= -->


<h2>EP007 — Investigación y Validación Técnica</h2>

<table border="1" cellpadding="6" cellspacing="0" width="100%">
  <tr>
    <th>Epic ID</th>
    <th>Título</th>
    <th>Descripción</th>
  </tr>

  <tr>
    <td>EP007</td>
    <td>Investigación y Validación Técnica</td>
    <td>
      Como developer, deseo investigar soluciones tecnológicas que permitan garantizar el funcionamiento eficiente de Bovix en entornos rurales y de baja conectividad.
    </td>
  </tr>
</table>

<br>

<!-- SP001 -->

<h3>SP001</h3>

<table border="1" cellpadding="6" cellspacing="0" width="100%">
  <tr>
    <th>Story ID</th>
    <th>User</th>
    <th>Priority</th>
    <th>Epic</th>
  </tr>

  <tr>
    <td>SP001</td>
    <td>Developer</td>
    <td>Alta</td>
    <td>EP007</td>
  </tr>

  <tr>
    <th colspan="4">Title</th>
  </tr>

  <tr>
    <td colspan="4">
      Investigación sobre Arquitectura Offline, Sincronización y Alertas en Bovix
    </td>
  </tr>

  <tr>
    <th colspan="4">Description</th>
  </tr>

  <tr>
    <td colspan="4">
      Como equipo de desarrollo, queremos investigar y validar arquitecturas offline, mecanismos de sincronización y sistemas de alertas para Bovix, con el fin de comprender las implicancias técnicas, riesgos y esfuerzo requerido para garantizar el funcionamiento de la aplicación en entornos rurales con conectividad limitada.
    </td>
  </tr>

  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>

  <tr>
    <td colspan="4">

  <b>E01: Investigación de tecnologías offline</b><br>
      Dado que Bovix será utilizado en zonas rurales.<br>
      Cuando el equipo evalúa tecnologías compatibles con funcionamiento offline.<br>
      Entonces se documentan las alternativas viables para almacenamiento local y persistencia de datos.<br><br>

  <b>E02: Evaluación de sincronización de datos</b><br>
      Dado que la aplicación puede operar sin conexión.<br>
      Cuando se restablece la conectividad.<br>
      Entonces la información almacenada localmente debe sincronizarse correctamente con el servidor.<br><br>

  <b>E03: Evaluación de conflictos de información</b><br>
      Dado que pueden existir modificaciones simultáneas.<br>
      Cuando ocurre un conflicto entre datos locales y remotos.<br>
      Entonces se identifican mecanismos adecuados para resolver inconsistencias.<br><br>

  <b>E04: Investigación de alertas y notificaciones</b><br>
      Dado que Bovix requiere comunicar eventos sanitarios importantes.<br>
      Cuando se analizan servicios de notificaciones compatibles.<br>
      Entonces el equipo identifica soluciones viables para alertas en tiempo real.<br><br>

  <b>E05: Documentación técnica</b><br>
      Dado que finaliza la investigación técnica.<br>
      Cuando el equipo consolida los resultados obtenidos.<br>
      Entonces se genera documentación con conclusiones y recomendaciones para la implementación futura.

  </td>
  </tr>
</table>

<br>

<h3>Contexto</h3>

<p>
Bovix es una aplicación móvil orientada a optimizar la gestión ganadera mediante herramientas digitales enfocadas en el monitoreo sanitario, registro del ganado y control de información productiva en zonas rurales.
</p>

<p>
La solución está desarrollada como una aplicación móvil multiplataforma utilizando tecnologías modernas enfocadas en accesibilidad, rendimiento y facilidad de uso para ganaderos y veterinarios. Asimismo, el sistema contempla el uso de servicios backend, persistencia local y disponibilidad de información y mecanismos de sincronización para garantizar la disponibilidad y consistencia de la información.
</p>

<p>
Debido a que gran parte de los usuarios de Bovix operan en entornos rurales con conectividad limitada o intermitente, surge la necesidad de investigar tecnologías y arquitecturas que permitan mantener el funcionamiento de la aplicación incluso sin acceso constante a internet.
</p>

<p>
Este Spike tiene como objetivo investigar y validar soluciones relacionadas con:
</p>

<ul>
  <li>Persistencia local de información y mecanismos de sincronización</li>
  <li>Sincronización de datos entre dispositivo y servidor</li>
  <li>Resolución de conflictos de información</li>
  <li>Sistemas de notificaciones y alertas sanitarias en tiempo real</li>
  <li>Arquitecturas móviles orientadas a conectividad limitada</li>
</ul>

<p>
La investigación permitirá identificar tecnologías viables para garantizar una experiencia estable y confiable en Bovix, incluso en condiciones de baja conectividad.
</p>

<br>

<h3>Fundamentación Académica</h3>

<p>
Diversos estudios destacan la importancia de la persistencia local y los mecanismos de sincronización en aplicaciones móviles utilizadas en zonas rurales o con conectividad limitada.
</p>

<p>
Según Satyanarayanan (2017), las estrategias orientadas al almacenamiento local permiten mejorar la disponibilidad y experiencia de usuario al reducir la dependencia de servicios remotos y garantizar acceso continuo a la información.
</p>

<p>
Asimismo, investigaciones sobre aplicaciones móviles en entornos agrícolas y veterinarios indican que la persistencia local de datos y la sincronización diferida son fundamentales para asegurar la continuidad operativa y evitar pérdida de información en áreas con acceso inestable a internet.
</p>

<p>
Por otro lado, el uso de sistemas de notificaciones y alertas en tiempo real contribuye significativamente a mejorar la capacidad de respuesta ante eventos sanitarios importantes, permitiendo una toma de decisiones más rápida y eficiente dentro del sector ganadero.
</p>

<p>
En este contexto, Bovix busca investigar soluciones tecnológicas que permitan integrar mecanismos de almacenamiento local, sincronización eficiente y alertas sanitarias  dentro de una arquitectura móvil moderna y escalable.
</p>

</table>


<br>



### 2.4.2. Impact Mapping

A continuación se presentan los dos Impact Maps elaborados para los principales objetivos de negocio de Bovix. Esta técnica permite visualizar la relación entre los goals del negocio, los actores involucrados, los impactos esperados en su comportamiento y las funcionalidades del producto necesarias para alcanzarlos. Los mapas guiaron la priorización del Product Backlog y aseguraron que cada funcionalidad responda a un objetivo de valor concreto.

#### Impact Map 1
![Impact Map 1](../Assets/impact-map-1.png)

#### Impact Map 2
![Impact Map 2](../Assets/Impact-map-2.png)


### 2.4.3. Product Backlog
El Product Backlog es un elemento esencial en la gestión ágil de proyectos, ya que representa una lista priorizada de
funcionalidades, mejoras y tareas necesarias para el desarrollo del producto. Este backlog fue construido a partir de las
necesidades identificadas en las entrevistas, el To-Be Scenario Mapping y las User Stories, permitiendo organizar y
planificar el trabajo del equipo de forma estructurada y alineada con los objetivos del proyecto. Cada ítem del backlog
está enfocado en generar valor para el usuario final y facilitar una entrega incremental y efectiva de la solución.

| Orden | User Story ID | Título | Story Points |
|--------|----------------|---------|---------------|
| 1 | US001 | Explorar Landing Page | 2 |
| 2 | US002 | Visualización de Funcionalidades y Servicios | 2 |
| 3 | US003 | Contacto con Bovix | 1 |
| 4 | US004 | Registro de Usuario | 3 |
| 5 | US005 | Inicio de Sesión | 3 |
| 6 | US006 | Cerrar Sesión | 1 |
| 7 | US007 | Registro de Ganado | 5 |
| 8 | US008 | Consulta de Información del Ganado | 3 |
| 9 | US009 | Actualización de Información del Ganado | 3 |
| 10 | US010 | Gestión de Lotes de Ganado | 3 |
| 11 | US011 | Registro de Alimentación | 3 |
| 12 | US012 | Monitoreo de Salud Animal | 5 |
| 13 | US013 | Registro de Vacunas | 5 |
| 14 | US014 | Generación de Alertas Sanitarias | 5 |
| 15 | US015 | Visualización de Reportes Productivos | 2 |
| 16 | US016 | Consulta de Historial Sanitario | 3 |
| 17 | US017 | Visualización de Alertas y Estadísticas Sanitarias | 2 |
| 18 | TS001 | Desarrollo de Landing Page Responsiva | 3 |
| 19 | TS002 | Desarrollo de Formulario de Contacto | 2 |
| 20 | TS003 | API de Registro de Usuarios | 5 |
| 21 | TS004 | Sistema de Autenticación JWT | 5 |
| 22 | TS005 | Implementación de Endpoint para Registro de Ganado | 5 |
| 23 | TS006 | Implementación de Endpoints de Consulta y Edición | 5 |
| 24 | TS007 | Implementación de Gestión de Lotes | 3 |
| 25 | TS008 | Implementación de Autenticación JWT y Control de Sesiones | 5 |
| 26 | TS009 | Implementación de Endpoints REST para Gestión de Ganado | 5 |
| 27 | TS010 | Implementación de Gestión de Lotes y Relaciones entre Animales | 3 |
| 28 | TS011 | Implementación de Endpoints para Gestión Sanitaria y Vacunas | 5 |
| 29 | TS012 | Implementación de Generación de Reportes y Estadísticas | 3 |
| 30 | SP001 | Investigación sobre Arquitectura Offline, Sincronización y Alertas en Bovix | 5 |

Referencia Url: https://trello.com/invite/b/69eb18faf9cfe282325fc7cf/ATTI73c118c2876f1a867d9e4232056eedadE5E6036F/bovix-product-backlog

## 2.5. Strategic-Level Domain-Driven Design
En esta sección se aplica el enfoque de Diseño Orientado al Dominio (DDD) a nivel estratégico para definir la arquitectura de Bovix. Se utiliza la técnica de EventStorming para modelar el dominio del problema, identificar los Bounded Contexts candidatos y establecer las relaciones entre ellos mediante el Context Mapping. Finalmente, se presentan los diagramas de arquitectura de software a nivel de contexto, contenedor y despliegue.
### 2.5.1. EventStorming

Con el fin de plantear una aproximación del modelado de nivel general para el dominio del problema, se aplicó la técnica de EventStorming. Este proceso permitió al equipo comprender el flujo de eventos que ocurren dentro del dominio y definir las interacciones principales entre los actores, comandos y políticas del sistema.

Pasos del proceso:

1. Eventos de Dominio (Tormenta de ideas): Identificar qué ha sucedido en el negocio, usando notas adhesivas naranjas escritas en pasado

![Event1](../Assets/Event1.png)

2. Ordenar Eventos: Organizar los eventos cronológicamente de izquierda a derecha, eliminando duplicados.

![Event2](../Assets/Event2.png)

3. Identificar Comandos (Acciones): Añadir notas azules que representan acciones que provocan los eventos.

![Event3](../Assets/Event3.png)

4. Actores y Sistemas: Determinar quién realiza la acción (persona) o qué sistema externo (API, pago) participa.

![Event4](../Assets/Event4.png)

5. Políticas (Reglas de Negocio): Identificar reacciones automáticas o reglas que siguen a un evento, usando notas moradas

![Event5](../Assets/Event5.png)

 6. Agregados y Contextos Delimitados: Agrupar comandos y eventos relacionados para definir límites lógicos o microservicios.

 ![EventF](../Assets/EventStormFinal.png)

### 2.5.1.1. Candidate Context Discovery

A partir del EventStorming realizado, se reorganizó la línea de tiempo del modelado del dominio agrupando los eventos, comandos y políticas que presentaban mayor cohesión conceptual. Este proceso permitió identificar los siguientes Bounded Contexts candidatos, cada uno con una responsabilidad claramente delimitada dentro del sistema:

**Bounded Context Identity and Access Management**

Se encarga de la seguridad y el control de acceso. Gestiona el registro de nuevos usuarios, la verificación de correos, el inicio de sesión (incluyendo integraciones con proveedores de OAuth) y el mantenimiento de sesiones activas tanto para ganaderos como para veterinarios

![Iam Context](../Assets/Iam Management.png)

**Bounded Context Profile Management**

Su objetivo es la personalización de la experiencia del usuario. Permite actualizar el perfil, subir fotos, modificar preferencias y asegurar que los datos del usuario estén validados para mostrar una vista de perfil completo
.

![Profile Context](../Assets/Profile Context.png)

**Bounded Context Livestock Management**

Se centra en el control del inventario animal. Permite formar lotes de ganado, registrar animales individualmente y gestionar sus traslados. Además, es responsable de asignar y actualizar planes alimentarios para generar la ración diaria recomendada
.

![Livestock Context](../Assets/Livestock Context.png)

**Bounded Context Veterinary and Health**

Es el núcleo clínico de la aplicación. Gestiona todo el proceso de salud animal, desde generar citas y programar visitas técnicas, hasta la emisión de diagnósticos, tratamientos y vacunas, culminando en la generación de certificados de trazabilidad
.

![Veterinary Context](../Assets/Veterinary Context.png)

**Bounded Context Payments**

Administra la parte financiera de los servicios. Maneja el flujo de inicio y confirmación de pagos a través de pasarelas, gestiona el historial de transacciones, valida suscripciones y permite la descarga de comprobantes y reportes mensuales
.

![Payment Context](../Assets/Payments Context.png)

**Bounded Context Notifications**

Actúa como el canal de comunicación directa con el usuario. Su función es programar y enviar notificaciones push basadas en eventos del sistema, como citas programadas o cambios en el estado de las mismas, manteniendo un historial para consulta del usuario
.

![Notification Context](../Assets/Notification Context.png)

### 2.5.1.2. Domain Message Flows Modeling

A continuación se presentan los principales flujos de mensajes entre los Bounded Contexts identificados, modelados mediante la técnica de Domain Storytelling. Estos diagramas muestran cómo los contextos colaboran e intercambian información ante los escenarios más relevantes del sistema, permitiendo validar las relaciones definidas en el Context Mapping y detectar posibles inconsistencias en el diseño arquitectónico.

**Nuevo registro de usuario y configuracion inicial del perfil**

![Flow1](../Assets/Flow1.png)

**Programacion de visita por parte de un ganadero y su gestion de pago**

![Flow2](../Assets/Flow2.png)

**Actualizacion de plan alimentario luego de un diagnostico**

![ Flow3](../Assets/Flow3.png)

### 2.5.1.3. Bounded Context Canvases

Para la presente sección, elaboramos el Bounded Context Canvas de cada uno de los Bounded Context candidatos que identificamos. Aplicamos el modelo versión 5 propuesto por el Domain Driven Design Group. En cada uno de los canvases registramos las secciones específicas como el Context Overview Definition, Business Rules Distillation y el Ubiquitous Language, identificando claramente el tipo de Bounded Context y sus interacciones de entrada y salida con otros contextos.

**Bounded Context Identity and Access Management**

![IamCanvas](../Assets/IAM canvas.png)

**Bounded Context Profile Management**

![ProfileCanvas](../Assets/Profile canvas.png)

**Bounded Context Livestock Management**

![LiveCanvas](../Assets/Livestock canvas.png)

**Bounded Context Veterinary and Health**

![VetCanvas](../Assets/Veterinary Canvas.png)

**Bounded Context Payments**

![PayCanvas](../Assets/Payments canvas.png)

**Bounded Context Notifications**

![NotiCanvas](../Assets/Notification canvas.png)

### 2.5.2. Context Mapping

A continuación se presenta el mapa de contexto de Bovix, que define las relaciones de colaboración e integración entre los Bounded Contexts identificados. Cada relación está caracterizada según los patrones de Context Mapping del DDD (Upstream/Downstream, Shared Kernel, Customer-Supplier, Open Host Service), permitiendo comprender las dependencias del sistema y los flujos de información entre contextos.

![ContextMap](../Assets/Context Map.png)

El mapa de contexto se articula mediante IAM Management
, que actúa como Upstream al emitir el evento de registro necesario para que Profile Management
 inicialice la identidad del usuario, sirviendo este último como Open Host Service para proveer datos biográficos a toda la plataforma. Los dominios principales, Veterinary and Health
 y Livestock Management
, están integrados mediante un Shared Kernel, lo que permite que los diagnósticos clínicos emitidos por el veterinario coordinen directamente la actualización de los planes alimentarios y la ración diaria recomendada para el ganado. Finalmente, Payments
 mantiene una relación de Customer-Supplier con el área veterinaria para procesar transacciones tras la programación de citas, mientras que Notifications
 funciona de manera transversal como un consumidor Downstream que reacciona a los eventos de éxito de todos los contextos para mantener informados a ganaderos y veterinarios.

### 2.5.3. Software Architecture
### 2.5.3.1. Software Architecture Context Level Diagrams

En el software architecture context diagram se puede apreciar los componentes mas importantes que componen el sistema,asi como los usuarios y las principales funciones.

![ContextDiagram](../Assets/Context Diagram.png)



### 2.5.3.2. Software Architecture Container Level Diagrams

En el software architecture container diagram se puede apreciar la forma de más alto nivel de la arquitectura del software y como se distribuyen las responsabilidades en ella.También muestra las principales opciones tecnológicas y cómo los contenedores se comunican entre sí.

![ContainerDiagram](../Assets/Container Diagram.png)

### 2.5.3.3. Software Architecture Deployment Diagrams

Este diagrama sirve para mapear la arquitectura física del sistema, visualizando cómo se distribuyen los artefactos de software en los nodos de hardware y sus rutas de comunicación.

![Deployment](../Assets/Deployment Diagram.png)

## 2.6. Tactical-Level Domain-Driven Design
En esta sección se desarrolla el diseño táctico de cada Bounded Context identificado en la etapa estratégica. Para cada contexto se documenta el Domain Layer (entidades, value objects, enumeraciones, servicios de dominio e interfaces de repositorio), la Interface Layer, la Application Layer, la Infrastructure Layer, y los diagramas de arquitectura a nivel de componentes, clases y base de datos.
## 2.6.1. Bounded Context: Identity and Access Management
### 2.6.1.1. Domain Layer
Este bounded context gestiona el ciclo de vida de la identidad del usuario: registro, verificación, autenticación y cierre de sesión. Los actores son Ganadero y Veterinario.

**Entities:**
- **User:**
  - Propósito: Representa a cualquier usuario del sistema, independiemente de su rol.
  - Atributos: id: UUID, email: Email (VO), passwordHash: String, role: UserRole (Enum), isVerified: Boolean, createdAt: DateTime, lastLogin: DateTime
  - Métodos: verifyEmail(), login(password), logout(), changePassword(newPassword)
- **OAuthProvider:**
  - Propósito: Representa un proveedor externo de autenticación (Google, Facebook, etc.).
  - Atributos: providerId: String, providerName: String, accessToken: String
  - Métodos: authenticate(), refreshToken()
  
**ValueObjects:**
  - **Email:**
    - Propósito: Encapsula y valida el formato del correo electrónico.
    - Atributos: value: String
    - Métodos: validate(), equals(other: Email)
  - **Password:**
    - Propósito: Encapsula las reglas de validación y hashing de contraseñas.
    - Atributos: hashedValue: String
    - Métodos: hash(rawPassword), matches(rawPassword)
    
**Enumeraciones:**
  - **UserRole:** GANADERO, VETERINARIO

**Aggregates:**
  - **UserAggregate(raíz:User)**
    - Agrupa User con su Email y Password, gestionando el ciclo completo de autenticación.

**Domain Services:**
  - **AuthenticationService:**
    - **Propósito:** Orquesta la lógica de autenticación y verificación.
    - **Métodos:** authenticate(email, password): User, sendVerificationEmail(user: User), verifyToken(token: String): Boolean

**Repository Interfaces:**
  - **IUserRepository:**
    - findById(id: UUID): User
    - findByEmail(email: String): User
    - save(user: User): void
    - delete(id: UUID): void

### 2.6.1.2. Interface Layer

**AuthController:**
  - Propósito: Expone los endpoints REST para registro, login, verificación y cierre de sesión.
  - Métodos:
    - POST /auth/register → registerUser(RegisterUserCommand)
    - POST /auth/verify-email → verifyEmail(token: String)
    - POST /auth/login → login(LoginCommand)
    - POST /auth/logout → logout(userId: UUID)
    - POST /auth/recover-password → recoverPassword(email: String

**OAuthController:**
  - Propósito: Maneja la autenticación mediante proveedores OAuth externos.
  - Métodos:
    - GET /auth/oauth/{provider} → redirectToProvider(provider: String)
    - GET /auth/oauth/callback → handleOAuthCallback(code: String)

### 2.6.1.3. Application Layer

  - **RegisterUserCommandHandler**
    - Propósito: Maneja el comando de registro de nuevo usuario.
    - Método: handle(RegisterUserCommand): void
    - Lógica: Crea el usuario, hashea la contraseña, persiste y dispara el evento UserRegistered.

  - **VerifyEmailCommandHandler**
    - Propósito: Maneja la verificación del correo electrónico.
    - Método: handle(VerifyEmailCommand): void
    - Lógica: Valida el token y marca al usuario como verificado.

  - **LoginCommandHandler**
    - Propósito: Maneja el inicio de sesión.
    - Método: handle(LoginCommand): AuthToken
    - Lógica: Valida credenciales y genera JWT.

  - **RecoverPasswordCommandHandler**
    - Propósito: Inicia el flujo de recuperación de contraseña.
    - Método: handle(RecoverPasswordCommand): void

**Event Handlers:**
  - **UserRegisteredEventHandler**
    - Propósito: Reacciona al evento UserRegistered enviando el correo de verificación.

  - **LoginFailedEventHandler**
    - Propósito: Reacciona al evento LoginFailed registrando el intento fallido y bloqueando si supera el límite.

### 2.6.1.4 Infrastructure Layer

**UserRepository (implementa IUserRepository)**
  - Propósito: Accede a la base de datos relacional para persistir y consultar usuarios.
  - Tecnología: JPA/Hibernate o Entity Framework.

**EmailService**
  - Propósito: Envía correos de verificación y recuperación de contraseña.
  - Tecnología: SMTP / SendGrid API.

**JwtTokenProvider**
  - Propósito: Genera y valida tokens JWT para sesiones activas.
  - Métodos: generateToken(user: User): String, validateToken(token: String): Boolean

**OAuthAdapterService**
  - Propósito: Conecta con proveedores OAuth externos para autenticación federada.

### 2.6.1.5. Bounded Context Software Architecture Component Level Diagrams

El siguiente diagrama detalla la arquitectura interna para el Bounded Context de gestión de accesos. Ilustra el flujo de peticiones desde los actores principales a través de la capa de interfaz (controladores REST), la delegación de intenciones hacia los manejadores de comandos en la capa de aplicación, y finalmente, la ejecución de la lógica de dominio y persistencia, incluyendo la integración con proveedores OAuth externos.

![Diagrama C4 IAM](../Assets/C4-IAM.png)

### 2.6.1.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.1.6.1. Bounded Context Domain Layer Class Diagrams

La siguiente imagen presenta el diagrama de clases modelado bajo los principios de Domain-Driven Design (DDD) para la seguridad del sistema. Se detallan el Aggregate Root (User), las Entidades secundarias (OAuthProvider), los Value Objects encargados de encapsular validaciones (Email, Password), y los contratos de las interfaces de repositorios.

![Diagrama UML IAM](../Assets/UML-IAM.png)

### 2.6.1.6.2. Bounded Context Database Design Diagram

El siguiente modelo físico de datos (ERD) define la estructura a nivel de base de datos relacional para el contexto de accesos. Representa el esquema de las tablas users y oauth_providers, especificando los tipos de datos, llaves primarias (UUIDs), llaves foráneas y las restricciones (constraints) necesarias para garantizar la integridad referencial.

![Diagrama BaseDatos IAM](../Assets/BaseDatos-IAM.png)

## 2.6.2. Bounded Context: Profile Management
### 2.6.2.1. Domain Layer

Gestiona la información del perfil de los usuarios (Ganadero y Veterinario), incluyendo foto, preferencias e idioma.

**Entities:**
  - **UserProfile:**
    - Propósito: Representa el perfil completo de un usuario en el sistema.
    - Atributos: id: UUID, userId: UUID, firstName: String, lastName: String, photoUrl: String, language: String, theme: ThemePreference (Enum), updatedAt: DateTime
    - Métodos: updatePhoto(url: String), updatePreferences(language, theme), modifyObject(data: ProfileData)

  - **VeterinarianProfile(extiende UserProfile):**
    - Atributos adicionales: licenseNumber: String, specialization: String, yearsOfExperience: Int
  
  - **FarmerProfile (extiende UserProfile)**
    - Atributos adicionales: farmName: String, farmLocation: String, livestockTypes: List<String>

**ValueObjects:**
  - **ProfileData:**
    - Propósito: Encapsula los datos modificables del perfil.
    - Atributos: firstName: String, lastName: String, language: String
    
  - **PhotoUrl:**
    - Propósito: Valida y encapsula la URL de la foto de perfil.
    - Atributos: value: String
    - Métodos: validate(): Boolean

**Enumeraciones:**
  - ThemePreference: LIGHT, DARK, SYSTEM

**DomainServices:**
  - **ProfileValidationService**
    - Propósito: Valida la coherencia de los datos del perfil antes de persistirlos.
    - Métodos: validateProfileData(data: ProfileData): Boolean

**Repository Intefaces:**
  - **IUserProfileRepository**
    - findByUserId(userId: UUID): UserProfile
    - save(profile: UserProfile): void
    - update(profile: UserProfile): void
  
### 2.6.2.2. Interface Layer

**ProfileController**
  - Propósito: Expone los endpoints REST para gestión del perfil.
  - Métodos:
    - GET /profile/{userId} → getProfile(userId: UUID)
    - PUT /profile/{userId} → updateProfile(UpdateProfileCommand)
    - POST /profile/{userId}/photo → uploadPhoto(file: MultipartFile)
    - PATCH /profile/{userId}/preferences → updatePreferences(PreferencesCommand)

### 2.6.2.3. Application Layer
  - **UpdateProfileCommandHandler**
    - Propósito: Maneja la actualización de datos del perfil.
    - Método: handle(UpdateProfileCommand): void
    - Lógica: Valida coherencia de datos y persiste cambios, dispara ProfileUpdated.

  - **UploadPhotoCommandHandler**
    - Propósito: Maneja la subida y cambio de foto de perfil.
    - Método: handle(UploadPhotoCommand): String
    - Lógica: Sube la imagen al storage y actualiza photoUrl.

  - **UpdatePreferencesCommandHandler**
    - Propósito: Maneja el cambio de idioma y tema.
    - Método: handle(UpdatePreferencesCommand): void

**Event Handlers:**
  - ProfileUpdatedEventHandler 
    - Propósito: Reacciona al evento ProfileUpdated para sincronizar datos con otros bounded contexts si es necesario.


### 2.6.2.4 Infrastructure Layer
**UserProfileRepository (implementa IUserProfileRepository)**
  - Tecnología: JPA/Hibernate.

**FileStorageService**
  - Propósito: Gestiona la subida y almacenamiento de fotos de perfil.
  - Tecnología: AWS S3 / Azure Blob Storage.
  - Métodos: upload(file): String, delete(url: String): void

### 2.6.2.5. Bounded Context Software Architecture Component Level Diagrams

El presente diagrama representa la estructura interna del contexto de gestión de perfiles. Se visualiza cómo los controladores delegan las operaciones de actualización de datos, configuración de preferencias y carga de fotografías hacia la capa de aplicación. Asimismo, se evidencia la conexión con la infraestructura para el almacenamiento físico en base de datos y la gestión de archivos en la nube

![Diagrama C4 PROFILE](../Assets/C4-Profile.png)

### 2.6.2.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.2.6.1. Bounded Context Domain Layer Class Diagrams

La figura a continuación modela la estructura orientada a objetos para los perfiles de los usuarios. Destaca la aplicación del polimorfismo mediante herencia, donde FarmerProfile y VeterinarianProfile extienden de la entidad base UserProfile, incorporando sus propios atributos específicos y delegando información a Value Objects asociados.
![Diagrama UML PROFILE](../Assets/UML-Profile.png)

### 2.6.2.6.2. Bounded Context Database Design Diagram

![Diagrama BaseDatos PROFILE](../Assets/BaseDatos-Profile.png)

## 2.6.3. Bounded Context: Livestock Management
### 2.6.3.1. Domain Layer

Gestiona la creación de lotes de ganado, el registro individual de animales, su edición, traslado entre lotes y la asignación de planes alimentarios.

**Entities:**
  - **LivestockBatch (Lote de ganado)**
    - Propósito: Representa un grupo de animales manejados como unidad.
    - Atributos: id: UUID, name: String, farmerId: UUID, location: String, createdAt: DateTime
    - Métodos: edit(name, location), addAnimal(animal: Animal), removeAnimal(animalId: UUID)

  - **Animal**
    - Propósito: Representa un animal individual dentro de un lote.
    - Atributos: id: UUID, batchId: UUID, name: String, species: String, breed: String, birthDate: Date, gender: AnimalGender (Enum), weight: Double, status: AnimalStatus (Enum), registeredAt: DateTime
    - Métodos: edit(data: AnimalData), transferToBatch(newBatchId: UUID), updateWeight(weight: Double)

  - **FeedingPlan (Plan alimentario)**
    - Propósito: Representa el plan de alimentación asignado a un lote.
    - Atributos: id: UUID, batchId: UUID, dailyRation: Double, foodType: String, updatedAt: DateTime, updatedBy: UUID
    - Métodos: update(dailyRation, foodType), getRecommendedRation(): Double

**Value Objects:**

  - **AnimalData**
    - Propósito: Encapsula los datos modificables de un animal.
    - Atributos: name: String, breed: String, weight: Double

  - **Location**
    - Propósito: Representa la ubicación física de un lote.
    - Atributos: description: String

**Enumeraciones:**
  - AnimalGender: MALE, FEMALE
  - AnimalStatus: HEALTHY, SICK, QUARANTINE, DECEASED

**Domain Services:**
  - **LivestockTransferService**
    - Propósito: Orquesta el traslado de animales entre lotes validando las reglas de negocio.
    - Métodos: transfer(animalId: UUID, targetBatchId: UUID): void

  - **FeedingPlanService**
    - Propósito: Calcula y valida las raciones diarias recomendadas según especie y peso.
    - Métodos: calculateRecommendedRation(animal: Animal): Double

**Repository Interfaces:**
  - **ILivestockBatchRepository**
    - findById(id: UUID): LivestockBatch
    - findByFarmerId(farmerId: UUID): List<LivestockBatch>
    - save(batch: LivestockBatch): void
    - update(batch: LivestockBatch): void

  - **IAnimalRepository**
    - findById(id: UUID): Animal
    - findByBatchId(batchId: UUID): List<Animal>
    - save(animal: Animal): void
    - update(animal: Animal): void

  - **IFeedingPlanRepository**
    - findByBatchId(batchId: UUID): FeedingPlan
    - save(plan: FeedingPlan): void
    - update(plan: FeedingPlan): void

### 2.6.3.2. Interface Layer

  - **LivestockBatchController**
    - POST /batches → createBatch(CreateBatchCommand)
    - PUT /batches/{id} → editBatch(EditBatchCommand)
    - GET /batches/{farmerId} → getBatchesByFarmer(farmerId: UUID)

  - **AnimalController**
    - POST /batches/{batchId}/animals → registerAnimal(RegisterAnimalCommand)
    - PUT /animals/{id} → editAnimal(EditAnimalCommand)
    - PATCH /animals/{id}/transfer → transferAnimal(TransferAnimalCommand)
    - GET /animals/{id}/history → getAnimalHistory(id: UUID)

  - **FeedingPlanController**
    - POST /batches/{batchId}/feeding-plan → assignFeedingPlan(AssignFeedingPlanCommand)
    - PUT /batches/{batchId}/feeding-plan → updateFeedingPlan(UpdateFeedingPlanCommand)
    - GET /batches/{batchId}/feeding-plan → getDailyRation(batchId: UUID)

### 2.6.3.3. Application Layer

  - **CreateBatchCommandHandler**
    - Método: handle(CreateBatchCommand): void
    - Lógica: Crea el lote, valida datos y persiste. Dispara BatchCreated.

  - **EditBatchCommandHandler**
    - Método: handle(EditBatchCommand): void

  - **RegisterAnimalCommandHandler**
    - Método: handle(RegisterAnimalCommand): void
    - Lógica: Valida coherencia del animal, lo asocia al lote y persiste. Dispara AnimalRegistered.

  - **EditAnimalCommandHandler**
    - Método: handle(EditAnimalCommand): void

  - **TransferAnimalCommandHandler**
    - Método: handle(TransferAnimalCommand): void
    - Lógica: Invoca LivestockTransferService y dispara AnimalTransferred.

  - **AssignFeedingPlanCommandHandler**
    - Método: handle(AssignFeedingPlanCommand): void
    - Lógica: Crea o asigna plan alimentario al lote usando FeedingPlanService.

  - **UpdateFeedingPlanCommandHandler**
    - Método: handle(UpdateFeedingPlanCommand): void

**Event Handlers:**
  - AnimalRegisteredEventHandler: Registra el evento en el historial del animal.
  - AnimalTransferredEventHandler: Actualiza los registros de ambos lotes involucrados.

### 2.6.3.4 Infrastructure Layer

- **LivestockBatchRepository (implementa ILivestockBatchRepository)**

- **AnimalRepository (implementa IAnimalRepository)**

- **FeedingPlanRepository (implementa IFeedingPlanRepository)**
  - Tecnología: JPA/Hibernate con base de datos relacional.

- **AnimalHistoryLogger**
  - Propósito: Registra eventos del historial de cada animal (traslados, ediciones, cambios de estado).
  - Tecnología: Log en base de datos o sistema de eventos.

### 2.6.3.5. Bounded Context Software Architecture Component Level Diagrams

El siguiente diagrama expone los componentes del contexto core del sistema: la gestión ganadera. Muestra la orquestación técnica entre la creación de lotes, el registro y traslado de animales, y la asignación de planes alimentarios; evidenciando la interacción directa con los servicios de dominio y el registro histórico de eventos en la infraestructura.

![Diagrama C4 LIFESTOCK](../Assets/C4-Livestock.png)

### 2.6.3.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.3.6.1. Bounded Context Domain Layer Class Diagrams

Este diagrama ilustra el modelo de clases que soporta la lógica central del negocio ganadero. Destaca el Aggregate Root LivestockBatch y su relación transaccional con entidades dependientes como Animal y FeedingPlan, mostrando claramente la cardinalidad, las enumeraciones de estados y las operaciones de dominio encapsuladas.

![Diagrama UML LIFESTOCK](../Assets/UML-Livestock.png)

### 2.6.3.6.2. Bounded Context Database Design Diagram

![Diagrama BaseDatos LIFESTOCK](../Assets/BaseDatos-Livestock.png)


## 2.6.4. Bounded Context: Veterinary and Health
### 2.6.4.1. Domain Layer
Gestiona integralmente el ciclo de atención veterinaria del ganado, abarcando la programación de citas, ejecución de visitas técnicas, registro de diagnósticos y tratamientos, así como la emisión de certificados sanitarios y de trazabilidad.

**Entities:**
- **VeterinaryVisit (Visita técnica)**
  - Propósito: Representa una visita veterinaria programada o ejecutada para evaluar el estado de salud del ganado.
  - Atributos: id: UUID, farmerId: UUID, veterinarianId: UUID, scheduledDate: DateTime, startedAt: DateTime, finishedAt: DateTime, status: VisitStatus (Enum)
  - Métodos: schedule(date: DateTime), start(), finish(), cancel()

- **Diagnosis (Diagnóstico)**
  - Propósito: Representa el diagnóstico médico emitido durante una visita veterinaria.
  - Atributos: id: UUID, visitId: UUID, description: String, severity: DiagnosisSeverity (Enum), createdAt: DateTime, veterinarianId: UUID
  - Métodos: edit(description, severity)

- **Treatment (Tratamiento)**
  - Propósito: Representa un tratamiento aplicado como resultado de un diagnóstico.
  - Atributos: id: UUID, diagnosisId: UUID, treatmentType: String, dosage: String, durationDays: Int, appliedAt: DateTime
  - Métodos: apply()

- **HealthCertificate (Certificado sanitario)**
  - Propósito: Documento oficial que certifica el estado de salud y trazabilidad del ganado tras una visita técnica finalizada.
  - Atributos: id: UUID, visitId: UUID, certificateNumber: String, issuedAt: DateTime, status: CertificateStatus (Enum)
  - Métodos: generate(), invalidate()

**Value Objects:**
- **MedicalRecord**
  - Propósito: Encapsula el historial médico del ganado.
  - Atributos: diagnoses: List<Diagnosis>, treatments: List<Treatment>

- **VisitDate**
  - Propósito: Representa una fecha válida para una visita veterinaria.
  - Atributos: date: DateTime

**Enumeraciones:**
- VisitStatus: SCHEDULED, IN_PROGRESS, COMPLETED, CANCELED
- DiagnosisSeverity: LOW, MEDIUM, HIGH, CRITICAL
- CertificateStatus: ISSUED, INVALIDATED

**Domain Services:**
- **VisitSchedulingService**
  - Propósito: Valida la disponibilidad del veterinario y las fechas de atención.
  - Métodos: validateAvailability(veterinarianId: UUID, date: DateTime): Boolean

- **CertificationService**
  - Propósito: Orquesta la emisión de certificados sanitarios asegurando que la visita haya sido completada.
  - Métodos: issueCertificate(visit: VeterinaryVisit): HealthCertificate

**Repository Interfaces:**
- **IVeterinaryVisitRepository**
  - findById(id: UUID): VeterinaryVisit
  - findByFarmerId(farmerId: UUID): List<VeterinaryVisit>
  - save(visit: VeterinaryVisit): void
  - update(visit: VeterinaryVisit): void

- **IDiagnosisRepository**
  - findByVisitId(visitId: UUID): List<Diagnosis>
  - save(diagnosis: Diagnosis): void

- **IHealthCertificateRepository**
  - findByVisitId(visitId: UUID): HealthCertificate
  - save(certificate: HealthCertificate): void

### 2.6.4.2. Interface Layer
- **VeterinaryVisitController**
  - POST /visits → scheduleVisit(ScheduleVisitCommand)
  - PATCH /visits/{id}/start → startVisit(id: UUID)
  - PATCH /visits/{id}/finish → finishVisit(id: UUID)
  - DELETE /visits/{id} → cancelVisit(id: UUID)

- **DiagnosisController**
  - POST /visits/{visitId}/diagnosis → emitDiagnosis(EmitDiagnosisCommand)

- **CertificateController**
  - POST /visits/{visitId}/certificate → generateCertificate(GenerateCertificateCommand)

### 2.6.4.3. Application Layer

- **ScheduleVisitCommandHandler**
  - Método: handle(ScheduleVisitCommand): void
  - Lógica: Valida disponibilidad, agenda la visita y persiste la información. Dispara VisitScheduled.

- **StartVisitCommandHandler**
  - Método: handle(StartVisitCommand): void

- **FinishVisitCommandHandler**
  - Método: handle(FinishVisitCommand): void
  - Lógica: Marca la visita como completada y habilita la emisión de certificados.

- **EmitDiagnosisCommandHandler**
  - Método: handle(EmitDiagnosisCommand): void
  - Lógica: Registra el diagnóstico y actualiza el historial médico.

- **GenerateCertificateCommandHandler**
  - Método: handle(GenerateCertificateCommand): void
  - Lógica: Invoca CertificationService y genera el certificado sanitario.

**Event Handlers:**
- VisitCompletedEventHandler: Habilita la generación de certificados sanitarios.
- DiagnosisEmittedEventHandler: Actualiza el historial médico del ganado.

### 2.6.4.4. Infrastructure Layer
- **VeterinaryVisitRepository (implementa IVeterinaryVisitRepository)**
- **DiagnosisRepository (implementa IDiagnosisRepository)**
- **HealthCertificateRepository (implementa IHealthCertificateRepository)**
- Tecnología: JPA/Hibernate con base de datos relacional.

### 2.6.4.5. Bounded Context Software Architecture Component Level Diagrams
El siguiente diagrama expone los componentes del contexto de salud veterinaria, mostrando la interacción entre la programación de visitas, el registro de diagnósticos, la aplicación de tratamientos y la emisión de certificados sanitarios.

![Diagram-veterinary](../Assets/Veterinary%20Architecture.png)


### 2.6.4.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.4.6.1. Bounded Context Domain Layer Class Diagrams
### 2.6.4.6.2. Bounded Context Database Design Diagram
Este diagrama ilustra el modelo de clases que soporta la lógica central del contexto veterinario.
![Class-veterinary](../Assets/veterinary-class.png)

### 2.6.4.6.2. Bounded Context Database Design Diagram
![Database-veterinary](../Assets/veterinary-database.png)


## 2.6.5. Bounded Context: Payments 
### 2.6.5.1. Domain Layer
Gestiona el procesamiento de pagos asociados a los servicios del sistema, incluyendo la generación de transacciones, validación de pagos, control de estados y emisión de comprobantes de pago.

**Entities:**
- **Payment**
  - Propósito: Representa un pago realizado por un usuario.
  - Atributos: id: UUID, farmerId: UUID, amount: Double, currency: String, status: PaymentStatus (Enum), createdAt: DateTime
  - Métodos: authorize(), complete(), fail()

- **Transaction**
  - Propósito: Representa una transacción financiera asociada a un pago.
  - Atributos: id: UUID, paymentId: UUID, provider: String, referenceCode: String, processedAt: DateTime
  - Métodos: register()

- **Invoice (Comprobante de pago)**
  - Propósito: Documento que certifica un pago exitoso.
  - Atributos: id: UUID, paymentId: UUID, invoiceNumber: String, issuedAt: DateTime
  - Métodos: generate()

**Value Objects:**
- **Money**
  - Propósito: Encapsula el valor monetario del pago.
  - Atributos: amount: Double, currency: String

**Enumeraciones:**
- PaymentStatus: PENDING, AUTHORIZED, COMPLETED, FAILED

**Domain Services:**
- **PaymentProcessingService**
  - Propósito: Orquesta la validación y ejecución del pago.
  - Métodos: process(payment: Payment): void

**Repository Interfaces:**
- **IPaymentRepository**
  - findById(id: UUID): Payment
  - findByFarmerId(farmerId: UUID): List<Payment>
  - save(payment: Payment): void
  - update(payment: Payment): void

- **IInvoiceRepository**
  - findByPaymentId(paymentId: UUID): Invoice
  - save(invoice: Invoice): void

---

### 2.6.5.2. Interface Layer
- **PaymentController**
  - POST /payments → createPayment(CreatePaymentCommand)
  - PATCH /payments/:id/process → processPayment(id: UUID)
  - GET /payments/:farmerId → getPaymentsByFarmer(farmerId: UUID)

- **InvoiceController**
  - GET /payments/:id/invoice → getInvoiceByPayment(id: UUID)

---

### 2.6.5.3. Application Layer
- **CreatePaymentCommandHandler**
  - Método: handle(CreatePaymentCommand): void
  - Lógica: Registra el pago y lo deja en estado PENDING.

- **ProcessPaymentCommandHandler**
  - Método: handle(ProcessPaymentCommand): void
  - Lógica: Invoca PaymentProcessingService y actualiza el estado del pago.

- **GenerateInvoiceCommandHandler**
  - Método: handle(GenerateInvoiceCommand): void
  - Lógica: Genera el comprobante si el pago fue exitoso.

**Event Handlers:**
- PaymentCompletedEventHandler: Dispara la generación del comprobante.
- PaymentFailedEventHandler: Registra el fallo del pago.

---

### 2.6.5.4. Infrastructure Layer
- **PaymentRepository (implementa IPaymentRepository)**
- **InvoiceRepository (implementa IInvoiceRepository)**
- **TransactionRepository**
- Tecnología: JPA/Hibernate con base de datos relacional.

---

### 2.6.5.5. Bounded Context Software Architecture Component Level Diagrams
El siguiente diagrama muestra el flujo de las APIs de pago, desde la creación del pago hasta la emisión del comprobante.

![Diagram-payment](../Assets/Payments%20Architecture.png)

### 2.6.5.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.5.6.1. Bounded Context Domain Layer Class Diagrams
![Class-payment](../Assets/payment-class.png)

### 2.6.5.6.2. Bounded Context Database Design Diagram
![Database-payment](../Assets/payment-database.png)



## 2.6.6. Bounded Context: Notifications
### 2.6.6.1. Domain Layer

Gestiona la programación, envío y seguimiento de notificaciones push generadas por eventos del sistema, como citas programadas o cambios en su estado, manteniendo un historial consultable por el usuario.

**Entities:**

- **Notification**
  - Propósito: Representa una notificación enviada o programada para un usuario.
  - Atributos:  
    id: UUID  
    userId: UUID  
    title: String  
    message: String  
    status: NotificationStatus (Enum)  
    scheduledAt: DateTime  
    sentAt: DateTime  
    readAt: DateTime
  - Métodos:  
    markAsSent()  
    markAsRead()

- **NotificationSchedule**
  - Propósito: Representa la programación de una notificación futura.
  - Atributos:  
    id: UUID  
    notificationId: UUID  
    scheduledTime: DateTime
  - Métodos:  
    reschedule(newTime: DateTime)

**Value Objects:**

- **NotificationContent**
  - Propósito: Encapsula el contenido del mensaje.
  - Atributos: title: String, body: String

**Enumerations:**

- NotificationStatus: PENDING, SENT, READ, FAILED

**Domain Services:**

- **NotificationDispatchService**
  - Propósito: Orquesta el envío de notificaciones push.
  - Métodos: send(notification: Notification): void

**Repository Interfaces:**

- **INotificationRepository**
  - findById(id: UUID): Notification
  - findByUserId(userId: UUID): List<Notification>
  - save(notification: Notification): void
  - update(notification: Notification): void

---

### 2.6.6.2. Interface Layer

- **NotificationController**
  - POST /notifications/schedule → scheduleNotification(ScheduleNotificationCommand)
  - GET /notifications/{userId} → getUserNotifications(userId: UUID)
  - PATCH /notifications/{id}/read → markAsRead(id: UUID)

---

### 2.6.6.3. Application Layer

- **ScheduleNotificationCommandHandler**
  - Método: handle(ScheduleNotificationCommand): void
  - Lógica: Programa la notificación y la persiste.

- **SendNotificationCommandHandler**
  - Método: handle(SendNotificationCommand): void
  - Lógica: Invoca NotificationDispatchService y actualiza el estado.

- **MarkNotificationReadCommandHandler**
  - Método: handle(MarkNotificationReadCommand): void

**Event Handlers:**

- AppointmentScheduledEventHandler: Genera notificación por cita programada.
- AppointmentStatusChangedEventHandler: Notifica cambios en el estado de la cita.

---

### 2.6.6.4. Infrastructure Layer

- **NotificationRepository (implementa INotificationRepository)**
- **PushNotificationProvider**
  - Tecnología: Firebase Cloud Messaging / OneSignal
- **NotificationScheduler**
  - Tecnología: Jobs programados / cola de eventos

---

### 2.6.6.5. Bounded Context Software Architecture Component Level Diagram

![Diagram-notification](../Assets/Notifications%20Architecture.png)

### 2.6.6.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.6.6.1. Bounded Context Domain Layer Class Diagrams
![Class-notification](../Assets/notification-class.png)

### 2.6.6.6.2. Bounded Context Database Design Diagram

![Database-noitifcations](../Assets/notification-database.png)
