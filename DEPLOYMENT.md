# Deployment Guide for csbrewed.com

This guide explains how to publish this landing page to GitHub Pages and configure your DNS so that `csbrewed.com` serves this homepage instead of redirecting to `the-surf-hero`.

---

## 1. Push to GitHub

1. Create a new repository on GitHub under your account (`schornon`):
   - Recommended repository name: `csland` (or `csbrewed.com`)
   - Keep it Public
   - Do not initialize with README or license (they are already included here)

2. Link your local repo and push:
   ```bash
   cd /Users/serhii/cs/github/csland
   git remote add origin https://github.com/schornon/csland.git
   git push -u origin main
   ```

---

## 2. Enable GitHub Pages

1. In your GitHub repository, go to **Settings** &rarr; **Pages**.
2. Under **Build and deployment**:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`, folder `/ (root)`
   - Click **Save**.
3. Under **Custom domain**:
   - Ensure `csbrewed.com` is entered (it will automatically pick up the `CNAME` file).
   - Check **Enforce HTTPS** (once DNS propagates and the certificate is issued).

---

## 3. Update DNS at Namecheap (Replacing the Redirect)

Currently, `csbrewed.com` has a **URL Redirect / URL Forwarding** record in Namecheap pointing to `https://the-surf-hero.csbrewed.com`.

To serve this new homepage directly at `csbrewed.com`:

1. Log into **Namecheap** &rarr; **Domain List** &rarr; Click **Manage** next to `csbrewed.com`.
2. Go to the **Advanced DNS** tab.
3. **Remove** the URL Redirect record for `@` pointing to `https://the-surf-hero.csbrewed.com`.
4. **Add four `A` records** for `@` pointing to GitHub Pages IP addresses:
   - Type: `A Record` | Host: `@` | Value: `185.199.108.153` | TTL: Automatic / 1 min
   - Type: `A Record` | Host: `@` | Value: `185.199.109.153` | TTL: Automatic / 1 min
   - Type: `A Record` | Host: `@` | Value: `185.199.110.153` | TTL: Automatic / 1 min
   - Type: `A Record` | Host: `@` | Value: `185.199.111.153` | TTL: Automatic / 1 min
5. **(Optional / Recommended) Add `www` CNAME record**:
   - Type: `CNAME Record` | Host: `www` | Value: `schornon.github.io.` | TTL: Automatic / 1 min
6. **Keep your existing subdomain CNAME records** intact:
   - Type: `CNAME Record` | Host: `teeth` | Value: `schornon.github.io.`
   - Type: `CNAME Record` | Host: `the-surf-hero` | Value: `schornon.github.io.`

---

## 4. Verification

Once DNS propagates (usually 5–30 minutes):
- Visiting `https://csbrewed.com` opens the new CS Brewed showcase!
- Visiting `https://teeth.csbrewed.com` continues to open the Teeth app site.
- Visiting `https://the-surf-hero.csbrewed.com` continues to open The Surf Hero site.
