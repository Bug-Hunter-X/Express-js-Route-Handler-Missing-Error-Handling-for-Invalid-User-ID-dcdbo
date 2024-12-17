# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user input.  Specifically, the code attempts to parse a user ID as an integer without checking if the input is valid. This can lead to crashes or unexpected behavior if the ID is not a number or is otherwise invalid.

## Bug

The `bug.js` file contains the erroneous code. The route handler for `/users/:id` directly attempts to parse the `id` parameter as an integer and uses it to search an array of users. If the `id` parameter is not a valid integer, or if a user with that ID does not exist, the code will either throw an error or return an unexpected result.

## Solution

The `bugSolution.js` file provides a corrected version of the code. It includes comprehensive error handling to gracefully manage cases where the `id` parameter is not a valid integer or a user with that ID is not found.  The solution involves checking if the `id` parameter is a valid number and handling both cases of a missing user and invalid input appropriately.

## How to run

1. Clone the repository
2. Navigate to the project directory
3. Run `npm install express`
4. Run `node bug.js` (for the buggy version)
5. Run `node bugSolution.js` (for the corrected version)