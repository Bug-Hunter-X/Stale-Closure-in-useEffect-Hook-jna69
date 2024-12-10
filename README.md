# Stale Closure in useEffect Hook

This repository demonstrates a common error in React applications involving stale closures within the `useEffect` hook.  The example showcases a counter that unexpectedly behaves erratically due to improper handling of the `setCount` function within a closure.

The issue lies in how the `setInterval` function is used within `useEffect`.  Because `setCount` is captured in a closure, it might not update to the latest version of the function when the component re-renders. This leads to either the counter updating slower than anticipated or the count completely stopping.

The solution demonstrates the correct approach using functional updates to prevent this stale closure issue.