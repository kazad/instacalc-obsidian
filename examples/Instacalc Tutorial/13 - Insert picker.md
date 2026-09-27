# Insert picker

![Demo: Insert picker](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/13-insert-picker.gif)

Hover a calc block and press **+** in its toolbar. The picker that opens is
written for that block: its suggestions use your names, and its charts are
drawn from your numbers.

```ic
flights = $840
hotel = $435
food = $260
people = 4
```

For this block it offers, among others:

- `per_person = sum(flights, hotel, food) / people`, the cost each
- `max(flights, hotel, food)`, the biggest expense
- `average(flights, hotel, food)`

Each shows its answer before you pick it. Picking one adds it as the block's
last line, where it computes like anything you typed.

Below the suggestions, the chart cards are pictures of **this** block: the donut
card is `donut([flights, hotel, food])`, already drawn. A block with no
numbers yet gets the same cards drawn from sample numbers, and inserts those
too, so what you saw is what lands in the note.

The search box finds functions by what they do: type `loan` and `pmt` is
first. The **?** button beside **+** opens the same panel as a reference,
where clicking copies instead of inserting.

Next: *14 - Share and present*.
