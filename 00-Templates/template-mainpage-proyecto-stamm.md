---
tags:
  - stamm/project/mainpage
fecha: <% tp.file.creation_date("YYYY-MM-DD") %>
Status: Backlog
proyecto: <% tp.file.title %>
mainpage: true
---
# <% tp.file.title %>
> Descripción del proyecto
- 
## tasks del proyecto
```dataview
table where contains(proyecto, "<% tp.file.title %>")
where !contains(status, "Done")
where mainpage != true
```

## tasks completadas
```dataview
table where contains(proyecto, "<% tp.file.title %>")
where contains(status, "Done")
```
