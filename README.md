# useEffect Cleanup Function Not Called on Unmount

This example demonstrates a scenario where the cleanup function in `useEffect` might not be called if the component is unmounted before the effect has a chance to run.

## Bug
The `useEffect` hook is used to log the count and perform a cleanup. If the component is unmounted quickly (e.g., in a rapid navigation), the cleanup may not be executed, leading to potential memory leaks or unexpected behavior. 

## Solution
Ensure that the cleanup function in `useEffect` is always executed, even if the component unmounts before the effect's first run.  The solution demonstrates an improved way to handle cleanup that will execute regardless of the timing of unmount.