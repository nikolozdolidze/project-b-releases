# Mosaic Browser

A browser for Windows, built on Firefox for heavy multitasking and for security. It was called Project B until 0.4.5.

This repository holds Mosaic Browser's releases: the installer, its checksums and the release notes. **[Download the latest release](https://github.com/nikolozdolidze/project-b-releases/releases/latest).**

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

- **Splits.** Any tab can become a split: panes beside and above one another, as many as you like, each with its own tabs. Split the pane you're in to the right or downwards, drag a tab onto a page to put it beside it, or let **snap layouts** lay a split out in one go and fill its spaces from your other tabs. Drag the borders to resize panes, or make them all equal. New panes slide in from the side they're split off to. Panes keep at least 280×200 px where there's room: a split that would make one smaller says so instead.
- **Each pane has its own bar**: its tabs and its own address bar. The bar slides in when you point at the pane's top edge, or stays put once pinned. The pane under the pointer takes the focus, and you can move between panes with Ctrl+Alt and the arrows. In a pane with many tabs, they can scroll instead of shrinking. In a narrow pane, the address bar keeps its room and the other buttons move into the pane's menu, where they work as they did.
- **The tab strip** holds single tabs and splits side by side. Point at a tab for a picture of its page and how much memory it's using. Drag tabs to reorder them, into a split, into another window, or out into a new window. Pin a tab to keep it at the start. Ctrl+1 to Ctrl+8 go to the strip's first eight, Ctrl+9 to its last.
- **Workspaces.** Named sets of tabs in one window, the strip showing one set at a time: a "Work" and a "Home", say. Switch between them from the pill at the start of the strip, move a tab to another from its right-click menu, and rename or delete one. They come back as they were when the browser restarts.
- **Recently closed and saved sessions.** Ctrl+Shift+T reopens the last closed tab, or a whole closed window with its splits. The History page lists what you closed lately, and saves a window's tabs and splits as a session to open again later, in a new window or the one you're in (only the tabs in front load until you go to the others).
- **Saved splits.** Save a split to the new tab page and open it again later in one go. It remembers which of its tabs were sandboxed or private, and opens those in fresh sandboxes, signed out.
- **Resting tabs.** Tabs you haven't looked at for a while hibernate (frozen, their memory handed back to Windows; they wake instantly, exactly as they were), and later sleep (unloaded, their history kept). You choose the timings, or rest a tab yourself from its menu. Pinned tabs and tabs playing sound never rest.
- **Every tab has its own volume.** A tab playing sound shows a speaker: click it to mute, turn the mouse wheel over it to raise or lower the volume, or right-click the tab for a volume slider. A video can play quietly while a call stays loud.
- **Picture-in-picture.** Right-click a video and choose **Picture-in-picture** to watch it in a small window of its own, on top of everything else. A tab with a video (long enough, with sound) offers it in its right-click menu too, so you can pop the video out without going to the tab: it picks the video that's playing, or else the longest. While it's out, the same items say **Exit picture-in-picture**. Ctrl+Shift+] pops out the video of the tab in front.
- **Video sandboxing.** A video going full screen fills only its tab's pane, not the whole screen, so the rest of a split stays in view. Turn it on for a tab from its right-click menu (in a split, from its pane's bar), or for every tab in a split in Settings > Tabs and panes. Esc or the player's own button leaves full screen as usual.
- **The command palette** (Ctrl+K) has every command the browser has, and your history: type what you're after. It also opens from the menu button, as a regular browser menu with search at the top.
- **The sidebar** (Ctrl+B), on the left or right of the window, with panels for bookmarks, history, downloads, your tabs and notes. Pin it open beside the page, or let it slide away when the pointer leaves.
  - **Sites pinned to the sidebar** live apart from your tabs: a chat or music site always at hand. Each can have sign-ins of its own, ask for the phone layout, and sleep when unused. Pin one from a page's or a link's right-click menu, or move a tab there.
  - **Notes**: a general note, and a note for each site, shown beside its page.
  - **Custom panels**: your own pages in the sidebar, written in HTML, CSS and JavaScript in Settings > Custom panels (start from a blank page or a scratchpad). Each runs like a tab, starting when you open it and sleeping when unused, or keeps running while the browser is open, so its timers and reminders go on while it's closed. What a panel saves is its own: no site, file or other panel can read it, and it stays through restarts and clearing browsing data until you delete the panel. A number in brackets at the start of its title shows on its icon, and it can show notifications.
