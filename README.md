# Tailwind CSS @apply Directive Silent Failure

This repository demonstrates a bug in Tailwind CSS where the `@apply` directive fails silently when a complex class name (containing multiple classes) includes an invalid class.  The error is not reported, making it difficult to debug.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` (or `yarn install`).
3. Start your development server.
4. Observe that the element with the `@apply` directive does not have the expected styles.

## Solution

The solution is to carefully check all classes within the `@apply` directive for correctness.  Use your IDE's autocompletion to avoid typos and confirm that all classes are defined in your `tailwind.config.js` file.

## Additional Notes

This issue highlights the importance of robust error handling in CSS preprocessors.  A more helpful error message from Tailwind CSS would make debugging this type of issue significantly easier.