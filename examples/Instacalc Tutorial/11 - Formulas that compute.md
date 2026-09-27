# Formulas that compute

![Demo: Formulas that compute](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/11-formulas-that-compute.gif)

A display equation in `$$ … $$` is typeset by Obsidian as usual. If it
assigns a name and every value it needs is defined above it, the answer appears
beside it, with units.

## Throwing a ball straight up

```ic
v_0 = 15 m/s
g = 9.8 m/s^2
```

How high it goes:

$$h = \frac{v_0^2}{2g}$$

How long until it comes back down:

$$t = \frac{2 v_0}{g}$$

The names it defines join the note like any other, so a later block, or a
sentence, can use them:

```ic
h in feet
```

## A formula with a parameter

Write the parameter on the left and the formula becomes a function you can call:

$$R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}$$

Thrown at 45° the ball lands `ic: R(45 deg)` away; at 30°, `ic: R(30 deg)`.

## What stays typesetting

An equation that is not an assignment is only typeset:

$$a^2 + b^2 = c^2$$

So is `$…$` math inside a sentence, and a formula whose values are not defined
yet: nothing is shown rather than a guess.

Next: *12 - Drag to explore*.
