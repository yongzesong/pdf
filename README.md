# pdf — paper PDFs for yongzesong.com

Static repository holding the paper PDFs linked from https://yongzesong.com/methods.html.
Published as a GitHub *project* site; because the user site `yongzesong.github.io` has the
custom domain `yongzesong.com`, this repo is served at **https://yongzesong.com/pdf/** — the
same URLs the site has always used (`pdf/<ABBR>-<author><year>.pdf`), so no site links change.

`index.html` is a plain listing (noindex). `.nojekyll` keeps GitHub Pages from running Jekyll.

## DEPLOY (manual, in this order)

1. Create an empty public repository `yongzesong/pdf` on GitHub (no README/licence).
2. From this folder:
   ```
   git add -A
   git commit -m "Paper PDFs served at yongzesong.com/pdf/"
   git branch -M main
   git remote add origin https://github.com/yongzesong/pdf.git
   git push -u origin main
   ```
3. Repository → Settings → Pages → Source "Deploy from a branch", branch `main`, folder `/ (root)`. Save; wait for the build (1–2 min).
4. Verify https://yongzesong.com/pdf/ and one file, e.g. https://yongzesong.com/pdf/GOS-song2022.pdf.
5. ONLY THEN delete the `pdf/` folder from the main site repo and push it — while the main site still contains `pdf/`, it shadows this project site.

## Adding a paper

Drop the PDF here, add a row to `index.html`, commit and push. Link it from the main site as `pdf/<file>.pdf` (root pages) or `../pdf/<file>.pdf` (pages in subfolders) exactly as before.
