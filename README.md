# Unexpected NaN return value in foo function

This repository demonstrates a subtle bug in a JavaScript function that results in an unexpected `NaN` return value when an `undefined` argument is passed. 

## Bug Description

The `foo` function is intended to return 0 if the input `x` is null, and `x + 1` otherwise. However, when an `undefined` value is passed, it unexpectedly returns `NaN`.

## How to reproduce

1. Clone this repository.
2. Navigate to the repository's root directory.
3. Open `bug.js` to see the buggy code.
4. Run `node bug.js` in your terminal.

## Solution

The solution involves explicitly checking for both `null` and `undefined` values using the loose equality operator (`==`) which handles `null` and `undefined` as equivalent, ensuring the correct return value in all cases.

This improved handling ensures the function behaves as intended, returning 0 for both `null` and `undefined` inputs and `x + 1` otherwise.