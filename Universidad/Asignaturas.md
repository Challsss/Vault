---
tags: [universidad, asignaturas]
---

# 🎓 Asignaturas

> [!tip] Cómo usar
> Registra aquí cada asignatura con todos sus datos. Puedes usar la plantilla `Plantillas/Plantilla Asignatura` para crear notas individuales por asignatura si prefieres más detalle.

## Listado de Asignaturas

| Asignatura | Profesor (Teoría) | Profesor (Seminario) | Profesor (Lab) | Aula Teoría | Aula Seminario | Aula Lab | Créditos |
| ---------- | ----------------- | -------------------- | -------------- | ----------- | -------------- | -------- | -------- |
|            |                   |                      |                |             |                |          |          |
|            |                   |                      |                |             |                |          |          |
|            |                   |                      |                |             |                |          |          |
|            |                   |                      |                |             |                |          |          |
|            |                   |                      |                |             |                |          |          |
|            |                   |                      |                |             |                |          |          |

---

## 📊 Vista Dataview — Asignaturas Individuales

> Si creas una nota por cada asignatura usando la plantilla, esta consulta las mostrará automáticamente:

```dataview
TABLE
  profesor AS "Profesor",
  aula AS "Aula",
  tipo AS "Tipo",
  creditos AS "Créditos"
FROM "Universidad"
WHERE contains(tags, "asignatura")
SORT file.name ASC
```
