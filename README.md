# Vincent Bastille – Custom Remix Landing (Static)

Ultra-simple static landing page in **English**, SEO oriented, dedicated to the custom remix service (house / tech house / drum & bass).

## Structure

- `index.html` – full landing page (hero, portfolio, how it works, FAQ, links).
- `assets/style.css` – design (dark club gradient, colorful but clean).

Everything works as a static site: **no backend**, no Python, no env vars.

---

## 1. Local quick preview (optional)

You can open `index.html` directly in your browser, or use a tiny HTTP server:

```bash
cd remix_static
python3 -m http.server 8000
```

Then go to http://localhost:8000

---

## 2. GitHub – create a repo and push

From inside the `remix_static` directory:

```bash
git init
git add .
git commit -m "Initial commit – remix landing static"

# Replace YOUR_GITHUB_USERNAME and REPO_NAME with your own
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/remix-landing-static.git
git branch -M main
git push -u origin main
```

Once this is done, your static site is ready to be deployed from GitHub.

---

## 3. Deploy as a static site on Render

1. Go to Render, click **New +** → **Static Site**.
2. Connect your GitHub account if not already done.
3. Select the repo you just pushed (`remix-landing-static`).
4. Settings:
   - **Root directory**: `/` (not a subfolder)
   - **Build command**: `None` or leave empty
   - **Publish directory**: `/`
5. Click **Create Static Site**.

Render will build and deploy your static landing.  
You’ll get a URL such as `https://remix-landing-static.onrender.com`.

Later you can point your domain `vincentbastille.online/remix` or a subdomain to it via DNS.

---

## 4. Stripe payment link (optional, later)

Right now, the big CTA button uses a placeholder:

```html
https://buy.stripe.com/your_payment_link_here
```

Once you create a Stripe **Payment Link** for your 299€ remix offer, simply edit `index.html` and replace all occurrences of `your_payment_link_here` with the real URL.

No code change, no env vars – just a copy/paste.

---

This repo is intentionally minimal so you don’t need to fight with Python, venv or frameworks just to have a clean, pro landing online.
