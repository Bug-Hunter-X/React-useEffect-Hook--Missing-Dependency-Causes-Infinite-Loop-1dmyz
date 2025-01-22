# React useEffect Hook: Missing Dependency Causes Infinite Loop

This repository demonstrates a common error in React's `useEffect` hook: omitting a dependency from the dependency array.  This can lead to unexpected behavior, often an infinite render loop.

## The Bug

The `bug.js` file shows the problematic code. The `useEffect` hook logs the current `count` to the console. However, `count` is *not* included in the dependency array.  This means the effect runs after *every* render, regardless of whether `count` has changed, leading to an infinite loop.

## The Solution

The `bugSolution.js` file demonstrates the correct usage. The `count` variable is now included in the dependency array (`[count]`).  The effect will only run when `count` changes. 