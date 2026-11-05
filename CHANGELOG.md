# Changelog

## 2.0.2 (2026-11-05)
- **Aphrodite for Linux.** Official Linux packages (`.AppImage` and `.deb`) now ship alongside Windows on the releases page, with automatic updates for AppImage installs, Linux font fallbacks in Studio, and platform-matched labels.

## 2.0.1 (2026-11-05)
- **What’s new shows the test versions too.** Settings → About now lists the versions from before the public release under their own **Pre-release** heading, below the released ones.
- A refreshed download page with screenshots of each feature.

## 2.0.0 (2026-11-05)
- **First public release.** Aphrodite is a private, calm browser by SolidCarbon Works. It has no accounts, no telemetry and no ads.

### Protection
- **Blocks ads and trackers**, including trackers disguised as a site's own address, and session-recording services.
- **Refuses cookie consent pop-ups** for you, through each site's own menus.
- **Warns about phishing and malware pages and downloads**, using lists kept on your computer. Nothing you visit is sent anywhere.
- **HTTPS-Only mode**, secure DNS, WebRTC IP-leak protection, Global Privacy Control, and removal of tracking tags from links.
- **Fingerprint protection.** Each site gets its own made-up device details, kept for as long as you keep its cookies. Sites can't link your visits to each other, and sites you log in to still recognise your device. The protection reaches frames, popups and every kind of background worker.
- **Bot checks work by default.** Sign-up and login pages that use Arkose, DataDome, hCaptcha, reCAPTCHA or Cloudflare work, and their cookies last only until you close Aphrodite. Pages see a normal browser window around the page, never your real window or a "DevTools is open" gap.
- **Trust this site:** one switch in the shield panel for sites that break. They get real device details and their own analytics, while other companies' trackers stay blocked.
- **Privacy receipts and grades** show what each site tried and what got through. The privacy guide explains every protection in plain words.

### Browsing
- Vertical tabs, workspaces, tab folders, split view, a command palette, reader view, Live clips, session restore and private windows.
- Bookmark import from other browsers, light and dark themes, and **Studio** for restyling every part of Aphrodite.
- Silent automatic updates from SolidCarbon Works' public releases page. No key or account is involved.

### Changes for earlier test versions
- Extensions are no longer supported. Ad blocking, consent refusal and tracker protection are built in.
- Aphrodite is now proprietary software by SolidCarbon Works. See Settings → About → Open-source licences for the parts it's built on.

# Pre-release

Test versions from before the public release, kept as they were written.

## 1.16.2 (2026-11-05)
- **Bot checks stop thinking DevTools is open.** Pages saw a maximised 1920-wide window around a page hundreds of pixels narrower (the real window includes Aphrodite’s sidebar). Security checks, GitHub’s included, read a gap that big as “DevTools is open” and count it against you. Pages now see a normal Chrome window just around the page, centred on the screen, with fingerprint protection on or off, and frames from other sites (like GitHub’s puzzle) report the same window as the page.
- **Sites you return to see the same device.** Made-up device details (canvas, audio, WebGL noise) used to change every launch, so GitHub saw a brand-new device on every visit. Each site now keeps its own made-up device for as long as you keep its cookies, separately in each workspace. Different sites still get unrelated values, and clearing a site’s data, “forget me” and clearing on exit give it a new one. Private windows still get a new one every launch.
- New bot-signal check: what anti-bot scripts see, with shields up, fingerprint protection off and shields down.

## 1.16.1 (2026-11-05)
- **GitHub sign-up completes on a trusted github.com.** Aphrodite still dropped every beacon (background report) on every site, before the trusted-site rule could run, so GitHub never got its own “a person is filling this in” reports and sent you back to sign-up. On a trusted site, beacons to that same site now go through; beacons to other companies stay blocked everywhere.
- The shield panel says so: “Its own analytics are allowed while you trust it” under Trust this site.

