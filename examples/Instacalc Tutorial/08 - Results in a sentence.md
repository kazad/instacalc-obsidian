# Results in a sentence

![Demo: Results in a sentence](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/08-results-in-a-sentence.gif)

Put a calculation in `{…}` and the sentence shows its answer.

```ic
guests = 8
per head = 23.50
food = guests * per head
drinks = guests * 9
total = food + drinks
```

Dinner comes to {total} for {guests} people, which is {total / guests} each.

Edit `guests` above and the sentence updates.

## How to write one

```markdown
Dinner comes to {total}.
Each pays {total / guests}.
Dinner comes to {ic total}.
```

`{total / 4}` is the everyday form. `{ic total}` is the explicit form, for when you want to be sure it computes.

An answer in a sentence never guesses. A name the note does not define, like {totl}, shows a reason instead of a number.

## Anything a row can do

Units, currencies, `[[references]]` and tables work in a sentence too. Sitting down for 45 minutes each comes to
{guests * 45 minutes in hours} of table time, and at the rate card in
[[Rates]] two hours of cooking bills {[[Rates]].hourly * 2}.

Next: [09 - Calculus](09%20-%20Calculus.ic.md).
