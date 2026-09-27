# Charts

![Demo: Charts](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/04-charts.gif)

A chart is one more line in a calc block. The plugin draws it offline, in your
theme's colours, and redraws it when a number changes.

## Where the money goes

```ic
rent = 1800
food = 600
utilities = 250
fun = 350
barchart
```

A bare `barchart` (or `piechart`) charts the values above it in the same
block. To chart only some of them, name them in a list:

```ic
donut([rent, food, utilities])
```

## A formula over a range

Ten thousand, growing at 7% a year for 30 years:

```ic
savings = 10000
plot savings * 1.07^x from 0 to 30
```

Change `savings` and the curve redraws.

## In three dimensions

```ic
surface sin(x) * cos(y)
```

Drag the surface to turn it. For charts you can pan and zoom, the block's
**Web** view (lesson 14) opens it in the full app.

Next: *05 - Reading other notes*.