## 1.16.0 (2026-11-05)
- **New GitHub accounts stop getting suspended.** Aphrodite was blocking DataDome’s script (`js.datadome.co`, labelled “Unnamed tracker”), the bot protection GitHub uses. With it blocked, a new account creating a repository looked like a bot and was suspended. Bot protection from the whole industry is now recognised: DataDome, Arkose (and GitHub’s octocaptcha.com), hCaptcha, reCAPTCHA, Cloudflare Turnstile, HUMAN/PerimeterX, Kasada, Imperva, Friendly Captcha, GeeTest and MTCaptcha.
- **Bot checks** setting (Settings → Shields): **Allow** (recommended), **Only on sites I trust**, or **Block everywhere**. Change it per site from the shield panel, or flip it for the site you’re on with the new “Turn bot checks on or off for this site” command (Ctrl+K, a shortcut of your own, or one of your buttons). Blocked bot checks show in the receipt as “Bot check: … (sign-ups here may fail)”, and on sign-up and login pages Aphrodite warns before you continue.
- **A trusted site’s own requests are never blocked** (for example GitHub’s `collector.github.com` on github.com). Other companies’ trackers stay blocked there.

## 1.15.0 (2026-11-05)
- **Sign-ups stop getting flagged.** Security checks on sign-up, login and payment pages (Arkose, hCaptcha, Cloudflare, DataDome, PerimeterX) can mistake privacy protection for a bot and suspend new accounts. Now, everywhere:
  - Security-check services are never blocked.
  - They may keep their own cookies inside the sites that use them, and those cookies are deleted when Aphrodite closes, so they can’t build a history of you. Google’s reCAPTCHA stays cookieless (its cookies are your Google account) unless you trust the site.
  - Every frame on a page, security checks included, already gets the same fingerprint as the page.
- **Trust this site** (top of the shield panel): for stubborn sign-ups, logins and payments, that one site and the frames inside it see your real browser and may use their own cookies. Ads, trackers, link cleaning and HTTPS stay on. On a sign-up or login page, or when a “verify you’re human” check appears, Aphrodite offers it once per site per session (turn the offer off in Settings → Shields). Trusted sites are listed under “Sites with their own settings”.
- The shield panel’s notes for a row sit on their own line, and on a trusted site the real-answers note is calm instead of a warning.
- A new tab puts the cursor in its search box and keeps it there, even after the page redraws its numbers.
- Smoke: trusting a site (real values after a reload, trackers still blocked), the shield panel switch, which services count as security checks and which may keep cookies, and recognising sign-up pages.

## 1.14.3 (2026-11-05)
- **Clips survive a lost connection.** A page that doesn’t load (no internet, site down, timed out, a server error) no longer makes a clip say “can’t find it”: it keeps its last value and shows it as offline, quietly (a hollow dot, no red). While Windows reports no network, checks pause. When the connection is back, waiting clips are checked within about 20 seconds; a site that didn’t answer is tried again after 2 minutes instead of at the clip’s next turn.
- The shield panel says **Got some real answers** with a link to the receipt, instead of listing every one.
- Smoke: a clip on a site that goes down and comes back; the saved-asleep check waits for the session file instead of a fixed time.

## 1.14.2 (2026-11-05)
- The tab menu says **Put this site to sleep**, **Never put this site to sleep** and **Let this site sleep again**, without the site’s full name.
- The shield panel’s count of blocked trackers sits level with its two-line label instead of hanging below it.

## 1.14.1 (2026-11-05)
- The right-click item is now simply **Live Clip**.
- The IP button no longer seems to grow when you reveal your address: it keeps the same size and look, with the stars (or your address) first and the eye at the very right.
- **Studio knows the new parts**: live clips (shelf, tiles, values, changes, the board, cards, graphs, the clip dialog), sleeping tabs, your own buttons, the controls button and panel, and the IP text. They’re in Interface CSS’s list of every part (now 145) and the picker.

