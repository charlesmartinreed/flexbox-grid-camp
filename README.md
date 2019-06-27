### Flexbox

- CSS tool for laying out rows and columns
- "One dimensional"
- Good for navigation, image galleries
- Has wide browser support

## Flexbox - Containers & Items

- Some properties are for the container, others are for the items in the container
- These are often referred to as "parent" and "children" properties
- Items within a container are either **justified** along the x-axis (main) or **aligned** around the y-axis (cross)
- Generally, flex children will not exceed the bounds of their parent containers.

# Flexbox Parent Properties

- display (flex)
- flex-direction (row, col, row-reverse, column-reverse)
- justify-content (center, flex-start, flex-end, space-between, space-around, space-evenly...)
- align-items (flex-start, flex-end, center, baseline -- align items based on the baseline of the child items -- stretch)
- wrapping on the next line when child sizes exceeds parent container is accomplished with flex-wrap (wrap, nowrap, wrap-reverse)
- **flex-flow** takes both flex wrap and direction

# Align-items vs Align-content

- Align content only works if you have more than one line of items **and** if you have extra space
- flex-end, center, space-between, space-around, stretch (won't work if you have a hard coded height set for the items )

# Flexbox Child Properties

- **align-self**: Overrides align values from the parent - baseline, stretch, flex-start, flex-end, center
- **flex-grow**: set item sizes, proportionally
- **flex-shrink**: when not enough space, specifies how much item should shrink relative to others in parent container
- **flex-basis**: set default size of an item before space is calculated, along the length of its axis
- **flex**: shorthand for flex-shrink and flex-basis - flex-grow, flex-shrink, flex-basis
- **order**: change order of where child items sit by assigning them a number. Default value is _0_.

[A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

### CSS Grid
