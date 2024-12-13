## React Native AsyncStorage: Accessing Data Before Loading

This repository demonstrates a common bug in React Native applications involving the use of AsyncStorage.  The bug occurs when attempting to access data from AsyncStorage before the asynchronous read operation has completed, resulting in undefined values or crashes.

The `bug.js` file illustrates the problematic code. The `bugSolution.js` file provides a corrected implementation that uses the `then` method to ensure the data is accessed only after the asynchronous read operation completes.

This issue highlights the importance of correctly handling asynchronous operations in React Native to prevent unexpected application behavior and crashes.

## Solution
Always handle AsyncStorage operations asynchronously using Promises, `.then()` method or async/await to ensure data is accessed after it has been loaded.  Avoid direct synchronous access to the AsyncStorage data.