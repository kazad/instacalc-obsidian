# Charts

![Demo: Charts](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/04-charts.gif)

A chart is one more line in a calc block. It is drawn offline in your theme's colours and updates when a number changes.

## Where the money goes

```ic
rent = 1800
food = 600
utilities = 250
fun = 350
barchart
```

A bare `barchart` or `piechart` charts the values above it. To chart only some, list them:

```ic
donut([rent, food, utilities])
```

## A formula over a range

Ten thousand, growing at 7% a year for 30 years:

```ic
savings = 10000
plot savings * 1.07^x from 0 to 30
```

## In three dimensions

```ic
surface sin(x) * cos(y)
```

Drag the surface to turn it.

Next: [05 - Reading other notes](05%20-%20Reading%20other%20notes.ic.md).
