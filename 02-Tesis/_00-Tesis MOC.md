---
tags:
  - project/tesis
---
# Tesis MOC
Link a los MOCs relacionados con la tesis
[[_01-Bibliografía MOC]]
[[_02-Logs MOC]]
[[_03-Reuniones MOC]]
[[_04-Database MOC]]

### notas del dia
- **daily note --> `=link("01-Personal/daily-notes/" + dateformat(date(today), "yyyy-MM-dd"))`**
- **daily log --> `=link("02-Tesis/01-Log/log-" + dateformat(date(today), "yyyy-MM-dd"))`**
### notas útiles
- [[TUPAC]]
- [[actuadores instalados]]
- versiones de directorios de casos
	- turbineWindTunnel
		- [[turbineWindTunnel-v2]]
		- [[turbineWindTunnel-v3]]

----
# tasks
## Doing
```dataview
TABLE Status AS status, activity, complete, total
FROM "02-Tesis/05-Tesis Project Folder"
WHERE contains(Status, "Doing")
```
## Backlog - todo
```dataview
TABLE Status AS status, activity, complete, total
FROM "02-Tesis/05-Tesis Project Folder"
WHERE contains(Status, "Backlog")
```

## Paused
```dataview
TABLE Status AS status, activity, complete, total
FROM "02-Tesis/05-Tesis Project Folder"
WHERE contains(Status, "Paused")
```
## Done
```dataview
TABLE Status AS status, activity, complete, total
FROM "02-Tesis/05-Tesis Project Folder"
WHERE contains(Status, "Done")
```

----
# Logs
```dataview
list
from #project/tesis/logs 
sort file.name desc
where file.name != "Template logs Tesis"
limit 5
```
# Reuniones
```dataview
list
from #project/tesis/reuniones  
sort file.name desc
where file.name != "Template reunión Tesis"
limit 5
```
