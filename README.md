# Asynchronous State Access in React Router Dom v6
This repository demonstrates a common issue encountered when working with location state in React Router Dom v6. The problem arises from attempting to access the location state directly within a component before it's fully populated, resulting in undefined state values or errors.

## Problem
The `useLocation()` hook in React Router Dom v6 provides asynchronous access to the route's location object, which includes the state property.  If you try to use the state property within a component before it's fully loaded, you might encounter `undefined` values or errors. This is especially problematic in conditional rendering or within `useEffect` hooks that execute only once during mounting.

## Solution
The solution involves ensuring the state is available before attempting to access it.  This can be done by using a conditional check to make sure the state object exists. Also, utilize useEffect with dependency array to handle the asynchronous nature of the state object.

## Usage
Clone this repository and run `npm install`.  Then, you can run `npm start` to see the buggy and fixed components in action.