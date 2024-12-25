# React 18 useEffect Without Dependencies Bug

This repository demonstrates a common error in React 18 and above related to the `useEffect` hook when used without dependency arrays.  Improper usage can lead to infinite loops or performance degradation.

## Bug Description

The `useEffect` hook, when called without a dependency array (`[]`), runs after every render. This can be problematic if the effect modifies state or performs side effects that trigger re-renders, creating an infinite render loop. In this case, it causes an infinite number of logs to the console.

## Bug Solution

The solution involves adding an empty dependency array `[]` to the `useEffect` to ensure it only runs after the initial render.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Open your browser and observe the console. You will see the message "Count updated" repeatedly logged.

## Solution

Refer to `bugSolution.js` for the corrected code.