# servecreative.github.io

Root GitHub Pages site for **SERVEcreative**. Serves AdMob `app-ads.txt` at:

`https://servecreative.github.io/app-ads.txt`

(Project repos such as [Dhyan](https://github.com/SERVEcreative/Dhyan) stay under `/Dhyan/` — that path cannot satisfy AdMob root-domain verification.)

## One-time GitHub setup

1. Create a **public** repo named exactly `SERVEcreative.github.io` under the SERVEcreative org (or your user account).
2. Push this folder to `main`:

   ```bash
   cd servecreative.github.io
   git init
   git add app-ads.txt index.html README.md
   git commit -m "Add root app-ads.txt for AdMob verification"
   git branch -M main
   git remote add origin https://github.com/SERVEcreative/SERVEcreative.github.io.git
   git push -u origin main
   ```

3. Enable Pages: **Settings → Pages → Build and deployment → Deploy from branch → `main` → `/ (root)`**.
4. After 1–2 minutes, open `https://servecreative.github.io/app-ads.txt` and confirm the publisher line is visible.

## Play Console & AdMob

- Set **Developer website** (Play Console → Store presence) to: `https://servecreative.github.io`
- In AdMob, use the same domain; crawlers expect `app-ads.txt` at the site root, not under `/Dhyan/`.
- Re-check verification in AdMob after the URL returns `200` with the correct `pub-6827778613476055` line.

## Updating app-ads.txt

Edit `app-ads.txt`, commit, and push to `main`. No app release required.
