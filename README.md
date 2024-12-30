# React useEffect Missing Dependency Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The example showcases an incorrect dependency array, leading to unexpected behavior and potentially stale data.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.  This bug is subtle but can lead to difficult-to-debug issues in larger applications.

## Bug Description
The `useEffect` hook attempts to fetch data and update the `count` state. However, the dependency array is empty (`[]`), meaning the effect runs only once when the component mounts. Subsequent changes to the `count` state do not trigger the effect, resulting in the data not updating accordingly. 

## Solution
The `bugSolution.js` file corrects this by adding `count` to the dependency array. Now, the effect will run whenever the `count` state changes, ensuring that the data is fetched and the component is updated properly.