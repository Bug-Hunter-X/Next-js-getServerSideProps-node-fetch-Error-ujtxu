# Next.js getServerSideProps node-fetch Error

This repository demonstrates a common error encountered when using `node-fetch` within a Next.js `getServerSideProps` function and provides a solution.

## Problem

The provided `bug.js` file attempts to use `node-fetch` within a `getServerSideProps` function.  This results in a runtime error because `node-fetch` is not automatically available in the Next.js environment.

## Solution

The `bugSolution.js` file shows the corrected code.  It addresses the error by:

1.  Using the correct import statement for `node-fetch`.  It's important to note that in the context of getServerSideProps it's already included in Next.js and doesn't need to be imported, however you will need to install it as a dependency
2. Implementing proper error handling to gracefully manage potential network issues during the fetch request.

## Setup

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the Next.js development server.  Navigate to `/about` to see the results.