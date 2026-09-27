# Share and present

![Demo: Share and present](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/14-share-and-present.gif)

```ic
nights = 4
hotel = $180 * nights
flights = 2 * $420
total = hotel + flights
```

## Three ways to show a block

Hover the block. The left of its toolbar has three views:

- **Text**: the fence as plain markdown, to edit by hand.
- **Native**: what you see above. Computed here, offline, in your theme.
- **Web**: the full instacalc.com app in a frame, with sliders and charts you
  can pan and zoom. Its menu picks a layout, and **Present** shows the block as
  a summary with the answer large.

Choosing a web layout rewrites the fence's first line, for example to
`` ```ic present ``, so the choice is saved with the note. The web views
need the network; Native never does.

## Share it

In the block's **⋯** menu, **Copy share link** copies a link that holds the
whole calculation: nothing is uploaded and no account is needed. It opens on
instacalc.com titled with this note's name. For the block above it is:

https://instacalc.com/%23_14_-_Share_and_present;nights_=_4;hotel_=_$180_*_nights;flights_=_2_*_$420;total_=_hotel_+_flights

If the block uses values from earlier in the note, the link brings them along,
so it works on its own. **Open on instacalc.com** opens the same link, and
**Copy calculation** copies the rows as text.

That is the tour. Every note here is ordinary markdown, readable without the
plugin, and everything except the web views works offline.
