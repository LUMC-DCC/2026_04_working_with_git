---
layout: center
transition: fade
---

# Undoing and recovering

One of the main points of version control: you can **go back in time to recover**.

<div class="p-4 border border-blue-400 rounded bg-blue-50 mt-4">

**It is almost always possible to recover.**
As long as you commit something once (or at least `git add` it), you can almost always get it back — no matter what you do.

</div>

> Some undo commands preserve history. Some modify it. If you've shared that history with others, modifying it can cause problems.

---

## Undoing uncommitted, unstaged changes

Undo all changes in the working directory:

```console
$ git restore .
```

Undo selectively:
```console
$ git restore -p              # choose which portions to undo
$ git restore PATH            # undo a specific file
```

If you have **staged** changes too:
```console
$ git restore --staged .      # unstage, then:
$ git restore .               # discard working dir changes

# Or do both at once:
$ git reset --hard HEAD
```

> `HEAD` is literally those four letters — not a placeholder.

---

## Reverting commits (preserves history)

You made a bad commit and want to undo it — safely:

```console
$ git log --oneline

e02efcd (HEAD -> main) not sure this is a good idea
b4af65b improve the documentation
e7cf023 don't forget to enjoy
```

Revert creates a **new commit** that does the opposite:

```console
$ git revert e02efcd
```

```console
$ git log --oneline

d3fc63a (HEAD -> main) Revert "not sure this is a good idea"
e02efcd not sure this is a good idea
b4af65b improve the documentation
```

The old commit stays in the history. You can revert any commit, no matter how old.

---

## Exercise: Revert a commit

1. Create a commit (commit A).
2. Revert it with `git revert` (commit B).
3. Inspect with `git log --oneline`.
4. Use `git show` on both commits A and B — what do you see?

---

## Amending the last commit (modifies history)

Forgot something? Add it to the previous commit:

```console
$ git add forgotten-file.md
$ git commit --amend
```

Also works to fix the last commit **message**.

<div class="p-4 border border-yellow-400 rounded bg-yellow-50 mt-4">

**Warning:** `--amend` changes the commit hash — it rewrites history.
Never amend commits you have already pushed and shared with others.

</div>

---

## Exercise: Amend a commit

1. Make an incomplete change, `git add` and `git commit` it.
2. Inspect it with `git show`. Note the commit hash.
3. Fix the change, then `git add` + `git commit --amend`.
4. What changed? (The commit hash is now different — history was rewritten.)

---

## Rewinding a branch (modifies history)

Move a branch label back to a previous commit — discarding everything after it:

```console
$ git reset --hard HASH
```

<div class="p-4 border border-red-400 rounded bg-red-50 mt-4">

Use this carefully. Check `git graph` before **and** after.
Other commits are not deleted immediately — dangling objects persist until garbage collection — but they become hard to find.

</div>

---

## Exercise: Reset to clean up

After experimenting with revert and amend, reset back to a known-good state:

```console
$ git log --oneline

d3fc63a (HEAD -> main) Revert "not sure this is a good idea"
e02efcd not sure this is a good idea
b4af65b improve the documentation
...

$ git reset --hard b4af65b

HEAD is now at b4af65b improve the documentation

$ git log --oneline

b4af65b (HEAD -> main) improve the documentation
e7cf023 don't forget to enjoy
...
```

---

## Recovering from committing to the wrong branch

**Solution 1 — `git cherry-pick`:**
1. Create the correct branch from the right starting point: `git branch BRANCHNAME HASH`
2. Switch to it.
3. `git cherry-pick HASH` — apply specific commits from oldest to newest.
4. Rewind the wrong branch with `git reset --hard`.

**Solution 2 — `git reset --hard`** (when the correct branch should have all commits):
1. Create the correct branch at the current commit: `git branch BRANCHNAME`
2. Verify with `git graph` that both branches point to the same commit.
3. Rewind the wrong branch with `git reset --hard`.

---

## Other recovery scenarios

**Merged/pulled into the wrong branch:**
1. Find the commit hash you want to rewind to with `git log`.
2. `git reset --hard HASH`

**Conflict after `git pull`:**
- Resolve the conflict as you would for a regular merge conflict.
- Or abort with `git merge --abort`.

---

<div class="p-4 border border-blue-400 rounded bg-blue-50">

**Test your understanding**

1. You accidentally remove a tracked file with `git rm`. Is it gone forever?
2. Is it OK to modify commits nobody has seen yet?
3. When would modifying Git history ever be justified?

</div>

<div class="p-4 border border-gray-300 rounded bg-gray-50 mt-4">

**Answers**

1. No — `git rm` makes a commit. `git revert` gets the file back.
2. Yes — if you haven't shared them, amending is fine.
3. Only in extraordinary cases: e.g. removing accidentally committed secrets or sensitive data.

</div>