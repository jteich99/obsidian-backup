---
fecha: <% tp.file.creation_date("YYYY-MM-DD") %>
tags:
  - project/tesis
Status: Backlog
activity: 
links: 
complete: 0
total: 1
---
<% await tp.file.move("/02-Tesis/05-Tesis Project Folder/" + tp.file.title) %>
# <% tp.file.title %>
- [ ] 