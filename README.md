# ErgoChair Studio — Live Posture Monitor (GitHub Pages Web App)

A Progressive Web App (PWA) for the 6-sensor **ErgoChair** Bluetooth Low Energy (BLE) posture monitoring system. Built to run on **GitHub Pages (`https://`)** so **Web Bluetooth**, **offline app caching**, and **persistent on-device user history** all work natively in Chrome on Android and Desktop.

## Features
- **Monitor 2 Detection Engine**: 6-sensor hysteresis thresholding (`800 ± 60` factory default) across `TH-L`, `TH-R`, `LB-L`, `LB-R`, `UB-L`, `UB-R` classifying all 12 postures (`BACK STRAIGHT`, `UPRIGHT`, `SLOUCHING`, `SLUMPING BACK`, `LEAN LEFT`, `LEAN RIGHT`, `ROTATE LEFT`, `ROTATE RIGHT`, `LEGS CROSSED L`, `LEGS CROSSED R`, `ADJUSTING`, `NOT SITTING`).
- **Netflix-Style Profile Selector**: Switch between users or create custom profiles; each profile stores its own posture history, daily stats, and multi-day trend data locally in Chrome.
- **Customizable 2-Split Main Screen**: Default layout shows **Detected Posture Live Animation** on top and **Posture Score & Daily Stats** below, with dropdowns to monitor any two modules simultaneously.
- **Dedicated Non-Scrolling Windows**: Bottom dock switches directly to `Monitor`, `Sensors`, `Session`, `Stretch`, `Settings`, and `All Views`.
- **Configurable Bad Posture Popup Alerts**: Alerts when holding any wrong posture past your chosen threshold (`5m 00s` factory default), with live animated posture preview and one-tap **Restore Factory Defaults**.
- **On-Device Persistence + JSON Backup**: Automatically saves profiles, settings, and daily posture logs per user, with **Export / Import Backup (`.json`)** inside Settings.

## Default Login Accounts
Click any Netflix-style profile tile (or use **Sign in with Username & Password**) and enter its simple password:

| Profile | Username | Password |
| :--- | :--- | :--- |
| Jack (Primary Chair) | `jack` | `1234` |
| Maya (Workstation) | `maya` | `2345` |
| Alex (Studio Desk) | `alex` | `3456` |
| Guest (Quick Session) | `guest` | `0000` |

You can also click **Add Profile** to create custom users with their own passwords, or change your password anytime under **Settings → Account Security & Password**.

## How to Publish on GitHub Pages (2 Minutes)
1. Create a new public repository on GitHub (e.g., `ergochair-monitor`).
2. Upload **all files inside this `ergochair-web` folder** (`index.html`, `manifest.json`, `sw.js`, `icon.svg`, `.nojekyll`, `README.md`) to the root of the repository.
3. In your GitHub repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**, select **`main`** and folder **`/ (root)`**, and click **Save**.
5. Wait ~1 minute — your live HTTPS app URL will appear at:
   `https://<your-username>.github.io/<your-repo-name>/`

## How to Install on Your Android Phone
1. Open your GitHub Pages `https://...` URL in **Chrome on Android**.
2. Tap **Install App** in the header (or Chrome menu **⋮ → Add to Home screen**).
3. Launch **ErgoChair** from your home screen anytime — Web Bluetooth pairing, offline loading, custom profiles, and posture history will all work automatically.
