# RESPUESTAS — Reflexión y Resumen (Plantilla genérica)

> **Actividad / ID:** 2526-u2-2-5-reflexionyresumen-Karitsu2281
> **Unidad / Tema:** Tema 2
> **Alumno/a:** Hugo Flores Molina
> **Fecha:** 19/02/2026

---

## 1) Reflexión crítica (preguntas)
Responde con **lenguaje técnico** y **argumentos** (no solo opiniones). Si procede, usa ejemplos, riesgos y decisiones justificadas.

### 1.1) ¿Qué te han parecido los temas tratados en la unidad?
- Ofrece una visión necesaria para la seguridad informática. Está muy bien quitar el tópico de hacker solitario, ya que se centran en SOCs (Centro de operaciones de seguridad.), que se sostienen en cuatro pilares: Personas, procesos, tecnologías y servicios. La teoría, desde la taxonomía de incidentes, hasta la herramienta, que es el SIEM (Sistema de Gestión de Eventos e Información de Seguridad), y el informe, aporta una buena coherencia. Es importante entender que el SIEM es inutil sin procesos automatizados, y las personas (Analistas L1/L2/L3).

### 1.2) ¿Qué ha sido más útil para tu futuro puesto de trabajo? ¿Por qué?
- Lo más util ha sido el manejo de incidentes y la estructura del informe, ya que independientemente del rol que me asignan, debo saber como escalar un problema (diferenciar de evento rutinario con un incidente) y como redactar un informe para audiencias no técnicas, ya que no serviría de nada si puedo escalar bien un problema pero no redactar un informe. Además es muy útil la regla KISS (Keep It Simple, Stupid), ya que cualquier audencia puede entenderlo sin mayor problema, y conocer la la audiencia para adaptarlo a dicha audiencia.

### 1.3) ¿Qué partes ya conocías y cuáles han sido nuevas para ti?
- Conocía conceptos básicos como el logging, la existencia del "malware" y herramientas de escaneo básicas (como Nmap), pero lo nuevo para mí ha sido distinguir roles dentro del propio SOC (Threat Hunters, Incident Response, etc.), correlación en el SIEM y la metodología de OSINT (qué suele estar diviido en unas 6 fases, desde planificación hasta difusión) como fase de reconocimiento, no hacer 4 búsquedas de Google y ya.

### 1.4) ¿Qué concepto/idea te ha llamado más la atención y por qué?
- El concepto de "Fatiga de alerta", porque en la mayoría de casos (no todos) suelen tener un problema de exceso de ruido, que suelen ser falsos positivos, y la importancia de la implantación del SIEM y definir claramente las reglas para no saturar a los analistas.

### 1.5) ¿Qué parte recortarías o simplificarías si hubiera menos tiempo? Justifica.
- Simplificar la comparativa entre taxonomías de incidentes, aunque es muy importante clasificarlos, en el día a día basta con dominar una estándar (como la del INCIBE/ENISA) o indicadores de Ataque (IoCs o TTPs en el caso de Mitre ATT&CK) y simplemente saber que existen otras. Para mí es más importante dominar los conceptos y procedimientos que los detalles de cada taxonomía.

### 1.6) ¿Qué tema has echado en falta o ampliarías? Justifica.
- Automatización (SOAR) con ejemplos de playbooks automatizados. La evolución el SIEM va para el SOAR para combatir la fatiga de alerta, ver como se realiza una respuesta automática, se habría explicado más facilmente.

### 1.7) ¿Qué aplicarías “mañana” en un entorno real con recursos limitados?
- Documentación y reporte, pudiendose implementar en SIEMs de todo tipo de presupuesto, y se estandariza como se comunicarían los fallos. No valdría la excusa de "si no se documenta, no pasa nada", habría que obligar a documentar fecha, hora, tipo de fallo, impacto, etc, creando una base algo rudimentaria, pero bastante útil, además de una sesión post-mortem al resolver el fallo para evitar que se repita.

### 1.8) ¿Qué duda, riesgo o punto crítico te queda abierto tras la unidad?
- El riesgo de privacidad y legaliad en OSINT, ya que se puede obtener información muy sensible de personas, y no está claro hasta que punto es legal obtenerla y usarla. ¿Hasta donde es inteligencia y donde acoso? ¿Donde está el límite?.


## 2) Resumen esquematizado (obligatorio)
Incluye **todos los puntos** vistos en la unidad. Prioriza esquema/tabla/listas sobre párrafos largos.

