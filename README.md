# Ryo Kanno — Personal Academic Website

Static HTML/CSS site hosted on GitHub Pages.
Live: https://cansathandler.github.io/PersonalWebsite/ (and https://ryokanno.net once DNS is set)

## Files

```
index.html          Home (hero, expertise, recent news)
projects.html       Project cards with embedded MP4
publications.html   Papers, patents, awards
about.html          Education & work experience
style.css           All styling (shared)
*.mp4 / *.png / ...  Media referenced by the pages
```

Only media actually referenced by the HTML is kept in this repo. Unused
originals (full-length source videos) stay on the local machine.

## Updating the site

```bash
git add .
git commit -m "Update projects page"
git push
```

GitHub Pages redeploys automatically, usually within a minute.

## Custom domain (ryokanno.net)

1. Repo → **Settings → Pages → Custom domain** → enter `ryokanno.net` → Save.
   (This creates a `CNAME` file in the repo — do not delete it.)
2. At the registrar for ryokanno.net, set:

   ```
   A     @     185.199.108.153
   A     @     185.199.109.153
   A     @     185.199.110.153
   A     @     185.199.111.153
   CNAME www   cansathandler.github.io
   ```
3. After DNS propagates, tick **Enforce HTTPS**.

## TODO

- [ ] Add `CV_Ryo_Kanno_General.pdf` to the repo root — the nav "CV ↗" link
      currently 404s because the file is missing.
- [ ] Optional: compress the MP4s further (`ffmpeg -crf 28`) to speed up loading.
