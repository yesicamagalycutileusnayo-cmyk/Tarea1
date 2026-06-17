# 🛒 SISTEMA WEB MINIMARKET SANTA MARÍA

Este proyecto consiste en el desarrollo e implementación de un sistema web para la gestión de productos de un minimarket, orientado al control de inventario y administración de datos en línea.

La solución fue diseñada bajo una arquitectura moderna basada en servicios en la nube, permitiendo que el sistema funcione de manera desacoplada, escalable y accesible desde cualquier navegador sin necesidad de servidores locales.

El enfoque del proyecto prioriza la simplicidad operativa, la automatización del despliegue y la integración de herramientas cloud actuales utilizadas en entornos reales de desarrollo web.

---

## ⚙️ ENFOQUE DEL SISTEMA

El sistema está construido bajo un modelo **JAMstack**, donde cada componente cumple una función específica:

- La interfaz de usuario se ejecuta completamente en el navegador.
- Los datos se gestionan en una base de datos remota.
- El despliegue se realiza de forma automática mediante integración continua.

Esto permite un flujo de desarrollo más limpio, rápido y mantenible, reduciendo la dependencia de servidores tradicionales.

---

## 🧩 STACK TECNOLÓGICO

- **Frontend:** HTML5, CSS3 y JavaScript modular nativo
- **Backend as a Service:** Supabase (PostgreSQL + API REST + autenticación)
- **Hosting y despliegue:** Vercel con integración CI/CD desde GitHub
- **Control de versiones:** GitHub como repositorio central del proyecto

---

## 📁 ESTRUCTURA GENERAL DEL PROYECTO

El sistema se encuentra organizado en archivos planos ubicados en la raíz del proyecto:

- `index.html` → Interfaz del cliente y catálogo de productos
- `admin.html` → Panel administrativo para gestión del inventario
- `cliente.js` → Lógica del catálogo y operaciones del usuario
- `admin.js` → Lógica de administración y control CRUD
- `config.js` → Conexión con servicios cloud (Supabase)
- `estilos.css` → Estilos visuales globales del sistema

---

## 🚀 DESPLIEGUE EN LA NUBE

El sistema fue publicado utilizando un flujo automatizado:

GitHub → Vercel → Producción

Cada actualización en el repositorio genera un nuevo despliegue automático, permitiendo mantener la aplicación en línea sin procesos manuales de servidor.

---

## 🔗 URL DEL SISTEMA

👉 https://minimarket-five.vercel.app/
