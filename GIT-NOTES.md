# Portfolio Workflow Notes (Git + VS Code)

## One-time setup (already done)
```bash
git --version
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global --list
```

## Where things are
- Projects folder: `C:\Users\ejajr\projects\git_repositories\portfolio`
- Check the repo is linked to GitHub: `git remote -v`

## Every session

### 1. Pull the latest changes first
```bash
git pull
```
Why: GitHub may have changes your computer doesn't (edits made on github.com,
another computer, a bot, or a contributor). Starting from the latest version
avoids rejected pushes and merge conflicts.

### 2. Preview live with Live Server
- Install the **Live Server** extension (Ritwick Dey): `Ctrl+Shift+X`
- Right-click `index.html` > **Open with Live Server**, or click **Go Live**
- Page refreshes every time you save (`Ctrl+S`)
- Stop it: click **Port: 5500** in the status bar

### 3. Edit and save
Change your files in VS Code and save them.

### 4. Commit and push

**With VS Code buttons:**
1. Source Control icon (`Ctrl+Shift+G`)
2. Click **+** to stage changes
3. Type a short message, e.g. `Update about section`
4. Click **Commit**
5. Click **Sync Changes** (or **Push**)

**With the terminal:**
```bash
git add .
git commit -m "Update about section"
git push
```

### 5. Check it's live
Refresh the repo on GitHub. If you use GitHub Pages, Netlify, or Vercel, the
site updates automatically within a minute or two.

## Routine summary
1. `git pull`
2. Open with Live Server and edit
3. Save and check the preview
4. Commit and push

## Common problems
- **Authentication failed:** sign in again when prompted, or use a GitHub
  Personal Access Token instead of a password.
- **Rejected / fetch first:** run `git pull`, then push again.
- **Merge conflict:** VS Code shows "Accept Current / Incoming / Both". Pick
  what you want, save, then commit.
- **fatal: not a git repository:** you're in the wrong folder, or the folder
  hasn't been set up with `git init`.
- **mkdir says folder already exists:** harmless, just `cd` into it.