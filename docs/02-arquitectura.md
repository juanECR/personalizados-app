# Arquitectura del Sistema

# Nombre del proyecto

**Personalizados App**

---

# Arquitectura General

El sistema seguirá una arquitectura desacoplada basada en cliente-servidor.

```text
                        INTERNET
                            │
                            │
                   ┌─────────────────┐
                   │    Frontend     │
                   │ React + Vite    │
                   └────────┬────────┘
                            │
                       HTTPS (REST API)
                            │
                            ▼
                   ┌─────────────────┐
                   │     Backend     │
                   │ Node.js + Express│
                   └────────┬────────┘
                            │
        ┌───────────────────┼────────────────────┐
        │                   │                    │
        ▼                   ▼                    ▼
┌────────────────┐  ┌────────────────┐  ┌─────────────────┐
│   Supabase     │  │   Cloudinary   │  │  Google Drive   │
│ PostgreSQL DB  │  │    Imágenes    │  │ Archivo maestro │
└────────────────┘  └────────────────┘  └─────────────────┘
```

---

# Responsabilidad de cada componente

## Frontend

El frontend será una aplicación SPA desarrollada con React.

Responsabilidades:

- Mostrar el catálogo público.
- Mostrar el detalle de los diseños.
- Administrar el panel privado.
- Consumir la API.
- Validaciones básicas del formulario.
- Manejo del estado de la interfaz.

El frontend nunca accederá directamente a la base de datos.

---

## Backend

El backend será el núcleo del sistema.

Responsabilidades:

- Exponer la API REST.
- Validar información.
- Gestionar autenticación.
- Gestionar permisos.
- Comunicarse con Supabase.
- Gestionar la subida de imágenes a Cloudinary.
- Responder al frontend.

Todo acceso a los datos pasará por el backend.

---

## Base de datos

Supabase almacenará exclusivamente información estructurada.

Ejemplo:

- Diseños
- Productos
- Categorías
- Etiquetas
- Relaciones entre entidades
- Usuarios

No almacenará archivos multimedia.

---

## Cloudinary

Cloudinary almacenará únicamente imágenes.

Tipos de imágenes:

- Imagen principal del diseño.
- Mockups.
- Miniaturas generadas automáticamente.

Cloudinary proporcionará:

- Optimización.
- CDN.
- Conversión automática.
- Redimensionamiento.

---

## Google Drive

Google Drive almacenará únicamente el archivo original del diseño.

Ejemplos:

- PNG
- WEBP

La aplicación únicamente almacenará el enlace al archivo.

---

# Flujo de un cliente

```text
Cliente

↓

Catálogo

↓

Detalle del diseño

↓

Selecciona producto

↓

Visualiza mockup

↓

Visualiza precio

↓

Botón WhatsApp

↓

Negocio
```

---

# Flujo del administrador

```text
Administrador

↓

Login

↓

Panel

↓

Registrar diseño

↓

Subir imagen principal

↓

Registrar enlace Drive

↓

Seleccionar categorías

↓

Registrar etiquetas

↓

Seleccionar productos compatibles

↓

Subir mockups

↓

Guardar
```

---

# Principios de arquitectura

## Desacoplamiento

Frontend y Backend funcionarán de manera independiente.

---

## Responsabilidad única

Cada componente tendrá una única responsabilidad.

Ejemplos:

Frontend → Interfaz.

Backend → Lógica.

Supabase → Datos.

Cloudinary → Imágenes.

Google Drive → Archivos originales.

---

## Escalabilidad

El sistema deberá permitir agregar nuevos módulos sin modificar la arquitectura principal.

---

## Mantenibilidad

Toda la lógica del negocio estará centralizada en el backend.

El frontend será un consumidor de la API.

---

## Seguridad

La base de datos nunca será accesible directamente desde el frontend.

Todo acceso será mediante la API.

---

# Flujo de comunicación

```text
Frontend

↓

API REST

↓

Backend

↓

Base de datos

↓

Respuesta JSON

↓

Frontend
```

---

# Integraciones externas

## WhatsApp

El sistema no enviará mensajes automáticamente.

Únicamente abrirá un enlace con un mensaje predefinido utilizando la API oficial de WhatsApp (`wa.me`).

---

## Cloudinary

El backend será responsable de subir y eliminar imágenes.

---

## Google Drive

El administrador registrará manualmente el enlace al archivo original.

No existirá integración directa con la API de Google Drive en la primera versión.

---

# Arquitectura objetivo

La aplicación será modular.

Cada módulo podrá evolucionar de forma independiente sin afectar el resto del sistema.
