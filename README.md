# Uncommon HTML Bug: Incorrect innerHTML Usage

This repository demonstrates a common yet often overlooked bug in HTML involving the misuse of `innerHTML`.  Improperly using `innerHTML` to insert entire HTML elements can lead to unexpected behavior, such as overwriting existing content and potential security vulnerabilities (cross-site scripting - XSS).

## Bug Description
The bug lies in using `innerHTML` to replace the content of a div with a new heading. This approach replaces *all* content within the `div`, rather than simply appending the heading, which can be unexpected behavior.  In more complex scenarios, this could lead to unexpected data loss or other issues.

## Solution
Instead of using `innerHTML` to insert an entire HTML element, it's best to create the element using DOM methods, then append it to the existing element. This method is safer and provides better control over the resulting DOM structure.