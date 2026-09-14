---
title: "Conceptualización"
layout: default
---

[← Volver al inicio](index.md)

# Entrega 1 · Conceptualización

> *Punto de partida: entender el problema y encuadrar el proyecto.*

---

## 1. Presentación del proyecto

**Nombre del sistema:** Cordillera CRM

**Integrantes del grupo:**

| Nombre | Rol |
|---|---|
| Sergio Adrian Brun Vargas | Arquitectura de Datos, Backend y Seguridad (Líder Técnico) |
| Eber Moises Aldama Villagra | Desarrollo Frontend y Diseño de Interfaz (UX/UI) |
| Luis Angel Martinez Chena | Control de Calidad (QA) y Gestor de Integraciones |

**Usuario / cliente real:** AC - INVERSIONES CORDILLERA

---

## 2. Definición del problema

"Actualmente, la gestión de clientes y la venta de terrenos se realiza de manera fragmentada y manual. La empresa depende de complejas hojas de cálculo para administrar su inventario inmobiliario, recurriendo a fórmulas anidadas para extraer y organizar identificadores de propiedades (como el ID del lote o el número de padrón) y llevar el control de las cuotas en los estados de cuenta (cta cte). Además, las negociaciones se dispersan en cadenas de mensajes de WhatsApp. Esta falta de centralización provoca confusión sobre qué terrenos están disponibles, reservados o vendidos, demoras en el seguimiento de prospectos y cobros, y un alto riesgo de errores al no tener un embudo de ventas claro que guíe al cliente desde la consulta inicial hasta la firma del contrato."¿Qué dificultades enfrenta?]

---

## 3. Propósito y objetivos

**Objetivo general:**

Desarrollar e implementar un sistema web de Gestión de Relaciones con Clientes (CRM) que centralice, organice y automatice el seguimiento de los procesos comerciales y operativos de la empresa.

**Objetivos específicos:**

1. Centralizar la base de datos de clientes y el historial de interacciones en una única plataforma accesible y segura.
2. Digitalizar el control de estado de cuentas y seguimiento de servicios, eliminando la dependencia de planillas de cálculo dispersas.
3. Proveer un panel de control (Dashboard) que brinde una visión panorámica e indicadores en tiempo real sobre el estado del negocio.

---

## 4. Alcance del proyecto

**Incluye (dentro del alcance):**

- Módulo de gestión de contactos y empresas (Registro, edición y categorización).

- Módulo de seguimiento de oportunidades de venta y estado de trámites (Pipeline).

- Registro de historial de actividades (llamadas, reuniones, correos) por cada cliente.

- Panel de control (Dashboard) con métricas básicas (clientes activos, trámites pendientes).

**No incluye (fuera de alcance):**

- Sistema de facturación electrónica integrado con la SET.

- Módulo de contabilidad pura (liquidación de impuestos, generación de libros contables).

- Aplicación móvil nativa (se accederá vía web responsive).
---

## 5. Interesados (stakeholders)

| Interesado | Descripción | Interés en el proyecto |
|---|---|---|
| Auxiliares / Ejecutivos | Empleados que interactúan en el día a día con los clientes. | Contar con una herramienta rápida y fácil de usar para registrar tareas y buscar información sin perder tiempo. |
| Gerencia / Propietario | Dueño de la empresa o líder del equipo. | Obtener una visión panorámica y control sobre el rendimiento del equipo, fidelizar clientes y asegurar que ningún trámite quede en el olvido. |
| Equipo de Desarrollo | Sergio, Luis y Eber (estudiantes de Ingeniería en Informática). | Construir un software robusto, escalable y seguro que cumpla con los estándares académicos y profesionales, resolviendo un problema real del mercado. |

---

## 6. Justificación / viabilidad

**Viabilidad técnica:** El equipo está compuesto por estudiantes de la carrera de Ingeniería en Informática con los conocimientos necesarios en estructuración de bases de datos, lógica de programación y desarrollo de interfaces. Las tecnologías a utilizar cuentan con amplia documentación y soporte comunitario.

**Viabilidad operativa:** El sistema se diseñará priorizando la usabilidad (interfaz intuitiva). Esto garantiza que los usuarios finales puedan adoptar la herramienta con una curva de aprendizaje mínima, reemplazando sus herramientas actuales (Excel/papel) sin interrumpir sus operaciones diarias.

**Viabilidad económica (alto nivel):** El proyecto es altamente viable, ya que en esta fase de desarrollo se utilizarán herramientas, frameworks y motores de bases de datos de código abierto (Open Source). Los costos de infraestructura inicial (servidores en la nube para pruebas) son mínimos y asumibles por el equipo.
---

## 7. Visión general de la solución

Cordillera CRM será una plataforma web donde cada miembro de la empresa tendrá su propio usuario. Al ingresar, verán un panel principal con los clientes que requieren atención urgente y los trámites en curso. En lugar de buscar datos en diferentes archivos, con un par de clics podrán acceder al perfil completo de un cliente, ver sus saldos, qué servicios tiene contratados y cuál fue la última conversación que el equipo tuvo con él, logrando una gestión "de altura" y sin fricciones.

---

## 8. Glosario de términos

| Término | Definición |
|---|---|
| CRM | Customer Relationship Management. Software utilizado para administrar y analizar las interacciones con los clientes. |
| Dashboard | Tablero visual de información que muestra métricas clave y el estado general de los procesos en tiempo real. |
| Pipeline (Embudo) | Representación visual de las distintas etapas por las que pasa un cliente o un trámite, desde el inicio hasta su conclusión. |

---

## 9. Riesgos iniciales

| Riesgo | Impacto | Estrategia de mitigación |
|---|---|---|
| Resistencia al cambio por parte de los usuarios (acostumbrados a usar Excel y papel). | Alto | Diseñar una interfaz extremadamente limpia y amigable; involucrar al usuario final desde las primeras pruebas para que sientan el sistema como propio. |
| Pérdida de integridad de datos durante la migración de la información antigua al nuevo sistema. | Alto | Desarrollar scripts de limpieza de datos robustos (ej. manejar correctamente caracteres especiales o formatos inconsistentes) y realizar pruebas en bases de datos aisladas antes del paso a producción. |
| Desajustes en la coordinación del equipo de desarrollo (arquitectura vs frontend). | Medio | Aplicar una metodología ágil con reuniones de sincronización cortas y control de versiones estricto (Git). |

---

## 10. Selección tecnológica preliminar

| Componente | Elección | Justificación breve |
|---|---|---|
| Lenguaje de programación | [ej. Python / Java / TypeScript] | [por qué] |
| Framework | [ej. Django / Spring Boot / React] | [por qué] |
| Base de datos | [ej. PostgreSQL / MongoDB] | [por qué] |

---

[← Volver al inicio](index.md) · [Siguiente: Análisis →](analisis.md)
