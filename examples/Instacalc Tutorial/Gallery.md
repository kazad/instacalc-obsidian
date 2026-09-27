# Gallery

What Instacalc can do, one example each. The titles open the examples in *Showcase*, where you can change them;
below each picture is the note as written, to copy into your own.
(The pictures load from GitHub, so they need the network; the examples themselves do not.)

## [[Showcase/Calculus|Calculus]]

![Calculus](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/calculus.png)

Derivatives, integrals and limits, worked out as you type.

````markdown
A derivative, a definite integral and a limit:

```ic
d/dx x^3 - 3x
integral x^2 from 0 to 3
limit(sin(x)/x, x, 0)
```
````

## [[Showcase/A function and its slope|A function and its slope]]

![A function and its slope](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/a-function-and-its-slope.png)

Plot f and its derivative on one graph.

````markdown
The curve and its slope, drawn together:

```ic
f(x) = x^3 - 3x
plot f(x), derivative(f(x)) from -2.5 to 2.5
```
````

## [[Showcase/Growth curves|Growth curves]]

![Growth curves](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/growth-curves.png)

Several functions on one plot: which grows fastest?.

````markdown
Linear, quadratic and exponential, side by side:

```ic
plot 4x, x^2, 2^x from 0 to 6
```
````

## [[Showcase/Surface|A 3D surface]]

![A 3D surface](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/surface.png)

One line draws a surface; drag it to turn it.

````markdown
```ic
surface sin(x) * cos(y)
```
````

## [[Showcase/Monthly spending|Monthly spending]]

![Monthly spending](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/monthly-spending.png)

A bar chart from the numbers above it.

````markdown
Where the money went in March:

```ic
rent = $1,850
groceries = $620
transport = $240
eating out = $310
barchart
total = rent + groceries + transport + eating out
```
````

## [[Showcase/A day|Where the day goes]]

![Where the day goes](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/a-day.png)

A pie chart, in your theme’s colours.

````markdown
```ic
sleep = 7.5 hours
work = 8.5 hours
commute = 1 hour
family = 4 hours
reading = 1 hour
piechart
awake = 24 hours - sleep
```
````

## [[Showcase/Compound growth|Compound growth]]

![Compound growth](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/compound-growth.png)

What $10,000 becomes at 7% a year.

````markdown
```ic
savings = $10,000
rate = 7%
plot savings * (1 + rate)^x from 0 to 30
after 30 years = savings * (1 + rate)^30
```
````

## [[Showcase/Mortgage|Mortgage, solved backwards]]

![Mortgage, solved backwards](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/mortgage.gif)

Drag the payment to what you can afford; it solves for the price.

````markdown
What can we afford?

```ic
price = $450,000
down = 20%
rate = 6.25%
years = 30
payment = pmt(rate/12, years*12, -price*(1 - down))
```
````

## [[Showcase/Tokyo prices|Currency conversion]]

![Currency conversion](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/tokyo-prices.png)

Prices in yen and euros, converted to dollars as you write them.

````markdown
What things cost on the trip, in dollars:

```ic
ramen = ¥1,200 in USD
hotel night = ¥18,500 in USD
rail pass = ¥50,000 in USD
paris hotel = €189 in USD
```
````

## [[Showcase/Braking energy|Physics with units]]

![Physics with units](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/braking-energy.png)

Units ride along through the whole calculation.

````markdown
A car braking from 100 km/h:

```ic
mass = 1,500 kg
speed = 100 km/h
energy = 0.5 * mass * speed^2
energy in kJ
energy in kWh
```
````

## [[Showcase/Conversions|Unit conversions]]

![Unit conversions](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/conversions.png)

Say it the way you would say it.

````markdown
```ic
marathon = 42.195 km in miles
3 cups in ml
72 F in C
```
````

## [[Showcase/Projectile|LaTeX that computes]]

![LaTeX that computes](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/projectile.png)

Write the formula; the answer appears beside it, with units.

````markdown
A ball thrown straight up:

```ic
v_0 = 25 m/s
g = 9.81 m/s^2
```

$$h = \frac{v_0^2}{2g}$$

$$t = \frac{2 v_0}{g}$$
````

## [[Showcase/Race times|Statistics]]

![Statistics](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/race-times.png)

Mean, spread and a histogram of your data.

````markdown
Eight 10k runs this autumn:

## Runs

| Date | Minutes |
|------|---------|
| Sep 6 | 31.2 |
| Sep 13 | 29.8 |
| Sep 20 | 30.5 |
| Sep 27 | 32.1 |
| Oct 4 | 28.9 |
| Oct 11 | 30.0 |
| Oct 18 | 31.7 |
| Oct 25 | 29.4 |

```ic
times = table("Runs", Minutes)
mean(times)
median(times)
stdev(times)
histogram(times, 4)
```
````

## [[Showcase/Kitchen quote|A table is data]]

![A table is data](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/kitchen-quote.png)

Sum and chart a markdown table where it sits.

````markdown
## Materials

| Item | Cost |
|------|------|
| Worktop | 640 |
| Cabinets | 1620 |
| Tiles | 385 |
| Paint | 96 |

```ic
materials = sum(table("Materials", Cost))
dearest = max(table("Materials", Cost))
barchart(table("Materials", Cost))
```
````

## [[Showcase/Dinner party|Properties are variables]]

![Properties are variables](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/dinner-party.png)

A note’s own properties are names its calculations can use.

````markdown
---
guests: 12
price: $28
---

```ic
food = guests * price
wine = ceil(guests / 3) * $19
total = food + wine
```
````

