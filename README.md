# Project B

A browser for Windows, built on Firefox for heavy multitasking and for security.

This repository holds Project B's releases: the installer, its checksums and the release notes. **[Download the latest release](https://github.com/nikolozdolidze/project-b-releases/releases/latest).**

- [What it does](#what-it-does)
  - [Many pages at once](#many-pages-at-once)
  - [Privacy and security](#privacy-and-security)
  - [Passwords, addresses and cards](#passwords-addresses-and-cards)
  - [Everyday browsing](#everyday-browsing)
  - [Settings](#settings)
- [Keyboard shortcuts](#keyboard-shortcuts)
- [Installing](#installing)
- [Uninstalling](#uninstalling)
- [Checking the download](#checking-the-download)
- [Updates](#updates)
- [Known limits](#known-limits)
- [Licenses](#licenses)

## What it does

### Many pages at once

- **Splits.** Any tab can become a split: panes beside and above one another, as many as you like, each with its own tabs. Split the pane you're in to the right or downwards, drag a tab onto a page to put it beside it, or let **snap layouts** lay a split out in one go and fill its spaces from your other tabs. Drag the borders to resize panes, or make them all equal. New panes slide in from the side they're split off to.
- **Each pane has its own bar**: its tabs and its own address bar. The bar slides in when you point at the pane's top edge, or stays put once pinned. The pane under the pointer takes the focus, and you can move between panes with Ctrl+Alt and the arrows. In a pane with many tabs, they can scroll instead of shrinking.
- **The tab strip** holds single tabs and splits side by side. Point at a tab for a picture of its page and how much memory it's using. Drag tabs to reorder them, into a split, into another window, or out into a new window. Pin a tab to keep it at the start.
- **Saved splits.** Save a split to the new tab page and open it again later in one go. It remembers which of its tabs were sandboxed or private, and opens those in fresh sandboxes, signed out.
- **Resting tabs.** Tabs you haven't looked at for a while hibernate (frozen, their memory handed back to Windows; they wake instantly, exactly as they were), and later sleep (unloaded, their history kept). You choose the timings, or rest a tab yourself from its menu. Pinned tabs and tabs playing sound never rest.
- **Every tab has its own volume.** A tab playing sound shows a speaker: click it to mute, turn the mouse wheel over it to raise or lower the volume, or right-click the tab for a volume slider. A video can play quietly while a call stays loud.
- **The command palette** (Ctrl+K) has every command the browser has, and your history: type what you're after. It also opens from the menu button, as a regular browser menu with search at the top.
- **The sidebar** (Ctrl+B), on the left or right of the window, with panels for bookmarks, history, downloads, your tabs and notes. Pin it open beside the page, or let it slide away when the pointer leaves.
  - **Sites pinned to the sidebar** live apart from your tabs: a chat or music site always at hand. Each can have sign-ins of its own, ask for the phone layout, and sleep when unused. Pin one from a page's or a link's right-click menu, or move a tab there.
  - **Notes**: a general note, and a note for each site, shown beside its page.
- **Right-click almost anything.** A tab: pin it, rest it, its volume, sandbox it or make it private, open a sandboxed or private copy beside it, save its split, close it or the tabs around it. The + button: a private tab, one with Tor, or a sandbox. The strip: new tabs and windows. A link: open it in a new tab, in a split, in a new window, in a private tab or one with Tor, or pin it to the sidebar. The address bar: paste and go in one.

### Privacy and security

- **Sandboxes.** A sandboxed tab has sign-ins of its own, so you can use two accounts on one site side by side. Everything it opens stays in its sandbox, and each sandbox has a number and a colour on its tabs, its pane's outline and the address bar. While it lasts, a sandbox is as private as a private window: its pages aren't kept in history, what you type into its forms isn't remembered, its downloads aren't added to your download history, it isn't written into the saved session, and nothing it loads is cached on disk. When its last tab closes, everything it kept (cookies, storage, permissions) is wiped, and after a crash that happens before any page loads.
- **Private tabs** are sandboxes that start on a new tab page, so a private tab can sit right beside a normal one.
- **Private tabs with Tor.** Every request from such a tab goes through Tor, DNS included, with nothing ever falling back to a direct connection. WebRTC is removed from its pages, onion sites work, and typing an onion address in a normal tab opens it in a new Tor tab. You can ask for a new Tor circuit for a tab. Tor ships with the browser and starts when you first need it.
- **Private and sandbox windows**: every new tab in a private window shares one private sandbox, and every new tab in a sandbox window gets its own. Unlike Firefox's private windows, tabs can move in and out of them.
- **Shields** block ads and trackers on every site, using EasyList, EasyPrivacy, Peter Lowe's list and uBlock Origin's lists. They also hide ad leftovers on pages, strip tracking parameters from addresses, and skip redirect trackers. Turn them off for a single site from the site menu.
- **Phishing and malware sites** are stopped before they load, with a warning page. You can still go on if you know better.
- **Fingerprinting protection.** Firefox's protection is on in every window. On top of it, what sites can measure of your computer (canvas, WebGL, audio, the number of processor cores) varies from site to site and session to session, so it can't be used to follow you. A Strict setting goes further.
- **HTTPS only.** An http site opens only after a warning, and you can go on over http for that site if you choose.
- **Secure DNS** with Quad9 (which also blocks domains known to be malicious), Cloudflare or Google, over HTTPS. Your computer's own DNS is used only when the provider can't be reached, or never, if you turn on strict mode.
- **Revoked certificates** are checked against lists downloaded in full, so no one is asked about the sites you visit.
- **Third-party cookies** are kept apart per site, and sites are told not to sell or share your data (Global Privacy Control).
- **Downloads held back**: files that can run code, a web page or picture a site downloaded by itself, and anything that came over plain http wait for you to keep or discard them. One never kept is deleted when the browser closes.
- **More guards.** A frame or picture from another site can't ask for a username and password. Files on other computers (`\\server\share`) are never opened. Links are never handed to Windows handlers that have been used to run code. WebRTC uses only your default network connection.
- **Nothing about you is sent to Mozilla**: no telemetry, studies or crash reports, and no Firefox account, sync or email masks. There are no sponsored tiles, suggestions, AI chat or promotions either.

### Passwords, addresses and cards

**Your passwords, addresses and cards never leave your computer through the browser.** There's no sync, no account and no cloud: they're kept in an encrypted vault on this computer, and only go out when you fill one into a site, or export or back them up to a file yourself. (A backup is encrypted; an exported CSV file isn't. Either goes wherever you save it, so a folder that OneDrive syncs, for instance, uploads it.)

- **Kept in a vault of their own**, not Firefox's store: every bit of them encrypted (sites and usernames too) with a key only your primary password opens (Argon2id, then AES-256-GCM). They're decrypted only in the browser's memory, and even then a password stays encrypted until it's used.
- **The primary password must be strong**: a meter shows how strong as you type.
- **It locks itself** when you step away from the computer or leave the browser unused for a few minutes (you choose how long), when Windows locks or sleeps, and when the browser closes. Or set it to **always ask**: unlocked for one use, then locked again at once.
- **Windows Hello and a recovery key**, if you want them, as other ways to unlock.
- **Filling in**: sign-in forms, addresses and cards are found and filled as in Firefox, from your vault. The browser asks whether to save new and changed passwords, addresses and cards, and asks to unlock only when you click into a sign-in field, never as a page loads. A card number stays sealed, even from the page's own process, until you give your primary password again to fill it (that holds for a few minutes).
- **The Passwords page**: see, copy, change, generate, add and delete passwords. Copied passwords and usernames are kept out of Windows' clipboard history and cloud clipboard, and a copied password is cleared after a minute. Addresses and cards work the same, and a card's full number shows only after your primary password. There's also a checkup of weak and reused passwords, the vault's settings, encrypted backups and restoring them, importing a CSV file from Chrome, Edge and others, exporting to CSV (asks for your primary password every time), and clearing it all (asks for your primary password, then for you to type CLEAR).

### Everyday browsing

- **The address bar** shows the site with its host standing out. As you type, it suggests searches from your search engine (Google, Bing, DuckDuckGo or Brave Search), your bookmarks and your history. Suggestions from the search engine aren't asked for in private or Tor tabs. A star bookmarks the page (Ctrl+D).
- **The site menu**, in the address bar: the connection's security; what the site may do (camera, microphone, location, notifications, MIDI devices, virtual reality, autoplay, storage); pop-ups and redirects; whether it may ask before you leave; its shields; and its zoom. Blocked pop-ups are offered from the address bar.
- **Sites' questions** (a site asking for your location, camera and so on) and pages' alerts and sign-ins appear in the browser's own prompt. Alt+Shift+A answers the waiting one. A camera, microphone or speakers come with the choice of which, the default already chosen. Closing a question just turns the site down this once.
- **The new tab page**: your shortcuts (drag them into order; undo a removal), your saved splits, and a background picture of your own (from a file or a link), with blur and frosted panels. Typing there goes straight into the address bar.
- **Sharing your screen**: windows and screens are shown as pictures, each on its own tab, and the one you choose plays live before you share it, with a warning for a whole screen or a Project B window. While you share, a small bar stays on top of everything: what's shared and with which site (click to go back to that tab), Stop sharing, and Hide.
- **History** (Ctrl+H): the pages you visited, by day, searchable, each removable. Clear browsing data by time range: history, downloads, cookies and site data, cache.
- **Downloads** (Ctrl+J): the downloads button shows progress, and its list and the downloads page let you open, show in folder, copy the address, retry, keep or discard a held-back file, and delete.
- **Bookmarks** in the sidebar, in folders (Ctrl+Shift+O).
- **Extensions** from addons.mozilla.org, with a button of their own beside the address bar. Pin any to the toolbar or into the address bar, with its icon, badge and popup. For each one, choose whether it may run in private tabs, Tor tabs and sandboxes; by default it's kept out of private and Tor tabs. The extensions page (Ctrl+Shift+A) turns them on and off, sets their permissions, options, updates and keyboard shortcuts, and installs from a file.
- **Zoom per site**, from 25% to 500%. Also find in page, print and developer tools.
- **Clear error pages**: why a page couldn't load, a warning before an http site or a dangerous one, and a page for a tab whose page crashed. Reload tries again.
- **The welcome tour** on first start: what the browser does, a step at a time, with importing bookmarks, history, passwords and cards from Chrome, Edge, Brave, Opera, Vivaldi and others on the same computer. It's in the command palette ("Welcome") to see again.

### Settings

- **Appearance**: light, dark or follow Windows, and an accent colour (ours, Windows' own, or any you pick).
- **On startup**: continue where you left off (tabs load when you go to them) or start with a new tab page. Make it your default browser.
- **Address bar and search**: the search engine, and search suggestions.
- **Toolbar**: always show the downloads button, and drag the toolbar's buttons into the order you like.
- **Tabs and panes**: sleeping tabs and when they hibernate and sleep, how far the mouse wheel turns a tab's volume, and scrollable tabs in split panes.
- **Sidebar**: its side, pinning, hiding, showing at the window's edge, its button in a split's corner, and which panels it has.
- **Keyboard shortcuts**: every command and its keys, each to change (click it and press new keys), add to, take away or put back.
- **Privacy and security**: clearing browsing data, shields, sites you've changed something for, always using secure connections, fingerprinting protection (Standard or Strict), and secure DNS.
- **Downloads**: where they go, or ask each time.
- **New tab page**: the background picture, its blur, and frosted panels.
- **About**: the version, and checking for updates.

## Keyboard shortcuts

These are the defaults: change any of them in Settings > Keyboard shortcuts. Click a shortcut and press the new keys (Ctrl or Alt with a key, or an F key); Backspace takes it away. Keys another command already has are asked about first, keys that would break typing (Ctrl+C, Ctrl+V and the like) are refused, and your keys win over Firefox's own. Every command, with or without keys, is also in the command palette (Ctrl+K).

| Keys | Command |
|---|---|
| Ctrl+T | New tab |
| Ctrl+N | New window |
| Ctrl+Shift+N | New private window |
| Ctrl+W, Ctrl+F4 | Close tab |
| Ctrl+Shift+T | Reopen closed tab |
| Ctrl+Tab, Ctrl+PageDown | Next tab |
| Ctrl+Shift+Tab, Ctrl+PageUp | Previous tab |
| Ctrl+L, Alt+D, F6 | Address bar |
| Ctrl+K, Ctrl+Shift+P | Command palette |
| Alt+Left, Alt+Right | Back, forward |
| F5, Ctrl+R | Reload |
| Ctrl+F | Find in page |
| F3, Ctrl+G / Shift+F3, Ctrl+Shift+G | Find next / previous |
| Ctrl+=, Ctrl+-, Ctrl+0 | Zoom in, out, back to 100% |
| Ctrl+\ | Split pane right |
| Ctrl+Shift+\ | Split pane down |
| Ctrl+Alt+Arrows | Move to the pane left, right, above, below |
| Ctrl+Shift+W | Close pane and its tabs |
| Ctrl+Shift+B | Keep pane bar visible |
| Ctrl+B | Sidebar |
| Ctrl+D | Bookmark this page |
| Ctrl+Shift+O | Bookmarks |
| Ctrl+H | History |
| Ctrl+J | Downloads |
| Ctrl+Shift+A | Extensions |
| Ctrl+, | Settings |
| Ctrl+Shift+Delete | Clear browsing data |
| Alt+Shift+A | Answer a site's question |
| Ctrl+P | Print |
| F12, Ctrl+Shift+I | Developer tools |
| Ctrl+Shift+Q | Exit |

## Installing

Download `projectb-<firefox version>.en-US.win64.installer.exe` from the latest release and run it. The installer isn't code-signed yet, so Windows SmartScreen says it "protected your PC": choose **More info**, then **Run anyway**.

Then **Install**. It installs as **Project B** in `C:\Program Files\Project B`, with a Start menu entry, a desktop shortcut, a taskbar pin and an uninstaller; **Options** lets you choose another folder, and leave out the shortcut or the pin. Installing in Program Files needs an administrator's permission, which Windows asks for. When it's done, **Open Project B**.

Run over a copy that's installed already, it offers **Update** instead, and keeps your profile: tabs, passwords and settings.

## Uninstalling

Uninstall from Windows' Installed apps. Project B's own uninstaller removes the program and its shortcuts. Turn on **Also delete my data** to delete everything Project B keeps on this computer as well: history, saved passwords and cards, bookmarks, cookies, sandboxes, Tor's data, settings and the Windows Hello key. Your downloaded files stay, and another Firefox on the same computer is never touched. Left off, your data is kept for when you install again.

## Checking the download

Each release has a `SHA256SUMS` file. In a terminal, in the folder you downloaded to:

```
certutil -hashfile projectb-158.0.1.en-US.win64.installer.exe SHA256
```

The result should match the installer's line in `SHA256SUMS`.

## Updates

Project B looks for a newer release here once a day (Settings > About > Check for updates, to look now). It downloads the new installer and checks it against that release's `SHA256SUMS`. When you choose **Install and restart**, it closes, the installer puts the new version in place with its progress showing, and Project B starts again.

## Known limits

- Windows only, 64-bit.
- Not code-signed yet (see Installing).
- Tor tabs send everything through Tor, but to a site they look like Firefox on Windows, not like Tor Browser.
- The camera question doesn't show a live preview of the camera yet.

## Licenses

Project B's own code is under the Mozilla Public License 2.0. It's built on [Firefox](https://www.firefox.com/) (Mozilla Public License 2.0), whose source is at [github.com/mozilla-firefox/firefox](https://github.com/mozilla-firefox/firefox). It includes the Tor Project's `tor.exe`, unchanged (GNU GPL 3.0; its source is at [dist.torproject.org](https://dist.torproject.org/)). The installer's `tor\docs` folder holds Tor's licenses and where its source is.
