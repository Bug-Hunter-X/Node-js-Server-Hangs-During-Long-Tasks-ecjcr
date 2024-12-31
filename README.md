# Node.js Server Hangs During Long Tasks

This repository demonstrates a common issue in Node.js where a server can hang or become unresponsive during long-running operations that block the event loop.  The example simulates a 5-second delay within a request handler.  This would manifest as slow or unresponsive server behavior in a real-world application.

## Bug
The `bug.js` file contains a simple HTTP server that simulates a long-running task within the request handler.  The server becomes unresponsive while executing this task because the event loop is blocked.

## Solution
The `bugSolution.js` file shows how to use asynchronous operations (or a worker thread for CPU-bound tasks) to prevent blocking the event loop and keep the server responsive.