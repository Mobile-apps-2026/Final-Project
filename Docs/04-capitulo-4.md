# Capítulo IV: Product Implementation & Validation

## 4. Product Implementation & Validation

##  4.1. Software Configuration Management
### 4.1.1. Software Development Environment Configuration

#### Gestión del Proyecto

Para la coordinación del proyecto se emplearon diversas plataformas de comunicación y gestión de versiones. Se estableció una organización en GitHub para concentrar el manejo del código fuente y su control de versiones. Respecto a la comunicación interna y reuniones del equipo, se empleó Discord como plataforma principal.

- **Coordinación del trabajo:** Github
- **Reuniones virtuales:** Discord
- **Comunicación diaria:** Whatsapp
- **Organización y seguimiento de tareas:** Trello

**Enlaces de referencia:**
- Github: https://github.com/
- Discord: https://discord.com/
- Trello: https://trello.com/

#### Gestión de Requerimientos

Durante esta etapa, se adoptaron estrategias específicas que permitieron la captura, estructuración y jerarquización de los requerimientos del proyecto. Se empleó Trello como plataforma visual para administrar actividades a través de tableros configurables. Se recurrió a UXPressia para elaborar user personas, mapas de empatía, journey maps y el lean UX canvas. Se utilizó Miro para construir los escenarios As-Is y To-Be.

**Enlaces de referencia:**
- Trello: https://trello.com/
- UXPressia: https://uxpressia.com/
- Miro: https://miro.com/es/

#### Diseño de Experiencia e Interfaz del Producto

En la fase de diseño de la experiencia e interfaz de usuario, el equipo empleó Figma para elaborar wireframes, maquetas y prototipos interactivos, lo cual facilitó la validación de la propuesta de diseño previo a su desarrollo.

**Enlaces de referencia:**
- Figma: https://www.figma.com/

#### Desarrollo de Software

Para la construcción de la aplicación móvil se utilizaron tecnologías como Kotlin para Android en Android Studio. La documentación del informe se desarrolló en archivos .md empleando IDEs como IntelliJ IDEA y Rider (cada integrante del equipo trabajó con alguna de estas herramientas). Para facilitar la descarga, instalación y actualización de estos IDEs se utilizó la herramienta de gestión JetBrains ToolBox.

**Enlaces de referencia:**
- JetBrains ToolBox: https://www.jetbrains.com/toolbox-app/
- Android Studio: https://developer.android.com/studio

#### Documentación de Software

Para el manejo de versiones y la colaboración en el desarrollo del informe, se empleó GitHub implementando la metodología GitHub Flow. Esta estrategia facilitó una administración organizada y eficaz del proyecto a través del uso de ramas específicas para cada característica o corrección, lo que optimizó el trabajo en equipo. Todo el material del proyecto fue consolidado y guardado en un repositorio dentro de una organización establecida en GitHub. Para la documentación técnica del proyecto se seleccionó el uso de archivos en formato Markdown, por su sencillez, claridad y perfecta integración con GitHub.

**Enlaces de referencia:**
- GitHub: https://github.com/

#### Despliegue de Software

Para la distribución de la aplicación móvil se utilizarán plataformas como Google Play Store para Android, las cuales son ideales para la publicación y distribución de aplicaciones móviles.

**Enlaces de referencia:**
- Google Play Console: https://play.google.com/console/

### 4.1.2. Source Code Management

#### Estructura de ramas Git Flow

- **main:** rama primaria donde siempre se mantiene el código estable y preparado para producción.
- **develop:** rama de desarrollo donde se consolidan todas las nuevas características antes de ser transferidas a producción.
- **feature/:** ramas destinadas a desarrollar nuevas funcionalidades.
- **release/:** ramas temporales para preparar una nueva versión estable.
- **hotfix/:** ramas para solucionar errores críticos en producción.

#### Versionado Semántico (Semantic Versioning)

Se implementará el sistema de versionado semántico (Semantic Versioning 2.0.0), aplicando el formato: **MAJOR.MINOR.PATCH**.

