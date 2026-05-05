# Nova Salud - Sistema Fullstack de Farmacia 🏥💊

Sistema integral para la gestión de inventario y ventas de una botica. Desarrollado con una arquitectura moderna separando el Backend (Node.js/Express) y el Frontend (React/Vite), diseñado para ser escalable, rápido y con una interfaz moderna (Tailwind CSS).

![Nova Salud Dashboard](https://via.placeholder.com/800x400.png?text=Nova+Salud+Dashboard) <!-- Reemplazar con una captura real de la pantalla -->

## 🌟 Características Principales

* **Autenticación Segura:** Sistema de login con JSON Web Tokens (JWT) y roles de usuario (Administrador y Vendedor).
* **Dashboard Interactivo:** Panel de control con métricas en tiempo real, resumen de ventas diarias y gráficas de actividad semanal usando `Recharts`.
* **Alertas de Stock:** Monitoreo y advertencia automática en el dashboard sobre medicamentos con stock crítico/bajo.
* **Gestión de Inventario (CRUD):** Creación, lectura, actualización y eliminación de productos y medicamentos. Búsqueda rápida por código o nombre.
* **Punto de Venta (POS):** Interfaz ágil a doble columna para registrar transacciones y agregar ítems a un ticket.
* **Sincronización Automática:** Al confirmar una venta, el sistema deduce el stock del inventario de forma atómica usando transacciones en la base de datos.
## 💻 Tecnologías Utilizadas



### Backend (`/PROYECTO`)
- **Node.js & Express:** Servidor rápido y estructurado en patrón MVC.
- **SQLite & Sequelize:** Base de datos relacional ligera, manejada a través de un ORM para fácil migración (configurable fácilmente a MySQL o PostgreSQL).
- **JWT & Bcrypt:** Seguridad para contraseñas y sesiones.

### Frontend (`/frontend`)
- **React.js & Vite:** Desarrollo ultrarrápido y renderizado eficiente.
- **Tailwind CSS v4:** Framework de CSS utilitario para un diseño moderno y totalmente responsive.
- **React Router DOM:** Manejo de rutas y layouts.
- **Axios:** Cliente HTTP para la comunicación con el API.
- **Lucide React:** Iconografía moderna y escalable.
---
## 🚀 Instalación y Ejecución Local

Para levantar el proyecto en tu entorno local, asegúrate de tener [Node.js](https://nodejs.org/) instalado. Debes ejecutar el backend y el frontend en dos terminales separadas.

### 1. Levantar el Backend (API)

```bash
cd PROYECTO
npm install
npm run dev
```
> El backend correrá en `http://localhost:3000`.

> *Nota: Al iniciar por primera vez, SQLite creará automáticamente el archivo `database.sqlite` y construirá todas las tablas requeridas.*

### 2. Levantar el Frontend (UI)

```bash
cd frontend
npm install
npm run dev
```

> El frontend estará disponible en `http://localhost:5173`.
---

## 🔐 Credenciales de Acceso por Defecto
Se ha provisto un script (`seedData.js` y `seed.js`) para inyectar datos de prueba y un usuario inicial. Para ingresar al sistema puedes usar:
- **Correo:** `admin@novasalud.com`
- **Contraseña:** `admin123`
---
## 📂 Estructura del Proyecto
```text
/
├── PROYECTO/                 # BACKEND
│   ├── config/               # Conexión a DB (database.js)
│   ├── controllers/          # Lógica de negocio (auth, productos, ventas)
│   ├── middlewares/          # JWT tokens y validaciones
│   ├── models/               # Modelos Sequelize (User, Product, Sale...)
│   ├── routes/               # Endpoints Express
│   ├── database.sqlite       # Base de datos (generada al arrancar)
│   └── server.js             # Punto de entrada
│
└── frontend/                 # FRONTEND
    ├── src/
    │   ├── components/       # Componentes reutilizables (Layout.jsx)
    │   ├── context/          # Estados globales (AuthContext)
    │   ├── pages/            # Vistas (Login, Dashboard, Inventario, POS)
    │   ├── App.jsx           # Rutas (React Router)
    │   └── main.jsx          # Punto de entrada
    └── vite.config.js        # Configuración de Vite y Tailwind v4
```
## 📝 Licencia

Este proyecto es de uso libre / educativo.
