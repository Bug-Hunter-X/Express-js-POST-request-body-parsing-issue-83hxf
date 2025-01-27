# Express.js POST Request Body Parsing Issue

This repository demonstrates a common issue in Express.js applications where the server fails to correctly parse the JSON payload from a POST request.  The problem arises when the necessary middleware to handle JSON requests is either missing or incorrectly configured.

## Bug Description

The `bug.js` file contains an Express.js server that attempts to handle a POST request containing JSON data.  However, due to a missing `express.json()` middleware, the `req.body` remains empty, leading to unexpected behavior or errors.

## Solution

The `bugSolution.js` file shows the corrected code. By adding `app.use(express.json());` before the POST request handler, the application correctly parses the incoming JSON data into the `req.body` object, allowing for proper processing.