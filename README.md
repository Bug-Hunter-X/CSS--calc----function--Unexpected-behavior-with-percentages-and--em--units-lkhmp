# CSS `calc()` Function: Unexpected Behavior with Percentages and `em` Units

This repository demonstrates a subtle but potentially problematic issue related to the use of the `calc()` function in CSS when mixing percentage and `em` units.  The primary issue centers around the dynamic nature of `em` units and the potential for unexpected order of operations in complex calculations.

## The Bug

The `bug.css` file contains CSS code that intends to set a container's width to 50% of its parent's width, minus 1em.  However, if the parent's font-size changes (e.g., due to user preferences or responsive design), the `1em` value changes, leading to inconsistent container width.

## The Solution

The `bugSolution.css` file offers a solution that addresses this issue.  To make the container width more robust, it suggests using `rem` units, which are relative to the root element's font-size and, therefore, typically more consistent.  This approach avoids the unpredictable behavior associated with dynamic parent `em` units.