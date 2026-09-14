# Cordillera CRM — Trabajo Práctico Integrador

> Plantilla base para el repositorio del grupo. Reemplacen todo el texto entre `[corchetes]` por la información real de su proyecto.

Este repositorio contiene el análisis y diseño del sistema **Cordillera CRM**, desarrollado como Trabajo Práctico Integrador de la asignatura **Ingeniería de Software**.

El sitio publicado en GitHub Pages es la entrega oficial del trabajo. **No se envían archivos impresos ni copias por otros medios.**

🔗 **Sitio publicado:** `https://adroan32.github.io/LUADSB-INMO/`

---

## Integrantes del grupo

| Nombre completo | Rol / Responsabilidad principal | Usuario de GitHub |
|---|---|---|
| Eber Aldama | Análisis de requisitos | @ebermoisesav |
| Luis Martinez | Modelado y diagramas | @luischena77-star |
| Adrian Brun | Diseño técnico y documentación | @adroan32 |

## Usuario / cliente real

**AC - INVERSIONES CORDILLERA** — AC Inversiones Cordillera es una agencia de bienes raíces dedicada a la comercialización, desarrollo y administración de propiedades en Caacupé y el departamento de Cordillera, Para dar un salto tecnológico. Buscamos centralizar nuestra información, dejar atrás las planillas manuales y automatizar el control exacto de nuestro inventario (padrones, cuentas corrientes e identificadores). Esto agilizará el trabajo de nuestros agentes y mejorará la atención al cliente.

## Metodología de diseño y desarrollo elegida

Proceso Unificado Ágil / Agile UP (Equilibrio estructurado)

Se optó por Agile UP debido a que ofrece un equilibrio perfecto entre la estructura del Proceso Unificado tradicional y la velocidad de las metodologías ágiles. Esta metodología permite al equipo transitar por fases claras (Inicio, Elaboración, Construcción y Transición) con iteraciones rápidas. Es la elección ideal para estructurar con precisión la complejidad de los datos (gestión de cuotas, identificadores de terrenos y estados de cuenta) durante la fase de Elaboración, mitigando los riesgos técnicos en la arquitectura y seguridad antes de iniciar la etapa intensiva de codificación.

---

## Entregas

| Entrega | Estado | Enlace |
|---|---|---|
| 1. Conceptualización | ✅ Entregado | [Ver documento](docs/conceptualizacion.md) |
| 2. Análisis | 🔲 Pendiente / ✅ Entregado | [Ver documento](docs/analisis.md) |
| 3. Diseño | 🔲 Pendiente / ✅ Entregado | [Ver documento](docs/diseno.md) |

## Estructura del repositorio

```
/docs           → contenido publicado en GitHub Pages (este es el sitio oficial de entrega)
  ├─ index.md          → página principal del sitio
  ├─ conceptualizacion.md
  ├─ analisis.md
  └─ diseno.md
/diagramas      → imágenes o archivos fuente de los diagramas (UML, mockups, etc.)
/src            → código fuente, si el grupo decide avanzar con una implementación
```

## Cómo publicar este sitio en GitHub Pages

1. Suban este repositorio a GitHub (público, o privado con acceso otorgado a la cátedra).
2. Vayan a **Settings → Pages**.
3. En **Source**, seleccionen la rama `main` (o `master`) y la carpeta **/docs**.
4. Guarden. GitHub publicará el sitio en `https://adroan32.github.io/LUADSB-INMO/` en unos minutos.
5. Verifiquen que `docs/index.md` se muestre correctamente como página principal.
6. Actualicen el enlace del sitio arriba en este README y entréguenlo a la cátedra antes de la fecha límite de cada entrega.

> 💡 Tip: cada vez que hagan `push` a la rama publicada, el sitio se actualiza automáticamente. No es necesario volver a configurar nada en las siguientes entregas.
