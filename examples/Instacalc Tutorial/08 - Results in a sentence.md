# Results in a sentence

![Demo: Results in a sentence](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/08-results-in-a-sentence.gif)

Most of what you write is a sentence with a number in it, and every one of those
numbers is a copy — stale the moment the block above it changes.

```ic
guests = 8
per head = 23.50
food = guests * per head
drinks = guests * 9
total = food + drinks
```

Dinner comes to {total} for {guests} people, which is {total / guests} each.
Showing the working instead: {ic= food + drinks}.

Edit `guests` above and the sentence rewrites itself.

## How to write one

```markdown
Dinner comes to {total} — the value on its own.
Each pays {total / guests} — any expression works.
Showing the working: {ic= food + drinks} — expression and value.
```

Syntax inside a fence is shown, never computed, which is why the block above
stays as typed while the sentence before it does not.

Opened without this plugin, the note still reads fine: `{total}` says what it
stands for. If braces clash with something in your vault, the code-span form
``ic: total`` does the same job (its trigger is configurable under
*Inline trigger*).

## The number it will not show you

This is the part worth knowing. Inside a sentence there is no result column and
no warning gutter, so a wrong number would look exactly like one you typed on
purpose. An inline expression therefore says a value or says a reason, and never
guesses:

- a name this note does not define — {totl} — reads *totl is not defined
  in this note*;
- a name defined further **down** the note says *defined later in this note*,
  because definitions flow forward only and the fix is to move a line;
- an expression whose answer would depend on where it sits is refused outright.

And a code span that is not ours is never touched: `const x = 1` in a
programming note comes out byte for byte.

## Anything a row can do

An inline expression takes the same path a fence row takes, so units,
currencies, `[[references]]`, folder totals and `table(…)` calls all work
mid-sentence. Sitting down for 45 minutes each comes to
{guests * 45 minutes in hours} of table time, and at the rate card in
[[Rates]] two hours of cooking bills {[[Rates]].hourly * 2}.

Next: *09 - Calculus*.
