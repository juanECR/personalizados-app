# Wireframes

## Proyecto

Personalizados App

---

# Filosofía de diseño

La aplicación deberá ser:

- Mobile First.
- Muy rápida.
- Minimalista.
- Fácil de navegar.
- Muy visual.
- Enfocada en convertir visitas en consultas por WhatsApp.

No será un ecommerce tradicional.

No existirá carrito.

No existirá checkout.

Todo el recorrido del usuario terminará en WhatsApp.

---

# Mapa del sitio

CATÁLOGO

```
Inicio
│
├── Catálogo
│
├── Detalle del Diseño
│
└── WhatsApp
```

ADMINISTRADOR

```
Login
│
└── Dashboard
      │
      ├── Diseños
      ├── Productos
      ├── Categorías
      └── Etiquetas
```

---

# FRONTEND

## Página Inicio

Objetivo:

Presentar rápidamente el catálogo.

Wireframe

```
------------------------------------------------

LOGO

Buscar...

------------------------------------------------

Categorías

[Todas]

[Anime]

[Marvel]

[Disney]

[Mascotas]

...

------------------------------------------------

Diseños

□□□□□□□□□□□□□□□□

□□□□□□□□□□□□□□□□

□□□□□□□□□□□□□□□□

□□□□□□□□□□□□□□□□

------------------------------------------------

Paginación

```

Cada tarjeta mostrará:

```
Imagen principal

Nombre

Categorías

Botón

Ver Diseño
```

No se mostrará precio.

No se mostrará producto.

---

# Búsqueda

La búsqueda será instantánea.

Permitirá buscar por:

- Nombre.
- Etiquetas.

Ejemplo

```
Naruto

↓

Resultados
```

---

# Filtros

Filtros disponibles:

Categorías.

No se implementarán más filtros en la primera versión.

---

# Tarjeta del diseño

```
+----------------------+

Imagen

Naruto Hokage

Anime

Ver diseño

+----------------------+
```

---

# Detalle del diseño

Objetivo:

Permitir al cliente escoger el producto.

```
------------------------------------------------

Imagen principal

------------------------------------------------

Nombre

Categorías

Descripción (opcional)

------------------------------------------------

Producto

[ Seleccionar ]

▼

Taza

Polo

Tomatodo

Mousepad

------------------------------------------------

Mockup

------------------------------------------------

Precio

S/. 25.00

------------------------------------------------

Botón

Solicitar por WhatsApp

------------------------------------------------
```

---

# Funcionamiento del selector

Cuando el usuario cambie el producto:

```
Taza

↓

Mockup taza

↓

Precio taza
```

Luego

```
Polo

↓

Mockup polo

↓

Precio polo
```

Todo ocurrirá sin recargar la página.

---

# Botón WhatsApp

Al presionar:

```
Hola.

Quiero cotizar:

Código:
DSN-000215

Diseño:
Naruto Hokage

Producto:
Taza Blanca

Precio:
S/.25.00
```

---

# ADMINISTRADOR

## Login

```
Correo

Contraseña

Ingresar
```

---

# Dashboard

Pantalla inicial.

Mostrará accesos rápidos.

```
----------------------------

Diseños

Productos

Categorías

Etiquetas

----------------------------
```

No tendrá gráficos.

No tendrá estadísticas.

---

# Pantalla Diseños

```
Buscar código

[____________]

+ Nuevo Diseño

------------------------------------

Tabla

Código

Nombre

Categorías

Productos compatibles

Editar

Eliminar
```

---

# Nuevo Diseño

Se dividirá en bloques.

---

## Información General

```
Nombre

Descripción

Imagen principal

Enlace Drive
```

---

## Categorías

```
☑ Anime

☑ Disney

☐ Navidad

☐ Profesiones
```

---

## Etiquetas

```
Naruto

Ninja

Akatsuki
```

---

## Productos compatibles

```
☑ Taza

Subir mockup

-----------------------

☑ Polo

Subir mockup

-----------------------

☐ Gorra

-----------------------

☑ Mousepad

Subir mockup
```

---

Guardar

Cancelar

---

# Productos

```
Nombre

Precio

Imagen (opcional)

Guardar
```

---

# Categorías

```
Nombre

Guardar
```

---

# Etiquetas

```
Nombre

Guardar
```

---

# Responsive

## Celular

Una sola columna.

Todo apilado.

---

## Tablet

Dos columnas cuando sea posible.

---

## Escritorio

Mayor ancho.

Sidebar para el administrador.

---

# Componentes reutilizables

Frontend

- Navbar
- Buscador
- Tarjeta de diseño
- Selector de producto
- Selector de categorías
- Botón WhatsApp
- Paginación
- Footer

Administrador

- Sidebar
- Header
- Tabla
- Modal
- Formulario
- Selector múltiple
- Upload Image
- Buscador
