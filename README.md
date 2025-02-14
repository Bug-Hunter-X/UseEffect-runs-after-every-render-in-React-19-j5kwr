# React 19 useEffect Bug

This repository demonstrates a common issue with the `useEffect` hook in React 19 where the effect runs after every render, potentially leading to performance issues.

## Bug Description

The provided `MyComponent` uses `useEffect` without any dependencies.  This means the effect runs after every render of the component, even if the count hasn't actually changed.  In this simple example, it's just logging to the console, but in a real-world application, this could cause unnecessary work and performance degradation.

## Solution

To fix this, add the count variable as a dependency array to the useEffect. This will ensure that the effect only runs when the `count` variable changes, thus improving efficiency and preventing unexpected behaviour.  See `bugSolution.js` for the corrected code.