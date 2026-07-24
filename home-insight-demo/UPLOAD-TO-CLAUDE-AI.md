# Moving the HomeInsight website into the `claude-ai` repo

The website is two files — `index.html` (the whole app, including the
compare-two-homes view) and `README.md`. Here's how to get them into your new
repo and finish the move.

## Step 1 — Upload the files to `claude-ai`

1. Open the repo: **https://github.com/saeidagheli88/claude-ai**
2. On the empty-repo page, click **“uploading an existing file”**
   (or **Add file → Upload files**).
3. Drag in the two files: **`index.html`** and **`README.md`**.
   - To keep them in a folder, type `home-insight-demo/` in front of the
     filename. Or just drop `index.html` at the root to keep it simple.
4. Click **Commit changes**.

## Step 2 — View the site

Open `index.html` in any browser (download it and double-click, or use GitHub
Pages later). No build step, no dependencies.

## Step 3 — Finish the move (Claude does this)

Once the files are in `claude-ai`, reply **“uploaded”** and I'll:

- delete `home-insight-demo/` from the **Jamf** repo, and
- close **PR #1** with a note pointing to the website's new home.

That completes the move — the website lives only in `claude-ai`.

---

### Why you had to upload manually

This session's GitHub access is locked to `saeidagheli88/jamf` only. Extending
it to the new `claude-ai` repo needs an "add repository" approval that couldn't
be completed from the assistant's side, so the upload had to be done by hand.
The Jamf-side cleanup (Step 3) works fine because that repo is in scope.
