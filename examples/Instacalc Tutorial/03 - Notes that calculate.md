# Notes that calculate

![Demo: Notes that calculate](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/03-notes-that-calculate.gif)

This is a plain `.md` note: Markdown, with Instacalc inside `` ```ic `` blocks and `{…}` in sentences. Type `` ```ic `` and press Enter: the closing `` ``` `` is added for you.

## Splitting the rent

```ic
rent = 2400
utilities = 180
internet = 60
housemates = 3
per person = (rent + utilities + internet) / housemates
```

A later block in the same note can use earlier values:

```ic
per year = per person * 12
```

## Callouts and lists

In an `.ic.md` note, callouts, lists and quotes calculate too. Here they stay text:

> [!note] Not in this file
> budget = 250

Next: [04 - Charts](04%20-%20Charts.md).
