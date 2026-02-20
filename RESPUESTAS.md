# RESPUESTAS — Reflexión y Resumen (Plantilla genérica)

> **Actividad / ID:** 2526-u2-2-5-reflexionyresumen-Karitsu2281
> **Unidad / Tema:** Tema 2
> **Alumno/a:** Hugo Flores Molina
> **Fecha:** 19/02/2026

---

## 1) Reflexión crítica (preguntas)
Responde con **lenguaje técnico** y **argumentos** (no solo opiniones). Si procede, usa ejemplos, riesgos y decisiones justificadas.

### 1.1) ¿Qué te han parecido los temas tratados en la unidad?
- Ofrece una visión necesaria para la seguridad informática. Está muy bien quitar el tópico de hacker solitario, ya que se centran en SOCs (Centro de operaciones de seguridad.) La teoría, desde la taxonomía de incidentes, hasta la herramienta, que es el SIEM (Sistema de gestión de incidentes), y el informe, aporta una buena coherencia. Es importante entender que el SIEM es inutil sin procesos automatizados, y las personas (Analistas L1/L2/L3).

### 1.2) ¿Qué ha sido más útil para tu futuro puesto de trabajo? ¿Por qué?
- Lo más util ha sido el manejo de incidentes y la estructura del informe, ya que independientemente del rol que me asignan, debo saber como escalar un problema (diferenciar de evento rutinario con un incidente) y como redactar un informe para audiencias no técnicas, ya que no serviría de nada si puedo escalar bien un problema pero no redactar un informe.

### 1.3) ¿Qué partes ya conocías y cuáles han sido nuevas para ti?
- Conocía conceptos básicos como el logging, la existencia del "malware" y herramientas de escaneo básicas (como Nmap), pero lo nuevo para mí ha sido distinguir roles dentro del propio SOC (Threat Hunters, Incident Response, etc.), correlación en el SIEM y la metodología de OSINT como fase de reconocimiento, no hacer 4 búsquedas de Google y ya.

### 1.4) ¿Qué concepto/idea te ha llamado más la atención y por qué?
- El concepto de "Fatiga de alerta", porque en la mayoría de casos (no todos) suelen tener un problema de exceso de ruido, que suelen ser falsos positivos, y la importancia de la implantación del SIEM y definir claramente las reglas para no saturar a los analistas.

### 1.5) ¿Qué parte recortarías o simplificarías si hubiera menos tiempo? Justifica.
- Simplificar la comparativa entre taxonomías de incidentes, aunque es muy importante clasificarlos, en el día a día basta con dominar una estándar (como la del INCIBE o Mitre ATT&CK) y simplemente saber que existen otras. Para mí es más importante dominar los conceptos y procedimientos que los detalles de cada taxonomía.

### 1.6) ¿Qué tema has echado en falta o ampliarías? Justifica.
- Automatización (SOAR) con ejemplos de playbooks automatizados. La evolución el SIEM va para el SOAR para combatir la fatiga de alerta, ver como se realiza una respuesta automática, se habría explicado más facilmente.

### 1.7) ¿Qué aplicarías “mañana” en un entorno real con recursos limitados?
- Documentación y reporte, pudiendose implementar en SIEMs de todo tipo de presupuesto, y se estandariza como se comunicarían los fallos. No valdría la excusa de "si no se documenta, no pasa nada", habría que obligar a documentar fecha, hora, tipo de fallo, impacto, etc, creando una base algo rudimentaria, pero bastante útil.

### 1.8) ¿Qué duda, riesgo o punto crítico te queda abierto tras la unidad?
- El riesgo de privacidad y legaliad en OSINT, ya que se puede obtener información muy sensible de personas, y no está claro hasta que punto es legal obtenerla y usarla. ¿Hasta donde es inteligencia y donde acoso? ¿Donde está el límite?.


## 2) Resumen esquematizado (obligatorio)
Incluye **todos los puntos** vistos en la unidad. Prioriza esquema/tabla/listas sobre párrafos largos.

### 2.1) Mapa/índice de la unidad (visión global)
- 2.1 Taxonomía de incidentes
- 2.2.1 SOC - Servicios y herramientas
- 2.2.2.1 Qué es un SIEM
- 2.2.2.2 Casos de uso
- 2.2.3 Implantación de un SIEM
- 2.2.4 Evolución del SIEM
- 2.3.1 Fuentes abiertas. OSINT
- 2.4.1 Documentación de Incidentes
- 2.4.2 Cómo escribir informes

### 2.2) Conceptos clave (lista breve)
- Evento vs Incidente: Todo incidente es un evento, pero no todo evento es un incidente.
- SOC (Security Operations Center): Centralización de la defensa.
- SIEM (Security Information and Event Management): Herramienta que permite gestionar la información de seguridad y los eventos de seguridad.
- Falso positivo: Alerta que no representa una amenaza real.
- OSINT (Open Source Intelligence): Inteligencia obtenida de fuentes abiertas.

### 2.3) Procesos / procedimientos (pasos o checklist)
- Ciclo de vida del incidente:
- Preparación: Herramientas preparadas, personal formado, etc.
- Detección y análisis: Triaje de alertas y validación de falsos positivos
- Contención, erradicación y recuperación: Frenar daño, eliminar amenaza y volver a la normalidad.
- Post-incidente (Lecciones aprendidas): Informe post-incidente y mejora continua.
Implantación del SIEM:
- Definir alcance y datos a monitorizar
- Recolección de logs
- Casos de Uso
- Ajuste para reducir falsos positivos

### 2.4) Herramientas / técnicas (si aplica)
- SIEM: Splunk, Elastic SIEM, QRadar, Wazuh
- OSINT: Google, Shodan, Maltego, theHarvester
- Gestión de casos: Jira, TheHive
- Técnicas: OSINT, correlación de logs, análisis de tráfico

### 2.5) Buenas prácticas y errores típicos
- Buenas prácticas:
  - Usar todos los logs en UTC
  - Aplicar principio de mínimo privilegio en los accesos al SOC
  - Documentación en tiempo real, no esperando al último momento
  - Preservar evidencia en caso de análisis forense
- Errores típicos:
  - Hacer log de todo sin ningún criterio
  - Dejar reglas por defecto (causa muchos falsos positivos)
  - Usar jerga incomprensible para directivos o público no técnico
  - Actuar sin autorización explícita

### 2.6) Glosario mínimo (términos y definiciones cortas)
- Analista L1: Triaje inicial, valida alertas, escalan cuando es necesario y siguen playbooks básicos
- Playbook: Guía paso a paso para manejar un tipo específico de incidente
- IoC (Indicator of Compromise): Dato que evidencia una intrusión (IP, hash, dominio, etc.)
- TTP (Tactic, Technique, and Procedure): Táctica, técnica y procedimientos, como se comporta un atacante
- Log: Registro de actividad generado por un equipo


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
- La unidad 2 ha establecido la base de la ciberseguridad defensiva. Más allá de las herramientas, lo vital ha sido comprender que la seguridad es un proceso continuo (SOC), detección (SIEM) y comunicación (Informes). La capacidad de transformar datos en inteligencia es el valor central que se espera de nosotros en un entorno real.
