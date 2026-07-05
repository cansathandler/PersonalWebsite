# Ryo Kanno — Personal Academic Website

Static HTML/CSS website for GitHub Pages

## Files

```
index.html        ← Home page
about.html        ← Education & work experience
publications.html ← Papers and awards
style.css         ← All styling (shared across pages)
README.md         ← This file
```

## How to publish on GitHub Pages

### Step 1 — Create a GitHub account
If you don't have one: https://github.com/signup

### Step 2 — Create a new repository
1. Go to https://github.com/new
2. Name it exactly: `yourusername.github.io`
   (replace `yourusername` with your actual GitHub username)
3. Set it to **Public**
4. Click **Create repository**

### Step 3 — Upload the files
**Option A (easiest — no coding needed):**
1. In your new repository, click **Add file → Upload files**
2. Drag all files (index.html, about.html, publications.html, style.css) into the browser
3. Click **Commit changes**

**Option B (using Git):**
```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

### Step 4 — Enable GitHub Pages
1. Go to your repository → **Settings** → **Pages**
2. Under "Source", select **main** branch, folder **/ (root)**
3. Click **Save**
4. Your site will be live at: `https://yourusername.github.io`

(It may take 1–2 minutes to go live after the first deploy.)

---

## How to add your photo

1. Create a folder called `images/` in the repository
2. Upload your headshot as `images/headshot.jpg`
3. In `index.html`, find the `photo-placeholder` div and replace it with:
   ```html
   <img src="images/headshot.jpg" alt="Ryo Kanno" />
   ```

## How to use your own domain (e.g. ryokanno.net)

1. In your repo → **Settings → Pages → Custom domain**, type `ryokanno.net`
2. In your domain registrar (wherever you bought ryokanno.net), add these DNS records:
   ```
   A    @    185.199.108.153
   A    @    185.199.109.153
   A    @    185.199.110.153
   A    @    185.199.111.153
   CNAME www  yourusername.github.io
   ```
3. Wait up to 24 hours for DNS to propagate, then check **Enforce HTTPS** in the Pages settings.

## Updating your CV

Replace `CV_Ryo_Kanno_General.pdf` in the repository with your latest PDF.
The nav links will automatically point to the new version.

## Adding more publications

Copy a `<div class="pub-entry">` block in `publications.html` and fill in your details.
