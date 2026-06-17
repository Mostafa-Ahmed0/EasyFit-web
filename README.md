# EasyFit — Landing Page

The marketing / download page for **EasyFit**, an AI nutrition tracker built as a
4th-semester project at Technische Hochschule Augsburg (Faculty of Computer Science, SS 2026).

Snap a photo of a meal → the AI estimates its nutrition. Mensa meals log in two taps.

**Live site:** `https://<your-username>.github.io/<repo-name>/`
(fill this in once GitHub Pages is enabled — see below)

---

## Folder structure

Everything lives in the **root** of the repository — no subfolders:

```
your-repo/
├── index.html              ← the landing page (must be named exactly this)
├── easyfit-screenshot.jpg  ← the phone screenshot shown in the hero
├── easyfit.apk             ← the Android app (YOU upload this — see step 2)
└── README.md               ← this file
```

That's it. Three files plus the README. Keep all filenames **lowercase and exactly
as written** — GitHub Pages is case-sensitive, so `EasyFit.APK` will not match the
`easyfit.apk` link in the page.

---

## How to publish it (GitHub Pages, free)

### 1. Create the repository
- On github.com, click **New** to create a repository.
- Give it a name (this becomes part of your URL).
- Set it to **Public** (Pages is free for public repos).
- Create it.

### 2. Upload the files
- In the repo, click **Add file → Upload files**.
- Drag in `index.html`, `easyfit-screenshot.jpg`, `README.md`, **and your `easyfit.apk`**.
- Click **Commit changes**.

> The APK must be named exactly `easyfit.apk`. The download button in the page links
> to that filename. If you name the file differently, the button will 404.

### 3. Turn on GitHub Pages
- Go to **Settings → Pages** (left sidebar).
- Under **Build and deployment → Source**, choose **Deploy from a branch**.
- Branch: **main**, folder: **/ (root)**. Click **Save**.
- Wait ~1–2 minutes, refresh, and the live URL appears at the top of that section.

Open the URL — your page is live, and the **Android APK** button downloads `easyfit.apk`.

---

## Important: the 100 MB file limit

GitHub blocks individual files over **100 MB**. Android APKs can exceed this.

- **Under 100 MB** → just upload it to the repo as described above. Nothing else to do.
- **Over 100 MB** → don't put it in the repo. Instead:
  1. Go to your repo's **Releases** → **Create a new release** (Releases allow files up to 2 GB).
  2. Attach `easyfit.apk` as a release asset and publish.
  3. Copy the download link of the attached file.
  4. In `index.html`, find the Android button (`href="easyfit.apk"`) and replace it
     with that full release URL.

---

## Editing things later

A few placeholders are left for the team to fill in:

| What | Where in `index.html` | Current value |
|------|------------------------|---------------|
| Contact email | search for `mailto:` | `easyfit-team@example.com` |
| iOS / TestFlight | the second download button | disabled until iOS is ready |

To change the contact email, edit the `mailto:` address. To enable the TestFlight
button later, replace its `href="#download"` with your real TestFlight URL and remove
the `onclick="return false;"` and the inline `style`.

---

## Custom domain (optional)

The free `github.io` address works forever. If you later want something like
`easyfit.app`:
1. Buy the domain from a registrar (Cloudflare, Porkbun, Namecheap — roughly €10–15/year).
2. In **Settings → Pages → Custom domain**, enter the domain and follow the DNS steps shown.

Hosting stays free — you'd only pay for the domain.

---

## The team

Ahmed Somida · Yousif Abdelaziz · Mahmoud Abdelazim · Ammar Altantawy ·
Mostafa Ahmed · Nazanin Moradi · Raphael Maringgele

Supervisor: **Prof. Dr. Jens Lauterbach**
Technische Hochschule Augsburg · Faculty of Computer Science · SS 2026
