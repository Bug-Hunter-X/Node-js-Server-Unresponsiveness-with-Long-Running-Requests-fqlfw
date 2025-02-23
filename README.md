# Node.js Server Unresponsiveness with Long-Running Requests

This repository demonstrates a common issue in Node.js applications where long-running requests can cause the server to hang or become unresponsive.  The example uses `setTimeout` to simulate a slow operation, but this could be replaced with any computationally intensive task or external API call.

The solution shows how to use asynchronous patterns (like Promises or async/await) or worker threads to handle these requests without blocking the main event loop.

## Bug

The `bug.js` file contains the problematic server implementation.  When a request is made to the `/` endpoint, it waits for 5 seconds before sending a response.  During this 5-second period, the server is unable to handle any other requests.