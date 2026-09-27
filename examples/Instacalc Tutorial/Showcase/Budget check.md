## Budget

| Category | Planned | Actual |
|----------|---------|--------|
| Rent | 1800 | 1800 |
| Food | 600 | 712 |
| Travel | 300 | 145 |
| Fun | 200 | 260 |

```ic
rows = table("Budget")
planned = sum(table("Budget", Planned))
spent = sum(table("Budget", Actual))
over = sum(map(rows, r => max(r.actual - r.planned, 0)))
donut(table("Budget", Actual), table("Budget", Category))
```
