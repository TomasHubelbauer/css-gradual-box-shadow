# CSS Gradual Box Shadow

This repository demonstrates an HTML+CSS technique for creating gradual box shadows by using multiple block elements
with negative bottom margins (so they slide under the antecendent content) and opposing heights to achieve a layering
system where each of the box shadow (effectively-)zero-sized blocks contributes a box shadow. The box shadow spread
and opacity is lineraly adjusted so that the resulting effect is that the box shadow fades on the sides of the enclosed
block.

[**DEMO**](https://tomashubelbauer.github.io/css-gradual-box-shadow/)

## Alternatives

A list of ideas I tried and why I haven't chosen them

### Multiple `::before`

Each `::before` would behave the same way the `.shadow-x` works in this demo. The nice thing about this approach would
have been that you need only the content HTML element and the shadows would all been pseudo-elements. The problem which
made it infeasible is that it is simply not possible to stack `::before` like so: `.content::before::before` so this
solution is infeasible due to technical limitations.

### CSS `clip`

The entire idea here was to clip the box with drop shadow and let if overflow achieving the hat effect.
However there was no solution for the opacity gradient nor the sharp shadow edge at the cutoff point.
Also `clip` is deprecated in CSS.

## CSS Mask Mode

Do not remember the problem here.

## Background Linear/Radial Gradient

Haven't tried this, could be interesting because we can fade the gradient strategically and doing a radial gradient
could even give us nice rounded corners on top of the container as the sides diminish downwards.


## CSS `filter`

Maybe it makes sense to use `filter` instead of `box-shadow`?
Should not make a difference for rectangular elements but would open up an option of rounded corners on the top side.

## To-Do

### Code up and document the alternatives as well
