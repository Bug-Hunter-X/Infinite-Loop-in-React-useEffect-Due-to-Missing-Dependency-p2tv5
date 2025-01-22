# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by an incorrectly used `useEffect` hook.  The `useEffect` hook is intended to perform side effects, but without specifying the dependencies correctly, it can lead to unexpected re-renders.

## Bug Description

The `bug.js` file contains a React component that uses `useEffect` to log the current count to the console. However, the dependency array is missing the `count` variable, causing the effect to run after every render, regardless of whether the `count` has actually changed. This creates an infinite loop, leading to performance issues and potential crashes.

## Bug Solution

The `bugSolution.js` file demonstrates the corrected implementation. By correctly specifying `[count]` as the dependency array, the `useEffect` hook only runs when the `count` value changes.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the console (bug.js). 
5. Compare to the corrected solution in bugSolution.js