## 1.14.0 (2026-11-05)
- **Live clips**: keep any part of any page live. Right-click a price, a score, a status, a chart (or press Alt+C) and choose **Clip this part of the page**. Point at it, use ↑ ↓ to make the selection bigger or smaller, and click. Name it and choose how often to check it (every minute to every 3 hours).
  - Clips sit in a new **shelf in the sidebar**, under Downloads, and on a **board on the new tab page** (drag cards to arrange them). Choose either or both.
  - Text clips show the value, how far a number moved since last time, and a **graph of its history**. Picture clips keep a fresh image of that part of the page.
  - Aphrodite checks each clip in a hidden window with shields on, waits for parts that load late, then closes the page. Clips on the same page share one visit. A changed clip glows until you look at it, and can send a **Windows notification**.
  - Each clip checks **as you** (your logins, for your orders or notifications) or **anonymously** (no cookies or logins, so the site can’t tie the visits to you). Clip checks don’t count as your visits in receipts.
  - If a site is redesigned and the part disappears, the clip says so and offers to pick it again. Click a clip to open its page with the part highlighted; right-click for its options.
  - Our scripts run in an isolated world on the page, so the page can’t read or tamper with them. Clips are never made in, or shown in, private windows.
- Settings: **Search** and **Shortcuts** now come right after General, so the privacy sections follow each other without a break.
- **Sleeping tabs stay asleep after a restart**, and pinned tabs show when they’re asleep (faded, with a dashed outline).
- While your IP is hidden, the toolbar shows `***.***.***.***` instead of “IP”.
- Smoke: picking, adding, refreshing, change and history, the board keeping what you type, as-me vs anonymous visits, late-loading parts, picture clips, a redesigned site, and the settings order, saved sleep and IP mask.

## 1.13.0 (2026-11-05)
- **Tab sleeping** (Settings → General): a tab you haven’t opened for a while (30 minutes by default; 5 minutes to 2 hours, or never) closes its page to free memory and loads again when you click it. Sleeping tabs look faded with a small moon. The tab you’re on, pinned tabs, tabs playing sound, tabs asking for a permission, tabs with text you typed and haven’t sent, and sites that forget you when closed never sleep on their own. Add sites that should never sleep in Settings or from the tab’s menu, which can also put a tab to sleep straight away.
- **Workspaces with their own look and protection.** From a workspace’s menu, pick one of your saved Studio themes for it and a protection level: Strict (everything on, and sites are forgotten when you close them), Balanced (Aphrodite’s defaults), Compatible (for sites that break: ads and trackers still blocked, fingerprinting and third-party cookies allowed) or your Shields settings. Switching workspace switches both. A site’s own settings still win, and the shield panel says when a workspace sets the level.
- **Shortcut editor** (Settings → Shortcuts): change the keys for any command (with a reset button), and give one key to one thing only (taking a key moves it and tells you). Make **your own shortcuts** that open a site, run any command, switch workspace, turn one of your CSS styles on or off, or flip one of your switches. Share them as a code (`APHK1.…`). Ctrl+Shift+Alt+M (turn off my theme and styles) always works and can’t be changed. Menus and Ctrl+K show your keys.
- **Your own buttons** (Studio → Buttons & controls): in the toolbar or at the bottom of the sidebar, with an Aphrodite icon, an emoji or your own SVG (drawn as an image, so it can’t run anything). They do the same things your shortcuts can.
- **Your own sliders and switches**, under a new sliders button in the toolbar: drive a CSS variable of yours (a “Blur” slider sets `--my-blur` for your interface CSS, live), or page zoom, text size, sidebar width, corner roundness, your interface CSS or the sidebar.
- **Toolbar examples** for Interface CSS: hide, move or shrink toolbar buttons.
- **Search keywords** in the address bar: `yt lofi beats` searches YouTube, `w Rome` Wikipedia, and `gh`, `r`, `maps`, `amz`, `imdb`, `so`, `mdn`, `ddg`, `b` and `g` come built in. Add your own in Settings → Search with a link that has `%s` where the search goes. The search goes only to that site, and the address bar suggests it first.
- Smoke: keywords, tab sleeping (and what keeps a tab awake), workspace levels and themes, changed and custom shortcuts pressed as real keys, the safety-net key, buttons, sliders, and the new Settings and Studio sections.

