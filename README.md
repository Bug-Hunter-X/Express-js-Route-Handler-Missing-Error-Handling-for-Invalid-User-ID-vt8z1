# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking for potential errors if the parameter is not a valid integer.  This can lead to unexpected behavior, including crashes or unexpected responses.

## Bug

The `bug.js` file contains the erroneous code.  It attempts to find a user based on the ID, but doesn't handle the case where the ID is not a valid integer or if the user is not found.

## Solution

The `bugSolution.js` file demonstrates a corrected version. It includes explicit checks to ensure the ID is a number and handles the case where the user is not found, returning a proper 404 response.