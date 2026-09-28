---
people: 3
nights: 2
---

# Road trip down the coast

Three of us, two nights, San Francisco down to Santa Cruz and back. This note is the whole plan. Every number in it is worked out as we go, so change one and the rest follows.

## The budget

`people` and `nights` are this note's properties, at the top. The car's mileage comes from its own note, [[Car]], and the tickets add up the stop notes in the `Road trip/Stops` folder.

```ic
drive = 190 miles
gas = $4.90/gallon
fuel = drive / [[Car]].mpg * gas
hotel = nights * $189
food = people * nights * $45
ticket each = $1 * vaultsum("**/Road trip/Stops/*", ticket)
tickets = people * ticket each
total = fuel + hotel + food + tickets
donut([fuel, hotel, food, tickets], ["Fuel", "Hotel", "Food", "Tickets"])
```

All in, the trip comes to {total}, which is {total / people} each. Inês pays in euros, so her share is {total / people in EUR}.

## Where to stop

Datasette's public demo database happens to list four roadside attractions near our route. This block reads them live, sorted north to south, which is the order we will pass them.

```ic
spots = import("https://latest.datasette.io/fixtures/roadside_attractions.json?_shape=array&_col=name&_col=latitude&_col=longitude") @sheet @cols(Id, Name, Latitude, Longitude) @sort(latitude desc)
distance = map(spots, s => round(69 * sqrt((s.latitude - 37.7749)^2 + ((s.longitude + 122.4194) * cos(37.7749))^2)))
bars(distance, map(spots, s => s.name))
farthest = max(distance)
```

Offline, the first row says it could not reach the server, the rows that read it say they have no data, and the rest of this note still works.

## Our picks

Each stop we chose is a note tagged `#roadtrip`, with its ticket price and how long we want there. This sheet collects them:

```ic
picks = vaulttable("#roadtrip", file, ticket, hours) @sheet @cols(File, Ticket, Hours) @sort(hours desc)
time at stops = sum(vaulttable("#roadtrip", hours)) hours
```

## Who paid what

We keep receipts here as we go:

### Paid

| Who | Paid |
|-----|------|
| Ana | 378 |
| Ben | 64 |
| Inês | 190 |

```ic
paid = table("Paid")
fair share = sum(table("Paid", Paid)) / people
settle = map(paid, r => {who: r.who, owed: round(r.paid - fair share, 2)}) @sheet @cols(Who, Owed) @sort(owed desc)
```

## What the car really does

Our fill-ups from the last trip are in a spreadsheet file in the vault, `Road trip/fuel log.csv`:

```ic
e_car = sum(csv("fuel log.csv", miles)) / sum(csv("fuel log.csv", gallons)) * 1 mi/gal
V_tank = [[Car]].tank
```

How far one tank goes, as a formula:

$$d = e_{car} \cdot V_{tank}$$

## What if

Drag `$4.90` sideways to try other gas prices, or drag the answer beside `each` to a number you like: the hotel price changes to fit.

```ic
gas price = $4.90/gallon // 3..7 by 0.1
hotel night = $189
each = (drive / [[Car]].mpg * gas price + nights * hotel night) / people + nights * $45 + ticket each
```

The cost each, for one to six people, and then for one to five nights too (drag the surface to turn it):

```ic
share(x, y) = (fuel + y * hotel night) / x + y * $45 + ticket each
plot share(x, nights) from 1 to 6
surface share(x, y) from x=1 to 6, y=1 to 5
```

## Snacks, and sending it

The snack list is its own note, [[Snacks.ic|Snacks]]. Its name ends in `.ic.md`, so every line in it computes without a code block.

To send the plan to the others, use **Copy share link** in any block's **⋯** menu. The link holds the whole calculation, the car's numbers included, and opens on instacalc.com without an account.

This last block is in Present view: the Web view's clean page with sliders, for the group chat. It runs the full instacalc.com app, so it needs the network.

```ic present
people = 3 // 1..6 @label(People)
nights = 2 // 1..5 @label(Nights)
tickets = $66 // 0..150 @label(Tickets each)
each = (190 miles / 31 mpg * $4.90 + nights * $189) / people + nights * $45 + tickets @hero @label(Each of us)
```