### 2.1) Mapa/índice de la unidad (visión global)
- 2.1 Taxonomía de incidentes: Consiste en evaluar la seguridad de un sistema en 5 grandes grupos: Confidencialidad, Integridad, Disponibilidad, Trazabilidad y autorización. A partir de eso, se determina la categoría de seguridad, además de que al realizar una taxonomía común permite agrupar y clasificar amenazas de forma más eficiente y rápida.
- 2.2.1 SOC - Servicios y herramientas: El SOC supervisa, detecta y previene amenazas contínuamente, a diferencia de los CERT y CSIRT, que actúan ante incidentes muy graves, no por una amenaza menor. Dichas amenazas se identifican mediante IOCs, que son evidencias que detectan actividad sospechosa. Se apoya en servicios, como Threat Intelligence, Monitoring & Triage, Incident Response, Forensics y Threat Hunting.  
- 2.2.2.1 Qué es un SIEM: Es el "corazón" del SOC, que permite gestionar la información de seguridad y los eventos de seguridad. Se basa en la recopilación de registros de seguridad de diferentes fuentes (logs, firewalls, aplicaciones, etc.) y su correlación para detectar amenazas en tiempo real con reglas o listas blancas/negras.
- 2.2.2.2 Casos de uso: Es un escenario específico que guía como las capacidades del SOC detectan y responden a amenazas. Detallan que datos se usan, reglas aplicadas e IOCs a implementar dentro del propio SIEM y que procedimientos de respuesta seguir. En el punto se detalla 10 casos de uso que debería tener un SOC para su correcto funcionamiento.
- 2.2.3 Implantación de un SIEM: Se debe realizar de forma gradual siguiendo 4 fases:
    - Descubrimiento y planificación: Evaluar políticas, controles de la organización y definir objetivos
    - Fase piloto: Probar el sistema de forma limitada para realizar reglas más precisas y comprobar si es útil.
    - Implementación: Desplegar de forma escalonada donde se documenta todo en un manual de respuesta o runbooks.
    - Mejora continua: Evolucionar de forma constante con nuevas reglas y actualizaciones ante el cambio constante de amenazas.
- 2.2.4 Evolución del SIEM: Las amenazas que hay y el crecimiento de la superficie de ataque, hacen que SIEM tenga un término llamado "fatiga de alertas", si no se integran herramientas adicionales como SOAR, que ayuda bastante a automatizar tareas repetitivas y estandarizar respuestas a través de playbooks automáticos, reduciendo bastante la carga de los analistas.
- 2.3.1 Fuentes abiertas. OSINT: Consiste en la recolección de información de fuentes abiertas para obtener información sobre amenazas, actividades de ciberdelincuentes, etc... mediante fuentes públicas y accesibles en Internet, diferenciandose de la huella, donde el OSINT tiene metodologías más rápidas y no interactúa con el objetivo. Sigue un ciclo de 6 fases desde la planificación
- 2.4.1 Documentación de Incidentes: Es vital para cumplir con la normativa vigente, apuntar lecciones aprendidas y identificar patrones de amenazas para mejorar las defensas en el futuro. Acompañan durante todo el ciclo de vida del incidente y se debe registrar de forma detallada, con información, clasificación de peligrosidad, detalles técnicos y una línea temporal de las acciones realizadas, culminando en la etapa post-mortem debatiendo un plan futuro debatiendo si se hizo bien, en que se falló y como evitar que se repita.
- 2.4.2 Cómo escribir informes: A la hora de redactar, el objetivo y la audiencia a la que se dirige debe ser adaptado según que información se quiera transmitir (técnico, legal o directivo), además de que se explican muchos consejos para redactarlo de forma efectiva, como KISS (Keep It Simple, Stupid), que es la idea de que menos es más (es decir, que es mejor leerse un informe de dos páginas bien explicado que uno de 20 páginas), además de siempre incluir un resumen ejecutivo que nunca ocupe más de una página, y definir claramente los hechos demostrables (con las pruebas adjuntas, por supuesto) y las hipótesis mientras se elabora dicho informe.

### 2.2) Conceptos clave (lista breve)
- Evento vs Incidente: Todo incidente es un evento, pero no todo evento es un incidente.
- SOC (Security Operations Center): Centralización de la defensa, integrando 4 pilares: personas, procesos, tecnología y servicios.
- SIEM (Security Information and Event Management): Herramienta que permite gestionar la información de seguridad y los eventos de seguridad.
- Falso positivo: Alerta que no representa una amenaza real.
- OSINT (Open Source Intelligence): Inteligencia obtenida de fuentes abiertas.
- Vector de ataque vs técnica: El vector de ataque es el canal por donde entra el atacante (correo, RDP expuesto o USB), mientras que la técnica es la acción que realiza el atacante (phishing, fuerza bruta, etc).

