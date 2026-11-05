---
name: tdd-first
description: Use when the user asks you to implement, add, or build a feature or function — propose the tests before writing code.
---

Before writing any implementation, propose how you will **test** it.

1. Read the code it touches and the project's existing test setup (framework, file layout, naming). Write tests against signatures that already exist or that the user has given you; when the shape is still open, get an implementation frame from the user first (`implementation-frame` skill).
2. Present the test cases: one line each, stating input → expected behaviour. Cover the happy path, the edges, and the failure cases. Show test code only if a case is hard to state in a line.
3. Wait for the user's verdict. Revise until they approve.
4. Write the tests, run them, see them go **red**.
5. Implement until they go **green**. Run the full suite.

Done when: the approved tests pass and nothing else broke.
