# KW Indy Metro South — Office Site

Static site for notifykwsouth.com. No build step, no dependencies — plain HTML and CSS.

## Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g. `kwsouth-site`). Public or private both work with Pages.
2. Upload everything in this folder to the repo root (drag-and-drop on github.com works: **Add file → Upload files**).
3. In the repo: **Settings → Pages → Source: Deploy from a branch → Branch: main, folder: / (root) → Save**.
4. Wait ~1 minute. The site is live at `https://<your-username>.github.io/kwsouth-site/`.

## Point notifykwsouth.com at it

1. In the repo: **Settings → Pages → Custom domain** → enter `www.notifykwsouth.com` → Save.
2. Wherever the domain's DNS is managed (currently Wix): add a **CNAME record** for `www` pointing to `<your-username>.github.io`, and either forward the bare domain to `www` or add GitHub's A records (185.199.108.153, .109., .110., .111.) for `@`.
3. Back in GitHub Pages settings, tick **Enforce HTTPS** once the DNS check passes (can take up to an hour).
4. Only cancel the Wix site plan after the new site answers at the domain.

## Embeds — already wired in

All 7 Cognito forms, the training calendar (published Google Sheet), and both YouTube
videos are embedded with the same URLs the old Wix site used. Form submissions flow to
the same Cognito account and notifications as before — nothing to reconfigure.

One optional extra: the old Locations page had a custom Google My Maps embed. The site
uses a regular Google Maps directions link instead; if you want the custom map back,
copy its embed code from the Wix editor (or Google My Maps) into office/index.html.

Intentionally NOT on this site (it's public): office door codes, the IGNITE password,
and personal login credentials. Keep those in the onboarding emails.

## Editing content

Each page is a standalone HTML file — open it in any text editor. Shared styles live in
`css/site.css`. Staff roster and addresses are in `office/index.html`. Keep the
`<meta name="robots" content="noindex">` tag if you'd rather search engines not index an
internal office site (remove it if you want the site findable on Google).
