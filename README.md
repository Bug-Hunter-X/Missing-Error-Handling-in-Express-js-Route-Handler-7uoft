# Express.js Route Handler Bug
This repository demonstrates a common bug in Express.js route handlers: missing error handling for invalid input.  The bug involves a route that retrieves a user by ID. If an invalid ID is provided, the application crashes instead of gracefully handling the error.

## Bug
The `bug.js` file contains the erroneous code.  It attempts to parse the user ID as an integer and then accesses the `users` array.  If the ID is not a valid integer or no user with that ID exists, it throws an error, causing the application to crash.

## Solution
The `bugSolution.js` file provides the corrected code.  It includes comprehensive error handling to catch invalid input and returns appropriate HTTP status codes (404 for user not found, 400 for bad request).

## How to Run
1. Clone this repository.
2. Navigate to the repository directory in your terminal.
3. Run `node bug.js` to reproduce the bug.
4. Run `node bugSolution.js` to see the solution.
