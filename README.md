# Unexpected calc() Behavior in CSS

This repository demonstrates an uncommon issue encountered when using the CSS `calc()` function with percentages and viewport units. The goal is to create a container whose width is 50% of its parent, minus 10vw (10% of the viewport width). However, the actual behavior may vary between browsers due to how `calc()` handles unit conversions and subtractions.

## Problem Description

The `calc(50% - 10vw)` expression in CSS is expected to dynamically adjust the container width based on both the parent's width and the viewport's width.  However, the outcome may be inconsistent across browsers, which might lead to layout issues.

## Solution

The solution involves refactoring the calculation to avoid direct subtraction of percentages and viewport units. The alternative is to use only one unit type for the calculation.