### 2.3) Procesos / procedimientos (pasos o checklist)
Flujo del SOC:
- Recolección: Agrupación de logs de puntos, firewalls y aplicaciones
- Correlación: Analisis de logs con casos de uso.
- Generación de alertas: Notificación al equipo de monitoreo ante comportamientos sospechosos
- Validación: Se verifica si es un incidente real o un falso positivo.
- Respuesta: Acciones realizadas para minimizar el impacto del incidente.
- Recuperación: Restauración de los sistemas afectados.
- Post-mortem: Análisis del incidente para mejorar las defensas.
Creación de un caso de uso (SIEM):
- Identificación de amenazas revelantes para la empresa, definiendo escenario
- Definición de fuentes de datos: Logs, métricas, etc.
- Definición de reglas y alertas: Diseñar "firmas" o patrones sospechosos de comportamiento (por ejemplo fuerza bruta, ataques DDoS, etc.)
- Definición de procedimientos de respuesta: Establecer pasos y "playbooks" para los analistas.
- Validación y ajuste: Pruebas y simulaciones para validar su correcta implementación y realizar ajustes si es necesario.

### 2.4) Herramientas / técnicas (si aplica)
- SIEM: Splunk, Elastic SIEM, QRadar, Wazuh
- OSINT: Google, Shodan, Maltego, theHarvester
- Gestión de casos: Jira, TheHive
- Técnicas: OSINT, correlación de logs, análisis de tráfico, análisis forense
- Inteligencia: Threat Intelligence (plataformas)
- SOAR: Splunk SOAR, Cortex XSOAR, TheHive
- EDR: CrowdStrike Falcon, SentinelOne, Microsoft Defender for Endpoint

### 2.5) Buenas prácticas y errores típicos
- Buenas prácticas:
  - Usar todos los logs en UTC
  - Aplicar principio de mínimo privilegio en los accesos al SOC
  - Documentación en tiempo real, no esperando al último momento
  - Preservar evidencia en caso de análisis forense
  - Implementar de forma gradual, empezando por lo más crítico
  - Usar la regla de KISS (Keep It Simple, Stupid)
- Errores típicos:
  - Hacer log de todo sin ningún criterio
  - Dejar reglas por defecto (causa muchos falsos positivos y fatiga de alertas)
  - Usar jerga incomprensible para directivos o público no técnico
  - Actuar sin autorización explícita

### 2.6) Glosario mínimo (términos y definiciones cortas)
- Analista L1: Triaje inicial, valida alertas, escalan cuando es necesario y siguen playbooks básicos
- Playbook: Guía paso a paso para manejar un tipo específico de incidente
- IoC (Indicator of Compromise): Dato que evidencia una intrusión (IP, hash, dominio, etc.)
- TTP (Tactic, Technique, and Procedure): Táctica, técnica y procedimientos, como se comporta un atacante
- Log: Registro de actividad generado por un equipo
- Threat Intelligence: Servicio que provee información (IoCs) sobre amenazas actuales y futuras para alimentar el SIEM.
- Falso positivo: Alerta que no representa una amenaza real.
- Threat Hunting: Proceso proactivo de búsqueda de amenazas en la red.


## 3) (Opcional) Evidencias y recursos usados
Enlaza aquí evidencias (capturas, logs, configuraciones, salidas de comandos, etc.) si forman parte de tu trabajo.

### Evidencia 1
- Archivo: `evidencias/01_ReglasSnortEjemplos.md`
- Qué demuestra: Cómo funciona una regla de Snort de forma rápida, ejemplos de reglas implementadas y justificación de las reglas elegidas.
- Qué he aprendido: He aprendido que las reglas pueden ser algo quisquillosas, ya que si no se definen bien pueden generar muchos falsos positivos.

### Evidencia 2
- Archivo: `evidencias/02_...`
- Qué demuestra:
- Qué he aprendido:


## 4) Conclusión (cierre)
- La unidad 2 ha establecido, para mí, la base de la ciberseguridad defensiva. Más allá de las herramientas, lo vital ha sido comprender que la seguridad es un proceso continuo (SOC), detección (SIEM) y comunicación (Informes). La capacidad de transformar datos en inteligencia es el valor central que se espera de nosotros en un entorno real, además, he entendido que debemos documentar correctamente los casos de uso para que puedan ser fácilmente replicables, ya que un SIEM puede ser inútil si no se documentan correctamente dichos casos o personal bien estructuado para responder a los fallos de forma efectiva.
