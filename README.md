# DailyDairy activation page

Support page for activating new DailyDairy installs:
https://nparekh165.github.io/dailydairy-activation/

The support team opens the page, enters the support password once per device, types the
customer's install code and replies with the 6-digit activation code.

The activation key inside `site/index.html` is encrypted with the support password
(AES-256-GCM, PBKDF2-SHA256 600 000 rounds). The plain key and the password are never in this repo.
The page is regenerated on the owner's PC (`seal-page.js`, kept outside git) when the password changes,
and GitHub Actions publishes `site/` to GitHub Pages on every push to `main`.
