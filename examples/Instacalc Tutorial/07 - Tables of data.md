# Tables of data

![Demo: Tables of data](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/07-tables-of-data.gif)

Frontmatter gives one number from this note, `[[Rates]]` one from another, and
`vaultsum` a folder full. The thing people actually keep by hand, in quantity,
is a **table** — and it computes where it already sits, with no second copy of
the numbers to keep in step.

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

Add a row to the table above and every number here follows. The table stays an
ordinary markdown table — sortable, editable, and readable by anyone who opens
the note without this plugin.

## Two shapes

`table("Materials")` is the whole grid, as rows you reach into with a lambda:
`r => r.unit_cost * r.qty`. `table("Materials", Unit Cost)` is a single
column as a flat list, which is what `sum`, `avg`, `min`, `max` and
`sort` already take.

A column heading becomes a lambda field by lower-casing and turning runs of
anything else into `_`, so `Unit Cost` is `unit_cost`. Either spelling
works inside `table(…)`.

## How a table is named

A markdown table has no identifier of its own, so it answers to two names you
already wrote: the **nearest heading above it** and its **first header cell**.
Case does not matter, so `table("item")` finds this same grid.

That is only safe because a name matching two tables is refused rather than
guessed. Position — "the second table" — was never offered: it starts reading
different data the day someone inserts a table above it.

## When it cannot be read, it says so

```ic
oops = sum(table("Matrials", Unit Cost))
```

A misspelt table lists the tables the note really has; a misspelt column lists
the real columns. Nothing here answers a question it could not read with a
`0`, which would look exactly like a real total.

Next: *08 - Results in a sentence*.
