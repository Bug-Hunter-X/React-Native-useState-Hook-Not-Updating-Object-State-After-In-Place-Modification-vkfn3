# React Native useState Hook Not Updating Object State After In-Place Modification

This repository demonstrates a common error encountered when using the `useState` hook in React Native with object state.  Directly modifying the object using methods like `push` or `splice` does not trigger a re-render because these methods mutate the object in place instead of creating a new one.  The solution showcases the correct approach using spread syntax (...) to create a new object, ensuring React detects the changes.

## Bug
The `bug.js` file contains the erroneous code that modifies the state object directly. The component doesn't re-render correctly. 

## Solution
The `bugSolution.js` file shows the corrected implementation using the spread syntax to create a new object, effectively triggering re-renders in React.

## How to Reproduce
1. Clone this repository
2. Run `npm install`
3. Run `npx react-native run-android` or `npx react-native run-ios`
4. Observe the behavior and compare `bug.js` and `bugSolution.js`