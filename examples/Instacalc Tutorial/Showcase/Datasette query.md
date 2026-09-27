Drag the floor: the SQL runs on Datasette's server, and only the matching rows come back.

```ic
floor = 95 // 80..100 by 1
rows = import(concat("https://latest.datasette.io/fixtures/-/query.json?_shape=array&sql=select+content,+sortable+from+sortable+where+sortable+%3E%3D+:floor+order+by+sortable+desc&floor=", floor)) @sheet
matches = count(rows)
average = mean(map(rows, r => r.sortable))
bars(map(rows, r => r.sortable), map(rows, r => r.content))
```
