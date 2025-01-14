# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React bug involving inefficient use of the `useEffect` hook. The `useEffect` hook, without dependency array, runs after every render, leading to performance issues and potential unexpected behavior. The solution shows how to correctly use the dependency array to optimize the hook's execution.

## Bug Description
The provided `MyComponent` function uses `useEffect` without a dependency array.  This causes the effect to run on every render of the component, logging 'Component rendered!' to the console repeatedly. This is inefficient and can negatively impact performance, especially in more complex components.

## Solution
The solution demonstrates the correct use of the dependency array in `useEffect`. By specifying `[count]` as a dependency array, the effect only runs when the `count` state variable changes, eliminating the unnecessary re-renders. 