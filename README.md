# React useEffect Hook Runs on Every Render

This repository demonstrates a common React issue where the `useEffect` hook runs on every render, leading to performance problems. The provided solution shows how to correctly use the `useEffect` hook's dependency array to optimize its execution.

## Bug

The initial `useEffect` hook in `bug.js` lacks the dependency array, causing it to execute on every render of the component, including every state update. This can be problematic for performance, especially if there are expensive computations inside the effect. The console log will also spam the console on every render.

## Solution

The solution in `bugSolution.js` shows the correct usage of `useEffect` hook's dependency array.  The dependency array `[count]` ensures the `useEffect` only runs when the `count` variable changes. This significantly improves the component's performance by avoiding unnecessary re-renders and computations. 