- 1.0.0 → versión estable inicial
- 1.1.0 → inclusión de nuevas características
- 1.1.1 → corrección de errores

#### Estándar de mensajes de commits

El equipo adoptará el estándar de mensajes de commits establecido en "Conventional Commits".

**Ejemplos de mensajes:**

- `feat: implementar nuevo sistema de autenticación`
- `fix: resolver validación en formulario de registro`
- `docs: actualizar README con guías de implementación`

#### Nomenclatura para numeración de versiones:

- **Cambios Mayores:** Cuando el código o versión nueva del proyecto implementado presenta modificaciones sustanciales respecto a la versión anterior, estos cambios resultan incompatibles con la versión previa.
- **Cambios Menores:** Cuando el código o versión nueva del proyecto implementado presenta modificaciones respecto a alguna característica específica.
- **Patch:** Cuando se resuelven errores menores.

#### Repositorio de Github:

- Enlace para acceder al repositorio de la landing page: 
- Enlace para acceder al repositorio de la aplicación móvil: 
- Enlace para acceder al repositorio del Informe: 

#### Metodología de trabajo GitFlow
La metodología de trabajo se fundamentará en un modelo de ramas Git Flow, el cual se basa en la generación de ramas específicas para cada funcionalidad o corrección de errores. El modelo de "A successful Git branching model"

#### Organización de branches (Ramas):

1. **Master branch (Rama primaria):** Es la rama fundamental del proyecto, donde se conserva el código estable y preparado para producción. Únicamente se incorporarán modificaciones que hayan sido probadas y validadas previamente en las ramas de desarrollo y funcionalidad.

2. **Develop Branch (Rama de Desarrollo):** Esta rama funciona como un espacio de consolidación para el trabajo colaborativo, facilitando pruebas y ajustes de las nuevas funcionalidades antes de fusionarlas con la rama primaria. Asegura que el código sea operativo y estable.

3. **Feature branch (Ramas de funcionalidad):** Cada nueva característica o tarea específica se construirá en su propia rama. Una vez finalizada y probada, se consolidará en la rama de desarrollo. Las ramas de funcionalidad seguirán un esquema de nombres descriptivos, como por ejemplo: `feature/user-authentication`.

### 4.1.3. Source Code Style Guide & Conventions

El equipo establecerá nomenclatura en inglés para todas las variables, funciones, clases y archivos del proyecto, con el propósito de preservar flexibilidad, escalabilidad y consistencia en el desarrollo.

#### Desarrollo Android (Kotlin)
Se implementa el estilo de código oficial de Android y las convenciones de Kotlin.

- Los nombres de clases seguirán PascalCase (`MainActivity`, `UserRepository`).
- Las funciones y variables utilizarán camelCase (`getCurrentUser`, `isLoggedIn`).
- Los recursos seguirán snake_case (`activity_main`, `btn_login`).
- Identificadores descriptivos y claros para accesibilidad y mantenimiento.

Se emplearon diferentes componentes para estructurar la aplicación móvil:

- **Activity:** Define las pantallas principales de la aplicación móvil.
- **Fragment:** Establece las secciones modulares que conforman las diferentes vistas de la aplicación.
- **View:** Permite la organización de diferentes elementos visuales dentro de la aplicación, facilitando la aplicación de estilos específicos para cada componente.
- **ImageView:** Facilita la integración de imágenes en la aplicación móvil, utilizado frecuentemente a lo largo de la aplicación.
- **RecyclerView:** Sirve para mostrar listas dinámicas de elementos, principalmente empleado para la visualización de datos y menús interactivos.
- **Button:** Establece botones interactivos personalizables que permiten a los usuarios ejecutar acciones específicas.
- **TextView:** Define los textos y etiquetas, diferenciándolos del resto del contenido visual.

### 4.1.4. Software Deployment Configuration

#### Despliegue de aplicación móvil:

Para publicar la aplicación móvil, es fundamental cumplir con ciertos requisitos previos, como disponer de una cuenta de desarrollador, configurar el proyecto y preparar los archivos de distribución. Una vez satisfechos estos requisitos, se pueden ejecutar los pasos detallados a continuación para realizar la publicación:

