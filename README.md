# React setInterval Memory Leak
This repository demonstrates a common error in React components: using `setInterval` within `useEffect` without a cleanup function. This leads to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a React component that increments a counter every second using `setInterval`. However, it fails to provide a cleanup function within the `useEffect` hook to stop the interval when the component unmounts. This results in the interval continuing to run even after the component is no longer rendered, leading to a memory leak.

## Solution
The `bugSolution.js` file provides the corrected component, which includes a cleanup function to `clearInterval` when the component unmounts. This ensures that the interval is properly stopped, preventing memory leaks.

## How to Run
1. Clone this repository.
2. Navigate to the repository directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.