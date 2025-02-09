# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue encountered when using `setTimeout` within a loop.  The problem arises because the closure created by `setTimeout` captures the variable `i` by reference, not by value.  This leads to all callbacks logging the final value of `i` (10) instead of the values 0 through 9 as might be expected.

The `bug.js` file contains the problematic code. The `bugSolution.js` file demonstrates the solution using an immediately invoked function expression (IIFE) to create a new scope for each iteration, thereby capturing the correct value of `i` for each callback.