1. Verificar que el proyecto esté configurado correctamente con las dependencias necesarias.
2. Asegurarse de que la aplicación cumpla con las convenciones de nomenclatura: archivos de configuración como "build.gradle", "AndroidManifest.xml", estructura de carpetas "res/" para recursos, y "src/" para código fuente.
3. Generar el archivo APK o AAB (Android App Bundle) para distribución.
4. Acceder a Google Play Console y crear una nueva aplicación o versión.
5. Configurar la información de la aplicación, capturas de pantalla y descripción.
6. Subir el archivo de la aplicación y esperar la revisión de Google Play Store.


#### Google Play Store:

El enlace de la aplicación en Google Play Store será proporcionado una vez completado el proceso de publicación y aprobación.

#### Despliegue de Landing Page:




## 4.2. Landing Page & Mobile Application Implementation
### 4.2.1. Sprint n


### 4.2.1.1. Sprint Planning n
### 4.2.1.2. Sprint Backlog 1

En esta primera iteración, el objetivo planteado fue implementar la landing page de
Bovix para dar a conocer las funciones y servicios de la plataforma, junto con las
funcionalidades base de autenticación y registro sanitario del ganado. Las secciones
deben estar correctamente implementadas al finalizar el Sprint: landing page, registro
de usuario, inicio de sesión y registro de vacunas.

| id | Title | Id | Title | Description | Estimations (Hours) | Status (To-do / In-Process / To-Review / Done) |
|---|---|---|---|---|---|---|
| US04 | Explorar landing page | CC01 | Header y navbar responsivos | Desarrollo e implementación de la estructura del encabezado y barra de navegación. Debe ser responsive. | 2 | Done |
| US04 | Explorar landing page | CC02 | Sección Hero | Desarrollo e implementación de los estilos correspondientes a la sección Hero. Debe ser responsive. | 2 | Done |
| US04 | Explorar landing page | CC03 | Sección About Us | Desarrollo e implementación de la sección que describe el equipo y la misión de Bovix. Debe ser responsive. | 2 | Done |
| US04 | Explorar landing page | CC04 | Sección Product | Desarrollo e implementación de la sección que describe las funcionalidades y segmentos del producto. | 2 | Done |
| US04 | Explorar landing page | CC05 | Sección Contact y Footer | Desarrollo e implementación de la sección de contacto y pie de página con enlaces a redes sociales. | 2 | Done |
| US01 | Registro de usuario | CC06 | Formulario de registro | Desarrollo del formulario de registro con validaciones de campos obligatorios y mensajes de error. | 3 | Done |
| US01 | Registro de usuario | CC07 | Lógica de creación de cuenta | Implementación de la lógica de creación de cuenta, hash de contraseña y persistencia en base de datos. | 4 | Done |
| US02 | Inicio de sesión | CC08 | Formulario de login | Desarrollo del formulario de inicio de sesión con validación de campos y credenciales. | 3 | Done |
| US02 | Inicio de sesión | CC09 | Lógica de autenticación | Implementación de la autenticación con JWT y redirección al dashboard tras login exitoso. | 4 | Done |
| US03 | Registrar vacuna | CC10 | Formulario de registro de vacuna | Desarrollo del formulario con campos: tipo de vacuna, fecha de aplicación, dosis y animal asociado. | 3 | Done |
| US03 | Registrar vacuna | CC11 | Lógica de guardado de vacuna | Implementación del guardado del registro de vacuna con control de errores y confirmación de éxito. | 5 | Done |

---

### 4.2.1.3. Development Evidence for Sprint Review

Durante el Sprint 1 se implementaron las funcionalidades base de la plataforma Bovix.
Se desarrolló la landing page, el flujo de registro de usuarios, el inicio de sesión
y el registro de vacunas del ganado.

**Software Development:**

- **GitHub:** Plataforma de desarrollo colaborativo que utiliza el sistema de control
  de versiones Git. Se utiliza para alojar, revisar y colaborar en los repositorios
  del proyecto, facilitando el trabajo en equipo.

