# Documento 6

# API REST

Proyecto

Personalizados App

Versión

1.0

---

# Arquitectura

Frontend

↓

HTTP

↓

Express API

↓

Supabase

Todas las respuestas serán en formato JSON.

---

# URL Base

/api/v1

---

# Autenticación

Solo el panel administrador requerirá autenticación.

El catálogo será completamente público.

---

# FORMATO DE RESPUESTA

Respuesta correcta

{
    "success": true,
    "message": "Operación realizada correctamente.",
    "data": {}
}

---

Respuesta con error

{
    "success": false,
    "message": "Descripción del error.",
    "errors": []
}

---

# CATÁLOGO

------------------------------------------------

Obtener diseños

GET

/designs

Parámetros

page

limit

search

category

Respuesta

{
    "success": true,
    "data": [
        {
            "code": "DSN-000001",
            "name": "Naruto Hokage",
            "main_image": "...",
            "categories": [
                "Anime"
            ]
        }
    ]
}

---

Obtener detalle de un diseño

GET

/designs/{code}

Respuesta

{
    "success": true,
    "data": {

        "code": "DSN-000001",

        "name": "Naruto Hokage",

        "description": "...",

        "main_image": "...",

        "categories": [],

        "tags": [],

        "products": [

            {

                "id": 1,

                "name": "Taza",

                "price": 25,

                "mockup": "..."

            }

        ]

    }

}

---

Obtener categorías

GET

/categories

---

Buscar diseños

GET

/designs?search=naruto

---

Filtrar por categoría

GET

/designs?category=anime

---

# ADMINISTRADOR

------------------------------------------------

Login

POST

/auth/login

Body

{

"email":"",

"password":""

}

Respuesta

{

"token":""

}

---

Cerrar sesión

POST

/auth/logout

---

# PRODUCTOS

------------------------------------------------

Listar

GET

/products

---

Obtener

GET

/products/{id}

---

Crear

POST

/products

---

Actualizar

PUT

/products/{id}

---

Eliminar

DELETE

/products/{id}

---

# CATEGORÍAS

------------------------------------------------

GET

/categories

POST

/categories

PUT

/categories/{id}

DELETE

/categories/{id}

---

# ETIQUETAS

------------------------------------------------

GET

/tags

POST

/tags

PUT

/tags/{id}

DELETE

/tags/{id}

---

# DISEÑOS

------------------------------------------------

Listar

GET

/designs/admin

---

Buscar por código

GET

/designs/code/{code}

Respuesta

{

"code":"DSN-000125",

"name":"Naruto Hokage",

"drive_url":"...",

"categories":[],

"tags":[],

"products":[]

}

---

Crear

POST

/designs

Body

{

"name":"",

"description":"",

"drive_url":"",

"categories":[],

"tags":[],

"products":[

{

"product_id":1,

"mockup":"..."

}

]

}

---

Actualizar

PUT

/designs/{id}

---

(No se permitirá modificar el código.)

---

Eliminar

(No disponible en la versión 1.)

---

# SUBIDA DE IMÁGENES

POST

/uploads/image

Respuesta

{

"url":"https://..."

}

Cloudinary devolverá la URL optimizada.

---

# CÓDIGOS HTTP

200

Consulta correcta

201

Registro creado

400

Datos inválidos

401

No autenticado

403

Sin permisos

404

No encontrado

409

Conflicto

422

Error de validación

500

Error interno

---

# VERSIONADO

Toda la API será versionada.

Ejemplo

/api/v1

Si en el futuro existen cambios incompatibles:

/api/v2

---

# REGLAS

Nunca devolver información innecesaria.

No exponer datos internos.

No enviar contraseñas.

Todas las consultas utilizarán paginación.

Todas las listas permitirán búsqueda.

Todas las operaciones del administrador requerirán autenticación.

---

FIN DEL DOCUMENTO
