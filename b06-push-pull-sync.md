---
layout: block-cover
blockNum: "06"
transition: fade
---

<SlideLevel :level="1" />

# Block 6 — Push, Pull & Sync

<div class="p-4 border border-green-400 rounded bg-green-50 mt-4 text-left">

**Learning objective**

Keep your local repository and GitHub/GitLab in sync — push your commits to share them, pull to receive others', and understand what happens when the two copies diverge.

</div>

---

<SlideLevel :level="1" />

## Local vs. remote — two copies of your repo

<img src="/img/illustrations/clone.png" class="rounded mt-3 max-h-48 mx-auto" />

<div class="grid grid-cols-3 gap-3 mt-3 text-sm">

<div class="p-3 border border-blue-400 rounded bg-blue-50 text-center">

**Push**

Send your local commits to GitHub/GitLab

↑

</div>

<div class="p-3 border border-gray-300 rounded bg-gray-50 text-center">

**Your laptop**

Where you edit and commit

</div>

<div class="p-3 border border-green-400 rounded bg-green-50 text-center">

**Pull**

Receive commits from GitHub/GitLab

↓

</div>

</div>

<div class="mt-3 text-sm text-gray-500 text-center">

Commits stay local until you push. The remote stays ahead until you pull.

</div>

---

<SlideLevel :level="1" />

## Push in VS Code

After committing, the Source Control panel shows **"Sync Changes"** or **"Push"**:

<img src="/img/sharing/vscode-publish-to-github1.png" class="border rounded mt-3 max-h-56 mx-auto" />

Click it — VS Code pushes your commits to GitHub and pulls any new remote commits in one step.

<div class="p-3 border border-yellow-400 rounded bg-yellow-50 mt-3 text-sm">

First push on a new branch? VS Code will ask you to publish the branch — click **OK**. It creates the remote branch automatically.

</div>

---

<SlideLevel :level="1" />

## Pull in VS Code

When a collaborator has pushed new commits (or you edited something on GitHub.com), use **Pull** to bring them down:

<img src="/img/sharing/vscode-publish-to-github2.png" class="border rounded mt-3 max-h-56 mx-auto" />

In VS Code: Source Control panel → **...** → **Pull**
— or click the **↓ number** in the status bar if it shows pending commits.

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-3 text-sm">

**Tip:** pull before you start working each day. It avoids diverged histories and makes merges much smaller.

</div>

---

<SlideLevel :level="2" />

## Push and pull in RStudio

The Git pane has dedicated **Push** (↑) and **Pull** (↓) buttons:

<img src="/img/commits/rstudio-remote-branches.png" class="border rounded mt-3 max-h-52 mx-auto" />

- **Push ↑** — sends your local commits to the remote
- **Pull ↓** — fetches and merges remote commits into your current branch

Both buttons show a counter badge when there are commits to send or receive.

---

<SlideLevel :level="2" />

## Fetch vs. Pull — what is the difference?

<div class="grid grid-cols-2 gap-4 mt-4">

<div class="p-4 border border-blue-400 rounded bg-blue-50 text-sm">

**Fetch**

Downloads remote commits into a holding area — but does **not** touch your working files.

Safe to run at any time. Use it to *check* what changed before deciding to pull.

</div>

<div class="p-4 border border-green-400 rounded bg-green-50 text-sm">

**Pull**

Fetch + immediately merge into your current branch.

The everyday command — use this when you are ready to incorporate remote changes.

</div>

</div>

<div class="p-3 border border-gray-300 rounded bg-gray-50 mt-4 text-sm text-center">

For day-to-day work: just use **Pull** (or **Sync** in VS Code). Fetch is useful when you want to look before you leap.

</div>

---

<SlideLevel :level="1" />

## What if local and remote have both moved on?

<img src="/img/gitink/git-collaborative.svg" class="rounded mt-3 max-h-32 mx-auto" />

Git will try to **auto-merge** when you pull. If the same lines were not changed on both sides, it succeeds silently.

If they were — you get a **merge conflict** (we cover this in the next block).

<div class="p-3 border border-yellow-400 rounded bg-yellow-50 mt-3 text-sm">

**Prevention:** push and pull frequently. Small divergences are easy to merge. Six months of divergence is not.

</div>

---
layout: takeaways
transition: fade
---

<SlideLevel :level="1" />

<div class="p-4 border border-green-400 rounded bg-green-50">

**Key takeaways — Block 6**

- Commits are local until you push — push to back up and share.
- Pull before you start work; push when you are done.
- VS Code **Sync** = pull + push in one click — fine for most workflows.
- Next: what happens when two people change the same line — merge conflicts.

</div>
