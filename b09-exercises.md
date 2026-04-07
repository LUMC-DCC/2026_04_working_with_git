---
layout: block-cover
blockNum: "Ex"
transition: fade
---

<SlideLevel :level="1" />

# Exercises — Putting it all together

<div class="p-4 border border-green-400 rounded bg-green-50 mt-4 text-left">

**Two main exercises — the rest are optional**

Exercise 1 gets you set up and makes your first commit. Exercise 2 is a live collaboration on this repo. Exercises 3–5 are there if you want to go further on your own.

</div>

---

<SlideLevel :level="1" />

## Before you start — Setup checklist

<div class="grid grid-cols-2 gap-x-8 gap-y-1 mt-3 text-xs">

<div>
<p class="font-semibold text-gray-500 uppercase tracking-wide text-[0.6rem] mb-1">GitHub / GitLab account</p>
<label class="flex items-start gap-2 cursor-pointer mb-1"><input type="checkbox" class="mt-0.5 shrink-0" /><span>Create a free account at github.com (or GitLab)</span></label>

<p class="font-semibold text-gray-500 uppercase tracking-wide text-[0.6rem] mb-1 mt-2">Git installed</p>
<label class="flex items-start gap-2 cursor-pointer mb-1"><input type="checkbox" class="mt-0.5 shrink-0" /><span>macOS: <code>brew install git</code> or Xcode Command Line Tools</span></label>
<label class="flex items-start gap-2 cursor-pointer mb-1"><input type="checkbox" class="mt-0.5 shrink-0" /><span>Windows: <strong>Git for Windows</strong> from git-scm.com</span></label>
<label class="flex items-start gap-2 cursor-pointer mb-1"><input type="checkbox" class="mt-0.5 shrink-0" /><span>Linux: <code>sudo apt install git</code></span></label>
<label class="flex items-start gap-2 cursor-pointer mb-1"><input type="checkbox" class="mt-0.5 shrink-0" /><span>Verify: <code>git --version</code></span></label>
</div>

<div>
<p class="font-semibold text-gray-500 uppercase tracking-wide text-[0.6rem] mb-1">SSH key (recommended)</p>
<label class="flex items-start gap-2 cursor-pointer mb-1"><input type="checkbox" class="mt-0.5 shrink-0" /><span>Generate: <code>ssh-keygen -t ed25519 -C "your@email"</code></span></label>
<label class="flex items-start gap-2 cursor-pointer mb-1"><input type="checkbox" class="mt-0.5 shrink-0" /><span>Copy key: <code>cat ~/.ssh/id_ed25519.pub</code></span></label>
<label class="flex items-start gap-2 cursor-pointer mb-1"><input type="checkbox" class="mt-0.5 shrink-0" /><span>Add on GitHub: <strong>Settings → SSH keys → New SSH key</strong></span></label>
<label class="flex items-start gap-2 cursor-pointer mb-1"><input type="checkbox" class="mt-0.5 shrink-0" /><span>Test: <code>ssh -T git@github.com</code></span></label>

<p class="font-semibold text-gray-500 uppercase tracking-wide text-[0.6rem] mb-1 mt-2">Editor</p>
<label class="flex items-start gap-2 cursor-pointer mb-1"><input type="checkbox" class="mt-0.5 shrink-0" /><span>VS Code or RStudio is open and ready</span></label>
</div>

</div>

---

<SlideLevel :level="1" />

## Exercise 1 — Your first commit <span class="ml-2 text-xs font-semibold px-2 py-0.5 rounded bg-green-100 text-green-800 border border-green-300">Beginner</span>

**Goal:** create your own repo, clone it, and record a meaningful commit.

<div class="text-sm space-y-1 mt-4">

<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Go to GitHub → <strong>New repository</strong>. Name it <code>git-cafe-practice</code>. Check "Add a README file". Click <strong>Create repository</strong>.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Clone into VS Code (<em>Clone Git Repository</em>) or RStudio (<em>File → New Project → Version Control → Git</em>).</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Open <code>README.md</code> and add a sentence describing what you will use this repo for.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Stage the file and commit with a message that explains <em>why</em> you made the change — not <em>what</em>.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Push to GitHub. Open the repo in your browser and confirm the commit is there.</span></label>

</div>

<div class="p-3 border border-green-400 rounded bg-green-50 mt-4 text-sm">

**Done when:** the history panel shows your commit with your message and the change is visible on GitHub.

</div>

---

<SlideLevel :level="1" />

## Exercise 2 — Collaborate on this repo <span class="ml-2 text-xs font-semibold px-2 py-0.5 rounded bg-blue-100 text-blue-800 border border-blue-300">Main exercise</span>

**Goal:** clone the session repo, add a slide on your own branch, and open a Pull Request.

<div class="text-sm space-y-1 mt-3">

