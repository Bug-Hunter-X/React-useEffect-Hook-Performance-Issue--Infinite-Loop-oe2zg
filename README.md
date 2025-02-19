# React useEffect Infinite Loop Bug
This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite loop due to missing dependencies. The `useEffect` runs after every render, which results in performance problems and excessive logging in this case.

## Bug Description
The `useEffect` hook in `MyComponent` lacks a dependency array, which makes it run after every render.  This leads to an infinite loop where the component continuously re-renders. 

## Solution
The solution involves adding the `count` variable to the dependency array. This ensures that the effect only runs when `count` changes.