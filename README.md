# Coach Check-In

A single-file web app that digitizes your coach's weekly check-in form, plus a daily tracker (meals, steps, water, cardio/training, weigh-in, sleep). Daily logs auto-fill the weekly check-in, which you send to your coach via your Mail app.

No server, no accounts, no cost. Your data stays in your browser on each device.

---

## Run it locally (fastest test)
- **Mac:** double-click `index.html` — it opens in your browser.
- **iPhone:** AirDrop `index.html` to your phone and open it, or host it (below) so it has a URL.

## Host it free on GitHub Pages (so it has a URL on any device)
1. Go to <https://github.com/new> and create a repo, e.g. `coach-checkin` (Public).
2. Click **uploading an existing file** and drag in `index.html` (and this README). Commit.
3. Repo → **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Branch: **main**, folder: **/ (root)**. Save.
6. Wait ~1 minute. Your URL appears at the top of the Pages screen, like:
   `https://<your-username>.github.io/coach-checkin/`

## Add to your Home Screen (feels like an app)
- **iPhone (Safari):** open the URL → Share → **Add to Home Screen**.
- **Mac (Safari):** File → **Add to Dock**. (Chrome: ⋮ → Cast/Save and Share → **Install Page as App**.)

---

## How to use
1. **Setup tab:** enter your name, your coach's email, and an email subject. Save.
2. **Daily tab:** each day, tap your 4 meals as you eat them, log steps, tap water (+250 mL), mark cardio/training, add your weigh-in (weight + time), sleep, and a note. **Save day.**
3. **Weekly tab:** tap **Prefill from this week** to auto-populate % diet followed, sessions missed, start/end weight, and roll your daily notes into comments. Fill the rest, then **Open email to coach** (or **Copy** and paste).

## Using both iPhone and Mac
Data is stored per device. To move it:
- On the device with your data: **Setup → Export backup** (saves a `.json`).
- On the other device: **Setup → Import backup** (it merges, won't wipe existing days).

If you later want true automatic sync across devices, that's the point to add a small backend (e.g., Railway) — the app is structured so its data layer can swap to an API without a rewrite.

## Notes
- Steps and water are entered manually (a web app can't read Apple Health directly).
- The email opens in your default Mail app. If you don't have one set, use **Copy** and paste into any email, Notes, or text.
- Every field from the original PDF check-in is included verbatim in the email.