<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Clone the session repo: <code>git clone git@github.com:LUMC-DCC/2026_04_working_with_git.git</code></span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Create a new branch: <code>git switch -c add-slide/&lt;topic&gt;</code> — pick a short topic name, no personal info needed.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Create a new file <code>contributions/&lt;topic&gt;.md</code> with a single slide — a quote, a tip, a lesson learned, or something you want to share. See the template on the next slide.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Stage and commit: <code>git add contributions/&lt;topic&gt;.md</code> then <code>git commit -m "add contribution slide: &lt;topic&gt;"</code></span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Push your branch: <code>git push -u origin add-slide/&lt;topic&gt;</code></span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Open a <strong>Pull Request</strong> on GitHub — base: <code>main</code>, compare: your branch. The instructor will merge!</span></label>

</div>

---

<SlideLevel :level="1" />

## Exercise 2 — Slide template

Create `contributions/<topic>.md` with this structure:

```markdown
---
layout: center
transition: fade
---

## Your slide title

Your content here — a quote, a tip, a thought, a tool you love.

No personal information needed. Just something worth sharing.
```

<div class="p-3 border border-yellow-400 rounded bg-yellow-50 mt-4 text-sm">

**Ideas:** a favourite quote about science or code · a Git tip you wish you knew earlier · a tool that changed your workflow · a lesson from a painful bug · a recommendation

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-3 text-sm">

Keep the file in the <code>contributions/</code> folder so it stays tidy. One file per branch = no merge conflicts.

</div>

---

<SlideLevel :level="3" />

## Exercise 3 — Push and pull <span class="ml-2 text-xs font-semibold px-2 py-0.5 rounded bg-gray-100 text-gray-600 border border-gray-300">Optional</span>

**Goal:** sync local work to GitHub and pull remote changes.

<div class="text-sm space-y-1 mt-4">

<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>On your <code>git-cafe-practice</code> repo, push <code>main</code> to GitHub and confirm both files are visible in the browser.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Edit <code>README.md</code> <strong>directly on GitHub</strong> (pencil icon) — add one line. Commit the change on GitHub.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Back in VS Code or RStudio, <strong>pull</strong> the changes. Confirm your local file now includes the line you added remotely.</span></label>

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**Done when:** <code>git status</code> reports "Your branch is up to date with 'origin/main'".

</div>

---

<SlideLevel :level="3" />

## Exercise 4 — Resolve a merge conflict <span class="ml-2 text-xs font-semibold px-2 py-0.5 rounded bg-gray-100 text-gray-600 border border-gray-300">Optional</span>

**Goal:** intentionally create a conflict and resolve it calmly.

<div class="text-sm space-y-1 mt-4">

<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Create a branch <code>experiment</code>. Edit the first line of <code>README.md</code> and commit.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Switch back to <code>main</code>. Edit the <strong>same first line</strong> differently. Commit.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Merge <code>experiment</code> into <code>main</code> — Git will report a conflict.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Open the conflicted file, choose (or combine) the two versions, remove all conflict markers, and save.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Stage the resolved file and complete the merge with a commit.</span></label>

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**Done when:** <code>git status</code> is clean and the log shows a merge commit.

</div>

---

<SlideLevel :level="3" />

## Exercise 5 — Add a `.gitignore` <span class="ml-2 text-xs font-semibold px-2 py-0.5 rounded bg-gray-100 text-gray-600 border border-gray-300">Optional</span>

**Goal:** protect your repo from files that should never be committed.

<div class="text-sm space-y-1 mt-4">

<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Create a file called <code>secret.env</code> with some dummy text. Run <code>git status</code> — Git sees it as untracked.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Create a <code>.gitignore</code> file and add the line <code>*.env</code>.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Run <code>git status</code> again — <code>secret.env</code> should no longer appear.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span>Commit <code>.gitignore</code> with an appropriate message.</span></label>
<label class="flex items-start gap-2 cursor-pointer"><input type="checkbox" class="mt-1 shrink-0" /><span><strong>Bonus:</strong> add patterns for editor junk: <code>.DS_Store</code>, <code>Thumbs.db</code>, <code>.Rhistory</code>, <code>.RData</code>.</span></label>

</div>

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**Done when:** <code>.gitignore</code> is committed and <code>secret.env</code> is invisible to Git.

</div>

---

<SlideLevel :level="1" />

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
git switch -c <name>
git switch <name>
git merge <name>
git branch -d <name>
```

</div>

<div class="p-4 border border-gray-300 rounded bg-gray-50">

**Remote**
```shell
git clone <url>
git push -u origin <branch>
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
layout: takeaways
transition: fade
---

<SlideLevel :level="1" />

<div class="p-4 border border-green-400 rounded bg-green-50">

**Well done!**

You have set up Git, made your first commit, and contributed a slide to a shared repo via a Pull Request — the same workflow used in open source projects every day.

The optional exercises are there whenever you want to dig deeper. Come back to them any time.

</div>
