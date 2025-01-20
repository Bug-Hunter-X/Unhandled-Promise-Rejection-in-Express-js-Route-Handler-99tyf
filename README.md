# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: unhandled promise rejections within route handlers.  Unhandled rejections can lead to crashes or unexpected behavior, making proper error handling crucial.

## Bug Description

The `bug.js` file contains an Express.js application with a route handler that performs an asynchronous operation.  However, it lacks proper error handling for the promise rejection.  If the asynchronous operation fails, the application won't gracefully handle the error.

## Solution

The `bugSolution.js` file demonstrates the correct way to handle promise rejections. It uses a `.catch()` block to handle errors gracefully and prevents the application from crashing.  It also includes more robust logging for better debugging.

## How to Run

1. Clone this repository.
2. Navigate to the repository directory.
3. Install dependencies: `npm install express`
4. Run the buggy application: `node bug.js` (Observe the unhandled rejection warning)
5. Run the fixed application: `node bugSolution.js` (Observe the graceful error handling)