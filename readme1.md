# 🛒 SISTEMA WEB MINIMARKET SANTA MARÍA

Este proyecto consiste en el desarrollo e implementación de un sistema web para la gestión de productos de un minimarket, orientado al control de inventario y administración en línea.

El sistema fue diseñado bajo una arquitectura moderna basada en servicios en la nube, aplicando el enfoque **JAMstack**, lo que permite desacoplar el frontend, backend y despliegue, logrando mayor escalabilidad, rendimiento y facilidad de mantenimiento.

---

## ⚙️ ENFOQUE DEL SISTEMA

El sistema sigue una arquitectura distribuida donde cada componente cumple una función específica:

- Interfaz de usuario ejecutada en el navegador (Frontend)
- Base de datos en la nube con acceso seguro (Supabase)
- Despliegue automatizado en plataforma serverless (Vercel)
- Control de versiones centralizado (GitHub)

Este enfoque permite que el sistema funcione sin necesidad de servidores locales tradicionales.

---

## 🧩 STACK TECNOLÓGICO

- HTML5, CSS3, JavaScript (Frontend)
- Supabase (Backend as a Service con PostgreSQL)
- Vercel (Hosting y despliegue automático)
- GitHub (Control de versiones y CI/CD)

---

## 📁 ESTRUCTURA DEL PROYECTO

- `index.html` → Interfaz del cliente y catálogo de productos
- `admin.html` → Panel de administración del sistema
- `cliente.js` → Lógica del usuario y consumo de datos
- `admin.js` → Lógica CRUD del inventario
- `config.js` → Conexión con Supabase
- `estilos.css` → Estilos globales

---

# 🚀 PROCESO DE DESPLIEGUE DEL SISTEMA

El despliegue del sistema se realizó mediante un flujo estructurado basado en integración continua y servicios en la nube.

---

## 🔹 1. Desarrollo local del sistema
El proyecto fue desarrollado inicialmente en entorno local utilizando HTML, CSS y JavaScript.  
En esta etapa se construyó:

- Interfaz del cliente
- Panel administrativo
- Lógica de inventario
- Conexión con Supabase mediante API

---

## 🔹 2. Configuración de la base de datos en Supabase
Se creó un proyecto en Supabase con una base de datos PostgreSQL.

Se configuró la tabla principal `productos` con los siguientes campos:

- id (identificador único)
- nombre (texto)
- precio (numérico)
- stock (entero)
- imagen_url (texto)
- creado_en (timestamp)

Además, se activó **Row Level Security (RLS)** para proteger el acceso a los datos:
- Lectura pública para usuarios generales
- Escritura restringida a usuarios autenticados

---

## 🔹 3. Subida del código a GitHub
El código fuente fue subido a GitHub como repositorio público.

Este repositorio permitió:
- Control de versiones del sistema
- Registro de cambios mediante commits
- Integración directa con Vercel

---

## 🔹 4. Conexión con Vercel (Despliegue)
Se conectó el repositorio de GitHub con Vercel.

Vercel realizó automáticamente:

- Detección del proyecto frontend
- Construcción del entorno de producción
- Generación de URL pública HTTPS

Cada actualización en GitHub genera un nuevo despliegue automático (CI/CD).

---

## 🔹 5. Configuración del sistema en producción
Se verificaron los siguientes elementos:

- Conexión correcta con Supabase
- Funcionamiento del catálogo de productos
- Acceso al panel administrativo
- Carga de imágenes desde URLs externas
- Persistencia de datos en la nube

---

## 🌐 URL DEL SISTEMA EN PRODUCCIÓN

👉 https://minimarket-five.vercel.app/

---

## 🧠 RESULTADO DEL DESPLIEGUE

El sistema fue desplegado exitosamente en la nube logrando:

- Acceso público desde cualquier navegador
- Integración completa frontend + backend
- Base de datos en tiempo real
- Actualización automática mediante GitHub + Vercel
- Arquitectura completamente serverless

---

## 📌 CONCLUSIÓN TÉCNICA

El proceso de despliegue permitió comprender un flujo real de desarrollo moderno, donde el código pasa de un entorno local a un entorno productivo sin necesidad de servidores físicos.

La combinación de Supabase, Vercel y GitHub representa una arquitectura actual utilizada en proyectos profesionales basados en la nube.