- **Right-click almost anything.** A tab: pin it, rest it, its volume, pop its video out into picture-in-picture, video sandboxing, sandbox it or make it private, open a sandboxed or private copy beside it, move it to another workspace, save its split, close it or the tabs around it. Anything on a page: block it (Block element…). The + button: a private tab, one with Tor, or a sandbox. The strip: new tabs and windows. A link: open it in a new tab, in a split, in a new window, in a private tab or one with Tor, or pin it to the sidebar. A video: play, mute, loop, its controls, picture-in-picture. The address bar: paste and go in one.

### Privacy and security

- **Sandboxes.** A sandboxed tab has sign-ins of its own, so you can use two accounts on one site side by side. Everything it opens stays in its sandbox, and each sandbox has a number and a colour on its tabs, its pane's outline and the address bar. While it lasts, a sandbox is as private as a private window: its pages aren't kept in history, what you type into its forms isn't remembered, its downloads aren't added to your download history, it isn't written into the saved session, and nothing it loads is cached on disk. When its last tab closes, everything it kept (cookies, storage, permissions) is wiped, and after a crash that happens before any page loads.
- **Private tabs** are sandboxes that start on a new tab page, so a private tab can sit right beside a normal one. A private tab (and one with Tor) fills nothing in and offers to save nothing: no saved sign-ins, addresses or cards, and nothing typed there kept. Its downloads are its own, as a private window's are: only its tabs' downloads button, list and downloads page show them, and your other tabs' never do.
- **Private tabs with Tor.** Every request from such a tab goes through Tor, DNS included, with nothing ever falling back to a direct connection. WebRTC is removed from its pages, onion sites work, and typing an onion address in a normal tab opens it in a new Tor tab. You can ask for a new Tor circuit for a tab. Tor ships with the browser and starts when you first need it.
- **Private and sandbox windows**: every new tab in a private window shares one private sandbox, and every new tab in a sandbox window gets its own. Unlike Firefox's private windows, tabs can move in and out of them.
- **Shields** block ads and trackers on every site, using EasyList, EasyPrivacy, Peter Lowe's list and uBlock Origin's lists. They also hide ad leftovers on pages, hide "we use cookies" notices (or turn them down where that's what makes them go), strip tracking parameters from addresses, skip redirect trackers, and stop pages a list says not to open at all (badware), with a warning you can go past. Turn them off for a single site from the site menu.
  - **Make them your own** (Settings > Ad blocking): add any number of filter lists by their address, and write your own filters, which win over the lists, including exceptions. The lists update once a day on their own, or only when you press **Update now**; a list is downloaded again only if it changed.
  - **Block an element**: right-click anything on a page and choose **Block element…** (or use the site menu). The picker outlines what's under the pointer; click to choose, make it broader or narrower, and press Enter to hide it on that site from then on. The page doesn't see your clicks while you pick. What you've blocked is in your own filters, to undo.
- **Phishing and malware sites** are stopped before they load, with a warning page. You can still go on if you know better. Typing a saved password into the wrong site is warned of too (see [Passwords](#passwords-addresses-and-cards)).
- **Fingerprinting protection.** Firefox's protection is on in every window. On top of it, what sites can measure of your computer (canvas, WebGL, audio, the number of processor cores) varies from site to site and session to session, so it can't be used to follow you. A Strict setting goes further.
- **HTTPS only.** An http site opens only after a warning, and you can go on over http for that site if you choose.
- **Secure DNS** with Quad9 (which also blocks domains known to be malicious), Cloudflare or Google, over HTTPS. Your computer's own DNS is used only when the provider can't be reached, or never, if you turn on strict mode.
- **Revoked certificates** are checked against lists downloaded in full, so no one is asked about the sites you visit.
- **Third-party cookies** are kept apart per site, and sites are told not to sell or share your data (Global Privacy Control).
- **Each site's cookies and data**: the site menu says how many cookies a site keeps, and Settings lists them, to delete one or all. Block a site's cookies, keep them only until the browser closes, clear everything it keeps, have it **forgotten when its tabs close**, or have it **always open in a sandbox** (or a private tab).
- **Downloads held back**: files that can run code, a web page or picture a site downloaded by itself, and anything that came over plain http wait for you to keep or discard them. One never kept is deleted when the browser closes. Nothing about a download is sent to Google to check it, as Firefox does for programs it doesn't know.
- **More guards.** A frame or picture from another site can't ask for a username and password. Files on other computers (`\\server\share`) are never opened. Links are never handed to Windows handlers that have been used to run code. WebRTC uses only your default network connection.
- **Nothing about you is sent to Mozilla**: no telemetry, studies or crash reports, and no Firefox account, sync or email masks. There are no sponsored tiles, suggestions, AI chat or promotions either.

### Passwords, addresses and cards

**Your passwords, addresses and cards never leave your computer through the browser.** There's no sync, no account and no cloud: they're kept in an encrypted vault on this computer, and only go out when you fill one into a site, or export or back them up to a file yourself. (A backup is encrypted; an exported CSV file isn't. Either goes wherever you save it, so a folder that OneDrive syncs, for instance, uploads it.)

- **Kept in a vault of their own**, not Firefox's store: every bit of them encrypted (sites and usernames too) with a key only your primary password opens (Argon2id, then AES-256-GCM). They're decrypted only in the browser's memory, and even then a password stays encrypted until it's used.
- **The primary password must be strong**: a meter shows how strong as you type.
- **It locks itself** when you step away from the computer or leave the browser unused for a few minutes (you choose how long), when Windows locks or sleeps, and when the browser closes. Or set it to **always ask**: unlocked for one use, then locked again at once.
- **Windows Hello and a recovery key**, if you want them, as other ways to unlock.
- **Filling in**: sign-ins aren't filled in on their own. Click a sign-in field and the site's saved sign-ins are listed under it; the one you pick is filled in (turn filling in as pages load back on in the Passwords page's settings). Addresses and cards are offered as you click their fields. The browser asks whether to save new and changed passwords, addresses and cards, and asks to unlock only when you click into a sign-in field, never as a page loads; say no on a site and it isn't asked there again for two minutes. Nothing is filled in or offered for saving in private or Tor tabs. A card number stays sealed, even from the page's own process, until you give your primary password again to fill it (that holds for a few minutes).
- **Two-factor codes.** Add a site's setup key (or its `otpauth://` link) to its saved sign-in, and the vault makes its six-digit codes, as an authenticator app does. They're offered under the site's code field, and in its right-click menu; the Passwords page shows the current one and how long it's good for, never the key. The key is sealed in the vault with the rest.
- **A warning when a saved password goes to the wrong site.** Type or paste a password you saved for one site into another (a fake sign-in page pretending to be Google, say) and it's taken out of the field, with a warning that the page may be pretending to be that site. It catches fake pages no list knows of yet, works while your passwords are locked, and sends nothing anywhere: it compares scrambled fingerprints of your saved passwords, kept under a key Windows seals for your account. "It's mine here too" puts the password back and stops warning about it on that site.
- **The Passwords page**: see, copy, change, generate, add and delete passwords. Copied passwords and usernames are kept out of Windows' clipboard history and cloud clipboard, and a copied password is cleared after a minute. Addresses and cards work the same, and a card's full number shows only after your primary password. There's also a checkup of weak and reused passwords, the vault's settings, encrypted backups and restoring them, importing a CSV file from Chrome, Edge and others, exporting to CSV (asks for your primary password every time), and clearing it all (asks for your primary password, then for you to type CLEAR).

### Everyday browsing

- **The address bar** shows the site with its host standing out. As you type, it suggests searches from your search engine (Google, Bing, DuckDuckGo or Brave Search), your bookmarks and your history. Suggestions from the search engine aren't asked for in private or Tor tabs. A star bookmarks the page (Ctrl+D).
- **The site menu**, in the address bar: the connection's security; what the site may do (camera, microphone, location, notifications, MIDI devices, virtual reality, autoplay, storage); pop-ups and redirects; whether it may ask before you leave; its shields and how many they blocked; blocking an element on the page; its cookies and data; and its zoom. Blocked pop-ups are offered from the address bar.
- **Sites' questions** (a site asking for your location, camera and so on) and pages' alerts and sign-ins appear in the browser's own prompt. Alt+Shift+A answers the waiting one. A camera, microphone or speakers come with the choice of which, the default already chosen. Closing a question just turns the site down this once.
- **Pop-ups are Mosaic Browser windows too.** A site's pop-up (a "Sign in with Google" window, say) has the browser's own title bar and a slim toolbar: its address (not for typing over), back, forward, reload and the site menu, at the size the site asked for. New tabs and links from it open in your main window.
- **Google's sign-in prompt** on a dark site (X, for one) sits on the page as it does in Chrome, not in a white box.
- **The new tab page**: your shortcuts (drag them into order; undo a removal), your saved splits, and a background picture of your own (from a file or a link), with blur and frosted panels. Each shortcut shows its site's own large icon where the site offers one, fetched from the site itself without your cookies; in Customize, line your shortcuts up to the left, in the middle or to the right, and choose the most in a row. Typing there goes straight into the address bar.
- **Sharing your screen**: windows and screens are shown as pictures, each on its own tab, and the one you choose plays live before you share it, with a warning for a whole screen or a Mosaic Browser window. While you share, a small bar stays on top of everything: what's shared and with which site (click to go back to that tab), Stop sharing, and Hide.
- **History** (Ctrl+H): the pages you visited, by day, searchable, each removable, with what you closed lately and your saved sessions at the top. Clear browsing data by time range: history, downloads, cookies and site data, cache.
- **Tools**: screenshots (Ctrl+Shift+S: an area you drag out, the visible part, or the whole page, copied or saved), reader view (F9, its button in the address bar for a page that can be read so), page translation (on your computer, its button in the address bar for a page in another language), the page's source (Ctrl+U), and a task manager (memory and processor use of each tab).
- **Spell check** as you type, in the languages you choose (Settings > Languages), with Mozilla's dictionaries to add. Right-click a text box for suggestions, to turn it off there, or to choose a site's languages. Checking happens on your computer.
- **Downloads** (Ctrl+J): the downloads button shows progress, and its list and the downloads page let you open, show in folder, copy the address, retry, keep or discard a held-back file, and delete. Quitting while anything's still downloading asks first.
- **Torrents**, among the same downloads: click a magnet link or download a `.torrent` file. A torrent with several files asks which ones you want first, with their sizes and where they go. Its row has its speeds, time left and peers, with pause, resume and Stop seeding; on the downloads page its details show the rest (what you've shared, availability, pieces, its trackers) and each file's progress, which you can still tick or untick. Every torrent asks before it starts. Torrents are downloaded by Transmission, which ships with the browser, and never from private or Tor tabs: everyone sharing a torrent can see your IP address, even through Tor.
- **Bookmarks** in the sidebar, in folders (Ctrl+Shift+O). Export them to an HTML file any browser can open, and import one (adding to yours, not replacing them).
- **Extensions** from addons.mozilla.org, with a button of their own beside the address bar. Pin any to the toolbar or into the address bar, with its icon, badge and popup. For each one, choose whether it may run in private tabs, Tor tabs and sandboxes; by default it's kept out of private and Tor tabs. The extensions page (Ctrl+Shift+A) turns them on and off, sets their permissions, options, updates and keyboard shortcuts, and installs from a file.
- **Zoom per site**, from 25% to 500%. Also find in page, print and developer tools.
- **Clear error pages**: why a page couldn't load, a warning before an http site, a dangerous one or one your filter lists say not to open, and a page for a tab whose page crashed. Reload tries again.
- **The welcome tour** on first start: what the browser does, a step at a time, with importing bookmarks, history, passwords and cards from Chrome, Edge, Brave, Opera, Vivaldi and others on the same computer. It's in the command palette ("Welcome") to see again.

### Settings

- **Appearance**: light, dark or follow Windows, and an accent colour (ours, Windows' own, or any you pick).
- **On startup**: continue where you left off (tabs load when you go to them) or start with a new tab page. Make it your default browser.
- **Address bar and search**: the search engine, and search suggestions.
- **Toolbar**: always show the downloads button, and drag the toolbar's buttons into the order you like.
- **Tabs and panes**: sleeping tabs and when they hibernate and sleep, how far the mouse wheel turns a tab's volume, scrollable tabs in split panes, and video sandboxing by default in split tabs.
- **Sidebar**: its side, pinning, hiding, showing at the window's edge, its button in a split's corner, and which panels it has.
- **Custom panels**: your own sidebar panels, each with its name, icon, how it runs, and its HTML, CSS and JavaScript to edit.
- **Keyboard shortcuts**: every command and its keys, each to change (click it and press new keys), add to, take away or put back.
- **Privacy and security**: clearing browsing data, shields, always using secure connections, fingerprinting protection (Standard or Strict), and secure DNS.
- **Ad blocking**: shields on or off, the filter lists and their updates, lists you've added, and your own filters.
- **Site settings**: each site you've changed something for, with its cookies to see and delete.
- **Languages**: spell check and its languages.
- **Downloads**: where they go, or ask each time; and for torrents, how long to keep sharing once one's downloaded (until as much is shared as downloaded, not at all, or until you stop it), and download and upload speed limits.
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
| Ctrl+Shift+T | Reopen closed tab (or window) |
| Ctrl+1 to Ctrl+8, Ctrl+9 | Go to tab 1 to 8, the last tab |
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
| Ctrl+Shift+S | Screenshot |
| F9 | Reader view |
| Ctrl+U | View page source |
| Ctrl+P | Print |
| F12, Ctrl+Shift+I | Developer tools |
| Ctrl+Shift+Q | Exit |

## Installing

Download `mosaic-browser-<firefox version>.en-US.win64.installer.exe` from the latest release and run it. The installer isn't code-signed yet, so Windows SmartScreen says it "protected your PC": choose **More info**, then **Run anyway**. It loads Windows' own system files only from Windows' folder, so a file a site left in your Downloads folder can't slip in when you run it from there.

Then **Install**. It installs as **Mosaic Browser** in `C:\Program Files\Mosaic Browser`, with a Start menu entry, a desktop shortcut, a taskbar pin and an uninstaller; **Options** lets you choose another folder, and leave out the shortcut or the pin. Installing in Program Files needs an administrator's permission, which Windows asks for. When it's done, **Open Mosaic Browser**.

Run over a copy that's installed already, it offers **Update** instead, and keeps your profile: tabs, passwords and settings. A copy installed as Project B is updated where it is, and its shortcuts take the new name.

## Uninstalling

Uninstall from Windows' Installed apps. Mosaic Browser's own uninstaller removes the program and its shortcuts. Turn on **Also delete my data** to delete everything Mosaic Browser keeps on this computer as well: history, saved passwords and cards, bookmarks, cookies, sandboxes, Tor's data, your torrents' list and progress, settings and the Windows Hello key. Your downloaded files stay, and another Firefox on the same computer is never touched. Left off, your data is kept for when you install again.

## Checking the download

Each release has a `SHA256SUMS` file. In a terminal, in the folder you downloaded to:

```
certutil -hashfile mosaic-browser-159.0.en-US.win64.installer.exe SHA256
```

The result should match the installer's line in `SHA256SUMS`. From 0.5.1 on, `SHA256SUMS.sig` is its signature, made with the project's own key; the browser checks it itself before it updates.

## Updates

Mosaic Browser looks for a newer release here once a day (Settings > About > Check for updates, to look now). From 0.5.1 on, it takes a release only if its `SHA256SUMS` is signed with the project's key, for that very version, so no one else can put out an update even if they got into this GitHub account. It downloads the new installer and checks it against that release's `SHA256SUMS`. When you choose **Install and restart**, it closes, the installer puts the new version in place with its progress showing, and Mosaic Browser starts again.

## Known limits

- Features new in 0.5.1 (custom panels, workspaces, video sandboxing, your own filter lists and filters, blocking an element, two-factor codes, saved sessions and the rest in its notes) aren't fully tested yet.
- Windows only, 64-bit.
- Not code-signed yet (see Installing).
- Tor tabs send everything through Tor, but to a site they look like Firefox on Windows, not like Tor Browser.
- The camera question doesn't show a live preview of the camera yet.

## Licenses

Mosaic Browser's own code is under the Mozilla Public License 2.0. It's built on [Firefox](https://www.firefox.com/) (Mozilla Public License 2.0), whose source is at [github.com/mozilla-firefox/firefox](https://github.com/mozilla-firefox/firefox). It includes the Tor Project's `tor.exe`, unchanged (GNU GPL 3.0; its source is at [dist.torproject.org](https://dist.torproject.org/)). It also includes Transmission's `transmission-daemon.exe`, unchanged (GNU GPL; its source is at [github.com/transmission/transmission](https://github.com/transmission/transmission)), with the libraries it needs: curl (curl license), OpenSSL (Apache License 2.0) and zlib (zlib license). The installer's `tor\docs` and `transmission\docs` folders hold their licenses and where their source is.
