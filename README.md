# React Router Dom v6 Catch-all Route Conflict

This repository demonstrates a common issue in React Router v6 involving catch-all routes (`/*`). When a catch-all route is defined, it can unintentionally override more specific routes, leading to unexpected behavior.

## Issue Description

The problem arises when a catch-all route (`/*`) is placed after more specific routes. In this scenario, the catch-all route will always match, regardless of the URL, effectively preventing other routes from working correctly.  This is especially problematic when trying to create a 404 Not Found page, as it will always render instead of the intended routes.

## Solution

The solution is to place the catch-all route as the *last* route within your `Routes` component. This ensures that it only matches URLs that don't match any other more specific routes.