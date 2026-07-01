# Domain transfer — lidarmatrix.com (do this later)

The site currently lives at `https://lidarmatrix.github.io`. The Wix site at
`lidarmatrix.com` stays live until you switch DNS, so there is **no downtime**.
When you're ready to move the custom domain over, follow these steps.

## 1. Add the custom domain on GitHub
- Repo → **Settings → Pages → Custom domain** → enter `lidarmatrix.com` → **Save**.
- This creates a `CNAME` file in the repo automatically (leave it there).

## 2. Point DNS at the registrar
Add these records where `lidarmatrix.com` is registered:

**Apex (`lidarmatrix.com`) — four A records:**
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**`www` subdomain — one CNAME:**
```
www  →  MYUSERNAME.github.io
```
(Replace `MYUSERNAME` with the account that owns this repo.)

## 3. Wait for DNS, then enforce HTTPS
- DNS can take anywhere from minutes to ~24 hours to propagate.
- Once GitHub shows the domain as verified, tick **Enforce HTTPS** in Settings → Pages.

## 4. Update the site URL
- In `_config.yml`, change:
  ```yaml
  url: "https://lidarmatrix.github.io"
  ```
  to:
  ```yaml
  url: "https://lidarmatrix.com"
  ```
- Commit and push. This keeps sitemaps, SEO tags, and the RSS feed pointing at the right domain.

## 5. Retire the Wix site
- Only after the new site is confirmed live on `lidarmatrix.com`, cancel/park the Wix site.
