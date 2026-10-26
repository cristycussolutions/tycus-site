# tycus-site

The website for **tycussolutions.com** (TYCUS Enterprises Corporation, operating as TYCUS Solutions). Everything in this repo is published on the site, so a file at `assets/docs/X.pdf` is live at `https://tycussolutions.com/assets/docs/X.pdf`.

## Pages

| Page | File | Live address |
|---|---|---|
| Industrial heaters & instruments (home) | `index.html` | https://tycussolutions.com/ |
| Biomedical & PT (dialysis water & machine care, physical therapy equipment) | `biomedical/index.html` | https://tycussolutions.com/biomedical/ |

The switch at the top of both pages links them. Both quote forms send through the same Formspree form (`assets/site-config.js`). Biomedical & PT enquiries have "Biomedical & PT" in the email subject.

Deep links used by the emails: `/biomedical/?need=assessment#contact` (free RO assessment) and `/biomedical/?need=pt#contact` (PT equipment quote).

Speed rule for the Biomedical & PT page: looping animations must only use `transform`/`opacity` and must pause off screen (the page adds a `paused` class). Check on https://pagespeed.web.dev after every change; aim for 90+ on mobile.

## Folder map

| Folder | What's in it |
|---|---|
| `index.html`, `404.html` | The website pages |
| `assets/img/` | Website images (product photos, team photos, icons) |
| `assets/img/biomed/` | Photos for the Biomedical & PT page |
| `assets/img/brands/` | Brand logos shown on the website |
| `assets/img/email/` | Images used inside outreach emails (see below) |
| `assets/docs/` | PDFs linked from the site and from emails |
| `assets/media/` | Video and other media for the website |

## Email campaigns

Each email loads its images from this repo, so **never rename, move or delete a file that a sent email uses.** Emails already in people's inboxes will show broken images if you do. To change a picture, upload it under a new name and point the next email at the new name.

### Shared by every email
`assets/img/email/logo-white.png`, `assets/img/email/pcab.png`

### Industrial heaters & sensors ("Heat. Measure. Control.")
Files sit at the top of `assets/img/email/`: `hero-v2.jpg`, `cat-heat.jpg`, `cat-measure.jpg`, `cat-control.jpg`, `brands.png` (plus the older `hero.jpg` and `logo.png`).
PDF button: `assets/docs/TYCUS-Company-Profile.pdf`

### Dialysis water & machine care (RO & dialysis PMS)
Images in `assets/img/email/dialysis/`: `hero.jpg`, `card-ro-pm.jpg`, `card-hd.jpg`, `card-supply.jpg`, `mark-drop.png`
PDF button: `assets/docs/TYCUS-Dialysis-Water-Machine-Care.pdf` (12-page brochure)

### Physical therapy equipment
Images in `assets/img/email/pt/`: `mark-cross.png`
PDF button: `assets/docs/TYCUS-Physical-Therapy-Equipment.pdf` (1-page flyer)

## Adding a new email campaign

1. Make a new folder under `assets/img/email/` named after the campaign, e.g. `assets/img/email/calibration/`.
2. Put that campaign's images in it. Reuse `logo-white.png` and `pcab.png` from the top folder.
3. Put any PDF it links to in `assets/docs/`, named `TYCUS-<Topic>.pdf`.
4. Add the campaign to the list above.
