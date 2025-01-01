# Inconsistent List Styling with :nth-child and General Sibling Combinator

This repository demonstrates a subtle CSS bug involving the interaction of `:nth-child` and the general sibling combinator (`~`). The bug causes unexpected styling of list items.

The `bug.css` file contains the erroneous code. The `bugSolution.css` file provides the correct solution.

## Bug Description
The goal is to style every other list item with a yellow background. The initial attempt uses `:nth-child(2n+1)` to select odd-numbered items and `~` to select their following siblings. However, this approach only styles every other item starting from the second item, missing the first item and others.

## Solution
The solution leverages the `:nth-child` selector directly to style every other item without relying on the sibling combinator. This effectively achieves the intended styling.