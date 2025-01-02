# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The improper use of the dependency array leads to an infinite render loop.

## Bug Description

The `useEffect` hook, without a dependency array or with an incomplete dependency array, will re-run after every render.  This can cause an infinite loop if the effect itself triggers a state update that causes a re-render.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output and the component's behavior. You'll see the component re-renders continuously, and the count increases rapidly.

## Solution

The solution involves correctly specifying the dependency array in the `useEffect` hook.  The dependency array should list all state variables or props that the effect depends on.  If the effect doesn't depend on any state variables or props, use an empty array `[]`.
