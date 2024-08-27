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
### Journal
#### Atrasados
#### Habituales
- [ ] Minox 
- [ ] Limpieza 
- [ ] Gym 
- [ ] Suplementacion 
- [ ] Lectura 20 min
- [ ] Dominadas
- [ ] Bañarse 
#### 6:00 - 7:00 Preparacion

#### 8:00 - 1:00 Instaleap
#### 1:30 - 5:30 Copilot
#### 00:00 - 00:00 Ingles
#### 19:00 - 21:00 Gym/Baile

### Integrations

#### Instaleap
```jira-search  
query: status != 'Done' AND assignee = currentUser() order by priority DESC  
account: Juanca
type: LIST
```
#### Copilot
```jira-search  
query: status != 'Done' AND assignee = currentUser() order by priority DESC  
type: List
account: Frank
```

...
