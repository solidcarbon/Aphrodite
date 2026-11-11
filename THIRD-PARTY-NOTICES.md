# Third-party notices

Aphrodite is proprietary software by SolidCarbon Works, and it's built with the open-source components below. Each component is licensed under its own terms, not under the Aphrodite EULA. Full licence texts are in the `licenses/` folder next to this file.

Generated 2026-11-11 for Aphrodite 2.10.0. Regenerate it whenever dependencies change.

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
| pdfjs-dist (PDF.js, © Mozilla Foundation), used by the PDF viewer | 6.4.299 | https://github.com/mozilla/pdf.js |

Licence text: `licenses/Apache-2.0.txt` (full text: https://www.apache.org/licenses/LICENSE-2.0).

## PDF viewer components

The PDF viewer uses **PDF.js** (Apache-2.0, listed above), unmodified. These parts come with it, each under its own licence. Their licence texts are in the installed app, next to the files (`resources/app.asar/build/pdf/`):

| Component | Licence | Licence file |
|---|---|---|
| Standard PDF fonts (Foxit; © PDFium Authors) | BSD-3-Clause | `standard_fonts/LICENSE_FOXIT` |
| Character maps (© Adobe Systems) | BSD-3-Clause | `cmaps/LICENSE` |
| OpenJPEG image decoder | BSD-2-Clause | `wasm/LICENSE_OPENJPEG`, `wasm/LICENSE_PDFJS_OPENJPEG` |
| JBIG2 image decoder (© PDFium Authors, Mozilla) | BSD-3-Clause and Apache-2.0 | `wasm/LICENSE_JBIG2`, `wasm/LICENSE_PDFJS_JBIG2` |
| qcms colour management (© Mozilla, Marti Maria) | MIT | `wasm/LICENSE_QCMS`, `wasm/LICENSE_PDFJS_QCMS` |

PDF.js's Liberation Sans fonts and its script sandbox are not included.

## Converter and PDF editor components

The Converter and the PDF editor are built with the packages below, and the packages those are built on. They are bundled into the app (`resources/app.asar/build/tools/libs.mjs` and `resources/app.asar/build/pdf/pdf-lib.min.mjs`), unmodified. Each is © its authors. Their licence texts are in the installed app at `resources/app.asar/build/tools/licenses/<package>.txt`, and the notices their authors ask to keep are in `resources/app.asar/build/tools/libs.mjs.LEGAL.txt`.

| Package | Version | Licence | Source |
|---|---|---|---|
| @cantoo/pdf-lib (changes to PDF files: pages, text, redaction, hidden details) | 2.11.1 | MIT | https://github.com/cantoo-scribe/pdf-lib |
| @xmldom/xmldom | 0.8.15 | MIT | https://github.com/xmldom/xmldom |
| argparse | 1.0.10 | MIT | https://github.com/nodeca/argparse |
| base64-js | 1.5.1 | MIT | https://github.com/beatgammit/base64-js |
| core-util-is | 1.0.3 | MIT | https://github.com/isaacs/core-util-is |
| culori | 4.0.2 | MIT | https://github.com/Evercoder/culori |
| dingbat-to-unicode | 1.0.2 | BSD-2-Clause | https://github.com/mwilliamson/dingbat-to-unicode |
| duck | 0.1.12 | BSD-2-Clause | https://github.com/mwilliamson/duck.js |
| fflate (zip files) | 0.8.3 | MIT | https://github.com/101arrowz/fflate |
| html-entities | 2.6.0 | MIT | https://github.com/mdevils/html-entities |
| immediate | 3.0.6 | MIT | https://github.com/calvinmetcalf/immediate |
| inherits | 2.0.4 | ISC | https://github.com/isaacs/inherits |
| isarray | 1.0.0 | MIT | https://github.com/juliangruber/isarray |
| jszip (MIT or GPL-3.0-or-later; used under MIT) | 3.10.2 | MIT | https://github.com/Stuk/jszip |
| lie | 3.3.0 | MIT | https://github.com/calvinmetcalf/lie |
| lop | 0.4.2 | BSD-2-Clause | https://github.com/mwilliamson/lop |
| mammoth (Word documents to HTML) | 1.13.0 | BSD-2-Clause | https://github.com/mwilliamson/mammoth.js |
| marked (Markdown to HTML) | 18.1.2 | MIT | https://github.com/markedjs/marked |
| node-html-better-parser | 1.5.9 | MIT | https://github.com/Sharcoux/node-html-parser |
| option | 0.2.4 | BSD-2-Clause | https://github.com/mwilliamson/node-options |
| pako | 1.0.11 | MIT and Zlib | https://github.com/nodeca/pako |
| process-nextick-args | 2.0.1 | MIT | https://github.com/calvinmetcalf/process-nextick-args |
| readable-stream | 2.3.8 | MIT | https://github.com/nodejs/readable-stream |
| safe-buffer | 5.1.2 | MIT | https://github.com/feross/safe-buffer |
| setimmediate | 1.0.5 | MIT | https://github.com/YuzuJS/setImmediate |
| sprintf-js | 1.1.3 | BSD-3-Clause | https://github.com/alexei/sprintf.js |
| string_decoder | 1.1.1 | MIT | https://github.com/nodejs/string_decoder |
| tslib | 2.9.1 | 0BSD | https://github.com/Microsoft/tslib |
| turndown (HTML to Markdown) | 7.2.4 | MIT | https://github.com/mixmark-io/turndown |
| underscore | 1.13.8 | MIT | https://github.com/jashkenas/underscore |
| util-deprecate | 1.0.2 | MIT | https://github.com/TooTallNate/util-deprecate |
| xmlbuilder | 10.1.1 | MIT | https://github.com/oozcitak/xmlbuilder-js |

The Converter also uses **PDF.js** and **DOMPurify**, listed above.

## Assistant engine

The optional assistant runs on **llama.cpp** (MIT licence, © The ggml authors, https://github.com/ggml-org/llama.cpp), through **node-llama-cpp** (MIT licence, © Gilad S., https://github.com/withcatai/node-llama-cpp). The ready-built llama.cpp libraries ship inside the `@node-llama-cpp` packages for this system (the processor build and the Vulkan build). Aphrodite uses all of these **unmodified**.

They are built with the packages below. Each one's own licence file is in its folder inside the Aphrodite install folder. The Blue Oak Model License text is in `licenses/BlueOak-1.0.0.txt`.

| Package | Version | Licence | Source |
|---|---|---|---|
| @huggingface/jinja | 0.5.11 | MIT | https://github.com/huggingface/huggingface.js |
| @isaacs/fs-minipass | 4.0.1 | ISC | https://github.com/npm/fs-minipass |
| @kwsites/file-exists | 1.1.1 | MIT | https://github.com/kwsites/file-exists |
| @kwsites/promise-deferred | 1.1.1 | MIT | https://github.com/kwsites/promise-deferred |
| @node-llama-cpp/win-x64 | 3.22.2 | MIT | https://github.com/withcatai/node-llama-cpp |
| @node-llama-cpp/win-x64-vulkan | 3.22.2 | MIT | https://github.com/withcatai/node-llama-cpp |
| @reflink/reflink | 0.1.19 | MIT | https://github.com/pnpm/reflink |
| @reflink/reflink-win32-x64-msvc | 0.1.19 | MIT | https://github.com/pnpm/reflink |
| @simple-git/args-pathspec | 1.0.4 | MIT | https://github.com/steveukx/git-js |
| @simple-git/argv-parser | 1.1.1 | MIT | https://github.com/steveukx/git-js |
| @tinyhttp/content-disposition | 2.2.4 | MIT | https://github.com/tinyhttp/tinyhttp |
| ansi-escapes | 6.2.1 | MIT | https://github.com/sindresorhus/ansi-escapes |
| ansi-regex | 5.0.1 | MIT | https://github.com/chalk/ansi-regex |
| ansi-styles | 4.3.0 | MIT | https://github.com/chalk/ansi-styles |
| ansi-styles | 6.2.3 | MIT | https://github.com/chalk/ansi-styles |
| async-retry | 1.3.3 | MIT | https://github.com/vercel/async-retry |
| bytes | 3.1.2 | MIT | https://github.com/visionmedia/bytes.js |
| chalk | 5.6.2 | MIT | https://github.com/chalk/chalk |
| chmodrp | 1.0.2 | MIT | https://github.com/leonzalion/chmodrp |
| chownr | 3.0.0 | BlueOak-1.0.0 | https://github.com/isaacs/chownr |
| ci-info | 4.4.0 | MIT | https://github.com/watson/ci-info |
| cli-cursor | 5.0.0 | MIT | https://github.com/sindresorhus/cli-cursor |
| cli-spinners | 2.9.2 | MIT | https://github.com/sindresorhus/cli-spinners |
| cli-spinners | 3.4.0 | MIT | https://github.com/sindresorhus/cli-spinners |
| cliui | 8.0.1 | ISC | https://github.com/yargs/cliui |
| cmake-js | 8.0.0 | MIT | https://github.com/cmake-js/cmake-js |
| color-convert | 2.0.1 | MIT | https://github.com/Qix-/color-convert |
| color-name | 1.1.4 | MIT | https://github.com/colorjs/color-name |
| commander | 10.0.1 | MIT | https://github.com/tj/commander.js |
| cross-spawn | 7.0.6 | MIT | https://github.com/moxystudio/node-cross-spawn |
| debug | 4.4.3 | MIT | https://github.com/debug-js/debug |
| deep-extend | 0.6.0 | MIT | https://github.com/unclechu/node-deep-extend |
| emoji-regex | 8.0.0 | MIT | https://github.com/mathiasbynens/emoji-regex |
| env-var | 7.5.0 | MIT | https://github.com/evanshortiss/env-var |
| escalade | 3.2.0 | MIT | https://github.com/lukeed/escalade |
| eventemitter3 | 5.0.4 | MIT | https://github.com/primus/eventemitter3 |
| filename-reserved-regex | 3.0.0 | MIT | https://github.com/sindresorhus/filename-reserved-regex |
| filenamify | 6.0.0 | MIT | https://github.com/sindresorhus/filenamify |
| fs-extra | 11.4.1 | MIT | https://github.com/jprichardson/node-fs-extra |
| get-caller-file | 2.0.5 | ISC | https://github.com/stefanpenner/get-caller-file |
| get-east-asian-width | 1.7.0 | MIT | https://github.com/sindresorhus/get-east-asian-width |
| graceful-fs | 4.2.11 | ISC | https://github.com/isaacs/node-graceful-fs |
| ignore | 7.0.14 | MIT | https://github.com/kaelzhang/node-ignore |
| ini | 1.3.8 | ISC | https://github.com/isaacs/ini |
| ipull | 3.9.5 | MIT | https://github.com/ido-pluto/ipull |
| is-fullwidth-code-point | 3.0.0 | MIT | https://github.com/sindresorhus/is-fullwidth-code-point |
| is-fullwidth-code-point | 5.1.0 | MIT | https://github.com/sindresorhus/is-fullwidth-code-point |
| is-interactive | 2.0.0 | MIT | https://github.com/sindresorhus/is-interactive |
| is-unicode-supported | 2.1.0 | MIT | https://github.com/sindresorhus/is-unicode-supported |
| isexe | 3.1.5 | BlueOak-1.0.0 | https://github.com/isaacs/isexe |
| jsonfile | 6.2.1 | MIT | https://github.com/jprichardson/node-jsonfile |
| lifecycle-utils | 2.1.0 | MIT | https://github.com/giladgd/lifecycle-utils |
| lifecycle-utils | 4.5.2 | MIT | https://github.com/giladgd/lifecycle-utils |
| lodash.debounce | 4.0.8 | MIT | https://github.com/lodash/lodash |
| log-symbols | 7.0.1 | MIT | https://github.com/sindresorhus/log-symbols |
| lowdb | 7.0.1 | MIT | https://github.com/typicode/lowdb |
| mimic-function | 5.0.1 | MIT | https://github.com/sindresorhus/mimic-function |
| minimist | 1.2.8 | MIT | https://github.com/minimistjs/minimist |
| minipass | 7.1.3 | BlueOak-1.0.0 | https://github.com/isaacs/minipass |
| minizlib | 3.1.0 | MIT | https://github.com/isaacs/minizlib |
| ms | 2.1.3 | MIT | https://github.com/vercel/ms |
| nanoid | 5.1.16 | MIT | https://github.com/ai/nanoid |
| node-addon-api | 8.9.2 | MIT | https://github.com/nodejs/node-addon-api |
| node-api-headers | 1.9.0 | MIT | https://github.com/nodejs/node-api-headers |
| node-llama-cpp | 3.22.2 | MIT | https://github.com/withcatai/node-llama-cpp |
| onetime | 7.0.0 | MIT | https://github.com/sindresorhus/onetime |
| ora | 9.4.1 | MIT | https://github.com/sindresorhus/ora |
| parse-ms | 4.0.0 | MIT | https://github.com/sindresorhus/parse-ms |
| path-key | 3.1.1 | MIT | https://github.com/sindresorhus/path-key |
| pretty-bytes | 6.1.1 | MIT | https://github.com/sindresorhus/pretty-bytes |
| pretty-ms | 8.0.0 | MIT | https://github.com/sindresorhus/pretty-ms |
| pretty-ms | 9.3.1 | MIT | https://github.com/sindresorhus/pretty-ms |
| proper-lockfile | 4.1.2 | MIT | https://github.com/moxystudio/node-proper-lockfile |
| rc | 1.2.8 | (BSD-2-Clause OR MIT OR Apache-2.0) | https://github.com/dominictarr/rc |
| require-directory | 2.1.1 | MIT | https://github.com/troygoode/node-require-directory |
| restore-cursor | 5.1.0 | MIT | https://github.com/sindresorhus/restore-cursor |
| retry | 0.12.0 | MIT | https://github.com/tim-kos/node-retry |
| retry | 0.13.1 | MIT | https://github.com/tim-kos/node-retry |
| semver | 7.8.6 | ISC | https://github.com/npm/node-semver |
| shebang-command | 2.0.0 | MIT | https://github.com/kevva/shebang-command |
| shebang-regex | 3.0.0 | MIT | https://github.com/sindresorhus/shebang-regex |
| signal-exit | 3.0.7 | ISC | https://github.com/tapjs/signal-exit |
| signal-exit | 4.1.0 | ISC | https://github.com/tapjs/signal-exit |
| simple-git | 3.36.0 | MIT | https://github.com/steveukx/git-js |
| sleep-promise | 9.1.0 | MIT | https://github.com/brummelte/sleep-promise |
| slice-ansi | 7.1.2 | MIT | https://github.com/chalk/slice-ansi |
| slice-ansi | 8.0.0 | MIT | https://github.com/chalk/slice-ansi |
| stdin-discarder | 0.3.2 | MIT | https://github.com/sindresorhus/stdin-discarder |
| stdout-update | 4.0.1 | MIT | https://github.com/keindev/stdout-update |
| steno | 4.0.2 | MIT | https://github.com/typicode/steno |
| string-width | 4.2.3 | MIT | https://github.com/sindresorhus/string-width |
| string-width | 7.2.0 | MIT | https://github.com/sindresorhus/string-width |
| string-width | 8.3.0 | MIT | https://github.com/sindresorhus/string-width |
| strip-ansi | 6.0.1 | MIT | https://github.com/chalk/strip-ansi |
| strip-ansi | 7.2.0 | MIT | https://github.com/chalk/strip-ansi |
| strip-json-comments | 2.0.1 | MIT | https://github.com/sindresorhus/strip-json-comments |
| tar | 7.5.22 | BlueOak-1.0.0 | https://github.com/isaacs/node-tar |
| universalify | 2.0.1 | MIT | https://github.com/RyanZim/universalify |
| url-join | 4.0.1 | MIT | https://github.com/jfromaniello/url-join |
| validate-npm-package-name | 7.0.2 | ISC | https://github.com/npm/validate-npm-package-name |
| which | 2.0.2 | ISC | https://github.com/isaacs/node-which |
| which | 6.0.1 | ISC | https://github.com/npm/node-which |
| wrap-ansi | 7.0.0 | MIT | https://github.com/chalk/wrap-ansi |
| y18n | 5.0.8 | ISC | https://github.com/yargs/y18n |
| yallist | 5.0.0 | BlueOak-1.0.0 | https://github.com/isaacs/yallist |
| yargs | 17.7.3 | MIT | https://github.com/yargs/yargs |
| yargs-parser | 21.1.1 | ISC | https://github.com/yargs/yargs-parser |
| yoctocolors | 2.2.0 | MIT | https://github.com/sindresorhus/yoctocolors |

## Font

**Source Serif 4** (© Adobe), packaged by Fontsource (`@fontsource-variable/source-serif-4` 5.3.0). It's licensed under the **SIL Open Font License 1.1** (`licenses/OFL-1.1.txt`). It's bundled with Aphrodite and isn't sold on its own.

## MIT, ISC, BSD and similar permissive licences

Each of these packages is © its authors, and its licence text is included in the package's folder inside the installed app (`resources/app.asar/node_modules/<package>/LICENSE`).

| Package | Version | Licence | Source |
|---|---|---|---|
| @types/trusted-types | 2.0.7 | MIT | https://github.com/DefinitelyTyped/DefinitelyTyped |
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

## The assistant's model (downloaded only when you ask for it)

The assistant's model isn't part of the installer. If you turn the assistant on and choose Download, Aphrodite fetches it from the Aphrodite releases page:

- **Qwen3.5-4B** (© Alibaba Cloud; **Apache License 2.0**, `licenses/Apache-2.0.txt`). Source: https://huggingface.co/Qwen/Qwen3.5-4B. Changes from the original: the weights were converted to the GGUF file format and reduced to 4-bit precision (Q4_K_M) by bartowski (https://huggingface.co/bartowski/Qwen_Qwen3.5-4B-GGUF), and the file is split into parts for download and joined again on your computer. Nothing else was changed. Alibaba Cloud and the Qwen team don't endorse Aphrodite.

## Data downloaded while Aphrodite runs (not distributed with Aphrodite)

Aphrodite downloads these lists straight from their publishers. They aren't part of the installer, and they remain under their authors' licences. Our thanks to:

- **EasyList, EasyPrivacy, EasyList Cookie** (EasyList authors; GPL-3.0 / CC BY-SA 3.0), via Ghostery's mirror
- **uBlock Origin filters** (Raymond Hill and contributors; GPL-3.0), via Ghostery's mirror
- **Peter Lowe's blocklist**, via Ghostery's mirror
- **AdGuard Base and URL Tracking filters** (AdGuard; GPL-3.0)
- **malware-filter** phishing and URLhaus lists (curbengh; CC0 / MIT), built from PhishTank, OpenPhish, PhishStats and abuse.ch URLhaus
