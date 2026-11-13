# Aphrodite privacy policy

**Effective 13 November 2026**

Short version: **Aphrodite doesn't collect your data.** There's no account, no telemetry, no crash reporting and no analytics. Your history, bookmarks and settings stay on your device.

## What stays on your device

These are stored only in your Aphrodite profile folder on your computer, and we never receive them:
- browsing history, bookmarks, open tabs and workspaces
- cookies, site permissions and consent choices
- downloads and settings
- the made-up device details each site sees (see below)
- signatures you ask the PDF editor to remember (kept as pictures; never in a private window)

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

## Links you paste or open from other apps

When you paste a link into the address bar or the new tab page, or another app opens a link in Aphrodite, Aphrodite checks it **on your device** before it loads: for known IP-logging services, addresses made to look like a well-known site, disguised links, the redirects of that first load, and a page that pretends to be a well-known site to get your password. To recognise well-known sites, it uses a list of popular websites that ships with Aphrodite, and your bookmarks; in **Strict mode** (on unless you turn it off), a link to a site on neither asks before opening. **The links themselves aren't sent anywhere and nothing is looked up online.** Turn the checks or Strict mode off in Settings → Privacy & security.

## Your computer and home network

A website's code runs on your computer, so it could try to reach programs running on it and devices on your network (router, printer, cameras). Aphrodite refuses that, and asks you first when a website tries to send you to such an address. Each attempt is listed on that site's privacy receipt, which stays on your device.

To do this, every website address lookup passes through a small relay inside Aphrodite. It keeps nothing on disk and remembers names only as scrambled fingerprints, until Aphrodite closes.

If you use a VPN app, Aphrodite tests it in the background, about every ten minutes: it asks the app for a public test name that points at your own computer (such as localtest.me) and watches whether a connection arrives. If the app doesn't refuse such names, Aphrodite looks up the names pages use itself, encrypted, at your secure-DNS provider (Quad9 unless you chose another), **through your VPN**. This happens even when secure DNS is turned off, because the alternative would be a lookup outside your VPN.

## Error reports websites ask for

A website can ask a browser to send it error reports up to a minute after you've left the page (the Reporting API and Network Error Logging). Aphrodite never sends these.

## Making Aphrodite your default browser

If you make Aphrodite your default browser, only your operating system's own settings change (on Windows, you choose it in Default apps; on Linux, Aphrodite asks your system to use it, and an AppImage adds a shortcut file to your account's applications folder). Nothing is sent anywhere.

## Connections Aphrodite makes by itself

To work, Aphrodite connects to the services below. None of them receive your browsing history from Aphrodite. Like any internet connection, they can see your IP address, and their own privacy policies apply.

| Service | Why | When |
|---|---|---|
| GitHub (github.com, raw.githubusercontent.com) | Checking for and downloading Aphrodite updates (from the public SolidCarbon Works releases page, with no account or key), and downloading filter lists published by Ghostery | At start-up and every few hours |
| AdGuard (filters.adtidy.org) | Ad and link-tracking filter lists | About once a day |
| malware-filter (malware-filter.gitlab.io) | Phishing and malware lists, checked on your device | About twice a day, or when you choose Update now |
| Your chosen secure-DNS provider (Quad9, Cloudflare or Mullvad) | Looking up website addresses privately | When secure DNS is on. Behind a VPN app also when it is off, through the VPN: for unmasking disguised trackers, for testing the VPN app, and for checking names when the app doesn't refuse ones that point at your network (see "Your computer and home network") |
| Cloudflare (cloudflare.com/cdn-cgi/trace) and ipinfo.io | Showing what websites see about your connection, and matching the time zone to your VPN | Only when you open that panel or turn on the VPN time-zone setting |
| Your search engine (DuckDuckGo by default) | Search suggestions and results | When you type in the address bar or search |
| GitHub (github.com and its download servers) | Downloading the assistant's models from the public SolidCarbon Works releases page, with no account or key | Only when you turn on the assistant and choose Download for a model |

Lists of dangerous sites are downloaded to your device and checked there, and one more list of scam sites (Phishing.Database) comes with Aphrodite itself. The addresses you visit are **not** sent to anyone for checking.

The assistant, if you turn it on, runs entirely on your device. What you ask it and the pages it reads are **not** sent anywhere, and its engine has no network access. To suggest a model that suits your computer, Aphrodite looks at how much memory it has and at its graphics card, on your device only; this isn't sent anywhere.

By default, chats are kept in memory only and are gone when you start a new chat or close the window. If you turn on **Save chats** (Settings → Assistant), each chat, with the text of the page it was about, is saved on your device so you can open it again. Saved chats are encrypted with your operating system's protection for your account on that computer (on Windows, DPAPI), are never saved for private windows, and are deleted after the time you choose (30 days unless you change it), when you delete them, or when you clear your browsing history. Saving is turned off where the system offers no such protection. Anyone signed in to your account on that computer can open them in Aphrodite, just like your browsing history.

## Fingerprint protection

Sites can try to recognise your device from details like your graphics card, screen and fonts. Aphrodite gives each site **made-up** answers instead:
- **Each site gets different values,** so sites can't link your visits to each other.
- **A site sees the same values every time you visit, for as long as you keep its cookies.** It can already recognise you from those cookies, so this tells it nothing new. It also means sites you log in to see a returning device, not a stranger every time, which is what security checks expect.
- **Clearing a site's data, "Forget me when I close this site" and "Clear data when Aphrodite closes"** all give that site new values. Private windows get new ones every time you open Aphrodite.
- **Your real window size and position stay hidden.** Pages see a normal browser window around the page.

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

SolidCarbon Works · Bulgaria · Questions: **simplecarbon@proton.me**
