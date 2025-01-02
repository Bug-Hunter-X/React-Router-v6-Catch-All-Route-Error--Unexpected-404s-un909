# React Router v6 Catch-All Route Error
This repository demonstrates a common error in React Router v6 related to the placement of catch-all routes (`/*`).  Improper placement leads to other routes never matching, resulting in frequent, unexpected 404 errors.

## The Problem
When a catch-all route (`/*`) is placed before more specific routes, React Router will always match the catch-all route first, regardless of the requested path. This effectively prevents any other routes from being reached.

## Solution
The solution is to move the catch-all route to the end of your route definitions. This ensures that React Router attempts to match other routes before resorting to the catch-all as a last resort.