# React Router Dom Catch-All Route Conflict

This repository demonstrates a common issue in React Router v6 where a catch-all route (`/*`) interferes with other routes, especially nested ones. The problem arises because the catch-all route always matches, effectively overriding specific routes even when they should take precedence.

## Problem

The provided `App.js` shows a simple React Router setup.  However, the catch-all route (`/*`) for the `NotFound` component is too broad and will always match, preventing other routes from working correctly.  This is a frequent error among developers using React Router's route matching mechanisms.

## Solution

The `AppSolution.js` demonstrates how to solve this problem using more specific route matching techniques and avoiding the broad catch-all route if possible. More fine-grained route matching enhances the accuracy and prevents unintentional overrides.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that navigating to `/about` will correctly display "About", but all other URLs will display "Not Found" even if not intended.
