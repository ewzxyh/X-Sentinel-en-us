## X-Sentinel - EN

Userscript and browser extension for X/Twitter that filters posts by country, region, or language, offering visual highlighting options.

### Features
- **Filter Management:** Add or remove countries, regions, and languages from the blocklist (starts with no defaults).

- **Flexible Behavior:** Choose between hiding or highlighting matches (red border/background). Accounts with region restrictions can be highlighted in yellow.

- **Data Persistence:** Session counts and historical totals are saved in IndexedDB; export function available in the UI.

- **Smart Detection:** Monitors the profile's "About" section to identify changes in country/region and username.

- **Easy Access:** The settings button (🚫 icon) in the side navigation bar opens the edit panel.

### Images

Sidebar Menu:

<img width="292" height="834" alt="image" src="https://github.com/user-attachments/assets/b6b3f009-c20d-4b2a-bc66-2bb86baa539f" />

Settings Menu:

<img width="684" height="741" alt="image" src="https://github.com/user-attachments/assets/85b074e2-5078-4df0-b785-a01e7c2b4d7f" />

Country Display on Posts:

<img width="601" height="280" alt="image" src="https://github.com/user-attachments/assets/dff19c3f-ee5a-4e8b-b6b6-5cc248636a81" />

### Usage
1) **Userscript:** Download `X-Sentinel.user.js` from the Releases section (or use `X-Sentinel-user.js` in this repo) and install it via your userscript manager (Tampermonkey/Greasemonkey).

2) **Chrome Extension:** Download the `X-Sentinel-extension.zip` file from Releases. In `chrome://extensions` (enable Developer Mode), load it as an unpacked extension or load the `extension/` folder directly.

3) **Access:** Open X/Twitter and click the **🚫 X-Sentinel** button in the side navigation bar.

4) **Configuration:** Add countries/regions/languages; toggle between hiding or visual highlighting modes.

5) **Apply:** Reload the page to apply changes; use the "Export Database" option for backups or debugging.

### Development Notes
- **Zero Build:** No build step required; edit the `X-Sentinel-user.js` file directly.

- **Formatting (Optional):** `npx prettier --check "X-Sentinel-user.js"`.

- **Storage:** Uses `localStorage` + IndexedDB (`known` store for users, `stats` for totals).

- **Extension:** Entry point at `extension/content.js`, manifest at `extension/manifest.json`.

- **CI/CD:** Pushes to `main`/`master` generate build artifacts (userscript, zipped extension, changelog). Tags `v*` automatically publish a Release on GitHub with these files and the changelog.

---

## Suggested Tweet (English)

Sick of the noise on your timeline? 🚫

I built **X-Sentinel**: An open-source extension/script to filter X posts by country, region, or language.

Filter out the spam farms or just content from regions you don't care about. Clean up your feed locally.

👇
https://github.com/ewzxyh/X-Sentinel

#OpenSource #JavaScript #Privacy
