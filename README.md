# Unexpected Flexbox Behavior with w-1/2 in Tailwind CSS

This repository demonstrates an unexpected behavior when using Tailwind CSS's `w-1/2` utility class within a flex container.  The expectation is that two divs with `w-1/2` would equally divide the available width. However, due to the default flex behavior, this doesn't always happen.

## Bug Description
The issue occurs because, by default, flex items will take up only the space they need.  `w-1/2` sets the width to half of the *available* space, but that space is initially undefined. In this example, that space might end up being a very small area, making each div seem very narrow, unless you set parent's width.

## Solution
The solution involves either setting a fixed width on the parent container or using the `basis` property to explicitly define the width of the flex items. 