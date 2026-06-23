# Faster Autoplay Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Reduce the 13-page H5 autoplay duration from 65.5 seconds to 43.3 seconds using content-aware page timing.

**Architecture:** Keep the existing `data-duration`-driven timer system unchanged. Update only the duration attributes and add a regression assertion that verifies the exact timing sequence and total runtime.

**Tech Stack:** HTML, JavaScript, Node.js assertions

---

### Task 1: Lock the intended playback rhythm

**Files:**
- Modify: `tests/xiaowei-online-fixes.test.mjs`
- Modify: `xiaowei_mom_demo.html`

- [ ] **Step 1: Write the failing test**

Extract all `data-duration` values, assert the exact 13-value sequence, and assert a total of `43300`.

- [ ] **Step 2: Run test to verify it fails**

Run: `node tests/xiaowei-online-fixes.test.mjs`

Expected: FAIL because the current durations total `65500`.

- [ ] **Step 3: Write minimal implementation**

Set the 13 slide durations to:

```text
2000, 3000, 2000, 4500, 3200, 2800, 2800, 4500, 4500, 3500, 3500, 3000, 4000
```

- [ ] **Step 4: Run test to verify it passes**

Run: `node tests/xiaowei-online-fixes.test.mjs`

Expected: PASS with all assertions.

- [ ] **Step 5: Verify and publish**

Run `git diff --check`, commit the HTML and documentation, push `main`, and download the GitHub Pages URL with a cache-busting query to verify the published durations.
