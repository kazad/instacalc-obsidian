## Materials

| Item | Cost |
|------|------|
| Worktop | 640 |
| Cabinets | 1620 |
| Tiles | 385 |
| Paint | 96 |

```ic
materials = sum(table("Materials", Cost))
dearest = max(table("Materials", Cost))
barchart(table("Materials", Cost))
```
