# Notes that calculate

![Demo: Notes that calculate](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/03-notes-that-calculate.gif)

This note is an ordinary `.md` file, so calculations live in ```ic fences.
Nothing outside one is touched: a shopping list stays a shopping list.

## Splitting the rent

```ic
rent = 2400
utilities = 180
internet = 60
housemates = 3
per person = (rent + utilities + internet) / housemates
```

Variables carry across fences in the same note, so a later block picks up where
this one left off:

```ic
per year = per person * 12
```

## Calculations where you keep them

In a **calc-first** note (`.ic.md`, like lessons 01 and 02), calculations
also compute inside callouts, lists and quotes. This note is not one, so the
last line of this callout stays prose:

> [!note] Not in this file
> budget = 250

Properties at the top of a note become variables too. Lesson 06 uses that for a
daily note.

Next: *04 - Charts*.
