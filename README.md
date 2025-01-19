# React setInterval Memory Leak

This repository demonstrates a common error in React components: using `setInterval` within the `useEffect` hook without proper cleanup. This can cause memory leaks and unexpected behavior.

## Problem
The `bug.js` file contains a component that uses `setInterval` to update a counter every second.  However, it fails to clear the interval when the component unmounts, leading to the interval continuing to run even after the component is no longer needed. This results in a memory leak.

## Solution
The `bugSolution.js` file shows the corrected implementation.  It uses the return value of `useEffect` to clear the interval when the component unmounts, preventing the memory leak.

## How to Run
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install the dependencies.
4. Run `npm start` to start the development server.