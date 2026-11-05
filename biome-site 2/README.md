# Biome Renovations portfolio site

A plain static site (HTML + CSS, no build step). Works as-is on GitHub Pages.

## Files
- `index.html`: home page with the project cards
- `kitchen.html`: the kitchen case study (the template for every future project)
- `style.css`: all colors and fonts live at the top as variables (`:root`)
- `images/kitchen/`: put photos here, named by photo number (e.g. `1324.jpg`)

## Photos
Export photos as JPG, roughly 1600px on the long edge, and name them by number:
`1453.jpg` (finished kitchen: home card, hero, and "after"), `2795.jpg` (before), `1324.jpg` (halfway), `1396.jpg` (nearly done), plus the other process shots.
Until a photo exists, its slot shows a labeled placeholder.

## Adding a new project
1. Copy `kitchen.html` to e.g. `bathroom.html` and swap the text and photo names.
2. Copy the `<a class="card">` block in `index.html` and point it at the new page.

## Publish on GitHub Pages
1. Create a repo (e.g. `biome-renovations`) and upload these files so `index.html` is at the top level.
2. Repo Settings > Pages > Deploy from a branch > `main` / root.
3. Your site is live at `https://<username>.github.io/<repo>/` within a couple of minutes.

## Custom domain + email
1. Buy a domain from a registrar (Cloudflare, Namecheap, Porkbun).
2. In the repo, add a file named `CNAME` containing just the domain (e.g. `biomerenovations.com`), or set it under Settings > Pages > Custom domain.
3. At the registrar's DNS settings, follow GitHub's current Pages instructions for the apex domain (A records) and `www` (CNAME). Then tick "Enforce HTTPS" in Pages settings.
4. Email forwarding: turn on the registrar's free email forwarding and forward `hello@yourdomain.com` to your existing inbox. Add the mail records the registrar asks for.
5. Update the `mailto:` address in `index.html` and `kitchen.html` (search for `hello@biomerenovations.com`).

## Before going live
- Registration number is in the footer of every page. Update it if it ever changes, and add it to any new page you create from the kitchen template.
- Confirm the kitchen photos show nothing you wouldn't want public (house numbers, personal items).
