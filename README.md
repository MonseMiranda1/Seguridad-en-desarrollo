# Seguridad-en-desarrollo
# Actividad: Seguridad 🔐
Es cómo proteger sistemas, redes y datos.

---

## 1. Concepto base

| Concepto | Definición simple | Nivel técnico breve | Ejemplo real |
| --- | --- | --- | --- |
| Permissions | Reglas de quién puede hacer qué | Control de acceso a recursos | Solo admin puede borrar usuarios |
| Password segura | Contraseña difícil de adivinar | Usa letras, números y símbolos | M0nse!2026 |
| Vulnerabilidad | Debilidad en el sistema | Falla que puede ser explotada | Formulario sin validación |
| Intrusión | Acceso no autorizado | Ataque a un sistema | Hacker entra sin permiso |
| Seguridad de red | Protección de datos y sistemas | Medidas para evitar ataques | Uso de firewall y HTTPS |

---

## 2. Permissions 🔑

### ¿Qué significa?
- **Autenticación → Identificación**: Verifica quién eres (login).  
- **Autorización → Permisos**: Define qué puedes hacer (permisos).  

**Diferencia:** primero te identificas, luego te dan acceso según tus permisos.

### Ejemplo developer:
- Login → autentificación, proceso para entrar al sistema  
- Roles (admin/user) → niveles de acceso  

**En APIs:**  
- Usuario hace login → obtiene acceso  
- Según su rol → puede o no usar ciertos endpoints  

### 🧠 Analogía
- **Autenticación** = mostrar tu carnet 🪪  
- **Autorización** = a qué salas puedes entrar  

---

## 3. Password segura 🔒

### ¿Qué la hace segura?
- Larga (mínimo 8-12 caracteres)  
- Mezcla de letras, números y símbolos  
- No usar datos personales  

### ¿Por qué no texto plano?
- Porque si roban la base de datos, ven todas las contraseñas.  

### ¿Qué es hashing?
- Hashing convierte una contraseña o dato en un código irreconocible.  
- **Ejemplo developer:** el backend guarda el hash, no la contraseña real.  

---

## 4. Vulnerabilities ⚠️

### ¿Qué es?
- Una falla que permite atacar el sistema.  

### Tipos comunes:
- **SQL Injection** → ataque donde alguien mete código SQL malicioso en un input para manipular la base de datos  
- **XSS (Cross-Site Scripting)** → inyectar scripts en la web  
- **Exposición de datos** → información visible sin protección  

**Ejemplo:** un input sin validar permite escribir código malicioso.

---

## 5. Intrusión (ATAQUES) 🚨

### ¿Qué es?
- Cuando alguien entra sin permiso a un sistema.  

### ¿Qué busca?
- Robar datos  
- Controlar el sistema  
- Romper la app  

### ¿Qué pasa si ocurre?
- Pérdida de información  
- Daño a usuarios  
- Problemas legales  

**Ejemplo real:** hackeo de una cuenta  

---

## 6. Seguridad de red 🌐

Es el conjunto de medidas para proteger una red, sus datos y dispositivos de accesos no autorizados o ataques.  

### ¿Qué protege?
- Datos  
- Servidores  
- Usuarios  

### Firewall
- Sistema de seguridad que controla el tráfico que entra y sale de una red o dispositivo.  
- Filtro que bloquea accesos no autorizados.  

### HTTPS
- HTTPS = “HyperText Transfer Protocol Secure”  
- Idioma seguro entre navegador y servidor  
- Protege los datos usando encriptación  

**Ejemplo developer:** usar HTTPS evita que roben datos en una API  

---

## 7. En desarrollo (CLAVE) 💻

### Errores comunes:
- No validar inputs  
- No proteger rutas  
- No usar HTTPS  

### ¿Qué pasa si?
- Sin validación → ataques (SQL, XSS)  
- Sin permisos → cualquiera accede  
- Sin HTTPS → datos pueden ser robados  

---

## 8. Caso real 🌍

**“Usuario accede a info que no le corresponde”**  

### ¿Qué falló?
- Permisos mal configurados  

### ¿Qué tipo es?
- Vulnerabilidad + problema de autorización  

### ¿Cómo evitarlo?
- Validar roles  
- Proteger endpoints  
- Revisar accesos en backend  

---

## Analogía

| Concepto | Analogía |
| --- | --- |
| Permissions | Tu tipo de pasaje (económica, business, VIP) |
| Password | Tu pasaporte |
| Vulnerabilidad | Puerta de seguridad sin vigilancia |
| Intrusión | Persona que entra al avión sin ticket |
| Seguridad de red | Todo el sistema de seguridad del aeropuerto |

**💡 Explicado simple:**
- Password (pasaporte) → demuestra quién eres  
- Permissions (pasaje) → define a qué áreas puedes entrar  
- Vulnerabilidad → falla que alguien puede aprovechar  
- Intrusión → alguien se cuela sin permiso  
- Seguridad de red → evita que eso pase
