# Visión del Proyecto

## Nombre del proyecto

**PERSONALIZADOS APP**

> Nombre interno del sistema utilizado durante el desarrollo. El nombre comercial podrá cambiar en cualquier momento sin afectar la arquitectura del software.

---

# Objetivo

Desarrollar una aplicación web que permita administrar y publicar un catálogo de diseños para productos personalizados.

El sistema estará orientado a negocios de personalización (sublimación, estampado e impresión), permitiendo que los clientes exploren un catálogo de diseños, seleccionen un producto compatible y soliciten su compra directamente mediante WhatsApp.

La aplicación reemplazará el proceso tradicional de enviar imágenes por chat, ofreciendo una experiencia organizada, rápida y escalable tanto para el cliente como para el administrador.

---

# Problema que resuelve

Actualmente la búsqueda de diseños suele realizarse mediante carpetas, redes sociales o conversaciones de WhatsApp, lo que genera dificultades para:

- Encontrar rápidamente un diseño específico.
- Mostrar únicamente los diseños compatibles con determinados productos.
- Identificar correctamente el diseño solicitado por el cliente.
- Gestionar un catálogo con cientos o miles de diseños.
- Centralizar la información necesaria para la producción.

El sistema solucionará estos problemas mediante un catálogo digital organizado y un panel administrativo sencillo.

---

# Público objetivo

El sistema está pensado para negocios dedicados a la personalización de productos, tales como:

- Sublimación
- Estampado textil
- Regalos personalizados
- Merchandising
- Impresión bajo demanda

---

# Alcance de la primera versión (MVP)

La primera versión incluirá:

## Catálogo público

- Visualización de diseños.
- Búsqueda por nombre.
- Filtros por categorías.
- Visualización del detalle de cada diseño.
- Selección de productos compatibles.
- Cambio dinámico del mockup según el producto seleccionado.
- Visualización del precio del producto seleccionado.
- Botón para solicitar el producto mediante WhatsApp.

---

## Panel administrador

Gestión completa de:

- Diseños
- Productos
- Categorías
- Etiquetas

Además permitirá:

- Registrar imágenes principales.
- Registrar mockups.
- Registrar enlaces de archivos originales (Google Drive).
- Buscar diseños mediante su código.
- Editar la información existente.

---

# Reglas del negocio

## Diseño

El diseño es la entidad principal del sistema.

Cada diseño posee:

- Un código único generado automáticamente.
- Un nombre.
- Una imagen principal.
- Un enlace al archivo original.
- Una o varias categorías.
- Una o varias etiquetas.
- Uno o varios productos compatibles.

---

## Producto

Cada producto posee:

- Nombre.
- Precio.
- Imagen representativa (opcional).

El precio pertenece exclusivamente al producto.

---

## Mockups

Los mockups son únicamente imágenes de referencia.

Su finalidad es mostrar al cliente cómo luce un diseño aplicado sobre un producto específico.

No forman parte del proceso de producción.

---

## Archivo original

Cada diseño tendrá un único archivo original almacenado en Google Drive.

La aplicación únicamente almacenará el enlace al archivo.

---

## Código del diseño

Cada diseño tendrá un código único.

El código será generado automáticamente por el sistema.

El código nunca podrá modificarse.

El código nunca será reutilizado.

---

## Estados

No existirán estados para los diseños.

Todos los diseños permanecerán disponibles para su utilización.

---

## Eliminación

El sistema no permitirá eliminar un diseño cuando dicha acción comprometa la integridad de la información almacenada.

---

# Tecnologías

## Frontend

- React
- Vite
- React Router
- TanStack Query
- Tailwind CSS

---

## Backend

- Node.js
- Express

---

## Base de datos

- PostgreSQL (Supabase)

---

## Imágenes

- Cloudinary

---

## Archivos originales

- Google Drive

---

# Objetivos de calidad

La aplicación deberá cumplir con los siguientes principios:

- Simplicidad.
- Escalabilidad.
- Alto rendimiento.
- Código modular.
- Fácil mantenimiento.
- Interfaz intuitiva.
- Arquitectura desacoplada entre frontend y backend.

---

# Futuras ampliaciones

La arquitectura deberá permitir incorporar nuevas funcionalidades sin necesidad de rediseñar el sistema.

Ejemplos:

- Nuevos tipos de productos.
- Más categorías.
- Más etiquetas.
- Nuevos canales de contacto.
- Nuevas formas de búsqueda.
