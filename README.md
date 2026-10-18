# Sunday Savings Bank

A kid's savings bank that works on iPhone, Android and iPad. The passbook is kept in a Google Sheet, so every device with the link sees the same money.

## Set up (about 10 minutes, once)

**1. Google Sheet**
1. Go to sheets.new and name the sheet *Sunday Savings Bank*.
2. Extensions → Apps Script. Delete what's there, paste all of `Code.gs`, click Save.
3. Deploy → New deployment → gear icon → Web app. Execute as **Me**, Who has access **Anyone** → Deploy.
4. Authorise it (Advanced → Go to project → Allow). Copy the **Web app URL** (ends in `/exec`).
5. Open the link once in a browser. You should see text starting with `{"ok":true`. The sheet now has *Passbook* and *Settings* tabs. Your grown-up PIN is in Settings → `parentPin`.

**2. GitHub Pages**
1. New repository `savings-bank`, Public.
2. Upload `index.html`, `config.js`, `manifest.webmanifest`, `sw.js` and the four `.png` icons.
3. Edit `config.js` (pencil icon) and paste the Web app URL between the quotes. Commit.
4. Settings → Pages → Deploy from a branch → `main` / root → Save.

The app is at `https://<your-username>.github.io/savings-bank/`.

## On a phone
- iPhone / iPad: open the link in Safari → Share → Add to Home Screen.
- Android: open it in Chrome → ⋮ → Add to Home screen (or Install app).

## Changing the code later
If you edit `Code.gs`, use Deploy → Manage deployments → pencil → Version: New version → Deploy, so the same URL keeps working.
