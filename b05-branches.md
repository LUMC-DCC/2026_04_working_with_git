---
layout: center
transition: fade
---

# Block 5 — Branches

<div class="p-4 border border-green-400 rounded bg-green-50 mt-4 text-left">

**Learning objective**

Create a branch, make commits on it, and merge it back — so you can experiment freely without ever breaking your working version.

</div>

---

## Why branches?

So far your history is a single line:

<img src="/img/gitink/git-branch-1.svg" class="rounded mt-3 max-h-24 mx-auto" />

That works for solo work on one thing. But what if you want to:

- Try a new analysis approach while keeping the current one working?
- Fix a bug in your pipeline while also adding a new feature?
- Let a colleague work on their part without waiting for you?

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**A branch costs nothing** — it is just a label on a commit. Creating one takes less than a second.

</div>

---

## Branches let work diverge — and come back together

<img src="/img/gitink/git-branch-3.svg" class="rounded mt-3 max-h-44 mx-auto" />

- Each branch moves forward independently
- `main` stays stable while you experiment on a feature branch
- When you are happy, you **merge** the branch back into `main`

---

## Create a branch in VS Code

Click the **branch name in the status bar** (bottom-left):

<img src="/img/commits/vscode-create-branch.png" class="border rounded mt-3 max-h-56 mx-auto" />

Type a new branch name (e.g. `feature/new-analysis`) and press **Enter** — VS Code creates the branch and switches to it immediately.

---

## Switch branches in VS Code

The status bar always shows your current branch. Click it to switch:

<img src="/img/commits/vscode-change-branch.png" class="border rounded mt-3 max-h-56 mx-auto" />

Any commits you make now go onto this branch only — `main` is untouched.

---

## Create and switch branches in RStudio

Click the **branch name** in the Git pane (top-right of the pane):

<div class="grid grid-cols-2 gap-4 mt-3">

<img src="/img/commits/rstudio-create-branch.png" class="border rounded w-full" />

<img src="/img/commits/rstudio-switch.png" class="border rounded w-full" />

</div>

- **Left:** type a new branch name → **Create** — RStudio creates and switches in one step
- **Right:** select an existing branch from the dropdown to switch

---

## Merging — bringing work back together

When your branch is ready, merge it back into `main`:

<img src="/img/gitink/git-merge-1.svg" class="rounded mt-2 max-h-28 mx-auto" />

Git combines the two histories. If the same lines were not touched on both sides, the merge is **automatic**.

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-3 text-sm">

**Best practice for collaboration:** instead of merging locally, push your branch to GitHub/GitLab and open a **Pull Request** — this gives your collaborators a chance to review before the merge.

</div>

---

## Merge via Pull Request on GitHub

<img src="/img/merging/github-branches.png" class="border rounded mt-2 max-h-48 mx-auto" />

GitHub will show a banner when your branch has new commits. Click **Compare & pull request** → review the diff → **Merge pull request**.

After merging on GitHub, pull `main` back locally to sync:

```console
$ git switch main
$ git pull
```

---

## See all branches and their history

<div class="grid grid-cols-2 gap-4 mt-4">

<div class="text-sm">

**VS Code — Git Graph extension**

Gives a visual timeline of all branches side by side.

<img src="/img/commits/vscode-add-commit.png" class="border rounded mt-2 w-full" />

</div>

<div class="text-sm">

**RStudio — History with all branches**

Git pane → History → check **All branches**

<img src="/img/commits/rstudio-history-all-branches.png" class="border rounded mt-2 w-full" />

</div>

</div>

---

<div class="p-4 border border-green-400 rounded bg-green-50">

**Key takeaways — Block 5**

- A branch is free to create — use one for every new feature, fix, or experiment.
- `main` should always contain your last working, stable version.
- Merge locally for solo work; use a Pull Request for collaborative work.
- Next: pushing and pulling — keeping your local and remote copies in sync.

</div>