## [[Showcase/Invoice|Numbers from other notes]]

![Numbers from other notes](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/invoice.png)

[[Note]].field reads one property; [[Note]] reads a note’s main number.

````markdown
Kitchen job for the Parkers.

```ic
hours = 16
labor = hours * [[Showcase rates]].hourly
materials = $2,741
total = labor + materials
left this year = [[Work budget]] - total
```
````

## [[Showcase/Coffee spend|Totals across the vault]]

![Totals across the vault](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/coffee-spend.png)

Add up a property over a folder, or over every note with a tag.

````markdown
```ic
receipts = vaultcount("Instacalc Tutorial/Showcase/Receipts/*", amount)
spent = $1 * vaultsum("Instacalc Tutorial/Showcase/Receipts/*", amount)
coffee = $1 * vaultsum("#coffee", amount)
```
````

## [[Showcase/Projects|A dashboard from tagged notes]]

![A dashboard from tagged notes](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/projects.png)

vaulttable collects a property from every #project note; chart it.

````markdown
```ic
budgets = vaulttable("#project", budget)
total = sum(budgets)
biggest = max(budgets)
barchart(budgets)
```
````

## [[Showcase/Countdown|Dates]]

![Dates](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/countdown.png)

Days between dates, and date arithmetic.

````markdown
```ic
booked = Sep 26, 2026
trip = Dec 18, 2026
trip - booked
return = trip + 10 days
```
````

## [[Showcase/Dinner split|Answers in a sentence]]

![Answers in a sentence](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/dinner-split.png)

Write {total / 4} in a paragraph and it becomes the number.

````markdown
```ic
bill = $186.40
tip = 20% of bill
total = bill + tip
```

Dinner came to {total} with the tip, so split four ways that's {total / 4} each.
````

## [[Showcase/Lisbon trip|Drag to explore]]

![Drag to explore](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/lisbon-trip.gif)

Drag a number sideways and everything below follows.

````markdown
Five days in Lisbon, two of us.

```ic
nights = 4
flights = 2 * $480
hotel = nights * $155
food = nights * 2 * $45
total = flights + hotel + food
```
````

## [[Showcase/Groceries.ic|Calc-first notes]]

![Calc-first notes](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/groceries-ic.png)

Name a note .ic.md and every line computes, with no code blocks.

````markdown
Weekly shop

milk = 2 * $3.49
bread = $4.25
coffee = 2 * $12
total = milk + bread + coffee
per day = total / 7
````

## [[Showcase/Present view|Present view]]

![Present view](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/present-view.png)

The same rows as a clean page with sliders, in the Web view.

````markdown
```ic present
price = 450000 // 200k..900k by 10k @label(Home price)
down = 20% // % 5..40 @label(Down payment)
rate = 6.25% // % 3..9 by 0.25 @label(Interest rate)
payment = pmt(rate/12, 360, -price*(1 - down)) // @hero @label(Monthly payment)
```
````

## [[Showcase/Text view|Text view]]

![Text view](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/showcase/text-view.png)

Plain lines on the left, answers on the right, in the Web view.

````markdown
```ic text
rent = $1,850
utilities = $210
internet = $60
housemates = 3
each = (rent + utilities + internet) / housemates
```
````

# The lessons

A picture of each lesson. The titles open the lessons; each lesson plays its demo at the top.
(The pictures load from GitHub, so they need the network; the lessons themselves do not.)

## [[01 - Start here.ic|Start here]]

![Start here](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/01-start-here.png)

Arithmetic, named values, percentages, comments.

## [[02 - Units and currencies.ic|Units and currencies]]

![Units and currencies](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/02-units-and-currencies.png)

Conversion, units through a product, offline money.

## [[03 - Notes that calculate|Notes that calculate]]

![Notes that calculate](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/03-notes-that-calculate.png)

Fences, variables across blocks, callouts.

## [[04 - Charts|Charts]]

![Charts](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/04-charts.png)

Bar, donut, line and 3D charts, drawn offline.

## [[05 - Reading other notes.ic|Reading other notes]]

![Reading other notes](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/05-reading-other-notes.png)

`[[references]]`, completion, stated failures.

## [[06 - Totals across the vault.ic|Totals across the vault]]

![Totals across the vault](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/06-totals-across-the-vault.png)

Frontmatter variables, folder queries.

## [[07 - Tables of data|Tables of data]]

![Tables of data](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/07-tables-of-data.png)

`table(…)`, how a table is named, refusals.

## [[08 - Results in a sentence|Results in a sentence]]

![Results in a sentence](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/08-results-in-a-sentence.png)

Inline results, and the number they will not show.

## [[09 - Calculus.ic|Calculus]]

![Calculus](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/09-calculus.png)

Derivatives, integrals, `solve`.

## [[10 - Making a note presentable.ic|Making a note presentable]]

![Making a note presentable](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/10-making-a-note-presentable.png)

The decorators, as a loan document.

## [[11 - Formulas that compute|Formulas that compute]]

![Formulas that compute](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/11-formulas-that-compute.png)

`$$` LaTeX with answers, using values from a fence.

## [[12 - Drag to explore|Drag to explore]]

![Drag to explore](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/12-drag-to-explore.png)

Drag a number to scrub it, drag an answer to solve backwards.

## [[13 - Insert picker|Insert picker]]

![Insert picker](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/13-insert-picker.png)

The + picker: suggestions with your names, charts from your numbers.

## [[14 - Share and present|Share and present]]

![Share and present](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/14-share-and-present.png)

Text, Native and Web views; Present; share links.
