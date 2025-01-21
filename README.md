# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js applications where a long-running synchronous operation in the request handler blocks the event loop, causing the server to become unresponsive.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Bug Description

The server uses a `while` loop to simulate a 5-second long operation.  During this time, the event loop is blocked, preventing the server from handling new requests or responding to existing ones.  This leads to unresponsiveness and potentially a timeout for clients.