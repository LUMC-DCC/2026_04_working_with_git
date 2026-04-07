---
layout: center
transition: fade
---

# Block 2 — Key Concepts

<div class="p-4 border border-green-400 rounded bg-green-50 mt-4 text-left">

**Learning objective**

Be able to define and recognise: repository, commit, branch, and remote — the four building blocks you will use in every git workflow.

</div>

---

## Repository

A **repository** (repo) is just a folder that Git is tracking.

- Everything lives inside that folder — your files and the full history
- The history is stored in a hidden `.git` subfolder
- Delete `.git` and you lose the history, but keep the files
- Move or rename the folder and everything still works

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**In VS Code / RStudio:** opening a repo folder is all you need — the IDE detects `.git` automatically and activates the Git panel.

</div>

---

## Commit

A **commit** is a snapshot of your entire project at one moment in time.

<img src="/img/basics/commits-snapshots.png" class="border rounded mt-3 max-h-52 mx-auto" />

<div class="grid grid-cols-2 gap-4 mt-3 text-sm">

<div class="p-3 border border-gray-300 rounded bg-gray-50">

- Each commit has a unique **hash** (e.g. `a3394e3`)
- Hash is computed from the content — identical content always gives the same hash
- Commits are **permanent** — you can always go back

</div>

<div class="p-3 border border-gray-300 rounded bg-gray-50">

- A commit also stores: author, timestamp, and a **message**
- The message is your note to your future self (and colleagues)
- Think of commits as checkpoints in a video game

</div>

</div>

---

## Commits form a chain

Each commit points back to its parent — forming a **history**:

<img src="/img/gitink/git-branch-1.svg" class="rounded mt-3 max-h-28 mx-auto" />

```
f146d25  adding ingredients
3696246  adding instructions
a3394e3  adding README
79161b6  add half an onion
e7cf023  don't forget to enjoy  ← most recent
```

> `HEAD` is just a label that says: *"this is where you are right now."*

---

## Branch

A **branch** is a separate line of work that can later be merged back.

<img src="/img/gopher/gophers.png" class="rounded mx-auto max-h-44 mt-2" />

<img src="/img/gitink/git-branch-3.svg" class="rounded mx-auto max-h-28 mt-2" />

- `main` is just the default branch name — nothing special about it
- Creating a branch is free and instant — it is just a label on a commit
- Branches let you experiment without touching your working version

---

## Remote

A **remote** is a copy of your repository hosted somewhere else — usually GitHub or GitLab.

<img src="/img/illustrations/sharing.png" class="rounded mx-auto max-h-48 mt-3" />

<div class="grid grid-cols-2 gap-4 mt-3 text-sm">

<div class="p-3 border border-gray-300 rounded bg-gray-50">

**Your laptop (local)**
- Where you edit files
- Where you make commits
- Works fully offline

</div>

<div class="p-3 border border-gray-300 rounded bg-gray-50">

**GitHub / GitLab (remote)**
- Backup of your history
- Shared with collaborators
- Source of truth for the team

</div>

</div>

---

## The four concepts together

<div class="grid grid-cols-2 gap-4 mt-4">

<div class="p-4 border border-blue-400 rounded bg-blue-50 text-sm">

**Repository**
Your project folder with full history stored in `.git`

</div>

<div class="p-4 border border-purple-400 rounded bg-purple-50 text-sm">

**Commit**
A named snapshot — the unit of history

</div>

<div class="p-4 border border-yellow-400 rounded bg-yellow-50 text-sm">

**Branch**
A parallel line of work — cheap to create, safe to experiment on

</div>

<div class="p-4 border border-green-400 rounded bg-green-50 text-sm">

**Remote**
The hosted copy on GitHub / GitLab — backup + collaboration hub

</div>

</div>

---

<div class="p-4 border border-green-400 rounded bg-green-50">

**Key takeaways — Block 2**

- A repo is a folder; a commit is a snapshot; a branch is a label; a remote is a hosted copy.
- You will use these four words constantly — everything else in Git is built on top of them.
- Next: we set up Git so it knows who you are and can talk to GitHub/GitLab.

</div>
