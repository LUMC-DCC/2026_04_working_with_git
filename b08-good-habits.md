---
layout: center
transition: fade
---

# Block 8 — Good Habits

<div class="p-4 border border-green-400 rounded bg-green-50 mt-4 text-left">

**Learning objective**

Know the handful of habits that keep your git history useful, your repo clean, and your future self grateful — and set up `.gitignore` so the wrong files never end up tracked.

</div>

---

## Write commit messages that explain *why*

The diff already shows *what* changed. The message should say *why*:

<div class="grid grid-cols-2 gap-4 mt-4">

<div class="p-4 border border-red-300 rounded bg-red-50 text-sm">

**Useless messages**
```
fix
oops
save work
wip
changes
update
```
Future you will have no idea what these mean.

</div>

<div class="p-4 border border-green-400 rounded bg-green-50 text-sm">

**Useful messages**
```
increase alpha to 2.0 for faster convergence

the motivation for this change is to
speed up training on large cohorts;
based on discussion in issue #42
```
One summary line. Details below if needed.

</div>

</div>

> **Better an imperfect message than no commit at all.**

---

## Commit small and often

<div class="grid grid-cols-2 gap-4 mt-4 text-sm">

<div class="p-4 border border-green-400 rounded bg-green-50">

**Do this**

- Commit one logical change at a time
- Commit at the end of each work session
- Use the staging area to separate unrelated edits into clean commits
- Too many commits is always better than too few

</div>

<div class="p-4 border border-red-300 rounded bg-red-50">

**Avoid this**

- One giant commit with 20 unrelated changes
- Waiting until the code is "finished" before committing
- Committing everything with `git add .` without checking what you're staging

</div>

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm text-center">

Once committed, it is very hard to truly lose work. Commit often and commit freely.

</div>

---

## What NOT to commit

<div class="grid grid-cols-2 gap-4 mt-4 text-sm">

<div class="p-4 border border-red-300 rounded bg-red-50">

**Generated / compiled files**

`*.pyc`, `__pycache__/`, `*.Rout`, `node_modules/`, `dist/`

These are reproducible from source — tracking them adds noise to diffs and bloats the repo.

</div>

<div class="p-4 border border-red-300 rounded bg-red-50">

**Secrets and credentials**

API keys, passwords, `.env` files, SSH private keys.

Once pushed, a secret is compromised — even if you delete it in a later commit, it stays in the history.

</div>

<div class="p-4 border border-red-300 rounded bg-red-50">

**Large binary files**

Raw data, images, `.docx`, model weights.

Git stores full copies of every version — a 500 MB file committed once stays 500 MB in history forever.

</div>

<div class="p-4 border border-red-300 rounded bg-red-50">

**Editor junk**

`.DS_Store`, `Thumbs.db`, `.vscode/`, `*.swp`

Clutter that means nothing to anyone else on the project.

</div>

</div>

---

## `.gitignore` — tell Git what to skip

Create a file called `.gitignore` in your repo root:

```shell
# Python
*.pyc
__pycache__/

# R
*.Rout
.Rhistory
.RData

# Secrets
.env
secrets/

# OS junk
.DS_Store
Thumbs.db

# Generated output
dist/
results/plots/
```

- Patterns are matched against file paths — `*` is a wildcard
- A leading `/` anchors to the repo root; a trailing `/` matches directories
- Prefix with `!` to un-ignore something: `!results/plots/final_figure.png`
- Commit `.gitignore` itself — so everyone on the project uses the same rules

---

## `.gitignore` in VS Code and RStudio

Both IDEs surface untracked files. The quickest way to ignore one:

<div class="grid grid-cols-2 gap-4 mt-4 text-sm">

<div class="p-4 border border-purple-400 rounded bg-purple-50">

**VS Code**

Source Control panel → right-click any untracked file → **Add to .gitignore**

VS Code creates or updates `.gitignore` automatically.

</div>

<div class="p-4 border border-orange-400 rounded bg-orange-50">

**RStudio**

Use the `usethis` package:

```r
usethis::use_git_ignore(c("*.Rout", ".RData"))
```

Or edit `.gitignore` directly — it is a plain text file.

</div>

</div>

<div class="p-3 border border-yellow-400 rounded bg-yellow-50 mt-4 text-sm">

**Shortcut:** GitHub's template `.gitignore` files cover most languages. When creating a repo, select your language from the dropdown — GitHub pre-fills sensible ignores for you.

</div>

---

## Branching level — keep it simple to start

<div class="mt-4 text-sm">

| Situation | Suggested approach |
|-----------|-------------------|
| Solo researcher | Just `main` + a branch per experiment |
| Small team, informal | Commit to `main`, branch for bigger changes |
| Small team, reviewed changes | Feature branches + Pull Requests for everything |
| Open source / larger team | Protected `main`, PRs required, CI checks |

</div>

<div class="p-3 border border-green-400 rounded bg-green-50 mt-4 text-sm text-center">

Start simple and grow your git practice with your project. You don't need the full workflow on day one.

</div>

---

<div class="p-4 border border-green-400 rounded bg-green-50">

**Key takeaways — Block 8**

- Commit messages are for humans — write the *why*, not the *what*.
- Small, frequent commits are always better than large, rare ones.
- `.gitignore` early — before you accidentally commit a secret or a 2 GB dataset.
- Match your branching strategy to your team size — start with the simplest thing that works.

</div>
