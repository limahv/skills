---
name: implementation-frame
description: Use when your next question to the user is about names, signatures, types, data shapes, or file placement — ask them to write an implementation frame in code instead of specifying it in prose.
---

Details that code states precisely (names, signatures, types, data shapes, where things live) get settled in code, by the user. Their **frame** is the ground truth; you build inside it.

Questions about *what* the feature should do stay in conversation. Reach for a frame once the open questions are about *how it's shaped*.

## 1. Ask for the frame

Tell the user which shape questions are open and ask them to write a frame covering them: function or method signatures, types/interfaces, empty classes, files in place, `TODO` bodies. One line on what you need beats a list of prose questions. Then wait until they say it's ready.

## 2. Read the frame

The frame is the unstaged changes: read it with `git diff` (plus `git status` for new untracked files). It's a **sketch**: read it for intent. Syntax errors, LSP diagnostics, and failing builds are expected at this stage; treat them as unfinished, not wrong.

## 3. Build inside the frame

Fill the gaps: empty bodies, `TODO`s, missing glue. Keep every name, signature, type, and file location exactly as the user wrote it. When the frame itself looks wrong or blocks you, stop and propose the change to the user before touching it.

Done when: every gap is filled, the code builds, and the frame's names, signatures, and locations are unchanged.
