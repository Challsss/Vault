---
tags: [trabajo, horas-extras]
---

# ⏱️ Registro de Horas Extras

## Registro Mensual

> [!tip] Cómo usar
> Añade una fila por cada día que hagas horas extras. El campo `motivo` es opcional.

### Septiembre 2026

| Fecha      | Hora Entrada | Hora Salida | Horas Extra | Motivo | Compensado |
| ---------- | ------------ | ----------- | ----------- | ------ | ---------- |
|            |              |             |             |        | ⬜          |

### Octubre 2026

| Fecha      | Hora Entrada | Hora Salida | Horas Extra | Motivo | Compensado |
| ---------- | ------------ | ----------- | ----------- | ------ | ---------- |
|            |              |             |             |        | ⬜          |

---

## 📊 Resumen con Dataview

```dataview
TABLE WITHOUT ID
  rows.Fecha AS "Fechas",
  sum(rows["Horas Extra"]) AS "Total Horas Extra"
FROM "Trabajo"
WHERE contains(tags, "horas-extras")
GROUP BY file.name
```

---

## Totales Acumulados

| Mes              | Horas Extras Totales | Compensadas | Pendientes |
| ---------------- | -------------------- | ----------- | ---------- |
| Septiembre 2026  |                      |             |            |
| Octubre 2026     |                      |             |            |
| Noviembre 2026   |                      |             |            |
| Diciembre 2026   |                      |             |            |
