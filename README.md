# React useEffect Infinite Loop Bug
This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from incorrectly updating a state variable within the dependency array of the `useEffect` hook, leading to an infinite loop.

## The Bug
The `bug.js` file contains a `MyComponent` that attempts to increment a counter using `useEffect`.  The problem is that `count` is included in the dependency array, meaning the effect runs every time `count` changes, creating an infinite loop.

## The Solution
The `bugSolution.js` file provides a corrected version of the component. The solution involves using a functional approach to avoid direct dependency on count, and remove the dependency on count from the array. 

## How to Reproduce
1. Clone this repository.
2. Navigate to the directory `bug.js`
3. Run `npm install` to install the necessary packages. 
4. Run `npm start` to start the React application.
5. Observe the infinite loop in your browser's console.