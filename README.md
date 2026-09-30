# Parañaque Emergency Ready (PER) v3

One-tap access to every Parañaque emergency hotline. **Prepared. Educated. Ready.**

Live web app: https://zayon-systems.github.io/ParanaqueCity · Developed by Zayon Systems

## Updating hotline numbers (no new APK needed)
Edit `contacts.json` on GitHub → commit. Every installed app picks up the new numbers the next time it opens online.
- Numbers are in calling order: the first is dialed, the rest are offered if the line is busy.
- Set `lastVerified` (YYYY-MM-DD) each time you confirm the numbers by phone — it shows in the app.
- Barangay hotlines go under `"barangays"`, using the exact names in the app, e.g. `"BF Homes": [["Brgy. BF Homes · (02) 8xxx-xxxx", "028xxxxxxx"]]`.

## Android APK — built from this same repo
- **Actions → Build PER Parañaque APK → Run workflow** builds a signed APK (5–8 min) and publishes it under **Releases**.
- Needs 4 secrets (Settings → Secrets and variables → Actions): `PER_KEYSTORE_BASE64`, `PER_KEYSTORE_PASSWORD`, `PER_KEY_ALIAS`, `PER_KEY_PASSWORD`.
- Keep a backup of the keystore — without it, future APKs can't update installed apps.
