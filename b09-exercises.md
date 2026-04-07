---
layout: center
transition: fade
---

# Exercises — Putting it all together

<div class="p-4 border border-green-400 rounded bg-green-50 mt-4 text-left">

**Goal**

Work through five short exercises that each revisit one core skill from the session. Do them in order — each one builds on the last. Use VS Code or RStudio, whichever you prefer.

</div>

---

## Exercise 1 — Create a repo and make your first commit

**Setup:** create a fresh repository on GitHub, clone it, and record a meaningful commit.

<div class="mt-4 text-sm space-y-2">

1. Go to GitHub → **New repository**. Name it `git-cafe-practice`. Check "Add a README file". Click **Create repository**.
2. Clone the repo into VS Code (`Clone Git Repository`) or RStudio (`File → New Project → Version Control → Git`).
3. Open `README.md` and add a short sentence describing what you will use this repo for.
4. Stage the file and commit it with a message that explains *why* you made the change — not *what*.
5. Check your commit history and confirm the message is there.

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**Done when:** `git log` (or the history panel) shows your commit with your message.

</div>

---

## Exercise 2 — Work on a branch

**Goal:** make changes on a separate branch without touching `main`.

<div class="mt-4 text-sm space-y-2">

1. Create a new branch called `add-notes` and switch to it.
2. Create a new file called `notes.md` and write a few bullet points about what you learned today.
3. Stage and commit the file with a clear message.
4. Switch back to `main` and confirm `notes.md` is not there.
5. Merge `add-notes` into `main`.
6. Confirm `notes.md` is now on `main`.

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**Done when:** the merge is complete and `notes.md` appears on `main`.

</div>

---

## Exercise 3 — Push and pull

**Goal:** sync your local work to GitHub and simulate pulling remote changes.

<div class="mt-4 text-sm space-y-2">

1. Push your `main` branch to GitHub. Open the repo in the browser and confirm both `README.md` and `notes.md` are visible.
2. Edit `README.md` **directly on GitHub** (click the pencil icon) — add one more line. Commit the change on GitHub with a clear message.
3. Back in VS Code or RStudio, **pull** the changes. Confirm your local `README.md` now includes the line you added on GitHub.

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**Done when:** local and remote are in sync and `git status` reports "Your branch is up to date".

</div>

---

## Exercise 4 — Resolve a merge conflict

**Goal:** intentionally create a conflict and resolve it calmly.

<div class="mt-4 text-sm space-y-2">

1. Create a new branch called `experiment`.
2. On `experiment`, edit the first line of `README.md` and commit the change.
3. Switch back to `main`. Edit the **same first line** of `README.md` differently. Commit.
4. Merge `experiment` into `main` — Git will report a conflict.
5. Open the conflicted file, choose (or combine) the two versions, remove the conflict markers, and save.
6. Stage the resolved file and complete the merge with a commit.

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**Done when:** `git status` is clean and the history shows a merge commit.

</div>

---

## Exercise 5 — Add a `.gitignore`

**Goal:** protect your repo from files that should never be committed.

<div class="mt-4 text-sm space-y-2">

1. Create a file called `secret.env` in your repo folder (just put some dummy text in it).
2. Run `git status` — notice Git sees it as untracked.
3. Create a `.gitignore` file and add the line `*.env` to it.
4. Run `git status` again — `secret.env` should no longer appear.
5. Stage and commit `.gitignore` with an appropriate message.
6. **Bonus:** add patterns for your editor's junk files (`.DS_Store`, `Thumbs.db`, `.Rhistory`, etc.).

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**Done when:** `.gitignore` is committed and `secret.env` is invisible to Git.

</div>

---

## Quick reference — commands used today

<div class="grid grid-cols-2 gap-4 mt-4 text-sm">

<div class="p-4 border border-gray-300 rounded bg-gray-50">

**Local workflow**
```shell
git status
git add <file>
git commit -m "message"
git log --oneline
git diff
```

</div>

<div class="p-4 border border-gray-300 rounded bg-gray-50">

**Branches**
```shell
git branch <name>
git switch <name>
git merge <name>
git branch -d <name>
```

</div>

<div class="p-4 border border-gray-300 rounded bg-gray-50">

**Remote**
```shell
git clone <url>
git push
git pull
git fetch
```

</div>

<div class="p-4 border border-gray-300 rounded bg-gray-50">

**Inspect**
```shell
git log --oneline --graph
git show <commit>
git diff <branch1> <branch2>
```

</div>

</div>

---

<div class="p-4 border border-green-400 rounded bg-green-50">

**Well done!**

You have practised the complete Git workflow: creating a repo, committing, branching, pushing and pulling, resolving conflicts, and keeping your repo clean with `.gitignore`.

These five operations cover 95 % of everything you will use Git for day-to-day. The rest is just variations on this theme.

</div>
