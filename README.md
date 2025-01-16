# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The `useEffect` hook, without proper dependency management, can lead to infinite re-renders and performance issues.

## Bug Description

The provided `MyComponent` utilizes the `useEffect` hook to log a message after each render. However, the dependency array is missing.  This omission means the effect runs after every render, triggering another re-render, leading to an infinite loop.

## Solution

The solution involves correctly specifying the `count` variable in the dependency array.  This ensures the effect only runs when the value of `count` changes.