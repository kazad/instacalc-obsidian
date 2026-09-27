# Drag to explore

![Demo: Drag to explore](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/12-drag-to-explore.gif)

In reading view, the numbers in a calc block are handles. This lesson is the
question people bring to a mortgage calculator: what can I afford?

```ic
price = $400,000
down payment = 20% of price
rate = 6.5%
years = 30
loan = price - down payment
monthly = pmt(rate / 12, years * 12, -loan)
```

## Drag a number

Press on `6.5%` and drag sideways. The rate moves in small round steps and
every answer below it follows while you drag. Let go and the new rate is written
into the note, so what you see is what the file says. The same works on
`$400,000` and `30`.

## Drag an answer to solve backwards

Now drag the **answer** beside `monthly`. You are setting the payment, and the
plugin works out the input that produces it. Drag it up to $2,500 and `price`
becomes $494,409: that is the house a $2,500 payment buys at this rate.

It changes the input the answer depends on most, which here is the price
rather than the rate, and writes the solved number into the note.

To type a target instead of dragging, use **Goal Seek (solve backwards)** in
the block's **⋯** menu.

Next: *13 - Insert picker*.
