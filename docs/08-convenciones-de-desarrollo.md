# Documento 8

# Convenciones de Desarrollo

Proyecto

Personalizados App

Versión

1.0

---

# Objetivo

Establecer un conjunto de normas y convenciones para garantizar que todo el código del proyecto sea consistente, legible, mantenible y escalable.

Todas las nuevas funcionalidades deberán respetar este documento.

---

# Idioma

## Código

Todo el código será escrito en inglés.

Ejemplos

DesignCard

ProductSelector

CategoryController

getProducts()

createDesign()

---

## Base de datos

Todas las tablas y columnas utilizarán inglés.

Ejemplos

designs

products

categories

tags

design_products

drive_url

main_image

created_at

updated_at

---

## API

Todas las rutas estarán en inglés.

Ejemplo

GET /designs

POST /products

PUT /categories/{id}

DELETE /tags/{id}

---

## Interfaz

Toda la interfaz será en español.

Ejemplos

Catálogo

Productos

Categorías

Guardar

Eliminar

Buscar

---

# Convenciones de nombres

## Carpetas

kebab-case

Ejemplo

design-detail

product-selector

---

## Componentes React

PascalCase

Ejemplo

DesignCard.jsx

Navbar.jsx

ProductSelector.jsx

SearchBar.jsx

---

## Hooks

Siempre comenzarán con use.

Ejemplo

useAuth()

useProducts()

useCategories()

---

## Context

Siempre terminarán en Context.

Ejemplo

AuthContext

ThemeContext

---

## Archivos JavaScript

camelCase

Ejemplo

designService.js

uploadService.js

generateCode.js

---

## Variables

camelCase

Ejemplo

designCode

productPrice

selectedProduct

---

## Constantes

UPPER_SNAKE_CASE

Ejemplo

MAX_UPLOAD_SIZE

DEFAULT_PAGE_SIZE

API_BASE_URL

---

## Funciones

Siempre comenzarán con un verbo.

Ejemplo

createDesign()

updateProduct()

deleteCategory()

generateCode()

formatPrice()

---

# Organización de Componentes

Cada componente tendrá su propia carpeta.

Ejemplo

DesignCard/

├── DesignCard.jsx
├── DesignCard.css
└── index.js

---

# Componentes

Los componentes deberán ser pequeños y reutilizables.

Un componente debe tener una única responsabilidad.

---

# Páginas

Las páginas únicamente organizarán componentes.

No contendrán lógica compleja.

---

# Servicios

Toda comunicación con la API estará centralizada.

Nunca se realizarán llamadas HTTP directamente desde los componentes.

Incorrecto

axios.get(...)

Correcto

designService.getAll()

---

# Estado

Estado global únicamente cuando sea necesario.

Preferir estado local.

Utilizar TanStack Query para datos del servidor.

---

# Formularios

Todos los formularios deberán:

Validar antes de enviar.

Mostrar errores.

Bloquear botón mientras procesa.

Mostrar notificación al finalizar.

---

# Validaciones

Frontend

Validación de experiencia de usuario.

Backend

Validación obligatoria.

Nunca confiar únicamente en el frontend.

---

# Manejo de errores

Nunca utilizar:

alert()

Siempre utilizar:

Toast

Modal

Mensajes visuales.

---

# Imágenes

Todas las imágenes deberán almacenarse en Cloudinary.

Nunca guardar imágenes en el servidor.

---

# Archivos originales

Siempre permanecerán en Google Drive.

La base de datos únicamente almacenará la URL.

---

# API

Todas las respuestas utilizarán el mismo formato.

Éxito

{
  "success": true,
  "message": "",
  "data": {}
}

Error

{
  "success": false,
  "message": "",
  "errors": []
}

---

# Base de datos

Nunca eliminar registros directamente desde SQL.

Toda modificación deberá realizarse mediante la aplicación.

---

# Código del diseño

Formato

DSN-000001

DSN-000002

DSN-000003

El código será:

Único.

Automático.

Inmutable.

---

# Git

Rama principal

main

Rama de desarrollo

develop

Nuevas funcionalidades

feature/nombre-funcionalidad

Correcciones

fix/nombre-error

---

# Commits

Formato

tipo: descripción

Ejemplos

feat: create design module

fix: validate duplicate code

refactor: improve search performance

style: update button spacing

docs: add api documentation

chore: update dependencies

---

# Dependencias

Agregar una librería únicamente si aporta un beneficio claro.

Evitar dependencias innecesarias.

---

# Seguridad

Nunca exponer:

JWT

API Keys

Cloudinary Secret

Supabase Secret

Todas las credenciales utilizarán variables de entorno.

---

# Rendimiento

Lazy Loading.

Code Splitting.

Optimización de imágenes.

Paginación.

Consultas eficientes.

---

# Calidad del código

Funciones pequeñas.

Archivos pequeños.

Sin código duplicado.

Sin variables sin uso.

Sin comentarios innecesarios.

El código debe ser autoexplicativo.

---

# Documentación

Toda nueva funcionalidad deberá actualizar la documentación correspondiente.

Si una decisión modifica la arquitectura o las reglas del negocio, también deberá registrarse en DECISIONES.md.

---

# Regla de oro

Antes de implementar cualquier funcionalidad, responder estas preguntas:

1. ¿Resuelve un problema real del negocio?

2. ¿Mantiene la simplicidad del sistema?

3. ¿Puede reutilizarse?

4. ¿Rompe alguna regla de negocio?

5. ¿Es escalable?

Si alguna respuesta es negativa, la implementación deberá revisarse antes de continuar.

---

# Filosofía del proyecto

Personalizados App no busca tener la mayor cantidad de funciones.

Busca resolver el proceso de venta de productos personalizados de forma rápida, organizada y escalable.

Cada decisión técnica deberá respetar ese objetivo.

---

FIN DEL DOCUMENTO
