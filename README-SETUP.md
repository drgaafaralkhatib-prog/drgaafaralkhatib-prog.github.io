# GAF LABS — GitHub Pages Starter (October 2026)

## Important: Review before launch

This package is a **site starter**. The website is not automatically deployed. Puzzle RealmHop's privacy policy is a **review draft**, and a public support contact is intentionally missing. Do **not** use the draft policy as a final production compliance statement until you verify the release code's data handling, age audience, permission/consent flows, Google Play Billing, and retention claims and provide a functional public support email. The visible "publisher review" notice in the privacy page is intentional and should be removed only after sign-off.

## Official site URL

GitHub username: `drgaafaralkhatib-prog` (verify account and ownership)
Repository to create: `drgaafaralkhatib-prog.github.io` (public)
Expected website: `https://drgaafaralkhatib-prog.github.io/`

Create the **username root Pages repository**, not `gaf-labs-website` as a project repository. AdMob crawls the domain root to find `app-ads.txt`.

## Contents

- `index.html` — responsive home page for the publisher
- `assets/styles.css` + `assets/gaf-mark.svg` — website styling and minimal original vector mark
- `apps/puzzle-realmhop/index.html` — game page (no false store link)
- `apps/puzzle-realmhop/privacy.html` — bilingual EN/AR preliminary privacy policy (NEEDS FACTUAL REVIEW)
- `support/index.html` — official support page (NEEDS PUBLIC CONTACT EMAIL)
- `app-ads.txt` — authorized sellers configuration (VERIFY publisher ID before publication)
- `.nojekyll` — disables special Jekyll path processing

## GitHub publication

1. Sign in to github.com and click **New repository**.
2. Owner: `drgaafaralkhatib-prog`.
3. Name EXACTLY: `drgaafaralkhatib-prog.github.io`.
4. Set **Public**. Avoid auto-initializing if using git CLI.
5. Extract this ZIP to a local folder. Open a PowerShell terminal in the extracted `gaf-labs-site` directory.
6. After reviewing the publicly visible content, run:

   ```powershell
   git init -b main
   git add .
   git commit -m "feat: launch GAF LABS site starter"
   git remote add origin https://github.com/drgaafaralkhatib-prog/drgaafaralkhatib-prog.github.io.git
   git push -u origin main
   ```

7. GitHub repository **Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save**.
8. Open `https://drgaafaralkhatib-prog.github.io/` and confirm 200 OK.
9. Open `https://drgaafaralkhatib-prog.github.io/app-ads.txt` and verify it serves PLAIN TEXT, not HTML and no 404.
10. When adding your Google Play developer website, use the root URL `https://drgaafaralkhatib-prog.github.io/` and link the relevant app privacy policy separately.

If the repository already exists, do not run `git init`/push blindly; inspect its state first.

## App-ads.txt confirmation

The included `app-ads.txt` uses `pub-5422716558284814` derived from the AdMob App ID screenshot in this conversation. Before production, copy the exact authorized sellers line from **AdMob → Apps → View all apps → app-ads.txt → How to set up** and compare every character. Google recommends `google.com, pub-ID, DIRECT, f08c47fec0942fa0` for direct sellers. Do not add made-up resellers.

## Privacy policy finalization required

- Specify a real public support email on `/support/` and in the policy.
- Validate code and SDK inventory in the final signed Android release build, including any Firebase, telemetry, crash reporting, Play Services or other processing if used.
- Confirm UMP settings and where users can manage consent later.
- Confirm the Play Console target age groups and Families requirements, if any.
- Align the policy with the Google Play Data Safety form.
- Verify language accuracy (English/Arabic), external links, and date before removing the draft warning.

## Adding another app

For every new app, add:
- `/apps/<slug>/index.html`
- `/apps/<slug>/privacy.html`

Then add a card on the homepage. Multiple apps can use the SAME verified app-ads.txt under this developer website if they are monetized using the SAME AdMob publisher ID.

## Sources

- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://support.google.com/admob/answer/9363762?hl=en
- https://developers.google.com/admob/android/next-gen/app-ads
