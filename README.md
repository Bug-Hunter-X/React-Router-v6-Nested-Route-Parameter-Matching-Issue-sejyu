# React Router v6 Nested Route Parameter Matching Issue

This repository demonstrates a subtle bug in React Router v6 related to nested routes and parameter matching.  When a parent route contains a nested route with parameters, the parent route might not match correctly, leading to unexpected rendering behavior.

## Problem Description
The provided example shows a `Contact` component with a nested route `/contact/:id`. When navigating to `/contact/123`, it renders the `ContactDetail` correctly.  However, this is the expected behaviour. The unexpected behaviour is that navigating to `/contact` does not render the `Contact` component as expected, instead it renders nothing. This is because of the nested route that has a parameter that clashes with the parent route. 

## Solution
The solution involves using the `Outlet` component from React Router to render the nested route's children. This clarifies the route hierarchy and fixes the unexpected rendering behaviour.  This example demonstrates the correct implementation.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/contact`. You should not see anything.
5. Navigate to `/contact/123`. This should work as expected.
