# Express.js Route Handler Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, the provided code attempts to parse a user ID from the request parameters but fails to handle cases where the ID is not a valid integer.

## Bug

The `bug.js` file contains the erroneous code.  It fetches a user based on their ID but does not check if the ID is a number before attempting to parse it. If an invalid ID is provided (e.g., a string), the `parseInt` function will return `NaN`, causing the `find` method to fail to locate the user.

## Solution

The `bugSolution.js` file demonstrates the corrected code. It includes error handling to check if the `userId` is a valid number before proceeding with the user lookup.  If the ID is invalid, it returns an appropriate error response.

## How to Run

1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install express` to install the required dependency.
4. Run `node bug.js` (or `node bugSolution.js`) to execute the code.  You can test with different user IDs.