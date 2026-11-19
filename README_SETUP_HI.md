# PLUS MEDISTOCK — GitHub Pages Design Build

## What this build fixes
- CSS is now a real external file: `assets/css/style.css`.
- JavaScript is in `assets/js/site.js`.
- Every page is a complete static HTML file. No Apps Script template tags such as `<?!= include(...) ?>` remain in the website pages.
- The site can be previewed locally by opening `index.html`, and deployed to GitHub Pages.
- Responsive navigation and mobile layout are included.

## Pages
- `index.html` — Home
- `about.html` — About
- `features.html` — Features
- `pricing.html` — Pricing
- `contact.html` — Contact form preview
- `privacy.html` — Privacy policy template
- `terms.html` — Terms template
- `help.html` — Help
- `login.html` — Login screen preview
- `app.html` — Dashboard layout preview

## GitHub Pages deployment
1. Extract this ZIP.
2. Create/open your GitHub repository.
3. Upload all files and folders, keeping the same folder structure.
4. Open repository Settings → Pages.
5. Under Build and deployment, choose Deploy from a branch.
6. Select `main` and `/ (root)`, then Save.
7. Wait for GitHub Pages to publish, then open the URL.

Do not upload only `index.html`; upload `assets` and all other pages too.

## Important functionality boundary
This ZIP fixes the design and GitHub Pages rendering. It is a **static front-end build**, not a completed live pharmacy SaaS:
- Login is a visual preview; it is not connected to authentication.
- Dashboard figures are placeholders.
- Purchases, sales, GST billing, stock ledger, expiry alerts, reports, subscriptions and payment gateway are not live.
- Contact form is a demo and does not send messages.
- Privacy/Terms pages are templates and require legal review and real business details.

The earlier Apps Script starter uses `google.script.run` and Apps Script HTML templating, which do not work by simply opening those template files on GitHub Pages. This build removes that mismatch for the public website. A secure backend/API still needs to be connected before real medical-store data or accounts are used.

## Before publishing
- Add verified business contact details.
- Review legal pages with a qualified professional.
- Do not add real patient/customer/store data until authentication, authorisation, backups, audit logs and security review are completed.


## Dashboard integration update
- `app.html` ko user ke pehle diye Dashboard structure ke hisab se sidebar workspace banaya gaya hai.
- Is project ka backend Google Apps Script `google.script.run` bridge (`clientApi`) use karta hai; isliye purane dashboard ka direct `fetch(API)` code yahan seedha paste nahi kiya gaya.
- Current `Code.gs` mein overview, medical registry, medicines, customers, suppliers aur stock report supported hain.
- Billing, purchase, invoice history, sales return aur expiry report ke server APIs abhi supplied backend mein nahi hain; app unhe clearly pending dikhata hai, fake success nahi.
