# Tables of data

![Demo: Tables of data](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/07-tables-of-data.gif)

A calculation can read a Markdown table in the same note. The table stays an ordinary table.

## Materials

| item    | Unit Cost | qty |
|---------|-----------|-----|
| worktop | 640       | 2   |
| cabinet | 180       | 9   |
| handle  | 12        | 24  |

```ic
materials = table("Materials")
line items = count(materials)
subtotal = sum(map(materials, r => r.unit_cost * r.qty))
dearest = max(table("Materials", Unit Cost))
```

Add a row to the table and every number here follows.

## Two shapes

`table("Materials")` gives the rows, which you reach into like `r => r.unit_cost * r.qty`. `table("Materials", Unit Cost)` gives one column as a list, ready for `sum`, `avg`, `min` and `max`.

In a row, a column name is lower-cased with spaces turned into `_`, so `Unit Cost` becomes `unit_cost`.

## How a table is named

A table goes by the heading above it or by its first column header, in any case, so `table("item")` finds this table too. A name that matches two tables gives an error instead of a guess.

## Mistakes

```ic
oops = sum(table("Matrials", Unit Cost))
```

A misspelled table or column shows an error that lists the real ones, never a `0`.

Next: [08 - Results in a sentence](08%20-%20Results%20in%20a%20sentence.md).
