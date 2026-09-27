# Formulas that compute

![Demo: Formulas that compute](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/11-formulas-that-compute.gif)

An equation in `$$ … $$` is typeset as usual. If it defines a name, its answer appears beside it.

## Throwing a ball straight up

```ic
v_0 = 15 m/s
g = 9.8 m/s^2
```

How high it goes:

$$h = \frac{v_0^2}{2g}$$

How long until it comes back down:

$$t = \frac{2 v_0}{g}$$

Later blocks can use the result:

```ic
h in feet
```

## A formula with a parameter

Put a parameter on the left and the formula becomes a function:

$$R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}$$

Thrown at 45° the ball lands {R(45 deg)} away; at 30°, {R(30 deg)}.

## What stays typesetting

An equation that defines nothing is only typeset:

$$a^2 + b^2 = c^2$$

A formula with unknown values shows no answer.

Next: [12 - Drag to explore](12%20-%20Drag%20to%20explore.md).
