# Start here: building the EELAM Solutions website with Claude Code

A beginner guide for Roy. Follow the parts in order. Do not skip ahead.
Each part ends with a check, so you know it worked before you continue.

---

## Part 0 — Words you will see

| Word | Simple meaning |
|---|---|
| HTML | The content of a web page: headings, text, images, buttons. |
| CSS | The look of the page: colours, fonts, spacing. |
| JavaScript | Small programs that make the page react (for example, checking the form). |
| Folder / project | The `eelam-solutions` folder on your computer. Everything for the site lives here. |
| Git | A tool that saves "snapshots" of your project so you can go back if something breaks. |
| Commit | One saved snapshot, with a short note about what changed. |
| GitHub | A website that stores your project online. |
| Repository (repo) | Your project's home on GitHub. |
| Push | Sending your commits from your computer to GitHub. |
| GitHub Pages | A free GitHub service that turns your repo into a live website. |
| Claude Code | Claude working directly inside your project folder: it can read, create and edit files and run commands, and it asks you before doing important things. |
| CLAUDE.md | A file in your project that tells Claude Code the background. It reads it every session, so you never need to explain the project again. |

---

## Part 1 — Install the tools (about 20 minutes, one time only)

### Step 1.1 — Install Git
1. Go to **git-scm.com/downloads/win** and download Git for Windows.
2. Run the installer. Click **Next** on every screen (the default options are fine).
3. Check: open the Start menu, type **PowerShell**, open it, type `git --version` and press Enter. You should see something like `git version 2.x`. Close PowerShell.

Why: Claude Code on Windows needs Git to work, and Git is how your site gets to GitHub.

### Step 1.2 — Create a GitHub account
1. Go to **github.com** and sign up (free).
2. Choose your username carefully. Your free website address will be `yourusername.github.io/eelam-solutions`.
3. Turn on two-factor authentication when GitHub asks (it protects your account).

### Step 1.3 — Install the Claude desktop app
1. Go to **claude.com/download** and download the Windows version.
2. Run the installer, then open **Claude** from the Start menu and sign in with the same account you use here.
3. Click **Code** at the top of the app.
   - If it asks you to upgrade, your plan does not include Claude Code. A paid plan is needed.
   - If Claude was already installed, first use **Help > Check for Updates** and restart.

Check: you can see the Code tab, and it asks you to choose a project folder.

---

## Part 2 — Set up the project folder (10 minutes)

### Step 2.1 — Put the files in place
1. Download the `eelam-solutions.zip` file from our chat.
2. Right-click it and choose **Extract All**. Extract it to a simple place, for example `C:\Users\Roy\Projects\`.
   - Avoid OneDrive folders, network drives and the Desktop if possible (they can cause sync problems).
3. Open the folder. You should see:

```
eelam-solutions/
├── CLAUDE.md        (background for Claude Code)
├── START-HERE.md    (this guide)
├── en/index.html    (English page)
├── ta/index.html    (Tamil page)
└── assets/img/      (put your images here)
```

Check: double-click `en/index.html`. The English page opens in your browser. Click **தமிழ்** — the Tamil page opens.

### Step 2.2 — Open the folder in Claude Code
1. In the Claude app, open the **Code** tab.
2. Choose **Local** (runs on your computer) and select the `eelam-solutions` folder.
3. Type your first message:

> Read CLAUDE.md and START-HERE.md. Then tell me in simple words what this project is, what is already built, and what we should do first.

Check: Claude answers with a summary that matches our plan (three $1,000 packages, three languages, A+C design). If it does, it has the full background.

---

## Part 3 — Save your first snapshot with Git (10 minutes)

Before changing anything, save the starting point. Then you can always go back.

Type in Claude Code:

> Set up Git for this project. Explain each command before you run it. Create a .gitignore file that ignores Windows system files. Then make the first commit with the message "Starting files".

Claude will ask permission before running commands. Read what it says, then approve.

Check: ask Claude **"Show me the Git history."** You see one commit called "Starting files".

---

## Part 4 — Build the missing pieces (one session each)

Do one item per session. After each one, open the page in your browser and look at it yourself. Then ask Claude to commit it.

### 4.1 — The French page (most important: French must be the default)
> Build the French page as index.html in the root folder, based on en/index.html. Use natural Québec French, not a word-for-word translation. Fix the image paths and language links for the root folder. Explain the differences between the root page and the en/ page.

Check: open `index.html`, click EN and தமிழ், and come back to FR. All three switch correctly.

Tip: ask a French-speaking friend or colleague to read the page once. Small language errors look unprofessional to Québec clients.

### 4.2 — Your images
1. Resize and name your images exactly as in the table in CLAUDE.md.
2. Copy them into `assets/img/`.
3. Ask:
> I added images to assets/img. Check that every filename matches the list in CLAUDE.md, tell me which are missing or too large, and help me compress any file over 300 KB.

Check: refresh the pages. The dashed placeholder boxes are replaced by your photos.

### 4.3 — Real content
> Help me replace all placeholders: email, phone, social links and portfolio project names. Ask me for each value one at a time, and update all three languages.

Also decide your **print quantities** (check prices with your printer first), then:
> Update the Marketing materials package with these print quantities: [your numbers]. Update all three languages.

### 4.4 — The quote form (Apps Script)
You already know Apps Script, so this part connects to what you know.
> Guide me step by step to create a Google Apps Script web app that receives the quote form, saves each request to a Google Sheet, and emails me. Give me the Apps Script code to paste, explain how to deploy it, then help me put the URL in FORM_ENDPOINT on all three pages.

Check: send a test request from the page. A new row appears in your sheet and you get an email.

### 4.5 — Privacy policy
> Create privacy.html in French, with English and Tamil versions, suitable for a small Québec business under Law 25. Keep it short and plain. Mark any part I must confirm myself.

Note: a lawyer review is a good idea before launch. Claude can draft it, but it is not legal advice.

---

## Part 5 — Publish on GitHub Pages (20 minutes)

### Step 5.1 — Create the repository
1. On github.com, click **+** (top right) > **New repository**.
2. Name: `eelam-solutions`. Choose **Public** (free GitHub Pages needs a public repo).
3. Do **not** add a README or other files. Click **Create repository**.
4. Copy the repository address (it looks like `https://github.com/yourusername/eelam-solutions.git`).

