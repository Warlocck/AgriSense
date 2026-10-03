# AgriSense

Plataforma web full-stack orientada a la comercialización directa de productos agrícolas, conectando agricultores con consumidores finales y reduciendo la intermediación en la cadena de venta.

## Descripción

AgriSense nace como una propuesta de startup para facilitar la comercialización de productos agrícolas mediante una plataforma digital.

El sistema permite gestionar productos, usuarios, carritos y pedidos, contemplando diferentes roles dentro de la plataforma.

## Funcionalidades

* Registro e inicio de sesión de usuarios.
* Autenticación mediante JWT.
* Gestión de usuarios según su rol.
* Gestión y publicación de productos agrícolas.
* Carrito de compras.
* Gestión de pedidos.
* Seguimiento de pedidos.
* Paneles diferenciados para agricultores, consumidores y administradores.
* Persistencia de información mediante PostgreSQL.
* Protección de rutas mediante middleware de autenticación.

## Roles

### Agricultor

* Gestiona sus productos.
* Publica productos disponibles para la venta.
* Participa directamente en la comercialización.

### Consumidor

* Consulta productos disponibles.
* Agrega productos al carrito.
* Gestiona sus compras.
* Consulta y realiza seguimiento de sus pedidos.

### Administrador

* Accede a funcionalidades de administración de la plataforma.

## Arquitectura

El proyecto utiliza una arquitectura separada entre frontend y backend:

```text
AgriSense
├── backend
│   └── API REST con Node.js + Express
│
└── fronted
    └── Aplicación web con React
```

## Tecnologías

### Frontend

* React 19
* TypeScript
* Tailwind CSS
* React Hook Form
* Radix UI
* Lucide React
* Recharts

### Backend

* Node.js
* Express 5
* TypeScript
* PostgreSQL
* JSON Web Token (JWT)
* bcrypt
* CORS
* dotenv

## Estructura del proyecto

```text
AgriSense/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── middlewares/
│   │   ├── routes/
│   │   ├── db.ts
│   │   └── index.ts
│   ├── package.json
│   └── tsconfig.json
│
├── fronted/
│   ├── src/
│   │   ├── components/
│   │   ├── guidelines/
│   │   └── styles/
│   ├── public/
│   └── package.json
│
└── .gitignore
```

## Instalación

### Backend

```bash
cd backend
npm install
```

Crear un archivo `.env` utilizando `.env.example` como referencia:

```env
DB_HOST=localhost
DB_PORT=5432
DB_USER=postgres
DB_PASSWORD=tu_contraseña
DB_NAME=agrisense
JWT_SECRET=tu_clave_secreta
```

Ejecutar en desarrollo:

```bash
npm run dev
```

### Frontend

En otra terminal:

```bash
cd fronted
npm install
npm start
```

## Objetivo del proyecto

El proyecto busca demostrar cómo una solución tecnológica puede utilizarse para conectar productores agrícolas con consumidores finales, facilitando la comercialización de productos y reduciendo la dependencia de intermediarios.

## Estado

Proyecto académico desarrollado como propuesta de solución tecnológica y modelo de startup.
