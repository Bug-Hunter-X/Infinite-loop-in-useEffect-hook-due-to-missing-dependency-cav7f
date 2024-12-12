# React useEffect Hook Bug

This repository demonstrates a common error when using the React `useEffect` hook: omitting a necessary dependency from the dependency array, leading to an infinite loop.  The bug and solution are explained below.

## Bug Description
The `useEffect` hook is designed to perform side effects after a component renders.  However, if a dependency within the effect is not included in the dependency array, the effect will run on every render, potentially causing unintended behavior, including infinite loops.

## Solution
The solution involves correctly identifying all values used within the `useEffect` function and including them in the dependency array.  Failure to include a state variable, for instance, will cause a loop as the function will re-execute every time that state variable changes. 
