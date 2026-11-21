# Changelog

## 3.2.3 (2026-11-21)
- **Fixed:** your Studio theme icon now stays on the pinned taskbar, Start menu and desktop shortcuts after closing Aphrodite, even when Windows had a shortcut locked or you closed right after switching themes.
- **Fixed:** changed live clips in the sidebar now use a concentric corner curve that matches the clip shelf around them.

## 3.2.2 (2026-11-21)
- **Fixed:** download cards stay anchored in the bottom-right corner as they update instead of jumping to the top right.
- **Fixed:** live clip cards on the new tab page now keep a fixed height with smoother rounded corners, and long previous values in the footer truncate cleanly on one line.
- **Fixed:** choosing **Quiet: nothing shows** under **Studio → Highlights → Changed live clips** now removes all border, fill and dot highlights on changed clips.
- **Fixed:** pinned taskbar, Start menu and desktop shortcuts now keep smooth, sharp edges for your Studio theme icon while Aphrodite is closed.
- **Shorter, cleaner descriptions.** Removed redundant explanation lines across tab sleep tooltips, update notices and settings.

## 3.2.1 (2026-11-21)
- **Fixed:** long hover tooltips near the right edge of the window no longer cut off mid-word and shift inward to fit on screen.
- **Fixed:** the **What websites see** pop-up now closes when you click elsewhere on the page, press Esc, or switch windows.
- **Fixed:** toggling **Show** / **Hide** on your IP address no longer shifts the separating dots or digits.
- **What’s new stays visible under Status.** Clicking **Later** on an update keeps the new version’s feature list and action button under **Settings → About & updates → Status**.

## 3.2.0 (2026-11-21)
- **A second logo mark in Studio.** In Studio → Layout → Logo mark, you can switch between **Petals (Aphrodite)** and **Twin capsules** across the sidebar, tabs and built-in pages.
- **Downloads live in the bottom-right corner.** Running, paused, finished and interrupted downloads now show in a compact bottom-right card with a bottom progress line, an icon that morphs smoothly between states, and icon buttons (Pause, Resume, Retry, Open file, Show in folder, Cancel, Dismiss). Interrupted downloads show a warning triangle badge.
- **Quieter notices in the top-right corner.** Browser notices now share one card layout that unfolds from and folds back into the top-right corner, while downloads sit separately at the bottom right.
- **Custom hover tooltips.** Pointing at toolbar and sidebar buttons shows a dark capsule tooltip with keyboard shortcuts styled as key badges.
- **Live clips and the hidden IP pill.** Live clips sit in a compact paper shelf in the sidebar and show smooth trend lines and the previous value (`Was …`) on the new tab page. The hidden IP address in the toolbar now shows centered dots (`•••.•••.•••.•••`) that match the height and position of the shown address.

