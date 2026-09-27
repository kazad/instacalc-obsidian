# Reading other notes

![Demo: Reading other notes](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/05-reading-other-notes.gif)

Numbers that matter usually live somewhere else — a rate card, a budget, a  
settings note. Reference one with the same `[[…]]` you already use for links.

The rates for this lesson live in [[Rates]]. That sentence is prose, and shows  
no number, because a bare reference only computes where arithmetic is  
happening.

hours = 12  
fee = [[Rates]].hourly * hours  
tax = fee * [[Rates]].taxRate  
invoice = fee + tax

Edit `hourly` in [[Rates]] and every row above follows.

## Typing one

Type `[[` and Obsidian's own note picker opens. After the closing `]]`,  
type a `.` and this plugin lists that note's numbers, each showing its current  
value — so you can tell one rate from another without leaving the line.

## A note's headline number

A note with a single obvious number can be referenced bare:

ceiling = [[Q3 Budget]]  
headroom = ceiling - invoice

## When it is wrong, it says so

A reference that names a property the note does not have tells you what it does  
have, rather than quietly showing nothing:

typo = [[Rates]].hourlyRate

Next: *06 - Totals across the vault*.
