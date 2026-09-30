# EELAM Solutions website — project context

This file gives Claude Code the full background of this project. Read it at the start of every session.

## About the owner

- Owner: Roy (Montréal, Québec). Works full time in food safety and quality; runs EELAM Solutions on the side.
- Roy knows some Python, React, Kotlin and Google Apps Script, but this is his **first web development project in Claude Code**.
- English is Roy's second language. Use plain, simple English.

## How to work with Roy (important)

This project is also a learning project. Roy wants to understand what is being built, not only get the result.

1. Work in **small steps**. One change at a time.
2. Before each change, explain in 1–3 simple sentences **what** you will do and **why**.
3. After each change, explain what changed and **how Roy can check it** (for example: "open en/index.html in your browser and scroll to the packages").
4. When you use a new concept (HTML tag, CSS property, Git command), explain it in one short sentence the first time.
5. Ask before large changes, deleting files, or running Git commands that publish (`git push`).
6. Challenge Roy's ideas when there is a better option. Say why, suggest the alternative, and continue only if the idea makes sense.
7. At the end of a session, give a short summary: what we did, what Roy learned, what comes next.

## The business

EELAM Solutions sells three flat-price packages to small businesses in Montréal. Every package costs **$1,000 CAD** (taxes extra).

| Package | Includes |
|---|---|
| Website | Up to 8 pages, French and English, contact form, privacy setup, 3 rounds of changes, 1 year hosting and domain |
| Business app | One tool built on Google Workspace (Apps Script): forms, sheets, live dashboard, works on phones by QR code, team training |
| Marketing materials | Design **and printing** of posters, business cards and flyers, plus social media post designs. Fixed print quantities included. Print-ready and web files |

Add-ons (priced separately): large print runs (cost plus fixed margin), monthly care plan (hosting, updates, fixes), extra pages or features.

Decisions already made — do not change without asking Roy:
- The word "branding" is **not** used anywhere. **No logo design** is offered.
- Marketing materials = posters, business cards, flyers, social media designs only.
- Printing is included in the $1,000 only for **fixed quantities**. Large runs are quoted separately (protects profit, because print cost grows with quantity).
- Price only changes when the client adds something outside the package.

## Languages

The site has three language versions, each in its own folder:

| Language | File | Status |
|---|---|---|
| French (default) | `index.html` (root) | **Not built yet** |
| English | `en/index.html` | Built |
| Tamil | `ta/index.html` | Built |

- French must be the default and at least as prominent as English (Québec Charter of the French Language / Bill 96).
- Tamil uses Sri Lankan Tamil spelling (டொலர், திகதி, ரோய்). Roy reviews all Tamil text.
- Tamil page uses the fonts Noto Serif Tamil and Noto Sans Tamil, smaller headings and taller line height.
- Language switcher links point to exact files (`../ta/index.html`, not `../ta/`) so they work both locally and on GitHub Pages.
- When content changes, **update all three languages**.

## Design (chosen: "A + C" = dark bento + warm editorial)

- Hero: dark evergreen background with a bento tile grid. The turmeric $1,000 tile is the main eye-catcher.
- Rest of page: light sage sections, serif headings, calm and readable.
- About section and footer return to dark evergreen.

Colours:
- `--evergreen #10231f` (dark base), `--evergreen-2 #183330`, `--evergreen-line #2a4742`
- `--sage #e4e8df` (light base), `--sage-2 #d6dccf`
- `--ink #1c2622` (text), `--ink-soft #4b5a54`, `--mist #b9c7c0`
- `--turmeric #e3a72f` (accent), `--turmeric-deep #8a5f0c`

Fonts: Newsreader (headings, serif) and Bricolage Grotesque (body). Tamil adds Noto Serif Tamil / Noto Sans Tamil.

Motion: only one animation (bento tiles rise on page load), turned off for reduced-motion users. Do not add more decorative animations.

Page sections in order: navigation, hero, packages, how it works (4 steps), about, recent work, FAQ, quote form, footer.

## Images

All images live in `assets/img/`. Each image slot shows its filename until the real image is added; the image appears automatically once a file with that exact name exists.

| Filename | Where | Size (px) |
|---|---|---|
| logo.png | Navigation (not placed yet; text logo used now) | 400 × 120 |
| logo-white.png | Footer | 400 × 120 |
| favicon.png | Browser tab | 512 × 512 |
| og-share.jpg | Link preview on social media | 1200 × 630 |
| hero-main.jpg | Hero, large tile | 1200 × 900 |
| service-website.jpg | Website card | 800 × 600 |
| service-app.jpg | App card and hero tile | 800 × 600 |
| service-marketing.jpg | Marketing card and hero tile | 800 × 600 |
| about-founder.jpg | About section | 800 × 800 |
| portfolio-1.jpg / -2 / -3 | Recent work | 1200 × 800 |
| contact-side.jpg | Beside quote form (optional) | 800 × 1000 |

Rules: lowercase, hyphens, no spaces. Roy keeps originals in Google Drive, but images must be **copied into `assets/img/`** in the repo (do not link to Google Drive; Drive links break on live sites). Compress images before adding (aim under 300 KB each).

Portfolio: Roy's work tools at his employer may not be shown publicly without permission; blur company names and data.

## Hosting and technical rules

- Hosting: **GitHub Pages** (static files only; no server code).
- Plain HTML, CSS and a little JavaScript. No frameworks, no build step. Keep each page in one file for now.
- Quote form: will send to a **Google Apps Script web app** that saves the request to a Google Sheet and emails Roy. The URL goes in `FORM_ENDPOINT` at the bottom of each page. Not set up yet.
- Privacy (Québec Law 25): the site needs `privacy.html` (French) and English/Tamil versions, because the form collects personal information. Not built yet.
- Keep the page accessible: keyboard focus visible, alt text on meaningful images, good colour contrast, works on phones.

## Open items (to do)

1. Build the French page (`index.html` at root) from the English page.
2. Decide real print quantities for the Marketing materials package (Roy to check supplier prices), then update all 3 languages.
3. Decide whether Tamil websites will be offered to clients.
4. Add images to `assets/img/`.
5. Build the Apps Script form endpoint and connect it.
6. Create privacy policy pages.
7. Replace placeholders: email, phone, social links, portfolio project names.
8. Publish on GitHub Pages; later connect a custom domain (for example eelamsolutions.ca) with a `CNAME` file.
9. Business checks for Roy (not code): GST/QST registration after $30,000 revenue; check his employment agreement about side businesses; consider how the name "EELAM" is received by general Montréal clients.