## 1.12.0 (2026-11-04)
- **Cloudflare checks work again**, with every protection on. "Verify you are human" no longer loops back after you tick it, and Cloudflare's own check passes without a click, as in Chrome. The causes, all fixed at the root (no exemptions for Cloudflare):
  - Cloudflare's check runs in a cross-site frame, and those sent Electron's own user agent ("… Electron/45.0.0"). The clearance it issued didn't match the page, so every reload got 403. Every frame now sends the same plain Chrome user agent.
  - `Accept-Language` was malformed (`en-US,en;q=0.9;q=0.9`); it is now `en-US,en;q=0.9`, as in Chrome.
  - The fake language list contradicted what Web Workers report, and Cloudflare compares the two. Workers now get the same values (below).
- **Fingerprint protection now reaches everywhere a script can run.** A fingerprint audit found 19 problems; all are fixed or listed under Honest limits in the README:
  - Same-origin iframes reached through `window.frames[i]`, `window[i]` or `innerHTML` (not just `.contentWindow`) got every real value. Every frame, and every popup, is now protected before a script can touch it.
  - Web Workers, workers started by workers, shared workers and service workers read your real GPU model, CPU cores, memory, languages and canvas. They now get the same defences, and the same values, as the page.
  - Canvas noise also covers copies through ImageBitmap, VideoFrame and WebGPU. It is tied to each pixel's position, so reading a canvas in tiles or one pixel at a time can't get around it, and a copy can't undo it.
  - Audio worklets get the same inaudible noise as other audio reads.
  - The GPU model is reported without its exact device ID (as WebGPU does) instead of a made-up "Generic Renderer".
  - Fakes that gave themselves away are now realistic: battery reads as a desktop on mains power, the keyboard as US English, speech voices only for the languages you report, the screen with a common taskbar size, Chrome's full version and Windows version as Chrome reports them, and a common storage quota instead of a share of your disk.
  - Patched functions can't be told apart from Chrome's own: no source code from another frame, no `prototype`, the same errors and error stack traces. CreepJS, which looks for exactly this, finds 0 lies (it found 207 before) and no privacy or stealth tool.
  - Solid colour fills and cleared canvases read back exactly, and rendered audio keeps true silence, so the noise only touches what can fingerprint you (text, emoji, curves, images, WebGL, rendered sound).
- **Time zone sites see** (Settings → Privacy, and in the shield panel): your own, **Match my VPN’s location** (the time zone of wherever your IP address appears to be, looked up at startup and every 10 minutes, with a restart offered when it changes) or UTC. Pages and their workers all agree on it. Off by default; applies after a restart.
- **Hide window size and position** (on by default): sites see a maximised window on your screen, the same in every frame, whatever your window’s real size and place. Nothing on screen changes.
- **Receipts say what sites got for real, not just what was faked.** “Got made-up answers” and “Got real answers” are listed apart, each real one with the reason: it can’t be hidden by a browser (fonts, graphics card model, cameras and microphones, browser version), fingerprinting or shields were off for the site, a protection switch was off, or your time zone setting. The summary now says, for example, “8 ways: 5 got made-up answers, 3 got real ones” (it used to say every answer was made up, which wasn’t true for fonts).
- Reads are noted even when a protection is off (without changing anything), so the **Leak log** now lists device details a site got because fingerprinting or shields were off, and **Raise shields** fixes them. The shield panel shows “Got real answers: …” at a glance, and a red dot on the shield button flags real answers a protection would have hidden.
- **History and Downloads** open in their own panel beside the sidebar instead of as tabs. Esc or a click outside closes it.
- A window no longer fails to start if an interface event is unknown (seen once as a blank private window during development).
- **Privacy guide** (Settings → Privacy guide): what Aphrodite hides from websites, what it can’t, where each protection reaches, when protections don’t apply, and what every privacy setting does, with each one’s current state.
- **Where fingerprint protection reaches** (Settings → Privacy & security), each on by default: frames and popups, background workers, shared workers, service workers, copies of drawings and audio worklets, and common device details. Turn one off only if a site breaks.
- Privacy receipts now also list WebGPU graphics card queries, storage space checks, font probing, and fingerprinting done from a site’s background workers (reported on a channel that’s secret for each launch, so a page can’t fake or read it).
- Pages get `chrome.app`, `chrome.csi` and `chrome.loadTimes` as in Chrome, instead of an empty `window.chrome`.
- **Electron 45** (Chromium 156).
- **Leak log** (Settings): trackers and third-party cookies that got through while shields were down or a protection was off, per site and company, with a Raise shields button. Recorded without blocking anything.
- **Studio**: an interface picker with Pause and Done, 121 named parts you can open and pick, custom drop-downs and colour picker, more fonts, colours and type options, Layout and New tab sections, wallpaper, 13 presets, search, and a pinned title and menu.
- Tab name animations: typewriter (default), pencil or slide.
- The lock button opens a panel with the site’s permissions; Settings groups permissions by site and keeps them current. Notifications fixed (origin mismatch, one-time answers).
- Home keeps showing until the new page arrives; the light/dark jump is fixed. A perfect score gets an S grade.
- Search on Settings and Studio no longer shifts the page sideways.
- Smoke: a fingerprint audit (every route above, on a local test site) runs on every `npm run smoke`, plus checks that DevTools still opens, receipts list real answers, the Leak log records them, and History and Downloads open in their panel. Opt-in: `SMOKE_ONLY=cfdebug,cloudflare` (Cloudflare) and `SMOKE_ONLY=sites` (CreepJS, BrowserLeaks, Cover Your Tracks, and worker-heavy apps).

