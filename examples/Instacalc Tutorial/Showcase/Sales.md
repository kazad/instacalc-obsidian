## Sales

```csv
month,orders,revenue
Jan,120,2400
Feb,95,1900
Mar,140,2800
Apr,160,3350
```

```ic
revenue = sum(csv("Sales", revenue))
per order = revenue / sum(csv("Sales", orders))
bars(csv("Sales", revenue), csv("Sales", month))
```
