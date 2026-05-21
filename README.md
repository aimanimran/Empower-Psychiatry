# Empower Complete Care Psychiatry — Website

Static website for Empower Complete Care Psychiatry PLLC. Built with plain HTML/CSS/JS — no build step required. Designed to be hosted on GitHub Pages.

## Project structure

```
.
├── index.html          # Home
├── about.html          # About Us
├── services.html       # Services
├── feedback.html       # Patient Feedback
├── contact.html        # Contact Us
├── assets/
│   ├── css/styles.css  # All site styles
│   ├── js/main.js      # Nav, mobile menu, scroll reveals
│   └── images/         # Logo, favicon, photos (add real photos here)
├── .nojekyll           # Tells GitHub Pages to skip Jekyll processing
└── CNAME               # (Add later) Your custom domain
```

## Local preview

Just open `index.html` in a browser. Or, from this folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Things to swap in before going live

1. **Doctor photo** — replace the SVG placeholder in `about.html` with a real photo at `assets/images/dr-mushtaq.jpg` and update the `<svg>...</svg>` block to `<img src="assets/images/dr-mushtaq.jpg" alt="Dr. Mushtaq">`.
2. **Booking link** — update the `href="#"` on the "Book Now" / "Schedule a Consultation" buttons in `index.html` and `contact.html`.
3. **Logo (optional)** — the butterfly is hand-drawn as inline SVG. If you have the real logo, drop it in `assets/images/` and replace the `<svg>` markup.
4. **Hero/feedback imagery (optional)** — the feedback page and contact page use abstract illustrations. Real photos can replace those `<svg>` blocks.

## Deploying to GitHub Pages

1. Create a new GitHub repo (e.g. `empower-psychiatry`).
2. Push these files to the `main` branch.
3. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / root**.
4. Your site will be live at `https://<username>.github.io/<repo>/` in a minute or two.

### Custom domain (GoDaddy)

1. In GitHub: **Settings → Pages → Custom domain** — enter `empowerpsychiatryil.com` and save. This creates/updates the `CNAME` file in the repo.
2. In GoDaddy DNS, point the domain at GitHub Pages:
   - **A records** for `@` to all four GitHub IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - **CNAME record** for `www` → `<username>.github.io`
3. Wait for DNS to propagate (minutes to a few hours).
4. Back in GitHub Pages, check **Enforce HTTPS** once the cert provisions.
