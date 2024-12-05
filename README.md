# TypeScript Type Guard Bug with 'undefined'

This repository demonstrates a subtle bug in TypeScript's type guards when dealing with `string | null` types and the `undefined` value.  The `greet` function is intended to handle both string inputs and `null`, but fails when passed `undefined` because TypeScript's type narrowing doesn't account for this possibility in this scenario.

The `bug.ts` file shows the erroneous code, while `bugSolution.ts` offers a fix.

## Reproduction

1. Clone this repository.
2. Compile the `bug.ts` file using TypeScript compiler (tsc bug.ts). 
3. Run the code.  Observe the error caused by calling `greet` with `undefined`.
4. The solution illustrates a corrected type handling approach.