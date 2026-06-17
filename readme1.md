# SISTEMA WEB MINIMARKET

El presente proyecto consiste en el desarrollo e implementación de un sistema web para la gestión de inventario y ventas de un minimarket. La solución está diseñada bajo una arquitectura moderna basada en servicios en la nube, utilizando un enfoque serverless que elimina la necesidad de servidores físicos.

El sistema permite la administración de productos, control de stock y visualización de un catálogo dinámico conectado en tiempo real a una base de datos en la nube.

---

## STACK TECNOLÓGICO

El sistema está compuesto por las siguientes tecnologías:

- **Frontend:** HTML5, CSS3 y JavaScript modular (sin frameworks)
- **Backend as a Service:** Supabase (PostgreSQL + API REST + autenticación)
- **Hosting y despliegue:** Vercel (plataforma serverless con CI/CD automático)
- **Control de versiones:** GitHub (repositorio central del proyecto)

---

## ARQUITECTURA DEL SISTEMA

El sistema sigue una arquitectura desacoplada tipo JAMstack:

Usuario → Frontend (navegador) → API Supabase → Base de datos PostgreSQL  
                     ↓  
               Vercel (hosting y despliegue automático)

Este modelo permite independencia entre capas, facilitando escalabilidad y mantenimiento.

---

## ESTRUCTURA DEL PROYECTO

El proyecto se organiza en archivos planos ubicados en la raíz:

- `index.html` → Interfaz del cliente (catálogo de productos)
- `admin.html` → Panel administrativo (CRUD de inventario)
- `cliente.js` → Lógica del catálogo y consumo de datos
- `admin.js` → Lógica de administración y control de stock
- `config.js` → Configuración de conexión con Supabase
- `estilos.css` → Estilos globales del sistema

---

## DESPLIEGUE DEL SISTEMA

El despliegue se realizó mediante un flujo automatizado basado en integración continua (CI/CD), dividido en las siguientes etapas:

### 1. Configuración del backend en Supabase
Se creó un proyecto en Supabase con base de datos PostgreSQL.

Se implementó la tabla principal `productos` con los siguientes campos:

- id (clave primaria)
- codigo_barras (identificador único del producto)
- nombre (descripción del producto)
- precio (valor numérico)
- stock (cantidad disponible)
- imagen_url (enlace de imagen)

Además, se activó Row Level Security (RLS) para controlar el acceso a los datos:
- Lectura pública para usuarios anónimos
- Escritura restringida a usuarios autenticados

---

### 2. Configuración de credenciales (API)
La conexión entre el frontend y Supabase se realiza mediante el archivo `config.js`.

Este archivo contiene variables de entorno públicas:

- SUPABASE_URL → URL del proyecto en Supabase
- SUPABASE_KEY → clave pública anon para consumo de API

Estas credenciales permiten la comunicación directa con la base de datos desde el frontend.

---

### 3. Versionamiento del código en GitHub
El proyecto fue alojado en un repositorio público de GitHub, lo que permitió:

- Control de versiones del sistema
- Registro de cambios mediante commits
- Integración directa con plataformas de despliegue

---

### 4. Despliegue en Vercel
El repositorio de GitHub fue conectado con Vercel.

Vercel ejecuta automáticamente el proceso de despliegue:

- Detecta el proyecto frontend
- Genera entorno de producción
- Publica una URL HTTPS pública
- Activa despliegue automático (CI/CD)

Cada cambio realizado en GitHub actualiza automáticamente la aplicación en producción.

---

## RESULTADO DEL DESPLIEGUE

El sistema quedó completamente funcional en entorno cloud con:

- Acceso público desde cualquier navegador
- Base de datos en tiempo real con Supabase
- Panel administrativo operativo
- Catálogo dinámico de productos
- Actualizaciones automáticas mediante GitHub + Vercel

---

## URL DEL SISTEMA

https://minimarket-five.vercel.app/
