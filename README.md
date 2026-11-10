# IronTrack 40+ — 5 Day Workout Tracker

A phone-friendly workout tracker for a 5-day Push / Legs / Pull / Upper / Lower program.

## Features
- **Saves as you type.** Weights, reps and checkmarks stay put through refreshes, app switches and locked screens.
- **No ✓ tap needed.** Enter the weight and reps. About 1.5 seconds after you stop typing (or as soon as you tap Done), the set completes itself and the rest timer starts.
- **Rest countdown screen.** A full-screen countdown ring shows your rest and what's next, with +30s, Skip and Hide buttons. When rest is over, the screen flashes, the phone vibrates (Android only), and it jumps you to your next set.
- **"Last time" numbers.** Each exercise shows what you lifted last session, and each box shows last time's number in grey. Tap ✓ on an empty set to reuse those numbers.
- **History.** Tap "Finish & Save Workout" to log the session. The 📈 History tab lists every workout with sets, duration and total pounds lifted.
- **Accurate rest timer.** It starts automatically with each exercise's rest time when a set is completed. It stays correct when the phone locks. Tap the time in the bottom bar to reopen the countdown screen. Quick buttons: 30s, 1m, 1:30, 2m, 3m.
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
- After any change, bump `CACHE` in `sw.js` (for example `irontrack-v4`) and `APP_VERSION` in `index.html`. Installed phones then switch to the new version the next time the app opens. The version number shows at the bottom of the History tab.

## Files
| File | Purpose |
|---|---|
| `index.html` | The whole app |
| `sw.js` | Offline support (service worker) |
| `manifest.json` | Home-screen app settings |
| `icon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | App icons |
