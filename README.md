# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency. The `useEffect` hook is used to perform side effects, but if its dependencies are not properly specified, it can lead to unexpected behavior and performance issues.

## Bug Description
The `useEffect` hook runs after every render unless the dependency array is specified. Without the dependency array, the component will re-render and the effect will run again infinitely. This example shows a basic counter component that illustrates this issue. 

## Solution
The correct way to prevent infinite loops in useEffect is to make sure that all dependencies are listed in the dependency array. Adding `[count]` to the dependency array ensures that the effect only runs when the value of `count` changes.