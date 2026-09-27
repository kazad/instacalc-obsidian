# Drag to explore

![Demo: Drag to explore](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/12-drag-to-explore.gif)

In reading view, you can drag the numbers in a calc block. Here is a mortgage: what can you afford?

```ic
price = $400,000
down payment = 20% of price
rate = 6.5%
years = 30
loan = price - down payment
monthly = pmt(rate / 12, years * 12, -loan)
```

## Drag a number

Drag `6.5%` sideways. The answers update as you drag, and the new rate is saved in the note when you let go. `$400,000` and `30` work the same way.

## Drag an answer to solve backwards

Drag the **answer** beside `monthly` to set the payment you want, and an input changes to match. Drag it to $2,500 and `price` becomes $494,409.

To type a target instead, use **Solve for target…** in the block's **⋯** menu.

Next: [13 - Insert picker](13%20-%20Insert%20picker.md).
