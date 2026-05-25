# duygucakmak.com (working title)

Static personal site — single page, four sections (Hero, About, Talks & Papers, Contact).

## Files

- `index.html` — content
- `styles.css` — styling
- `README.md` — this file

No build step. Open `index.html` in a browser to preview locally.

## Deploy to GitHub Pages (no custom domain)

1. Create a new GitHub repo. Two options:
   - **User site:** name it `<your-username>.github.io` — it will be served at `https://<your-username>.github.io/`.
   - **Project site:** name it anything (e.g. `website`) — it will be served at `https://<your-username>.github.io/website/`.
2. From this folder:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin git@github.com:<your-username>/<repo>.git
   git push -u origin main
   ```
3. In the repo on GitHub: **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, Branch to **main**, folder to **/ (root)**. Save.
4. Wait ~1 minute, then visit the URL shown on the Pages settings page.

## Add a custom domain later

When you're ready to move to e.g. `duygucakmak.com`:

1. Buy the domain (Namecheap, Cloudflare, etc.).
2. Add a `CNAME` file to the repo root containing just the domain (no `https://`, no trailing slash):
   ```
   duygucakmak.com
   ```
3. At your DNS provider, add these records pointing to GitHub Pages:
   - **A records** for the apex (`@`) pointing to:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - **CNAME record** for `www` pointing to `<your-username>.github.io`.
4. In **Settings → Pages**, enter the custom domain and enable **Enforce HTTPS** once GitHub has issued the certificate (can take a few minutes to a few hours).

## Things still to fill in

These are placeholders in `index.html` — search for them and replace:

- `hello@example.com` — your public email
- `https://www.linkedin.com/in/your-handle/` — your LinkedIn URL
- `https://bsky.app/profile/your-handle.bsky.social` — your Bluesky handle

## Content notes

- Awards sit at the bottom of **Talks & Papers**, inside the Editorial & service area, per the content doc.
- Mindful Cloud Games is intentionally not referenced while you remain at CA.
- Several talks still need links — see `site-content.md` open questions list.
