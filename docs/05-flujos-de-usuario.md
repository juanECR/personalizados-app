# Documento 5
# Flujos de Usuario

Proyecto:
Personalizados App

Versión:
1.0

---

# Objetivo

Definir el recorrido completo de los usuarios dentro de la aplicación.

Este documento describe únicamente el comportamiento del sistema, no su implementación técnica.

---

# Tipos de Usuario

El sistema tendrá únicamente dos tipos de usuario.

## Cliente

Usuario que visita el catálogo.

No necesita registrarse.

No inicia sesión.

Su objetivo es encontrar un diseño y solicitarlo por WhatsApp.

---

## Administrador

Usuario autorizado.

Accede mediante Login.

Gestiona toda la información del sistema.

---

# FLUJOS DEL CLIENTE

--------------------------------------------------

## Flujo 1
### Explorar el catálogo

Inicio

↓

Carga del catálogo

↓

Visualiza los diseños

↓

Puede desplazarse por la página

↓

Fin

---

Resultado esperado

El usuario puede explorar libremente todos los diseños disponibles.

---

## Flujo 2
### Buscar un diseño

Inicio

↓

Escribe una palabra

↓

El sistema filtra los diseños

↓

Visualiza resultados

↓

Selecciona uno

↓

Detalle del diseño

---

La búsqueda deberá considerar:

- Nombre
- Etiquetas

---

## Flujo 3
### Filtrar por categoría

Inicio

↓

Selecciona una categoría

↓

El catálogo muestra únicamente los diseños pertenecientes a esa categoría

↓

Selecciona un diseño

↓

Detalle

---

## Flujo 4
### Ver un diseño

Inicio

↓

Abre el detalle

↓

Visualiza:

Imagen principal

Nombre

Categorías

Descripción

Productos compatibles

↓

Selecciona un producto

↓

Actualiza:

Mockup

Precio

↓

Solicitar por WhatsApp

↓

Fin

---

## Flujo 5
### Solicitar por WhatsApp

Inicio

↓

Selecciona producto

↓

Presiona botón

↓

Se abre WhatsApp

↓

Mensaje generado automáticamente

↓

El cliente envía el mensaje

↓

Fin

---

Mensaje

Hola.

Quiero solicitar el siguiente producto.

Código:

DSN-000215

Diseño:

Naruto Hokage

Producto:

Taza Blanca

Precio:

S/.25.00

---

# FLUJOS DEL ADMINISTRADOR

--------------------------------------------------

## Flujo 6
### Iniciar sesión

Inicio

↓

Correo

↓

Contraseña

↓

Validación

↓

Dashboard

↓

Fin

---

## Flujo 7
### Registrar un producto

Dashboard

↓

Productos

↓

Nuevo

↓

Nombre

↓

Precio

↓

Imagen (opcional)

↓

Guardar

↓

Producto registrado

---

## Flujo 8
### Registrar categoría

Dashboard

↓

Categorías

↓

Nuevo

↓

Nombre

↓

Guardar

↓

Categoría creada

---

## Flujo 9
### Registrar etiqueta

Dashboard

↓

Etiquetas

↓

Nueva

↓

Nombre

↓

Guardar

↓

Etiqueta creada

---

## Flujo 10
### Registrar un diseño

Dashboard

↓

Diseños

↓

Nuevo

↓

Información General

Nombre

Descripción

Imagen principal

Enlace Google Drive

↓

Seleccionar Categorías

↓

Registrar Etiquetas

↓

Seleccionar Productos Compatibles

↓

Subir Mockup para cada producto

↓

Guardar

↓

Código generado automáticamente

↓

Diseño registrado

---

## Flujo 11
### Editar diseño

Dashboard

↓

Buscar diseño

↓

Editar

↓

Modificar información

↓

Guardar

↓

Actualización correcta

---

El código nunca podrá modificarse.

---

## Flujo 12
### Buscar diseño

Dashboard

↓

Buscar código

↓

Resultado

↓

Nombre

Código

Drive

Categorías

Etiquetas

Productos compatibles

↓

Fin

---

## Flujo 13
### Eliminar diseño

Dashboard

↓

Eliminar

↓

Confirmación

↓

Validación

↓

Si existen restricciones

↓

Mostrar mensaje

↓

Cancelar eliminación

---

Si no existen restricciones

↓

Eliminar relaciones

↓

Eliminar diseño

↓

Fin

---

# VALIDACIONES

Diseños

Nombre obligatorio.

Imagen principal obligatoria.

Al menos una categoría.

Al menos un producto compatible.

Drive obligatorio.

---

Productos

Nombre obligatorio.

Precio obligatorio.

---

Categorías

Nombre obligatorio.

---

Etiquetas

Nombre obligatorio.

---

# MENSAJES

Registro correcto.

Actualización correcta.

Eliminación correcta.

Error inesperado.

Datos incompletos.

Código no encontrado.

---

# COMPORTAMIENTOS

Todos los formularios deberán:

Validar antes de enviar.

Mostrar errores debajo del campo.

Bloquear el botón mientras se guarda.

Mostrar notificación al finalizar.

---

# REGLAS DE NEGOCIO

Un diseño:

Debe tener al menos un producto compatible.

Puede pertenecer a varias categorías.

Puede tener múltiples etiquetas.

Tiene un único código.

Tiene un único archivo original.

Puede tener un mockup diferente para cada producto compatible.

---

Un producto:

Tiene un único precio.

Puede utilizarse en muchos diseños.

---

Un mockup:

Siempre pertenece a la relación entre un diseño y un producto.

Nunca representa el archivo de impresión.

---

El archivo original:

Siempre pertenece al diseño.

Nunca pertenece al producto.

Nunca pertenece al mockup.

---

# FIN DEL DOCUMENTO
