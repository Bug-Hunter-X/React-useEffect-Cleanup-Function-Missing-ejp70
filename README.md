# React useEffect Cleanup Function Missing

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include a return statement for the cleanup function.  This can lead to memory leaks and unexpected behavior when components unmount.

## Problem

The `useEffect` hook in `bug.js` is missing a `return` statement within its effect function.  This is crucial for performing cleanup actions, such as canceling subscriptions, clearing timeouts, or removing event listeners, when the component is unmounted.

## Solution

`bugSolution.js` provides a corrected version of the code with a proper return statement in `useEffect`.  This ensures that any cleanup actions are performed before the component is removed from the DOM, preventing potential issues.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs to see the missing and corrected cleanup functions behavior.