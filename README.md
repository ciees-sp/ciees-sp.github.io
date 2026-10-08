# CIEES Special Projects — Client Deliverables Site

A lightweight GitHub Pages site for serving interactive HTML prototypes and proposals to clients.

---

## One-Time Setup (10 minutes)

### 1. Create a GitHub Account
- Go to [github.com](https://github.com) and sign up
- Suggested username: `ciees-sp` (your site URL will be `ciees-sp.github.io`)

### 2. Create a New Repository
- Click the **+** in the top-right corner → **New repository**
- Repository name: `ciees-sp.github.io` (must match your username exactly — this tells GitHub to serve it as a website)
- Set to **Public**
- Do **not** initialize with a README (you already have one)
- Click **Create repository**

### 3. Upload These Files
- On your new repo page, click **"uploading an existing file"** (in the quick setup section)
- Drag the entire contents of this folder into the upload area:
  - `index.html`
  - `template.html`
  - `README.md`
  - `assets/` folder (with logos)
  - `projects/` folder (with sample)
- Click **Commit changes**

### 4. Enable GitHub Pages
- Go to **Settings** → **Pages** (left sidebar)
- Under "Source", select **Deploy from a branch**
- Branch: **main**, folder: **/ (root)**
- Click **Save**
- Wait 1–2 minutes. Your site is live at `https://ciees-sp.github.io`

---

## Adding a New Prototype

### Step 1: Create a project folder
In `projects/`, create a folder for the client or project:
```
projects/
  dbhds-sbhc/
  vcsi-report/
  recovery-schools/
```

### Step 2: Add your HTML file
Drop your Cowork-built HTML file into that folder. You can either:

**Option A — Standalone file (simplest)**
Just put your HTML file in the folder as-is. Link directly to it from the landing page.

**Option B — Branded wrapper**
Copy `template.html` into your project folder, rename it, and paste your prototype content into the marked area. This adds the SP header bar and "All Deliverables" back link.

### Step 3: Update the landing page
Open `index.html` and add a new entry to the project list. Copy an existing `<a class="project-item">` block and update:
- `href` — path to your HTML file (e.g., `projects/dbhds-sbhc/dashboard-v2.html`)
- Project name
- Meta text (client name, date)
- Badge text (Prototype, Proposal, Report, Draft)

### Step 4: Upload to GitHub
- Go to your repo on github.com
- Click **Add file** → **Upload files**
- Drag in the new/changed files
- Commit. The site updates within a minute or two.

---

## Folder Structure

```
ciees-sp.github.io/
├── index.html              ← Landing page (client deliverable list)
├── template.html           ← Wrapper template for branded prototypes
├── README.md               ← This file
├── assets/
│   ├── logo-horizontal.png
│   ├── logo-horizontal-white.png
│   └── logo-stacked.png
└── projects/
    └── sample/
        └── prototype-demo.html   ← Demo page (safe to delete later)
```

---

## Tips

- **URL to share with clients**: `https://ciees-sp.github.io/projects/folder-name/file.html`
- **The repo is public** but unlisted — no one finds it unless you share the link
- **No passwords needed** — clients click the link and see the prototype immediately
- **Update workflow**: edit locally → drag files to GitHub → auto-deploys in ~60 seconds
- **With Cowork**: I can help you push files directly to GitHub once you give me repo access via a personal access token — but the drag-and-drop upload works fine for low volume
