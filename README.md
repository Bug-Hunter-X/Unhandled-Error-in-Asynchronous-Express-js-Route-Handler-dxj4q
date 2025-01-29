# Unhandled Error in Asynchronous Express.js Route Handler

This repository demonstrates a common error in Express.js applications where an unhandled error in an asynchronous route handler causes the server to crash silently.  The provided `bug.js` file showcases the problematic code, while `bugSolution.js` presents the corrected version with proper error handling.

## Problem

Asynchronous operations within route handlers can throw errors. If these errors are not caught, the Express.js application will likely crash without any useful error message in the console, making debugging challenging.

## Solution

The solution involves proper error handling within the `.catch` block of the `Promise`. This allows for logging the error, sending a proper error response to the client, or taking other necessary actions to prevent the application from crashing.