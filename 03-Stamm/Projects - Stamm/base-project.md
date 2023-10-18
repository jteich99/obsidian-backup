---
tags:
  - stamm/project/mainpage
fecha: 2023-10-14
Status: Backlog
proyecto: base-project
---
# base-project
> Descripción del proyecto
- 
## tasks del proyecto
```dataview
table where contains(proyecto, "<% tp.file.title %>")
where !contains(statu, "Done")
```

## tasks completadas
```dataview
table where contains(proyecto, "<$ tp.file.title $>")
where contains(statu, "Done")
```