## 1.11.0 (2026-11-04)
- **Studio**: a new page for making Aphrodite yours. Open it with the palette button next to Settings, from the menu, or with "Studio" in the command palette. Everything shows live as you change it and is kept in your profile, so updates never undo it.
  - **Theme**: seven presets (Aphrodite, Sage, Harbor, Plum, Rosewater, Graphite, Typewriter), your own accent colour, and a separate dark-mode accent if you want one.
  - **Every colour**: each surface and text colour, for light and dark mode, with a live mini preview. Borders and hover shades follow your text colour.
  - **Shape & type**: corner roundness, sidebar width, text size, and fonts for headings and for the interface.
  - **Your themes**: save themes to switch between them, share one as a code (`APH1.…`), and paste a code to use someone else's. Codes hold only colours and numbers, and every value is checked.
  - **Site styles**: your own CSS for any website, or every website at once. Each one can be switched on and off, and changes reach open tabs straight away.
  - **Interface CSS**: restyle Aphrodite itself, with examples to start from.
- Styles can't load anything from the internet: `@import` and web addresses in `url()` are removed, including ones hidden with CSS escapes. A shared style can't be used as a tracking pixel.
- **Safety net**: if a theme or style makes something unusable, press Ctrl+Shift+Alt+M (or use "Turn off my theme and styles" in the command palette) to turn everything off at once. Starting Aphrodite with `--no-mods` skips it all for that session.
- The window's title-bar strip now takes the window's real colour, including your Studio theme and the daily papers.

## 1.10.0 (2026-11-04)
- **Daily papers**: the light theme follows your day. From 5:00 to 10:00 it's crisp, fresh paper; in the evening it turns warm cream with soft brown ink, like a book under a lamp, until 5:00. The change fades in over a few seconds, and the window's title bar and reader view match. Choose when the morning paper starts (04:00 to 10:00, it lasts five hours) and when the evening paper starts (16:00 to 23:00), preview either one with the Morning and Evening buttons, or turn papers off in Settings → General. Dark mode is never changed.
- **Smoother motion**: when the sidebar folds, its labels fade out first, and when it opens they slide back in. Switching tabs settles in instead of snapping. Menus and panels (shield, IP, menu) open with a gentle lift and fade out when closed. Dialogs and toasts ease in.
- **Animations switch** in Settings → General turns all interface motion off. Motion is also always off when Windows is set to reduce motion.

## 1.9.0 (2026-11-04)
- **What changed since your last visit**: when you come back to a site after six hours or more, Aphrodite tells you what's new. That covers tracking companies it never had before, new fingerprinting or disguised trackers, more ad partners holding your consent (for example 212 → 247), and an edited privacy policy, quoting a new paragraph. The policy is re-read at most every 3 days, straight from the site, without cookies or logins. Changes are also kept under each site in Cookies & site data. You can turn this off in Settings → Privacy & security.
- **Sites you said yes to**: a new Settings section listing every site whose cookie pop-up holds a "yes" from you, with the uses and ad partners it covers. **Withdraw** (or **Withdraw everywhere**) deletes only that answer, so you stay signed in. On your next visit the pop-up asks again and Aphrodite refuses it. Answers kept in local storage are removed before the page's scripts can read them.
- **Grade before you click**: point at a link to a site you've visited and a small badge shows its privacy grade, from the receipts on this computer. Nothing is looked up. You can turn it off in Settings → Privacy & security.

