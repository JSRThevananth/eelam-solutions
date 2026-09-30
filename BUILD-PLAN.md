# EELAM Solutions website: build plan (7 tasks)

The site is built in three languages: French (default, root `index.html`), English (`en/index.html`) and Tamil (`ta/index.html`).
Every change is made in all three languages, and the language switcher links are tested at each task.

Rule: we start the next task only after Roy gives the output of the current one.
All cost work is in Task 7.

## Status

| # | Task | Status |
|---|---|---|
| 1 | Setup and safe start | [ ] |
| 2 | French page (default) | [ ] |
| 3 | Images | [ ] |
| 4 | Real content | [ ] |
| 5 | Quote form | [ ] |
| 6 | Privacy and quality checks | [ ] |
| 7 | Costs and launch | [ ] |

---

## Task 1: Setup and safe start
**What we do**
- [ ] Copy the project files into the repo (`CLAUDE.md`, `START-HERE.md`, `en/`, `ta/`, `assets/img/`)
- [ ] Add `.gitignore` (Windows system files)
- [ ] Make the first commit, "Starting files"
- [ ] Review the existing English and Tamil pages together

**Output from Roy:** confirm that `en/index.html` and `ta/index.html` open in the browser and the EN / தமிழ் links work.

## Task 2: French page (default)
**What we do**
- [ ] Build root `index.html` from `en/index.html`, in natural Québec French (not word-for-word)
- [ ] Fix image paths and language links for the root folder
- [ ] Make FR, EN and தமிழ் link to each other on all three pages (exact file names, for example `../ta/index.html`)
- [ ] French is at least as prominent as English (Bill 96)

**Output from Roy:** open the three pages, switch between them, and report anything wrong. Ideally a French speaker reads the text once.

## Task 3: Images
**What we do**
- [ ] Check every filename, size and file weight against the table in `CLAUDE.md`
- [ ] Compress files over 300 KB
- [ ] Confirm the images replace the placeholder boxes on all 3 pages

**Output from Roy:** images in `assets/img/`, or a list of the ones he does not have yet.

## Task 4: Real content
**What we do**
- [ ] Replace placeholders: email, phone, social links, portfolio project names (all 3 languages)
- [ ] Roy reviews all Tamil text (Sri Lankan spelling)
- [ ] Portfolio: blur employer names and data

**Output from Roy:** email, phone, social links, 3 portfolio project names with short descriptions, and Tamil corrections.

## Task 5: Quote form
**What we do**
- [ ] Write the Google Apps Script web app (saves each request to a Google Sheet and emails Roy)
- [ ] Deploy it
- [ ] Put the URL in `FORM_ENDPOINT` on all 3 pages

**Output from Roy:** the deployed script URL, and proof that a test request added a row and sent an email.

## Task 6: Privacy and quality checks
**What we do**
- [ ] Write `privacy.html` in French, English and Tamil (Québec Law 25), marking parts Roy must confirm
- [ ] Accessibility check: visible keyboard focus, colour contrast, alt text
- [ ] Phone layout check

**Output from Roy:** answers to the "confirm yourself" items in the privacy text, and phone test results. A lawyer review of the privacy text is recommended before launch.

## Task 7: Costs and launch
**What we do (all cost work is here)**
- [ ] Print quantities: Roy gets supplier prices for posters, business cards and flyers and picks the fixed quantities included in the $1,000. Update the Marketing materials package in all 3 languages.
- [ ] Add-on pricing: large print runs (cost plus fixed margin), monthly care plan, extra pages or features
- [ ] Domain and hosting costs: buy the domain (for example `eelamsolutions.ca`), add a `CNAME` file, DNS steps. Check that the $1,000 packages still leave a profit after the 1 year of domain and hosting.
- [ ] Business checks (not code): GST/QST after $30,000 revenue, employment agreement about side businesses, how the name "EELAM" is received
- [ ] Decide whether Tamil websites will be offered to clients
- [ ] Go live: push, turn on GitHub Pages (Settings > Pages > main, root), test the live site

**Output from Roy:** supplier prices and chosen quantities, add-on prices, the domain name, and results of the live-site test.

The site does not go public until this task is done, so it never shows undecided prices or quantities.
