# Aphrodite privacy policy

**Effective 11 November 2026**

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

## Connections Aphrodite makes by itself

To work, Aphrodite connects to the services below. None of them receive your browsing history from Aphrodite. Like any internet connection, they can see your IP address, and their own privacy policies apply.

| Service | Why | When |
|---|---|---|
| GitHub (github.com, raw.githubusercontent.com) | Checking for and downloading Aphrodite updates (from the public SolidCarbon Works releases page, with no account or key), and downloading filter lists published by Ghostery | At start-up and every few hours |
| AdGuard (filters.adtidy.org) | Ad and link-tracking filter lists | About once a day |
| malware-filter (malware-filter.gitlab.io) | Phishing and malware lists, checked on your device | About twice a day |
| Your chosen secure-DNS provider (Quad9, Cloudflare or Mullvad) | Looking up website addresses privately | Only if you turn on secure DNS |
| Cloudflare (cloudflare.com/cdn-cgi/trace) and ipinfo.io | Showing what websites see about your connection, and matching the time zone to your VPN | Only when you open that panel or turn on the VPN time-zone setting |
| Your search engine (DuckDuckGo by default) | Search suggestions and results | When you type in the address bar or search |

Lists of dangerous sites are downloaded to your device and checked there. The addresses you visit are **not** sent to anyone for checking.

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

As we hold no personal data about you, there's nothing for us to access, correct or delete. To remove all your data, clear your browsing data in Aphrodite's settings, or uninstall Aphrodite and delete its profile folder.

## Changes and contact

If this policy changes, the new version will ship with an update and appear here.

SolidCarbon Works · Bulgaria · Questions: **simplecarbon@proton.me**
