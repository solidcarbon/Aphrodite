# Aphrodite privacy policy

**Effective 19 November 2026**

Short version: **Aphrodite doesn't collect your data.** There's no account, no telemetry, no crash reporting and no analytics. Your history, bookmarks and settings stay on your device.

## What stays on your device

These are stored only in your Aphrodite profile folder on your computer, and we never receive them:
- browsing history, bookmarks, open tabs and workspaces
- cookies, site permissions and consent choices
- downloads and settings
- the made-up device details each site sees (see below)
- signatures you ask the PDF editor to remember (kept as pictures, encrypted with your operating system's protection for your account; never in a private window)
- disguised trackers Aphrodite has caught, for two weeks, so it can block them at once next time (scrambled, so the file doesn't show which sites they were on, and encrypted; not from private windows or with Save browsing history off; forgotten with Clear history)
- extensions you add, your choices for each (where it runs, which programs it may start, whether it may route your browsing, and the proxy servers it set), and what each extension stores for itself (deleted when you remove it); other sites whose scripts you allowed on a site (never from a private window)

With **Save browsing history** off, no visit is written: no history list, downloads list, visit times or privacy receipts. Sites' own cookies and data, and the list of sites that stored data, stay until you delete them. **Clear history** removes the history list together with visit times, receipts, the Leak log and noticed changes. A **private window** writes none of these, and nothing you choose in it (lowering shields, trusting a site, continuing to an HTTP site) is kept after it closes.

**Clear data when Aphrodite closes** deletes cookies, site data, cache and history each time you quit. Windows doesn't let an app finish this when it shuts down, restarts or signs out, so if that happens (or Aphrodite crashes), the deletion is done the next time Aphrodite starts, before any window opens.

## Files you open, edit or convert

PDFs you read or edit, and files you convert, make smaller or clean in the Converter, are handled **only on your computer**:
- They are never uploaded, and we never receive them or anything about them.
- They are read in a locked-down page that can't connect to the internet, so a file can't contact a website while it is open (for example through a picture or link inside it).
- The original is left as it is. Every result is a new file, saved where you choose.

A PDF that a website sends you is downloaded from that website, in the same way as the page that linked to it.

**Web pages saved on your computer** (.html files) open as ordinary web pages, read from your computer:
- They can open other files next to them on your computer, but never files on another computer's shared folders, and Aphrodite never opens a page straight from a network share. Reaching another computer's files could make your operating system hand your sign-in to it.
- Like any web page, a local page can load pictures, fonts and scripts from the internet, and its scripts can see where the file is on your computer (which can include your account's name). Aphrodite's tracker blocking and fingerprint protection apply to it as to any page. Open only files you trust.
- Local pages aren't kept in your browsing history. Websites can never open files on your computer.

## Links: checked before they open

Aphrodite checks a link **on your device** before it loads, in three cases:
- you paste it into the address bar or the new tab page;
- another app (Discord, email, chat) opens it in Aphrodite;
- you click it on a website and it leads to a different site.

It looks for known IP-logging services, addresses made to look like a well-known site, disguised links, the redirects of that first load, and a page that pretends to be a well-known site to get your password. To recognise well-known sites, it uses a list of popular websites that ships with Aphrodite, and your bookmarks.

Not checked: addresses you type, links within one site, and links on a search engine's results.

In **Strict mode** (on unless you turn it off), a pasted link or a link from another app that leads to a site on neither list asks before opening. Strict mode never applies to links you click on websites.

**The links themselves aren't sent anywhere and nothing is looked up online.** Each of the three (the checks, the checks for clicked links, Strict mode) has its own switch in Settings → Privacy & security.

## Your computer and home network

A website's code runs on your computer, so it could try to reach programs running on it and devices on your network (router, printer, cameras). Aphrodite refuses that, and asks you first when a website tries to send you to such an address. Each attempt is listed on that site's privacy receipt, which stays on your device.

To do this, every website address lookup passes through a small relay inside Aphrodite. It keeps nothing on disk and remembers names only as scrambled fingerprints, until Aphrodite closes.

If you use a VPN app, Aphrodite tests it in the background, about every ten minutes: it asks the app for a public test name that points at your own computer (such as localtest.me) and watches whether a connection arrives. If the app doesn't refuse such names, Aphrodite looks up the names pages use itself, encrypted, at your secure-DNS provider (Quad9 unless you chose another), **through your VPN**. This happens even when secure DNS is turned off, because the alternative would be a lookup outside your VPN.

## Extensions

Extensions are made by other people and companies, and **their own privacy policies apply to what they do**. Before you add one, Aphrodite shows in plain words what it will be able to do, and says so when it isn't from a store. What Aphrodite does around them:
- **Local Firefox files.** Aphrodite checks supported Mozilla signatures on this computer and displays the result before installation. Checking a local file makes no request to Mozilla.
- **Request headers.** An extension with blocking web-request permission and site access can see the request URL and edit supported HTTP headers in that workspace. The header listener receives a limited set of fields. Aphrodite applies Global Privacy Control and its cookie protections afterward.
- **Where they run:** never in private windows. Each one runs on the sites you choose (every site, every site except some, only some, or only when you click it), and you can turn one off on any site.
- **Their own connections** go through Aphrodite's protections: known dangerous and tracking addresses are refused, plain HTTP is made secure, and they can't reach your computer or your home network unless their own list names an address there. Each extension's card lists the sites it contacted, kept in memory until Aphrodite closes.
- **Their own rules** for blocking or redirecting requests (declarativeNetRequest) run only after Aphrodite's protections: they can block more, never less, and can't remove Aphrodite's privacy signal or cookie protection. Their rules and settings are kept on this computer.
- **Cookies:** an extension with that permission sees and changes cookies only for sites it can reach, never for a site you turned it off for.
- **Settings for syncing** that an extension saves stay on this computer; Aphrodite syncs nothing. Facts about your computer it may ask for (processor, memory, screens, disks) are rounded.
- **Recording and saving:** an extension can record your screen or a window only after you choose it in Aphrodite's picker, and a tab only after you allow it (a red dot shows while it records), each time. It can save copies of pages it can reach after you allow that once. What it records or saves goes to the extension, and its own privacy policy applies.
- **Sign-in windows** an extension opens show the site's name; the code meant for the extension is handed to it directly and never sent anywhere else.
- **Your bookmarks, history and downloads:** an extension with those permissions can read them on this computer (never a private window's). It asks the first time it wants to delete history or browsing data, or open or delete downloaded files. It can make a site stricter but never looser, and it can only read privacy settings, never change them.
- **User scripts** an extension adds run only on sites it can reach, never on a site you turned it off for, each in a space of its own.
- **VPN extensions (proxies):** an extension can send your browsing through its own servers only after you say yes; **whoever runs those servers can see which sites you visit**, and their own privacy policy applies. It never applies to private windows, the shield panel shows it while it's active, and taking it back on the extension's card restores your computer's proxy settings. A sign-in to its servers is answered by that extension only.
- **Asking first:** an extension can start a program on your computer (native messaging) or get more access only after you say yes. Apart from the store contacts below, Aphrodite doesn't send anything about your extensions anywhere.
- **Stores:** Aphrodite contacts the Chrome Web Store (Google) or Firefox Add-ons (Mozilla) only when you choose to add an extension from one, or press **Check for updates**, after a notice saying what they'll see. They see your IP address and which extensions you ask about; Google also sees a browser version number, which its store needs to pick the right file. No cookies or sign-in are sent.

## Error reports websites ask for

A website can ask a browser to send it error reports up to a minute after you've left the page (the Reporting API and Network Error Logging). Aphrodite never sends these.

## Making Aphrodite your default browser

If you make Aphrodite your default browser, only your operating system's own settings change (on Windows, you choose it in Default apps; on Linux, Aphrodite asks your system to use it, and an AppImage adds a shortcut file to your account's applications folder). Nothing is sent anywhere.

## Connections Aphrodite makes by itself

To work, Aphrodite connects to the services below. None of them receive your browsing history from Aphrodite, and none of these requests carries a cookie or an identifier. Like any internet connection, they can see your IP address, and their own privacy policies apply.

| Service | Why | When |
|---|---|---|
| GitHub (github.com, raw.githubusercontent.com) | Checking for and downloading Aphrodite updates (from the public SolidCarbon Works releases page, with no account, key or identifier: every copy of Aphrodite sends the same request), and downloading filter lists published by Ghostery | At start-up and every few hours |
| AdGuard (filters.adtidy.org) | Ad and link-tracking filter lists | Ad lists about once a day, the link-tracking list about once a week |
| malware-filter (malware-filter.gitlab.io) | Phishing and malware lists, checked on your device | About twice a day, or when you choose Update now |
| Your chosen secure-DNS provider (Quad9, Cloudflare or Mullvad) | Looking up website addresses privately | When secure DNS is on. Behind a VPN app also when it is off, through the VPN: for unmasking disguised trackers, for testing the VPN app, and for checking names when the app doesn't refuse ones that point at your network (see "Your computer and home network") |
| Cloudflare (cloudflare.com/cdn-cgi/trace) and ipinfo.io | Showing what websites see about your connection, and matching the time zone to your VPN | Only when you open that panel or turn on the VPN time-zone setting |
| Your search engine (DuckDuckGo by default) | Search results | Only when you press Enter on a search. Suggestions while you type come from your own tabs, bookmarks and history, on your device |
| IAB Europe (vendor-list.consensu.org) | The public list of advertising companies' names, so a site's consent record can show who your "yes" went to | At most once a week, only when you open a privacy receipt or Cookies & site data |
| Sites you return to | Their privacy-policy page, to tell you when it changed (Tell me what changed) | At most every 3 days per site, only for the site you're on, over HTTPS only (redirects included), without cookies or logins |
| Pages you clip | Checking the part of the page you clipped | At the interval you chose for each clip; "anonymously" without your cookies, "as you" with them |
| GitHub (github.com and its download servers) | Downloading the assistant's models from the public SolidCarbon Works releases page, with no account or key | Only when you turn on the assistant and choose Download for a model |
| Chrome Web Store (Google: clients2.google.com and its download servers) and Firefox Add-ons (Mozilla: addons.mozilla.org) | Downloading an extension you chose, and checking your extensions from them for updates | Only when you add one from a store or press Check for updates, after a notice (see "Extensions") |

Lists of dangerous sites are downloaded to your device and checked there, and one more list of scam sites (Phishing.Database) comes with Aphrodite itself. They are checked for the pages you open, your downloads, and everything a page loads from another site. The addresses you visit are **not** sent to anyone for checking.

The assistant, if you turn it on, runs entirely on your device. What you ask it and the pages it reads are **not** sent anywhere. Its engine runs in a process of its own in which every way to the network is closed (sockets, name lookups, Electron's network stack, other programs and threads), and every build checks this. To suggest a model that suits your computer, Aphrodite looks at how much memory it has and at its graphics card, on your device only; this isn't sent anywhere.

By default, chats are kept in memory only and are gone when you start a new chat or close the window. If you turn on **Save chats** (Settings → Assistant), each chat, with the text of the page it was about, is saved on your device so you can open it again. Saved chats are encrypted with your operating system's protection for your account on that computer (on Windows, DPAPI), are never saved for private windows, and are deleted after the time you choose (30 days unless you change it), when you delete them, or when you clear your browsing history. Saving is turned off where the system offers no such protection. Anyone signed in to your account on that computer can open them in Aphrodite, just like your browsing history.

## Fingerprint protection

Sites can try to recognise your device from details like your graphics card, screen and fonts. Aphrodite gives each site **made-up** answers instead:
- **Each site gets different values,** so the usual fingerprinting scripts can't link your visits to each other. It can't make you impossible to recognise: your screen size, installed fonts and graphics card family stay real, and a determined tracker can still try to filter the noise out.
- **A site sees the same values every time you visit, for as long as you keep its cookies.** It can already recognise you from those cookies, so this tells it nothing new. It also means sites you log in to see a returning device, not a stranger every time, which is what security checks expect.
- **Clearing a site's data, "Forget me when I close this site" and "Clear data when Aphrodite closes"** all give that site new values. Each private window gets values of its own.
- **Your real window size and position stay hidden.** Pages see a normal browser window around the page, also in the positions mouse events report.

## Security checks (bot checks)

Sign-up, login and payment pages often run a security check that tells people from bots, such as Arkose (used by GitHub), DataDome, hCaptcha, reCAPTCHA or Cloudflare Turnstile. These are run by the website you're on, under its own privacy policy.

You choose what happens in Settings → Shields → Bot checks:
- **Allow (recommended):** security checks load, as well as the messages they send back to their own service. Other companies' trackers stay blocked.
- **Only on sites I trust:** the same, but only on sites you've marked with "Trust this site".
- **Block everywhere:** security checks don't load. Sign-ups and logins on those sites will usually fail.

Their cookies are kept only until Aphrodite closes, so they can't build a history of you.

**"Trust this site"** is a per-site choice, made in the shield panel. On a site you trust:
- it and its frames get **real** device details;
- third-party cookies are allowed there;
- the site's own background reports to itself (its own analytics) go through.

Ads and other companies' trackers stay blocked on trusted sites. Use it only for sites you rely on and that break without it.

## Websites

Websites you visit can collect data under their own policies. Aphrodite blocks many trackers and can reject cookie consent pop-ups automatically, but it can't guarantee that no site collects anything.

## Children

Aphrodite collects no personal data from anyone, including children.

## Your rights

As we hold no personal data about you, there's nothing for us to access, correct or delete. To remove single pages from your history, use History; to remove all your data, clear your browsing data in Aphrodite's settings, or uninstall Aphrodite and delete its profile folder.

## Changes and contact

If this policy changes, the new version will ship with an update and appear here.

SolidCarbon Works · Bulgaria · Questions: **solidcarbonworks@gmail.com**
