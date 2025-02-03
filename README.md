# ReferenceError in Script Tag Outside Body
This repository demonstrates a subtle HTML error that can lead to a `ReferenceError`.  The issue arises when a script tag attempting to manipulate the DOM is placed outside the `<body>` element.  This prevents the script from accessing the DOM before it's fully parsed and rendered.

## Bug
The provided `bug.html` file includes a script tag that calls `document.getElementById` to hide a div. However, because the script is outside the `<body>`, the DOM isn't fully ready, and the `ReferenceError` is thrown.

## Solution
The `bugSolution.html` file demonstrates the correct approach by placing the script tag within the `<body>` element, ensuring that the DOM is fully parsed when the script executes.