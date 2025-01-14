# Silent Failure in Node.js HTTP Server

This repository demonstrates a subtle bug in a Node.js HTTP server where a missing response header causes the server to fail silently.  The server starts, but doesn't respond correctly to requests.

## Bug Description
The `bug.js` file contains a simple HTTP server.  The issue lies in the request handling function: a response header is missing, leading to unexpected behavior. This can be difficult to debug as there are no explicit error messages.

## Solution
The `bugSolution.js` file provides a fix for this problem by adding the necessary `Content-Type` header to the response. 

## How to reproduce
1. Clone this repository.
2. Run `node bug.js`.
3. Try to access the server in a browser. You will likely get no response or an incomplete one. 
4. Run `node bugSolution.js` to see the corrected version.