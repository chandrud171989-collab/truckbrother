# Deploy Guide — GitHub Pages (Free)

Your live URL will be:
**`https://<your-username>.github.io/haulx-booking`**

No credit card. No server. Completely free forever.

---

## Step 1 — Create a GitHub account (if you don't have one)

Go to https://github.com and sign up. Free plan is all you need.

---

## Step 2 — Create a new repository

1. Click the **+** icon (top-right) → **New repository**
2. Repository name: `haulx-booking`
3. Set to **Public** ← required for free GitHub Pages
4. Do NOT tick "Add a README" (you already have one)
5. Click **Create repository**

---

## Step 3 — Upload files (no terminal needed)

### Option A — Drag & Drop (easiest)
1. On your new empty repo page, click **uploading an existing file**
2. Drag and drop ALL files from the `haulx-booking/` folder:
   - `index.html`
   - `README.md`
   - `DEPLOY.md`
3. For the `.github/workflows/deploy.yml` file:
   - Click **create new file** instead
   - Type the path: `.github/workflows/deploy.yml`
   - Paste the contents of that file
4. Click **Commit changes** → **Commit directly to main**

### Option B — Git CLI (faster for future updates)
```bash
# 1. Download or clone your new empty repo
git clone https://github.com/<your-username>/haulx-booking.git

# 2. Copy your project files into it
cp -r /path/to/haulx-booking/* haulx-booking/
cp -r /path/to/haulx-booking/.github haulx-booking/

# 3. Push
cd haulx-booking
git add .
git commit -m "Initial deploy: HaulX booking page"
git push origin main
```

---

## Step 4 — Enable GitHub Pages

1. Go to your repo → **Settings** tab
2. Left sidebar → **Pages**
3. Under **Source**, select **GitHub Actions**
4. Click **Save**

That's it. GitHub Actions will now auto-deploy on every push.

---

## Step 5 — Watch it deploy

1. Click the **Actions** tab in your repo
2. You'll see a workflow run called **Deploy to GitHub Pages**
3. It takes about 60–90 seconds
4. When it shows a green ✅, your site is live

---

## Step 6 — Visit your site

Open: `https://<your-username>.github.io/haulx-booking`

Share this URL with anyone. It works on mobile and desktop.

---

## How to update the site later

Just push any change to the `main` branch:

```bash
# Edit index.html, then:
git add index.html
git commit -m "Update vehicle prices"
git push
```

GitHub Actions picks it up automatically. Live in ~60 seconds.

---

## Custom domain (optional, still free)

If you own a domain (e.g. `haulx.in`):

1. Go to repo → **Settings → Pages → Custom domain**
2. Enter your domain (e.g. `haulx.in`)
3. At your domain registrar, add a CNAME record:
   - **Name:** `www`
   - **Value:** `<your-username>.github.io`
4. GitHub handles the free SSL certificate automatically.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| Actions tab shows red ✗ | Go to Settings → Pages → Source = GitHub Actions |
| Site shows 404 | Make sure the file is named exactly `index.html` (not `Index.html`) |
| Old version showing | Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac) |
| Workflow not triggering | Check you pushed to `main`, not `master` |