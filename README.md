# Next.js 15: Blank screen on initial load with slow API route

This repository demonstrates a bug in a Next.js 15 application where a slow API route causes a blank screen on the initial load of a page.  The page displays a loading indicator, but the actual content does not render until after the API request completes. This issue is specific to Next.js 15's new features, which handle data fetching differently.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm run dev` to start the development server.
4. Navigate to `/about`. You will see a blank screen momentarily before the data is loaded.

## Solution

The solution involves using `Suspense` to handle asynchronous operations gracefully, making sure the loading state is managed correctly. Refer to the `aboutSolution.js` for a better implementation.