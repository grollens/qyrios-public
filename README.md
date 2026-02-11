# qyrios-chat

Public GitHub repo for the Content Interview chat page (GitHub Pages).  
Source of truth for the HTML lives in `qyrios-backbone`; this repo is the deployed copy.

## One-time setup (create repo and enable Pages)

1. **Create the repo on GitHub**
   - Go to https://github.com/new
   - Repository name: `qyrios-chat`
   - Visibility: **Public**
   - Do **not** add a README, .gitignore, or license (we're pushing existing content)
   - Click **Create repository**

2. **Push this folder**
   ```bash
   cd /path/to/qyrios-backbone/qyrios-chat
   git init
   git add interview-chat.html README.md
   git commit -m "Add interview chat page for GitHub Pages"
   git branch -M main
   git remote add origin https://github.com/grollens/qyrios-chat.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - In the repo: **Settings** → **Pages**
   - Under "Build and deployment": Source = **Deploy from a branch**
   - Branch: **main**, Folder: **/ (root)**
   - Save

4. **Verify**
   - After 1–2 minutes, open: https://grollens.github.io/qyrios-chat/interview-chat.html?recordId=test  
   - You should see the chat page (or the "Saknar innehålls-ID" message if recordId is missing).

## Updating the page

When you change the HTML in `qyrios-backbone` (in `systems/content-engine/workflows/insight-gathering/interview-chat.html` or `docs/interview-chat.html`), copy the updated file here and push:

```bash
cp /path/to/qyrios-backbone/docs/interview-chat.html .
git add interview-chat.html
git commit -m "Update interview chat page"
git push
```
