---
title: "Análisis - AC Inversiones Cordillera"
layout: default
---

[← Volver al inicio](index.md)

# Entrega 2 · Análisis

> *Definición de las capacidades, alcance y restricciones del sistema de gestión inmobiliaria para AC Inversiones Cordillera, desde la perspectiva del negocio y de los agentes inmobiliarios.*

---

## 1. Requisitos funcionales

| ID | Requisito | Prioridad |
|---|---|---|
| RF-01 | El sistema debe permitir el registro, modificación y baja (lógica) de propiedades inmobiliarias (lotes, casas, departamentos), incluyendo fotos, ubicación y precio. | Alta |
| RF-02 | El sistema debe permitir la asignación de uno o más agentes inmobiliarios a una propiedad específica. | Alta |
| RF-03 | El sistema debe contar con un buscador con filtros múltiples (rango de precio, tipo de propiedad, ciudad/zona, estado) para facilitar el trabajo de los agentes. | Alta |
| RF-04 | El sistema debe registrar los datos de los clientes potenciales (leads) y su historial de interacciones o visitas a propiedades. | Media |
| RF-05 | El sistema debe permitir registrar el cambio de estado de una propiedad (Ej: Disponible, Reservada, Vendida, Alquilada) y generar un comprobante básico de la operación. | Media |

---

## 2. Requisitos no funcionales

| ID | Requisito | Categoría |
|---|---|---|
| RNF-01 | La base de datos debe estar implementada en **PostgreSQL**, garantizando la integridad referencial y el soporte transaccional (ACID) para las operaciones de venta/reserva. | Arquitectura / Datos |
| RNF-02 | El backend del sistema debe estar desarrollado en **Python** (ej. usando frameworks como Django o FastAPI). | Arquitectura |
| RNF-03 | Las imágenes de las propiedades deben optimizarse automáticamente al subirse para no saturar el almacenamiento ni la red, cargando la galería en menos de 3 segundos. | Rendimiento |
| RNF-04 | La interfaz web debe ser "mobile-first", permitiendo a los agentes inmobiliarios consultar datos desde sus teléfonos mientras están en terreno mostrando las propiedades. | Usabilidad |

---

## 3. Modelo de casos de uso

**Diagrama de casos de uso:**

`<img width="777" height="431" alt="image" src="https://github.com/user-attachments/assets/b191129c-ea1f-417d-877e-d207ee9ca358" />
`  
*(Debe mostrar al "Agente", al "Administrador" y al "Cliente/Visitante" interactuando con módulos como Gestión de Propiedades y Gestión de Clientes).*

**Especificación de casos de uso principales:**

### CU-01 · Registrar Nueva Propiedad

- **Actor(es):** Agente Inmobiliario, Administrador.
- **Precondición:** El usuario debe estar autenticado en el sistema.
- **Flujo principal:**
  1. El agente selecciona la opción "Agregar Propiedad".
  2. El sistema despliega el formulario de registro (Datos, Ubicación, Dimensiones, Precio).
  3. El agente completa los datos obligatorios, incluyendo el número de finca o padrón, y sube al menos una fotografía.
  4. El agente guarda los cambios.
  5. El sistema valida los datos, guarda el registro en la base de datos PostgreSQL y asigna el estado "Disponible".
  6. El sistema confirma el registro exitoso.
- **Flujos alternativos:** 
  - *5a. Faltan datos obligatorios:* El sistema resalta los campos faltantes (ej. Precio o Ubicación) y detiene el guardado.
  - *5b. Error de formato en imágenes:* El sistema rechaza archivos que no sean JPG o PNG y solicita una nueva subida.
- **Postcondición:** La nueva propiedad está visible en el catálogo interno para ser ofrecida a los clientes.

---

## 4. Modelo de dominio

**Diagrama de clases conceptual:**

`[Insertar imagen: diagramas/modelo-dominio-inmobiliaria.png]`

**Descripción de entidades principales:**
* **Agente:** Empleado de AC Inversiones Cordillera (Nombre, Teléfono, Email, Porcentaje de comisión).
* **Propiedad:** El bien inmueble (Tipo, Dirección, Ciudad, Dimensiones, Precio, Finca/Padrón, Estado).
* **Cliente:** Persona interesada o comprador final (Nombre, Documento, Teléfono, Preferencias).
* **Transacción:** Registro de la venta, reserva o alquiler (Fecha, Monto final, Tipo de operación, Relaciona a un Agente, un Cliente y una Propiedad).

---

## 5. Diagramas de comportamiento

**Diagrama de secuencia — CU-01: Registrar Nueva Propiedad:**

`[Insertar imagen: diagramas/secuencia-registrar-propiedad.png]`

**Explicación del flujo:** 
El *Agente* envía los datos del formulario a través de la Interfaz. El *Controlador de Propiedades (Python)* recibe el request, valida las reglas de negocio, procesa las imágenes y ejecuta el `INSERT` en la *Base de Datos (PostgreSQL)*. Finalmente, retorna un código HTTP 201 (Created) con el mensaje de éxito a la vista.

---

## 6. Prototipo de interfaz (Mockups)

**Pantalla — Catálogo / Buscador Interno:**

`[Insertar imagen: diagramas/mockup-catalogo-agentes.png]`

**Descripción:** 
Pantalla de uso diario para el agente. Muestra una barra superior con filtros (Ciudad en Cordillera, Rango de Precios, Tipo de Inmueble) y una grilla de tarjetas. Cada tarjeta muestra la foto principal de la propiedad, su estado actual en una etiqueta de color (Verde = Disponible, Rojo = Vendido) y un botón de "Ver detalles".

---

## 7. Reglas del negocio

| ID | Regla |
|---|---|
| RN-01 | Una propiedad marcada como "Vendida" o "Reservada" no puede ser asignada a una nueva transacción hasta que su estado vuelva a "Disponible". |
| RN-02 | Todo inmueble debe tener registrado obligatoriamente su identificador legal (Ej: Número de Finca o Padrón) para evitar duplicidad en la base de datos. |
| RN-03 | Los precios de las propiedades pueden registrarse en Guaraníes (Gs.) o Dólares (USD), pero el sistema debe guardar la moneda de la transacción. |
| RN-04 | Solo un usuario con rol de "Administrador" puede eliminar (baja lógica) una propiedad del sistema o anular una transacción completada. |

---

## 8. Matriz de trazabilidad

| Requisito | Caso(s) de uso relacionado(s) | Módulo / Entidad PostgreSQL |
|---|---|---|
| RF-01 | CU-01 (Registrar Propiedad), CU-02 (Editar Propiedad) | Módulo Propiedades (`tabla: propiedades`) |
| RF-02 | CU-03 (Asignar Agente) | Módulo Agentes (`tabla: agente_propiedad`) |
| RF-03 | CU-04 (Buscar Propiedades) | Módulo Búsqueda |
| RF-05 | CU-05 (Registrar Transacción) | Módulo Transacciones (`tabla: transacciones`) |
---

[← Anterior: Conceptualización](conceptualizacion.md) · [Siguiente: Diseño →](diseno.md)
