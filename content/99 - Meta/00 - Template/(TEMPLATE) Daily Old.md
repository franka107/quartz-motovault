---
date: <%tp.date.now("YYYY-MM-DD")%>T<%tp.date.now("HH:mm")%>
cssclasses:
  - daily
  <% "- " + tp.date.now("dddd", 0, tp.file.title, "YYYYMMDD").toLowerCase() %>
---

tags: [[📆Daily]]

# DAILY NOTE
## <% tp.date.now("dddd, MMMM Do, YYYY", 0, tp.file.title, "YYYYMMDD") %>
***
### Available tasks

#instaleap #personal #ingles #copilot
### Journal
#### Habituales
- [ ] Minox #personal #tick ⏫ 📅 <%tp.date.now("YYYY-MM-DD")%>
- [ ] Limpieza #personal #tick ⏫ 📅 <%tp.date.now("YYYY-MM-DD")%>
- [ ] Gym #personal #tick ⏫ 📅 <%tp.date.now("YYYY-MM-DD")%>
- [ ] Suplementacion #personal #tick ⏫ 📅 <%tp.date.now("YYYY-MM-DD")%>
- [ ] Lectura 20 min #personal #tick ⏫ 📅 <%tp.date.now("YYYY-MM-DD")%>
- [ ] Bañarse #personal #tick ⏫ 📅 <%tp.date.now("YYYY-MM-DD")%>
#### 7:00 - 8:00 Preparacion
#### 8:00 - 1:00 Instaleap
```jira-search  
query: status != 'Done' AND assignee = currentUser() order by priority DESC  
account: Juanca
type: LIST
```
#### 1:30 - 5:30 Copilot
```jira-search  
query: status != 'Done' AND assignee = currentUser() order by priority DESC  
type: List
account: Frank
```
#### 00:00 - 00:00 Ingles
#### 00:00 - 00:00 Gym/Baile
#### Atrasados
...
