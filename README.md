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

- A two dimensional grid based layout system
- Whereas flexbox was row or column (1D), CSS Grid allows you to set rows OR colums, all _within the same container_

# CSS Grid parent properties

- display: grid
- **grid-template-columns:** set column size and number of columns. _this is called the track list_
- **grid-template-rows:** set row size and number of row. _this is called the track list_
- using the 'auto' value in the track list, column or row, allows the element to resize according to the available space

# Grid lines

- grid lines seperate items in a track
- anything between the lines is considered a track
- we use **grid gaps** to set the distance between track items
- **grid-column-gap**, **grid-row-gap**, **grid-gap** (on main and cross axis)
- the gaps are _not_ are a measure of the distance between track items, but rathe the size of the gaps (gutters) themselves
- layouts can also be specified according according to the grid-lines with the **grid-column-start** and **grid-column-end** syntax
- there are also negative grid lines, which go from right to left on the main axis and bottom to top on the cross axis

# Fractional units

- CSS Grid introduces fr, which behaves similarly to auto but allows for equal proportions of track items
- fr takes into account the other items on the grid to size accordingly whereas auto only looks at remaining, unused space
- We can use repeat notation to set multiple tracks to the same item in a more concise manner - _grid-template-columns: repeat(3, 1fr)_ means 3 grid items, each taking up 1 fraction of the available space

# minmax

- set a minimum width and maximum column width for a row or column
- repeat(3, minmax(100px, 1fr))

# auto-fill vs auto-fit

- _auto-fill_ will make each item a certain size, wrap items when no more room is left
- _auto-fit_ will tell the browser to automatically fill the grid with columsn when room is available

### Implicit grid

- whenever we hve items that wrap outside of what we've explicitly defined as a grid, this is the _implicit grid_
- we can use **grid-auto-rows** and **grid-auto-columns** to set the implicit grid for us, dynamically.
- without this setting, spillover grid items are sized according to content
- **grid-auto-flow** allows us to set how the spillover grid items should be laid out, row or column
