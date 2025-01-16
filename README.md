# Uncommon React useEffect Bug: Missing Dependency

This repository demonstrates a subtle bug in React's `useEffect` hook that can lead to unexpected behavior and performance issues.  The problem arises when the dependency array is missing or incorrect, causing the effect to run excessively.

## The Bug

In the `bug.js` file, the `useEffect` hook is used to log the current value of the `count` state variable. However, the dependency array is missing entirely. This causes the effect to run after every render, leading to an infinite loop of console logs and potentially blocking the UI.

## The Solution

The `bugSolution.js` file demonstrates the fix. By adding `count` to the dependency array `[count]`, the effect now only runs when the value of `count` changes. This prevents the infinite loop and ensures that the effect is only executed when necessary.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to run the application.
4. Observe the console log in `bug.js`. It will log excessively.
5. After fixing, run `npm start` for `bugSolution.js` and check the log.