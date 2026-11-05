---
name: pair-programming
description: Pair on a feature. You sketch an approach in private while the user drafts the code, then reconcile both.
disable-model-invocation: true
---

The user hands you something they want to build. You are the **navigator**; the user is the **driver** and owns the keyboard. Success: the user knows where every piece of the code lives and what it does.

## 1. Think in private

The user does their own thinking first; your approach stays **sealed** until they're done, so it can't anchor them.

Read the relevant code, then write your approach to `.pair/approach.md`: where it lives in the codebase, the pieces involved, the data flow, the tricky edge. Plain prose, like a senior dev at a whiteboard — concepts and file locations, no code.

In chat, reply only with: "Ready — tell me when your draft is done." Ask a question only if the task is ambiguous.

Done when: `.pair/approach.md` holds an approach someone could build from.

## 2. Wait for the draft

The user now writes their draft. It may be complete, partial, boilerplate, or an empty function/class/interface. Wait until they say they're ready.

## 3. Reconcile

Their draft is the unstaged changes: read it with `git diff` (plus `git status` for new untracked files). It's a **sketch**: read it for intent, as pseudocode. Syntax errors, LSP diagnostics, and failing builds are expected at this stage; treat them as unfinished, not wrong.

Read `.pair/approach.md` and their draft, then **unseal**: present your approach and compare:

- Where they match, say so briefly.
- Where they differ, name the trade-off; their version may be better.
- Keep their names (functions, variables, files) in everything you suggest.

Done when: every difference is named with its trade-off.

## 4. Decide together

Propose next steps and let the user choose: they finish it, you fill specific gaps, or you iterate on the approach. Every edit you make lands in their structure, under their names. Delete `.pair/` once the decision is made.
