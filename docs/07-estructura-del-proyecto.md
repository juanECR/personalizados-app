# Documento 7

# Estructura del Proyecto

Proyecto

Personalizados App

Versión

1.0

---

# Objetivo

Definir una estructura de carpetas organizada, modular y escalable para facilitar el desarrollo y mantenimiento del sistema.

---

# Arquitectura General

Personalizados App

```
personalizados-app/

├── apps/
│   ├── client/
│   └── admin/
│
├── backend/
│
├── docs/
│
├── README.md
│
└── .gitignore
```

---

# Frontend

Tecnologías

- React
- Vite
- React Router
- Tailwind CSS
- TanStack Query

Estructura

```
frontend/

├── public/

├── src/

│   ├── assets/
│   │
│   ├── components/
│   │
│   ├── layouts/
│   │
│   ├── pages/
│   │
│   ├── routes/
│   │
│   ├── services/
│   │
│   ├── hooks/
│   │
│   ├── context/
│   │
│   ├── utils/
│   │
│   ├── constants/
│   │
│   ├── styles/
│   │
│   ├── App.jsx
│   │
│   └── main.jsx
│
├── package.json
```

---

# Componentes

Los componentes deberán ser reutilizables.

Ejemplo

```
components/

Button/

Card/

Input/

Modal/

Navbar/

Sidebar/

Table/

Toast/

Skeleton/

Pagination/

Search/

ImageUploader/

ProductSelector/
```

Cada componente tendrá su propia carpeta.

Ejemplo

```
Button/

Button.jsx

Button.module.css
```

---

# Pages

```
pages/

Home/

DesignDetail/

Login/

Dashboard/

Designs/

Products/

Categories/

Tags/

NotFound/
```

Cada página representará una ruta.

---

# Services

Responsables de consumir la API.

Ejemplo

```
services/

auth.service.js

design.service.js

product.service.js

category.service.js

tag.service.js

upload.service.js
```

---

# Backend

Tecnologías

- Node.js
- Express
- Supabase

Arquitectura Modular

```
backend/

├── src/

│   ├── modules/
│   │
│   ├── middleware/
│   │
│   ├── config/
│   │
│   ├── utils/
│   │
│   ├── routes/
│   │
│   ├── app.js
│   │
│   └── server.js
│
├── package.json
```

---

# Módulos

Cada módulo representa una entidad del negocio.

```
modules/

auth/

designs/

products/

categories/

tags/

uploads/
```

Cada módulo tendrá exactamente la misma estructura.

Ejemplo

```
designs/

controller.js

service.js

repository.js

routes.js

validator.js
```

---

# Responsabilidad

Controller

Recibe la petición HTTP.

---

Service

Contiene la lógica del negocio.

---

Repository

Consulta la base de datos.

---

Validator

Valida los datos recibidos.

---

# Configuración

```
config/

database.js

cloudinary.js

supabase.js

env.js
```

---

# Middleware

```
middleware/

auth.js

errorHandler.js

notFound.js

validation.js
```

---

# Utilidades

```
utils/

codeGenerator.js

response.js

pagination.js

slug.js
```

---

# Documentación

Toda la documentación vivirá en:

```
docs/

01-vision-del-proyecto.md

02-arquitectura.md

03-base-de-datos.md

04-ui-ux.md

05-flujos-de-usuario.md

06-api-rest.md

07-estructura-del-proyecto.md

08-estandares.md

09-roadmap.md

DECISIONES.md
```

---

# Convención de nombres

Carpetas

kebab-case

Ejemplo

```
design-detail
```

---

Archivos React

PascalCase

Ejemplo

```
DesignCard.jsx

ProductSelector.jsx
```

---

Archivos JavaScript

camelCase

Ejemplo

```
codeGenerator.js

uploadService.js
```

---

Variables

camelCase

Ejemplo

```
designCode
```

---

Constantes

UPPER_SNAKE_CASE

Ejemplo

```
MAX_UPLOAD_SIZE
```

---

# Variables de entorno

Nunca se subirán al repositorio.

Archivo

```
.env
```

Ejemplo

```
PORT=

SUPABASE_URL=

SUPABASE_KEY=

JWT_SECRET=

CLOUDINARY_NAME=

CLOUDINARY_KEY=

CLOUDINARY_SECRET=
```

---

# Git

Rama principal

```
main
```

Rama desarrollo

```
develop
```

Cada nueva funcionalidad utilizará una rama propia.

Ejemplo

```
feature/login

feature/designs

feature/products
```

---

# Objetivo

La estructura deberá permitir que cualquier desarrollador pueda localizar un archivo en pocos segundos y añadir nuevas funcionalidades sin reorganizar el proyecto.
