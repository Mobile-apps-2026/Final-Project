<div style="page-break-before: always;"></div>

# Conclusiones y Recomendaciones

## Conclusiones

### Sobre los Problem Statements

El problema central identificado en el Lean UX Problem Statement (la ausencia de herramientas digitales accesibles y adaptadas a la realidad rural peruana para la gestión ganadera) quedó validado a lo largo del proceso de entrevistas y del desarrollo del producto. Los dos segmentos objetivo manifestaron de forma independiente y coincidente la misma brecha: los ganaderos operan con registros manuales dispersos en cuadernos o Excel, y los veterinarios carecen de acceso a historiales clínicos completos al momento de realizar sus visitas de campo. Esta coincidencia entre los pain points definidos en la etapa de descubrimiento y los hallazgos reales de las entrevistas confirma que el problema era genuino y que la dirección del producto estuvo correctamente enfocada desde el inicio.

El desarrollo de Bovix en sus tres sprints permitió abordar directamente ambas dimensiones del problema: la plataforma Android para ganaderos cubrió los módulos de registro de ganado, establos, alimentación y citas veterinarias, mientras que la aplicación Flutter para veterinarios abordó el registro de visitas técnicas, diagnósticos clínicos y controles sanitarios. Aunque la integración completa con el backend del módulo veterinario se completó en el Sprint 3, el sistema en su conjunto representa una respuesta concreta y funcional a la brecha identificada.

### Sobre los Assumptions

Los assumptions de usuario definidos en el proceso Lean UX se vieron parcialmente confirmados por los resultados de las entrevistas. El assumption de que los ganaderos adoptarían la aplicación si es fácil de usar y resuelve problemas concretos fue validado por los tres entrevistados del segmento ganadero, quienes coincidieron en priorizar la simplicidad, los recordatorios automáticos y el acceso rápido a la información sobre sus animales. Del mismo modo, el assumption sobre la disposición de los veterinarios a adoptar la plataforma si les permite hacer seguimiento clínico remoto y centralizar historiales fue confirmado por Johan Bottger y Ricardo Salazar, quienes identificaron exactamente estas funcionalidades como sus necesidades más urgentes.

Sin embargo, el assumption relacionado con el modo offline (que los ganaderos en zonas rurales usarían la app regularmente sin conexión constante) no pudo ser validado empíricamente durante el ciclo de sprints, ya que la sincronización con Room se implementó como caché local pero no se realizaron pruebas formales en condiciones de baja conectividad. Este punto representa una brecha entre el supuesto planteado y los resultados efectivamente observados.

El assumption de negocio que planteaba que la integración de un módulo veterinario incrementaría la confianza de los ganaderos en la plataforma resultó coherente con lo observado en las entrevistas: los ganaderos valoraron positivamente la posibilidad de que su veterinario pudiera acceder al historial del animal antes de una visita, lo que sugiere que este módulo tiene potencial de diferenciación real frente a los competidores analizados.

### Sobre los Hypothesis Statements

De las seis hipótesis definidas en el proceso Lean UX, el equipo pudo avanzar en la validación cualitativa de al menos tres de ellas durante el ciclo de desarrollo.

La **Hipótesis 1** (que una interfaz intuitiva permitiría al usuario registrar animales en su primer uso sin asistencia) se vio respaldada por el diseño progresivo implementado en la aplicación Android, con formularios guiados y validaciones en tiempo real. No obstante, al no haberse realizado pruebas de usabilidad formales con usuarios reales sobre la aplicación desarrollada, no se puede afirmar que se alcanzó el umbral del 70% de usuarios completando el registro sin asistencia.

La **Hipótesis 5** (que las funciones de salud animal, alimentación y reproducción representarían al menos el 70% del uso total) fue coherente con la priorización del backlog: los módulos de salud, alimentación y ganado concentraron la mayor cantidad de User Stories implementadas y recibieron la mayor dedicación de horas de desarrollo en los tres sprints, lo que refleja que el equipo internalizó correctamente las necesidades críticas del usuario.

La **Hipótesis 6** (que el 60% de los usuarios reportaría mejoras en el rendimiento de su ganado tras tres meses de uso) no pudo ser evaluada en el alcance de este proyecto, ya que el tiempo de desarrollo no permite observar resultados productivos a mediano plazo. Esta hipótesis queda pendiente para una fase de validación posterior con usuarios reales en producción.

### Sobre los criterios de éxito y las validaciones

