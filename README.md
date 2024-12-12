# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue within a `setTimeout` loop.  The expected behavior is to log numbers 0-9 sequentially, with a 1-second delay between each.  However, due to the nature of closures and how `setTimeout` works, all logs will show '10'.

## Bug Description

The problem lies in how the `setTimeout` callbacks capture the variable `i`.  By the time the `setTimeout` functions finally execute, the loop has already completed, and `i` has its final value of 10.

## Bug Solution

The solution involves creating a new scope for each iteration of the loop, ensuring that each `setTimeout` callback captures its own unique value of `i`.

## How to run

1. Clone the repository
2. Open the `bug.js` and `bugSolution.js` files in your browser's developer console or a JavaScript environment.
3. Run `myFunction()` from the `bug.js` file to observe the issue.
4. Run `myFunction()` from the `bugSolution.js` file to see the corrected behavior.