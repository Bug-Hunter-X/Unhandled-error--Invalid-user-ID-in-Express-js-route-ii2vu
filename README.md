# Express.js Unhandled Error: Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  failure to handle invalid input gracefully.  Specifically, the code lacks error handling for non-numeric user IDs, leading to potential application crashes or unexpected behavior.

## Bug Report

The `bug.js` file contains the problematic code.  It attempts to fetch a user from an array using an ID parsed from the request parameters.  However, it doesn't validate the ID or handle the case where the ID is not a valid integer, causing errors if the ID is something other than a number.

## Solution

The `bugSolution.js` file presents a corrected version with improved error handling.  It validates that the user ID is a number before attempting to use it to find a user.  If the ID is invalid, it returns an appropriate HTTP error code (400 Bad Request) with a meaningful error message.

This illustrates the importance of robust input validation and error handling in building secure and reliable web applications with Express.js.