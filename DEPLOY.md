# How to Deploy zerogrobots.com to Cloudflare Pages (Free)

## What you have
This folder contains your complete rebuilt website — 7 HTML pages + 1 CSS file. All images
still load from GoDaddy's CDN, so keep your GoDaddy account active until the migration
is fully live and tested, then cancel hosting (keep the domain registration).

---

## Step 1 — Create a free GitHub account (if you don't have one)
Go to https://github.com and sign up. It's free.

## Step 2 — Create a new repository
1. Click the **+** button → **New repository**
2. Name it `zerogrobots` (or anything you like)
3. Set it to **Public** (required for free Pages)
4. Click **Create repository**

## Step 3 — Upload your files
1. On the repository page, click **Add file → Upload files**
2. Drag all the files from this folder into the upload area:
   - index.html, need.html, challenge.html, design-requirements.html,
     robot-design.html, robot-motion.html, about.html, style.css
3. Click **Commit changes**

## Step 4 — Deploy to Cloudflare Pages
1. Go to https://pages.cloudflare.com and sign up for a free account
2. Click **Create a project → Connect to Git**
3. Authorize Cloudflare to access your GitHub account
4. Select your `zerogrobots` repository
5. Build settings:
   - **Framework preset:** None
   - **Build command:** (leave blank)
   - **Build output directory:** `/` (just a slash)
6. Click **Save and Deploy**
   - Cloudflare will give you a URL like `zerogrobots.pages.dev` — your site is live!

## Step 5 — Point zerogrobots.com to Cloudflare
1. In Cloudflare Pages, go to your project → **Custom domains** → **Set up a custom domain**
2. Enter `zerogrobots.com` and follow the prompts
3. Cloudflare will show you nameservers (e.g. `ns1.cloudflare.com`, `ns2.cloudflare.com`)
4. Go to **GoDaddy → My Domains → zerogrobots.com → DNS → Nameservers**
5. Switch from GoDaddy nameservers to **Custom** and paste in Cloudflare's nameservers
6. DNS propagation takes up to 24 hours, but usually under 30 minutes

## Step 6 — Set up the contact form (optional)
The About page contact form uses Formspree (free for up to 50 submissions/month):
1. Go to https://formspree.io and create a free account
2. Create a new form — you'll get an endpoint like `https://formspree.io/f/abcd1234`
3. Open `about.html` and replace `YOUR_FORM_ID` with your actual form ID (the part after `/f/`)

## Step 7 — Cancel GoDaddy hosting
Once your site is live at zerogrobots.com on Cloudflare:
1. Log into GoDaddy → **My Products**
2. Cancel the **Website Builder / Hosting** plan (~$21.99/month)
3. **Keep** the domain registration (zerogrobots.com) — that's separate and cheap (~$15-20/year)

---

## Cost after migration
| Item | Before | After |
|------|--------|-------|
| Hosting | $21.99/month | $0 |
| Domain | included | ~$15-20/year |
| **Annual total** | **~$264** | **~$15-20** |