### Step 5.2 — Send your project to GitHub
In Claude Code:
> Connect this project to my GitHub repository [paste the address] and push it. Explain each step. If a login window appears, tell me what to do.

The first time, a browser window will ask you to sign in to GitHub. Sign in and approve. This is normal.

Check: refresh your repository page on github.com. You see your files.

### Step 5.3 — Turn on GitHub Pages
1. In your repository, go to **Settings > Pages**.
2. Under **Source**, choose **Deploy from a branch**.
3. Branch: **main**, folder: **/ (root)**. Click **Save**.
4. Wait 1–3 minutes, then refresh. GitHub shows your site address.

Check: open the address. Your French page loads. Test the language links, the form and the page on your phone.

### Step 5.4 — Custom domain (later)
When you buy a domain (for example `eelamsolutions.ca`), ask Claude Code:
> Help me connect my domain [name] to GitHub Pages. Explain the DNS settings I need to enter at my domain provider.

---

## Part 6 — Your routine for every future change

1. Open the project in the Code tab.
2. Describe **one** change in plain words.
3. Read Claude's explanation, approve, then check the page in your browser.
4. If you like it: **"Commit this with a clear message and push it."**
5. If you don't: **"Undo that change."** (Git makes this safe.)
6. The live site updates about one minute after the push.

---

## Part 7 — Prompts that help you learn

Use these any time:

- "Explain this section of the code line by line, like I'm a beginner."
- "Why did you choose this way instead of another way?"
- "Let me try this change myself first. Tell me which file and line to edit, then check my work."
- "Give me a small exercise to practise what we just did."
- "Summarize what I learned today in five simple points."

A good habit: once per session, make one small change **yourself** (for example, change a colour or a sentence) and ask Claude to review it. That is how the knowledge stays with you.

---

## Part 8 — If something goes wrong

| Problem | What to do |
|---|---|
| "git is not recognized" | Install Git (Step 1.1), then close and reopen the Claude app. |
| Code tab asks to upgrade | Your plan does not include Claude Code. |
| Page looks broken after a change | Ask: "The page looks broken after the last change. Find the problem and fix it, and explain what went wrong." |
| An image doesn't appear | Check the filename: exact spelling, lowercase, correct extension (.jpg vs .png). |
| Language link shows an error | The target page may not exist yet (for example, French before step 4.1). |
| Live site did not update | Wait 2 minutes, then refresh with Ctrl + F5. Ask Claude: "Did the last push succeed?" |
| You want to go back to yesterday's version | Ask: "Show me the Git history and help me go back to [commit]." |