## 3.1.0 (2026-11-20)
- Fixed overlapping address text when another window covers Aphrodite while the URL is selected.
- **VPN extensions work.** Browser "VPN" extensions route your browsing through their own servers (they're proxy switchers, not VPN apps). The first time one wants to, Aphrodite asks you, naming the servers: **Let it route your browsing through its servers?** Your answer is remembered for that extension.
- **You can see it and take it back.** While one is active, the shield panel says **Your traffic goes through** that extension, and its card on the Extensions page shows **Routes your browsing through its servers**. The ✕ there goes straight back to a direct connection, and the extension asks again next time.
- **It stays on across restarts,** as in Chrome. Aphrodite puts it back as it starts, before it opens your tabs. If restoring the proxy fails, requests wait instead of going direct. Turning the extension off, switching it off for a workspace or removing it goes back to a direct connection; turning it on again brings its proxy back.
- **Signing in to its servers** works: only the extension that set the proxy is asked for its own servers' sign-in, never for a site's.
- **Fixed: a click in an extension's popup could be lost.** When an extension's background had gone idle, a button in its popup (a VPN's Connect, for example) sometimes did nothing. Its background now keeps running while its popup, side panel or options page is open.

- Extension background workers now receive local storage changes from their workspace, including changes made by a popup and the worker's own writes. Browsec uses these notifications to apply its routing settings.
- Local Firefox XPI installers show whether Mozilla signed the package. Aphrodite verifies supported signatures offline and rejects changes to the signed files.
- Extensions with host access and blocking web-request permission can edit supported HTTP request and response headers. Aphrodite still applies its privacy rules afterward.
- Developer mode includes an **Inspect worker** console for each enabled workspace, with a line breakpoint and a Resume control. Background workers now receive install, update and startup notifications.

### Privacy and security
- **One extension at a time** controls the proxy in a window or workspace; another is told so and can't take over.
- **Your shields keep working behind it:** the checks that stop sites reaching your computer or home network through a proxy are on from the moment it's set. Aphrodite also tests, as it does for VPN apps, whether its servers refuse names that lead to your network.
- **What isn't allowed:** automatic proxy discovery (anyone on your network could answer it), proxy scripts fetched over plain HTTP, and server addresses Aphrodite can't check. Firefox's per-request proxying isn't available: such an extension shows an error instead of looking connected while your browsing goes direct.
- **With Prevent WebRTC IP leaks on** (the default), video-call features may only connect through the proxy. If you turned it off, the shield panel says that your real address can still show.

## 3.0.0 (2026-11-19)
- **Extensions are back, Chrome and Firefox.** Add them from the Chrome Web Store (its button reads **Add to Aphrodite**) or Firefox Add-ons (Aphrodite offers it on an extension's page), from a .zip, .crx or .xpi file, or from a folder, your own or one from GitHub. Before anything is added, you see in plain words what it will be able to do, the most serious first, and whether a store has checked it.
- User-script managers can keep a connection open between a script and its extension. A saved Tampermonkey script now runs again when you reload its page.
- Tampermonkey can register its script-install redirects and open a confirmation window with Install and Cancel when you follow a supported script link.
- Extensions receive history-removal notices only for sites they can see. Download cleanup respects date and size filters and refuses unsupported filters before removing any entries.
- Clearing one kind of extension site setting preserves its other settings. An extension's temporary network rules survive opening it in another workspace.
- An extension's side panel reports its position even while the window is covered. Tab recording shows as pending until capture starts, and the red dot appears when the tab is being captured.
- **You choose where each one runs:** every site, every site except some, only on some, or only when you click it. **Turn off on this site** is in the shield panel, in the toolbar and on its card.
- **A puzzle button in the toolbar** lists your extensions, grouped by what each can do on the site you're on: can read and change it, waiting for your click (**Give access**), turned off here (**Turn on**), or doesn't need it. Pin one to give it its own button, with its badge; its popup opens right under it. Each has a ⋯ menu, and a right-click on its button, for Options, Turn off on this site, Unpin and Remove.
- **The Extensions page** (Manage extensions, or the command palette) shows a card for each: where it came from, where it runs, which workspaces have it, the programs it may start, what it can do and **what it contacted**. Developer mode reloads an extension from its folder, by itself when you save a file there.
- **Extensions can do more than Electron allows by itself:** network-rule blockers (such as uBlock Origin Lite), cookie editors, screenshots and eyedroppers (a picture of the visible tab), reading aloud, keeping the computer awake, settings saved for syncing (kept on this computer), more control of tabs and windows, and rounded facts about the computer.
- **Extensions' own pages inside Aphrodite:** one can be your new tab page (a notice the first time offers Undo, and its card switches it), show a panel docked beside the page, or answer a keyword you type in the address bar.
- **Screen and tab recorders, page savers and sign-in:** an extension may record your screen or a window you choose in Aphrodite's own picker, record a tab after you allow it (a red dot shows on the tab, and Stop recording is in its menu), save whole pages (asked the first time), and open sign-in pages in a window that names the site.
- **Extensions that work with your browser data:** bookmark managers (on Aphrodite's bookmarks), history and most-visited tools, recently closed tabs, downloads managers, cleaners, search, and user-script managers such as Tampermonkey and Violentmonkey.
- **Check for updates** asks the stores about your extensions only when you press it. An update that wants more access shows what's new first; you can keep the version you have.
- **Block other sites' scripts.** A gentler choice beside Block scripts: a site runs its own scripts, and scripts from other companies' servers are held back, even ones no blocklist knows yet. On in Strict workspaces, per site from the shield button, which also lists what was held back so you can allow a source for that site. Each site on shared hosting (like github.io) counts as its own, and space anyone can rent from a cloud company doesn't count as that company. Pages embedded from other sites (videos, maps) still run their own built-in scripts.

### Privacy and security
How extensions are kept in check:
- **Their own connections go through your shields:** dangerous and tracking addresses are refused, plain HTTP is made secure, and **they can't reach your computer or your home network** unless their own list names an address there.
- **Harder for sites to spot your extensions:** each install gets an ID of its own, so sites can't look for it by its well-known one (except extensions from the Chrome Web Store that talk to a program on your computer, which need their real ID; one added from a file always gets its own), and a site you turned an extension off for can't load its files.
- **Packages are checked:** Chrome packages must be properly signed, files from Firefox Add-ons must match what Mozilla states, and files that try to reach outside their folder, links and zip bombs are refused. An extension whose files change on your computer is turned off until you say so.
- **"Turned off on this site" holds:** an extension can't run scripts on a site you turned it off for, also through frames of that site inside another page or while a tab is being redirected there, and it can't contact it.
- **Updates that reach further always ask,** compared site by site and permission by permission, and files changed on your computer can't be accepted by changing an extension's settings.
- **Extensions' network rules come after your shields:** they can block more, but never let through anything Aphrodite blocked, and they can't remove its privacy signal or its cookie protection.
- **Cookies only where allowed:** an extension sees and changes cookies only on sites it can reach, never on a site you turned it off for.
- **Recording asks every time,** and each yes allows one recording. A sign-in code meant for an extension is caught by Aphrodite and never sent anywhere else.
- **Your data, your yes:** an extension asks the first time it wants to delete history or browsing data, open or delete downloaded files, or make sites stricter. It can never loosen a site's settings or change privacy settings, and it never sees private windows.
- **Nothing is synced:** settings an extension saves for syncing stay on this computer. Facts about the computer are rounded so they can't single you out.
- **Extensions are disabled in private windows.** In workspaces with their own logins, you switch each extension on separately.
- **Some permissions are never given**, such as full control of pages (debugger) and routing your traffic elsewhere (proxy). Starting a program on your computer, or asking for more access later, needs your yes first.
- **Stores are contacted only when you ask**, with no cookies or sign-in, after a notice saying what they'll see. Extensions are never updated by themselves.

## 2.22.0 (2026-11-18)
- **Every version in one list.** Settings → About & updates shows this version's changes in full, and every earlier one, test versions included, under **Previous versions**: a line each that opens its notes.
- **Style the newest parts.** Interface CSS's list of every part now includes the assistant, the privacy receipt, What this site saw, update notes and the changelog. Its examples show how to style light mode and dark mode separately.
- **Easier to read: What this site saw.** The two hidden drawings sit one above the other at full size, instead of side by side at half size.
- **Disguised trackers are remembered.** Once caught, a tracker hiding behind a site's own address is blocked at once on later visits, without asking DNS again. The first check waits longer for its answer, and says so when it takes a while.
- **Tidier Settings and Studio.** Their side lists group sections under headings. Controls you rarely need are folded away: where fingerprint protection reaches (Privacy & security) and fine-tuning of type (Studio). In Studio, the menus and buttons on each card line up at the width of the longest one. The Privacy guide's labels share one width, and "When you use it" now reads "On use only".
- **Fixed:** after you switched between light and dark, a pinned taskbar icon could keep the old theme's colours while Aphrodite was closed.

### Privacy and security
After a full review of Aphrodite's privacy protections:
- **Update checks carry no identifier.** Every copy of Aphrodite now sends the same update request, and the ID the update system used to keep is deleted.
- **Your computer's network addresses stay private** from pages and their background workers.
- **Asked first, also by name.** A website that sends you, by a link, a script or a form, to an address that leads to a device on your network now stops and asks, also when the address is a name rather than numbers.
- **Video-call features can't reveal your IP address in any window**, including hidden ones and pop-ups.
- **No advertising features in pages.** Topics, ad auctions, ad-interest groups, attribution reporting, shared storage and fenced frames are all switched off.
- **Third-party cookie blocking is stricter.** Embedded companies can't reach cookies by script or start background service workers, and a page can't change which site counts as the one you're on.
- **Stronger fingerprint noise,** on more ways of reading drawings, 3D graphics and sound. Plain shapes now read back exactly, as in Chrome. Your graphics card is reported by its family only, without its model number. Mouse positions follow the made-up window, and pages see the same date and number formats whatever language your computer uses.
- **Web pages saved on your computer** get the same fingerprint protection as websites.
- **Private windows keep nothing,** not even counts or the choices you make in them, and each one gets its own made-up device.
- **Save browsing history off** now writes no visit at all, and **Clear history** also removes visit times and receipts.
- **Clear data when Aphrodite closes** also happens after Windows shuts down with Aphrodite open: at the next start.
- **Forget me** also deletes a site's cached files, and what other companies stored inside it.
- **The assistant's engine** runs with every way to the network closed, checked on every build. A page can no longer pretend its text has ended.
- **Redaction** also removes form fields on a redacted page, and the bookmark list. **Clean hidden details** also removes commenters and the camera and place of photos inside Word and Excel files.
- **Remembered signatures** are stored encrypted. A Studio style can't load anything from the internet, however it's written. Opening Settings no longer copies another browser's history to look for bookmarks.
- The privacy policy and the Privacy guide now list every connection Aphrodite makes by itself, and say plainly what stays visible to sites.

## 2.21.0 (2026-11-15)
- **See what’s new before you update.** When Aphrodite finds an update, a window lists what’s new in it. With automatic updates off, it downloads only when you press Download.
- **Fixed:** with automatic updates off, Check now still started downloading a found update, and a downloaded update installed itself when Aphrodite closed.

## 2.20.0 (2026-11-15)
- **The assistant knows Aphrodite's own pages.** On Settings she knows which section you're looking at: ask her to sum it up, or what a setting there does, and she answers from your settings as they are now. On Downloads and History she says what the page is for, with counts; she's never told which sites you visited.
- **Ask whether a setting is on.** "Is fingerprint protection on?" gets a straight answer with the setting's name and where to find it, including when a site has its own value or its shields are down.
- **She knows her way around.** Ask where the command palette, Studio or any button is, or how to hide the sidebar.
- **New chats start sooner.** Every other new chat used to make the assistant read her instructions again first.
- **Fixed:** the assistant named the wrong Settings section for Block local network access, Unmask disguised trackers and Skip redirect trackers.
- **Fixed:** "where is…" questions, and questions matching a long help article, could get no help text.

## 2.19.1 (2026-11-15)
- **Fixed:** in the installed app, the assistant couldn’t use a graphics chip or a graphics card, so Speed on this computer only offered the processor.
- **Fixed:** on the model cards in Settings → Assistant, “In use” now sits where the Use button is, so nothing moves when you switch models, and Speed on this computer is laid out more evenly.
- **Fixed:** asked about the page while Settings or another Aphrodite page was open, the assistant could answer about something unrelated instead of saying she can only read websites.
- **Fixed:** the assistant could show her own draft before her answer, ending in "</think>".
- **Fixed:** the Delete button on a model card turned see-through when you pointed at it.

## 2.19.0 (2026-11-15)
- **Speed on this computer.** New in Settings → Assistant: a speed test times the assistant on your processor and, if your computer has one, on its graphics chip: how long she takes to wake up, to start answering and to start on a page summary, how fast she writes, and how much memory she uses. It recommends the one that suits your computer and says why; you choose where she runs. On some laptops the graphics chip starts her answers several times sooner.
- **The assistant wakes up much sooner.** She keeps her instructions ready on this computer instead of reading them again each time she starts.
- **A timer while she gets ready.** The assistant's window counts the seconds while she wakes up, reads the page or thinks.
- **The model is chosen in Settings → Assistant.** The assistant's window no longer has its own model menu.
- **Today's briefing from the command palette.** The sun button is no longer in the sidebar: once the daily briefing has shown, **Show today's briefing** in the command palette (Ctrl+K) opens it again for the rest of the day.
- **Fixed:** after a few questions, a new chat could make the assistant slow to answer again.

## 2.18.1 (2026-11-14)
- **Quicker assistant replies.** Opening the assistant gets her ready while you type, and in a chat she only reads your newest message, not the whole conversation again.
- **The assistant's window shows which model is answering.**
- **Fixed:** the assistant could treat the browser information she's given as something you had written.
- **Fixed:** a casual message could get an answer about an unrelated feature.
- **Fixed:** choosing a model in Settings → Assistant now shows the change straight away.
- **Fixed:** asked what she is, the assistant could name the wrong model.

## 2.18.0 (2026-11-14)
- **Ask the assistant about Aphrodite itself.** She now knows your browser: your name from Settings, how many tabs are open and which are asleep or pinned, what the shields have stopped (in total, this week and today), what's on this site's privacy receipt, your settings, and what's kept on this computer. Ask why your daily briefing shows only two things and she tells you which parts had nothing to show, and why (for example, "Save browsing history is off"). She also explains how every protection works, and what it doesn't do, from a help library of over a hundred short articles written for this version. Everything is read on this computer, for that one question, and never leaves it. Private windows tell her nothing about other windows, history or the briefing.
- **She can point you to the right setting.** When a question is about a setting, an **Open Settings → …** button appears under her answer. She can't change settings herself: you click.
- **Answers start sooner.** The assistant no longer re-reads her instructions before every answer.
- **Fixed:** the daily briefing's shield numbers were counted by UTC day, so things blocked just after midnight landed on the wrong day.
- **Fixed:** Settings said fingerprint values change "per session" and ad lists refresh "weekly"; values last as long as a site's cookies, and ad lists refresh daily. The Privacy guide now says a site with shields down still can't reach your computer or home network. The daily briefing's description no longer lists live clips twice.
- **Licence and privacy policy:** the licence (1.4) now names the checks on links you click on websites too, and the privacy policy says how often each AdGuard list is fetched.

## 2.17.1 (2026-11-14)
- **Highlights without the coloured outline.** Studio → Highlights now chooses how things show themselves, not just how the glow looks. **When you type** (search boxes, text fields, menus and the card you chose): Accent outline, Quiet (no colour at all), Soft fill (a faint tint instead of a line) or Lift (rises a little with a soft shadow). **Changed live clips**: Accent outline, Soft fill, Dot only (the card stays plain, only the dot shows it changed) or Quiet. Thickness, strength, colour and the pulse still apply where they fit.

## 2.17.0 (2026-11-14)
- **A daily briefing.** The first new tab of the day greets you in ink, and a panel slides out beside the sidebar, like History and Downloads, with a small still life drawing itself at the top and the day before underneath: websites visited, downloads finished, trackers stopped and cookie pop-ups refused, each with its number counting up. Click a row for its details: the sites you spent most time on, the files you downloaded, what else Aphrodite stopped (with a bar against your usual day). Below come the live clips that changed, one per line with how much they moved, and the page to pick up where you left off. A row only shows when there's something to say, and it all comes from what's already on this computer. Close it with Esc; the sun button at the bottom of the sidebar opens it again for the rest of the day. Turn it off in **Settings → General → Daily briefing**.
- **Hide any part of a website.** Right-click a banner, a sidebar or anything else you never want to see and choose **Hide an element…** (or use the command palette). Point, press ↑ or ↓ to take more or less of the page, and click: it stays hidden on that site from then on. Undo it from the notice, or see and show hidden parts again in **Studio → Site styles → Hidden elements**.
- **Studio changes arrive with motion.** A new theme dyes out from where you clicked, and everything else it changes moves at the same time: ink threads for its accent, warping letters for its fonts, rippling corners and springing rows. A new accent colour flies in short ink threads to every button and switch that wears it. Fonts warp letter by letter into the new ones. Corners ripple round their edges like a sound wave and spring into their new shape. And the new **Density** setting (Compact, Default, Airy) springs rows and buttons to their new size. With Animations off, changes simply happen.
- **Studio → Highlights.** The soft light around a focused search box or text field, a live clip that changed and the card you chose can now be a soft ring, a glow, a thin outline or nothing, in any thickness, strength and colour, with or without the pulse on changed clips.
- **The assistant's petal.** While the assistant reads a page or thinks, a small petal drifts in the wind beside what it's doing, and a gust carries it off when the answer starts.
- **The Converter folds.** While a file is converted, it folds over into its new format.
- **Quiet empty pages.** Empty Downloads, History and Bookmarks pages draw a small still life once, then stay still.
- **Tracking snipped off.** When a link loses its tracking parameters (*?utm_source=…*, *fbclid=…*), you see them snipped off the end of the address, and on **Copy clean link** too.
- **Fixed:** after an update, the assistant's button could stay hidden even with the assistant on, until you turned it off and on again.

## 2.16.0 (2026-11-13)
- **Links you click on websites are checked too.** Until now only pasted links and links from other apps were checked. A link on a website that takes you to another site now gets the same checks before it opens: IP loggers, lookalike addresses (*dlscord.com*, *liches.com*), disguised links, each redirect, and a page that pretends to be a well-known site to get your password. It never asks on a search engine's results or for links within one site, and Strict mode's "unknown site" question stays for pasted and outside links only. A check takes about a tenth of a millisecond. Turn it off with **Check links you click on websites** in Settings → Privacy & security.
- **Scam lists also cover what a page loads.** The phishing and malware lists were checked for pages you open and for downloads. Now a page that isn't on any list also can't load a script, a picture or anything else from an address that is. It shows on the privacy receipt.
- **VPN apps with their own made-up address range.** A VPN app in TUN mode can be set to make addresses up from a range of its own choosing. Aphrodite now notices that range by itself (Secure DNS off), and protects your network there as well.

## 2.15.0 (2026-11-12)
- **Websites can't look into your computer or home network.** A website's code runs on your computer, so it can try to reach programs running on it and devices on your network, like your router, printer or cameras. Some sites do this to see which apps you have, which helps to fingerprint you, and a malicious page can try to change your router's settings. Aphrodite now stops any website from sending requests to this computer (localhost) or to your home network, including the "0.0.0.0" trick, your computer's own internet (IPv6) address, names that secretly point there, and names that switch to your computer after the page has loaded ("DNS rebinding"), from the very first request. That covers what Aphrodite loads for a page too, such as its tab icon and its privacy-policy link, and connections that aren't ordinary web requests: a video-call (WebRTC) relay server or a WebTransport address pointing at your computer or network is refused. Addresses you open yourself, links you click and local web pages still work, and so does your router's page when you open it by its name — but a page can't quietly submit a form to a device on your network behind your back.
- **Asked first when a website sends you to your router.** A link, a script, a redirect or a pop-up from a website that leads to a device on your network or a program on this computer no longer just opens: Aphrodite stops and asks, because one address is enough to change a setting on some routers. **Open it** continues; addresses you type, bookmarks and sites you allowed open as before. Signing in to an app that waits on this computer (it sends you back to "localhost") takes one extra click.
- **Tab icons can't be used to follow you.** A site's icon used to be loaded by Aphrodite's own window, outside every protection, where a tracker could leave a cookie on one site and read it back on the next. Icons are now fetched by the tab itself, protected like the rest of the page, without cookies, and never from a blocked tracker. Aphrodite's window can no longer load anything from the internet.
- **See every attempt.** The privacy receipt lists what a site tried to reach, such as *127.0.0.1:3389*, and the shield panel's week view counts them. A site that really needs it (a router's setup page, Plex, a printer, an app's companion page) can be allowed with one click from the note in the shield panel, or with **Block local network access** in its list. Turn it off for every site in **Settings → Shields**.
- **How names are checked.** Every address lookup now goes through a small relay inside Aphrodite. It asks the same place as before (your Secure DNS provider, or Windows' own DNS when Secure DNS is off) and refuses any answer that would point a website at your computer or your network, so the browser never gets that address. It adds about 2 milliseconds per lookup, keeps nothing on disk, and nothing goes around your VPN.
- **VPN apps that work as a proxy** (such as v2rayN or Clash set as the system proxy) look names up themselves, so the relay can't see where those names lead. Aphrodite tests the VPN app instead: it asks it for a name that points at this computer and watches whether anything arrives. If the app refuses (it has a "block private addresses" rule, or looks names up at its far end), nothing more is needed and nothing is slowed down. If it doesn't, Aphrodite looks up each new name a page reaches for itself, over encrypted DNS through the VPN, and blocks the ones that point home; that adds a short wait the first time a page uses a name. Two ways to avoid both the gap and the wait: use the VPN app's **TUN mode** (then Aphrodite's relay sees every name, as with an ordinary VPN), or add a routing rule that sends private addresses to "block" (in v2rayN: `geoip:private`, with domain strategy *IPIfNonMatch*). Addresses written as such (127.0.0.1, 192.168.x.x, localhost and the like) are blocked as always.
- **VPN apps that make addresses up** (TUN mode with "fake-IP", as Clash and sing-box can do). With Secure DNS off, such an app answers every name with a made-up address, so Aphrodite couldn't see where a name leads. It now tests the app the same way and, if the app doesn't refuse names that point home, asks for each name's real address over encrypted DNS through the VPN. A made-up address written straight into a page is refused too.
- **A proxy on another device of your network** (a company's proxy, one on a router or NAS) can't be tested that way, so Aphrodite always checks names itself there. A proxy given by a name that leads to your network keeps working.
- **No late error reports.** A site can ask the browser to send error reports up to a minute after you've left it (Reporting API, Network Error Logging). Aphrodite never sends them.
- **Fixed: a lookup around VPN apps.** With Secure DNS turned off and a VPN app that works as a proxy, **Unmask disguised trackers** asked your internet provider about some site addresses directly, around the VPN. It now asks over encrypted DNS through the VPN instead, so it keeps catching disguised trackers and nothing goes around your VPN.
- **See what a site was told: "What it saw".** The privacy receipt has a new view that shows what a site's fingerprinting scripts actually got. It runs the same tests they use in a hidden, offline window, with that site's own secret: the hidden drawing next to the one the site got, with the changed pixels magnified, the audio fingerprint, your real graphics card, CPU cores, storage and languages next to what the site was shown, and proof that another site is told something else again. Nothing is saved, and the site's page is never touched. Open it from **Receipt → What it saw** in the shield panel.

## 2.14.0 (2026-11-12)
- **390,000 more scam sites known.** Phishing.Database's list of phishing sites now comes with Aphrodite and is checked for every page you open and every download, alongside the lists that update twice a day. It's read straight from disk, so it uses almost no memory.
- **Lookalikes of any well-known site.** A pasted link or a link from another app that's one letter away from one of the 10,000 best-known sites, like *liches.com* for lichess.org, now gets a warning with a **Go to lichess.org** button. Before, only about 50 big brands were checked.
- **Strict mode, on by default.** A pasted link or a link from another app that leads to a site that isn't one of the 100,000 best-known sites, and isn't in your bookmarks, now asks before opening: scam links often lead to new, little-known sites. Small real sites ask too, and one click opens them. Links you click inside pages and addresses you type aren't affected. Turn it off in **Settings → Privacy & security**.

## 2.13.0 (2026-11-12)
- **Open web pages saved on your computer.** Aphrodite now opens .html and .htm files (and .shtml and .xhtml): double-click one after choosing Aphrodite for them in Windows' Default apps, use **Open with → Aphrodite**, or drop the file on Aphrodite's window. It opens in its own tab.
- **Links between those files work.** A saved page can open the pages next to it, such as offline documentation or a page saved with its parts. Websites still can't open files on your computer, and a local page can only reach files on this computer: never another computer's shared folders, which could make Windows hand your sign-in to them. Files opened straight from a network share (\\server\folder) aren't opened for the same reason; mapped drives work.
- **Linux:** the .deb and the AppImage now list Aphrodite for web pages too.
- **Privacy guide and documents.** Settings → Privacy guide now explains the link checks and local web pages. The privacy policy describes them, and the licence agreement (version 1.3) notes that link checks are best-effort.

## 2.12.0 (2026-11-12)
- **Make Aphrodite your default browser.** **Settings → General → Default browser** sets it up on Windows and Linux, so links from Discord, email and other apps open in Aphrodite. On Windows, it opens Windows' Default apps page on Aphrodite, where you choose it (Windows doesn't let apps make themselves the default). Windows users need to install this version with the installer for Aphrodite to appear there.
- **Links checked before they open.** When you paste a link into the address bar or the new tab page, or another app opens one in Aphrodite, it's checked first, on this computer:
  - known **IP loggers** (Grabify, IPLogger and their disguised addresses) are stopped, because opening one shows your IP address to whoever made the link;
  - **lookalike addresses** made to pass for a well-known site, like *dlscord.com*, *steamcommunlty.com*, *rnicrosoft.com* or a name spelled with letters from another alphabet;
  - **disguised links**, like *discord.com.free-nitro.ru* or *microsoft.com@another-site*, where the real site is hidden further along;
  - links to a bare IP address, or straight to a program from a site you don't know.
- **Redirects and fake sign-in pages too.** A short link is followed and checked where it really lands. Once the page opens, Aphrodite also warns you if it calls itself Discord, Steam, PayPal or another well-known name and asks for your password on an address that isn't theirs.
- **No false alarms on real links.** Only the site's name counts, not the rest of the link, so *discord.com/channels/…* is fine. Well-known sites and sites you bookmarked are never treated as lookalikes, and links you click inside pages or addresses you type aren't checked at all. Nothing is looked up anywhere. You can still open a flagged link if you trust it. Turn the checks off in **Settings → Privacy & security**.
- **Update the phishing and malware lists yourself.** Settings → Privacy & security now shows when the lists were last updated, with an **Update now** button. They still update by themselves twice a day.
- **Remove single pages from your history.** Point at a page in History and click the bin to remove just that visit, or **Remove day** to remove everything from one day.
- **Smaller touches.** Model cards in Settings → Assistant are tidier once a model is downloaded, the download line no longer jumps as the speed changes, the sidebar's bottom buttons are evenly spaced, and window titles read "Page - Aphrodite" like other browsers.

## 2.11.1 (2026-11-12)
- **A clearer way to pick a model.** Settings → Assistant now shows the four models as cards, side by side: what each is good for, how fast and how smart it is, its download size and the memory it needs. The one that fits your computer is marked "Best for this computer".
- **Shorter warnings, still there.** Light's and Max's warnings are now one word on their cards; tap or point at it to read the whole thing, and it's shown in full again before you download.
- **Your models at a glance.** A downloaded model's card shows whether it's in use, its speed check result, and Test speed; Delete is under the "…" button. The speed of the model in use also appears next to your computer's details.
- **Fixed:** Max showed a "Less reliable" label next to "Experimental".

## 2.11.0 (2026-11-12)
- **A model for every computer.** The assistant now comes in four sizes, all from the same open-source Qwen family: **Light** for older or modest computers, **Standard** (the one from 2.10), **Strong** for computers with plenty of memory or a separate graphics card, and **Max** for computers with 32 GB of memory or more. Download as many as you like in **Settings → Assistant** and choose which one answers. Max is marked experimental: it hasn't been fully tested yet. Light is marked less reliable: it gets facts wrong more often, so don't rely on it for health, legal or money questions.
- **Harder to fool, safer to ask.** Sentences in a page that try to give the assistant orders are taken out before it reads the page, and it tells you when a page tried. Text you select for Explain or Translate is treated as text, never as orders. It won't call a shop or site safe (it can't check), and points out warning signs instead. It doesn't give medicine doses, answers with care when someone is struggling, and no longer repeats itself or adds emojis you didn't ask for.
- **Still an AI, so check what matters.** Every model can be wrong, misread a page or make things up, even when it sounds sure. Its answers aren't medical, legal, financial or other professional advice, and they aren't statements by SolidCarbon Works: you use them at your own risk. The licence agreement (version 1.2) now covers the new models, the warnings and saved chats.
- **Aphrodite suggests the right one.** Settings looks at your computer's memory and graphics card, on this computer only, and marks the model that fits it best. If your computer looks too small for the assistant, or for the model you pick, it says so before the download and still lets you go ahead.
- **Test speed.** Each downloaded model can write a short answer and time it, so you see how fast it really is on your computer.
- **Saved chats, if you want them.** Turn on **Save chats** and your chats are kept with the page each one was about, so you can open one from the panel's history button and carry on where you left off, even on another page. Choose **Use the page I'm on instead** to switch the chat to the page in front of you. Saved chats stay on this computer, are encrypted with your account's protection, are never saved for private windows, and are deleted after the time you choose (30 days to start with), with **Delete all**, or when you clear your history.

## 2.10.0 (2026-11-11)
- **An assistant that never leaves your computer.** Aphrodite can now answer questions about the page you're on: **summarise** it, **explain** a passage you selected, **translate** a selection, or just talk. It runs on a language model stored on your own computer. What you ask, and the pages it reads, are never sent anywhere, and the assistant's engine has no network access at all.
- **Off until you turn it on.** Nothing is downloaded with this update. In **Settings → Assistant**, switch it on and choose Download: the model is a 2.8 GB file from Aphrodite's own releases page, checked against its published checksum before it is used. You can pause and carry on the download, and delete the model whenever you like.
- **A panel you can put anywhere.** The sparkle button at the bottom of the sidebar opens the assistant. Drag it by its title bar, size it from its corner, and it stays where you left it. **This page** decides whether it reads the page first; turn that off for quicker answers that aren't about the page.
- **It only reads.** The assistant can't click, type, open pages or search. A page's text is given to it as material to read, never as instructions, and its answers are shown as plain text.
- **Light on memory when idle.** The model is loaded when you ask something (about ten seconds) and put away again after a few quiet minutes; you choose how long, or put it away at once. While it's awake it uses about 5 GB of memory, so on computers with little memory it is slow. It runs on the processor unless the computer has a separate graphics card.
- **Answers can be wrong.** It is a small AI model: it can misread a page or make things up. A notice says so the first time you turn it on. Check anything that matters; its answers aren't professional advice.

## 2.9.0 (2026-11-11)
- **Edit PDFs.** The pencil on a PDF's bar opens the tools, right beside the page controls: **highlight**, **draw**, **type** (in a sans, serif or mono face, bold or italic, any colour), **add pictures** and **sign** (draw your signature, type it, or use a picture of it; Aphrodite can remember it on this computer). The **hand** selects what you added so you can move or change it, the **eraser** removes it, and **Undo** and **Redo** step through everything in order. Form fields you fill in are kept. **Save a copy** writes a new file and leaves the original alone, and Aphrodite asks before you close a PDF with changes you haven't saved.
- **Organise pages.** While editing, the page previews get their own buttons: turn, duplicate or delete pages, add an empty page, add pages from another PDF or a picture, drag a page to move it, or save the chosen pages as a new PDF. A deleted page is really gone from the file, not just hidden.
- **Redact.** Drag a box over anything, or put a box on every match of a search. Nothing is removed until you apply it. Each redacted page is then rebuilt as a picture with the boxes burnt in, so the words under them are gone from the file, and Aphrodite checks the result before showing it. Text on a redacted page can no longer be selected.
- **Hidden details and flatten.** The ⋯ button shows what a PDF says about itself (author, program, dates), removes it, or makes what you added a permanent part of the pages.
- **Converter.** A new page, next to Studio in the sidebar, changes a file's format on this computer. Pictures (PNG, JPEG, WebP, AVIF, GIF, BMP, ICO, SVG) become PNG, JPEG, WebP, BMP, ICO or a PDF. PDFs become pictures or plain text. Word documents, Markdown, HTML, plain text and e-books (EPUB) become PDF, HTML, Markdown, plain text or EPUB. Excel sheets, CSV, TSV and JSON become each other, an HTML table or a PDF. Several files can go at once, and the camera, place, author and other hidden details are left out of what is made.
- **Reduce size.** Also in the Converter: make pictures and PDFs smaller with Light, Balanced or Strong, or fit a picture under a size you name.
- **Clean metadata.** Takes the camera, place, author, company, dates and editing history out of JPEG, PNG, WebP, PDF, Word, Excel and EPUB files, and changes nothing else.
- **Nothing is uploaded.** The Converter and the PDF tools work in a locked-down page with no network: a file you convert can't contact a site, and no site sees it. Originals are never changed; every result is a new file.
- **PDFs keep their own colours.** A dark theme no longer turns PDF pages dark by itself. Use the moon on the PDF bar when you want dark pages. A PDF that is already on your computer can now be saved as a copy from that bar too.
- **Bookmark icons without a visit.** A bookmark's icon is now kept from the last time you were on the site, so the new tab page no longer contacts your bookmarked sites to draw their icons.

## 2.8.0 (2026-11-10)
- **The intro wears your theme.** The welcome animation now uses your Studio theme's colours: its card, the handwriting and the petals.
- **Theme icon, made dependable.** The taskbar, desktop and Start menu icons now follow the theme you saved, and only that: not a theme you are trying out, a workspace's look or the time of day. A change made just before closing is no longer lost, the icon is put right again after an update, and shortcuts you renamed or pinned again are found too.

## 2.7.0 (2026-11-10)
- **Delete a site's data from the lock.** The lock button's panel now has **Delete all data**: it removes that site's cookies, sign-ins and stored data and reloads the page. It asks once more on the button itself, so a stray click can't sign you out.
- **Aphrodite's own drop-downs in the Shields panel.** Bot checks, Cookie pop-ups and Time zone now open the same rounded lists as the rest of the browser, instead of the system's.
- **Workspace dots have their own row.** They now sit above the protection card, and a long row scrolls sideways. The buttons at the bottom of the sidebar stay put: Private window and Limiters on the left, Studio and Settings on the right.

## 2.6.0 (2026-11-10)
- **Pause and resume downloads.** A download's notification and the Downloads page now have **Pause** and **Resume** next to Cancel, and show the speed and the time left. A download that was interrupted can be picked up again.
- **Verify a download.** On a finished download, **Verify** compares the file with the SHA-256 checksum its publisher lists and tells you whether it is exactly the file they made. It is worked out on your computer; nothing is sent.
- **Ask where to save.** A new switch in Settings asks for a folder and name before each download. **Save link as…**, **Save image as…** and **Save page as…** in the right-click menu now always ask.
- **Export bookmarks.** Settings → Your data saves all your bookmarks as an HTML file that any browser can import.
- **Full screen.** **F11** fills the screen with the page and hides the sidebar and toolbar. Press it again to come back.
- **Downloads in the sidebar.** The Downloads entry shows a ring that fills while files download, how far along they are, and a dot when one has finished and you haven't looked yet.
- **Livelier notifications.** Notifications now slide away when they close and shuffle smoothly into place, and a download's icon changes as it finishes. A download notification you close stays closed until the file is done.
- **Privacy guide, brought up to date.** New parts cover downloads and files, protections around the page (permissions, devices, link pings, separate logins), and what Aphrodite itself sends and to whom.

## 2.5.2 (2026-11-10)
- **Build housekeeping.** A small fix to how Aphrodite is packaged. Nothing changes in how it looks or works.

## 2.5.1 (2026-11-10)
- **Theme icon on your shortcuts, fixed.** The taskbar, desktop and Start menu icons now really follow your theme while Aphrodite is closed. Windows was holding on to the old picture.
- **Tidier sidebar footer.** The Limiters button now sits next to Private window, so the workspace dots are centred between two buttons on each side.

## 2.5.0 (2026-11-10)
- **Page previews in the PDF viewer.** A strip down the right side shows every page. Click one to jump to it; the button on the bar hides the strip, and your choice is remembered.
- **Open your own PDFs.** Aphrodite now appears under **Open with** for PDF files on Windows and Linux (it never makes itself the default), and you can drop a PDF onto the window.
- **Taskbar and dock actions.** Right-click Aphrodite's icon for **New tab**, **New window** and **New private window**.
- **Limits for one tab.** Right-click a tab → **Limit this tab** to give it its own speed, its own network cap, and a memory size past which it goes to sleep. A lightning mark shows which tabs are limited.
- **Download speed in Limiters.** The popup now shows how fast this window's tabs are downloading, in total and per tab. It is only measured while the popup is open.

## 2.4.0 (2026-11-10)
- **PDF viewer.** PDFs now open inside their tab instead of showing an empty page, in Aphrodite's own viewer: turn pages, zoom, fit to width, search every page, rotate, select and copy text, and download. It takes the colours of your theme, and **dark pages** (on with a dark theme, or from the moon button) redraws the document light on dark while pictures keep their own colours. The viewer page can't reach the network and never runs scripts inside a PDF. Back returns to the page you came from, and **⋯ → Open a PDF from this computer** opens a local file.
- **Limiters.** A new gauge button at the bottom of the sidebar shows how much memory and processor Aphrodite is using and lets you cap it with sliders: a memory limit that puts tabs you aren't looking at to sleep (with an optional hard limit), a slower speed for background tabs, and a network speed cap. It also lists the heaviest tabs, with buttons to sleep or close them.

## 2.3.6 (2026-11-10)
- **Fingerprint protection restored.** In 2.3.5 the fingerprint defences did not switch on, so sites could read real device details. They are back on in every page, frame and worker, and still leave nothing on the page that a site could use to spot Aphrodite.
- **Tracker blocking restored for a site's own trackers.** 2.3.5 let every request to a site's own domain through. A site's own analytics and disguised (CNAME) trackers are blocked again unless you choose "Trust this site".

## 2.3.5 (2026-11-09)
- **Forms work on more sites.** A site's own sign-in, posting and checkout requests go through without needing Trust this site.

## 2.3.4 (2026-11-09)
- **Tidier installation.** A part Aphrodite no longer used was removed.

## 2.3.3 (2026-11-09)
- **New tab button under your tabs.** A + button sits right below the tabs in the sidebar and slides down as tabs are added.
- **Shortcut icons match your theme.** The taskbar, desktop and Start menu icons show your theme's colours, even while Aphrodite is closed.

## 2.3.2 (2026-11-08)
- **Fixed:** the search box text in Settings and Studio jumped up by a pixel when you started scrolling.

## 2.3.1 (2026-11-08)
- **Fixed:** the section menu in Settings and Studio moved slightly when you started or stopped scrolling.

## 2.3.0 (2026-11-06)
- **Mute pinned tabs in place.** A pinned tab playing sound shows a speaker you can click to mute or unmute it, and **Shift + middle-click** closes a pinned tab.
- **Drag pinned tabs and folders.** Drag pinned tabs to reorder them or into split view, and drag a folder to move it with all its tabs.
- **Edit bookmarks and new tab shortcuts.** Right-click a shortcut on the new tab page or a bookmark in the Library to open it in a new tab or split view, rename it, change or copy its address, or remove it. Drag shortcuts on the new tab page into any order.
- **Clearer error pages that reconnect by themselves.** When a page can't load, Aphrodite says why in plain words (offline, the site's name couldn't be found, timed out, a certificate problem and so on), offers what might fix it, and reloads the tab as soon as you're back online.

## 2.2.2 (2026-11-06)
- **Fixed:** Aphrodite could crash when starting after an update if a workspace had its own logins.

## 2.2.1 (2026-11-06)
- **Better on scaled screens.** With Windows display scaling (125% and up), Aphrodite keeps its usual proportions, and the shield panel and menus fit the window, so their bottom buttons are never cut off.

## 2.2.0 (2026-11-06)
- **Tab opening and closing animations.** New tabs and closed tabs now animate in the sidebar, with five opening styles (**Ink stamp**, **Scroll unroll**, **Silk ribbon**, **3D unfold** and **Petal bloom**) and five closing styles (**Strikethrough**, **Blurry glitch**, **Paper split**, **3D flip** and **Wind-up flick**) in **Studio → Layout**, alongside **Off**.

## 2.1.0 (2026-11-06)
- **A hand-written welcome.** On first launch and after each update, Aphrodite opens with a small card: the Petal A mark is drawn in, then "Aphrodite" is written stroke by stroke, underlined, and signed with a petal. Click or press Esc to skip it. You can watch it again from Settings → About or the command palette (**Replay welcome animation**).

## 2.0.3 (2026-11-05)
- **The icon matches your theme.** When you switch themes or change colours in Studio, Aphrodite's window and taskbar icon change to match.

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

# Pre-release

Test versions from before the public release.

## 1.16.2 (2026-11-05)
- **Bot checks stop thinking DevTools is open.** Security checks on some sites could mistake Aphrodite's window for one with DevTools open. Pages now see a normal browser window.
- **Sites you return to see the same device.** A site keeps the same made-up device details for as long as you keep its cookies, so sites you log in to don't see a new device every visit. Different sites still get unrelated details.

## 1.16.1 (2026-11-05)
- **GitHub sign-up works when you trust github.com.** A trusted site's own background reports now go through; other companies' stay blocked.
- The shield panel says so: “Its own analytics are allowed while you trust it” under Trust this site.

## 1.16.0 (2026-11-05)
- **Sign-ups work with bot protection.** Bot-protection services (DataDome, Arkose, hCaptcha, reCAPTCHA, Cloudflare Turnstile, HUMAN, Kasada, Imperva, Friendly Captcha, GeeTest and MTCaptcha) are recognised and no longer blocked as trackers, so sign-ups on sites that use them stop failing.
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

## 1.14.3 (2026-11-05)
- **Clips survive a lost connection.** A page that doesn’t load (no internet, site down, timed out, a server error) no longer makes a clip say “can’t find it”: it keeps its last value and shows it as offline, quietly (a hollow dot, no red). While Windows reports no network, checks pause. When the connection is back, waiting clips are checked within about 20 seconds; a site that didn’t answer is tried again after 2 minutes instead of at the clip’s next turn.
- The shield panel says **Got some real answers** with a link to the receipt, instead of listing every one.

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

## 1.13.0 (2026-11-05)
- **Tab sleeping** (Settings → General): a tab you haven’t opened for a while (30 minutes by default; 5 minutes to 2 hours, or never) closes its page to free memory and loads again when you click it. Sleeping tabs look faded with a small moon. The tab you’re on, pinned tabs, tabs playing sound, tabs asking for a permission, tabs with text you typed and haven’t sent, and sites that forget you when closed never sleep on their own. Add sites that should never sleep in Settings or from the tab’s menu, which can also put a tab to sleep straight away.
- **Workspaces with their own look and protection.** From a workspace’s menu, pick one of your saved Studio themes for it and a protection level: Strict (everything on, and sites are forgotten when you close them), Balanced (Aphrodite’s defaults), Compatible (for sites that break: ads and trackers still blocked, fingerprinting and third-party cookies allowed) or your Shields settings. Switching workspace switches both. A site’s own settings still win, and the shield panel says when a workspace sets the level.
- **Shortcut editor** (Settings → Shortcuts): change the keys for any command (with a reset button), and give one key to one thing only (taking a key moves it and tells you). Make **your own shortcuts** that open a site, run any command, switch workspace, turn one of your CSS styles on or off, or flip one of your switches. Share them as a code (`APHK1.…`). Ctrl+Shift+Alt+M (turn off my theme and styles) always works and can’t be changed. Menus and Ctrl+K show your keys.
- **Your own buttons** (Studio → Buttons & controls): in the toolbar or at the bottom of the sidebar, with an Aphrodite icon, an emoji or your own SVG (drawn as an image, so it can’t run anything). They do the same things your shortcuts can.
- **Your own sliders and switches**, under a new sliders button in the toolbar: drive a CSS variable of yours (a “Blur” slider sets `--my-blur` for your interface CSS, live), or page zoom, text size, sidebar width, corner roundness, your interface CSS or the sidebar.
- **Toolbar examples** for Interface CSS: hide, move or shrink toolbar buttons.
- **Search keywords** in the address bar: `yt lofi beats` searches YouTube, `w Rome` Wikipedia, and `gh`, `r`, `maps`, `amz`, `imdb`, `so`, `mdn`, `ddg`, `b` and `g` come built in. Add your own in Settings → Search with a link that has `%s` where the search goes. The search goes only to that site, and the address bar suggests it first.

## 1.12.0 (2026-11-04)
- **Cloudflare checks work again**, with every protection on. "Verify you are human" no longer loops back after you tick it, and Cloudflare's own check passes without a click, as in Chrome. The causes, all fixed at the root (no exemptions for Cloudflare):
  - Frames from other sites sent a different browser name than the page, so Cloudflare's clearance never matched. Every frame now sends the same one.
  - `Accept-Language` was malformed (`en-US,en;q=0.9;q=0.9`); it is now `en-US,en;q=0.9`, as in Chrome.
  - The fake language list contradicted what Web Workers report, and Cloudflare compares the two. Workers now get the same values (below).
- **Fingerprint protection now reaches everywhere a script can run.** A fingerprint audit found 19 problems; all are fixed or listed under Honest limits in the README:
  - Same-origin iframes reached through `window.frames[i]`, `window[i]` or `innerHTML` (not just `.contentWindow`) got every real value. Every frame, and every popup, is now protected before a script can touch it.
  - Web Workers, workers started by workers, shared workers and service workers read your real GPU model, CPU cores, memory, languages and canvas. They now get the same defences, and the same values, as the page.
  - Canvas noise also covers copies through ImageBitmap, VideoFrame and WebGPU. It is tied to each pixel's position, so reading a canvas in tiles or one pixel at a time can't get around it, and a copy can't undo it.
  - Audio worklets get the same inaudible noise as other audio reads.
  - The GPU model is reported without its exact device ID (as WebGPU does) instead of a made-up "Generic Renderer".
  - Fakes that gave themselves away are now realistic: battery reads as a desktop on mains power, the keyboard as US English, speech voices only for the languages you report, the screen with a common taskbar size, Chrome's full version and Windows version as Chrome reports them, and a common storage quota instead of a share of your disk.
  - Protected values behave like Chrome's own, so they don't give themselves away.
  - Solid colour fills and cleared canvases read back exactly, and rendered audio keeps true silence, so the noise only touches what can fingerprint you (text, emoji, curves, images, WebGL, rendered sound).
- **Time zone sites see** (Settings → Privacy, and in the shield panel): your own, **Match my VPN’s location** (the time zone of wherever your IP address appears to be, looked up at startup and every 10 minutes, with a restart offered when it changes) or UTC. Pages and their workers all agree on it. Off by default; applies after a restart.
- **Hide window size and position** (on by default): sites see a maximised window on your screen, the same in every frame, whatever your window’s real size and place. Nothing on screen changes.
- **Receipts say what sites got for real, not just what was faked.** “Got made-up answers” and “Got real answers” are listed apart, each real one with the reason: it can’t be hidden by a browser (fonts, graphics card model, cameras and microphones, browser version), fingerprinting or shields were off for the site, a protection switch was off, or your time zone setting. The summary now says, for example, “8 ways: 5 got made-up answers, 3 got real ones” (it used to say every answer was made up, which wasn’t true for fonts).
- Reads are noted even when a protection is off (without changing anything), so the **Leak log** now lists device details a site got because fingerprinting or shields were off, and **Raise shields** fixes them. The shield panel shows “Got real answers: …” at a glance, and a red dot on the shield button flags real answers a protection would have hidden.
- **History and Downloads** open in their own panel beside the sidebar instead of as tabs. Esc or a click outside closes it.
- **Fixed:** a window could fail to start and stay blank.
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
- **Fixed:** receipts counted the previous page's requests: beacons a page sends as you leave it (DuckDuckGo's, for example) were filed under the next site you opened, and could make a company look like it followed you there.
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
- **Fixed:** an error window could still appear ("A JavaScript error occurred in the main process"). Now fixed for good: every download in the app, including the extension store's (installs, icons, update checks), now goes through the browser's own network stack. 1.5.1 had only moved the filter lists.
- Cookies & site data: the time and the arrow sit in fixed columns, so times line up whether a row expands or not.

## 1.5.2 (2026-11-04)
- **Fixed:** Cloudflare and other bot checks could treat Aphrodite as a bot. It now sends the same browser details as Chrome.
- The publisher name now shows in Windows' installed-apps list and the program's file details.

## 1.5.1 (2026-11-04)
- **Fixed:** an error window ("A JavaScript error occurred in the main process") could appear while filter lists updated. Filter lists and the ad-partner list now download through the browser's own network stack instead of Node's, which had the bug.

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
- **Fixed:** a crash when tabs closed with extensions loaded.

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
- Clearer update error messages.

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
