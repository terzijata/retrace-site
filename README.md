# Retrace — website

Source for the Retrace website: <https://terzijata.github.io/retrace-site/>

Static HTML/CSS, no build step. `index.html` is the landing page and `privacy.html` is the
privacy policy.

## Security notes

- Every page carries a strict Content-Security-Policy `<meta>` (own files only, no network, no
  inline code). So: **no inline `<script>` or `style="…"` attributes** — put code in a `.js` file
  (see `year.js`) and styles in `styles.css`, or the browser will block them.
- `.nojekyll` makes GitHub Pages serve files as-is (needed for the `.well-known/` folder).
- `.well-known/security.txt` has an **`Expires:` date (2027-09-23) — renew it yearly**.
