---
layout: block-cover
blockNum: "04"
transition: fade
---

<SlideLevel :level="1" />

# Block 4 — Your First Commit

<div class="p-4 border border-green-400 rounded bg-green-50 mt-4 text-left">

**Learning objective**

Create a repository on GitHub, clone it into VS Code or RStudio, make a change, and record it as a commit — the core loop you will repeat hundreds of times.

</div>

---

<SlideLevel :level="1" />

## Step 1 — Create a repository on GitHub

Click **"+"** in the top-right → **New repository**:

<img src="/img/basics/new-repo-form.png" class="border rounded mt-2 max-h-64 mx-auto" />

<div class="text-sm mt-2 text-gray-600">

- Give it a name (e.g. `my-first-repo`)
- Check **"Add a README file"** — this gives you something to clone immediately
- Leave everything else as default for now

</div>

---

<SlideLevel :level="1" />

## Step 2 — Clone into VS Code

**Copy the clone URL** from GitHub (green Code button → HTTPS or SSH).

In VS Code:

<img src="/img/sharing/vscode-start.png" class="border rounded mt-2 max-h-52 mx-auto" />

**Clone Git Repository** → paste the URL → choose a local folder → **Open** the cloned folder.

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-3 text-sm">

The Source Control icon in the left sidebar will now show the Git panel — that is your control centre for everything that follows.

</div>

---

<SlideLevel :level="2" />

## Step 2 (RStudio) — Clone into RStudio

**File → New Project → Version Control → Git**

<div class="grid grid-cols-2 gap-4 mt-3">

<img src="/img/commits/rstudio-remote-branches.png" class="border rounded w-full" />

<div class="text-sm mt-2">

1. Paste the clone URL
2. Choose a local folder
3. Click **Create Project**

RStudio opens the project with the **Git pane** active in the top-right panel — this is your Git control centre.

</div>

</div>

---

<SlideLevel :level="1" />

## The staging area — why it exists

Git records changes in **two steps** on purpose:

<img src="/img/git_stage_commit.svg" class="rounded mt-3 max-h-44 mx-auto" />

<div class="grid grid-cols-2 gap-4 mt-3 text-sm">

<div class="p-3 border border-gray-300 rounded bg-gray-50">

**Stage** — choose exactly which changes go into this commit. You can have 10 edited files but only commit 2.

</div>

<div class="p-3 border border-gray-300 rounded bg-gray-50">

**Commit** — permanently save that chosen snapshot with a message describing *why* you made this change.

</div>

</div>

---

<SlideLevel :level="1" />

## Step 3 — Stage and commit in VS Code

Edit `README.md`, then open the **Source Control panel** (`Ctrl+Shift+G`):

<img src="/img/commits/vscode-add-and-commit.png" class="border rounded mt-2 max-h-64 mx-auto" />

1. Hover over the changed file → click **+** to stage it
2. Type a commit message in the box at the top
3. Click **✓ Commit**

---

<SlideLevel :level="2" />

## Step 3 (RStudio) — Stage and commit in RStudio

Edit a file, then open the **Git pane → Commit**:

<div class="grid grid-cols-2 gap-4 mt-3">

<img src="/img/commits/rstudio-add-commit.png" class="border rounded w-full" />

<img src="/img/commits/rstudio-commit-changes.png" class="border rounded w-full" />

</div>

1. Check the box next to files you want to stage (left panel)
2. Review the diff (bottom panel — green = added, red = removed)
3. Type a commit message (top-right)
4. Click **Commit**

---

<SlideLevel :level="1" />

## Step 4 — View your history

After committing, check the log to see your work recorded:

<div class="grid grid-cols-2 gap-4 mt-4">

<div class="text-sm">

**VS Code**

Source Control panel → **...** menu → **View History**
(or install the **Git Graph** extension for a visual timeline)

<img src="/img/basics/history.png" class="border rounded mt-2 w-full" />

</div>

<div class="text-sm">

**RStudio**

Git pane → **History** (clock icon)

<img src="/img/browsing/history_RStudio.png" class="border rounded mt-2 w-full" />

</div>

</div>

---
layout: takeaways
transition: fade
---

<SlideLevel :level="1" />

<div class="p-4 border border-green-400 rounded bg-green-50">

**Key takeaways — Block 4**

- Create repo on GitHub → clone locally → edit → stage → commit. That is the core loop.
- The staging area lets you make clean, focused commits even when you have edited many files.
- Your history is now searchable — every change has a who, when, and why.
- Next: branches — how to work on a new idea without touching your working version.

</div>
