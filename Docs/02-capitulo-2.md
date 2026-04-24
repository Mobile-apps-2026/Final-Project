# Capítulo II: Requirements Development and Software Solution Design
## 2.1. Competidores
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
        <img src="" alt="competidor 1 logo" style="max-width:100px; display:block; margin:6px auto;">
      </th>
      <th scope="column" style="width:20%; text-align:center;">
        Herdwatch<br>
        <img src="" alt="competidor 2 logo" style="max-width:100px; display:block; margin:6px auto;">
      </th>
      <th scope="column" style="width:20%; text-align:center;">
        AgriWebb<br>
        <img src="" alt="competidor 3 logo" style="max-width:100px; display:block; margin:6px auto;">
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
### 2.2.1. Diseño de entrevistas
### 2.2.2. Registro de entrevistas
### 2.2.3. Análisis de entrevistas

## 2.3. Needfinding
### 2.3.1. User Personas 
Los user persona que se muestran a continuación, fueron realizados a partir de la información recopilada de la sección de entrevistas. Estos nos ayudarán a describir de forma general nuestro segmento objetivo.

- Productores Ganaderos
<img src="..\Assets\User Persona 1.png">

<div style="page-break-after: always;">

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
### 2.4.1. User Stories
### 2.4.2. Impact Mapping
### 2.4.3. Product Backlog

## 2.5. Strategic-Level Domain-Driven Design
### 2.5.1. EventStorming
### 2.5.1.1. Candidate Context Discovery
![Iam Context](<../Assets/Iam Management.png>)
![Profile Context](<../Assets/Profile Context.png>)
![Livestock Context](<../Assets/Livestock Context.png>)
![Veterinary Context](<../Assets/Veterinary Context.png>)
![Payment Context](<../Assets/Payments Context.png>)
![Notification Context](<../Assets/Notification Context.png>)
### 2.5.1.2. Domain Message Flows Modeling
### 2.5.1.3. Bounded Context Canvases
### 2.5.2. Context Mapping
### 2.5.3. Software Architecture
### 2.5.3.1. Software Architecture Context Level Diagrams
### 2.5.3.2. Software Architecture Container Level Diagrams
### 2.5.3.3. Software Architecture Deployment Diagrams

## 2.6. Tactical-Level Domain-Driven Design
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
### 2.6.1.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.1.6.1. Bounded Context Domain Layer Class Diagrams
### 2.6.1.6.2. Bounded Context Database Design Diagram


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
### 2.6.2.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.2.6.1. Bounded Context Domain Layer Class Diagrams
### 2.6.2.6.2. Bounded Context Database Design Diagram


## 2.6.3. Bounded Context: <Bounded Context Name>
### 2.6.3.1. Domain Layer
### 2.6.3.2. Interface Layer
### 2.6.3.3. Application Layer
### 2.6.3.4 Infrastructure Layer
### 2.6.3.5. Bounded Context Software Architecture Component Level Diagrams
### 2.6.3.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.3.6.1. Bounded Context Domain Layer Class Diagrams
### 2.6.3.6.2. Bounded Context Database Design Diagram


## 2.6.4. Bounded Context: <Bounded Context Name>
### 2.6.4.1. Domain Layer
### 2.6.4.2. Interface Layer
### 2.6.4.3. Application Layer
### 2.6.4.4 Infrastructure Layer
### 2.6.4.5. Bounded Context Software Architecture Component Level Diagrams
### 2.6.4.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.4.6.1. Bounded Context Domain Layer Class Diagrams
### 2.6.4.6.2. Bounded Context Database Design Diagram


## 2.6.5. Bounded Context: <Bounded Context Name>
### 2.6.5.1. Domain Layer
### 2.6.5.2. Interface Layer
### 2.6.5.3. Application Layer
### 2.6.5.4 Infrastructure Layer
### 2.6.5.5. Bounded Context Software Architecture Component Level Diagrams
### 2.6.5.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.5.6.1. Bounded Context Domain Layer Class Diagrams
### 2.6.5.6.2. Bounded Context Database Design Diagram


## 2.6.6. Bounded Context: <Bounded Context Name>
### 2.6.6.1. Domain Layer
### 2.6.6.2. Interface Layer
### 2.6.6.3. Application Layer
### 2.6.6.4 Infrastructure Layer
### 2.6.6.5. Bounded Context Software Architecture Component Level Diagrams
### 2.6.6.6. Bounded Context Software Architecture Code Level Diagrams
### 2.6.6.6.1. Bounded Context Domain Layer Class Diagrams
### 2.6.6.6.2. Bounded Context Database Design Diagram