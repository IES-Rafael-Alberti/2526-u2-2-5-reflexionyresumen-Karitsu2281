# Evidencia 1: Reglas de Snort (Explicación y Ejemplos)

### 1.1) ¿Cómo funciona una regla de Snort de forma rápida?
- Se divide en dos: **Cabecera** (quién se comunica y cómo) y **Opciones** (detalle a buscar).
- **Cabecera:** `[Acción] [Protocolo] [Origen] -> [Destino]` (ej. alerta TCP hacia mi servidor).
- **Opciones:** Entre paréntesis. Define qué buscar (`content`), qué decir (`msg`) y su ID (`sid`).

### 1.2) Ejemplos de reglas implementadas
- **Admin HTTP:** `alert tcp any any -> 192.168.1.100 80 (msg:"Intento admin"; content:"/admin.php"; sid:1000001; rev:1;)`
- **Pings ICMP:** `alert icmp any any -> 192.168.1.100 any (msg:"Ping detectado"; itype:8; sid:1000002; rev:1;)`
- **Acceso SSH:** `alert tcp any any -> 192.168.1.100 22 (msg:"Intento SSH"; flags:S; sid:1000003; rev:1;)`

### 1.3) Justificación de las reglas elegidas
- **HTTP:** Vital para proteger y registrar accesos a paneles de administración web.
- **ICMP:** Ayuda a identificar fases de reconocimiento (escaneo) por posibles atacantes.
- **SSH:** Permite monitorear inicios de sesión remotos y descubrir intentos de fuerza bruta.