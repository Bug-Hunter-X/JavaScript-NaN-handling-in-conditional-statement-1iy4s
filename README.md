# JavaScript NaN Handling Bug

This repository demonstrates a subtle bug related to handling `NaN` (Not a Number) values in JavaScript conditional statements. The provided `foo` function intends to check if the input is `null`, negative, or positive, but it fails to explicitly handle the `NaN` case.

## Bug Description

The issue occurs when the function `foo` receives `NaN` as input.  `NaN` is not equal to any value, including itself (`NaN === NaN` is `false`). Therefore, the conditional checks fail to identify `NaN`, and the function incorrectly returns 1.

## Solution

The solution involves explicitly checking for `NaN` using `isNaN()` function before other conditional checks.