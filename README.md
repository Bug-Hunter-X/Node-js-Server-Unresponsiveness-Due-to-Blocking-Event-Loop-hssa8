# Node.js Event Loop Blocking Bug

This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive. The bug is in `bug.js`, and the solution is in `bugSolution.js`.

## Bug Description
The server uses a `while` loop to simulate a long-running task that takes 5 seconds.  During this time, the event loop is blocked, preventing the server from handling new requests. This results in the server becoming unresponsive.

## Solution
The solution involves using asynchronous operations or offloading long-running tasks to worker threads to prevent blocking the event loop.