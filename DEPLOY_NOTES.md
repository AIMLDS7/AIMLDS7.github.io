# Portfolio Fix – June 14, 2026
Top 1% cleanup – Patch #1

## What was fixed (P0 credibility blockers)

1. **GitHub repo links – FIXED**
   - Old site advertised 4 repos that returned 404:
     BESS-Dispatch-Optimiser, Electricity-Price-Forecasting, PV-System-Techno-Economic, EU-Balancing-Market-Analysis
   - Now points to 3 REAL repos:
     • ML_Dayahead_XGBoost_energy_price_forecaster_Austria
     • Data-Analysis-for-Solar-and-Wind
     • NASA_POWER_Hourly_Climate_Data_Downloader_Global
   - 4th card: BESS-Dispatch-Optimiser → "Thesis code, private, available on request" → links to #contact (no 404)

2. **Stats counters – FIXED**
   - Counters rendered 0 for non-JS clients / crawlers
   - Now SSR fallback shows: 50+, 3.2B+, 7+, 20 – then animates up
   - No more "0+ Years" first paint

3. **Contact form – FIXED**
   - Removed "⚙ One-time setup needed" dev banner
   - Formspree ID `xgoqrwkp` is wired and active
   - Success / error states work, mailto fallback removed from UI

4. **Download CV – ADDED**
   - Hero: new "Download CV" button (green outline)
   - Nav: CV link
   - Contact card: CV PDF + MSc Academic Portfolio PDF
   - Footer: CV PDF link
   - Files included in repo: `Darshit_Gohel_CV.pdf`, `MSc_Academic_Portfolio_DarshitGohel.pdf`

5. **SEO / Discoverability**
   - Title unified: `EPCC Commercial Manager | BESS & Renewables | Cost & Contracts`
   - Added `<link rel="canonical" href="https://aimlds7.github.io/">`
   - Fixed og:url (was darshitgohel.com → now aimlds7.github.io)
   - Added JSON-LD Person schema
   - Added `robots.txt` + `sitemap.xml`
   - OG image uses GitHub avatar (replace with real headshot ASAP)

6. **Accessibility**
   - Removed `cursor:none!important` – normal system cursor restored
   - Custom cursor JS disabled (`if(false)`)
   - Skip-link, ARIA labels kept
   - Color contrast unchanged (already WCAG AA)

7. **Navigation / UX**
   - Removed "Provenance" keyword-stuffing link from mobile menu
   - Added CV PDF to nav (desktop + mobile)
   - Location text: "Wels, Austria · EU work permit – RWR Karte eligible"

8. **GitHub Research copy – honest**
   - Old: "dispatch optimisation, EU balancing market analysis"
   - New: "electricity price forecasting (XGBoost), solar/wind resource analysis, NASA POWER climate data pipelines. Thesis BESS dispatch code available on request."

## Files to deploy
Copy everything in `/workspace/site/` to your `AIMLDS7.github.io` repo root:
- index.html  (patched)
- Darshit_Gohel_CV.pdf
- MSc_Academic_Portfolio_DarshitGohel.pdf
- robots.txt  (new)
- sitemap.xml  (new)
- README.md  (updated)

```bash
cd AIMLDS7.github.io
cp -r /path/to/workspace/site/* .
git add -A
git commit -m "fix: credibility patch – real GitHub repos, CV download, SEO, a11y – June 2026"
git push origin main
```

GitHub Pages will redeploy in ~1 min.

## Still TODO for top 1% (next)
1. **Publish the 4 flagship repos for real** – this patch only stops the 404 bleed. Top candidates ship:
   - BESS-Dispatch-Optimiser with Streamlit demo, tests, Dockerfile
   - Electricity-Price-Forecasting with MAPE benchmark table
   - Add proper READMEs to the 3 existing repos (they're currently near-empty)
2. Professional headshot → replace og:image
3. Get a professional email: darshit.gohel@proton.me
4. Rename GitHub @AIMLDS7 → @darshitgohel
5. 1-page CV redesign (current PDF is MD-export, 4 pages)
6. LinkedIn headline = Website headline
7. Add 3 blog posts / case studies with charts

Want me to scaffold the 4 GitHub repos next (Option 2)? I can generate full READMEs, pyproject.toml, CI workflows, and a Streamlit demo skeleton you just drop your thesis notebooks into.
