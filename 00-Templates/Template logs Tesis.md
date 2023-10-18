---
tags:
  - project/tesis/logs
fecha: <% tp.file.creation_date("YYYY-MM-DD") %>
---
<% tp.file.rename("log-" + tp.date.now()) %>
### Log
- 

### Tareas marcadas para hacer
```tasks
not done
tags include #project/tesis/todo
group by tags
sort by filename
```
#### Tareas hechas hoy
```tasks
done
tags include #project/tesis/todo
done in 'today'
```

### Ideas/to-do
- [ ] 

### Dudas disparadas
>- [ ] ejemplo de duda --> [[00-Dudas]]
> selecciono "ejemplo de duda -->" --> hago el shortcut para agregar una duda --> le agrego link a este log y tag duda
- [ ] 

```tasks
tags include #duda
description includes {{query.file.pathWithoutExtension}}
```
