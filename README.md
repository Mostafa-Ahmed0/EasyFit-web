# EasyFit — Landing Page

A single-page, bilingual (German / English) marketing site for **EasyFit**, the AI-powered nutrition tracker built as a 4th-semester project at the Technische Hochschule Augsburg (Faculty of Computer Science, SS 2026).

The page lets visitors learn about the app and download the Android APK directly, since EasyFit is not on the Google Play Store yet.

## Files

| File | Purpose |
|------|---------|
| `easyfit.html` | The complete landing page — HTML, CSS, and JavaScript in one file. |
| `easyfit-screenshot.jpg` | The dashboard screenshot shown inside the phone mockup. |
| `README.md` | This file. |

Both `easyfit.html` and `easyfit-screenshot.jpg` must stay in the **same folder** — the page loads the image by relative path (`src="easyfit-screenshot.jpg"`).

## Before you publish — fill in 3 placeholders

Open `easyfit.html` in any text editor and replace these:

1. **`REPLACE_WITH_APK_URL`** — the direct link to your hosted `.apk` file (the download button). Appears once.
2. **`REPLACE_WITH_TESTFLIGHT_URL`** — your iOS TestFlight invite link. If you don't have one yet, you can delete the whole `<a ... class="dl-btn ios">...</a>` block instead.
3. **`REPLACE_WITH_EMAIL`** — a contact email for the team. This one appears **twice** (once in the German text, once in the English text), so search for all occurrences.

> Tip: a quick "Find & Replace All" in your editor handles each placeholder in one go.

## Languages (DE / EN)

The page is fully bilingual and chooses a language automatically:

- On first visit it reads the visitor's browser language. **German browser → German**, anything else → **English**.
- **DE / EN** buttons in the top navigation switch the language instantly.
- The chosen language is remembered (via `localStorage`) so a manual choice sticks on the next visit.

### Editing or adding text

All text lives in a single dictionary in the `<script>` block near the bottom of the file, under the `I18N` object with `de` and `en` sections. Each piece of text has a key (e.g. `hero.sub`). To change wording, edit the value for that key in **both** languages. The matching element in the HTML carries the same key via a `data-i18n` attribute, so the two stay linked.

The default-language text is also written directly into the HTML, so the page still reads correctly even if JavaScript is disabled.

## How to deploy

The site is fully static — no build step, no server-side code. Any static host works:

- **GitHub Pages** — push both files to a repo and enable Pages.
- **Netlify / Vercel / Cloudflare Pages** — drag the folder into the dashboard.
- **University web space** — upload both files via FTP/SFTP into the same directory.

Then host the `.apk` somewhere downloadable (the same host, a release attachment, or cloud storage) and point `REPLACE_WITH_APK_URL` at it.

## Installing the APK (for visitors)

Because the app isn't on the Play Store, Android will warn before installing an app from outside the store. Visitors tap **Install anyway** to continue. The page already explains this in the small print under the download buttons.

## Tech notes

- Plain HTML + CSS + a small vanilla-JavaScript snippet for the language switch. No frameworks or dependencies.
- Fonts (Fraunces + Plus Jakarta Sans) are loaded from Google Fonts and require an internet connection to display as designed; the page falls back to system fonts otherwise.
- Responsive down to mobile, with keyboard focus styles and reduced-motion support.

## Credits

**Team:** Ahmed Somida · Yousif Abdelaziz · Mahmoud Abdelazim · Ammar Altantawy · Moustafa Ahmed · Nazanin Moradi · Raphael Maringgele

**Supervisor:** Prof. Dr. Jens Lauterbach

Technische Hochschule Augsburg · Faculty of Computer Science · SS 2026
