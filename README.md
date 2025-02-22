# Unexpected Behavior in useEffect Hook

This repository demonstrates a potential issue in React applications related to using the `useEffect` hook with multiple state updates within a single function call. The `bug.js` file contains the buggy code. The solution is provided in `bugSolution.js`.

## Problem

The problem occurs when `setCount` is called twice within the `handleClick` function.  React's state updates are batched, but the second update might lead to unexpected behavior, especially when this state is also used within the `useEffect` hook, which might cause an infinite loop.