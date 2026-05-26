# Deploying Cubero Consulting to GitHub Pages (Free)

This guide walks you through getting your site live at a custom domain using GitHub Pages — completely free.

---

## What You'll Need

- A free GitHub account (github.com)
- Your custom domain: `cuberoconsulting.com`
- Access to your domain's DNS settings (wherever you registered the domain)

**Estimated time: 20–30 minutes**

---

## Step 1 — Create a GitHub Account (if you don't have one)

1. Go to [github.com/join](https://github.com/join)
2. Sign up with your email (cuberovera@gmail.com works great)
3. Choose the **Free** plan

---

## Step 2 — Create a New Repository

1. Once logged in, click the **+** icon (top right) → **New repository**
2. Name it exactly: `cuberoconsulting.com`
   *(or use your GitHub username: `yourusername.github.io` for the cleanest URL)*
3. Set it to **Public**
4. Check **Add a README file**
5. Click **Create repository**

---

## Step 3 — Upload Your Website Files

1. On your new repository page, click **Add file** → **Upload files**
2. Upload ALL the files in this folder:
   - `index.html`
   - `resume.html`
   - `spotlight.html`
   - The entire `css/` folder (with `styles.css` inside)
3. Scroll down, write a commit message like "Initial website upload"
4. Click **Commit changes**

---

## Step 4 — Enable GitHub Pages

1. Go to your repository → **Settings** tab
2. In the left sidebar, click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Set branch to **main**, folder to **/ (root)**
5. Click **Save**

GitHub will show you a URL like `https://yourusername.github.io/cuberoconsulting.com/`
Your site is now live! Now let's connect your real domain.

---

## Step 5 — Connect Your Custom Domain (cuberoconsulting.com)

### In GitHub Pages Settings:
1. Still in **Settings → Pages**, find the **Custom domain** field
2. Type: `cuberoconsulting.com`
3. Click **Save**
4. Check **Enforce HTTPS** (this makes it secure — free SSL!)

### In Your Domain Registrar's DNS Settings:
Log in to wherever you bought `cuberoconsulting.com` (likely Squarespace, GoDaddy, Namecheap, etc.) and add these DNS records:

**A Records** (point the root domain to GitHub):
```
Type: A    Name: @    Value: 185.199.108.153
Type: A    Name: @    Value: 185.199.109.153
Type: A    Name: @    Value: 185.199.110.153
Type: A    Name: @    Value: 185.199.111.153
```

**CNAME Record** (point www to GitHub):
```
Type: CNAME    Name: www    Value: yourusername.github.io
```

DNS changes take 10 minutes to 24 hours to propagate. Once they do, `cuberoconsulting.com` will point to your new site!

---

## Step 6 — Set Up Your Contact Form (Free)

The contact form needs a backend to receive submissions. Use **Formspree** (free plan: 50 submissions/month — plenty to start):

1. Go to [formspree.io](https://formspree.io) → Sign up free
2. Click **New Form** → Give it a name → Your email to receive submissions
3. Copy your **Form Endpoint** (looks like `https://formspree.io/f/xabc1234`)
4. Open `index.html` in a text editor
5. Find this line:
   ```
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```
6. Replace `YOUR_FORM_ID` with your actual form ID
7. Re-upload `index.html` to GitHub

Now form submissions go straight to your email!

---

## Updating Your Site

Whenever you want to make changes:

1. Edit the files locally (or use GitHub's online editor)
2. Upload the changed files to GitHub (replace the old ones)
3. GitHub Pages rebuilds your site automatically within 1–2 minutes

---

## Cost Summary

| Service | Cost |
|---------|------|
| GitHub Pages hosting | **Free forever** |
| SSL certificate | **Free** (via GitHub Pages) |
| Formspree contact form (50/month) | **Free** |
| Domain (cuberoconsulting.com) | ~$12–15/year (you already own it) |
| **Total** | **~$12–15/year** vs ~$200+/year on Squarespace |

---

## Need Help?

- GitHub Pages docs: [docs.github.com/pages](https://docs.github.com/en/pages)
- Formspree docs: [help.formspree.io](https://help.formspree.io)
- DNS help: Search "[your registrar name] how to change DNS records"
