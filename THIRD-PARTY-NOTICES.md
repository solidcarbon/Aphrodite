# Third-party notices

Aphrodite is proprietary software by SolidCarbon Works, and it's built with the open-source components below. Each component is licensed under its own terms, not under the Aphrodite EULA. Full licence texts are in the `licenses/` folder next to this file.

Generated 2026-11-05 for Aphrodite 2.0.0. Regenerate it whenever dependencies change.

## Chromium and Electron

Aphrodite runs on **Electron 45.0.0** (MIT licence, © GitHub Inc. and Electron contributors), which includes **Chromium** (BSD-3-Clause and many other licences) and **Node.js** (MIT).

The full licence texts for Chromium and everything it bundles are in **`LICENSES.chromium.html`**, and Electron's licence is in **`LICENSE.electron.txt`**. Both are in the Aphrodite install folder.

Chromium includes **FFmpeg**, which is licensed under the **GNU LGPL 2.1**. It ships as a separate library (`ffmpeg.dll`). You may replace it with your own build, and the Aphrodite EULA allows the reverse engineering needed to debug such a change. Source: https://ffmpeg.org and https://chromium.googlesource.com/chromium/third_party/ffmpeg

## Mozilla Public License 2.0 components

The following are covered by the **MPL-2.0** (`licenses/MPL-2.0.txt`). Aphrodite uses them **unmodified**. You can get the source code for each one at the address listed, or ask us at simplecarbon@proton.me for a copy.

| Package | Version | Source |
|---|---|---|
| @duckduckgo/autoconsent (including its consent rules) | 16.56.0 | https://github.com/duckduckgo/autoconsent |
| @ghostery/adblocker | 2.20.1 | https://github.com/ghostery/adblocker |
| @ghostery/adblocker-content | 2.20.3 | https://github.com/ghostery/adblocker |
| @ghostery/adblocker-extended-selectors | 2.20.3 | https://github.com/ghostery/adblocker |
| @ghostery/url-parser | 1.3.1 | https://github.com/ghostery/url-parser |
| @remusao/guess-url-type | 2.1.0 | https://github.com/remusao/mono |
| @remusao/small | 2.1.0 | https://github.com/remusao/mono |
| @remusao/smaz | 2.2.0 | https://github.com/remusao/mono |
| @remusao/smaz-compress | 2.2.0 | https://github.com/remusao/mono |
| @remusao/smaz-decompress | 2.2.0 | https://github.com/remusao/mono |
| @remusao/trie | 2.1.0 | https://github.com/remusao/mono |
| dompurify (MPL-2.0 or Apache-2.0; used under Apache-2.0) | 3.4.17 | https://github.com/cure53/DOMPurify |

## Apache License 2.0

| Package | Version | Source |
|---|---|---|
| @mozilla/readability (© Arc90 Inc., Mozilla) | 0.6.0 | https://github.com/mozilla/readability |
| dompurify (© Cure53 and contributors) | 3.4.17 | https://github.com/cure53/DOMPurify |

Licence text: `licenses/Apache-2.0.txt` (full text: https://www.apache.org/licenses/LICENSE-2.0).

## Font

**Source Serif 4** (© Adobe), packaged by Fontsource (`@fontsource-variable/source-serif-4` 5.3.0). It's licensed under the **SIL Open Font License 1.1** (`licenses/OFL-1.1.txt`). It's bundled with Aphrodite and isn't sold on its own.

## MIT, ISC, BSD and similar permissive licences

Each of these packages is © its authors, and its licence text is included in the package's folder inside the installed app (`resources/app.asar/node_modules/<package>/LICENSE`).

| Package | Version | Licence | Source |
|---|---|---|---|
| @types/trusted-types | 2.0.7 | MIT | https://github.com/DefinitelyTyped/DefinitelyTyped |
| adm-zip | 0.5.18 | MIT | https://github.com/cthackers/adm-zip |
| argparse | 2.0.1 | Python-2.0 | https://github.com/nodeca/argparse |
| builder-util-runtime | 9.7.0 | MIT | https://github.com/electron-userland/electron-builder |
| debug | 4.4.3 | MIT | https://github.com/debug-js/debug |
| electron-updater | 6.8.10 | MIT | https://github.com/electron-userland/electron-builder |
| fs-extra | 10.1.0 | MIT | https://github.com/jprichardson/node-fs-extra |
| graceful-fs | 4.2.11 | ISC | https://github.com/isaacs/node-graceful-fs |
| js-yaml | 4.3.2 | MIT | https://github.com/nodeca/js-yaml |
| jsonfile | 6.2.1 | MIT | https://github.com/jprichardson/node-jsonfile |
| lazy-val | 1.0.5 | MIT | https://github.com/develar/lazy-val |
| lodash.escaperegexp | 4.1.2 | MIT | https://lodash.com/ |
| lodash.isequal | 4.5.0 | MIT | https://lodash.com/ |
| ms | 2.1.3 | MIT | https://github.com/vercel/ms |
| sax | 1.6.1 | BlueOak-1.0.0 | https://github.com/isaacs/sax-js |
| semver | 7.7.4 | ISC | https://github.com/npm/node-semver |
| tiny-typed-emitter | 2.1.0 | MIT | https://github.com/binier/tiny-typed-emitter |
| tldts | 7.4.18 | MIT | https://github.com/remusao/tldts |
| tldts-core | 7.4.20 | MIT | https://github.com/remusao/tldts |
| tldts-experimental | 7.4.19 | MIT | https://github.com/remusao/tldts |
| universalify | 2.0.1 | MIT | https://github.com/RyanZim/universalify |

## Data downloaded while Aphrodite runs (not distributed with Aphrodite)

Aphrodite downloads these lists straight from their publishers. They aren't part of the installer, and they remain under their authors' licences. Our thanks to:

- **EasyList, EasyPrivacy, EasyList Cookie** (EasyList authors; GPL-3.0 / CC BY-SA 3.0), via Ghostery's mirror
- **uBlock Origin filters** (Raymond Hill and contributors; GPL-3.0), via Ghostery's mirror
- **Peter Lowe's blocklist**, via Ghostery's mirror
- **AdGuard Base and URL Tracking filters** (AdGuard; GPL-3.0)
- **malware-filter** phishing and URLhaus lists (curbengh; CC0 / MIT), built from PhishTank, OpenPhish, PhishStats and abuse.ch URLhaus
