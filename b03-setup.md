---
layout: block-cover
blockNum: "03"
transition: fade
---

<SlideLevel :level="1" />

# Block 3 — Setup

<div class="p-4 border border-green-400 rounded bg-green-50 mt-4 text-left">

**Learning objective**

Have Git configured with your identity and connected to GitHub/GitLab before writing a single line of code — so every commit is yours and every push just works.

</div>

---

<SlideLevel :level="1" />

## Step 1 — Check that Git is installed

Open a terminal (VS Code: `` Ctrl+` `` / RStudio: **Tools → Terminal**) and run:

```console
$ git --version
git version 2.x.x
```

Not installed? Download from [git-scm.com](https://git-scm.com/downloads) — or on Mac: `xcode-select --install`

<div class="p-3 border border-blue-400 rounded bg-blue-50 mt-4 text-sm">

**VS Code tip:** Git is automatically detected once installed. A source control icon will appear in the left sidebar.

</div>

---

<SlideLevel :level="1" />

## Step 2 — Tell Git who you are

Every commit is stamped with your name and email. Set them once, globally:

```console
$ git config --global user.name "Your Name"
$ git config --global user.email yourname@lumc.nl
```

Set the default branch name to `main` (modern standard):

```console
$ git config --global init.defaultBranch main
```

Verify everything:
```console
$ git config --list
```

<div class="p-3 border border-yellow-400 rounded bg-yellow-50 mt-3 text-sm">

Use the same email as your GitHub/GitLab account — this is how the platform links commits to your profile.

</div>

---

<SlideLevel :level="1" />

## Step 3 — Connect to GitHub / GitLab

Two ways to authenticate — choose one:

<div class="grid grid-cols-2 gap-4 mt-3">

<div class="p-4 border border-blue-400 rounded bg-blue-50 text-sm">

**SSH key** (recommended)

Works for both GitHub and GitLab. Set it up once, never type a password again.

Clone URLs look like:
```
git@github.com:user/repo.git
```

</div>

<div class="p-4 border border-green-400 rounded bg-green-50 text-sm">

**HTTPS** (simpler for beginners)

VS Code and RStudio can handle this through a built-in browser login flow — no terminal needed.

Clone URLs look like:
```
https://github.com/user/repo.git
```

</div>

</div>

---

<SlideLevel :level="2" />

## Setting up an SSH key — step by step

<div class="grid grid-cols-2 gap-4 mt-3 text-sm">

<div>

**1. Generate a key pair:**
```console
$ ssh-keygen -t ed25519 -C "yourname@lumc.nl"
# Press Enter for default location
# Set a passphrase (optional)
```

**2. Copy your public key:**
```console
$ cat ~/.ssh/id_ed25519.pub
# Select and copy the output
```

</div>

<div>

**3. Add to GitHub:**
Settings → SSH and GPG keys → **New SSH key** → paste → Save

**4. Add to GitLab** (if needed):
Preferences → SSH Keys → paste → Save

**5. Test:**
```console
$ ssh -T git@github.com
# Hi username! You've successfully
# authenticated.
```

</div>

</div>

---

<SlideLevel :level="2" />

## Authentication in VS Code and RStudio

<div class="grid grid-cols-2 gap-4 mt-4">

<div class="p-4 border border-purple-400 rounded bg-purple-50 text-sm">

**VS Code**

Uses a built-in GitHub sign-in flow.

1. Open Command Palette (`Ctrl+Shift+P`)
2. Search: `GitHub: Sign In`
3. A browser window opens — log in once
4. Done — VS Code handles auth automatically

Use **HTTPS** clone URLs.

</div>

<div class="p-4 border border-orange-400 rounded bg-orange-50 text-sm">

**RStudio**

Uses HTTPS via the `usethis` package:

```r
install.packages("usethis")
usethis::create_github_token()
# Follow the prompts — a browser opens
gitcreds::gitcreds_set()
# Paste the token when asked
```

Use **HTTPS** clone URLs.

</div>

</div>

---
layout: takeaways
transition: fade
---

<SlideLevel :level="1" />

<div class="p-4 border border-green-400 rounded bg-green-50">

**Key takeaways — Block 3**

- Do this once per machine — not per project.
- SSH key = the gold standard: works everywhere, no passwords.
- VS Code and RStudio users: the HTTPS browser flow is just as good for day-to-day work.
- Next: we open VS Code, clone a repo, and make our first commit.

</div>
