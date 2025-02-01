# Lua Pairs Iteration Order Bug

This example demonstrates a potential issue with Lua's `pairs` iterator: the lack of guaranteed iteration order.  While it often works as expected, the order is not explicitly defined and can change in unpredictable ways. This can lead to bugs, particularly when relying on a specific order for processing nested tables.

The `bug.lua` file contains a simple function demonstrating the problem. The `bugSolution.lua` file shows one approach to mitigate the problem.

## Reproducing the Bug

1.  Save the code in `bug.lua`.
2.  Run it using a Lua interpreter (e.g., `lua bug.lua`).
3.  Observe that while the code appears to work correctly most of the time, the order is not reliably consistent.

## Solution

The solution involves using an approach that does not depend on iteration order, such as explicitly keeping track of the keys in a separate data structure.