# Pentacle Investment Plan — website

Static website for **pentaclefranchise.com**, ready to deploy on **Vercel**.

| File | Purpose |
|---|---|
| `index.html` | The complete website (all pages, photos, logo and styles in one file) |
| `og-image.png` | Preview image when the link is shared on WhatsApp / social media |
| `robots.txt` | Allows Google to index the site |
| `sitemap.xml` | Helps Google find the site |
| `vercel.json` | Vercel settings (security headers, caching) |
| `docs/` | Downloadable documents: franchise agreement (PDF + Word) and GST certificate (PDF) |

No build step, no `package.json`, no installs needed.

## Deploy on Vercel — Option 1: GitHub (recommended)

1. Create a new repository on GitHub named **`pentacle-investment-plan`**.
2. Click **Add file → Upload files**, drag in all the files from this folder, and click **Commit changes**.
3. Go to **https://vercel.com/new**, choose **Import** next to the `pentacle-investment-plan` repository.
4. Settings:
   - **Project Name:** `pentacle-investment-plan`
   - **Framework Preset:** `Other`
   - **Root Directory:** `./`
   - **Build Command:** leave empty
   - **Output Directory:** leave empty
5. Click **Deploy**. The site goes live at `pentacle-investment-plan.vercel.app`.

Future changes: edit `index.html` on GitHub and commit — Vercel redeploys automatically.

## Deploy on Vercel — Option 2: Vercel CLI

```bash
npm i -g vercel
cd pentacle-investment-plan
vercel            # first time: log in, accept the project name "pentacle-investment-plan"
vercel --prod     # publish to production
```

## Connect your domain

Vercel → your project → **Settings → Domains** → add `pentaclefranchise.com` (and `www.pentaclefranchise.com`).
If the domain is already attached to your old Vercel project, remove it there first, then add it here.
Follow the DNS records Vercel shows, if any. HTTPS is set up automatically.

## Change details later

Open `index.html` and find the **SETTINGS** block near the top of the script:

- `whatsappNumber`, `contacts` (emails & phones), `address`
- `franchisesCompleted` (currently 43)
- `sendTo` — where Apply / Contact details are sent (WhatsApp +91 99526 42243, ragavendraragul12@gmail.com)
- `formEndpoint` — optional Formspree / Web3Forms link to receive applications automatically by email
- `productsSite` — link used on the Products page
- `documents` — the download list. To replace a document, upload a new file to `docs/` with the same name.

Page links: `/#/franchise-investment-plan`, `/#/apply`, `/#/contact`, `/#/manufacturing-infrastructure` …
