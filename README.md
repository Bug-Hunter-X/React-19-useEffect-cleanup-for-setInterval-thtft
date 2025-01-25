# React 19 useEffect Cleanup for setInterval

This repository demonstrates a common error in React 19 related to the use of `setInterval` within the `useEffect` hook. Forgetting to return a cleanup function to stop the interval can lead to memory leaks. 

## Problem
The provided `bug.js` demonstrates an incorrect implementation where a `setInterval` is started but never stopped.  When the component unmounts, the interval continues running in the background, consuming resources.

## Solution
The `bugSolution.js` provides a corrected implementation. It includes a cleanup function that is returned from the `useEffect` hook, ensuring the interval is cleared when the component is unmounted or when dependencies change.