- **Android Studio:** Entorno de desarrollo integrado (IDE) creado por Google para
  el desarrollo de aplicaciones Android. Permite escribir, depurar y empaquetar la
  aplicación móvil de Bovix.

- **Visual Studio Code:** Editor de código utilizado para el desarrollo de la
  landing page y servicios complementarios del proyecto.

**Source Code Management:**

Utilizamos GitHub para llevar el control de versiones y trabajar de forma colaborativa.
Hemos creado una organización con los repositorios correspondientes:

- Repositorio de la Landing Page: *(Insertar enlace)*
- Repositorio de la aplicación móvil: *(Insertar enlace)*
- Repositorio del backend: *(Insertar enlace)*

**Mobile Application — Kotlin:**

Para el desarrollo móvil nos guiamos por la "Guía de Estilo de Kotlin" de Android Developers:

- **Nombres de clases:** Se escriben en formato PascalCase y son sustantivos o frases nominales.
- **Nombres de funciones:** Se escriben en camelCase y suelen ser verbos o frases verbales.
- **Sangría:** Cada bloque nuevo aumenta la sangría en 4 espacios.
- **Constantes:** Se escriben en UPPER_SNAKE_CASE con palabras separadas por guiones bajos.
- **No constantes:** Se escriben en camelCase para propiedades de instancia y parámetros.

**Landing Page — HTML/CSS:**

- Siempre declarar el tipo de documento (`<!DOCTYPE html>`) en la primera línea.
- Usar minúsculas para los nombres de etiquetas y atributos.
- Cerrar todas las etiquetas correctamente.
- Usar comillas dobles para los valores de los atributos.
- Especificar los atributos `alt`, `width` y `height` en todas las imágenes.

---

### 4.2.1.4. Testing Suite Evidence for Sprint Review

Para el Sprint 1 se elaboraron pruebas de aceptación basadas en los criterios
Gherkin definidos en las User Stories priorizadas. Se verificaron todos los
escenarios (E01, E02, E03) de cada historia de usuario.

**Lenguaje Gherkin:**

El lenguaje Gherkin es un lenguaje de dominio específico utilizado para escribir
pruebas de aceptación en formato legible por el equipo. Se utilizaron las siguientes
palabras clave: `Feature`, `Scenario`, `Given`, `When`, `Then` y `And`.

| User Story | Escenario | Criterio verificado | Estado |
|---|---|---|---|
| US04 – Explorar landing page | E01 | La landing page carga correctamente en Chrome y Firefox | Done |
| US04 – Explorar landing page | E02 | La navegación entre secciones funciona con scroll suave | Done |
| US01 – Registro de usuario | E01 | El sistema crea la cuenta con datos válidos y muestra confirmación | Done |
| US01 – Registro de usuario | E02 | El sistema solicita completar los campos obligatorios vacíos | Done |
| US01 – Registro de usuario | E03 | El sistema muestra mensaje de error con datos de formato inválido | Done |
| US02 – Inicio de sesión | E01 | El sistema permite el acceso con credenciales válidas | Done |
| US02 – Inicio de sesión | E02 | El sistema rechaza el acceso con credenciales incorrectas | Done |
| US02 – Inicio de sesión | E03 | El sistema solicita completar los campos vacíos antes de procesar | Done |
| US03 – Registrar vacuna | E01 | El sistema guarda correctamente el registro de vacuna | Done |
| US03 – Registrar vacuna | E02 | El sistema muestra error al ingresar datos incorrectos en el formulario | Done |

---

### 4.2.1.5. Execution Evidence for Sprint Review

Durante el Sprint 1 se implementaron y ejecutaron satisfactoriamente las siguientes
funcionalidades:

**Landing Page de Bovix**

Se desarrolló la landing page completa con las secciones: Home, About Us, Product,
About the Team y Contact. La página es completamente responsive y permite la
navegación fluida entre secciones mediante scroll suave, facilitando que cualquier
visitante conozca el producto antes de registrarse.

