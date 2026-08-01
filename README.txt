REDACTED ARSENAL — WEBSITE V3

Open index.html in a web browser to preview the website.

Active links:
- YouTube: https://www.youtube.com/@RedactedArsenal
- Buy Me a Coffee: https://buymeacoffee.com/Redacted_Arsenal

The Download tile is a temporary placeholder until the Google Drive link is added.
The package is ready for deployment to GitHub Pages.

Correction: increased hero section height so the full introductory sentence is always visible.

V3.1 correction: restored and explicitly protected the YouTube Watch tile while retaining the complete hero sentence.

V3.2 correction: replaced the clipped YouTube artwork with a clean red YouTube play button and isolated its styling.

V3.3 corrections (cosmetic pass):
- Added favicon (assets/favicon.svg) in the brand style.
- Added og:image (assets/og-image.jpg, 1200x630) plus og:url and twitter:card meta tags. og:url and og:image point to https://lukaszsadlowsky-svg.github.io/redacted-arsenal/ — already filled in.
- Hero image: cropped the leftover clipped letter from the left edge of maus-hero.webp.
- Profile photo: fake sea coordinates replaced with an on-brand [ REDACTED ] bar.
- Buy Me a Coffee tile copy reworded (concrete benefit instead of thanking in advance).
- Decorative divider elements marked aria-hidden for screen readers.
- CSS cleanup: merged the v3.1/v3.2 emergency !important patches into the main stylesheet; the YouTube icon and card rules now use normal cascade order. No visual change intended.

V3.4 — PDF LIBRARY:
- New page pdfs.html: the dossier library. It reads the list of files from pdfs.json and builds the page automatically (file numbers, sizes and search included).
- The Download tile on the main page now links to pdfs.html. The old placeholder toast and script.js are no longer used (script.js can be deleted from the repo).
- Search box appears automatically once the library has more than 6 files.
- File sizes are detected automatically — no need to type them anywhere.

HOW TO ADD A NEW DOSSIER (2 steps, browser only):
1. Upload the PDF into the pdfs folder on GitHub (Add file -> Upload files).
   File names: lowercase, hyphens instead of spaces, no Polish characters.
   Example: wojtek-dossier.pdf
2. Open pdfs.json on GitHub, click the pencil (Edit), and add one entry
   at the TOP of the list, just after the opening [ bracket:

   {
     "title": "Corporal Wojtek — Companion Dossier",
     "file": "wojtek-dossier.pdf",
     "tag": "Unlikely Recruits",
     "desc": "A 36-page study of the soldier bear of the Polish II Corps."
   },

   Rules: "title" and "file" are required, "tag" and "desc" are optional.
   Every entry except the LAST one must end with a comma after }.
   Commit changes — the website updates itself within a minute or two.
