# Portfolio – CV/Portfolio gated – June 14, 2026

## Changes in this patch (v2 – full gate)
- Removed Download CV button from hero
- Removed CV link from nav (desktop + mobile)
- Removed CV PDF + MSc Academic Portfolio PDF contact cards
- Replaced with single "CV & Portfolio – Available on request" card
  → mailto:er.darshit7@gmail.com?subject=CV%20%26%20Portfolio%20Request
- Removed CV PDF link from footer
- Deleted Darshit_Gohel_CV.pdf and MSc_Academic_Portfolio_DarshitGohel.pdf from repo
- Updated sitemap.xml – removed PDF URL
- Updated README.md

## Files to deploy (gated version)
workspace/site/
├── index.html
├── robots.txt
├── sitemap.xml
├── README.md
└── DEPLOY_NOTES_v2.md

NO PDFs in the public repo anymore.

## To deploy (overwrites the previous CV-public version)
cd AIMLDS7.github.io
# remove old PDFs from git history in the repo
git rm -f Darshit_Gohel_CV.pdf MSc_Academic_Portfolio_DarshitGohel.pdf || true
# copy new site
cp -r /path/to/workspace/site/index.html .
cp /path/to/workspace/site/robots.txt .
cp /path/to/workspace/site/sitemap.xml .
cp /path/to/workspace/site/README.md .
git add -A
git commit -m "chore: gate CV & portfolio – available on request only"
git push origin main

GitHub Pages will rebuild in ~60s.

Note: the old PDFs will still be in git history. If you want them fully purged (GDPR / data minimization), run:
git filter-repo --path Darshit_Gohel_CV.pdf --path MSc_Academic_Portfolio_DarshitGohel.pdf --invert-paths
git push origin --force --all
Only do this if you understand force-push risks.