Se implementó el formulario de registro con validaciones en tiempo real.
El sistema detecta campos vacíos y formatos inválidos mostrando mensajes de error
descriptivos. Ante un registro exitoso el usuario recibe confirmación y es redirigido
al formulario de inicio de sesión.


**Inicio de sesión (US02)**

Se implementó el flujo completo de autenticación. Las credenciales inválidas generan
un mensaje de error sin permitir el acceso al sistema. Ante un login exitoso el
usuario es redirigido al dashboard principal.


**Registro de vacuna (US03)**

Se implementó el formulario para registrar vacunas del ganado. El ganadero puede
ingresar el tipo de vacuna, fecha de aplicación, dosis y animal asociado. El sistema
valida los datos y confirma el guardado con un mensaje de éxito.

---

### 4.2.1.6. Services Documentation Evidence for Sprint Review

Durante el Sprint 1 se documentaron de forma preliminar los servicios de backend
según la arquitectura definida en el Capítulo II. La documentación completa en
Swagger se publicará en el Sprint 2 una vez los endpoints estén desplegados.

**Plataforma de despliegue planificada:** Render (Web Service con Docker) + Aiven (Base de datos MySQL 8.4.8)

<td><p align="center"><img src="/Assets/Images-deplyoment/deployment-database.jpg" alt="deploy-database" width="70%"></p></td>

<td><p align="center"><img src="/Assets/Images-deplyoment/deployment-backend.jpg" alt="deploy-backend" width="70%"></p></td>

**Tabla de Endpoints de la API de Bovix:** 



> **Enlace a documentación Swagger:** [BackEnd](https://bovix-backend.onrender.com/swagger/index.html)


---

### 4.2.1.7. Software Deployment Evidence for Sprint Review

Durante el Sprint 1 se realizó el despliegue de la landing page de Bovix como
primer entregable público de la plataforma.

**Plataforma utilizada:** Github Pages

<td><p align="center"><img src="/Assets/Images-deplyoment/deployment-landingpage.png" alt="deploy-landing" width="70%"></p></td>


**Pasos realizados para el despliegue:** 
Se desarrolló la landing page en el repositorio del equipo bajo la organización Mobile-apps-2026.
Se configuró GitHub Pages desde la sección Settings > Pages del repositorio, seleccionando la rama main como fuente de publicación.
GitHub Pages generó automáticamente la URL pública del sitio una vez activado el despliegue.
Se verificó el correcto funcionamiento de la página accediendo a la URL generada.

**URL de la Landing Page:** [Landing page](https://mobile-apps-2026.github.io/Landing-Page-Bovix/)

---

### 4.2.1.8. Team Collaboration Insights during Sprint

Durante el Sprint 1 el equipo mantuvo comunicación activa y colaboración organizada
mediante las siguientes herramientas:

**Project Management:**

- **Discord:** Canal principal de comunicación para reuniones de planificación,
  daily check-ins y resolución de dudas técnicas en tiempo real.
- **Google Meet:** Plataforma de videoconferencias utilizada para reuniones de
  revisión y retrospectiva del sprint.

**Source Code Management:**

Utilizamos GitHub para el control de versiones y el trabajo colaborativo.
Se siguió el modelo GitFlow con ramas `feature/` para cada funcionalidad y
se aplicó la convención de Conventional Commits en los mensajes
(`feat:`, `fix:`, `docs:`, `style:`, `refactor:`).

**Distribución del trabajo por integrante:**

| Integrante | Tareas principales en Sprint 1 |
|---|---|
| Flores Manrique, Sebastian Enrique | Lógica de creación de cuenta y guardado de vacunas |
| De las Casas Latour, Sebastián | Secciones de landing page y formulario de login |
| Esquirva León, Miguel Juan Diego | Estructura HTML de landing page y validaciones de vacuna |
| Inga Hernández, Ayrton Damian | Formulario de registro de usuario y lógica de autenticación |
| Meza Tataje, David | Estilos responsive de landing page y formulario de vacuna |


## 4.3. Validation Interviews
### 4.3.1. Diseño de Entrevistas
### 4.3.2. Registro de Entrevistas
### 4.3.3. Evaluaciones según heurísticas
