# Unresponsive Node.js Server

This repository demonstrates a common Node.js issue: an unresponsive server caused by a long-running synchronous operation that blocks the event loop.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Problem

The original server code performs a 5-second CPU-bound task synchronously.  This prevents the event loop from processing other requests during this time, effectively making the server unresponsive to new connections.

## Solution

The solution involves refactoring the long-running task to use asynchronous operations or offloading it to a worker thread (for CPU-bound tasks).  The improved code in `serverSolution.js` demonstrates this improved approach.