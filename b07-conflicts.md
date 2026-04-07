---
layout: center
transition: fade
---

# Block 7 — Merge Conflicts

<div class="p-4 border border-green-400 rounded bg-green-50 mt-4 text-left">

**Learning objective**

Recognise what a merge conflict is, understand why it happens, and resolve one using VS Code's merge editor or RStudio — without losing anyone's work.

</div>

---

## What causes a conflict?

Two branches modify the **same lines** of the same file in **different ways**:

<div class="grid grid-cols-3 gap-3 mt-4">

<div class="p-3 border border-gray-400 rounded bg-gray-50 text-sm">

**Original:**
```
1 tbsp cilantro
2 avocados
1 chili
1 lime
1 tsp salt
1/2 onion
```

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 text-sm">

**Branch A** — more cilantro:
```
2 tbsp cilantro
2 avocados
1 chili
1 lime
1 tsp salt
1/2 onion
```

</div>

<div class="p-3 border border-purple-400 rounded bg-purple-50 text-sm">

**Branch B** — less cilantro:
```
1/2 tbsp cilantro
2 avocados
1 chili
1 lime
1 tsp salt
1 onion
```

</div>

</div>

Git can auto-merge the onion change — but not cilantro. That is your conflict.

---

## Conflicts are not errors — they are questions

<div class="p-4 border border-blue-400 rounded bg-blue-50 mt-4">

Git is asking: *"Both branches touched this line. I cannot decide which version to keep — you need to tell me."*

</div>

- Git **never silently overwrites** one version with another
- Conflicts look alarming at first — with practice they take seconds to resolve
- You only get conflicts because you *can* work in parallel — simpler tools just prevent that

---

## What the conflict looks like in the file

Git inserts **conflict markers** directly into the file:

```
<<<<<<< HEAD
2 tbsp cilantro
=======
1/2 tbsp cilantro
>>>>>>> branch-b
```

<div class="grid grid-cols-3 gap-3 mt-4 text-sm">

<div class="p-3 border border-blue-400 rounded bg-blue-50">

`<<<<<<< HEAD`

Your current branch's version

</div>

<div class="p-3 border border-gray-300 rounded bg-gray-50">

`=======`

The divider between the two versions

</div>

<div class="p-3 border border-purple-400 rounded bg-purple-50">

`>>>>>>> branch-b`

The incoming branch's version

</div>

</div>

Your job: edit the file to look exactly how you want it, then remove all three markers.

---

## Resolving conflicts in VS Code

VS Code detects conflict markers and shows a visual editor:

<img src="/img/gh-desktop-changes/vscode_conflicts.jpg" class="border rounded mt-3 max-h-64 mx-auto" />

Click one of the inline options above the conflict:
- **Accept Current Change** — keep your version
- **Accept Incoming Change** — keep the other branch
- **Accept Both Changes** — keep both (one after the other)
- **Compare Changes** — open a side-by-side diff first

---

## Resolving conflicts in RStudio

RStudio highlights conflict markers in the editor. Open the conflicted file and edit it manually:

<div class="grid grid-cols-2 gap-4 mt-4">

<img src="/img/contributing/conflict-resolution.png" class="border rounded w-full" />

<div class="text-sm mt-2">

1. Find the `<<<<<<<` markers in the file
2. Decide which version to keep (or combine them)
3. Delete all three marker lines
4. Save the file
5. In the Git pane: stage the resolved file (check the box)
6. Click **Commit** — the merge commit message is pre-filled

</div>

</div>

---

## After resolving — complete the merge

Once you have edited the file and removed all markers:

**VS Code:**
1. Save the file
2. Source Control panel → the file moves from **Merge Changes** to **Staged Changes** automatically
3. Click **✓ Commit** — the message "Merge branch '...'" is pre-filled

**RStudio:**
1. Stage the resolved file in the Git pane
2. Click **Commit** — pre-filled message, just click Commit again

<div class="p-3 border border-yellow-400 rounded bg-yellow-50 mt-3 text-sm">

Not happy with how the resolution is going? Both IDEs let you abort: VS Code → **...** → **Abort Merge** / RStudio terminal: `git merge --abort`. The repo returns to exactly the state before the merge.

</div>

---

## How to avoid conflicts in the first place

<div class="grid grid-cols-2 gap-4 mt-4 text-sm">

<div class="p-4 border border-green-400 rounded bg-green-50">

**Work habits**

- Pull before you start each day
- Push small commits often — don't sit on local work for days
- Keep branches short-lived and focused

</div>

<div class="p-4 border border-blue-400 rounded bg-blue-50">

**Team habits**

- Talk before starting work on the same file
- Use issues or PRs to signal what you are working on
- Don't put unrelated changes in the same branch

</div>

</div>

---

<div class="p-4 border border-green-400 rounded bg-green-50">

**Key takeaways — Block 7**

- A conflict means Git found the same lines changed two different ways — it needs your decision.
- VS Code's inline buttons make simple conflicts a one-click fix.
- When in doubt, abort the merge — your work is safe, nothing is lost.
- Next: good habits that keep your history clean and conflicts rare.

</div>