## 1.8.1 (2026-11-04)
- The shield's count shows a dash on new tabs, Settings and other built-in pages (and when shields are down), and 0 on a website where nothing was blocked, instead of an empty space.
- Who follows you: a little space between an expanded company and its list of sites, so the two grey backgrounds no longer touch.

## 1.8.0 (2026-11-04)
- **Changelog in About & updates**: when an update is found you see what's new in it before installing, and every earlier version's changes are listed below.
- The privacy grade badge is always there: before you open a website it shows a plain grade icon in the same spot.
- The toolbar no longer shifts: the grade, the shield count and the IP button keep fixed sizes, so a new letter, a bigger count or showing your IP doesn't push the address bar around. Long IPv6 addresses are shortened (hover for the full address).
- Fixed receipts counting the previous page's requests: beacons a page sends as you leave it (DuckDuckGo's, for example) were filed under the next site you opened, and could make a company look like it followed you there.
- DuckDuckGo's own usage pixels are now named ("DuckDuckGo usage pixel, anonymous usage counts").

## 1.7.0 (2026-11-04)
- **Privacy grade**: a letter from A to F next to the shield says how hard the site you're on tries to track you: the companies it uses, session recording, data brokers, fingerprinting, disguised trackers, ad tracking. It counts what Aphrodite blocked too. Click it for the reasons.
- **Who follows you**: a new Settings section showing which companies' trackers appeared on more than one site you visited ("Google: on 9 of 14 sites"), with the sites listed. Built from the receipts on this computer.
- **Permission audit**: a new Settings section listing every permission sites asked for (camera, microphone, location, notifications and more), your answer, and when it was last asked or used. Forget an answer to be asked again.
- Remembered permission answers now last until you forget them, instead of until Aphrodite closes. Private windows still keep nothing.
- **What websites see**: an "IP" button in the toolbar, hidden by default. Click it to see your public address, provider and rough location, whether it looks like a VPN, proxy or data centre (or Cloudflare WARP), whether your clock's time zone gives a VPN away, and whether WebRTC is protected. The lookup only runs when you ask: it contacts Cloudflare and ipinfo.io and sends nothing else.

## 1.6.1 (2026-11-04)
- Cookies & site data now includes sites you still have open. A page's receipt used to appear only after you left it, so long visits (YouTube, for example) never showed up.
- Smoother scrolling in the receipt and other popover lists: they now scroll on the GPU instead of being repainted at every step, which lagged over playing videos. The shield count's bump no longer forces the whole window to re-layout.
- The receipt's total is split in two: requests stopped, and fingerprinting answers faked (those aren't blocked, they get made-up values).
- YouTube's generate_204 ping is now named ("Google usage ping") instead of "Unnamed tracker".

