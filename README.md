# React useEffect Hook - Infinite Re-renders

This repository demonstrates a common issue with React's `useEffect` hook: infinite re-renders caused by missing dependencies in the dependency array.

## Problem

The `MyComponent` component uses `useEffect` to log the count to the console after every render. However, the `count` variable is not included in the dependency array. This causes the effect to run on every render, leading to an infinite loop. 

## Solution

The solution is to include `count` in the dependency array: `[count]`. This ensures that the effect only runs when the value of `count` changes.