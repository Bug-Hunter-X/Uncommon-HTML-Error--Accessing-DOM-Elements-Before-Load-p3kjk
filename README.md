# Uncommon HTML Error: DOM Access Before Load

This repository demonstrates a subtle but common error in HTML/JavaScript: trying to access and manipulate DOM elements before the browser has finished parsing and loading them.  This often leads to `null` values or unexpected behavior.

The `bug.html` file shows the erroneous code; `solution.html` provides a corrected version that ensures the DOM element is ready before manipulation.

## Reproduction
1. Open `bug.html` in a web browser.
2. Observe that the code attempts to add content to a div element before the element exists in the DOM.
3. Open `solution.html` and see the correct implementation using `DOMContentLoaded`.

## Solution
The solution lies in using the `DOMContentLoaded` event. This event is fired once the entire HTML document has been completely loaded and parsed, but before any other elements and scripts have been loaded.