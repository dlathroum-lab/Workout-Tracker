# IronTrack 40+ — 5 Day Workout Tracker

A phone-friendly workout tracker for a 5-day Push / Legs / Pull / Upper / Lower program.

## Features
- **Saves as you type.** Weights, reps and checkmarks stay put through refreshes, app switches and locked screens.
- **"Last time" numbers.** Each exercise shows what you lifted last session, and each box shows last time's number in grey. Tap ✓ on an empty set to reuse those numbers.
- **History.** Tap "Finish & Save Workout" to log the session. The 📈 History tab lists every workout with sets, duration and total pounds lifted.
- **Accurate rest timer.** It starts automatically when you check off a set, stays correct when the phone locks, and beeps and vibrates when rest is over. Use +15 to add time.
- **Keeps the screen on** during a workout, on supported phones.
- **Opens on your next workout.** After you finish Day 1, the app opens on Day 2.
- **Works offline** once installed to your home screen.
- **Backup.** Export or import your data from the History tab. Data is stored only in your phone's browser, so export now and then.

## Install on your phone
1. In this repo on GitHub, open **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, choose **main** and **/ (root)**, then click **Save**.
2. After a minute, the app will be live at `https://<your-username>.github.io/Workout-Tracker/`.
3. Open that link on your phone:
   - **iPhone (Safari):** Share → **Add to Home Screen**
   - **Android (Chrome):** ⋮ menu → **Install app** / **Add to Home screen**

## Changing the workouts
Every exercise lives in the `PROGRAM` list near the top of the `<script>` in `index.html`. Edit names, sets, reps, rest seconds or notes there, and the page builds itself from that list.
- Keep each exercise's `id` the same once you have history, or its "last time" numbers won't show.
- After any change, bump `CACHE` in `sw.js` (for example `irontrack-v3`) so installed phones download the new version.

## Files
| File | Purpose |
|---|---|
| `index.html` | The whole app |
| `sw.js` | Offline support (service worker) |
| `manifest.json` | Home-screen app settings |
| `icon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | App icons |
