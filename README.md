# Mini LeetCode Clone

A compact, self-contained single-file HTML web app that provides a tiny LeetCode-like experience directly in the browser. Users can browse a small set of problems, read their descriptions, write JavaScript solutions in a code editor, and run automated tests to verify correctness.

Targeted to be drop-in deployable as a static page (index.html).

Generated: 2025-10-23

## Summary

The app presents a clean, modern UI with:
- A problem list and filtering (by difficulty) on the left.
- A problem detail view with description and sample tests on the right.
- An in-browser code editor (textarea) where users implement solve(input).
- A test runner that executes user code against predefined test cases and reports per-test results.

This is designed to be a minimal but fully functional introductory LeetCode-like environment that runs entirely in the browser without any server-side support.

## Key Features

- Problem catalog with 4 starter problems
  - Two Sum (Easy)
  - Reverse String (Easy)
  - Fizz Buzz (Easy)
  - Maximum Subarray (Medium)
- Problem filtering by difficulty (All / Easy / Medium / Hard)
- Live problem details view (title, difficulty badge, description, examples)
- In-browser code editor (JavaScript)
- Submit button to run tests against predefined inputs
- Per-test result reporting with pass/fail status
- Client-side deep equality checker for test verification
- Small, responsive UI with dark aesthetic

## Setup Instructions

- Save the provided file as index.html
- Open index.html in any modern web browser (Chrome, Firefox, Edge, Safari)
- No server is required; it’s a static front-end page

## Usage

1. Open the app and browse the problem list on the left.
2. Click a problem to load its details on the right.
3. Read the problem description and examples.
4. In the code editor, implement a function with the signature:
   - function solve(input) { ... }
   - The function must return the expected output for the given input.
5. Click “Submit” to run the tests.
6. Review per-test results and overall pass rate. The results panel shows input, expected, and actual outputs for each test case.
7. Use “Reset” to restore the starter template for the current problem.

## Technical Details

- Single HTML file: index.html with embedded CSS and JavaScript
- HTML structure:
  - Header with branding
  - Two-column responsive layout: sidebar (problem list) and main content (problem detail + editor)
- CSS:
  - Modern dark theme with glassy card UI
  - Responsive grid for desktop/tablet and single-column for smaller screens
  - Badges for difficulty with color cues
- JavaScript:
  - In-file problem data (PROBLEMS array)
  - Client-side rendering of problem list and details
  - Code editor is a plain textarea
  - Test harness uses a sandboxed Function() to evaluate user code
  - Deep equality checker for test result validation
  - Lightweight notification via inline messaging

## Deployment

- This is designed for static hosting (GitHub Pages, Netlify, Vercel, etc.)
- To deploy on GitHub Pages:
  - Create a new repository (e.g., mini-leetcode-clone)
  - Add index.html (the file above)
  - Push to main branch
  - In GitHub repo, enable Pages (root / main)
- The app will be served at https://<your-username>.github.io/<repo-name>/

## License

MIT License

## Generated

Date: 2025-10-23

## Notes

- The problem set is intentionally small for clarity and speed; you can expand PROBLEMS in the script to add more challenges.
- All code runs in the browser, with no external dependencies.