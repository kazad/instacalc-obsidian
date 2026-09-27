# Reading other notes

![Demo: Reading other notes](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/05-reading-other-notes.gif)

Use a number from another note with the same `[[…]]` you use for links. The rates for this lesson live in [[Rates]].

hours = 12  
fee = [[Rates]].hourly * hours  
tax = fee * [[Rates]].taxRate  
invoice = fee + tax

Edit `hourly` in [[Rates]] and every row above follows.

## Typing one

Type `[[` to pick a note. After the closing `]]`, type a `.` to see that note's numbers and their values.

## A note's headline number

A note with a single obvious number can be referenced bare:

ceiling = [[Q3 Budget]]  
headroom = ceiling - invoice

## Mistakes

A property the note does not have shows an error that lists the ones it does have:

typo = [[Rates]].hourlyRate

Next: [06 - Totals across the vault](06%20-%20Totals%20across%20the%20vault.ic.md).
