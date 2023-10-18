---
tags:
  - stamm/project
  - moc
---
# proyectos


```dataviewjs
for (let group of dv.pages('"03-Stamm/Projects - Stamm"').groupBy(p => p.proyecto)) {
	dv.header(3, group.key);
	dv.table(["Name", "status", "due"],
		group.rows
		.map(b => [b.file.link, b.status, b.due]))
}
```

