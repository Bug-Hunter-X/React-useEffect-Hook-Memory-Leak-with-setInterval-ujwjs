# React useEffect Hook Memory Leak with setInterval
This repository demonstrates a common mistake when using the `useEffect` hook in React with `setInterval`.  Forgetting to return a cleanup function from `useEffect` leads to memory leaks, as the interval continues even after the component unmounts.

## Bug Description
The `bug.js` file contains a component that uses `setInterval` to update a counter every second.  However, it lacks the essential `return` statement within the `useEffect` cleanup function that is needed to stop the `setInterval` when the component unmounts.

## Solution
The `bugSolution.js` file shows the corrected code with the cleanup function properly implemented.