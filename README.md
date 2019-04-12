# CSS Gradual Box Shadow

This repository demonstrates an HTML+CSS technique for creating gradual box shadows by using multiple block elements
with negative bottom margins (so they slide under the antecendent content) and opposing heights to achieve a layering
system where each of the box shadow (effectively-)zero-sized blocks contributes a box shadow. The box shadow spread
and opacity is lineraly adjusted so that the resulting effect is that the box shadow fades on the sides of the enclosed
block.

[**DEMO**](https://tomashubelbauer.github.io/css-gradual-box-shadow/)

## To Do

- See if using `filter` is better than `box-shadow` (should make no difference for rectangular elements)
- See if we can stack `::before` on another `::before` so that pseudo-elements could be used instead
