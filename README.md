# Unhandled Exception in Express.js Asynchronous Route Handler

This repository demonstrates a common error in Express.js applications where unhandled exceptions within asynchronous route handlers lead to silent crashes.  The server may appear unresponsive, logging only cryptic errors in the console.

The `bug.js` file showcases the problematic code. The `bugSolution.js` file shows a corrected version. 

## Problem

The original code uses a `Promise` to handle an asynchronous operation. However, error handling within the `.catch` block is not robust enough to prevent the application from crashing if an exception occurs during the asynchronous operation. 

## Solution

The solution involves more robust error handling. A centralized error handler is added to capture unhandled exceptions and provide informative responses to the client.