El proceso de validación mediante entrevistas permitió confirmar que las funcionalidades priorizadas en el Product Backlog responden a necesidades reales y urgentes de ambos segmentos. Los entrevistados del segmento veterinario señalaron de manera unánime tres necesidades funcionales: registro del historial clínico, control de vacunas y operación sin conexión a internet, las tres consideradas en el diseño de la solución. Esta alineación entre las entrevistas de needfinding y las épicas implementadas (EP003 y EP004) evidencia que el proceso Lean UX fue efectivo como marco de trabajo para orientar el desarrollo.

En términos de los criterios de éxito técnicos, el equipo logró desplegar un sistema completo con backend en producción, aplicación Android integrada con autenticación JWT, sincronización Room y vistas Flutter funcionales para el segmento veterinario. Esto representa un logro significativo para un equipo de cinco integrantes trabajando en tres sprints, y valida la viabilidad técnica del producto.

## Recomendaciones

### Roadmap de los productos digitales

**Corto plazo (próximos 1 a 3 meses):**

Se recomienda realizar pruebas de usabilidad formales con ganaderos y veterinarios reales sobre las versiones desplegadas de la aplicación Android y Flutter, con el fin de validar cuantitativamente las hipótesis que permanecen abiertas (en especial las relacionadas con la facilidad de uso y la adopción sin asistencia). Asimismo, se debe completar la integración offline de la aplicación Android mediante Room, priorizando los módulos de registro de ganado y citas veterinarias (dado que este es el assumption con mayor riesgo no validado y una de las principales expectativas de los ganaderos en zonas rurales). Finalmente, se recomienda publicar la aplicación Android en Google Play Store para iniciar la distribución orgánica y comenzar a recopilar métricas reales de uso.

**Mediano plazo (3 a 6 meses):**

Se recomienda desarrollar el módulo de alertas y recordatorios automáticos para vacunas y controles sanitarios (identificado como una de las funcionalidades más valoradas por ambos segmentos en las entrevistas), ya que esta característica es clave para sustentar la Hipótesis 2 sobre reducción del tiempo en tareas administrativas. Del mismo modo, se debe implementar el módulo de reportes productivos con exportación a PDF o Excel, que permita a los ganaderos compartir información con veterinarios, proveedores o instituciones del agro, cerrando el ciclo de valor de la plataforma. Adicionalmente, se recomienda evolucionar la aplicación Flutter hacia una solución completamente integrada con el backend, añadiendo la gestión completa del historial clínico veterinario y la coordinación de citas desde el lado del profesional de la salud.

**Largo plazo (6 meses en adelante):**

Se recomienda evaluar la expansión del modelo de negocio hacia un esquema freemium con suscripción, una vez validada la propuesta de valor con usuarios reales y obtenidas las primeras métricas de retención y satisfacción. También se recomienda explorar la integración con plataformas institucionales peruanas como SENASA o el Ministerio de Agricultura, que podrían validar y ampliar el alcance de la plataforma en el contexto de trazabilidad animal y cumplimiento normativo. Por último, se recomienda considerar la expansión a otros mercados latinoamericanos con problemáticas similares (como Colombia, Ecuador y Bolivia), donde la brecha de digitalización del sector ganadero presenta características análogas a las identificadas en el Perú.

<div style="page-break-before: always;"></div>

# Bibliografía

EY Perú. (2024). Guía de Negocios e Inversión en Agricultura y Agribusiness en el Perú 2024/2025. EY Perú & ComexPerú. Recuperado de https://www.ey.com/es_pe/insights/entrepreneurship/guia-negocios-inversion-agricultura-agribusiness-peru

CEPAL. (2021). Digitalización y cambio tecnológico en las mipymes agrícolas y agroindustriales en América Latina. Comisión Económica para América Latina y el Caribe. Recuperado de https://www.cepal.org/es/publicaciones/46965-digitalizacion-cambio-tecnologico-mipymes-agricolas-agroindustriales-america

OSIPTEL. (2024). Encuesta Residencial de Servicios de Telecomunicaciones – Erestel 2024. Organismo Supervisor de Inversión Privada en Telecomunicaciones. Recuperado de https://www.osiptel.gob.pe

OSIPTEL. (2025). Checa tu señal: cobertura móvil garantizada en el Perú. Recuperado de https://www.osiptel.gob.pe/portal-del-usuario/noticias/checa-tu-senal-asi-puedes-verificar-la-cobertura-movil-en-tu-distrito/
