---
tags: [universidad, tareas]
---

# ✅ Tareas Pendientes

> [!tip] Cómo usar
> - Usa `- [ ]` para tareas pendientes y `- [x]` para completadas
> - También puedes crear notas individuales por tarea con la plantilla `Plantillas/Plantilla Tarea`
> - La consulta Dataview al final mostrará automáticamente las tareas de notas individuales

---

## 📌 Tareas por Asignatura

### 📚 Asignatura 1
- [ ] 

### 📚 Asignatura 2
- [ ] 

### 📚 Asignatura 3
- [ ] 

---

## 📊 Vista Dataview — Tareas Individuales

> Si creas notas de tarea individuales con la plantilla, esta consulta las lista automáticamente:

```dataview
TABLE
  asignatura AS "Asignatura",
  fecha_entrega AS "Fecha Entrega",
  tipo_tarea AS "Tipo",
  estado AS "Estado",
  prioridad AS "Prioridad"
FROM "Universidad/Tareas"
WHERE contains(tags, "tarea")
SORT fecha_entrega ASC
```

---

## 📋 Vista rápida — Todas las tareas pendientes del vault

```dataview
TASK
FROM "Universidad"
WHERE !completed
SORT file.name ASC
```
