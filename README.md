# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook and its dependency array.  The `useEffect` hook, while powerful for managing side effects, can lead to unexpected behavior if its dependencies are not correctly specified.

## The Bug

The `bug.js` file contains a component that uses `useEffect` to update a counter every second. However, the dependency array is empty (`[]`), meaning the effect runs after every render. This causes an infinite loop because each update triggers a re-render, leading to continuous counter increments. 

## The Solution

The solution, provided in `bugSolution.js`, correctly includes `count` in the dependency array. This ensures that the effect only runs when the `count` value changes, preventing the infinite loop.

## How to reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in `bug.js` and the correct behavior in `bugSolution.js`.