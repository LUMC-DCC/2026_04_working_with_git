---
layout: center
transition: fade
---

# Block 1 — Why Version Control?

<div class="p-4 border border-green-400 rounded bg-green-50 mt-4 text-left">

**Learning objective**

Understand the problem version control solves and why it is worth adding to your workflow — even if you work alone.

</div>

---

## Does this look familiar?

<div class="p-4 border border-gray-300 rounded bg-gray-50 font-mono text-sm mt-4">

```
analysis-2023.zip
analysis-2024-February.zip
analysis-2024-August.zip
analysis-2024-09-19-working.zip
analysis-2024-09-21.zip
analysis-2024-09-21-test.zip
analysis-2024-09-21-myversion.zip
analysis-2024-09-21-newfeature.zip
... (100 more files)
```

</div>

<div class="p-4 border border-red-300 rounded bg-red-50 mt-4 text-sm">

**The problem:** Which one is the final version? What changed between them? Can you merge your colleague's changes with yours?

</div>

---

## Questions version control answers

- "It broke... hopefully I have a working version somewhere?"
- "Can you please send me the latest version?"
- "Which version did the paper use — can I reproduce the results?"
- "Found a bug! Since when was it there?"
- "My laptop is gone. Is my thesis gone too?"
- "We both edited the same file — whose changes do we keep?"

<div class="mt-4 text-sm text-gray-500">

These are not hypothetical. Every researcher hits them.

</div>

---

## What version control gives you

<div class="grid grid-cols-3 gap-4 mt-4">

<div class="p-3 border border-blue-400 rounded bg-blue-50 text-sm">

**Roll-back**

Always go back to any previous state and compare exactly what changed.

</div>

<div class="p-3 border border-purple-400 rounded bg-purple-50 text-sm">

**Branching**

Try an idea in isolation. Keep a stable version while experimenting. Discard safely if it doesn't work.

</div>

<div class="p-3 border border-green-400 rounded bg-green-50 text-sm">

**Collaboration**

Multiple people work in parallel without overwriting each other. Review, discuss, merge.

</div>

</div>

---

## Git tracks your history on GitHub

<img src="/img/git-log-github.png" class="border rounded mt-2 max-h-64 mx-auto" />

<p class="text-center text-sm text-gray-500 mt-2">Every change recorded — who, what, when, and why.</p>

---

## What you can track with Git

Not just code — anything text-based benefits:

- **Scripts** (R, Python, bash, …)
- **Analysis pipelines**
- **Manuscripts** (Quarto, LaTeX, Markdown)
- **Configuration files**
- **Data** (small, plain-text tables work well)

<div class="p-3 border border-yellow-400 rounded bg-yellow-50 mt-4 text-sm">

Git is not ideal for large binary files (images, raw data, `.docx`). For those, consider keeping them outside the repo or using tools like DVC.

</div>

---

<div class="p-4 border border-green-400 rounded bg-green-50">

**Key takeaways — Block 1**

- Version control replaces the zip-file habit with an automatic, searchable history.
- Git is the industry standard: easy to set up, works offline, backed by GitHub & GitLab.
- Any version control is better than none — and the basics take 10 minutes to learn.

</div>