## 1.6.0 (2026-11-04)
- **Receipts list every tracker**: under each company the receipt lists each tracker on its own line: what it is (Google Analytics, Sentry, Meta Pixel, PostHog's session recording, click tracking and event logging, and about 45 more), what it's for (advertising, analytics, session recording, error monitoring…), the address it called and how (script, data request, beacon, pixel). Unknown trackers are labelled by purpose from their address, such as "Analytics endpoint".
- **Receipts are kept per site**: Cookies & site data now shows, for each site, everything it tried across your visits: trackers by company, disguised trackers, fingerprinting attempts and refused cookies. Kept on this computer only, never for private windows, and deleted with the site's data.
- Fixed the "A JavaScript error occurred in the main process … assert(!this.paused)" window for good: every download in the app, including the extension store's (installs, icons, update checks), now goes through the browser's own network stack. 1.5.1 had only moved the filter lists.
- Cookies & site data: the time and the arrow sit in fixed columns, so times line up whether a row expands or not.

## 1.5.2 (2026-11-04)
- Fixed Cloudflare and other bot checks treating Aphrodite as a bot: it now sends the brand headers (Sec-CH-UA) that Chrome sends on every secure request, matching what pages read from the browser. They were missing because Aphrodite sets its own plain user agent.
- The publisher name now shows in Windows' installed-apps list and the program's file details.

## 1.5.1 (2026-11-04)
- Fixed an error window ("A JavaScript error occurred in the main process … assert(!this.paused)") that could appear while filter lists updated. Filter lists and the ad-partner list now download through the browser's own network stack instead of Node's, which had the bug.

## 1.5.0 (2026-11-04)
- **Privacy receipts**: the shield panel's new Receipt button explains what happened on the page in plain words. It names the companies whose trackers were blocked, any trackers disguised as the site, third-party cookies refused, each fingerprinting attempt (and which script made it), skipped redirect trackers, cleaned links, HTTPS upgrades, what happened with the cookie pop-up, and which ad partners have your consent. It can be copied as text.
- **Your week**: on built-in pages the shield shows the last 7 days: trackers blocked, fingerprint reads faked, cookies refused, pop-ups rejected, and the companies that tried hardest. All counted on this computer.
- **Separate logins per workspace**: a workspace can keep its own cookies and sign-ins (tick it when creating one, or use the workspace menu). You can use a second account there, and sites can't follow you between workspaces. Turning it off or deleting the workspace deletes its sign-ins. Extensions only run in workspaces that share logins.
- **Many more consent platforms understood**: Cookies & site data now reads Osano, TrustArc, Usercentrics, iubenda, Klaro, Borlabs, Civic Cookie Control, Axeptio, tarteaucitron, CookieFirst, Ketch, Shopify, Wix, HubSpot, CookieConsent, CookieHub, Cookie Information, Cookie Notice, GDPR Cookie Consent (CookieLawInfo), Moove, Ensighten, Google's Additional Consent and the US Privacy string, as well as the previous formats. Consent kept in local storage is read through the page's standard TCF / US-privacy API.
- **Named ad partners**: instead of only "212 ad partners", the site details list who they are (Google, Criteo and so on), from the public IAB vendor list, which is downloaded at most weekly and holds no data about you. Didomi purposes now show readable names.
- Site data covers every workspace: the list says which workspace stored a site's data, and deleting removes it from all of them.
- **YouTube works again with ad blocking on, without ads**: uBlock Origin's page fixes (scriptlets) now run together as one script, as in uBlock itself. Run one by one, they wrapped each other until YouTube's player crashed ("Maximum call stack size exceeded"). Ad slots on YouTube pages (home, search, sidebar) are hidden too.
- **Stronger ad blocking**: AdGuard Base is added to EasyList, EasyPrivacy, Peter Lowe and uBlock Origin's lists. The ad lists now refresh daily instead of weekly, so fixes for sites like YouTube arrive faster.
- Friendlier buttons: a soft press on every button, toolbar icons that hint at what they do (back nudges left, reload turns, the star tilts), and switches that squish as you toggle them. Turned off when Windows asks for reduced motion.

## 1.4.1 (2026-11-03)
- **New logo**: the "Petal A", two leaning petals that form a soft A, replaces the scallop shell on the new tab page, internal pages, the window and taskbar icon, and the installer.
- New-tab shortcuts show each site's real icon, loaded straight from the site with no referrer (no third-party icon service). The letter badge stays as a fallback and is still used in private windows.

## 1.4.0 (2026-11-03)
- **Chrome extensions**: install from the Web Store page, a store link, a .crx/.zip file or a folder; toolbar buttons and popups; right-click menu items; an Extensions page (menu or Ctrl+K).
- **Extension protections**: a plain-language permission warning before every install; site access limited to chosen sites (enforced); off in private windows unless allowed; no automatic contact with Google (manual "Check for updates"); a hint when an extension duplicates Aphrodite's ad blocking.
- Fixed a crash ("Object has been destroyed") when tabs closed with extensions loaded.

## 1.3.0 (2026-11-03)
- **Phishing and malware protection.** Known scam and malware pages are stopped with a warning page, and dangerous downloads are blocked. Uses PhishTank, OpenPhish, PhishStats and URLhaus lists (via malware-filter) plus uBlock's badware list, stored on this computer and refreshed twice a day, so no address is ever sent anywhere. Can be turned off in Settings → Privacy & security.
- **Workspaces**: separate tab sets (Work, Study…) with their own colour, pinned tabs and folders. Switch from the sidebar header, the dots at the bottom, the command palette, or Ctrl+Alt+←/→. Move tabs between workspaces from the tab menu.
- **Tab folders**: group tabs in the sidebar; collapse, rename, ungroup, or close them together. Drag tabs onto a folder to add them.
- **Bookmark import** from Chrome, Edge, Brave, Vivaldi, Opera, Firefox, Zen and LibreWolf on this computer, or any bookmarks HTML file (Settings → Your data).
- **What you consented to**: Cookies & site data now decodes each site's consent cookie (IAB TCF, OneTrust, Cookiebot, Didomi, CookieYes, Cookie-Script, Complianz) to show which uses you allowed or refused and how many ad partners got consent.
- **Update progress**: a live download toast with percentage, size and speed, then "ready to restart".
- The Settings menu now highlights the section you've scrolled to.

## 1.2.1 (2026-11-03)
- Updates install silently in the background: "Restart now" no longer opens the installer wizard. Aphrodite closes, updates and reopens by itself.

## 1.2.0 (2026-11-03)
- **Home button** (and Alt+Home) shows the start page in the current tab. Back returns to the page you were on, still loaded.
- **Split view with tabs you already have open**: the split button (Ctrl+\) asks which tab goes beside this one. You can also drag a tab from the sidebar onto the page, or type "split" in the command palette.
- **More greetings** on the new tab page, matched to the time of day and the day of the week, using your name when it's set in Settings.
- The new-tab **+** now spins around its exact centre (it sat on a half pixel before).

## 1.1.1 (2026-11-03)
- Automatic updates.
- Clearer update error messages (expired key, offline, nothing released yet).

## 1.1.0 (2026-11-03)

### Privacy
- **Cookie consent pop-ups are rejected automatically** (DuckDuckGo autoconsent rules), including multi-step "manage options" menus. Can be set to accept, hide or leave alone, globally or per site. Leftover or unknown banners are hidden.
- **Per-site controls** in the shield menu: ads & trackers, cookie pop-ups, fingerprinting, third-party cookies, link cleaning, HTTPS upgrade, block scripts and "forget me", each changeable for one site.
- **Forget me when I close this site**: deletes the site's cookies and storage shortly after its last tab closes (per site, or for every site).
- **Cookies & site data manager** (Settings): every site that stored data, its cookie count, what happened with its consent pop-up, and per-site or full deletion.
- **CNAME uncloaking**: first-party subdomains are resolved over encrypted DNS and blocked if they really point to a tracker.
- **Redirect-tracker skipping** (debouncing) for Google, Facebook, Instagram, Reddit, YouTube, LinkedIn, Steam, Slack and others.
- **Stronger link cleaning** with AdGuard's URL-tracking list (thousands of `$removeparam` rules), plus "Copy clean link".
- **Stronger fingerprinting defences**: same-origin iframes can't be used to grab untouched APIs; screen and window metrics, WebGL pixel reads, OffscreenCanvas, audio copies and speech voices are now covered.
- Downloads get the Windows "Mark of the Web", so SmartScreen checks them; executables ask before opening.

### Browser
- Session restore (tabs come back after a restart; background tabs load when opened).
- Pinned tabs, split view (drag the divider), command palette (Ctrl+K), reader view (F9), downloads page (Ctrl+J).
- Automatic updates from GitHub releases, which can be turned off in Settings → About & updates.

## 1.0.0 (2026-11-03)
- First release: ivory-and-terracotta interface, ad & tracker blocking, cookie-banner hiding, HTTPS-Only, fingerprint randomisation, third-party cookie blocking, tracking-parameter stripping, secure DNS, WebRTC protection, GPC, private windows, delete-data confirmations.
