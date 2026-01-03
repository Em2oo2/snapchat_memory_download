# Snapchat Memory Downloader (Turbo ZIP)

A powerful Tampermonkey/Userscript designed to fix Snapchat's "My Data" export. Instead of manually clicking thousands of broken links or dealing with incorrect file extensions, this script allows you to download your entire Snapchat history into a single, organized ZIP file directly from your browser.

## ✨ Features

* **Turbo Mode:** Downloads up to 15 files simultaneously (Parallel processing).
* **Binary Fix:** Automatically detects the correct file format (JPG, MP4, or ZIP) using binary headers—no more photos renamed as `.mp4`.
* **One-Click Archive:** Packages everything into a single ZIP file so your browser doesn't block multiple downloads.
* **No Software Required:** Runs entirely in your browser via Tampermonkey.

## 🚀 How to Use

### 1. Prerequisites

* Install the **Tampermonkey** extension for your browser ([Chrome](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo), [Firefox](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/), or [Edge](https://www.google.com/search?q=https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepogocplenbaon)).
* Request your data from [Snapchat My Data](https://accounts.snapchat.com/accounts/downloadmydata).
* Once you receive your data, extract the folder and locate the `memories_history.html` file.

### 2. Installation

1. Click on the **`snapchat_turbo.user.js`** file in this repository.
2. Click the **"Raw"** button at the top right.
3. Tampermonkey will automatically detect the script; click **Install**.

### 3. Downloading your Memories

1. Open your browser's **Extension Settings** > **Tampermonkey** > **Details** and ensure **"Allow access to file URLs"** is turned **ON**.
2. Open your local `memories_history.html` file in your browser (Right-click > Open with Chrome/Firefox).
3. Look for the **Snap Turbo V2.2** panel in the top-right corner.
4. Click **GENERATE ZIP**.
5. Wait for the progress bar to finish. Once done, a single ZIP file will automatically download.

## 🛠️ Technical Details

Snapchat's export often fails because:

1. Browser download limits block more than ~100 concurrent files.
2. The export file lacks proper extensions for many media types.

This script uses **JSZip** to handle the archiving in-memory and performs a **binary "magic byte" analysis** on every file to ensure `image/jpeg` becomes `.jpg` and `video/mp4` stays `.mp4`.

## ⚠️ Important Note

Snapchat download links are **temporary** (usually expiring within 48–72 hours). If the script reports errors or downloads 0KB files, you may need to request a fresh data export from Snapchat to get updated links.

---

### Pro-Tips for your GitHub:

1. **Naming the file:** Name your script `snapchat_turbo.user.js`. The `.user.js` suffix is what tells Tampermonkey to trigger the auto-install when someone clicks "Raw".
2. **GreasyFork:** You might also want to upload it to [GreasyFork](https://greasyfork.org/), which is the most popular site for hosting userscripts. It provides an even easier "Install" button.
3. **License:** Add an MIT license file so people know they can use and share it.

**Would you like me to help you write the Reddit post to announce it on the subreddit?**
